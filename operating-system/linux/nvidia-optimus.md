---
title: Linux 環境で dGPU (NVIDIA Optimus) を使用してアプリケーションを起動する
description: 
published: true
date: 2022-01-28T04:31:23.207Z
tags: linux, nvidia, nvidia-optimus
editor: markdown
dateCreated: 2022-01-28T04:31:23.207Z
---

![06a0ba4e7a3777b3d139db301e68d96f-png.png](/images/06a0ba4e7a3777b3d139db301e68d96f-png.png)

#### 方針
* 軽量なアプリケーションでは iGPU を使用します。(今回は Intel HD Graphics 4600)
* 重量級のアプリケーションでは dGPU を使用します。(今回は NVIDIA GeForce GTX 850M)

#### 手順
1. オープンソースの GPU ドライバーをインストールします。
* **重要: プロプライエタリのドライバーを使用しないでください。**
    * 例として、Arch Linux の場合は、`nvidia` パッケージをインストールしないでください。
* インストールは、次のコマンドを用いて行うことができます。(Arch Linux, pacman)
    * `sudo pacman -S mesa lib32-mesa xf86-video-nouveau xf86-video-intel`
* ドライバーのインストールが完了したら、変更をシステムに反映させるため再起動します。
2. PRIME を使用して、iGPU と dGPU を連携させます。<br>
* はじめに、2つの GPU が認識されていることを確認します。
    * `xrandr --listproviders` を実行してください。
    * 表示されない場合、`/etc/modprobe.d` や `/usr/lib/modprobe.d` の中に `nouveau` カーネルモジュールを無効にしている記述が存在していないか確認してください。
* PRIME GPU オフロード という機能を使用して、レンダリングデバイス (NVIDIA) からシンクプロバイダ (= ディスプレイが接続されている GPU, Intel) にアプリケーションの出力を送信します。
    * この設定は、次のコマンドで行うことができます。
        * `xrandr --setprovideroffloadsink nouveau Intel`
    * 次のコマンドを使用して、正常に設定が完了したことを確認します。
        * `DRI_PRIME=1 glxinfo | grep "OpenGL renderer"`
        ![8abf9267ed6c0e6b58164a248905bc47.png](/images/8abf9267ed6c0e6b58164a248905bc47.png)
3. dGPU を使用して、アプリケーションを起動します。<br>
* 基本的には、`DRI_PRIME` の環境変数を `1` に設定すると使用できます。
* 例えば、Minecraft を dGPU で起動するには、次のようにします。
    * `env DRI_PRIME=1 minecraft-launcher`