# CHANGELOG · openclaw-minimax-skills

> 規格書版本演進：v1.0 (overnight validation) → v3.0.2 (fleet hardening)
> 完整規格書見 [`PRD/SPEC.md`](./SPEC.md)

---

## v3.0.2 · 2026-09-07 · fleet hardening (Batch 8B)

**Patch 性質**：補齊完整規格書 + 部署面 / CI 面 hardening。

### Added
- `PRD/SPEC.md` — 9 章 v3.0.2 規格書（首篇完整規格，原 repo 只有 README validation marker）
- `PRD/CHANGELOG.md` — 本檔案（v1.0 / v3.0.2 變更日誌）
- `.github/workflows/ci.yml` — 4-job CI（lint / test / build / deploy to GitHub Pages）

### Changed
- `README.md` — 補完整內容（從 79 bytes validation marker → 正式 README，含安裝 / 部署 / spec 連結）

### Validation
- `dashboard.html` 14 KB 純靜態 — mint 主題 + Tailwind CDN + 7 分頁 sidebar + 響應式
- 內部連結 / 外部連結：0 失效
- Pages 部署目標：靜態檔案直接 publish，無需 build step
- 觸發分支：`main`

### Spec 章節覆蓋
- §1 產品概述（問題 / 使用者 / 價值 / Non-Goals）
- §2 使用者場景與流程（mermaid + 5 場景表）
- §3 功能需求（10 個 FR，P0/P1/P2 分級）
- §4 Non-Functional Requirements（Performance / Security / Privacy / A11y / Browser）
- §5 技術架構（arch diagram + module map + 降級策略）
- §6 Definition of Done（7 個 checkbox）
- §7 部署契約（Pages + Vercel 雙軌）
- §8 Out of Scope（6 個不做項目）
- §9 變更日誌（本檔）

### Risk
- 預設分支若改為 `master`，需更新 `ci.yml` 觸發條件為 `[main, master]`
- v2 才接真實 LLM API（BYOK 存 localStorage）—— v1 為純 mock 數據
- Vercel 與 Pages 雙軌並行：URL 各自獨立，無衝突

---

## v1.0 · 2026-09-06 · overnight validation

OpenClaw Overnight Dev 標記此 repo 已觸達並通過驗證：
- 79 bytes README 標記
- `dashboard.html` 14 KB 純靜態（mint 主題 + 7 分頁 sidebar）
- Tailwind CDN + Noto Sans TC + JetBrains Mono 字型
- localStorage 持久化（API key 預留位）
- 響應式（desktop sidebar + mobile bottom nav）
