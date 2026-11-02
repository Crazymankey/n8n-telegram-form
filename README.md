# ⚡ 5-Min Setup: Webform to Telegram & Google Sheets Blueprint

這套藍圖能在 5 分鐘內架設完成：前端萬用表單 + Google 試算表歸檔 + Telegram 免費即時推播。

---

## 🚀 核心優勢 (Key Features)

- **零維護成本**：GitHub Pages (前端) + n8n + Google Sheets + Telegram。
- **全球時區對齊**：預設 Asia/Taipei (UTC+8) 時間戳記。
- **零成本推播**：採用 Telegram Bot API，完全免費且無發送上限。
- **精緻 HTML 排版**：視覺化訊息模組，無廣告頁腳。

---

## 🛠️ 5 分鐘快速設定指南 (Quick Start)

### 步驟 1：匯入 n8n 工作流
1. 登入 n8n，點擊右上角 `...` 選擇 **Import from File**。
2. 上傳 `n8n_telegram_form_blueprint.json`。

### 步驟 2：設定 Google Sheets 節點
1. 點開 `寫入表單` 節點。
2. 選擇你的 Google 帳號憑證並填入 **Document ID** 與 **Sheet Name**。

### 步驟 3：設定 Telegram Bot 節點
1. 在 Telegram 搜尋 `@BotFather` 建立機器人取得 Token。
2. 在 Telegram 搜尋 `@userinfobot` 取得你的 Chat ID。
3. 點開 `發送通知` 節點，填入你的 Chat ID。

### 步驟 4：連接前端 HTML 表單
1. 複製 n8n 中 `接收表單資料` (Webhook) 節點的 Production URL。
2. 開啟 `index.html`，將 `N8N_WEBHOOK_URL` 替換為你的 Webhook 網址。
3. 推送至 GitHub Pages 即完成部署！
