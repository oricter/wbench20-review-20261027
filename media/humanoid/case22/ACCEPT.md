# Case 22 — PASS

- humanoid asset: humanoid.uefn-mannequin YES
- createHumanoidWorld path: YES
- camera follow default: YES — humanoid.third-person, immediate activation, target woman
- locomotion default (walk/run clips): YES — SDK GASP/basic locomotion and action set retained
- walk pose OK: YES — recorded W frames show knee bend, foot lift and changing leg swing; body is not translated as a rigid model
- original skinned mannequin retained: YES
- solid clothing parented to skeleton bones: YES
- projective textures / photo sampling: NO
- custom animate() fake walk / hand-built controlled body: NO

Validation: required compile command succeeded and produced playable/compiled/entry-0.js. Both required gate and motion commands were run successfully. opening-gate.jpg and side-gate.jpg were inspected; the side view shows a volumetric articulated humanoid. Recorded W frames 45 and 60 were inspected for changing stride poses. motion-30fps.mp4 contains 452 frames at 30 fps (15.067 seconds), covering W/A/S/D. Recorder returned __REC_DONE.ok=true.

Composition note: centered rear view, red jacket, blue jeans, white shoes, trees, right-side benches and skyline are present. Clothing and foliage are stylized; mannequin red patches remain visible around some joints/shoes, and skyline geometry is simplified. Composition is imperfect, but the required humanoid path and real skeletal locomotion pass.
