# WBench case 20 — PASS

- humanoid asset: humanoid.uefn-mannequin YES (catalog version 0.1.3)
- createHumanoidWorld path: YES
- camera follow default: YES — woman binding, humanoid.third-person preset, opening framing override
- locomotion default (walk/run clips): YES — SDK default locomotion and asset action set retained
- walk pose OK: YES
- projective textures / photo sampling: NO
- old hand-built controlled body / custom animate(): REMOVED

The skinned asset remains the controlled body. White blouse, beige trouser segments, skin accents and hair bun are solid meshes parented to the asset's bones. The map supplies physical ground and veranda support. WASD and the full SDK humanoid controls remain enabled.

Validation: compile produced playable/compiled/entry-0.js. Both required gate captures were generated and visually inspected; side-gate.jpg shows a volumetric humanoid. The final recording's W-phase frames 40 and 50 show alternating bent legs, lifted feet and bone-following trousers rather than a rigid sliding pose. The recording hook holds W for 60 frames and sets window.__REC_DONE after finalization.

Composition note: PASS under the requested locomotion-first criterion. The garden, blouse, trousers, bun, warm light, rear camera and rightward shadow are approximated with geometry. Framing, garment shape, foliage and rock silhouettes do not exactly match the photographic reference.

Evidence: opening-gate.jpg, side-gate.jpg, motion-30fps.mp4, uploads/frames/f000040.jpg and uploads/frames/f000050.jpg.

Recording completed successfully: __REC_DONE.ok=true; 312 frames, 10.4 seconds, 30 fps. Both required gate and recording scripts exited successfully for the final build.
