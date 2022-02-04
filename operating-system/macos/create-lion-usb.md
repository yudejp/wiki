---
title: 最新の macOS で Mac OS X Lion のインストール USB メディアを作成する
description: 
published: true
date: 2022-02-04T01:21:31.572Z
tags: macos
editor: markdown
dateCreated: 2022-02-04T01:21:31.572Z
---

## 方法
1. Mac OS X Lion のインストーラーを[ここ](https://support.apple.com/kb/DL2077?locale=ja_JP) からダウンロードする。
2. ダウンロードした `Install Mac OS X Lion.app` の中にある `InstallESD.dmg` を取り出す。
3. 以下のコマンドで `InstallESD.dmg` を USB フラッシュメモリに直接書き込めるような形式に変換する。
```
hdiutil convert -format UDRW -o Lion /path/to/InstallESD.dmg
```
成功時のログの例:
```
Driver Descriptor Map（DDM: 0）を読み込み中…
（Apple_Free: 1）を読み込み中…
Apple（Apple_partition_map: 2）を読み込み中…
Macintosh（Apple_Driver_ATAPI: 3）を読み込み中…
（Apple_Free: 4）を読み込み中…
disk image（Apple_HFS: 5）を読み込み中…
.........................................................................
（Apple_Free: 6）を読み込み中…
経過時間: 17.489s
速度: 280.7Mバイト/秒
節約率: 0.0%
created: /Users/yude/Lion.img.dmg
```
