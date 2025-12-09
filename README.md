# NVIDIA vGPU Script For PVE

![License](https://img.shields.io/github/license/Mapleawaa/NVIDIA-vGPU-Script-For-PVE?style=flat-square)
![Go Version](https://img.shields.io/github/go-mod/go-version/Mapleawaa/NVIDIA-vGPU-Script-For-PVE?style=flat-square)
![Build Status](https://img.shields.io/github/actions/workflow/status/Mapleawaa/NVIDIA-vGPU-Script-For-PVE/build.yml?style=flat-square)
> [!WARNING]
> ⚠️ 警告 / WARNING: 防诈骗声明
>
> **本项目是完全免费且开源的！如果你是付费购买的本软件，请立即申请退款并举报商家！**
> **This project is completely FREE and OPEN SOURCE. If you paid for this software, you have been SCAMMED. Please request a refund immediately.**

## 📖 项目简介 | Introduction

**NVIDIA-vGPU-Script-For-PVE** 是 [PVE-Tools-9](https://github.com/Mapleawaa/PVE-Tools-9) 的分支项目，旨在为 Proxmox VE (PVE) 系统提供一站式的 NVIDIA vGPU 自动化部署方案。

本工具使用 Go 语言重构，解决了传统 Shell 脚本在复杂环境下的兼容性问题，集成了驱动安装、vGPU 解锁配置以及授权容器的自动部署。

### ✨ 核心功能 | Features

* 🚀 **自动检测与安装**：根据内核版本自动匹配并编译安装 NVIDIA vGPU 驱动。
* 🔓 **vGPU Unlock**：自动化配置 `vgpu_unlock-rs`，打破消费级显卡限制。
* 🐳 **授权服务集成**：一键部署并配置 `FASTAPI-DLS` 容器，实现本地授权验证。
