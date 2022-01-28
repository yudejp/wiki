---
title: RDP Wrapper Library と自動アップデータの導入・使用方法
description: 
published: true
date: 2022-01-28T04:04:49.327Z
tags: windows, rdp wrapper library, rdp
editor: markdown
dateCreated: 2022-01-28T04:04:49.327Z
---

* これは、基本的には以下のページの日本語訳になります。
[rdpwrap/binary-download.md at master · asmtron/rdpwrap · GitHub](https://github.com/asmtron/rdpwrap/blob/master/binary-download.md)
	* 適宜操作の説明を入れることにより、分かりやすくしています。
	* Windows 10 21H1 での動作を確認しています。

#### 方法
* 1. `RDPWrap-v1.6.2.zip` をダウンロードします。
	ダウンロード先: [https://github.com/stascorp/rdpwrap/releases/download/v1.6.2/RDPWrap-v1.6.2.zip](https://github.com/stascorp/rdpwrap/releases/download/v1.6.2/RDPWrap-v1.6.2.zip)
* 2. `RDPWrap-v1.6.2.zip` の中身を、`C:\Program Files\RDP Wrapper` に展開します。
    * ディレクトリが存在しない場合、新規で作成する必要があるかもしれません。
    * `C:\Program Files\RDP Wrapper` 以外の場所に展開することは推奨されていません。
* 3. `autoupdate.zip` をダウンロードします。
    * ダウンロード先: [https://github.com/asmtron/rdpwrap/raw/master/autoupdate.zip](https://github.com/asmtron/rdpwrap/raw/master/autoupdate.zip)
* 4. `autoupdate.zip` の中身を RDP Wrapper と同じ場所に展開します。 (つまり `C:\Program Files\RDP Wrapper` に展開します。)
* 5. あなたが使用しているウイルス対策ソフトウェアまたは Windows Defender の例外に以下のディレクトリを追加します。
    * `C:\Program Files\RDP Wrapper`
* 6. `autoupdate.bat` を管理者権限で実行します。
    * これまでの手順を推奨通りに行っている場合、このファイルは `C:\Program Files\RDP Wrapper` に保存されています。