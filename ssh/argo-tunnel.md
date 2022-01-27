---
title: Cloudflare Argo Tunnel (cloudflared) 経由で SSH 接続
description: 
published: true
date: 2022-01-27T05:16:56.102Z
tags: ssh, cloudflared, argo tunnel
editor: markdown
dateCreated: 2022-01-27T05:16:56.102Z
---

## 方法
1. `cloudflared` をインストール
2. `cloudflared login` でログイン
3. `~/.ssh/config` に以下を書き込む
```
 Host MyHost
   User MyUser
   HostName ssh.example.com
   ProxyCommand cloudflared access ssh --hostname %h
```