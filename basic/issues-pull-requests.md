# Using Issues and Pull Requests on GitHub  
GitHub 中的 Issues 与 Pull Requests 使用指南

---

## 🐞 What Are Issues?  
什么是 Issues（问题）？

**Issues** are used to track bugs, tasks, feature requests, or general discussion in a GitHub repository.  
**Issues** 用于在 GitHub 仓库中追踪 Bug、任务、功能建议或进行讨论。

Typical use cases:  
常见用途：

- Report a bug or problem  
  报告一个问题或错误  
- Propose a new feature  
  提出一个新功能建议  
- Ask a question or start a discussion  
  提问或发起讨论  
- Assign tasks to team members  
  指派任务给团队成员

---

## 📝 How to Create an Issue  
如何创建一个 Issue：

1. 打开仓库主页（如：https://github.com/username/repo）
2. 点击上方的 **"Issues"** 标签页  
3. 点击绿色按钮 **"New issue"**  
4. 填写标题和描述内容，可以添加标签、指派协作者、设置里程碑等  
5. 点击 **"Submit new issue"** 提交问题

> 🧠 Good practice: Use clear, descriptive titles and step-by-step problem descriptions.  
> 🧠 最佳实践：标题清晰，描述中包含复现步骤和预期结果。

---

## ✅ What Is a Pull Request (PR)?  
什么是 Pull Request（拉取请求）？

A **Pull Request** lets you propose code changes from one branch to another. It is the core of collaboration on GitHub.  
**Pull Request（PR）** 是一种提交代码更改提案的方式，是 GitHub 协作开发的核心。

Typical PR flow:  
PR 工作流程：

- Make changes in a feature branch  
  在一个功能分支中进行更改  
- Push the branch to GitHub  
  将分支推送到 GitHub  
- Create a pull request targeting `main`  
  创建一个 PR，请求合并到主分支  
- Review, discuss, and approve the code  
  审查、讨论并批准代码  
- Merge the pull request  
  合并该请求，代码正式更新

---

## 🌿 How to Create a Pull Request  
如何创建一个 Pull Request：

### 1. Create and switch to a new branch  
创建并切换到新分支：

```bash
git checkout -b feature/my-change
```

### 2. Make changes and commit them  
修改代码并提交：

```bash
git add .  
git commit -m "Add my feature"
```

### 3. Push the branch to GitHub  
将分支推送到远程仓库：

```bash
git push origin feature/my-change
```

### 4. Open GitHub and create a PR  
在 GitHub 仓库页面中会看到提示：**“Compare & pull request”**  
点击它，填写 PR 标题与描述，然后点击 **“Create pull request”**

---

## 🔍 Reviewing a Pull Request  
如何审查一个 PR：

- 点击 PR 页面 → 查看文件改动（Files changed）  
- 添加评论（Review comments）  
- 点击 **"Approve"** 或 **"Request changes"**  
- 审查完成后，由项目维护者点击 **"Merge pull request"**

---

## 🧠 Tips for Better Collaboration  
更好的协作建议：

- 每次更改使用新分支，避免直接操作主分支  
- Issue 用于沟通，Pull Request 用于代码合并  
- 审查者可以通过评论指出问题，提交者可继续修改后更新 PR  
- PR 合并后自动关闭相关的 issue：在提交信息中添加 `Fixes #1`

示例：

```bash
git commit -m "Fix login bug (Fixes #12)"
```

---

## 🧾 Summary  
总结：

| 功能 | 用途 |
|------|------|
| Issue | 报告问题、建议功能、分配任务 |
| Pull Request | 提交代码修改，申请合并到主分支 |
| Review | 代码审查，确保代码质量 |
| Merge | 确认无误后，将分支合并入主分支 |

> GitHub collaboration is built around **open discussion and controlled merging**.  
> GitHub 的协作流程基于“开放讨论 + 审查合并”。

使用好 Issues 与 Pull Requests，可以帮助你高效协作、优雅开发。
