---
title: No chain/target/match by that name. (iptables)
description: 
published: true
date: 2022-01-25T07:55:59.974Z
tags: firewall, iptables
editor: markdown
dateCreated: 2022-01-25T07:31:39.165Z
---

![https://gyazo.com/cd003db59a1202182defb698ae79dab1/max_size/1000](https://gyazo.com/cd003db59a1202182defb698ae79dab1/max_size/1000)

## 解決策
1. すべてのチェーンを削除する。
 `sudo iptables -t filter -F`
 `sudo iptables -t filter -X`
2. Docker デーモンを再起動する。
 `sudo systemctl restart docker`
## 参考
* [Running docker container : iptables: No chain/target/match by that name - Stack Overflow](https://stackoverflow.com/questions/31667160/running-docker-container-iptables-no-chain-target-match-by-that-name)