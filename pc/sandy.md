---
title: Untitled Page
description: 
published: true
date: 2022-01-25T07:01:33.093Z
tags: 
editor: markdown
dateCreated: 2022-01-25T07:01:33.093Z
---

# sandy
* サーバー (メイン)
![sandy](https://gyazo.com/db5bbab80d6b27be95ec151cfae927d1/max_size/1000)
## スペック
* CPU: [Intel Core i7-2600 @ 3.40GHz](https://ark.intel.com/content/www/jp/ja/ark/products/52213/intel-core-i7-2600-processor-8m-cache-up-to-3-80-ghz.html) (4C/8T)
* RAM: DDR3 4GB * 2 + 8GB * 2 = 24GB
* OS: [Arch Linux](https://www.archlinux.jp/)
* GPU: [NVIDIA GeForce GTX 650](https://www.nvidia.com/en-us/geforce/graphics-cards/geforce-gtx-650/specifications/)
* ストレージ (システム): [Crucial MX500 250GB CT250MX500SSD1](https://www.crucial.jp/ssd/mx500/ct250mx500ssd1)
* ストレージ (録画, VM, 一時保存): [Samsung 850 EVO SSD 256GB MZ-7KE256](https://www.samsung.com/semiconductor/minisite/jp/ssd/consumer/850pro/)
* ストレージ (データ): [Western Digital WD40EZRZ-22GXCB0 4TB](https://kakaku.com/item/K0000927098/)
* ストレージ (データ): [Western Digital WD10EZEX-22MFCA0 1TB](https://www.cfd.co.jp/product/hdd/3_5inch/wd10ezex/)
* ストレージ (データ): [Western Digital WD5000AAKX-00ERMA0 500GB](https://www.tekwind.co.jp/WDC/products/entry_9230.php)

## 歴史
* 2014年7月: 基礎となる構成 i7-2600, 8GB RAM, GTX 650 で組む。当初はサーバー用途ではなく、4代目のメイン PC [富士通 FMV-BIBLO LOOX M/E 10](https://www.fmworld.net/fmv/pcpm0910/looxm/index.html) のリプレース先であったが、当時は知識不足により最後まで組むことができず約4ヶ月放置。そのときの続投先は一旦 [パソコン工房 iiyama 15H7100-i7-VG](https://news.mynavi.jp/article/20140404-a270/) ([pc/saika]) を購入することとなる。放置後構築に再チャレンジし、今度は正常に起動まで持っていくことができた。しかし、そのときは既に十分な性能の PC を手に入れていたため、弟の PC 兼 Minecraft サーバー用として使用されることとなる。当初は Windows 7 Professional がインストールされていた。
* 2015年末: Windows 10 Pro にアップデート。Hyper-V 上に Ubuntu Server をインストールし、その上でサーバーを運用することを決定。
* 2016年末: RAM を 16GB に増設。[PLEX PX-W3U4](http://www.plex-net.co.jp/product/px-w3u4/) 等を導入し、録画サーバーとしての運用も開始。電源の故障により一定期間起動し続けるとシャットダウンしてしまう不具合が発生。電源を [玄人志向 電源 KRPW-BKシリーズ 80PLUS Bronze 650W ATX電源 KRPW-BK650W/85+](https://www.amazon.co.jp/gp/product/B078HDTV8P/) にリプレースし解決。他のパーツを巻き込まず済んだのは非常に幸運だった。
* 2018年: システムをインストールしているストレージを SSD に変更。
* 2019年: ホスト OS を Ubuntu Server に変更。弟は yude が大学受験の影響で [pc/saika] を使用する頻度が低くなったことからそちらを利用するようになり、このマシンから Windows を消し去ることができた。(元々 PLEX PX-W3U4 の Windows 向けデバイスドライバーが極めて不安定で、オープンソースドライバーの [nns779/px4_drv: Unofficial Linux driver for PLEX PX4/PX5/PX-MLT series ISDB-T/S receivers (not V4L-DVB)](https://github.com/nns779/px4_drv) を使用できる Linux 環境にしたいとは思っていたが、弟が Windows を使用するので変更できないでいた。当時は Windows 向け px4_drv は存在していなかった。)
* 2021年: ホスト OS を Arch Linux に変更。[ハル](https://twitter.com/haruLBP) さんから頂いた 8GB の RAM を増設し、計 24GB の RAM を搭載する。ケースを [Fractal Design Define R5](https://shop.tsukumo.co.jp/goods/4537694191098) に変更。