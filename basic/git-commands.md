# Common Git Commands Cheat Sheet  
常用 Git 命令速查表

---

## 📦 Project Setup  
📦 项目初始化

### Initialize a new Git repository  
初始化一个新的 Git 仓库：

```bash
git init
```

---

### Clone an existing repository  
克隆一个已有的远程仓库：

```bash
git clone https://github.com/username/repo.git
```

---

## 📄 File Changes  
📄 文件操作与变更

### Check the current status  
查看当前文件状态：

```bash
git status
```

---

### Track a file (stage it for commit)  
添加文件到暂存区：

```bash
git add filename
```

添加所有改动文件：

```bash
git add .
```

---

### Commit changes with a message  
提交更改，并附带说明信息：

```bash 
git commit -m "Your message here"
```

---

### View commit history  
查看提交历史记录：

```bash
git log
```

简洁模式查看历史：

```bash
git log --oneline
```

---

## 🔀 Branching & Merging  
🔀 分支管理与合并

### List all branches  
列出所有分支：

```bash
git branch
```

---

### Create and switch to a new branch  
创建并切换到新分支：

```bash
git checkout -b feature/my-branch
```

---

### Switch to an existing branch  
切换到已有分支：

```bash
git checkout main
```

---

### Merge a branch into the current one  
将某个分支合并到当前分支：

```bash
git merge feature/my-branch
```
e.g. / 示例

```bash
git checkout main         # 切换到 main 分支（如果你不在 main）
git pull origin main      # 先拉一下最新的 main（推荐）
git merge charge          # 把 charge 分支的更改合并进当前 main 分支
```

---

## 🌐 Remote Repositories  
🌐 远程仓库操作

### Add a remote repository  
添加远程仓库地址：

```bash
git remote add origin https://github.com/username/repo.git
```

---

### View remote repositories  
查看当前配置的远程仓库：

```bash
git remote -v
```

---

### Push changes to remote  
推送本地更改到远程仓库：

```bash
git push origin main
```

第一次推送时使用 `-u` 绑定远程分支：

```bash
git push -u origin main
```

---

### Pull the latest changes from remote  
拉取远程仓库的最新更改：

```bash
git pull
```

---

## 🧽 Undo Changes  
🧽 撤销更改

### Unstage a file (remove from staging)  
将文件从暂存区移除（不删除内容）：

```bash
git reset HEAD filename
```

---

### Discard changes in a file  
放弃对某个文件的所有更改：

```bash
git checkout -- filename
```

---

## 🧠 Helpful Extras  
🧠 其他实用命令

### Show current branch  
显示当前所在的分支：

```bash
git branch --show-current
```

---

### See diff between staged and last commit  
查看暂存区与上次提交的差异：

```bash
git diff --cached
```

---

### Rename a branch (e.g., master → main)  
重命名当前分支：

```bash
git branch -m main
```

---

## 📖 Summary  
总结

| 命令 | 功能 |
|------|------|
| git init | 初始化本地仓库 |
| git clone | 克隆远程仓库 |
| git add / commit / push | 添加、提交并推送更改 |
| git branch / checkout / merge | 管理与合并分支 |
| git status / log | 查看状态与历史 |
| git pull / push | 同步远程仓库 |
| git reset / checkout | 撤销更改 |

---

> Practice these commands regularly to gain Git confidence!  
> 多加练习这些命令，你会更熟练掌握 Git！
