---
title: VMware Workstation Player で Windows 9x 系を動かす
description: 
published: true
date: 2022-01-28T04:11:36.430Z
tags: windows, vmware
editor: markdown
dateCreated: 2022-01-28T04:11:36.430Z
---

#### 知見
* FreeDOS でも動かすことはできる。
* 予め仮想ハードディスクを Windows XP 等から FAT でフォーマットしておく。
* フォーマットした仮想ハードディスクに MS-DOS 6.22 (または FreeDOS) と Windows 95 のセットアップディスクの中身を移しておき、それらを DOS から実行すると、ディスクドライブ等のドライバーに悩まされることがない。
* セットアップ終了後フロッピードライブを切断しないと DOS の画面に戻って起動できなくなる。 (?)
    * プロンプトされるのでそのタイミングで切断すれば良い。
* 万一の時のために起動ディスクは作成しておくべきである。
    * VMware の `flp` ファイルで良い。
    ![flp1.png](/flp1.png)
#### 音が出ない
* VMware Tools をインストールしても、サウンドドライバーはインストールされない。
* 以下の方法では MIDI の音が出ないかもしれないが、起動音や音声ファイル等に関しては再生できる。
    * `ES1371` という型番のデバイスのドライバーをインストールすればよい。
        * 参考: [VMWare に入ったWindows 95用のサウンドドライバ - Windows 2000 Blog](http://blog.livedoor.jp/blackwingcat/archives/1434847.html)
    * ダウンロード先: [Creative Media (Japan) : Customer Support - Drivers & more for all your Creative products](https://jp.creative.com/support/downloads/download.asp?Product_ID=420&Product_Name=Creative+Ensoniq+Audio+PCI&OSName=Windows+98&OS=2&DriverType=0&details=1)
        ![flp2.png](/flp2.png)
#### インターネットに接続する
* 画像のとおりにやればいいですよ
* ![flp3.png](/flp1.png)
##### Internet Explorer 4.0 で接続できた Web サイトの一覧
* [ようこそ AMAKATAs' WEBSITE へ](http://www.asahi-net.or.jp/~mi5k-amkt/)
* [1998特報!!倶楽部](http://www.big.or.jp/~talk/t-club/)
* [阿部寛のホームページ](http://abehiroshi.la.coocan.jp/)
* [侍魂](http://www6.plala.or.jp/private-hp/samuraidamasii/tamasiitop/tamasiitop.htm)
* [kota'sHomePageへようこそ](http://www5.airnet.ne.jp/kota/)
* [ようこそ、幸子のホームページへ](http://ftp.fuchu.or.jp/~sachiko3/index.htm)
* `'s home page　ようこそ` で Google 検索 を行うと、たくさん出てくる。
        * 参考: 懐かしの90年代（〜2000年代初頭）ホームページ