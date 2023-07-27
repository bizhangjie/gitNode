在Git中登录GitHub通常涉及使用SSH密钥或用户名密码进行认证。以下是两种常见的登录方式：

**1. 使用SSH密钥认证**：

在GitHub上使用SSH密钥认证可以免去每次操作都需要输入用户名密码的步骤，提供了更方便且安全的方式。

**步骤1：生成SSH密钥**：
首先，检查本地是否已经有SSH密钥。在终端或命令行中运行以下命令：
```
ls ~/.ssh
```
如果没有显示任何文件，则表示没有SSH密钥，可以生成一个新的密钥。

生成SSH密钥，运行以下命令：
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
将`your_email@example.com`替换为你的GitHub邮箱地址。按照提示选择保存密钥的位置和设置密码（可选）。

**步骤2：添加SSH密钥到GitHub账号**：
打开生成的SSH密钥文件（默认在`~/.ssh/id_ed25519.pub`），复制公钥内容。

登录GitHub账号，转到"Settings" -> "SSH and GPG keys" -> "New SSH key"，粘贴复制的SSH公钥内容，并保存。

**步骤3：测试SSH连接**：
运行以下命令测试SSH连接：
```
ssh -T git@github.com
```
你将会收到一条欢迎消息，表示SSH连接已经成功建立。

**2. 使用用户名密码认证**：

使用用户名密码认证在某些情况下可能会比较繁琐，但也是一种有效的登录方式。

**步骤1：在终端或命令行中运行以下命令**：
```
git config --global user.name "YourGitHubUsername"
git config --global user.email "your_email@example.com"
```
将`YourGitHubUsername`替换为你的GitHub用户名，`your_email@example.com`替换为你的GitHub邮箱地址。

**步骤2：进行第一次推送**：
在你的本地代码库中进行第一次提交，并将其推送到GitHub远程仓库：
```
git add .
git commit -m "Initial commit"
git push -u origin main   # 或 master，具体取决于你的默认分支名称
```
Git会提示你输入用户名和密码，输入GitHub账号的用户名和密码即可。

以上是在Git中登录GitHub的两种常见方式。SSH密钥认证提供了更方便和安全的方式，特别是对于频繁进行Git操作的用户。使用用户名密码认证也是一种有效的方式，尤其是在不需要频繁进行Git操作的情况下。选择哪种方式取决于你的偏好和具体需求。