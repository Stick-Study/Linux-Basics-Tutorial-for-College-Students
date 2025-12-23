Windows Subsystem for Linux
========
适用于 Linux 的 Windows 子系统（WSL）是 Windows 的一项功能，可用于在 Windows 计算机上运行 Linux 环境，而无需单独的虚拟机或双重启动。 

我们只需要在 Windows Powershell 中使用 WSL 学习 Linux，而无需使用繁重的 VMware Workstation Pro 或是 Parallel Desktop 来学习。接下来我将介绍一下有关 WSL 的基础用法：

# 基础

### Ubuntu 安装
使用
```
wsl --list --online
```
来查看在线商店提供的 Linux 分发版列表，

![](https://github.com/Stick-Study/Linux-Basics-Tutorial-for-College-Students/blob/main/Photos/00-WSL-Selection.png)

然后使用
```
wsl --install [名称]
```
来安装想要的版本。

例如想要安装 Ubuntu-24.04，可以直接输入
```
wsl --install Ubuntu-24.04
```

### 启动 Ubuntu

直接在 Powershell 中输入
```
wsl
``` 
即可进入默认的 Linux 发行版

![](https://github.com/Stick-Study/Linux-Basics-Tutorial-for-College-Students/blob/main/Photos/00-WSL-Start.png)

### 访问 Linux 文件
在 Windows 资源管理器中输入
```
\\wsl$
```
即可访问 Linux 下的文件。

![](https://github.com/Stick-Study/Linux-Basics-Tutorial-for-College-Students/blob/main/Photos/00-File.png)
# 进阶

### 更新 WSL
更新 WSL 内核和组件
```
wsl --update
```
```
wsl --update --web-download //从 GitHub 下载最新更新。
```

### 关机
```
wsl --shutdown
```
一般来说，直接关闭 PowerShell 或终端窗口即可结束当前会话，但如果需要彻底停止所有 WSL 后台进程，可以使用该命令。

### 查看已安装的发行版
查看已安装的 Linux 发行版
```
wsl --list --verbose
```

### 设置默认发行版
```
wsl --set-default Ubuntu-24.04
```
