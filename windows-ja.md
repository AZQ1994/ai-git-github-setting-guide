# Windows: Git / GitHub 初期設定

Windowsをまっさらな状態から始める人向けです。

![Windowsの流れ](assets/windows-ja.svg)

## 先に入れるアプリ

どちらかを入れて、ログインします。

Codexを使う場合:

1. [Codex - Get started](https://openai.com/codex/get-started/) を開く
2. Codexのデスクトップアプリを入れる
3. ChatGPTアカウントでログインする

Claudeを使う場合:

1. [Claude Desktop - Install](https://support.anthropic.com/en/articles/10065433-installing-claude-for-desktop) を開く
2. Windows用のClaude Desktopアプリを入れる
3. Claudeアカウントでログインする
4. Claude Desktopアプリの `Code` タブを開く

## 先にGit for Windowsを入れる

1. [Git - Downloads](https://git-scm.com/downloads/win) を開く
2. Git for Windowsをダウンロードしてインストールする（インストール中の選択はすべて既定のままでOK）
3. インストール後、Codex または Claude Desktopを開き直す

## GitHubで用意するもの

- GitHubアカウント
- GitHubで使うメールアドレス
- Gitに表示したい名前

## Codex / Claude の Code タブに貼るプロンプト

下の `名前` と `メール` だけ自分のものに変えてください。

```text
私はWindowsを使っています。GitHubでコードを扱えるように初期設定してください。

目的:
- Git for Windowsが使える状態か確認する
- Gitの名前とメールを設定する
- GitHub用のSSH鍵を作る
- SSH公開鍵を表示する
- GitHubの Settings > SSH and GPG keys に貼る手順を案内する
- ssh -T git@github.com で接続確認する

Gitに設定する名前: 名前
GitHubのメール: メール

Git for Windowsは手動でインストール済みです。そのまま使ってください。再インストールは不要です。
SSH鍵は ed25519 で作ってください。
PowerShellまたはGit Bashを使って進めてください。
表示された公開鍵は、私がGitHubにコピーします。
インストール画面やパスワード入力が出たら、私が操作します。
```

## GitHubに貼る場所

1. GitHubを開く
2. 右上のアイコンを押す
3. `Settings` を開く
4. `SSH and GPG keys` を開く
5. `New SSH key` を押す
6. `Title` に `Windows` など分かりやすい名前を入れる
7. `Key type` は `Authentication Key` のままにする
8. `Key` に表示された公開鍵を貼る
9. `Add SSH key` を押す

## 最後にやること

GitHubにSSH公開鍵を貼ったら、Codex または Claude の `Code` タブにこう送ります。

```text
GitHubにSSH公開鍵を追加しました。接続確認してください。
```

GitHubへの接続が確認できた、と表示されたら完了です。
