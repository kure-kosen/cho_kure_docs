# Mac
## 開発環境構築の準備
[@kobakazu0429](https://github.com/kobakazu0429)が作ってくれた[こちら](https://github.com/kure-kosen/cho_kure_setup_for_mac)から引用、一部改変。
下記コマンドを順に実行することで、開発に必要な諸々がインストールされる。

```bash
mkdir ~/workspace
cd ~/workspace
git clone git@github.com:kure-kosen/cho_kure_setup_for_mac.git
cd cho_kure_setup_for_mac
./setup.sh
```

## 開発環境構築

```bash
cd ~/workspace

git clone git@github.com:kure-kosen/cho_kure_web.git
cd cho_kure_web

gem install bundler
bundle install

yarn install

bin/setup

bundle exec reails db:seed_fu
```

おわり。
