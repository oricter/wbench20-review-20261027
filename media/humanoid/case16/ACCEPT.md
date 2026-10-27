# Case 16 acceptance

- humanoid asset: humanoid.uefn-mannequin YES (installed 0.1.3 catalog)
- createHumanoidWorld path: YES
- camera follow default: YES — humanoid.third-person preset, bound to hiker, immediate activation; distance/FOV tuned for the reference.
- locomotion default (walk/run clips): YES — SDK GASP/basic motion set and full default action controls retained.
- walk pose OK: YES — recorded W frames 30, 45 and 60 show changing knee bends, alternating forward/back leg swing and lifted feet, rather than rigid sliding.
- no projective textures: YES — solid materials, vertex colors and procedural sky only.
- clothing: solid meshes parented to the existing asset skeleton; mannequin retained with characterColor #5a6a5e.

PASS. Humanoid path and animated walking satisfy the required acceptance criteria.

Composition note: the centered rear camera, mountain silhouettes, lake reflections and forest retain the reference layout. Rendering is stylized, the backpack is oversized and obscures the head from behind, and some mannequin joints show through the simple clothing. Side capture confirms character and backpack volume. These are appearance limitations, not a locomotion failure.

Validation: compile_playable.sh built playable/compiled/entry-0.js. Required capture_gates_lane.sh 1 16 generated opening-gate.jpg and side-gate.jpg. Required record_motion_lane.sh 1 16 records the ?rec=1 WASD demo, including sustained W input; index.html retains window.__REC_DONE reporting.

Recording completed successfully: window.__REC_DONE.ok=true; motion-30fps.mp4 contains 457 frames at 30 fps (15.233 seconds). Both required gate and recording commands exited successfully.
