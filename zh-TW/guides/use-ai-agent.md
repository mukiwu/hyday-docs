---
locale: zh-TW
category: guides
slug: use-ai-agent
source: src/content/docs/zh-TW/guides/use-ai-agent.tsx
---
> *Hyday Agent 可以讀寫你的筆記、執行 skill、用互動 widget 回應、並透過 Buddy 累積對你的長期記憶，讓 AI 真的變成**了解你的協作者**，而不是每次都要從頭解釋一遍的陌生人*

## 1. 進入 Hyday Agent

點擊側邊欄的**Hyday Agent**進入對話頁面

![Hyday Agent 主介面：左側對話歷史、中間訊息流、右上模式切換](https://hyday.tw/docs/screenshots/guides-use-ai-agent-1.png)

## 2. Widget — 互動式回應

Hyday Agent 不只回傳純文字，它會根據任務性質呼叫**render_widget**工具，在對話中嵌入可互動的卡片。目前支援的 widget 類型：

- **note-list**：篩選結果以筆記清單呈現，可直接點擊跳轉
- **summary-card**：分段摘要，適合每日總結、健康檢查報告
- **tag-cloud**：標籤雲，展示頻率分佈與顏色標記
- **health-report**：筆記庫健檢報告，依嚴重度分類列出問題項目
- **connection-map**：兩則筆記的隱藏連結，附上「橋接概念」說明
- **action-buttons**：建議的下一步操作，點擊可導航、套用標籤、新增筆記或送出後續 prompt
- **option-compare**：「請你二選一」型的決策卡，並排呈現選項供比較

Widget 是 Agent 主動選用的，我們不需要在 prompt 裡指定要哪一種，AI 會依照任務性質自動挑合適的格式

## 3. 技能 (Skill) — 一鍵啟動的預設任務

Skill 是預先寫好的常用工作流，分為幾類：

- **內建 skill**：今日筆記摘要、發現筆記間的隱藏連結、筆記庫健康檢查、卡片組合成文章、筆記整理成白板
- **使用者 skill**：自行新增的個人化任務，最多 50 個，可隨時編輯 / 複製 / 匯出 / 刪除
- **CLI skill**：當後端為 Claude Code / Gemini CLI 等 CLI 訂閱時，CLI 本身的 skill 也會被列入選單
- **MCP**：透過 MCP 協定接入的外部工具

點擊**Hyday Agent 上方選單的「技能」按鈕**以集中管理 Skills，可重新排序、停用、或匯出分享給其他人

## 4. Buddy — 長期記憶與人格

Hyday 在 Agent 旁邊養著一隻**Buddy**，它是 Agent 的記憶層。Buddy 會在你與 Agent 互動的過程中，**定期反思**並把對你的長期觀察寫進四份檔案：

- **溝通風格**：你習慣的語氣、回應節奏、喜歡簡短還是詳細
- **偏好**：你關心的主題、討厭的東西、堅持的原則
- **反覆主題**：你經常思考、追蹤、糾結的主題
- **近期脈絡**：最近這段時間正在做的事、卡關的點

每次 Agent 回應時會自動把這些觀察當作背景注入，所以對話次數越多，**Agent 會越認識你**，不需要每次重新解釋你是誰、在做什麼

> **ℹ️ Info**
> 所有 Buddy 觀察都存在筆記資料夾的`.hyday/observations/`底下，是純 markdown 檔案。你可以直接打開檢視 Buddy 對你的理解，覺得不對也可以手動修改

## 5. 對話歷程的儲存位置

所有 Agent 對話集中儲存在筆記資料夾的`.hyday/agent-conversations/v1.json`，可隨資料夾一起備份或版本控制

## 典型應用場景

- **知識整理**：把 #靈感 標籤裡與產品設計相關的內容，整合成文章草稿
- **脈絡追蹤**：列出我最近 30 天有提到 @深度工作力 的所有段落
- **檔案維護**：建立一篇 type 為 card 的筆記，標題 X、內容 Y
- **深度分析**：對 #身心狀態 標籤做一次脈絡演化分析

## 延伸閱讀

- [Agent 工具清單](https://hyday.tw/docs/reference/agent-tools)：完整工具與權限說明
- [Hyday Channel](https://hyday.tw/docs/guides/hyday-channel)：把 Claude Code 接成即時協作夥伴
- [疑難排解：工具呼叫失敗](https://hyday.tw/docs/troubleshooting/agent-tool-failed)：常見錯誤對策
