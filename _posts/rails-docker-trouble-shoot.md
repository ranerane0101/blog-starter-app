---
title: 'Rails Dockerトラブルシューティング'
excerpt: 'テスト'
coverImage: '/assets/blog/hello-world/cover.jpg'
date: '2024-03-31'
author:
  name: Hikari
  picture: '/assets/blog/authors/IMG_5429.png'
ogImage:
  url: '/assets/blog/hello-world/cover.jpg'
---





could not open directory "pg_logical/snapshots": Operation not permitted

docker-compose.ymlnのpostgresSQLのポートマッピングの競合で発生する

他プロジェクトで左のhostパソコンのポート番号を使っていたので被らせないようにすればOK！

```
services:
  db:
    image: postgres
    volumes:
      - ./tmp/db:/var/lib/postgresql/data
    environment:
      - POSTGRES_HOST_AUTH_METHOD=trust
      - POSTGRES_PASSWORD=admin
    ports:
      - "15431:5432" # 他のDockerで環境構築したプロジェクトのモノでは15432だった
```

何が原因で起こったエラーか？
- 一度環境構築する際にあるサイトを見てDockerを使い環境構築をした、その際のdocker-compose.ymlをそのまま使い流用しようとした為    