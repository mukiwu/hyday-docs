---
locale: zh-CN
category: reference
slug: privacy
source: src/content/docs/zh-CN/reference/privacy.tsx
---
<!-- UNCONVERTIBLE: Lock -->绝不上传

<!-- UNCONVERTIBLE: Cloud -->

> *Hyday 100% 承诺使用者所有的笔记专属于使用者自己，笔记内容只会储存在使用者自己的设备中，不会上传到 Hyday 的伺服器。云端同步仅限于少量的系统偏好与授权设置，下表详细说明系统中各类资料的流向*

## 资料分类与流向对照表

资料类别储存位置是否同步至云端？笔记原文内容指定的本机文件夹 (`.md`)<!-- UNCONVERTIBLE: LocalOnly -->日记纪录与生活点滴指定的本机文件夹 (`.md`)<!-- UNCONVERTIBLE: LocalOnly -->视觉化白板数据本机文件夹`.hyday/whiteboards-v2.json`<!-- UNCONVERTIBLE: LocalOnly -->AI 代理对话历程本机文件夹`.hyday/agent-conversations/v1.json`<!-- UNCONVERTIBLE: LocalOnly -->标签、人事物统计与索引本机隐藏文件夹的缓存目录<!-- UNCONVERTIBLE: LocalOnly -->全域过滤器与钉选清单本机`preferences.json`<!-- UNCONVERTIBLE: LocalOnly -->帐号登录信息加密安全传输<!-- UNCONVERTIBLE: CloudSynced -->VVIP 订阅与支付状态加密数据库<!-- UNCONVERTIBLE: CloudSynced -->已授权的装置清单加密数据库<!-- UNCONVERTIBLE: CloudSynced -->首页卡片配置加密数据库<!-- UNCONVERTIBLE: CloudSynced -->电子报订阅偏好加密数据库<!-- UNCONVERTIBLE: CloudSynced -->

## 关于 AI 功能的隐私处理

启动 AI 相关功能 (如对话、Agent 代理、人格蒸馏或脉络分析) 时，相关的笔记片段会传送至选取的服务供应商：

- **云端供应商**(OpenAI / Claude / Gemini / OpenRouter 等)：资料处理受各公司的隐私政策规范。大多数供应商提供**不将 API 资料用于模型训练**的选项，请参阅官方文件
- **本机供应商**(Ollama)：所有的运算皆在电脑内部执行，资料绝不离开区域网络，且离线可用

> **⚠️ Warning**
> Hyday 无法控制选用的**云端供应商**如何存取伺服器上的资料。针对涉及高度敏感内容 (如商业机密、个人健康隐私或身分信息)，强烈建议选用本机执行的 Ollama 作为 AI 引擎

## 遥测与使用统计

Hyday 致力于无追踪体验，**不收集**任何关于使用者行为的遥测数据 (例如：点击了哪个按钮、打开了哪些笔记等)，仅在登录帐户时，系统会传送以下必要信息以确保功能运作：

- **应用程序版本号**：用于自动检查与提示更新
- **装置硬件信息**：包括作业系统与晶片类型，用于授权验证与相容性最佳化

## 帐号退出登录时的处理机制

当执行退出登录时：

- **本机的所有内容与设置皆会完整保留**
- 储存于云端 Firestore 的**首页配置**与**电子报订阅设置**会同步移除
- VVIP 授权记录依然安全储存于帐户中，下次重新登录后即可恢复

## 解除安装应用程序后的状态

- **笔记文件夹将完整保留**，可以随时使用任何第三方 Markdown 编辑器继续读取内容
- 本机的`preferences.json`设置档通常会保留在系统路径中，重新安装时可选择继承 (需手动)
- 云端纪录将继续保存，直至主动要求删除帐号为止

## 联系隐私团队

若对资料安全有任何疑问或疑虑，欢迎致信至`mukispace@gmail.com`。会在 7 个工作日内提供详细回复
