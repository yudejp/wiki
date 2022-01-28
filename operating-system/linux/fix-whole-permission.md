---
title: ルート以下の権限を破壊してしまったとき
description: 
published: true
date: 2022-01-28T07:11:06.760Z
tags: linux
editor: markdown
dateCreated: 2022-01-28T07:10:41.322Z
---

## 方法
* とりあえず、Live CD で起動して sudo を使えるようにする。
* 以下のコマンドを実行していく:
```
chmod -R go-w /bin
chmod -R go-w /etc
chmod -R go-w /boot
chmod -R go-w /dev
```
* 特殊なパーミッションを持つディレクトリについては、以下のコマンドを実行していく:
```
chmod 440 /etc/sudoers
chmod 440 /etc/sudoers.d/README
chmod 755 /etc/sudoers.d
chmod 640 /etc/shadow /etc/gshadow
chmod 600 /etc/ssh/*_key
chmod 600 /etc/ssh*key
chmod 710 /etc/ssl/private
chmod 710 /etc/cups/ssl
chmod 1777 /tmp /var/tmp /var/lock
chmod 4755 /bin/su /usr/bin/passwd /usr/bin/sudo /usr/bin/sudoedit
chmod 2755 /var/mail /var/spool/mail
```

## 参考
* [誤って” / “以下のパーミッションを一括で変更した場合の対処法 – wp.bmemo.pw](https://wp.bmemo.pw/759)