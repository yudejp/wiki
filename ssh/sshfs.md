---
title: リモートのディレクトリをマウントする
description: 
published: true
date: 2022-01-28T07:14:38.506Z
tags: ssh, sshfs
editor: markdown
dateCreated: 2022-01-27T05:16:21.532Z
---

## 方法
1. `sshfs` パッケージをインストールする。
2. `modprobe fuse` を実行し、`fuse` カーネルモジュールが読み込まれていることを確認する。
3. 公開鍵認証を設定する。 (パスワードなし)
4. `/etc/fstab` を編集する。
  ```
  /bin/sshfs#[user]@[host]:[remote directory] [mount point] fuse IdentityFile=[path to private key],allow_other,compression=yes,transform_symlinks,idmap=user,reconnect,_netdev,ServerAliveInterval=60 0 0
  ```
5. `mount -a` を実行して設定を検証する。