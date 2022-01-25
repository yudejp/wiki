---
title: Google Pixel 5a (5G) に Floko v4 をインストール
description: 
published: true
date: 2022-01-25T04:33:24.886Z
tags: flokorom, barbet, pixel, custom-rom
editor: markdown
dateCreated: 2022-01-25T04:33:24.886Z
---

# 環境
イメージのビルドを行わない手段を使用するので、あまり関係ないとは思いますが...
* 端末: Google Pixel 5a (5G) 128GB
* OS: WSL 2 on Windows 11

`adb`, `fastboot` コマンドが実行でき、かつ実端末上に対してそれらが実行できることを確認してください。

# 方法
* 自己責任でお願いします。
## 1. 必要なファイルのダウンロード
### FlokoROM GSI
* [FlokoROM GSI](https://treble.andro.plus/)
### LineageOS Recovery (barbet 用)
* [lineage-18.1-20220120-recovery-barbet.img](https://mirrorbits.lineageos.org/recovery/barbet/20220120/lineage-18.1-20220120-recovery-barbet.img)
### `vbmeta.img`
1. まず、以下のページから barbet 向けファクトリイメージをダウンロードします。
[Factory Images for Nexus and Pixel Devices  |  Google Play services  |  Google Developers](https://developers.google.com/android/images)
1. ダウンロードした zip ファイルの中にある `` を取り出し、解凍します。
1. `vbmeta.img` を取得できます。
### `product_gsi.img`
Google Pixel 5a (5G) の既定のパーティション構成では、Magisk 等をインストールする空き容量が残されていません。
このイメージは、`product` パーティションを FlokoROM GSI のフラッシュ時に可能な限り縮小し、空き容量を作る役割を担います。

以下のページからダウンロードします。
* [[Tutorial] Magisk on GSI on devices with dynamic partition | XDA Forums](https://forum.xda-developers.com/t/tutorial-magisk-on-gsi-on-devices-with-dynamic-partition.4311045/)
### (必要な場合: Magisk, MagiskGapps)
* [Magisk](https://github.com/topjohnwu/Magisk/releases) (ファイル名: `Magisk-v[version].apk`)
* [MagiskGapps](https://mg.pixel-fy.com/download.html) (ファイル名: `MagiskGApps-[edition]-V[version].zip`)
MagiskGapps については、core バージョンでの動作を確認しています。

## 2. ROM のインストール
1. `adb reboot fastboot` を Android が起動し、かつ開発者向けモードが有効になっている状態で実行します。
2. fastbootd に遷移したことを確認したら、`fastboot flash product product_gsi.img` を実行し、product 領域にパーティション空き容量の対策のためのイメージを書き込みます。
3. 