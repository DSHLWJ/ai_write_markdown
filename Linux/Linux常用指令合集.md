---
title: Linux常用指令
description:  Linux常用指令
date: 2022-06-09T20:12:52+08:00
lastmod: 2022-06-09T20:12:52+08:00
tags:
  - Linux
---

当然可以！以下是一些Linux常用指令的合集，涵盖了文件管理、系统监控、网络管理、用户管理等方面。

### 1. 文件和目录管理
- **ls**: 列出目录中的文件
  ```bash
  ls -l     # 详细列表
  ls -a     # 包含隐藏文件
  ```

- **cd**: 切换目录
  ```bash
  cd /path/to/directory  # 切换到指定目录
  cd ..                   # 返回上一级目录
  cd ~                    # 切换到用户主目录
  ```

- **pwd**: 显示当前工作目录
  ```bash
  pwd
  ```

- **mkdir**: 创建新目录
  ```bash
  mkdir new_directory     # 创建名为new_directory的新目录
  ```

- **rmdir**: 删除空目录
  ```bash
  rmdir empty_directory    # 删除名为empty_directory的空目录
  ```

- **rm**: 删除文件或目录
  ```bash
  rm file.txt             # 删除文件
  rm -r directory_name     # 递归删除目录及其内容
  ```

- **cp**: 复制文件或目录
  ```bash
  cp source.txt destination.txt      # 复制文件
  cp -r source_directory/ target_directory/  # 递归复制目录
  ```

- **mv**: 移动或重命名文件或目录
  ```bash
  mv old_name.txt new_name.txt      # 重命名文件
  mv file.txt /path/to/destination/  # 移动文件
  ```

- **touch**: 创建空文件或更新文件的时间戳
  ```bash
  touch newfile.txt
  ```

### 2. 文件内容查看和编辑
- **cat**: 显示文件内容
  ```bash
  cat file.txt               # 显示文件内容
  ```

- **less**: 分页查看文件内容
  ```bash
  less file.txt              # 分页查看文件，按q退出
  ```

- **head**: 查看文件的前几行
  ```bash
  head -n 10 file.txt        # 查看前10行
  ```

- **tail**: 查看文件的后几行
  ```bash
  tail -n 10 file.txt        # 查看最后10行
  tail -f file.txt           # 实时查看文件增加的内容
  ```

- **nano / vim**: 编辑文件
  ```bash
  nano file.txt              # 使用nano编辑文件
  vim file.txt               # 使用vim编辑文件
  ```

### 3. 系统监控
- **top**: 动态显示系统运行情况
  ```bash
  top
  ```

- **htop**: 更友好的系统监控工具（需安装）
  ```bash
  htop
  ```

- **df**: 查看文件系统的磁盘空间使用情况
  ```bash
  df -h                      # 以人类可读格式显示
  ```

- **du**: 查看目录或文件的磁盘使用情况
  ```bash
  du -sh /path/to/directory  # 显示目录总大小
  ```

- **free**: 查看内存使用情况
  ```bash
  free -h                    # 以人类可读格式显示
  ```

### 4. 用户管理
- **whoami**: 显示当前用户
  ```bash
  whoami
  ```

- **useradd**: 添加新用户
  ```bash
  sudo useradd username      # 添加新用户
  ```

- **passwd**: 修改用户密码
  ```bash
  passwd username             # 修改用户的密码
  ```

- **usermod**: 修改用户属性
  ```bash
  sudo usermod -aG groupname username  # 将用户添加到组
  ```

- **userdel**: 删除用户
  ```bash
  sudo userdel username       # 删除用户
  ```

### 5. 网络管理
- **ifconfig**: 查看或配置网络接口（老旧）
  ```bash
  ifconfig
  ```

- **ip**: 查看和配置网络接口（推荐使用）
  ```bash
  ip a                       # 查看网络接口和IP地址
  ```

- **ping**: 检查网络连接
  ```bash
  ping google.com            # 检查与Google的连接
  ```

- **netstat**: 查看网络连接情况（可用ss替代）
  ```bash
  netstat -tuln              # 显示所有监听的端口
  ```

- **curl / wget**: 下载文件
  ```bash
  wget http://example.com/file.zip  # 使用wget下载文件
  curl -O http://example.com/file.zip # 使用curl下载文件
  ```

### 6. 其他有用指令
- **chmod**: 更改文件或目录的权限
  ```bash
  chmod 755 script.sh       # 设置文件可执行权限
  ```

- **chown**: 更改文件或目录的所有者
  ```bash
  chown user:group file.txt  # 修改文件的所有者和用户组
  ```

- **find**: 查找文件
  ```bash
  find /path -name "file.txt"  # 在指定路径下查找文件
  ```

- **grep**: 搜索文本内容
  ```bash
  grep "pattern" file.txt      # 在文件中搜索指定模式
  ```

以上是一些常用的Linux指令，希望对你有所帮助！如果你有特定指令的使用问题，欢迎随时问我。
