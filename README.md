# HTML/CSS 交互式控制台

**HTML/CSS Interactive Console**  
改一行代码，看懂一条规则。

每个知识点都配一个页面内的可编辑控制台：修改 HTML/CSS，预览立即更新。不是只读教程，而是可以反复试错、立刻看到结果的 HTML/CSS 学习环境。

> **在线体验：** [打开 HTML/CSS 交互式控制台 →](https://ding9715.github.io/html-css-console/)  
> 打开即用，无需安装。

## 核心体验

- **实时控制台**：点“编辑代码”直接修改示例，输入即运行，不用切换页面。
- **141 个知识点**：覆盖 HTML 语义、表单、CSS 选择器、盒模型、Flex/Grid、定位、动画与响应式。
- **可视化实验台**：拖动滑块调参数，实时观察盒模型、Flex、Grid、阴影、缓动等变化。
- **对比实验室**：同一份 DOM，只改一条规则，直接看命中范围和结果差异。
- **学习反馈**：掌握勾选、学习进度、搜索、背诵模式、深色主题和辅助线。
- **单文件运行**：无后端、无构建、无外部资源依赖，双击即可离线使用。

## 本地运行

直接双击 `index.html`，或在项目目录执行：

```bat
cd /d "D:\html+css交互式学习网站"
python -m http.server 8000
```

然后打开 <http://127.0.0.1:8000/>。

## 部署到 GitHub Pages

先创建一个空的公开仓库，仓库名建议为 `html-css-console`，不要勾选初始化 README、.gitignore 或 license。

### 方式一：网页上传（零命令）

1. 进入仓库，点击 **Add file → Upload files**。
2. 把 `index.html`、`README.md`、`.gitignore` 拖到仓库根目录。
3. 点击 **Commit changes**。

### 方式二：Git 命令

```bat
cd /d "D:\html+css交互式学习网站"

git init
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/html-css-console.git

git add .
git commit -m "feat: HTML/CSS interactive console"

git branch -M main
git push -u origin main
```

把 `YOUR_GITHUB_USERNAME` 替换成你的 GitHub 用户名。首次推送按提示完成浏览器登录。

### 开启 Pages

两种方式都完成后，进入仓库：

**Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` → 目录: `/(root)` → Save**

等待 1–3 分钟，访问：

```text
https://{用户名}.github.io/html-css-console/
```

## 项目结构

```text
html-css-console/
├─ index.html                # 主入口
├─ README.md
├─ .gitignore
└─ html-css-handbook.html    # 可选：旧链接跳转页
```

部署时至少上传前三个文件。旧跳转页用于兼容之前分享过的地址，不需要时可以删除。

## 常见问题

- **根地址 404**：Pages 尚未构建完成，或分支不是 `main`、目录不是 `/(root)`。
- **页面空白**：页面由 JavaScript 渲染，请启用 JavaScript 后刷新。
- **仍是旧版本**：等待 1–3 分钟，按 `Ctrl + F5` 或用无痕窗口访问。

## 说明

- 学习进度保存在浏览器 `localStorage`，不会上传服务器。
- 代码示例运行在独立 `iframe` 中，不会影响主页。
- 图片示例中的 `missing-image.jpg` 是故意写的错误地址，用于演示加载失败；出现该 404 属于正常现象。
- 已验证：UTF-8 编码、无外链资源、内联 JavaScript 语法通过、本地 HTTP 访问返回 200。
