---
layout: post
title: "テストを落としたのでTravis-CIのbuildを再キックする"
date: 2013-09-03 23:46
comments: true
author: sanemat
categories:
---
こんにちは。さねまつです。

Travis-CIでテストを落とした時に、capybaraか何かタイミングのせいで失敗した!(だからオレは悪くない!)と思い込めたら、歯車アイコンの'Restart Build'を選んでbuildを再キックします。

![restart-build](/images/travis-pro_400x400.gif 'restart')

弊社オーマイグラスはprivate なreposもテストしたいので、[Travis PRO](http://travis-ci.com/)使ってます。Restart Buildは、pro関係なく、自分にadmin権限あればrestartできます。権限足りないと押せないみたい。
なお[cli client](https://github.com/travis-ci/travis)からだと
`$ travis restart 57.1` で実行できるらしい READMEより

pro関係あるのは、'feedback & support' のtabです。ここからメッセージを送ると、サポート宛にチケットが切られて、メールでやりとりします。ぼくがオーマイグラスにJoinしてからの一年弱で2回(2012-12-25, 2013-01-30)問い合わせしてます。開発者がそのまま返事くれるので、伝言ゲームにならないのがよかったです(当時)。

タイミングで落ちるテストは近いうちに直します!!!

以上デース
