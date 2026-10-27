# 构图质检门禁（硬规则）

Hanna 2026-10-27：构图必须与官方首帧相同；颜色可近似；禁止投影贴图；人必须 createHumanoidWorld。

## 必过（任一不过 → FAIL，不得标 PASS）
1. **主体剪影位置**：人物/主体在画面中的 bbox 中心与官方首帧偏差 ≤ 8% 画幅（宽/高各自）。
2. **主体尺度**：主体 bbox 面积相对官方偏差 ≤ 25%。
3. **地平线/主水平线**：若官方有清晰地平线或地面交界，开场帧同位置垂直偏差 ≤ 6% 画高。
4. **关键道具相对位**：题面点名的关键物（旗/冰山/亭/石灯笼/栏杆等）相对主体的左右与前后关系不得颠倒；显著错位 → FAIL。
5. **相机俯仰**：开场不得明显比官方更俯视/更仰视（主观+侧景辅助）；人形第三人称跟随后仍须把 opening framing 调到与官方一致。
6. **可通行空间**：人物周围/前方必须有可走的地面（WASD 能真正迈步前进）；禁止用石头/栏杆把人堵死或把可走区域填满。
7. **禁止**：为「好看」改摆位；用投影贴图凑像；手搓几何人。

## 不做 / 非验收项
- **影子可不还原**：不要为对齐官方去补/追长影、光影方向；影子不是验收项。

## 允许
- 颜色/材质 stylized；表面不完全照片级。
- 人形骨架外观块状（uefn-mannequin）——但站位与镜头必须对齐。
- 光照/影子与官方不同（只要构图与可走空间达标）。

## 产物
每题必须产出：
- `opening-gate.jpg`（开场）
- `COMPOSITION.json`（数值门禁结果）
- `ACCEPT.md` 中单独一行：`composition gate: PASS|FAIL` + 原因

## Hanna 追加（2026-10-27 晚）
- **正背面明显区分**：人物正面与背面必须一眼可辨（脸/发型/衣襟前后）；禁止前后对称糊成一样。背影题必须是明确背影。


## 强制重跑（Hanna 2026-10-27 夜 · 统一，不单题）

**任何改 camera / opening / 重录 motion / 改 playable 机位之后，必须对着「当前 opening + official」重跑 `composition_gate.py`，用新 JSON 更新验收页徽章。禁止沿用旧 PASS 徽章或旧数值。**

- 开场锁定（OPENING_LOCK mae≤8）与构图门禁是两道独立门禁；开场锁定 PASS ≠ 构图 PASS。
- 改机位只修了 opening-lock 却不重跑构图 → 视为假 PASS（#3 已实锤：徽章 cxΔ=0.007 为旧数，现跑无 mask cxΔ=0.088 FAIL / 有 mask area_rel=0.369 FAIL）。
- 验收页徽章只能来自本轮 gate JSON；手工抄旧表禁止。
- 全量核验：Pages/仓内现 opening+official 对 20 题重跑，产出 TSV；徽章 PASS 但现跑 FAIL 的一并改 FAIL 并入修复队列。

## Opening lock (universal, not per-case)

视频首帧必须 = opening-gate。见同目录 `OPENING_LOCK_RULE.md`。
- shared `record_motion_lane.sh`：settle → upload_opening → OPEN_HOLD → WASD；录完自动写 `OPENING_LOCK.txt`（mae）。
- shared `capture_gates_lane.sh`：mae≤8 时不覆盖 opening-gate。
- 改 camera/main 后必须 `compile_playable.sh`。
- 新录任何题都走上述 shared 脚本，禁止旁路单题特判。

## Detector note (2026-10-27 21:48)
Standing-person color-match: when the first CC is too wide (dark seats/shadows glued to subject), re-run CC in a narrow column around the official mask hint (`half_w ≈ 0.55 * hint_w`) and drop pixels below official feet. Heuristic over-seg clamp multipliers tightened to 1.08× so fallback can still satisfy `area_rel≤0.25`. Re-run all openings after this change.
