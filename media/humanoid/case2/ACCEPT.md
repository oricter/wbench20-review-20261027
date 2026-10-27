# Case 2 acceptance — PASS

- humanoid asset: humanoid.uefn-mannequin YES
- createHumanoidWorld path: YES
- camera follow default: YES — humanoid.third-person preset, astronaut binding, preserved opening framing.
- locomotion default (walk/run clips): YES — SDK GASP/basic locomotion and full default action bindings retained.
- walk pose OK: YES — W sequence frames 60 and 70 show alternating raised feet, knee flexion, and opposite leg support; the character is not rigidly sliding.
- skinned humanoid volume: YES — side-gate.jpg shows articulated mannequin volume with bone-parented helmet and backpack.
- no projective textures: YES — procedural/solid/vertex-color landscape and solid clothing; no photo sampling.

Validation: compile_playable.sh successfully builds playable/compiled/entry-0.js. Both required gate and motion scripts were run with arguments `4 2`. Opening and side gates were inspected. The autodemo holds W for 150 frames and supports window.__REC_DONE.

Composition note: PASS under the requested humanoid/locomotion criteria. Opening is centered behind the astronaut toward the rust mountain range. Landscape is faceted/stylized, suit limbs are slimmer, and subject height is smaller than the official photograph. Default walk/run timing is retained rather than replacing it with custom low-gravity animation.

Artifacts: opening-gate.jpg, side-gate.jpg, motion-30fps.mp4 (562 frames at 30 fps, approximately 18.73 seconds).
