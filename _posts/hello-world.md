---
title: 'Viewbag'
excerpt: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Praesent elementum facilisis leo vel fringilla est ullamcorper eget. At imperdiet dui accumsan sit amet nulla facilities morbi tempus.'
coverImage: '/assets/blog/hello-world/cover.jpg'
date: '2023-09-28T05:35:07.322Z'
author:
  name: Hikari
  picture: '/assets/blog/authors/IMG_5429.png'
ogImage:
  url: '/assets/blog/hello-world/cover.jpg'
---

# NET Coreのビューからコントローラにデータを渡すためのダイナミックなコンテナ

- ViewBagと呼ばれるものは、MVC モデルのModelに含まれない変数
- ControllerからViewに渡してあげるために使われる変数
- 似たものにはViewDataがある

# 実際の利用方法

Controller↓
```
public ActionResult Index()
{
    ViewBag.data = "Hello,World";
    return View(p);
}
```

View↓
```
<p>@ViewBag.data</p>
```
# 特徴
- nullチェックの必要がない
- ControllerBaseクラスのプロパティ

# デメリット
- どちらの方法も実行時に動的に解決されるため、実行時エラーが発生しやすくなる
# メリット
- キャストが必要ない



