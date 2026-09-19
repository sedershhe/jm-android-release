# JM Android

阅前提示：孩子们这个项目是我睡觉前一句话让deepseek V4.1 flash自己照着另一个python小程序（基于hect0x7大佬的jmcomic库）琢磨的，还没写约束文档，里面全是大粪ai代码用出bug概不负责。。。

## 当前状态

- Android 技术栈：Kotlin、Jetpack Compose
- 构建环境：GitHub Codespaces
- CI 与 Android 模拟器测试：GitHub Actions
- 浏览器自动化：Edge CDP，仅用于网页流程
- 账号配置：应用提供账号修改窗口，测试配置通过 Codespaces Secrets 注入
- 下载目录：支持 Android Storage Access Framework 目录选择
- 最终产物：可在 Android 模拟器验收后从 GitHub Actions 下载 Debug APK

## 原则

- 不提交账号、密码、Cookie、Token、签名密钥。
- Android 客户端提供账号修改窗口，正式包不内置账号密码。
- 先把桌面版功能做成可测试的规格，再逐项实现。
- 每次提交必须能通过单元测试、Lint 和 Debug 构建。

## 开发环境

使用仓库的 Dev Container 启动 Codespaces。首次创建后，容器会运行
`.devcontainer/postCreate.sh` 检查 Java、Node、GitHub CLI 和 Android SDK。

Android SDK 的 Platform 和 Build Tools 版本将在项目骨架阶段从官方稳定源确定
