# Case 14 acceptance — PASS

- humanoid asset: humanoid.uefn-mannequin YES (0.1.3)
- createHumanoidWorld path: YES
- camera follow default: YES — setCameraFollow, humanoid.third-person preset, man binding.
- locomotion default (walk/run clips): YES — SDK GASP/basic motions and full default action set retained.
- walk pose OK: YES — W frames show alternating leg swing, bent knees, lifted feet and arm swing. No rigid sliding body.
- no projective textures: YES — solid materials, vertex tints and procedural plaza/sky; no reference sampling.
- original skinned mannequin retained: YES — solid clothing/skin accessories parented to asset bones.

PASS: correct humanoid path, animated walking and no projective textures.

Validation: required compile command built playable/compiled/entry-0.js. Required gate command produced opening-gate.jpg and side-gate.jpg. Required recording command produced motion-30fps.mp4: 452 frames, 30fps, 15.067 seconds; __REC_DONE.ok=true. W frames 45 and 60 were visually inspected for articulated leg poses. Side gate confirms humanoid volume.

Composition limitation: rear view, subject placement, plaza horizon, arched facades, white shirt, navy trousers and diagonal shadow approximate the reference. Mannequin proportions are broader; clothing, buildings and lighting remain stylized. Opening uses the asset idle pose; movement uses real clips.
