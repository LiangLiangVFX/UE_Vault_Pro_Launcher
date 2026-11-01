<div align="center">

# ⚡ UE VAULT PRO (v1.1.0 Flagship)

**专为虚幻引擎 5 (Unreal Engine 5) 技术美术 (TA)、关卡设计师、VFX 视效师与游戏研发团队打造的次世代一站式工作站控制台**

*Next-Gen Unreal Engine 5 Project Hub · Digital Asset Vault · BlueprintUE Graph Workshop · R&D Knowledge Base*

[![Version](https://img.shields.io/badge/Release-v1.1.0_Flagship-00E5FF?style=for-the-badge)](https://github.com/LiangLiangVFX/UE_Vault_Pro/releases)
[![Unreal Engine](https://img.shields.io/badge/Unreal_Engine-5.0_~_5.7-F59E0B?style=for-the-badge)](https://www.unrealengine.com/)
[![Platform](https://img.shields.io/badge/Platform-Windows_10_/_11_(64--bit)-10B981?style=for-the-badge)](https://github.com/LiangLiangVFX/UE_Vault_Pro/releases)
[![Author](https://img.shields.io/badge/Author-LiangLiangArtist-A855F7?style=for-the-badge)](https://github.com/LiangLiangVFX)

</div>

---

## 📖 项目简介 (Introduction)

在日常 Unreal Engine 5 研发、LookDev 资产测试、VFX 调优与团队联调中，开发者往往面临 **多版本工程散落各盘、DDC/Intermediate 缓存吞噬数百 GB 磁盘空间、Fab 商城与网盘资产包难以预览检索、常用蓝图/材质节点难以跨项目复用、研发文档与工程脱节** 等核心痛点。

**UE Vault Pro** 是一款采用 **“暗物质与深空霓虹 (Dark Matter & Cyber Neon)”** 工业级视觉规范打造的 Windows 桌面端旗舰控制台。它将 **UE 工程版本纳管、高清实机媒体剧场、Fab 数字资产金库、BlueprintUE 交互式节点画布、Notion 研发知识库** 深度融于一体，提供毫秒级响应的次世代工作流体验。

---

## ✨ 四大核心工作台模块 (Core Modules)

### 1. 🏰 UE 工程管理中心 (Project Center)
* **智能 `.uproject` 深度解析**：支持拖拽或浏览导入工程，自动识别 **UE 引擎版本 (4.27 / 5.0 ~ 5.7)**、已启用插件列表 (`Plugins`)、C++/蓝图工程属性，并自动统计工程真实磁盘体积与可清理缓存体积。
* **版本控制与渲染管线体检 (`DefaultEngine.ini`)**：
  * 自动识别工程目录是否挂载 **`Git` / `Perforce (P4V)` / `SVN`** 版本控制并显示状态角标。
  * 自动检视 `Config/DefaultEngine.ini`，直观展示 **`DX12`、`Lumen GI`、`Lumen 反射`、`VSM 虚拟阴影`、`HWRT 硬件光追`、`Substrate 材质`** 等管线状态标签。
* **沉浸式剧场巨幕模式 (Theater Modal)**：双击任意工程卡片弹出 1280×820 全息环境光巨幕浮层，支持多张实机截图与 **MP4 / MOV / WebM 演示视频** 混排轮播、拖拽排序，所有媒体自动归档至工程专属 `_UEVault_Media` 目录。
* **工程缓存分项精准清理**：独立统计并支持勾选清理 **`DerivedDataCache` (DDC 着色器缓存)**、**`Intermediate` (编译中间产物)** 与 **`Saved/Logs & Crashes`**，提供快捷预设方案，释放数十 GB 空间且不误伤 C++ 编译环境。
* **高频研发快捷工具链**：
  * 🚀 **带参数一键唤醒引擎**：支持配置 `-game -ResX=1920 -ResY=1080 -log -dx12` 等附加启动参数。
  * 💻 **一键生成 VS 解决方案 (`.sln`)**：直接调用对应版本引擎的 `UnrealBuildTool.exe` 生成项目文件。
  * 🔌 **插件打包编译助手 (`BuildPlugin`)**：自动扫描工程内 `.uplugin` 文件，一键调用 `RunUAT.bat BuildPlugin -Rocket` 完成跨引擎版本插件编译与打包分发。
  * 📄 **崩溃日志秒查**：一键定位并打开 `Saved/Logs` 下最新生成的 `.log` 运行日志或 Crash 转储目录。

---

### 2. 📦 UE 数字资产金库 (Digital Asset Vault)
* **压缩包与文件夹混合纳管**：支持 `.zip`、`.7z`、`.rar`、`.uasset` 压缩包与已解压资产文件夹直接入库，支持批量扫描 `Epic VaultCache`、百度网盘或本地资产目录，并内置跨格式防重复入库校验。
* **内置 Chromium 引擎一键抓取 Fab 商城原图与描述**：
  * 粘贴任意 Fab 商城链接，无需安装任何外部插件，自动提取商城 **1920P 高清轮播原图集** 并持久化下载至该资产专属的 `_PreviewMedia` 文件夹。
  * **内嵌多路神经网络 + 本地离线 AI 翻译 (`_AI_Models`)**：内置 UE5 技术美术专业术语词库校准（如 *Vertex-Painted* ➔ *顶点颜色绘制*、*Tiling Detail Materials* ➔ *无缝平铺细节材质*），支持一键中/英双语零延迟切换。
* **超轻量级本地元数据存档 (`_vault_meta.json`)**：资产配置信息自动以 `< 0.5KB` 存档写入资产目录，删除重传或跨目录迁移后可瞬间自动恢复分类、来源、引擎版本、Fab 链接与中英文详情描述。
* **🚀 一键投送/迁移至指定 UE 工程 (`Deploy to Project`)**：支持将资产金库中的压缩包（自动后台异步解压）或文件夹一键投送至任意 UE 工程，智能嗅探并对齐 `Content/` 与 `Plugins/` 目录结构，确保 `/Game/` 引用路径 100% 完好不丢失材质。

---

### 3. 🕸️ BlueprintUE 蓝图与材质节点工坊 (Blueprint & Material Workshop)
* **T3D 剪贴板源码双向无损解析**：在 UE5 蓝图或材质编辑器中选中节点按 `Ctrl + C`，即可直接粘贴进工坊生成可视化节点连线画布；点击 **「一键复制还原回 UE5」** 后在引擎内按 `Ctrl + V` 即可 100% 还原所有节点与连接。
* **真实材质与蓝图节点名识别**：精准解析 `K2Node_Event`、`K2Node_CallFunction` 以及 `MaterialGraphNode`（如 `TextureSample`、`Lerp`、`ScalarParameter` 等），支持画布平滑缩放、自由拖拽节点并实时同步回写 `NodePosX / NodePosY` 坐标。
* **拓扑分层防堆叠自动排版 (Auto-Layout)**：一键根据引脚连线拓扑关系与动态引脚高度自动排列节点层级，彻底消除节点重叠。

---

### 4. 📘 研发知识库与 Notion 同步中心 (R&D Knowledge Base)
* **Notion 公开链接全文深度递归同步**：粘贴 Notion 分享链接，自动多轮递归拉取完整页面块树（标题、代码块、表格、Callout 提示框、待办清单与高清插图），自动转换为标准 Markdown 格式。
* **本地 Word (`.docx`) / HTML / Markdown 图文转换**：导入 `.docx` 文档时自动解压提取内嵌图片至 `_UEVault_DocsMedia`，保留原文档章节与表格结构。
* **内置 10 套大厂级研发标准模板**：涵盖 *Lumen & VSM 调优指南*、*GAS 战斗框架规范*、*PCG 大世界生态散射*、*Unreal Insights 性能剖析报告*、*MRQ 4K 影视渲染预设*、*PSO 预编译打包指南* 等，支持在**不覆盖原有正文**的前提下无损套用模板结构。
* **🔄 跨电脑知识资产同步 (`vault_knowledge_bp_sync.json`)**：支持一键导出或智能合并导入「蓝图节点图 + 研发笔记」轻量级数据包，轻松实现公司与家里多台电脑无缝协同。

---

## ⌨️ 全局快捷键一览 (Global Shortcuts)

> 💡 所有快捷键均可在 **「⚙️ 系统设置 ➔ 全局快捷键设置」** 中点击按键徽章自由录制修改或单独开关。

| 快捷键 | 功能说明 (中文) | Function (English) |
| :--- | :--- | :--- |
| **`F5`** | 触发全息激光扫描，平滑刷新全库工程与资产真实磁盘体积 | Rescan Disk Sizes & Media Vault |
| **`Ctrl + K`** | 快速聚焦顶部全局搜索框 | Focus Global Search Input |
| **`Ctrl + M`** | 一键解锁 / 锁定全局「管理模式」 | Toggle Admin / Read-Only Mode |
| **`Ctrl + L`** | 一键切换界面显示语言（🇨🇳 简体中文 / 🇺🇸 English） | Switch Interface Language (ZH / EN) |
| **`Ctrl + N`** | 快速呼出「导入/纳管新工程」弹窗 | Open Quick Import Project Modal |
| **`Ctrl + B`** | 快速折叠 / 展开左侧多功能导航栏 | Collapse / Expand Left Sidebar |
| **`Alt + Space`** | 呼出 / 隐藏主控制台窗口 | Show / Hide Main Window |

---

## 📥 下载与安装说明 (Download & Installation)

1. 前往本仓库右侧的 **[Releases 发布页面](https://github.com/LiangLiangVFX/UE_Vault_Pro/releases)**。
2. 下载最新版本的安装包 **`UE_Vault_Pro_Setup_v1.1.0.exe`**（或免安装便携版压缩包）。
3. 双击运行安装程序即可启动工作站；后续版本更新可直接点击软件内 **「⚙️ 系统设置 ➔ 关于软件与更新 ➔ 检测版本更新」** 在线检测并获取最新安装包。

---

## 📝 版本更新日志 (Changelog)

### 🎉 Release v1.1.0 Flagship (当前最新版本)
* **新增** 工程中心 `Git / P4V / SVN` 版本控制自动识别角标与 `Config/DefaultEngine.ini` 渲染管线自动体检标签。
* **新增** 工程崩溃日志秒查（一键打开最新 `.log`）与 `.uplugin` 插件自动化编译打包助手 (`RunUAT BuildPlugin`)。
* **新增** 资产金库「🚀 一键投送至工程」功能，支持压缩包自动解压与 `Content / Plugins` 目录深度对齐。
* **新增** 资产文件夹 `_vault_meta.json` 超轻量级配置存档与上次导入目录持久化记忆。
* **新增** 蓝图工坊与研发知识库跨电脑同步包 (`vault_knowledge_bp_sync.json`) 导出与智能无损合并导入。
* **新增** 内置 Chromium 引擎抓取 Fab 商城 1920P 高清原图集，以及 `_AI_Models` 本地离线神经网络翻译模型 + 多路云端神经网络并发翻译。
* **优化** 5 款高定多维光效主题（暗物质电光青、虚幻琥珀金、荒坂激光绯红、黑客矩阵翡翠、星云钛空紫）与中英双语 UI 100% 覆盖。

---

## 👨‍💻 作者与联系方式 (Author & Contact)

* **Author (作者)**：**LiangLiangArtist**
* **Email (邮箱)**：`liangliangvfx@gmail.com`
* **GitHub**：['https://github.com/LiangLiangVFX'](https://github.com/LiangLiangVFX)
* **YouTube**：['https://www.youtube.com/@zhaol2259'](https://www.youtube.com/@zhaol2259)
* **Bilibili (哔哩哔哩)**：['https://space.bilibili.com/75504176'](https://space.bilibili.com/75504176)
* **X (Twitter)**：['https://x.com/lemonzliang'](https://x.com/lemonzliang)

---

<div align="center">
  <sub>Copyright © 2026 LiangLiangArtist. Crafted with ❤️ for Unreal Engine 5 Developers & Technical Artists.</sub>
</div>