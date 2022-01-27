---
title: MySQL のパスワードが合っているにも関わらず、接続に失敗する。
description: 
published: true
date: 2022-01-27T05:09:43.761Z
tags: mysql
editor: markdown
dateCreated: 2022-01-27T05:09:43.761Z
---

* バージョンが新しくなったことで生まれる不具合。

## 対処法
* MySQL にログイン後、下記コマンドを実行する。
  `grant all privileges on *.* to 'user'@'localhost' with grant option;`