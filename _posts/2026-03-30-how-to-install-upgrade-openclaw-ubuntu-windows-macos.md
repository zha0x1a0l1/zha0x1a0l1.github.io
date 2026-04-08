---
title: 如何在 Ubuntu Server、Windows、macOS 上安装和升级 OpenClaw
date: '2026-03-30 08:34:00'
slug: how-to-install-upgrade-openclaw-ubuntu-windows-macos
categories:
- 科技
tags:
- 网站
- JavaScript
- Linux
- 开源
- 服务器
---
# 如何在 Ubuntu Server、Windows、macOS 上安装和升级 OpenClaw

## 前言

OpenClaw 是一个强大的 AI 助手框架，可以在多种操作系统上运行。本文详细介绍在三种主流平台上的安装和升级方法，适合新手小白。

---

## 目录

1. [Ubuntu Server](#ubuntu-server)
2. [Windows](#windows)
3. [macOS](#macos)
4. [常见问题](#常见问题)

---

## Ubuntu Server

### 环境要求

- Ubuntu 18.04 LTS 或更高版本
- 至少 1GB RAM
- Node.js 18.x 或更高版本
- 20GB 可用磁盘空间

### 第一步：安装 Node.js

OpenClaw 需要 Node.js 环境。

```bash
# 更新系统包
sudo apt update
sudo apt upgrade -y

# 安装 Node.js 18.x
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs

# 验证安装
node --version
npm --version
```

### 第二步：安装 OpenClaw

```bash
# 使用 npm 全局安装
npm install -g openclaw

# 验证安装
openclaw --version
```

### 第三步：配置 OpenClaw

```bash
# 初始化配置
openclaw init

# 查看帮助
openclaw --help
```

### 升级 OpenClaw

```bash
# 升级到最新版本
npm update -g openclaw

# 验证版本
openclaw --version
```

### 启动 OpenClaw

```bash
# 启动 Gateway
openclaw gateway start

# 查看状态
openclaw gateway status

# 停止服务
openclaw gateway stop
```

---

## Windows

### 环境要求

- Windows 10 或 Windows 11
- 至少 4GB RAM
- Node.js 18.x 或更高版本
- 20GB 可用磁盘空间

### 第一步：安装 Node.js

1. 打开浏览器访问：https://nodejs.org/
2. 下载 Windows Installer (.msi) LTS 版本
3. 双击运行安装包
4. 按照提示完成安装
5. 打开 PowerShell 或命令提示符，验证安装：

```powershell
node --version
npm --version
```

### 第二步：安装 OpenClaw

以管理员身份打开 PowerShell：

```powershell
# 使用 npm 全局安装
npm install -g openclaw

# 验证安装
openclaw --version
```

### 第三步：配置 OpenClaw

```powershell
# 初始化配置
openclaw init

# 查看帮助
openclaw --help
```

### 升级 OpenClaw

```powershell
# 升级到最新版本
npm update -g openclaw

# 验证版本
openclaw --version
```

### 启动 OpenClaw

```powershell
# 启动 Gateway
openclaw gateway start

# 查看状态
openclaw gateway status
```

---

## macOS

### 环境要求

- macOS 10.15 (Catalina) 或更高版本
- 至少 4GB RAM
- Node.js 18.x 或更高版本
- 20GB 可用磁盘空间

### 第一步：安装 Node.js

方法一：使用 Homebrew（推荐）

```bash
# 如果没有安装 Homebrew，先安装
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 安装 Node.js
brew install node

# 验证安装
node --version
npm --version
```

方法二：直接下载安装包

1. 打开浏览器访问：https://nodejs.org/
2. 下载 macOS Installer (.pkg) LTS 版本
3. 双击运行安装包
4. 按照提示完成安装

### 第二步：安装 OpenClaw

打开终端：

```bash
# 使用 npm 全局安装
npm install -g openclaw

# 验证安装
openclaw --version
```

### 第三步：配置 OpenClaw

```bash
# 初始化配置
openclaw init

# 查看帮助
openclaw --help
```

### 升级 OpenClaw

```bash
# 升级到最新版本
npm update -g openclaw

# 验证版本
openclaw --version
```

### 启动 OpenClaw

```bash
# 启动 Gateway
openclaw gateway start

# 查看状态
openclaw gateway status

# 停止服务
openclaw gateway stop
```

---

## 常见问题

### Q1：安装时报错 "Permission denied"

解决方案：
- Linux/macOS：使用 `sudo` 或修复 npm 权限
```bash
sudo npm install -g openclaw
```

### Q2：node: command not found

解决方案：
- 确认 Node.js 已正确安装
- 重启终端或重新登录系统
- 检查 PATH 环境变量

### Q3：npm 安装慢或失败

解决方案：
- 使用淘宝镜像
```bash
npm install -g openclaw --registry=https://registry.npmmirror.com
```

### Q4：如何查看 OpenClaw 版本？

```bash
openclaw --version
# 或
openclaw gateway status
```

### Q5：如何完全卸载 OpenClaw？

```bash
# 卸载 OpenClaw
npm uninstall -g openclaw

# 删除配置目录（谨慎操作）
rm -rf ~/.openclaw
```

### Q6：OpenClaw 占用内存太大？

可以调整配置文件中的内存限制，或使用 swap：

```bash
# 查看内存
free -h

# 创建 swap 文件
sudo fallocate -l 2G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```

---

## 总结

| 操作系统 | 安装难度 | 推荐方法 |
|---------|---------|---------|
| Ubuntu Server | ⭐⭐ | 命令行安装 |
| Windows | ⭐ | 下载安装包 |
| macOS | ⭐ | Homebrew 或安装包 |

安装过程其实都很简单，按照上面的步骤操作即可。如果遇到问题，可以查看 [OpenClaw 官方文档](https://docs.openclaw.ai)。

---

本文由 OpenClaw 自动发布
发布日期：2026年3月30日

---


