---
title: PostgreSQL の鍵の権限が存在しない
description: 
published: true
date: 2022-01-27T05:08:51.496Z
tags: postgresql
editor: markdown
dateCreated: 2022-01-27T05:08:51.496Z
---

## 対処法
下記コマンドを順に実行する。
* `chown postgres:ssl-cert /etc/ssl/private/`
* `chown postgres:postgres /etc/ssl/private/ssl-cert-snakeoil.key`

## 参考
* [誤って” / “以下のパーミッションを一括で変更した場合の対処法 – wp.bmemo.pw](https://wp.bmemo.pw/759)