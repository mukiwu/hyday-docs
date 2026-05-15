---
locale: zh-TW
category: reference
slug: file-structure
source: src/content/docs/zh-TW/reference/file-structure.tsx
---
> *本指南詳述 Hyday 筆記資料夾的內部檔案佈局，並說明各檔案所扮演的角色*

## 典型的資料夾結構範例

```
``
```

## 主要內容檔案 (使用者可直接編輯)

副檔名功能用途`.md`筆記與日記核心，採用純 Markdown 格式搭配 YAML Frontmatter`.hyday/whiteboards-v2.json`所有視覺化白板的單一集中存檔，採標準 JSON 格式`.hyday/agent-conversations/v1.json`所有 AI 對話歷程的單一集中存檔，採標準 JSON 格式，完整記錄對話脈絡

## 索引系統

為了提供極速的搜尋與統計體驗，Hyday 會在`.hyday/`資料夾內建立影子索引檔

- **notes-index/v1**：儲存標題、首段摘要與元資料快照，加速列表渲染
- **tag-stats.json**：記錄標籤的出現次數與關聯性統計
- **lineage-cache.json**：緩存脈絡分析的運算結果，避免重複調用 AI

這些檔案具備**可重建性**：如果刪除`.hyday/`資料夾並重啟應用程式，系統會自動掃描整個筆記庫並完整重建索引

## 版本控制建議 (.gitignore)

`.hyday/`目錄下混合了兩類檔案：白板與 AI 對話是**使用者的真實內容**（建議納入版控），其餘檔案是**可重建的衍生快取**（建議排除）。`.gitignore`設定參考如下：

```
``
```

上面的寫法是「先忽略`.hyday/`第一層所有內容，再用`!`取消忽略白板與 AI 對話」。新增的索引檔預設會被忽略，若以後想保留其他檔案，再加一行`!.hyday/...`即可

## 系統偏好設定檔

Hyday 的全域設定（介面主題、過濾器組合、AI
        功能後端選擇等）**不存放在筆記資料夾中**，而是儲存於作業系統的應用程式支援路徑底下兩個檔案：

- `settings.json`：資料夾路徑等系統層設定
- `preferences.json`：UI 與功能偏好

實際位置：

- **macOS**：`~/Library/Application Support/Hyday/`
- **Windows**：`%APPDATA%\Hyday\`

> **ℹ️ Info**
> 登入 Hyday 後，介面主題、UI 語言、過濾器組合、AI 功能後端選擇、Lineage 權重、Tasks 與 Journal 視圖偏好等 27
>           項設定會自動同步到雲端，新裝置登入後可直接套用手動同步`settings.json`/`preferences.json`（例如放 iCloud +
>           symlink）依然可行，適合不想登入但需要跨機的使用者

## 大型筆記庫的效能表現

- **1,000 篇以下**：操作體驗流暢，檢索無延遲
- **1,000 至 10,000 篇**：首次掃描建立索引時較慢，建立完成後日常使用依然極速
- **超過 10,000 篇**：基於檔案系統效能考慮，建議將筆記拆分為多個獨立的 Hyday 資料夾管理
