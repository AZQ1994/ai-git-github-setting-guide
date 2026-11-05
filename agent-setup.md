# Git / GitHub setup instructions for coding agents

The user is a beginner who asked you to follow this file. Goal: Git works and this computer connects to GitHub over SSH.

Do everything yourself. Reply in the language the user wrote in, using simple words. The user only needs to act for the browser authorization, and for installer screens or password prompts.

## Steps

1. Check that `git` and `gh` are available.
   - Mac: install anything missing with Homebrew (install Homebrew first if needed).
   - Windows: the user installs Git for Windows manually. If `git` is missing, ask them to install it from https://git-scm.com/downloads/win and reopen this app. Install `gh` with `winget install --id GitHub.cli`. If `gh` is not found right after installing, reopen the terminal or use its full path. Use PowerShell or Git Bash.
2. Log in to GitHub.
   - If `gh auth status` shows a login, do not log in again. If `admin:public_key` is missing, run `gh auth refresh --hostname github.com --scopes admin:public_key` in the background and handle its one-time code as below. Then run `gh config set git_protocol ssh`.
   - Otherwise run `gh auth login --web --git-protocol ssh --scopes admin:public_key` in the background. Give the user the one-time code and https://github.com/login/device, then wait for them to authorize.
3. If `user.name` or `user.email` is missing from `git config --global`, set it from `gh api user`: name is `name` (or `login` if empty), email is `<id>+<login>@users.noreply.github.com`. Do not change existing values.
4. If `~/.ssh` already has a key, use it and never overwrite it. Otherwise create an ed25519 key with no passphrase.
5. Add the public key with `gh ssh-key add`, titled `Mac` or `Windows`. Skip this if the key is already on the account.
6. Confirm with `ssh -o StrictHostKeyChecking=accept-new -T git@github.com`. Success is the text `successfully authenticated`; this command exits with code 1 even on success.

## Rules

- Never display or send a private key.
- If an installer screen or password prompt appears, tell the user what to do and let them do it.
- When finished, say in one or two sentences what was set up.
