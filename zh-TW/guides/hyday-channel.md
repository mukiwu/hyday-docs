---
locale: zh-TW
category: guides
slug: hyday-channel
source: src/content/docs/zh-TW/guides/hyday-channel.tsx
---
> * Hyday Channel 把 Claude Code 變成你在 Hyday 旁邊的即時協作夥伴，透過雙向通訊，讓 Claude Code 主動感知你在筆記裡讀什麼、寫什麼、停在哪裡，並透過用 Hyday 的夥伴 (Buddy) 與你互動 *

## 為什麼需要 Channel？

一般的 AI Agent 是「你問它才答」的單向對話，而 Hyday Channel 是**雙向**的，這表示我們在筆記裡的閱讀與寫作行為會即時被 Claude Code 看到，它可以主動丟出觀察、提醒、或讓你選擇下一步要做什麼

例如：

- 你連續閱讀同一篇筆記 30 秒以上，Claude Code 會主動拉出相關的歷史筆記
- 你寫到一半停了 15 秒，Claude Code 可能會問「需要我幫你接下去嗎？」
- 你在處理一個棘手主題，Claude Code 可以用 Buddy 的記憶提醒你過去類似情境怎麼處理

## 運作原理

Channel 透過 **Hyday MCP (`@mukiwu/hyday-channel`)** 與 Claude Code 對接：MCP server 由 Claude Code 以子程序方式啟動，並在本機開一個輕量 HTTP 伺服器 (預設 port `8789`)。Hyday app 把事件 POST 過去、Claude Code 透過 MCP 的 reply 工具回送，整個通訊只在本機，**不經過任何雲端中繼**

- **Hyday → Claude Code**：閱讀、寫作、訊息等事件即時推送
- **Claude Code → Hyday**：回應透過 Buddy 的對話框呈現，並可附帶 widget

> **ℹ️ Info**
>  本機需有 Claude Code CLI (v2.1.80 以上) 並完成登入，加上 Bun 或 Node.js 18+；Hyday 端則需先孵化一隻 Buddy (在 Hyday Agent 頁面進行)，因為 Channel 的對話視窗綁在 Buddy 上 

## 1. 安裝 Hyday MCP

在你的 Hyday 筆記資料夾根目錄建立 `.mcp.json` 檔案，內容如下：

```
``
```

透過 Hyday MCP，Claude Code 可以：

- **即時接收 Hyday 推送的事件**：你正在閱讀哪篇筆記、停留多久、寫到什麼段落、傳了什麼訊息
- **回送訊息到 Buddy 對話氣泡**：透過內建的 `reply` 工具，把回覆 (支援 markdown、清單、表格、程式碼區塊) 直接顯示在 Hyday 右下角
- **讀寫你的筆記資料夾**：因為 Claude Code 啟動時 `cd` 到筆記資料夾，可以直接讀、搜尋、新增、修改 markdown 檔案 (透過 Claude Code 內建的檔案工具)
- **對你的筆記做深度任務**：歸納主題、找出被遺忘的關聯、產出摘要、針對你正在讀的內容提出洞察

第一次啟動時，MCP server 會自動產生一份 `CLAUDE.md` 描述筆記資料夾結構，讓 Claude 不必每次重新探索目錄

## 2. 啟動 Claude Code

切換到剛放 `.mcp.json` 的筆記資料夾，啟動 Claude Code：

```
``
```

Hyday 側邊欄的 Buddy 圖示會從「未連線」變成「已連線」，並隨 Claude Code 當下狀態顯示**閱讀中**、**寫作中**、**思考中**等提示

![Hyday 側邊欄顯示 Channel 已連線狀態，並有 Buddy 對話氣泡](https://hyday.tw/docs/screenshots/guides-hyday-channel-1.png)

## 3. 跟 Claude Code 對話

按下 **Cmd + Shift + B** 切換 Channel 對話氣泡，或點右側的 **Hyday Channel** 進入完整頁面。氣泡裡可以：

- 輸入文字、上傳圖片給 Claude Code
- 看到 Claude Code 主動丟出的觀察、widget、建議下一步

## 4. 隱私事件開關

並不是所有行為都要推給 Claude Code。在**設定 → AI → Channel**可以分項開關以下事件：

- **筆記閱讀**：停留在同一篇筆記 30 秒以上時的閱讀事件
- **日記閱讀**：停留在日記頁面的閱讀事件
- **寫作活動**：你停止打字 15 秒後的寫作事件 (含當前段落的內容差異)
- **聊天訊息**：你主動傳送的訊息

## 5. 跟 Hyday Agent 的差異

    Hyday Agent Hyday Channel     運作模式 你問才答的對話 雙向，AI 可主動發起   後端 API / CLI / Ollama 皆可 Claude Code (專屬)   感知能力 只看你送進來的 prompt 讀寫行為即時推送   適合情境 明確任務、執行 skill 長時間陪伴、即時建議   

> **ℹ️ Info**
>  Hyday Agent 跟 Channel 是兩條獨立的線路。可以一邊跑 Agent 處理明確任務、一邊讓 Channel 在背景觀察你的閱讀寫作流動，互不干擾 

## 常見問題

### 為什麼只支援 Claude Code？

Channel 需要 CLI 端能透過 MCP 協定**主動回傳訊息**並理解 Hyday 推送的事件結構，目前只有 Claude Code 的 development-channels 模式針對這套協定做了實作。未來不排除支援其他 CLI

### 連線斷掉怎麼辦？

當 Claude Code 結束或當機，Hyday 側邊欄會顯示「Channel 未連線」並提供「重新偵測」按鈕。Channel 服務也會每 30 秒自動重試一次，**不需要重啟 Hyday**

### 對話會被存到哪裡？

Channel 對話目前儲存在記憶體中，Hyday 重啟後會清空，這是設計上的取捨，讓 Channel 保留「即時對話」的性質。而 Buddy 的長期記憶會透過反思流程寫到 `.hyday/observations/`，讓重要的觀察不會遺失

## 延伸閱讀

- [Hyday Agent](https://hyday.tw/docs/guides/use-ai-agent)：理解 Agent、Skill、Widget、Buddy 的完整脈絡
- [設定 AI 供應商](https://hyday.tw/docs/guides/configure-ai-provider)：多個 AI 供應商的設定與介紹
