<div align="center">

<img src="./docs/logo.png" width="112" alt="UE Vault Pro Logo" />

# ⚡ UE VAULT PRO (v1.1.0 Flagship)

**专为虚幻引擎 5 (Unreal Engine 5) 技术美术 (TA)、关卡设计师、VFX 视效师与游戏研发团队打造的次世代一站式工作站中枢**

*Next-Gen Unreal Engine 5 Project Hub · .uasset Dependency Migrator · Digital Asset Vault · BlueprintUE Workshop · R&D Knowledge Base*

[![Version](https://img.shields.io/badge/Release-v1.1.0_Flagship-00E5FF?style=for-the-badge)](https://github.com/LiangLiangVFX/UE_Vault_Pro_Launcher/releases)
[![Unreal Engine](https://img.shields.io/badge/Unreal_Engine-4.27_/_5.0_~_5.7-F59E0B?style=for-the-badge)](https://www.unrealengine.com/)
[![Platform](https://img.shields.io/badge/Platform-Windows_10_/_11_(64--bit)-10B981?style=for-the-badge)](https://github.com/LiangLiangVFX/UE_Vault_Pro_Launcher/releases)
[![Website](https://img.shields.io/badge/Official_Web-Interactive_Portal-3B82F6?style=for-the-badge)](https://liangliangvfx.github.io/UE_Vault_Pro_Launcher/)
[![Author](https://img.shields.io/badge/Author-LiangLiangArtist-A855F7?style=for-the-badge)](https://github.com/LiangLiangVFX)

</div>

---

## 📖 项目简介 (Introduction)

在日常 Unreal Engine 5 研发、LookDev 资产测试、VFX 调优与团队联调中，开发者往往面临 **多版本工程散落各盘、DDC/Intermediate 缓存吞噬数百 GB 磁盘空间、跨工程提取单个 `.uasset` 必须启动庞大编辑器否则丢失贴图材质引用、Fab 商城与网盘资产包难以预览检索、常用蓝图/材质节点难以跨项目复用** 等核心痛点。

**UE Vault Pro** 是一款采用 **“暗物质与深空霓虹 (Dark Matter & Cyber Neon)”** 工业级视觉规范打造的 Windows 桌面端旗舰工作站。它将 **UE 工程管理中枢、`.uasset` 依赖嗅探迁移、Crash 崩溃智能诊断、Fab 数字资产金库、BlueprintUE 交互式节点画布、Notion 研发知识库** 深度融于一体，提供毫秒级响应的次世代工作流体验。

---

## ✨ 四大核心工作台模块与工业级工具链 (Core Modules)

### 1. 🏰 UE 工程管理中心 (Project Hub)
* **智能 `.uproject` 深度解析与实时盘符同步**：支持拖拽或浏览导入工程，自动识别 **UE 引擎版本 (4.27 / 5.0 ~ 5.7)**、已启用插件列表 (`Plugins`)、C++/蓝图工程属性，自动同步磁盘存活状态与真实占用体积。
* **版本控制与渲染管线体检 (`DefaultEngine.ini`)**：
  * 自动识别工程目录是否挂载 **`Git` / `Perforce (P4V)` / `SVN`** 版本控制并显示状态角标。
  * 自动解析 `Config/DefaultEngine.ini`，直观展示 **`DX12`、`Lumen GI`、`Lumen 反射`、`VSM 虚拟阴影`、`HWRT 硬件光追`、`Substrate 材质`** 等管线标签。
* **🧬 `.uasset` 依赖关系深度嗅探与单资产无损迁移器 (Lossless Migrator)**：
  * **免启动 UE5 编辑器**：直接在客户端内选定任意 `.uasset` / `.umap` 文件，0.1 秒内递归解析二进制名字表中的 `/Game/...` 引用树。
  * **全链路防丢引用**：自动顺藤摸瓜找出关联的母材质、材质实例、纹理贴图、网格体及同目录 `.uexp / .ubulk` 数据体，保持 `Content/` 相对路径结构一键无损迁移至目标工程。
* **🩺 UE 崩溃日志 (`CrashContext`) 智能中文诊断卡**：
  * 一键扫描 `Saved/Crashes` 下最新的 `CrashContext.runtime-xml` 与运行日志尾部，自动匹配 **GPU Hang (D3D12 设备丢失)、C++ 空指针越界、蓝图无限递归死循环、着色器/DDC 缓存损坏、显存 OOM、模块版本失配** 等核心故障，给出中文定性结论、修复建议与关键堆栈一键复制。
* **沉浸式剧场巨幕模式 (Theater Modal)**：双击任意工程卡片弹出全息环境光巨幕浮层，支持多张实机截图与 **MP4 / MOV / WebM 演示视频** 混排轮播、拖拽排序，所有媒体自动归档至工程专属 `_UEVault_Media` 目录。
* **分项精准清理 & 多工程批量缓存清理 (Batch DDC Cleaner)**：独立统计并支持一键批量清理多个工程的 **`DerivedDataCache` (DDC)**、**`Intermediate`** 与 **`Saved/Logs & Crashes`**，轻松释放上百 GB 磁盘空间。
* **高频研发快捷工具链**：
  * 🚀 **带参数一键唤醒引擎 & 桌面快捷方式**：支持配置 `-game -ResX=1920 -ResY=1080 -log -dx12` 等启动参数，并支持一键在 Windows 桌面生成工程快捷方式 (`.lnk`)。
  * ⚡ **剔除缓存极速克隆 (`Clone`) & 瘦身打包归档 (`ZipProjectUp`)**：支持剥离冗余缓存极速克隆新分支，或仅将 `Config / Content / Source / Plugins / .uproject` 高速压缩为纯净 `.zip` 归档包。
  * 💻 **一键生成 VS 解决方案 (`.sln`)**：直接调用对应版本引擎的 `UnrealBuildTool.exe` 生成项目文件（纯蓝图工程可自动补齐标准 C++ Source 模块骨架）。
  * 🔌 **插件打包编译助手 (`BuildPlugin`)**：自动扫描工程内 `.uplugin` 文件，一键调用 `RunUAT.bat BuildPlugin -Rocket` 完成跨引擎版本插件编译与打包分发。

---

### 2. 📦 UE 数字资产金库 (Digital Asset Vault)
* **压缩包与文件夹混合纳管**：支持 `.zip`、`.7z`、`.rar`、`.uasset` 压缩包与已解压资产文件夹直接入库，支持批量扫描 `Epic VaultCache`、百度网盘或本地资产目录，内置跨格式防重复入库校验。
* **智能检索匹配 Fab 商城链接 + 1920P 高清原图抓取**：
  * 导入本地资产包时支持根据资产名称**自动检索匹配 Fab 商城商品链接**，提取商城 **1920P 高清轮播原图集** 并持久化保存至该资产专属的 `_PreviewMedia` 文件夹。
  * **多路神经网络 + 本地离线 AI 翻译 (`_AI_Models`)**：内置 UE5 技术美术专业术语词库校准（如 *Vertex-Painted* ➔ *顶点颜色绘制*、*Tiling Detail Materials* ➔ *无缝平铺细节材质*），支持一键中/英双语零延迟切换。
* **超轻量级本地元数据存档 (`_vault_meta.json`)**：资产配置信息自动以 `< 0.5KB` 存档写入资产目录，删除重传或跨目录迁移后可瞬间恢复分类、来源、引擎版本、Fab 链接与中英文详情描述。
* **🚀 一键自动解压投送至指定 UE 工程 (`Deploy to Project`)**：支持将资产金库中的压缩包（自动调用 Bandizip / 7-Zip / 原生解压引擎）或文件夹一键投送至任意 UE 工程，智能剥离外层包装壳并对齐 `Content/` 与 `Plugins/` 目录结构。

---

### 3. 🕸️ BlueprintUE 蓝图与材质节点工坊 (Blueprint & Material Workshop)
* **T3D 剪贴板源码双向无损解析**：在 UE5 蓝图或材质编辑器中选中节点按 `Ctrl + C`，即可直接粘贴进工坊生成可视化节点连线画布；点击 **「一键复制还原回 UE5」** 后在引擎内按 `Ctrl + V` 即可 100% 还原所有节点与连接。
* **真实材质与蓝图节点名识别**：精准解析 `K2Node_Event`、`K2Node_CallFunction` 以及 `MaterialGraphNode`（如 `TextureSample`、`Lerp`、`ScalarParameter`、`StaticSwitchParameter` 等），支持画布平滑缩放、自由拖拽节点并实时同步回写 `NodePosX / NodePosY` 坐标。
* **拓扑分层防堆叠自动排版 (Auto-Layout)**：一键根据引脚连线拓扑关系与动态引脚高度自动排列节点层级，彻底消除节点重叠。

---

### 4. 📘 研发知识库与 Notion 同步中心 (R&D Knowledge Base)
* **Notion 公开链接全文深度递归同步**：粘贴 Notion 分享链接，自动多轮递归拉取完整页面块树（标题、代码块、表格、Callout 提示框、待办清单与高清插图），自动转换为标准 Markdown 格式。
* **本地 Word (`.docx`) / HTML / Markdown 图文转换**：导入 `.docx` 文档时自动提取内嵌图片至 `_UEVault_DocsMedia`，保留原文档章节与表格结构。
* **内置 10 套大厂级研发标准模板**：涵盖 *Lumen & VSM 调优指南*、*GAS 战斗框架规范*、*PCG 大世界生态散射*、*Unreal Insights 性能剖析报告*、*MRQ 4K 影视渲染预设*、*PSO 预编译打包指南* 等，支持在**不覆盖原有正文**的前提下无损融合套用模板。
* **🔄 跨电脑知识资产同步 (`vault_knowledge_bp_sync.json`)**：支持一键导出或智能无损合并导入「蓝图节点图 + 研发笔记」轻量级数据包，轻松实现公司与家里多台电脑无缝协同。

---

## 🎨 五款高定光影主题与双语工作台 (Themes & Bilingual UI)

内置 5 套专为不同工种调校的次世代光影主题，并配备**可自由拖拽的桌面全息悬浮球**与 **简体中文 / English (US)** 一键无缝切换：
1. **暗物质电光青 (Dark Matter Cyan)** — 经典赛博工业深空配色，高对比电光青全息流光
2. **虚幻官方琥珀金 (Unreal Official Gold)** — 致敬 Unreal Engine 5 官方流光琥珀金与曜石碳黑
3. **荒坂激光绯红 (Cyber Crimson Red)** — 高侵略性机甲红黑工业配色
4. **黑客矩阵翡翠 (Matrix Emerald Green)** — 护眼极夜森林绿，适合长时间代码联调与 TA 检视
5. **星云钛空紫 (Nebula Titanium Violet)** — 全息合成器深紫美学，专为影视虚拟制片与灯光师打造

---

## ⌨️ 全局快捷键一览 (Global Shortcuts)

> 💡 所有快捷键均可在 **「⚙️ 系统设置 ➔ 全局快捷键设置」** 中点击按键徽章自由录制修改或单独开关。

| 快捷键 | 功能说明 (中文) | Function (English) |
| :--- | :--- | :--- |
| **`Alt + Space`** | 呼出 / 隐藏全局秒开搜索启动面板 (Spotlight Bar) | Toggle Global Spotlight Bar |
| **`F5`** | 触发全息激光扫描，平滑刷新全库工程与资产真实磁盘体积 | Rescan Disk Sizes & Media Vault |
| **`Ctrl + K`** | 快速聚焦顶部全局搜索框 | Focus Global Search Input |
| **`Ctrl + M`** | 一键解锁 / 锁定全局「管理模式」 | Toggle Admin / Read-Only Mode |
| **`Ctrl + L`** | 一键切换界面显示语言（🇨🇳 简体中文 / 🇺🇸 English） | Switch Interface Language (ZH / EN) |
| **`Ctrl + N`** | 快速呼出「导入/纳管新工程」弹窗 | Open Quick Import Project Modal |
| **`Ctrl + B`** | 快速折叠 / 展开左侧多功能导航栏 | Collapse / Expand Left Sidebar |

---

## 📥 下载与安装说明 (Download & Installation)

1. 前往本仓库右侧的 **[Releases 发布页面](https://github.com/LiangLiangVFX/UE_Vault_Pro_Launcher/releases)**。
2. 下载最新版本的安装包 **`UE Vault Pro Setup 1.1.0.exe`**。
3. 双击运行安装程序即可启动工作站；后续版本更新可直接点击软件内 **「⚙️ 系统设置 ➔ 关于软件与更新 ➔ 检测版本更新」** 在线检测并获取最新升级包。

---

## 👨‍💻 作者与联系方式 (Author & Contact)

* **Author (作者)**：**LiangLiangArtist**
* **Email (邮箱)**：`liangliangvfx@gmail.com`
* **GitHub**：[https://github.com/LiangLiangVFX](https://github.com/LiangLiangVFX)
* **YouTube**：[https://www.youtube.com/@zhaol2259](https://www.youtube.com/@zhaol2259)
* **Bilibili (哔哩哔哩)**：[https://space.bilibili.com/75504176](https://space.bilibili.com/75504176)
* **X (Twitter)**：[https://x.com/lemonzliang](https://x.com/lemonzliang)

---

<div align="center">
  <sub>Copyright © 2026 LiangLiangArtist. Crafted with ❤️ for Unreal Engine 5 Developers & Technical Artists.</sub>
</div>