# xxk-2 / Case 2 acceptance

Composition gate: **PASS** with the supplied `subject-mask.png`, using the unchanged shared `composition_gate.py`. Passed on camera iteration 4 of this fix.

- Subject center deltas: x 0.0133, y 0.0764 (limits 0.08).
- Subject area relative delta: 0.1756 (limit 0.25).
- Horizon delta: 0.0167 (limit 0.06); upper-fill delta: 0.0008 (limit 0.18).
- Final camera: position [0, 1.235, 6.0], look-at [0, 0.815, 0], FOV 44 degrees; follow distance 6.0 m, initial pitch 0.07 radians. Preserved opening and opening settle remain enabled.
- Rear opening visually checked: life-support backpack and US flag visible on back; no face or visor visible from this view.
- `createHumanoidWorld`, `humanoid.uefn-mannequin`, default SDK follow and default locomotion retained. Only camera configuration changed in source; compiled bundle refreshed.
- Forward route: continuous 300 m collision ground and a central rock-free corridor extending 60 m toward -Z. Recorded W movement traveled 12.469 m in 5 seconds; S 2.354 m, A and D 7.412 m each. Frames 60 and 70 show alternating leg poses with attached backpack and flag.
- Shadows were not acceptance criteria. Procedural materials and solid geometry retained.

Validation sequence completed: camera edit → compile_playable.sh → capture_gates_lane.sh 4 2 → composition_gate.py official-first-frame.jpg opening-gate.jpg COMPOSITION.json subject-mask.png → PASS → record_motion_lane.sh 4 2 → RECORD_OK.

Fresh motion: `motion-30fps.mp4`, 562 frames at 30 fps, 18.733 seconds. Telemetry: `MOTION_CHECKS.json`. Gate evidence: `opening-gate.jpg`, `side-gate.jpg`, `COMPOSITION.json`. Scope: xxk-2 only; no preview-at used.

The quantitative gate passes; the scene remains a stylized geometric rendering.
