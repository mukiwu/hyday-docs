---
locale: zh-CN
category: guides
slug: use-command-palette
source: src/content/docs/zh-CN/guides/use-command-palette.tsx
---
> * Hyday 有提供命令面板，可让使用者无须离开键盘即可快速跳转至任何页面或执行各种功能指令 *

## 1. 核心快捷键对照

   功能用途 macOS Windows     **命令面板** (执行功能指令) `Cmd`+`Shift`+`P` `Ctrl`+`Shift`+`P`   **全域搜索** (寻找笔记与内容) `Cmd`+`K` `Ctrl`+`K`   

可将**命令面板**视为执行**动作**的窗口，而将**全域搜索**视为寻找**资料**的入口。两者相辅相成，分工明确。

![命令面板功能界面展示](https://hyday.tw/docs/screenshots/guides-use-command-palette-1.png)

## 2. 命令面板的主要功能范围

- **内容建立**：例如**建立新笔记**或**新增日记**
- **快速导航**：和 Hyday Agent 对话、跳转至日记、任务、白板、设置页面或垃圾桶

## 3. 全域搜索支援的检索对象

- 笔记标题与全文内容检索
- 标签名称 (Tags)
- 人事物 (Entities)
- 搭配 embedding 语意模型进行非关键字搜索

## 4. 编辑器内的触发机制

除了上述全域快捷键外，编辑器内也支援多种基于字元的快速触发：

- `/`：唤起斜线指令菜单。
- `[``[`：插入双向链接。
- `#`：标记标签。
- `@`：标记实体。

## 5. 一切功能的起点

若忘记某项功能的所在位置，最直觉的方式就是按下 `Cmd (Ctrl)`+`Shift`+`P` 并输入关键字，系统通常能立即找出对应的操作指令。
