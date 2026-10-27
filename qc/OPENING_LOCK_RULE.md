# Humanoid opening-lock rule

**视频首帧 = 开场图** (Hanna 2026-10-27 #3)

1. `record_motion_lane.sh` / playable `?rec=1`: same settle -> `/__upload_opening` -> freeze `OPEN_HOLD` frames -> then WASD. No second settle before record.
2. After editing `camera.json` / `main.ts`, always `compile_playable.sh <playable>` (JSON is bundled into `entry-0.js`).
3. `capture_gates_lane.sh`: if `OPENING_LOCK.txt` exists with mae<=8, keep `opening-gate.jpg` and only refresh side.

4. **After any camera/opening/re-record change**: re-run `composition_gate.py` on current opening vs official and refresh the review-page composition badge from the new JSON. **Never keep an old composition PASS badge** after moving camera or re-recording. Opening-lock PASS does not imply composition PASS.
