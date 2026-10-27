# WBench case 21 — PASS

- humanoid asset: humanoid.uefn-mannequin YES
- camera follow default: YES — SDK setCameraFollow, humanoid.third-person preset, beach_man binding.
- locomotion default (walk/run clips): YES — createHumanoidWorld retains the installed GASP/basic motion set and default controls/action set.
- walk pose OK: YES — sampled W-phase recording frames 40 and 50 show alternating leg swing, knee bending and lifted feet, with corresponding arm motion; the body is not rigidly sliding.
- createHumanoidWorld path: YES. Original skinned mannequin remains the controlled body.
- no projective textures: YES. Landscape uses procedural/solid/vertex-color materials; character textures are disabled.
- clothing follows skeleton: YES — shirt, sleeves, shorts, hair and backpack are bone-parented; original skinned surfaces have joint-region colors.

Validation: compiled/entry-0.js builds; exact capture_gates_lane.sh 3 21 and record_motion_lane.sh 3 21 commands run. Opening and side gates show three-dimensional skinned volume. Recording holds W for 150 frames, with subsequent turning and forward movement. index.html preserves ?rec=1 upload/finalization and window.__REC_DONE hooks.

Composition note: rear camera, timber boardwalk, dune grass, ocean and sunset approximate the reference. Mannequin anatomy, rectangular backpack, vegetation and lighting are stylized; the opening is not a photographic match. This does not affect the verified humanoid locomotion path.

Recording result: RECORD_OK; window.__REC_DONE.ok=true; 341 frames, 30 fps, 11.367 seconds, motion-30fps.mp4 (12,247,845 bytes).
