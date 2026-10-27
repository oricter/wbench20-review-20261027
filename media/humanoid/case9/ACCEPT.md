# WBench case 9 — PASS

- humanoid asset: humanoid.uefn-mannequin YES
- createHumanoidWorld path: YES
- camera follow default: YES — humanoid.third-person preset, bound to toddler
- locomotion default (walk/run clips): YES — SDK GASP/basic locomotion and action set retained
- walk pose OK: YES — W capture frames 30, 45, and 60 show alternating legs, knee flexion, and lifted feet; no rigid sliding
- no projective textures: YES — solid and vertex-color landscape; model textures disabled
- clothing: red base and solid jacket, jeans, shoes, skin, and blue beanie meshes attached to skeleton bones; skinned asset retained

Validation: compiled/entry-0.js built successfully. Required gate command produced opening-gate.jpg and side-gate.jpg; both inspected. Required motion command completed with RECORD_OK and window.__REC_DONE.ok=true. motion-30fps.mp4 contains 502 frames at 30 fps (16.733 seconds, 960×540). The ?rec=1 demo includes sustained W, S, A, D, and camera orbit segments.

Composition note: the opening preserves the centered rear subject, winding autumn path, benches, and woodland framing. Geometry is stylized and the full-size mannequin proportions are retained, so the reference toddler and photographic detail are approximate. This does not affect the humanoid/locomotion PASS.
