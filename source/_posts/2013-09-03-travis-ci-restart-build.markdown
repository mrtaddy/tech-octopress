---
layout: post
title: "テストを落としたのでTravis-CIのbuildを再キックする"
date: 2013-09-03 23:46
comments: true
author: sanemat
categories:
---
こんにちは。さねまつです。

Travis-CIでテストを落とした時に、capybaraか何かタイミングが!(だからオレは悪くない!)と思い込めたら、'restart build'を選んでbuildを再キックします。

![restart-build](/images/travis-pro_400x400.gif 'restart')

Restart Buildは、自分にadmin権限あればrestartできます。権限足りないと押せないみたい。
[cli client](https://github.com/travis-ci/travis)からだと
`$ travis restart 57.1` で実行できるらしい READMEより

弊社オーマイグラスは[Travis PRO](http://travis-ci.com/)使ってます。ただしrestart buildはpro関係ない。

pro関係あるのは、feedback & support のtabです。ここからメッセージを送ると、サポート宛にチケットが切られて、メールでやりとりします。ぼくがオーマイグラスにJoinしてからの一年弱で2回問い合わせしてます。開発者がそのまま返事くれるので、伝言ゲームにならないのがよかったです。

以上デース
