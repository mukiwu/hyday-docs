---
locale: zh-CN
category: troubleshooting
slug: folder-not-loading
source: src/content/docs/zh-CN/troubleshooting/folder-not-loading.tsx
---
> * 若打开 Hyday 后画面一直停留在加载中的状态，或发现侧边栏内容完全空白，请参考以下步骤进行排除 *

## 1. 确认文件夹路径是否有效

应用程序纪录的文件夹路径可能因为文件夹被移动、改名，或存放在未连接的外接硬盘而失效

请按下 `⌘` + `,` 进入**设置** → **储存空间** → 点击**变更文件夹**并选取正确路径

![设置页面中的资料管理分页](https://hyday.tw/docs/screenshots/ui-settings-data-folder.png)

## 2. 确认文件存取权限

在 macOS 系统中，初次打开位于外接硬盘、iCloud 或随身碟的文件夹时，系统会要求授予存取权限。若先前不慎点选了**不允许**，请至**系统设置 → 隐私权与安全性 → 文件与文件夹**手动打开 Hyday 的存取权限

## 3. 执行索引重建

若手动对文件夹结构进行了大变动 (例如透过 `git pull` 批次同步了大量文件)，本机索引可能暂时未能同步更新

请打开命令面板并搜索执行**Rebuild folder index**指令

## 若上述步骤皆无效

1. 完全关闭 Hyday 应用程序
2. 前往笔记文件夹，将 `.hyday/` 子文件夹整个删除 (系统将于下次启动时自动完全重建)
3. 重新启动 Hyday

> **⚠️ Warning**
>  此操作不会对笔记内容产生任何损害，所有的 `.md` 文件皆会完整保留。索引资料纯属系统衍生的缓存，可随时安全重建 

若完全重建后问题依旧，请前往 [GitHub Issues](https://github.com/mukiwu/hyday/issues) 提交回报，并请附上 Console 日记截图与文件夹的大致文件数量说明
