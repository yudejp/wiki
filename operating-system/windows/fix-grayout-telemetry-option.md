---
title: 「診断データ」のオプションがグレーアウトして選択できない
description: 
published: true
date: 2022-01-28T04:05:45.603Z
tags: windows, telemetry
editor: markdown
dateCreated: 2022-01-28T04:05:45.603Z
---

* 参考: [windows 10 - Diagnostics and usage data option disabled - Super User](https://superuser.com/questions/970011/diagnostics-and-usage-data-option-disabled)
* レジストリの値 `AllowTelemetry` を削除
    * `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\DataCollection` の中にある