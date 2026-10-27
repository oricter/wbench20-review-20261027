# Case 33 acceptance

Composition gate: **PASS**, round 1 of at most 8 (2026-10-27).

- Horizon: official 0.3528, opening 0.3889; delta **0.0361** ≤ 0.06.
- Subject center deltas: x 0.0, y 0.0194 (limit 0.08 each).
- Subject area relative delta: 0.0406 ≤ 0.25.
- Upper-fill delta: 0.0179 ≤ 0.18.
- NORECTEX: **YES**. Solid mesh materials and procedural grain; no projective textures. Runtime mesh inspection found zero texture maps.
- Walkable aisle: **OK**. A centered 2 m wide, 38 m long corridor has zero mesh blockers above the floor. Browser test walked forward 36 m; WASD roundtrip error was 0 m.
- First-person camera: position [0, 3.6, 22], pitch 0.235 radians, vertical FOV 46°. Altar distance and scene geometry retained.
- Shadows: **not required**.
- Build and opening/side captures: **PASS** using the requested scripts.

The supplied heuristic gate passes; this does not establish exact visual identity with the official photograph. Architecture, congregation and ornament remain simplified, and the gate's detected “horizon” is an image band rather than the geometric horizon.

Evidence: COMPOSITION.json, opening-gate.jpg, side-gate.jpg, logs/walkability.json.
