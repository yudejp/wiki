---
title: Docker Compose で構築した Mastodon をアップグレードする
description: 
published: true
date: 2022-02-03T20:35:48.696Z
tags: mastodon, docker, docker-compose
editor: markdown
dateCreated: 2022-02-03T20:34:21.498Z
---

## 手段
1. `docker-compose.yml` を開き、`tootsuite/mastodon` のタグがアップグレードしたいバージョンになっていることを確認する。
    なっていない場合は適宜編集する。
2. 指定したバージョンをダウンロードする。
  ```
  docker-compose pull
  ```
3. データベースのマイグレーションを行う。
  ```
  docker-compose run --rm web rails db:migrate
  ```
4. アセットのプリコンパイルを行う。
  ```
  docker-compose run --rm web rails assets:precompile
  ```
5. コンテナを再起動する。
  ```
  docker-compose stop && docker-compose up -d
  ```