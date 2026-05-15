---
locale: zh-CN
category: reference
slug: file-structure
source: src/content/docs/zh-CN/reference/file-structure.tsx
---
> * 本指南详述 Hyday 笔记文件夹的内部文件布局，并说明各文件所扮演的角色 *

## 典型的文件夹结构范例

```
``
```

## 主要内容文件 (使用者可直接编辑)

   副档名 功能用途    `.md`笔记与日记核心，采用纯 Markdown 格式搭配 YAML Frontmatter `.hyday/whiteboards-v2.json`所有视觉化白板的单一集中存档，采标准 JSON 格式 `.hyday/agent-conversations/v1.json`所有 AI 对话历程的单一集中存档，采标准 JSON 格式，完整记录对话脉络  

## 索引系统

为了提供极速的搜索与统计体验，Hyday 会在 `.hyday/` 文件夹内建立影子索引档

- **notes-index/v1**：储存标题、首段摘要与元资料快照，加速列表渲染
- **tag-stats.json**：记录标签的出现次数与关联性统计
- **lineage-cache.json**：缓存脉络分析的运算结果，避免重复调用 AI

这些文件具备**可重建性**：如果删除 `.hyday/` 文件夹并重启应用程序，系统会自动扫描整个笔记库并完整重建索引

## 版本控制建议 (.gitignore)

`.hyday/` 目录下混合了两类文件：白板与 AI 对话是**使用者的真实内容**（建议纳入版控），其余文件是**可重建的衍生缓存**（建议排除）。`.gitignore` 设置参考如下：

```
``
```

上面的写法是「先忽略 `.hyday/` 第一层所有内容，再用 `!` 取消忽略白板与 AI 对话」。新增的索引档默认会被忽略，若以后想保留其他文件，再加一行 `!.hyday/...` 即可

## 系统偏好设置档

Hyday 的全域设置（界面主题、过滤器组合、AI 功能后端选择等）**不存放在笔记文件夹中**，而是储存于作业系统的应用程序支援路径底下两个文件：

- `settings.json`：文件夹路径等系统层设置
- `preferences.json`：UI 与功能偏好

实际位置：

- **macOS**：`~/Library/Application Support/Hyday/`
- **Windows**：`%APPDATA%\Hyday\`

> **ℹ️ Info**
>  登录 Hyday 后，界面主题、UI 语言、过滤器组合、AI 功能后端选择、Lineage 权重、Tasks 与 Journal 视图偏好等 27 项设置会自动同步到云端，新装置登录后可直接套用 手动同步 `settings.json` / `preferences.json`（例如放 iCloud + symlink）依然可行，适合不想登录但需要跨机的使用者 

## 大型笔记库的效能表现

- **1,000 篇以下**：操作体验流畅，检索无延迟
- **1,000 至 10,000 篇**：首次扫描建立索引时较慢，建立完成后日常使用依然极速
- **超过 10,000 篇**：基于文件系统效能考虑，建议将笔记拆分为多个独立的 Hyday 文件夹管理
