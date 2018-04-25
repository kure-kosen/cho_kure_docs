# ちょっくれ開発環境構築

## 共通
### GitHubの設定
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

## Windows
[Windows編](/windows.md)にて解説しています。


## Mac
### Homebrewのインストール
[Mac編](/mac.md)にて解説しています。