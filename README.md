# openclaw-minimax-skills

> OpenClaw 一人公司 skill 集總覽 + 多模型用量統計 + 開發者模式入口
> 純前端 mint 主題 dashboard，零依賴，零月費，繁中友善

## Live Demo

- **GitHub Pages**（待啟用）：`https://openclawsean024-create.github.io/openclaw-minimax-skills/`
- **Vercel**（既有）：`https://openclaw-minimax-s.vercel.app/`

## 規格書

完整 v3.0.2 規格書見 [`PRD/SPEC.md`](./PRD/SPEC.md)（9 章 + Definition of Done + 部署契約）

## 變更日誌

[`PRD/CHANGELOG.md`](./PRD/CHANGELOG.md)（v1.0 / v3.0.2）

## 7 個分頁

1. 🏠 **首頁** — KPI（12,847 calls / 3 models / $48.20）+ 快速操作 + 本月行程
2. 💬 **對話** — AI 對話入口
3. 🛠️ **工具** — Skill 執行入口
4. 📚 **知識庫** — OpenClaw skill 樹 + 學習路徑
5. 📊 **用量統計** — GPT-4o / Claude / Gemini 多模型統一用量
6. ⚙️ **API 設定** — BYOK（OpenAI / Anthropic / Google）存 localStorage
7. ❓ **文件** — 學習路徑 / 命名規範 / 貢獻指南

## 部署

- 觸發：`push to main` → GHA `ci.yml` 跑 4 jobs（lint / test / build / deploy-to-Pages）
- 部署目標：**GitHub Pages**（純靜態，無 build step）
- 觸發分支：`main`

## 技術棧

- 純靜態 HTML（`dashboard.html` 14 KB）
- Tailwind CDN（無 build step）
- Noto Sans TC + JetBrains Mono 字型
- localStorage 持久化（API key / 偏好設定）
- 響應式（desktop sidebar + mobile bottom nav）
- WCAG 2.1 AA

## Source

Sean 10-repo-fleet Batch 8B (2026-09-07)
