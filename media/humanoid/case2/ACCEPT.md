# Case 2 acceptance

- Composition gate: PASS, round 2 of 10; unmodified shared composition_gate.py.
- Key deltas: cx 0.0086; cy 0.0069; area relative 0.0521 (5.21%); horizon 0.0278; upper_fill 0.0008.
- Detected subject center: (0.4945, 0.4556), official (0.4859, 0.4486). Detected area: 0.0183, official 0.0193.
- Humanoid: YES — createHumanoidWorld and humanoid.uefn-mannequin retained.
- Camera: YES — default SDK follow, astronaut binding, preserve-opening, openingSettle enabled. Opening position [0, 1.26, 4.3], target [0, 0.916, 0], FOV 44 degrees; preset distance 4.3 m, pitch 0.08 radians.
- Locomotion: YES — default SDK locomotion and controls; no custom controlled body or fake walk. Frames 60 and 70 show alternating foot support and bent knees. Helmet, backpack, and US flag remain attached to animated bones.
- Walkable: OK — continuous 300 m ground collision; central rock-free corridor extends 60 m in both Z directions. W traveled 12.469 m in five seconds; S traveled 2.354 m, A and D each 7.412 m. The opening camera faces -Z, so W follows -Z toward the mountains; +Z is also clear.
- Shadows: not required; not used as acceptance criteria.
- No projective textures: procedural sky/ground and geometric rocks/mountains retained.

Validation: compile_playable.sh succeeded; capture_gates_lane.sh 4 2 succeeded; composition_gate.py returned PASS; record_motion_lane.sh 4 2 returned RECORD_OK. Motion is 562 frames at 30 fps (18.733 seconds). Position telemetry is in MOTION_CHECKS.json.

Artifacts: opening-gate.jpg, side-gate.jpg, COMPOSITION.json, motion-30fps.mp4.

The quantitative composition gate passes. The landscape and mannequin remain stylized, so this is not a photorealistic or pixel-exact reproduction of the reference.
