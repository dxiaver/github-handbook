# How to Commit and Push Code  
如何提交并推送代码

---

## ✍️ What is a Commit?  
什么是 Commit（提交）？

**commit** in Git is like saving a snapshot of your project at a specific moment.  
**Commit（提交）** 就像是给你项目的某个状态“拍了一张快照”。

Each commit contains:  
每次提交包含：

- A list of changes (what was added, changed, or deleted)  
  更改内容（新增、修改或删除）
- A commit message (a short description)  
  提交信息（对更改的简要描述）
- Metadata (author, time, etc.)  
  元数据（作者、时间等）

---

## 🚀 What is Push?  
什么是 Push（推送）？

**Push** means sending your local commits to the remote GitHub repository.  
**Push（推送）** 指的是将你本地的提交上传到 GitHub 仓库。

> Without pushing, your code changes stay only on your computer.  
> 如果不推送，你的更改只保存在本地，GitHub 上不会看到。

---

## 🔧 Step-by-Step: How to Commit and Push  
逐步指南：如何提交并推送代码

---

###  0. (First Time Only) Connect to Remote Repository  
0. 第一次操作时：关联远程仓库

If your project is created locally with `git init`, you need to connect it to your GitHub repository first:    
如果你的项目是通过 `git init` 本地创建的，需要先连接远程仓库：

```bash
git remote add origin https://github.com/your-name/your-project.git
```

e.g. / 示例

```bash
git remote add origin https://github.com/dxiaver/github-handbook.git
```

这一步是将本地仓库与 GitHub 上的远程仓库绑定起来。

---

### 1. Make Changes in Your Project  
1. 修改你的项目文件  
Add, delete, or edit files in your local repository.  
在本地仓库中添加、删除或修改文件。

---

### 2. Check Status  
2. 检查当前状态

```bash
git status
```
This shows which files have been changed.  
查看哪些文件被修改了。

---

### 3. Stage Files  
3. 添加文件到暂存区（准备提交）
```bash
git add filename
```
e.g. / 示例：  
```bash
git add github-handbook/
```
Or add all files: / 添加所有文件
```bash
git add .
```
这一步告诉 Git：“我要提交这些文件”。

---

### 4. Commit with a Message
4. 提交并添加说明信息
```bash
git commit -m "Your commit message"
```
e.g. / 示例：
```bash
git commit -m "Add introduction section to README"
```
每次提交都应写明更改内容，保持清晰。

---

### 5. Push to GitHub
5. 推送到 GitHub
```bash
git push origin main
```

This will push your commit to the `main` branch on GitHub.  
这会将你的提交推送到远程的 `main` 分支。

---

### 📌 Note
注意：

- In the past, Git used `master` as the default branch.  
  以前 Git 的默认分支是 `master`。

- Now, Git and GitHub use `main` by default for new repositories.  
  现在的新版本 Git 和 GitHub 默认使用 `main` 分支。

> ✅ It is recommended to rename `master` to `main` to keep consistency.  
> ✅ 建议将旧仓库的 `master` 分支改为 `main`，保持一致性。  

### 🔄 How to Rename `master` to `main`
如何将 `master` 改为 `main`

If your local branch is still named `master`, you can rename it like this:  
如果你的本地分支仍叫 `master`，可以这样重命名：

```bash
git branch -m master main          # Rename the branch
git push -u origin main            # Push the new main branch
git push origin --delete master    # (Optional) Delete old master on remote
```

---

If your default branch is still `master`, and you haven’t renamed it, you can also push like this:  
如果你尚未改名，也可以继续使用 `master`：
```bash
git push origin master
```

---

## 💡 (Optional First-Time Push) 
💡（可选）首次推送时使用 `-u` 参数绑定远程分支：
```bash
git push -u origin main
```

This tells Git:  
“From now on, my local `main` branch should track the remote `main` branch.”  
表示：从现在起，本地 `main` 分支将默认对应远程 `main` 分支。


---

## ✅ Example Workflow
提交与推送的完整示例流程：

```bash
git status
git add .
git commit -m "Initial project structure"
git push origin main
```
## 📌 Tips
小贴士：

- Every change requires a new round of `add` → `commit` → `push`  
  每次修改代码都需要重新 `add` → `commit` → `push`

- `commit` saves your changes locally; only `push` uploads to GitHub  
  `commit` 只是本地保存，必须 `push` 才能上传到 GitHub

- Keep commit messages clear and meaningful  
  提交信息应清晰、有意义，方便版本追踪

## 📖 Summary
总结

- Add: Tell Git which files to track  
  `git add`：告诉 Git 哪些文件要提交

- Commit: Save the changes locally with a message  
  `git commit`：本地保存更改并添加说明

- Push: Upload the commit to GitHub  
  `git push`：将更改上传到 GitHub

Now your changes are saved both locally and on GitHub!  
现在你的更改已经保存在本地，并成功同步到 GitHub！

