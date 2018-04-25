# Windows
## 開発環境構築の準備
[@srpkdyy](https://github.com/srpkdyy)が作ってくれた[こちら](https://github.com/kure-kosen/cho_kure_setup_for_windows)のシェルスクリプトを使用する。

```bash
mkdir ~/workspace
cd ~/workspace
git clone git@github.com:kure-kosen/cho_kure_setup_for_mac.git
cd cho_kure_setup_for_windows
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