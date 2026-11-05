# Mac: Git / GitHub 初期設定

Macをまっさらな状態から始める人向けです。GitHubアカウントが必要です（まだなければ [github.com](https://github.com/) で作成）。

![Macの流れ](assets/mac-ja.svg)

## 1. アプリを入れる

どちらかを入れて、ログインします。

- Codex: [Codex - Get started](https://openai.com/codex/get-started/) からデスクトップアプリを入れ、ChatGPTアカウントでログインする
- Claude: [Claude Desktop - Install](https://support.anthropic.com/en/articles/10065433-installing-claude-for-desktop) からMac用を入れ、Claudeアカウントでログインして `Code` タブを開く

## 2. プロンプトをAIに貼る

そのままコピーして、Codex または Claude の `Code` タブに貼ります。書き換える場所はありません。

```text
GitとGitHubの設定をお願いします。次の手順書を読んで、そのとおりに実行してください: https://raw.githubusercontent.com/AZQ1994/ai-git-github-setting-guide/main/agent-setup.md
```

## 3. ブラウザで許可する

AIが認証コード（8文字）を表示したら、次のように操作します。

1. AIが案内したページを開いて、GitHubにログインする
2. 認証コードを入力する
3. `Authorize github` を押す

あとはAIに戻り、接続できたと表示されたら完了です。登録された鍵は、GitHubの `Settings` > `SSH and GPG keys` で確認できます。
