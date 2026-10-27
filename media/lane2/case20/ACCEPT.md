# WBench case 20

- composition gate: PASS
- humanoid/camera/locomotion YES: createHumanoidWorld, humanoid.uefn-mannequin, default camera follow bound to woman, and default SDK walk locomotion retained.
- dressWoman bone clothing retained; no hand-built controlled body.
- walkable space OK: continuous 36 × 36 meter ground; clear forward gravel corridor, right-side rocks, and no added blocking collision boxes in the walking path.
- shadows not required; no sun or shadow tuning performed.
- No projective textures.

Opening camera: height 1.42 meters, distance 2.8 meters, pitch approximately 0.10 radians, FOV 36 degrees. Preserve-opening and openingSettle remain enabled. Spawn is left of center. Fence height is 1.8 meters, with its visible top near 31% of frame height. Lantern remains left, rock group right, and stepping stones lower-left. Removed a rear slab whose ground projection crossed the camera horizon.

Validation: compilation and gate capture succeeded. The final COMPOSITION.json reports PASS: subject center deltas x=0.0016, y=0.0181; subject area relative delta=0.1957; horizon delta=0.0167. Two capture rounds were used, including the slab correction. This is a pass against the supplied heuristic thresholds, not a claim of pixel-exact photographic reproduction; geometry and clothing remain stylized.

Motion: final-build W-phase frames f000024.jpg, f000040.jpg, and f000050.jpg show forward progress relative to the garden, alternating bent legs, and arm swing. The recording uses the SDK keyboard controls and default animation clips, with 60 frames of W input.

Evidence: opening-gate.jpg, side-gate.jpg, COMPOSITION.json, and uploads/frames/f000040.jpg and f000050.jpg.

Final recording completed successfully: __REC_DONE.ok=true, RECORD_OK, 312 frames, 10.4 seconds at 30 fps. Video: motion-30fps.mp4. Compile, final capture, composition gate, and recording all exited successfully. world500-preview-at was not touched.
