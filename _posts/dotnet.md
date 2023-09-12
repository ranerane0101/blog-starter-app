---
title: '.NETについて'
excerpt: 'テスト'
coverImage: '/assets/blog/hello-world/cover.jpg'
date: '2023-09-12'
author:
  name: Hikari
  picture: '/assets/blog/authors/IMG_5429.png'
ogImage:
  url: '/assets/blog/hello-world/cover.jpg'
---





## .NETについて

名前のみしか知らなかった為、簡単に調べた内容を残しておく。
そもそも、.NETには.NET Frameworkと.NET CoreとASP.NET Coreがある。

### .NET Frameworkはwindowsでしか動かない
### .NET CoreはMacでも動く
### ASP.NET CoreはMacでも動く

上記3点が最も今私が欲しかった情報だった。

Macで使えないものに今は触れない為Macで使うことのできる上記二つについてもう少しだけ比較すると、

### .NET Coreは.NET Coreはプラットフォーム自体
### ASP.NET CoreはWebアプリケーションフレームワーク

## 下記はRazorと言われるLaravelのBlade、SpringのThymeleaf。

```csharp:hello.cshtml
@page
@model IndexModel
@{
    ViewData["Title"] = "Home page";
}

<div class="text-center">
    <h1 class="display-4">Welcome</h1>
    <p>Learn about <a href="https://docs.microsoft.com/aspnet/core">building Web apps with ASP.NET Core</a>.</p>
</div>
```

@pageはこのファイルがHTMLではなくC#でのRazorであることを示す（LaravelのBlade...etc）

## その他継承の記法

```public class IndexModel : PageModel```