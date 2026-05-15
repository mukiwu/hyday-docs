---
locale: zh-TW
category: troubleshooting
slug: folder-not-loading
source: src/content/docs/zh-TW/troubleshooting/folder-not-loading.tsx
---
> *若開啟 Hyday 後畫面一直停留在載入中的狀態，或發現側邊欄內容完全空白，請參考以下步驟進行排除*

## 1. 確認資料夾路徑是否有效

應用程式紀錄的資料夾路徑可能因為資料夾被移動、改名，或存放在未連接的外接硬碟而失效

請按下`⌘`+`,`進入**設定**→**儲存空間**→ 點擊**變更資料夾**並選取正確路徑

![設定頁面中的資料管理分頁](https://hyday.tw/docs/screenshots/ui-settings-data-folder.png)

## 2. 確認檔案存取權限

在 macOS 系統中，初次開啟位於外接硬碟、iCloud 或隨身碟的資料夾時，系統會要求授予存取權限。若先前不慎點選了**不允許**，請至**系統設定 → 隱私權與安全性 → 檔案與資料夾**手動開啟 Hyday 的存取權限

## 3. 執行索引重建

若手動對資料夾結構進行了大變動 (例如透過`git pull`批次同步了大量檔案)，本機索引可能暫時未能同步更新

請開啟命令面板並搜尋執行**Rebuild folder index**指令

## 若上述步驟皆無效

1. 完全關閉 Hyday 應用程式
2. 前往筆記資料夾，將`.hyday/`子資料夾整個刪除 (系統將於下次啟動時自動完全重建)
3. 重新啟動 Hyday

> **⚠️ Warning**
> 此操作不會對筆記內容產生任何損害，所有的`.md`檔案皆會完整保留。索引資料純屬系統衍生的快取，可隨時安全重建

若完全重建後問題依舊，請前往[GitHub Issues](https://github.com/mukiwu/hyday/issues)提交回報，並請附上 Console 日記截圖與資料夾的大致檔案數量說明
