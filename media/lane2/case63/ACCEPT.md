# Case 63 — ACCEPTED (composition gate)

Round2 completed in six edit / lane2 compile / capture / masked gate iterations. The final COMPOSITION.json is PASS. The official-vs-official masked self-check also passes (logs/gate-self-check.json), superseding the previous detector-defect report. No gate code, thresholds, official image, or subject mask were edited.

Final metrics:
- Subject center delta: x 0.0016, y 0.0014 (limits 0.08).
- Subject area relative error: 0.1616 (limit 0.25).
- Horizon: official 0.4250, opening 0.4306; delta 0.0056 (limit 0.06).
- Upper-fill delta: 0.0460 (limit 0.18).

Changes: raised the rear doorway lintel and its steel flanges, moved FADED lettering above it, restored recessed left-bay steel shelf girders, added skylight bounce illumination, and adjusted rotor envelopes and motor height. The warehouse structure uses weathered steel with procedural materials and solid geometry; no photo or projective textures. Orange propellers and red rear LEDs retain the flying-away presentation. The opening camera is unchanged. All new structural pieces are outside the central flight aisle; the navigation support and controller remain unchanged.

Validation: lane2/tools/compile_playable.sh succeeded; capture_gates_port.sh 2 63 8563 produced fresh opening-gate.jpg and side-gate.jpg; the required command below returned exit 0:

```sh
python3 /tmp/humanoid-scripts/composition_gate.py official-first-frame.jpg opening-gate.jpg COMPOSITION.json subject-mask.png
```

Per-iteration gate reports are in logs/composition-round2-1.json through logs/composition-round2-6.json. The prior forward-flight check remains in logs/forward-check.log; forward flight was not retested this round. Existing motion videos predate these composition edits and were not regenerated. No preview-at or other case workspace was edited.

Acceptance is for the requested composition gate. The render remains a geometric approximation, not a photorealistic match; gray MAE is 43.53. The wide-subject detector clamps its estimated box using the mask hint, so its area result is not an independent silhouette measurement.
