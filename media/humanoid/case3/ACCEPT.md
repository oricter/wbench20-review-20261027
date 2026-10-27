# WBench case 3 — PASS

- humanoid asset: humanoid.uefn-mannequin YES
- camera follow default: YES — SDK setCameraFollow, humanoid.third-person preset, athlete binding, opening framing tuned to reference.
- locomotion default (walk/run clips): YES — createHumanoidWorld retains the bundled GASP/basic locomotion and full default action set; no custom animation or locomotion override.
- walk pose OK: YES — recorded held-W frames show alternating leg swing, knee flexion, raised feet, and forward progress. Frames 60 and 75 show opposite stride phases. The side gate shows the solid skinned character volume.
- createHumanoidWorld path: YES.
- projective textures / photo sampling: NONE. Landscape uses solid/procedural materials; character textures are disabled.
- Appearance: original skinned mannequin retained, base characterColor #1a2744, with bone-parented solid shirt, shorts, skin surfaces, calf sleeves, hair, and orange-accent shoes.

Validation: compile_playable.sh built playable/compiled/entry-0.js. Required capture_gates_lane.sh 1 3 and record_motion_lane.sh 1 3 were run. Opening and side screenshots are opening-gate.jpg and side-gate.jpg. The autodemo holds W for 300 frames, then demonstrates lateral walking, and reports window.__REC_DONE. Recording completed successfully: motion-30fps.mp4, 436 frames at 30 fps (14.53 seconds), __REC_DONE.ok=true.

Composition note: stadium, scoreboard, lane markings, and hurdles retain the reference framing. Athlete proportions, clothing, and stadium surfaces are stylized; the opening is not an exact photographic match. Hurdles are visual props; automatic hurdle-specific jumping is not implemented. SDK action controls remain available.

PASS is based on the required asset path, verified animated walking, and absence of projective textures.
