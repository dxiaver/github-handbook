# How to Set Up SSH for GitHub  
如何为 GitHub 配置 SSH

---

## 🔐 What is SSH and Why Use It?  
什么是 SSH？为什么使用 SSH？

**SSH (Secure Shell)** is a secure way to authenticate with GitHub without using your username and password every time.  
**SSH（安全外壳协议）** 是一种安全的认证方式，可以免去每次操作 GitHub 时输入用户名和密码的麻烦。

Benefits of using SSH:  
使用 SSH 的优点：

- More secure than HTTPS  
  比 HTTPS 更安全  
- No need to enter username/password each time  
  操作 Git 时无需反复输入账号和密码  
- Required for automation and private repositories  
  自动化脚本和访问私有仓库时必须用 SSH

---

## 🧰 Step-by-Step: Set Up SSH for GitHub  
逐步指南：配置 GitHub 的 SSH

---

### ✅ 1. Check for Existing SSH Keys  
✅ 1. 检查是否已有 SSH 密钥

```bash
ls ~/.ssh
```

If you see files like `id_rsa` and `id_rsa.pub`, you already have an SSH key.  
如果你看到类似 `id_rsa` 和 `id_rsa.pub` 的文件，就说明你已有 SSH 密钥，可跳过下一步。

---

### ✅ 2. Generate a New SSH Key (if needed)  
✅ 2. 生成新的 SSH 密钥（如果你没有）

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

如果你的系统不支持 ed25519，可使用：

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

然后连续按回车即可完成。生成后你会在 `~/.ssh` 目录下看到：

- `id_ed25519`：私钥（不要泄露）
- `id_ed25519.pub`：公钥（稍后要上传到 GitHub）

---

### ✅ 3. Add the SSH Key to Your GitHub Account  
✅ 3. 将公钥添加到你的 GitHub 账号

1. 复制公钥内容：

```bash
cat ~/.ssh/id_ed25519.pub
```

复制终端输出的整行内容（以 `ssh-ed25519` 开头）。

2. 登录 GitHub → 点击右上角头像 → Settings  
3. 左侧选择 **"SSH and GPG keys"**  
4. 点击 **“New SSH key”**  
5. 填入标题（如：My Laptop）和复制的公钥 → 点击 **Add SSH key**

---

### ✅ 4. Test Your SSH Connection  
✅ 4. 测试 SSH 是否配置成功

```bash
ssh -T git@github.com
```

第一次连接会提示：

```bash
Are you sure you want to continue connecting (yes/no)?  
输入：yes 并按回车
```

若成功，你将看到类似信息：

```bash
Hi your-username! You've successfully authenticated, but GitHub does not provide shell access.  
说明你已成功通过 SSH 验证！
```

---

### ✅ 5. Set Git to Use SSH Instead of HTTPS  
✅ 5. 设置 Git 使用 SSH 地址（替代 HTTPS）

如果你原本是通过 HTTPS 克隆的项目：

```bash
https://github.com/username/repo.git
```

建议改为 SSH 地址：

```bash
git@github.com:username/repo.git
```

你可以选择以下任意一种方式：

**方式一：重新克隆项目**

```bash
git clone git@github.com:username/repo.git
```

**方式二：修改现有项目的远程地址**

```bash
git remote set-url origin git@github.com:username/repo.git
```

---

## 📖 Summary  
总结

- SSH 可以安全地连接 GitHub，避免频繁输入密码  
- 设置步骤包括：检查或生成密钥 → 上传公钥到 GitHub → 测试连接 → 设置 Git 使用 SSH  
- 推荐每台开发设备都生成并添加自己的 SSH 密钥

> Now your GitHub is connected securely via SSH! 🔐  
> 现在你的 GitHub 已通过 SSH 成功连接！🔐
