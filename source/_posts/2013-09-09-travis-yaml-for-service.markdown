---
layout: post
title: ".travis.ymlのギャラリー"
date: 2013-09-09 01:18
comments: true
author: sanemat
categories:
---
こんにちは。さねまつです。

`.travis.yml`のギャラリー作ってます。オーマイグラスの.travis.ymlはこんなかんじです。

```yaml
language: ruby
rvm:
  - 2.0.0
env:
  - DB=mysql
before_install: gem install bundler --pre
before_script:
  - cp config/database.yml.example config/database.yml
  - cp config/settings.yml.example config/settings.yml
  - export DISPLAY=:99.0
  - sh -e /etc/init.d/xvfb start
  - RAILS_ENV=test bundle exec rake 'parallel:create[4]' 'parallel:load_schema[4]' 'parallel:prepare[4]'
bundler_args: --deployment --without development production --jobs=4
notifications:
  email:
    - notify@example.com
script: bundle exec parallel_test -n 4 -t rspec spec
branches:
  only:
    - master
```

サービスレベルで実運用してる`.travis.yml`見たいですよね!!!
他にもご存知でしたらpull requestください。
https://github.com/sanemat/soryu

![soryu](/images/submarine_400x300.jpg 'soryu')

以上デース
