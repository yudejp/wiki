---
title: SSH 関連のファイルの権限設定
description: 
published: true
date: 2022-01-28T07:14:09.952Z
tags: ssh
editor: markdown
dateCreated: 2022-01-27T05:13:18.095Z
---

* 大半の Web サイトでは、`.ssh/authorized_keys` 周りの権限設定を重視するが、ホームディレクトリ自体の権限設定も重要である。
* 不適切な権限設定により、SSH 接続が無効化されることがある。

## 矯正コマンド
`sudo chmod 600 ~/.ssh`
`sudo chmod 600 ~/.ssh/authorized_keys`
`sudo chmod 755 ~/`
