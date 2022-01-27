---
title: SSH 接続を簡単にする
description: 
published: true
date: 2022-01-27T05:15:03.768Z
tags: ssh
editor: markdown
dateCreated: 2022-01-27T05:15:03.768Z
---

## 概要
* `ssh host` 等と入力するだけで接続を可能にします。

## 方法
* 設定ファイルに以下の内容を書き込む。
```
Host [name]
 	HostName (宛先サーバーのIPアドレス または ホスト名)
 	User (ユーザー名)
 	Port (ポート番号)
 	IdentityFile (公開鍵認証に使用する秘密鍵)
```