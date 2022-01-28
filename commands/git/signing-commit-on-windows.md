---
title: コミットに署名を行う (on Windows)
description: 
published: true
date: 2022-01-27T05:05:43.440Z
tags: git, gpg
editor: markdown
dateCreated: 2022-01-27T05:05:43.440Z
---

## 方法
1. Chocolatey などから Gpg4Win をインストールする。
`choco install gpg4win`
2. 鍵を生成する。
`gpg --gen-key` → 表示に従う。
3. PC に入っている鍵の一覧を表示する。
`gpg --list-keys` → 鍵の ID を確認する。
4. Git で指定した鍵を使うようにする。 
`git config --global user.signingkey [ステップ 3 で確認した鍵の ID]`
5. コミット時にデフォルトで署名するようにする。 
`git config --global commit.gpgsign true`
6. GitHub 等のリモートに鍵を登録する。
`gpg --armor --export [鍵のID]` でサイトに登録するべき文字列が表示されるので、コピペする。
(7. エラーが発生した場合)
`git config --global gpg.program "gpg コマンドの実行ファイルへのパス"` を実行してみる。

## 参考
* [Git Commit で OpenPGP 署名を行う | text.Baldanders.info](https://text.baldanders.info/openpgp/git-commit-with-openpgp-signature/)