---
title: ufw で作成したルールを削除する
description: 
published: true
date: 2022-01-25T07:26:25.869Z
tags: ufw, firewall
editor: markdown
dateCreated: 2022-01-25T07:26:25.869Z
---

# ufw で作成したルールを削除する
1. `ufw status numbered` で削除したいルールにどの番号が割り当てられているか確認する。
2. `ufw delete [番号]` で削除する。