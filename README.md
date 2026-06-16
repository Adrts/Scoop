<h1 align="center">Scoop</h1>

<p align="center">Windows 命令行包管理器 - 国内网络优化版</p>

---

Scoop 是一个 Windows 命令行安装工具，可自动管理软件的安装、更新和卸载。

## 本版本特性

针对国内网络环境做了以下优化和增强：

- **GitHub 下载加速**：支持通过 `github_proxy` 配置 GitHub Release 下载加速镜像，自动将 GitHub 下载链接替换为代理加速链接
- **下载信息透明**：下载时显示原始链接和是否使用了加速代理
- **配置灵活**：代理地址完全可自定义

**使用方式**：

```powershell
# 设置 GitHub 下载加速代理（以 https://github-proxy.memory-echoes.cn 为例）
scoop config github_proxy https://github-proxy.memory-echoes.cn

# 查看当前配置
scoop config github_proxy

# 取消加速代理
scoop config rm github_proxy
```

设置后，所有 GitHub Release 下载链接会自动经过加速代理，显著提升国内下载速度。

## 快速开始

```powershell
# 安装常用工具
scoop install sudo git 7zip aria2

# 查找软件
scoop search <name>

# 安装软件
scoop install <app>

# 更新所有软件
scoop update *
```

## 多线程下载

安装 `aria2` 后 Scoop 会自动使用多线程加速下载：

```powershell
scoop install aria2
```

## 常用 Bucket

```powershell
scoop bucket add extras
scoop bucket add versions
```

---

该项目基于 [ScoopInstaller/Scoop](https://github.com/ScoopInstaller/Scoop) 修改，仅做国内网络适应性优化。
