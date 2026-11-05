# Windows: Git / GitHub 初始设置

适合从全新 Windows 电脑开始的人。需要一个 GitHub 账号（还没有的话，先到 [github.com](https://github.com/) 注册）。

![Windows 流程](assets/windows-zh.svg)

## 1. 安装应用

安装其中一个，然后登录。

- Codex: 从 [Codex - Get started](https://openai.com/codex/get-started/) 安装桌面应用，用 ChatGPT 账号登录
- Claude: 从 [Claude Desktop - Install](https://support.anthropic.com/en/articles/10065433-installing-claude-for-desktop) 安装 Windows 版，用 Claude 账号登录，打开 `Code` 标签

## 2. 安装 Git for Windows

从 [Git - Downloads](https://git-scm.com/downloads/win) 下载并安装，选项全部保持默认。安装完成后，重新打开 Codex 或 Claude Desktop。

## 3. 把提示词发给 AI

直接复制，粘贴到 Codex 或 Claude 的 `Code` 标签，不需要修改。

```text
请帮我设置 Git 和 GitHub。请读取这份文档，并按照里面的步骤执行: https://raw.githubusercontent.com/AZQ1994/ai-git-github-setting-guide/main/agent-setup.md
```

## 4. 在浏览器里授权

AI 显示验证码（8 位）后，这样操作:

1. 打开 AI 给出的页面，登录 GitHub
2. 输入验证码
3. 点击 `Authorize github`

之后回到 AI，等它显示连接成功就完成了。添加好的 key 可以在 GitHub 的 `Settings` > `SSH and GPG keys` 里确认。
