---
locale: zh-TW
category: troubleshooting
slug: agent-tool-failed
source: src/content/docs/zh-TW/troubleshooting/agent-tool-failed.tsx
---
> *若 AI Agent 在執行工具呼叫後跳出錯誤，或是陷入重複呼叫同一工具而無結果的無限循環，請參考以下排除方案*

## 1. 陷入 Widget 渲染重試循環

當 Agent 嘗試呼叫`render_widget`失敗時，偶爾會發生過度重試的情況。**症狀表現**：

- 對話視窗中不斷自動跳出新的、且呈現錯誤的 Widget 元件
- 對話歷程長度急遽增加，導致`.hyday/agent-conversations/v1.json`檔案異常變大並拖慢系統效能

**處理對策**：

1. 立即點擊對話介面右上角的**停止**按鈕強行中斷任務
2. 棄用當前對話，並開啟一段新對話
3. 若特定指令必然觸發此現象，請前往 GitHub 提交 Issue 並附上該 Widget 的內容格式範例

## 2. 服務商不支援工具呼叫

若 AI Agent 完全不執行任何工具，僅透過純文字描述其**想做的事**，通常代表選用的模型不支援 Function Calling 語法

請參考[AI 供應商對照表](/docs/reference/ai-providers)，確保已切換至具備代理能力的進階模型

## 3. 清理損壞的對話紀錄檔案

若某段對話檔案因先前的異常循環而導致開啟緩慢或卡死，建議將其徹底移除：

1. 於側邊欄對話列表中找到該問題對話
2. 點擊 「...」 選取**刪除對話**進行刪除
3. 從乾淨的狀態重新開始對話任務

> **⚠️ Warning**
> 清理對話紀錄僅會影響`.hyday/agent-conversations/v1.json`內被刪除的那段對話，**不會刪除或修改筆記原文內容**。但請注意，**刪除對話**是一項不可撤銷的操作，一旦執行即無法恢復。若內容極其重要，建議先備份對話檔
