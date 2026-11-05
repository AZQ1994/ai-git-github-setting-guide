# Coding Agent 用 Git / GitHub 初期設定ガイド

非技術者が Codex や Claude Desktop の `Code` タブにそのまま頼める、短いプロンプト集です。

まっさらなPCを前提にしています。アプリを入れてプロンプトを貼れば、あとはブラウザで許可するだけです。

![全体の流れ](assets/overview-ja.svg)

## ガイド

| OS | 日本語 | 中文 |
| --- | --- | --- |
| Mac | [mac-ja.md](mac-ja.md) | [mac-zh.md](mac-zh.md) |
| Windows | [windows-ja.md](windows-ja.md) | [windows-zh.md](windows-zh.md) |

## 使い方

1. 自分のOSと言語のページを開く
2. Codex または Claude Desktop を入れる（Windows は Git for Windows も）
3. ページ内のプロンプトをコピーして、Codex または Claude Desktop の `Code` タブに貼る（書き換え不要）
4. ブラウザで認証コードを入れて GitHub を許可する

プロンプトは1行だけです。AIが手順書 [agent-setup.md](agent-setup.md) を読み、SSH鍵の作成と GitHub への登録、名前とメールの設定まで `gh`（GitHub CLI）で行います。公開鍵のコピペは不要です。

コミットのメールアドレスには、自分のアドレスが公開されない GitHub の noreply アドレスを使います（すでに `git config` に設定があれば、そのまま使います）。

## 公式リンク

- [Codex - Get started](https://openai.com/codex/get-started/)
- [Claude Desktop - Install](https://support.anthropic.com/en/articles/10065433-installing-claude-for-desktop)
- [Claude Code Desktop](https://code.claude.com/docs/en/desktop)
- [Git - Downloads](https://git-scm.com/downloads)
- [GitHub CLI - gh auth login](https://cli.github.com/manual/gh_auth_login)
- [GitHub CLI - gh ssh-key add](https://cli.github.com/manual/gh_ssh-key_add)
- [GitHub CLI - Install](https://github.com/cli/cli#installation)
