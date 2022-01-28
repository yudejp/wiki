---
title: チートシート
description: 
published: true
date: 2022-01-28T07:07:35.763Z
tags: youtube-dl
editor: markdown
dateCreated: 2022-01-28T07:07:35.763Z
---

## 動画の wav ファイルをほぼ最高音質でダウンロードする
* `youtube-dl -f bestaudio --extract-audio --audio-format wav --audio-quality 0 [URL]`

## プレイリストを一括でダウンロードする
* `youtube-dl -i -f bestvideo+bestaudio [プレイリストの URL]`
* `bestvideo+bestaudio` オプションにより、最高画質のファイルと最高音質のファイルが ffmpeg によって結合される。

## テキストファイル内に列挙された URL をすべてダウンロードする
* `youtube-dl -f best -a [テキストファイルへのパス]`

## 特定のチャンネルの動画をすべてダウンロードする
* `youtube-dl -f best -ciw -o "%(title)s.%(ext)s" -v [チャンネル URL]`
