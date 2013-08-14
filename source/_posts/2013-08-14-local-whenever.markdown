---
layout: post
title: "localのcronから朝会を通知したい"
date: 2013-08-14 10:25
comments: true
author: sanemat
categories:
---
こんにちは。さねまつです。

ローカルのcrontab, 特に管理してなくてうっかり消しました。wheneverで書いてリポジトリ管理しておくとうれしいですね。

```ruby
every :weekday, at: '10:15 am' do
  command "echo '朝会です'| #{ENV['PATH_TO_HIPCHAT_CLI_BIN']} -t #{ENV['HIPCHAT_TOKEN']} -r #{ENV['ROOM_AOBA']} -f 'sebastian'"
end
every :thursday, at: '3pm' do
  command "echo 'コードレビューです'| #{ENV['PATH_TO_HIPCHAT_CLI_BIN']} -t #{ENV['HIPCHAT_TOKEN']} -r #{ENV['ROOM_AOBA']} -f 'sebastian'"
end
```

こんな感じ。[sebastian](https://github.com/mrtaddy/sebastian/blob/e6f3ec4ea6a55b319c1250e5b8d9fd79af2c7a55/config/schedule.rb)

heroku エコシステム駆使するとか、空いてるサーバーにいれちゃうとか、ちょっと考えてめんどくさくなったのでローカルのまま運用してます。

### hipchat api

どれ使ってもいいんじゃないでしょうか(未確認)
https://www.hipchat.com/docs/api/libraries

- bash
  - https://github.com/hipchat/hipchat-cli
- ruby
  - https://github.com/hipchat/hipchat-rb
  - https://github.com/czarneckid/hipchat-api

pure rubyの使うと取り回し良さそうなのですが、ひとまずbash版で動いているのでほっといてます。パイプで動くとunixのテコの原理に載ってる気になれてよい。

```bash
echo 'コードレビューです'| ./hipchat_room_message -t TOKEN -r ROOM_NUMBER -f NAME
```

設定管理は大げさじゃないのがいいなと[dotenv](https://rubygems.org/gems/dotenv)使ってます。まあまあ便利。

see: [The Ruby Toolbox - Configuration Management](https://www.ruby-toolbox.com/categories/Configuration_Management)

### ローカルで動かしてる最大の欠点

朝会開始の時間に自分が出社してないと発言しないので、あれだ。可視化されますね。

以上デース
