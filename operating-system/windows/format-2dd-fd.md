---
title: Windows で 3.5 インチ 2DD フロッピーディスクをフォーマットする
description: 
published: true
date: 2022-01-28T04:01:04.888Z
tags: windows, floppy, format
editor: markdown
dateCreated: 2022-01-28T04:01:04.888Z
---

* 最近の Windows では GUI から 3.5 インチ 2DD フロッピーディスクをフォーマットすることができません。
* フォーマットを行うには、コマンド プロンプトや Windows PowerShell で以下のコマンドを実行します。
	* `format a: /f:720`
		* `a:` はフロッピードライブを示すように適宜変更してください。
		* `/f:720` というパラメータは、2DD ディスクを使用することを示します。