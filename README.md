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

## 注意事项

- GitHub Pages 是完全免费的
- 网站是公开的，任何人都可以访问
- 如果使用自定义域名，可以在 Settings > Pages 中配置
