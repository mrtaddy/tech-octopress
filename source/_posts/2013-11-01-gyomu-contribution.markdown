---
layout: post
title: "ギョームでもcontribution"
date: 2013-11-01 19:44
comments: true
author: sanemat
categories:
---
# ギョームでもcontribution

こんにちは。さねまつです。ギョームのpull requestを思い出しつつ書いてみた。

[![github-contributions](https://gist.github.com/sanemat/7201059/raw/github-contributions.gif)](https://github.com/mrtaddy?tab=members)

# contribution事例

## [kei-s](https://github.com/kei-s)
- [Fix transration in ja spree/spree_i18n](https://github.com/spree/spree_i18n/pull/203)

日本語化だ。

- [Fix for Passenger version 4 barttenbrinke/munin-plugins-rails](https://github.com/barttenbrinke/munin-plugins-rails/pull/21)

passenger v4対応。バージョン上げたらフォーマット変わってmuninで取れなくなった。

## [libkazz](https://github.com/libkazz)
- [Html with microdata, for google SEO zachinglis/crummy](https://github.com/zachinglis/crummy/pull/31)

パンくずリストのmicrodata対応。

## [fukajun](https://github.com/fukajun)
:)

## [sanemat](https://github.com/sanemat)
- [Require version file for checking capistrano version bundler/bundler](https://github.com/bundler/bundler/pull/2616)

バグ修正。bundle --jobs=4 の並列bundle使いたかった。
deploy用のserverにbundler v1.4.0.pre.2 入れた。
そしたらcap deployできなくなった。
1.4.0.rc.1で直ってます!

- [Use line_item price instead of variant price in return_authorization spree/spree](https://github.com/spree/spree/pull/2342)

バグ修正。
一度閉じられたけど食い下がって説明して取り込んでもらった。

## おわり

バグ修正は踏んだからだけなので、普通だナー。
