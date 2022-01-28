---
title: PuTTY の設定ファイルをエクスポートする
description: 
published: true
date: 2022-01-28T07:04:55.568Z
tags: ssh, putty
editor: markdown
dateCreated: 2022-01-28T07:04:55.568Z
---

## 手段
* コマンド プロンプト (管理者権限) で次のコマンドを実行する。
`reg export HKEY_CURRENT_USER\Software\SimonTatham\PuTTY putty.reg`
## 参考
* [puttyの設定を別PCに移行する - Qiita](https://qiita.com/nemuiten/items/f64b569b4c347a626e0d)