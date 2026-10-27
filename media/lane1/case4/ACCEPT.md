# Case 4 acceptance

Composition gate: PASS (round 1 of at most 8).

- Upper fill: official 0.3595, opening 0.3334; delta 0.0261 (limit 0.18).
- Horizon: official 0.3472, opening 0.35; delta 0.0028 (limit 0.06).
- Subject center delta: x 0.0, y 0.0194 (limit 0.08).
- Subject area relative delta: 0.0406 (limit 0.25).

Raised the six distant extruded glacier outlines by 3.8 times their previous height above their fixed bases. Glacier fronts remain 65–80 metres ahead. Camera remains centered at its existing low position with 44-degree FOV; orange flag remains on the right.

Norectex: YES. Solid, procedural, and vertex materials only; no projective reference textures added. Penguin mesh controller retained; no createHumanoidWorld.

Walkable snow: OK. A two-second W input moved the penguin 1.31 metres forward; it remained grounded and collided only with snowfield. Evidence: walk-check.json.

Shadows not required; shadow setup unchanged.

Validation: compile_playable.sh succeeded; capture_gates_xxk3.sh 1 4 succeeded; composition_gate.py passed. Opening and side captures are opening-gate.jpg and side-gate.jpg. record_motion.sh 4 produced motion-30fps.mp4: 457 frames, 30 fps, 15.233333 seconds, including W/S/A/D movement. Sampled recording frames contain rendered scene imagery.

Gate limitation: the supplied subject heuristic selected near-whole-frame bounding boxes, so its subject metrics do not establish exact silhouette agreement. The opening capture was also visually inspected. The enlarged glacier band is taller than the official silhouettes, as requested to meet the upper-fill target; this is a gate PASS, not pixel-exact equivalence.

Only case 4 was edited; preview-at and other cases were not modified.
