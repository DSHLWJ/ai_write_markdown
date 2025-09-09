---
title: Dos常见基础指令
description: Dos常见基础指令
date: 2022-06-09T20:12:52+08:00
lastmod: 2022-06-09T20:12:52+08:00
tags:
  - Windows
  - Dos
categories:
  - windows
---

# dos基本常见命令

## 文件和目录管理

### cd指令切换目录

```
cd directory_name # 进入指定目录
cd .. # 返回上一级目录
cd \ # 切换到根目录
```

### md或mkdir指令:创建目录

```
md new_directory
```

### `rd` 或 `rmdir`：删除一个空目录

```
rd directory_name
```

### `del` 或 `erase`：删除指定文件

```
del filename
```

### `copy`：复制文件

```
copy source_file destination
```

### `rename` 或 `ren`：重命名文件或目录

```
rename old_filename new_filename
```

### `xcopy`：复制文件和目录，包括子目录

```
xcopy source destination /s /e  # /s 复制子目录，/e 包括空目录
```

## 查看和编辑文件

### `type`：显示文件的内容

```
type filename
```

### `notepad`：启动记事本编辑器

```
notepad filename
```

## 磁盘操作

### `diskpart`：启动磁盘分区工具

```
diskpart
```

### `format`：格式化磁盘或驱动器

```
format drive_letter:  # 格式化驱动器
```

### `chkdsk`：检查磁盘上的文件系统错误

```
chkdsk drive_letter:
```

### `label`：更改磁盘的卷标

```
label drive_letter: volume_label
```

## 系统和网络

### `cls`：清除屏幕

```
cls
```

### `exit`：退出命令提示符窗口

```
exit
```

### `shutdown`：关闭计算机

```
shutdown /s /t 0    # 立即关闭计算机
```

### `ping`：测试网络连接

```
ping 192.168.1.1    # Ping 一个IP地址，检查是否通畅
```

### `ipconfig`：显示计算机的网络配置

```
ipconfig /all
```

### `netstat`：显示网络连接信息

```
netstat
```

### `tasklist`：显示当前运行的任务和进程

```
tasklist
```

### `taskkill`：结束进程

```
taskkill /f /im process_name.exe
```

批处理和自动化

### `echo`：显示一行文本或输出到文件

```
echo：显示一行文本或输出到echo Hello World!
echo Hello World! > file.txt  # 输出到文件
```

### `pause`：暂停批处理文件的执行，等待用户按任意键继续

```
pause
```

### `set`：设置环境变量

```
set variable_name=value
```

### `for`：循环结构，执行批处理文件中的重复任务

```
for %i in (*.txt) do echo %i
```

### `call`：调用其他批处理文件或命令

```
call script.bat
```

## 系统信息

### `ver`：显示当前操作系统的版本

```
ver
```

### `systeminfo`：显示系统的详细配置信息

```
systeminfo
```

### `hostname`：显示当前计算机的主机名

```
hostname
```

## 文件属性和权限

### `attrib`：显示或修改文件属性（只读、隐藏等）

```
attrib +r filename    # 设置文件为只读
attrib -r filename    # 取消只读属性
```

### `cacls` 或 `icacls`：修改文件或文件夹的访问控制列表（ACLs）

```
cacls filename /E /P user_name:F   # 为文件设置权限
```

## 查看磁盘和文件系统

### tree：显示目录结构的树形图

```
tree
```

### dir /s：列出当前目录及其子目录中的所有文件

```
dir /s
```
