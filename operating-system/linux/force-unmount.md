---
title: 強制的にマウントを解除する
description: 
published: true
date: 2022-01-28T07:01:08.333Z
tags: linux
editor: markdown
dateCreated: 2022-01-28T07:01:08.333Z
---

* オプション: `-l` を用いれば良い。
* これは、例えば google-drive-ocamlfuse のリードが追いつかなくなって固まった時に有用。
	e.g. `sudo unmount -l /path/to/gdrive`