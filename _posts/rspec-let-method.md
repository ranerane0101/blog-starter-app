---
title: 'letメソッドについて'
excerpt: 'テスト'
coverImage: '/assets/blog/hello-world/cover.jpg'
date: '2024-03-31'
author:
  name: Hikari
  picture: '/assets/blog/authors/IMG_5429.png'
ogImage:
  url: '/assets/blog/hello-world/cover.jpg'
---





# Rspec letとlet!の違い

## let

- 定義した定数が呼ばれたときに評価される
- 遅延評価
- テストが実行される前にレコードが読み込まれない

## let!

- before do~endみたいなもの
- 事前評価
- テストが実行される前に自動的にテストレコードが読み込まれる

