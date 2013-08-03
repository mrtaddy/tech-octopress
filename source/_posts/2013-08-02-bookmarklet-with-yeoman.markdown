---
layout: post
title: "なかむらくんに通報する、あるいはYeomanでbookmarkletを作る"
date: 2013-08-02 16:40
comments: true
author: sanemat
categories:
---
こんにちは。さねまつです。

商品情報簡単に編集できるといいね、ということでなかむらくんに通報するためのbookmarkletをいくつか作りました。

### なかむらくんに通報する

![なかむらくんに通報する](/images/police_400x483.jpg 'police')

技術的にはYeomanでbookmarkletを作ってみた話です。もう少し細かく言うと、yoでbookmarklet用のtempleateをgenerateして、gruntで変更をwatch, 変更あったらminifyしてbookmarkletとして出力しています。変更をwatch~というのもgenerateしたtemplateに書いてあるので、やるのは `grunt server` 実行するだけです。

[商品情報をアラートするブックマークレット](https://github.com/mrtaddy/omg-copy-sku)

#### 使い方

1. bookmarkletを登録します。(dist/bookmarklet.js)
2. [商品ページ](http://www.ohmyglasses.jp/products/plus-omg-OMG-004-1)を開きます。
3. bookmarkletを実行すると、ページ内の商品情報をスクレイピングしてalertします。

#### 仕組み

```bash
yo bookmarklet # bookmarklet用のtemplateをgenerate
grunt server
```

app/main.js を編集していくと保存するたびに dist/bookmarklet.js にbookmarkletを作成します。処理内容はgeneratorがGruntfile.js を生成していて、そこに書いてあります。

coffeescriptで書けたらいいなーというのはgruntfile書けば良さそうで、あとGruntfile自体もcoffeeで書けるそうだ(伝聞)。

#### see

* [Node.js - Yeomanのあれこれ - Qiita [キータ]](http://qiita.com/sys1yagi/items/4d8c2994580c274fd3fa)
* [JavaScript - Bookmarklet作るのにYeoman使ってみる - Qiita [キータ]](http://qiita.com/Layzie/items/5c4af49ef083b2c1cbf0)

### その他なかむらくんに通報するtips

#### なかむらくんに通報するブックマーク

https://mail.google.com/mail/?view=cm&fs=1&to=nakamura@example.com&cc=ops@example.com&su=%e5%95%86%e5%93%81%e3%83%87%e3%83%bc%e3%82%bf%e3%81%ab%e3%83%9f%e3%82%b9%e7%99%ba%e8%a6%8b&body=&tf=1

こちらはリンクだけ。やりたいことを最短で満たしたしいいやこれで。

#### 管理画面のeditページ直接開くbookmarklet

商品ページからjQueryで要素拾って、管理画面の対応するeditページをopen

#### 画像を横並びに比較して間違いに気づきやすいview

- controllerはadmin側
- model, serviceは検索で使ってるものと同じ
- viewがちょっと違う
- だいたい[これ](http://www.ohmyglasses.jp/search/frame/mens?color%5B%5D=black&color%5B%5D=gray&shape=wellington)の別view

編集ページのパーマリンクへリンクあり

### 実現したストーリー

before:

* 商品情報が間違っているのを見つけた!
* どこに書いていいかわからない… 直していいかわからない… 直すのだるい…
* 間違ってるから直してって言われたけどどの商品のどこだっけ

after:

* 商品情報が間違っているのを見つけた!
* 自分でedit, キャッシュも消す
* コピペが楽になったので、送って直してもらう場合にもお互い分かりやすい
* ひとまずメールで残る

ﾔｯﾀｰ! (メールってフォーマットだるいですねというのはまた別のお話)

以上デース
