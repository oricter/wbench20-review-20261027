# WBench case 6 — PASS

- humanoid asset: humanoid.uefn-mannequin YES (installed 0.1.3 catalog)
- camera follow default: YES — SDK setCameraFollow, humanoid.third-person preset, target monk; opening framing tuned to reference.
- locomotion default (walk/run clips): YES — createHumanoidWorld with unmodified default locomotion and shipped GASP/basic action bindings.
- walk pose OK: YES — recorded W frames 35 and 45 show alternating lifted legs, knee flexion and arm swing; clothing follows the bone motion. No rigid-body sliding or custom walk animation.
- createHumanoidWorld path: YES. Old buildMonk, createWorld/addCharacter controller and fake animate function removed.
- no projective textures: YES. Solid materials and procedural paving only; no reference image sampling.
- clothing: maroon characterColor plus solid bone-attached torso, split leg garments, left sleeve, skin shells, yellow collar and handheld prayer wheel. Original skinned mannequin retained.

Validation: required compile command built playable/compiled/entry-0.js. Required capture_gates_lane.sh 2 6 produced opening-gate.jpg and side-gate.jpg; the side view shows the animated humanoid and clothing in volume. Required record_motion_lane.sh 2 6 uses the existing ?rec=1 keyboard demo and window.__REC_DONE completion hook.

Composition note: PASS under the humanoid/walk gate. Centered rear view, monastery wings, prayer flags, chorten and Himalayan silhouettes approximate the reference. Geometry, robe silhouette, lighting and surface detail remain stylized; distant geometric people were removed. This is not a photographic or exact composition match.

Recording completed successfully: window.__REC_DONE.ok=true, 457 frames, 30 fps, 15.23 seconds, saved as motion-30fps.mp4.
