---
title: 'エラーハンドリング'
excerpt: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Praesent elementum facilisis leo vel fringilla est ullamcorper eget. At imperdiet dui accumsan sit amet nulla facilities morbi tempus.'
coverImage: '/assets/blog/dynamic-routing/cover.jpg'
date: '2020-03-16T05:35:07.322Z'
author:
  name: Hikari
  picture: '/assets/blog/authors/IMG_5429.png'
ogImage:
  url: '/assets/blog/dynamic-routing/cover.jpg'
---
エラーハンドリングについて

業務でnullReferenceExceptionが発生しその対処の調査を備忘として

下記はcatchブロッックの中でログを記録している。
これは例外が発生した場合でもユーザーに問題がない時に用いる

## Lorem Ipsum
```csharp:hello.cshtml
try
{
    // ここにエラーが発生する可能性のあるコードを記述します
    var result = 10 / 0; // 0で割り算を試みる例外を発生させます
}
catch (Exception ex)
{
    Log.Error(ex, "エラーが発生しました");
}
```

また、下記はいわゆる「例外を握りつぶす」とされる方法

```csharp:nigiru.cshtml
try
{
    // ここにエラーが発生する可能性のあるコードを記述します
    var result = 10 / 0; // 0で割り算を試みる例外を発生させます
}
catch (Exception ex)
{
    return;
}
```
