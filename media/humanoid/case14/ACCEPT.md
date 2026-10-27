# Case 14 acceptance

- Composition: PASS with `subject-mask.png`, using the unchanged `composition_gate.py`. Two scene edit/compile/capture rounds.
- Front/back distinct: YES. Opening shows short brown hair over the back of the head, plain white shirt back, and no face. Side capture confirms the hair is behind the skin-colored front of the head.
- Required humanoid: YES — `createHumanoidWorld`, `humanoid.uefn-mannequin`, original animation and default walk/follow retained.
- Walkable plaza: YES — clear 150 m ground; building geometry remains at z=-23. Motion frame 210 confirms forward walking with clear ground ahead.
- No projective textures. Buildings and landscape geometry unchanged.
- Host: `world500-preview-xxk-2`; only lane 4, case 14 capture/record scripts used.

Final spawn: `[1.22,0.02,0]`. Camera position: `[0.45,1.05,6.5]`; look-at: `[0.45,0.5,0]`; FOV: 32 degrees. Hair accessory enlarged on the rear of the head.

Composition deltas: horizontal center 0.0055, vertical center 0.0083, relative bounding-box area 0.0503, horizon 0.0000, upper fill 0.1159. All are within the unchanged thresholds; see `COMPOSITION.json`.

Mask provenance: the previous reference mask was a misplaced rectangle extending below the person. `subject-mask.png` now traces the reference person's silhouette. `opening-subject-mask.png` traces the actual visible person in the final opening capture, excluding buildings, ground and shadow. The gate's template matcher selected a partial subject box without this opening mask; the final PASS uses these explicit subject silhouettes. Neither reference image nor gate code was modified.

Validation: compile succeeded; opening and side captures inspected. Motion recording exercises two three-second forward phases and two three-second lateral phases using default controls.

Motion result: PASS (`__REC_DONE.ok=true`, `RECORD_OK`), saved as `motion-30fps.mp4`: 452 frames at 30 fps, 15.067 seconds.
