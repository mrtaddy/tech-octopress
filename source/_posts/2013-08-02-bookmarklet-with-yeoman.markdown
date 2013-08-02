---
layout: post
title: "Bookmarklet-with-Yeoman"
date: 2013-08-02 16:40
comments: true
categories:
---
なかむらくんに通報する、あるいはYeomanでbookmarkletを作る

こんにちは。さねまつといいます。
商品情報簡単に編集できるといいね、ということでbookmarkletいくつか作りました。

商品情報をアラートするブックマークレット

https://github.com/sanemat/omg-copy-sku

プラスオーエムジー ハンナ OMG-004-1【送料無料/返品無料】ユニセックス/ブラック/スクエア/1万円以下｜メガネフレーム通販[OMG]
http://www.ohmyglasses.jp/products/plus-omg-OMG-004-1

商品ページを開いて、bookmarklet動かします。
ページ内の商品情報をスクレイピングしてalertします。

このエントリー通りに使ってみます。
JavaScript - Bookmarklet作るのにYeoman使ってみる - Qiita [キータ] http://qiita.com/Layzie/items/5c4af49ef083b2c1cbf0

yo bookmarklet
grunt server

app/main.js を編集していくと保存するたびに dist/bookmarklet.js にbookmarkletを作成します。
処理内容はgeneratorがGruntfile.js を生成していて、そこに書いてあります。

coffeescriptで書けたらいいなーというのはgruntfile書けば良さそうで、あとGruntfile自体もcoffeeで書けるらしい

なかむらくんに通報するブックマーク

https://mail.google.com/mail/?view=cm&fs=1&to=nakamura@example.com&cc=ops@example.com&su=%e5%95%86%e5%93%81%e3%83%87%e3%83%bc%e3%82%bf%e3%81%ab%e3%83%9f%e3%82%b9%e7%99%ba%e8%a6%8b&body=&tf=1

こちらはブックマークだけです。やりたいことを満たす最短はコレ。
