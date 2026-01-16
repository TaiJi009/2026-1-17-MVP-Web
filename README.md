# 今天只做一件事

一个极简的单页网站，显示"今天只做一件事"。

## 部署到 GitHub Pages

### 步骤 1：创建 GitHub 仓库

1. 登录 [GitHub](https://github.com)
2. 点击右上角的 "+" 号，选择 "New repository"
3. 输入仓库名称（例如：`today-one-thing`）
4. 选择 "Public"（GitHub Pages 免费版需要公开仓库）
5. **不要**勾选 "Initialize this repository with a README"（因为我们已经有了文件）
6. 点击 "Create repository"

### 步骤 2：上传文件到仓库

#### 方法 A：使用 GitHub 网页界面（最简单）

1. 在新建的仓库页面，点击 "uploading an existing file"
2. 将本地的 `index.html` 文件拖拽到页面中
3. 在页面底部填写提交信息（例如："Initial commit"）
4. 点击 "Commit changes"

#### 方法 B：使用 Git 命令行

```bash
# 初始化 Git 仓库
git init

# 添加文件
git add index.html README.md

# 提交
git commit -m "Initial commit"

# 添加远程仓库（将 YOUR_USERNAME 和 YOUR_REPO_NAME 替换为你的实际值）
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

### 步骤 3：启用 GitHub Pages

1. 在仓库页面，点击 "Settings"（设置）
2. 在左侧菜单中找到 "Pages"
3. 在 "Source" 部分，选择 "Deploy from a branch"
4. 选择分支为 "main"（或 "master"），文件夹为 "/ (root)"
5. 点击 "Save"
6. 等待几分钟，GitHub 会显示你的网站 URL，格式为：
   ```
   https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
   ```

### 步骤 4：访问网站

部署完成后（通常需要 1-2 分钟），访问 GitHub 提供的 URL 即可看到网站。

## 更新网站

如果需要更新网站内容：

1. 修改本地的 `index.html` 文件
2. 将修改后的文件上传到 GitHub（使用网页界面或 Git 命令）
3. GitHub Pages 会自动更新（通常需要几分钟）

## 故障排除

### 问题：DNS 检查失败（DNS check failed）

如果您在 GitHub Pages 设置中看到 "DNS检查失败" 的错误，有两种解决方案：

#### 方案 1：使用默认域名（推荐，最简单）

**如果您不需要自定义域名，直接使用 GitHub 提供的免费域名即可：**

1. 在 GitHub Pages 设置页面，找到 "自定义域名" 部分
2. 点击红色的 **"消除"（Delete）** 按钮，删除自定义域名
3. 保存后，您的网站将使用默认域名：`https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`
4. 这个域名完全免费，任何人都可以访问，无需任何 DNS 配置

#### 方案 2：配置自定义域名（如果您确实需要）

如果您需要使用 `www.taiji009mvpweb.com` 这样的自定义域名，需要：

1. **在您的域名注册商（如阿里云、腾讯云等）配置 DNS 记录：**
   - 添加一条 **CNAME 记录**：
     - 主机记录：`www`
     - 记录值：`YOUR_USERNAME.github.io`（替换为您的 GitHub 用户名）
   - 或者添加一条 **A 记录**：
     - 主机记录：`www`
     - 记录值：`185.199.108.153`（GitHub Pages 的 IP 地址）

2. **等待 DNS 生效**（通常需要几分钟到几小时）

3. **在 GitHub Pages 设置中点击 "再次检查"** 按钮

4. DNS 配置正确后，错误会消失，可以启用 HTTPS

**注意**：对于最简单的网站部署，强烈建议使用方案 1，无需配置 DNS，立即可用。

## 注意事项

- GitHub Pages 是完全免费的
- 网站是公开的，任何人都可以访问
- 默认域名（username.github.io）无需任何配置，立即可用
- 如果使用自定义域名，需要配置 DNS 记录
