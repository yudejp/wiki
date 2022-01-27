---
title: 別リポジトリにあるディレクトリを他のリポジトリで既に使用中のドメインのサブディレクトリとして GitHub Pages で公開する
description: 
published: true
date: 2022-01-27T05:04:55.524Z
tags: git, github, github-pages
editor: markdown
dateCreated: 2022-01-27T05:04:55.524Z
---

## gh-pages ブランチ (または公開したいブランチ) を submodule として追加する。
 1. 使用中のドメインのディレクトリに入る。
 2. 以下のコマンドを実行する。
  `git submodule add -b gh-pages (別リポジトリにあるディレクトリ) ./(公開するサブディレクトリの名前)`