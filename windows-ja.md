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

## 先に Git for Windows を入れる

1. [Git - Downloads](https://git-scm.com/downloads/win) を開く
2. Git for Windowsをダウンロードしてインストールする（インストール中の選択はすべて既定のままでOK）
3. インストール後、Codex または Claude Desktopを開き直す

## GitHubで用意するもの

- GitHubアカウント（まだなければ [github.com](https://github.com/) で作成）

名前とメールアドレスは、AIが途中で質問します。事前に入力しておく必要はありません。

## Codex / Claude の Code タブに貼るプロンプト

そのままコピーして貼るだけです。書き換える場所はありません。

```text
私はWindowsを使っている初心者です。GitHubでコードを扱えるように、GitとGitHubの初期設定をしてください。
最終的に、SSHでGitHubに接続できる状態にしたいです。

Git for Windowsは手動でインストール済みです。そのまま使ってください。再インストールは不要です。
コマンドはPowerShellまたはGit Bashで実行してください。

進め方:
1. Gitが使えること、GitHub CLI（gh）が入っていることを確認する。ghがなければ winget install --id GitHub.cli で入れる。入れた直後に gh が見つからない場合は、ターミナルを開き直すか、フルパスで実行する
2. Gitに設定する名前と、GitHubで使うメールアドレスを私に質問する。すでに git config に設定があれば、それを見せて使ってよいか確認する
3. git config で user.name と user.email を設定する
4. ed25519 のSSH鍵を作る（パスフレーズなしでよい）。すでに鍵があれば上書きせず、そのまま使う
5. gh auth login でGitHubにログインする（GitHub.com、SSH、ブラウザでログイン）。ログイン時の権限に SSH鍵の登録（admin:public_key）を含める
6. gh ssh-key add で、公開鍵をGitHubアカウントに自動で登録する。Title は「Windows」にする
7. ssh -T git@github.com と gh auth status で、接続できたことを確認する

ルール:
- 私が決めることや入力することは、1つずつ、やさしい言葉で質問する
- ブラウザでの操作（認証コードの入力、許可ボタンなど）が必要なときは、何をすればよいか具体的に教える
- gh auth login のように対話が必要なコマンドが実行できないときは、ターミナルでの実行方法を教える
- 秘密鍵（private key）は絶対に表示・送信しない
- インストール画面やパスワード入力が出たら、私が操作する
- 終わったら、何を設定したかを短く説明する
```

## ブラウザでやること

AIから案内があったら、ブラウザで次のように操作します。

1. GitHubにログインする
2. AIが表示した認証コード（8文字）を入力する
3. 権限の確認画面で `Authorize github` を押す

公開鍵をコピーして貼る作業はありません。`gh` が自動でGitHubに登録します。

GitHubへの接続が確認できた、と表示されたら完了です。

登録された鍵は、GitHubの `Settings` > `SSH and GPG keys` で確認できます。
