---
layout: post
title: "hubotの居る生活"
date: 2014-06-20 18:29
comments: true
author: sanemat
categories:
---
こんにちは。さねまつです。Growth Hackerゆるくクビになって5月半ばからエンジニアに戻ってます。

今`hubot-script`ブームが社内でぼくと1syoだけに吹いてます。さらに、「そろそろちゃんとした使えるものを作ってよ(1syo)」と煽られてます。

[omg-hubot](https://github.com/mrtaddy/omg-hubot)

##1syoが作ったリスト

- [travisci](https://github.com/mrtaddy/omg-hubot/blob/42213d04e91d99034631e0d89958df6ad36ab1e9/scripts/travisci.coffee)
- [deploy-announce](https://github.com/mrtaddy/omg-hubot/blob/42213d04e91d99034631e0d89958df6ad36ab1e9/scripts/deploy-announce.coffee)
- [airbrake](https://github.com/mrtaddy/omg-hubot/blob/42213d04e91d99034631e0d89958df6ad36ab1e9/scripts/airbrake.coffee)

##ぼくが作ったリスト

- [hubot-tantanmen](https://github.com/sanemat/hubot-tantanmen)
- [hubot-phonetic-alphabet](https://github.com/sanemat/hubot-phonetic-alphabet)
- [hubot-53cal-jp](https://github.com/sanemat/hubot-53cal-jp)
- [hubot-google-transliterate](https://github.com/sanemat/hubot-google-transliterate)

たしかに!! しかも一番使えるゴミ収集情報botは勝手にページスクレイピングしてて怒られるやつだ。まだまだ作るぞ。

# 背景

最近、エンジニアチャットをhipchatからslack(+hubot)に変えました。

##hipchat pros

- iphoneクライアントの出来が良い push notificationちゃんと来るなど
- 画像を上げると、s3直アドレスになるので、アップローダー代わりになる 特にiphoneからの場合便利
- ユーザー数5までは無料、そこからはユーザー課金(乗り換え2014-05-15当時, 現在2014-06-20はユーザー数無制限)

##slack pros

- ユーザーのアイコンが表示される 重要
- 画像を上げるとslackのユーザー認証が間に入るので、正しい権限のある人だけがアクセスできる
- 他サービスとのintegration 5までは無料、そこからはユーザー課金

slackのintegration課金をひとまずすり抜けようと、通知系をhubotに集約してます。
github, hubot, newrelicの3本に抑えてる。
さてslackの課金体型変わったらどうしよ?

以上デース
