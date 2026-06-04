# Mac: Git / GitHub 初期設定

Macをまっさらな状態から始める人向けです。

![Macの流れ](assets/mac-ja.svg)

## 先に入れるアプリ

どちらかを入れて、ログインします。

Codexを使う場合:

1. [Codex - Get started](https://openai.com/codex/get-started/) を開く
2. Codexのデスクトップアプリを入れる
3. ChatGPTアカウントでログインする

Claudeを使う場合:

1. [Claude Desktop - Install](https://support.anthropic.com/en/articles/10065433-installing-claude-for-desktop) を開く
2. Mac用のClaude Desktopアプリを入れる
3. Claudeアカウントでログインする
4. Claude Desktopアプリの `Code` タブを開く

## GitHubで用意するもの

- GitHubアカウント
- GitHubで使うメールアドレス
- Gitに表示したい名前

## Codex / Claude の Code タブに貼るプロンプト

下の `名前` と `メール` だけ自分のものに変えてください。

```text
私はMacを使っています。GitHubでコードを扱えるように初期設定してください。

目的:
- Gitを使える状態にする
- Gitの名前とメールを設定する
- GitHub用のSSH鍵を作る
- SSH公開鍵を表示する
- GitHubの Settings > SSH and GPG keys に貼る手順を案内する
- ssh -T git@github.com で接続確認する

Gitに設定する名前: 名前
GitHubのメール: メール

Gitが入っていなければ、Mac向けの方法で入れてください。
SSH鍵は ed25519 で作ってください。
表示された公開鍵は、私がGitHubにコピーします。
インストール画面やパスワード入力が出たら、私が操作します。
```

## GitHubに貼る場所

1. GitHubを開く
2. 右上のアイコンを押す
3. `Settings` を開く
4. `SSH and GPG keys` を開く
5. `New SSH key` を押す
6. `Title` に `Mac` など分かりやすい名前を入れる
7. `Key type` は `Authentication Key` のままにする
8. `Key` に表示された公開鍵を貼る
9. `Add SSH key` を押す

## 最後にやること

GitHubにSSH公開鍵を貼ったら、Codex または Claude の `Code` タブにこう送ります。

```text
GitHubにSSH公開鍵を追加しました。接続確認してください。
```

GitHubへの接続が確認できた、と表示されたら完了です。
