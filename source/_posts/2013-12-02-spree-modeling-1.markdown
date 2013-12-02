---
layout: post
title: "Spree のモデリング解説 第一弾"
date: 2013-12-02 20:59
comments: true
author: kei-s
categories: 
---

こんにちは。kei-s です。当ブログやっと二人目の執筆者です。

先日 [Kuniaki.rb](http://kuniakirb.doorkeeper.jp/events/6616) というイベントの第一回が開かれ、
そこで [Spree](http://spreecommerce.com/) のモデリングについて LT をしました。

(Spree とはなんぞや、などについては Sapporo RubyKaigi 2012 で発表した資料をご覧ください。 https://speakerdeck.com/kei\_s/ruby-on-rails-and-spree )

<script async class="speakerdeck-embed" data-id="54dc9090245301317cb5020c2f9a5198" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>

(スライドの途中から本題が始まります)

スライド中では、

- `Product` と `Variant`
- `LineItem` と `InventoryUnit`

という対比をしています。
前者の組は、サイト上に掲載する商品に関するモデルです。後者の組は、注文されたアイテムに関するモデルです。
詳しいことはスライドに図示しているので、そちらを見てみてください。

Spree の日本語情報はあまり無いので、第二弾ができるといいなあと思っています。
