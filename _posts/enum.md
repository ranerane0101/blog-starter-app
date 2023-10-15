---
title: 'Enum'
excerpt: Enumについて
coverImage: '/assets/blog/preview/cover.jpg'
date: '2023-10-15'
author:
  name: Hikari
  picture: '/assets/blog/authors/IMG_5429.png'
ogImage:
  url: '/assets/blog/preview/cover.jpg'
---
Enum型のDayOfWeek。

SUNDAYなどは列挙子。

SUNDAYなどの初期値はint型

メモリ効率が良い

.csの一ファイルにあるがclassというキーワードが無い

```csharp
using System;

public enum DayOfWeek
{
    SUNDAY,
    MONDAY,
    TUESDAY,
    WEDNESDAY,
    THURSDAY,
    FRIDAY,
    SATURDAY
}

class Program
{
    static void Main()
    {
        DayOfWeek today = DayOfWeek.WEDNESDAY;

        switch (today)
        {
            case DayOfWeek.SUNDAY:
                Console.WriteLine("今日は日曜日です。");
                break;
            case DayOfWeek.MONDAY:
                Console.WriteLine("今日は月曜日です。");
                break;
            case DayOfWeek.TUESDAY:
                Console.WriteLine("今日は火曜日です。");
                break;
            case DayOfWeek.WEDNESDAY:
                Console.WriteLine("今日は水曜日です。");
                break;
            case DayOfWeek.THURSDAY:
                Console.WriteLine("今日は木曜日です。");
                break;
            case DayOfWeek.FRIDAY:
                Console.WriteLine("今日は金曜日です。");
                break;
            case DayOfWeek.SATURDAY:
                Console.WriteLine("今日は土曜日です。");
                break;
            default:
                Console.WriteLine("不明な曜日です。");
                break;
        }
    }
}
```
