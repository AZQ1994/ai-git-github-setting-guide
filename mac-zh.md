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

- GitHub 账号
- GitHub 使用的邮箱
- 想显示在 Git 里的名字

## 发给 Codex / Claude 的 Code 标签的提示词

把下面的 `名字` 和 `邮箱` 改成你自己的。

```text
我使用 Mac。请帮我完成 GitHub 代码使用的初始设置。

目标:
- 让 Git 可以使用
- 设置 Git 的名字和邮箱
- 为 GitHub 创建 SSH key
- 显示 SSH public key
- 告诉我怎样把 public key 粘贴到 GitHub 的 Settings > SSH and GPG keys
- 用 ssh -T git@github.com 确认连接

Git 使用的名字: 名字
GitHub 邮箱: 邮箱

如果还没有安装 Git，请用适合 Mac 的方式安装。
SSH key 请使用 ed25519。
显示出来的 public key 由我复制到 GitHub。
如果出现安装画面或密码输入，我来操作。
```

## 粘贴到 GitHub 的位置

1. 打开 GitHub
2. 点击右上角头像
3. 打开 `Settings`
4. 打开 `SSH and GPG keys`
5. 点击 `New SSH key`
6. 在 `Title` 输入容易识别的名字，比如 `Mac`
7. `Key type` 保持 `Authentication Key`
8. 在 `Key` 粘贴显示出来的 public key
9. 点击 `Add SSH key`

## 最后一步

把 SSH public key 粘贴到 GitHub 后，发给 Codex 或 Claude 的 `Code` 标签:

```text
我已经把 SSH public key 添加到 GitHub。请确认连接。
```

如果显示已经成功连接 GitHub，就完成了。
