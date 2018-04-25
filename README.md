# ちょっくれ開発環境構築
説明

## Windows
説明

## Mac
### Homebrewのインストール
[こちら](https://brew.sh/index_ja)を参照
ターミナルなどでコマンドを叩く。

### GitHubの設定
[@kobakazu0429](https://github.com/kobakazu0429)が作ってくれた[こちら](https://github.com/kure-kosen/cho_kure_setup_for_mac)から引用、一部改変。

[GitHub](https://github.com/)のアカウントを作成しておく。
下記コマンドを順に実行する。

```bash
mkdir ~/.ssh
chmod 700 ~/.ssh
cd ~/.ssh
ssh-keygen -t rsa -f github
chmode 600 github
touch config
echo 'Host github.com\n  HostName github.com\n  IdentityFile ~/.ssh/github\n  User git\n' >> config
cat github.pub | pbcopy
```

[GitHub Settings - SSH Keys](https://github.com/settings/keys)へアクセスする。
New SSH key に github.pub をコピーする(上記コマンドを実行していたらすでにコピーされているので貼り付けるだけ)。

```
$ ssh github.com
Hi << Your user id >>! You've successfully authenticated, but GitHub does not provide shell access. Connection to github.com closed.

```

とコマンドを入力して出力が上記のものになったら成功。

下記コマンドを順に実行することで、開発に必要な諸々がインストールされる。
```
mkdir ~/workspace
cd ~/workspace
git clone git@github.com:kure-kosen/cho_kure_setup_for_mac.git
cd cho_kure_setup_for_mac
./setup.sh
```
