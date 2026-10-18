# Mac: Git / GitHub 初始设置

适合从全新 Mac 开始的人。

![Mac 流程](assets/mac-zh.svg)

## 先安装应用

安装其中一个，然后登录。

使用 Codex:

1. 打开 [Codex - Get started](https://openai.com/codex/get-started/)
2. 安装 Codex 桌面应用
3. 用 ChatGPT 账号登录

使用 Claude:

1. 打开 [Claude Desktop - Install](https://support.anthropic.com/en/articles/10065433-installing-claude-for-desktop)
2. 安装 Mac 版 Claude Desktop 应用
3. 用 Claude 账号登录
4. 打开 Claude Desktop 应用里的 `Code` 标签

## 需要准备

- GitHub 账号（还没有的话，先到 [github.com](https://github.com/) 注册）

名字和邮箱会由 AI 在过程中询问，不需要提前填写。

## 发给 Codex / Claude 的 Code 标签的提示词

直接复制粘贴即可，不需要修改任何地方。

```text
我是使用 Mac 的新手。请帮我完成 Git 和 GitHub 的初始设置。
最终目标是可以通过 SSH 连接 GitHub。

步骤:
1. 检查 Git 和 GitHub CLI (gh) 是否已安装。没有的话用 Homebrew 安装（没有 Homebrew 就先安装它）
2. 向我询问 Git 要显示的名字，以及 GitHub 使用的邮箱。如果 git config 里已经有设置，先给我看，确认能不能直接用
3. 用 git config 设置 user.name 和 user.email
4. 创建 ed25519 的 SSH key（不设 passphrase 即可）。如果已经有 key，不要覆盖，直接使用
5. 用 gh auth login 登录 GitHub（GitHub.com、SSH、浏览器登录）。登录时的权限要包含上传 SSH key（admin:public_key）
6. 用 gh ssh-key add 把 public key 自动添加到我的 GitHub 账号，Title 用 "Mac"
7. 用 ssh -T git@github.com 和 gh auth status 确认连接成功

规则:
- 需要我决定或输入的内容，一次只问一个，用简单的话
- 需要我在浏览器里操作时（输入验证码、点击授权等），告诉我具体怎么做
- 如果 gh auth login 这类需要交互的命令你无法执行，告诉我怎样在终端里运行
- 绝对不要显示或发送 private key
- 如果出现安装画面或密码输入，由我来操作
- 完成后，简短说明你设置了什么
```

## 在浏览器里要做的事

AI 提示之后，在浏览器里这样操作:

1. 登录 GitHub
2. 输入 AI 显示的验证码（8 位）
3. 在权限确认页面点击 `Authorize github`

不需要复制粘贴 public key，`gh` 会自动把它添加到 GitHub。

显示已经成功连接 GitHub，就完成了。

添加好的 key 可以在 GitHub 的 `Settings` > `SSH and GPG keys` 里确认。
