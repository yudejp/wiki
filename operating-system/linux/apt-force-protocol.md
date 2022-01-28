---
title: apt が使用するプロトコルに IPv4 または IPv6 を強制する
description: 
published: true
date: 2022-01-28T07:02:30.839Z
tags: linux, apt, ipv4, ipv6
editor: markdown
dateCreated: 2022-01-28T07:02:30.839Z
---

### 一時的
* IPv4 を使用する
`apt -o Acquire::ForceIPv4=true update`
* IPv6 を使用する
`apt -o Acquire::ForceIPv6=true update`
### 恒久的
* IPv4 を使用する
`/etc/apt/apt/conf.d/99force-ipv4` に以下を追記する。
`Acquire::ForceIPv4 "true";`
* IPv6 を使用する
`/etc/apt/apt/conf.d/99force-ipv6` に以下を追記する。
`Acquire::ForceIPv6 "true";`