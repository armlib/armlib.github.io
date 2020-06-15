---
title: Git干货学习篇-创建修改git本地端用户信息
summary: Git Bash创建和修改git用户名/邮箱/密码及如Bash何保持密码
tags:
  - 创建户名邮箱
  - 修改用户信息
categories:
  - Git干货学习篇
abbrlink: 1602138242
date: 2020-06-14 19:25:00
---

## 创建和修改git用户名/邮箱/密码及如何保持密码
用户名和邮箱地址是本地git客户端的信息，不随git库不同而改变，Git的每一次提交都会使用该信息，并且写入到每一次提交信息中。

### 以Windows环境下为例：

- 打开Git Bash命令窗口：
库文件夹内 - 右键 - 选择Git Bash Here

- 查看用户名、邮箱地址和密码命令：
```git命令
$ git config user.name
$ git config user.email
$ git config user.password
```

- 创建和修改用户名、邮箱地址和密码的命令：
```
$ git config --global user.name “username”
$ git config --global user.email “email”
$ git config --global user.password “password”
```

- 本地每次commit都需要用户名和邮箱纪录，提示我们输入密码，所以在修改完密码以后，输入以下命令，以后只要再输入一次用户名和密码即可。
```
$ git config --global credential.helper store
```
