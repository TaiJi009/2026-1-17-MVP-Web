# 蒙德里安时钟

一个融合蒙德里安和构成主义艺术风格的实时时钟网站。

## 功能特点

- ⏰ 实时时钟显示，格式为 `00:00:00`
- 🎨 蒙德里安风格设计（红、黄、蓝三原色，黑色线条）
- 📐 构成主义艺术元素（几何形状、斜线、工业感）
- 📱 响应式设计，适配各种设备

## 设计风格

### 蒙德里安风格
- **三原色色块**：红色、黄色、蓝色
- **黑色粗线条**：垂直和水平分隔线
- **白色背景**：简洁纯净
- **网格布局**：经典的几何构图

### 构成主义风格
- **几何形状装饰**：黄色和红色方块
- **斜线元素**：动态视觉感
- **粗体字体**：等宽字体，工业感
- **3D 阴影效果**：立体层次感
- **黑色粗边框**：强烈的视觉冲击

## 部署到 GitHub Pages

### 步骤 1：创建 GitHub 仓库

1. 登录 [GitHub](https://github.com)
2. 点击右上角的 "+" 号，选择 "New repository"
3. 输入仓库名称（例如：`mondrian-clock`）
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

部署完成后（通常需要 1-2 分钟），访问 GitHub 提供的 URL 即可看到实时时钟网站。

## 本地运行

直接在浏览器中打开 `index.html` 文件即可查看效果。

```bash
# 或者使用简单的 HTTP 服务器（可选）
# Python 3
python -m http.server 8000

# 然后访问 http://localhost:8000
```

## 技术栈

- **HTML5**：页面结构
- **CSS3**：蒙德里安/构成主义风格设计，响应式布局
- **JavaScript**：实时时钟更新逻辑

## 浏览器支持

- Chrome（推荐）
- Firefox
- Safari
- Edge
- 现代移动浏览器

## 更新网站

如果需要更新网站内容：

1. 修改本地的 `index.html` 文件
2. 将修改后的文件上传到 GitHub（使用网页界面或 Git 命令）
3. GitHub Pages 会自动更新（通常需要几分钟）

## 故障排除

### 问题：DNS 检查失败

如果您在 GitHub Pages 设置中配置了自定义域名但出现 DNS 错误：

1. **推荐方案**：删除自定义域名，使用默认的 GitHub 域名（`username.github.io/repo-name`）
   - 在 GitHub Pages 设置中点击 "消除"（Delete）按钮删除自定义域名
   - 默认域名完全免费，无需 DNS 配置，立即可用

2. **如果需要自定义域名**：需要在域名服务商处配置 DNS 记录（CNAME 或 A 记录）

## 许可证

本项目采用 MIT 许可证。

## 艺术风格参考

- **蒙德里安**（Piet Mondrian）：荷兰风格派运动代表，以红、黄、蓝三原色和黑色线条著称
- **构成主义**（Constructivism）：20 世纪初的现代艺术运动，强调几何形式、工业材料和实用主义

---

享受这个融合艺术与功能的实时时钟！⏰🎨
