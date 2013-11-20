---
layout: post
title: "rake stats"
date: 2013-11-20 12:50
comments: true
author: sanemat
categories:
---
こんにちは。さねまつです。弊社サービスで一番大きいのはspreeを使ったアプリケーションです。
[![omg-mono-app](/images/omg-mono-app_800x600.gif)](http://www.ohmyglasses.jp)

それ以外に、sinatraで商品画像確認・rails4でデータ周りを扱うなどの衛星アプリがあります。まだ一つの巨大なアプリでギリギリまかないきれる感じですね。まかないきれてるのかな。いつかはSOA。

see: [I-Tier: Dismantling the Monoliths - Groupon Engineering Blog](https://engineering.groupon.com/2013/misc/i-tier-dismantling-the-monoliths/)

一番大きいアプリケーションのrake stats:

```text
$ bundle exec rake stats
+----------------------+-------+-------+---------+---------+-----+-------+
| Name                 | Lines |   LOC | Classes | Methods | M/C | LOC/M |
+----------------------+-------+-------+---------+---------+-----+-------+
| Controllers          |  4393 |  3456 |      58 |     396 |   6 |     6 |
| Helpers              |   925 |   720 |       0 |      87 |   0 |     6 |
| Models               |  8680 |  6763 |     189 |     789 |   4 |     6 |
| Libraries            |  9723 |  8065 |     118 |     409 |   3 |    17 |
| Controller specs     |  1207 |   985 |       0 |       1 |   0 |   983 |
| Feature specs        |  6177 |  4627 |       0 |       5 |   0 |   923 |
| Helper specs         |   398 |   351 |       0 |       0 |   0 |     0 |
| Lib specs            |  1182 |  1005 |       0 |       0 |   0 |     0 |
| Model specs          | 12829 | 10834 |       0 |      23 |   0 |   469 |
| Routing specs        |    13 |    11 |       0 |       0 |   0 |     0 |
| Service specs        |  1508 |  1283 |       0 |       0 |   0 |     0 |
| Validator specs      |    50 |    44 |       0 |       0 |   0 |     0 |
| View specs           |   119 |    89 |       0 |       0 |   0 |     0 |
+----------------------+-------+-------+---------+---------+-----+-------+
| Total                | 47204 | 38233 |     365 |    1710 |   4 |    20 |
+----------------------+-------+-------+---------+---------+-----+-------+
  Code LOC: 19004     Test LOC: 19229     Code to Test Ratio: 1:1.0
$ date
2013年 11月19日 火曜日 13時21分26秒 JST
```

see: [求人の際に「自社のコードベースがどれくらい健全か」というのをアピールする視点を持つとよいのではないか、と思いました。 - Sooey](http://journal.sooey.com/229)

いや、一番大きいコードベースはWordPressな気もする… [メガネスタイルマガジンOMG PRESS](http://www.ohmyglasses.jp/blog/)
