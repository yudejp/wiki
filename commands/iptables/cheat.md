---
title: チートシート
description: 
published: true
date: 2022-01-25T07:29:59.727Z
tags: firewall, iptables
editor: markdown
dateCreated: 2022-01-25T07:29:59.727Z
---

# チートシート
* 設定を確認する: `sudo iptables -L`
* 該当ポートを許可する: `sudo iptables -I INPUT 5 -p tcp --dport [ポート番号] -j ACCEPT`
* 設定を永続化する
  `sudo /etc/init.d/netfilter-persistent save`
  `sudo /etc/init.d/netfilter-persistent reload`