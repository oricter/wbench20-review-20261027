# WBench case 21 — composition PASS

- composition gate: PASS, round 1, using the supplied unmodified composition_gate.py.
- Horizon: official 0.3222; opening 0.3194; delta 0.0028 (limit 0.06).
- Subject center deltas: x 0.0000, y 0.0194; relative area delta 0.0406; upper-fill delta 0.0163. All within gate thresholds.
- Detector limitation: subject bounding boxes cover nearly the full frame. This gate result verifies the requested measured horizon correction, but does not establish an exact subject silhouette or photographic match.
- Camera: initialPitchRadians 0.145; opening height 1.6 m; opening distance 3.0 m; look-at height 1.161926 m. preserve-opening, openingSettle and beach_man binding retained.
- humanoid: YES — createHumanoidWorld + humanoid.uefn-mannequin. Original skinned mannequin remains the controlled body; no hand-built controlled body introduced.
- camera default follow: YES — SDK setCameraFollow with humanoid.third-person preset.
- locomotion default: YES — existing SDK walking controls and animation retained.
- walkable boardwalk: OK — clear 2.34 m-wide deck extends ahead to the landing and sand; grass and railings remain beside the path. No blocking props added.
- shadows not required. No lighting or shadow tuning performed.
- no projective textures: YES — existing procedural/solid/vertex-color materials retained.

Validation: compile_playable.sh succeeded; capture_gates_xxk3.sh 3 21 produced opening-gate.jpg and side-gate.jpg; composition_gate.py returned exit 0. Changes are confined to case 21.

Motion recording: RECORD_OK; record_motion_lane.sh 3 21 completed with window.__REC_DONE.ok=true. motion-30fps.mp4 contains 341 frames at 30 fps (11.367 seconds), 11,690,427 bytes. Inspected frames 90 and 165 show animated walking along the deck and onward onto clear sand toward the ocean, confirming forward traversal.
