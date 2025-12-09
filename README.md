# NVIDIA vGPU Script For PVE

![License](https://img.shields.io/github/license/Mapleawaa/NVIDIA-vGPU-Script-For-PVE?style=flat-square)
![Go Version](https://img.shields.io/github/go-mod/go-version/Mapleawaa/NVIDIA-vGPU-Script-For-PVE?style=flat-square)
![Build Status](https://img.shields.io/github/actions/workflow/status/Mapleawaa/NVIDIA-vGPU-Script-For-PVE/build.yml?style=flat-square)

> [!WARNING]
> **本项目是完全免费且开源的！如果你是付费购买的本软件，请立即申请退款并举报商家！**
> **This project is completely FREE and OPEN SOURCE. If you paid for this software, you have been SCAMMED. Please request a refund immediately.**

## 📖 项目简介 | Introduction

**NVIDIA-vGPU-Script-For-PVE** 是 [PVE-Tools-9](https://github.com/Mapleawaa/PVE-Tools-9) 的分支项目，旨在为 Proxmox VE (PVE) 系统提供一站式的 NVIDIA vGPU 自动化部署方案。

本工具使用 Go 语言重构，解决了传统 Shell 脚本在复杂环境下的兼容性问题，集成了驱动安装、vGPU 解锁配置以及授权容器的自动部署。

### ✨ 核心功能 | Features

* 🚀 **自动检测与安装**：根据内核版本自动匹配并编译安装 NVIDIA vGPU 驱动。
* 🔓 **vGPU Unlock**：自动化配置 `vgpu_unlock-rs`，打破消费级显卡限制。
* 🐳 **授权服务集成**：一键部署并配置 `FASTAPI-DLS` 容器，实现本地授权验证。
* 🛡️ **遥测透明**：内置可选的错误追踪系统，帮助开发者快速定位适配问题。

---

## 📥 下载与使用 | Usage

推荐直接从 [Releases](../../releases) 页面下载最新编译好的二进制文件。

### 快速开始

```bash

````

### 交互式确认

程序启动时会要求用户确认是否开启数据收集（见下文），并同意免责声明。

-----

## 🕵️ 数据收集与隐私 | Telemetry & Privacy

为了改进脚本在不同 PVE 魔改版本下的稳定性，本程序默认集成 [Sentry](https://sentry.io) 用于收集**运行错误日志**。

  * **我们收集什么：** PVE 版本号、内核版本、程序崩溃时的堆栈信息 (Stack Trace)。
  * **我们绝不收集：** 您的 IP 地址、服务器密码、私钥、容器数据或任何显卡序列号。
  * **代码审计：** 遥测代码完全开源，欢迎查阅 `pkg/telemetry` 目录，看清我们到底发了什么。

**如何关闭？**
如果您介意数据发送，请在启动时选择 `No`，或使用以下参数启动：

```bash
./nv-vgpu-tool_linux_amd64 --no-telemetry
```

-----

## ⚖️ 免责声明 | Disclaimer

1.  **仅供学习研究**：本项目仅供个人学习 Linux 驱动架构及虚拟化技术使用。
2.  **无商业用途**：严禁将本项目用于任何商业环境或作为盈利服务的一部分。
3.  **版权声明**：
      * NVIDIA 驱动及 vGPU 技术版权归 NVIDIA Corporation 所有。
      * 本项目不包含任何 NVIDIA 专有二进制文件，仅提供自动化配置脚本。
      * 用户需自行确保其行为符合当地法律法规及软件许可协议。
4.  **风险提示**：使用非官方驱动和解锁工具可能会导致系统不稳定或硬件损坏，开发者不对任何损失负责。

-----

## 🔗 致谢与上游 | Credits

本项目基于以下开源项目构建，感谢原作者的贡献：

  * [vgpu\_unlock-rs](https://github.com/mbilker/vgpu_unlock-rs) (MIT)
  * [fastapi-dls](https://git.collinwebdesigns.de/oscar.krause/fastapi-dls)
  * [PVE-Tools-9](https://github.com/Mapleawaa/PVE-Tools-9)

-----

**Made with ❤️ by Mapleawaa**
