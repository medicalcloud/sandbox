---

## 2. 英語版 (README.md)

```markdown
# 📦 Sandbox: A Secure Shell Environment for the AI Era

`sandbox` is a portable shell script designed to execute AI-generated commands and unfamiliar system operations **safely and transparently**.

This tool prevents irreversible accidents on your Linux desktop and records all activities as an "Audit Log."

## ✨ Key Features

### 1. 🔍 Pre-execution Preview (Safety Check)
Before executing `rm`, the script lists all files targeted for deletion. This physically prevents accidental data loss caused by incorrect wildcard (`*`) expansions.

### 2. 🛡️ System Protection & Auto-Backup
Restricts write access to critical system directories such as `/etc`, `/boot`, and `/usr`. Additionally, it automatically backs up files to `~/.sandbox_backup/` before moving (`mv`) or copying (`cp`) them.

### 3. ♻️ Prevention of Irreversible Deletion
Instead of permanent deletion, `rm` is redirected to `trash-cli`. You can easily restore files from your GUI trash bin if a mistake occurs.

### 4. 📝 Automatic Audit Logging
All inputs and outputs (commands and results) during the session are automatically saved to `$HOME/.sandbox_logs/`. This log is invaluable for post-task analysis by AI or as a personal reference.

## 🚀 How to Use

### Installation
Grant execution permission to the script:

```bash
chmod +x sandbox
