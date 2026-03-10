# 部署指南 - 温馨家庭网站

本指南将帮助你将温馨家庭网站部署到互联网上，让家人可以访问。

## 推荐部署平台

### 方法一：Vercel（推荐，免费且简单）

#### 步骤 1：准备代码

1. 确保你有以下文件：
   - `index.html` - 主网页
   - `package.json` - 项目配置
   - `vercel.json` - Vercel 配置
   - `README.md` - 说明文档

#### 步骤 2：创建 GitHub 仓库

1. 访问 [GitHub](https://github.com) 并登录
2. 点击右上角的 "+" → "New repository"
3. 填写仓库名称，例如：`family-memories`
4. 选择 "Public" 或 "Private"
5. 点击 "Create repository"

#### 步骤 3：上传代码到 GitHub

在终端中执行以下命令：

```bash
# 进入项目目录
cd /Users/hanzheng/WorkBuddy/20260309171646

# 初始化 git
git init

# 添加所有文件
git add .

# 提交
git commit -m "Initial commit"

# 添加远程仓库（替换为你的仓库地址）
git remote add origin https://github.com/你的用户名/family-memories.git

# 推送代码
git branch -M main
git push -u origin main
```

#### 步骤 4：连接到 Vercel

1. 访问 [Vercel](https://vercel.com)
2. 使用 GitHub 账号登录
3. 点击 "Add New" → "Project"
4. 选择你的 `family-memories` 仓库
5. 点击 "Import"

#### 步骤 5：配置部署

1. **Framework Preset**: 选择 "Other"
2. **Root Directory**: 保持默认 `./`
3. **Build and Output Settings**: 保持默认
4. 点击 "Deploy"

#### 步骤 6：获取网址

部署完成后（通常 1-2 分钟），Vercel 会给你一个网址，例如：
```
https://family-memories.vercel.app
```

你可以：
- 访问这个网址查看网站
- 在项目设置中自定义域名
- 分享给家人使用

---

### 方法二：Netlify（免费，拖拽部署）

1. 访问 [Netlify](https://www.netlify.com) 并注册账号
2. 将项目文件夹拖拽到 Netlify 的 "Sites" 区域
3. Netlify 会自动部署，并提供一个网址
4. 你可以在 "Site settings" 中设置自定义域名

---

### 方法三：GitHub Pages（免费，需要 GitHub 账号）

1. 在你的 GitHub 仓库中，点击 "Settings"
2. 找到 "Pages" 选项
3. 在 "Source" 下选择 "Deploy from a branch"
4. 选择 `main` 分支和 `/ (root)` 目录
5. 点击 "Save"
6. 几分钟后，你的网站会在 `https://你的用户名.github.io/family-memories` 上线

---

## 部署后的注意事项

### 数据存储说明

⚠️ **重要提示**：

当前版本使用浏览器 LocalStorage 存储数据，这意味着：
- ✅ 每个设备的数据是独立的
- ❌ 家人之间无法共享数据
- ❌ 换设备后数据会丢失

### 解决方案

如果你希望家人共享数据，需要：

#### 方案 1：使用云数据库（推荐）

可以集成以下服务：
- **Firebase**（Google 提供，免费额度）
- **Supabase**（开源，免费额度）
- **MongoDB Atlas**（免费额度）

#### 方案 2：升级到后端服务

需要开发后端 API，使用：
- Node.js + Express
- Python + Flask/FastAPI
- 或使用云服务如 CloudBase

---

## 自定义域名

### 在 Vercel 上设置自定义域名

1. 进入项目设置
2. 点击 "Domains"
3. 添加你的域名（例如：family.yourdomain.com）
4. 按照提示配置 DNS

### 免费域名

如果还没有域名，可以使用：
- **Freenom** - 免费顶级域名（.tk, .ml, .ga 等）
- **EU.org** - 免费子域名

---

## 网站分享

### 分享给家人

1. 复制 Vercel 提供的网址
2. 通过微信、邮件等方式分享
3. 家人可以直接在浏览器中打开访问

### 二维码分享

使用在线工具将网址转换为二维码，家人扫码即可访问：
- [草料二维码](https://cli.im)
- [联图二维码](https://www.liantu.com)

---

## 维护和更新

### 更新网站内容

1. 修改 `index.html` 文件
2. 使用 git 提交并推送到 GitHub
3. Vercel 会自动检测更改并重新部署

### 查看部署日志

在 Vercel 控制台中，可以查看：
- 部署历史
- 访问统计
- 错误日志

---

## 成本说明

使用 Vercel 部署：
- ✅ 个人使用免费
- ✅ 流量充足（100GB/月）
- ✅ 自动 HTTPS
- ✅ 全球 CDN 加速
- ✅ 无需维护服务器

---

## 需要帮助？

- Vercel 文档：https://vercel.com/docs
- Netlify 文档：https://docs.netlify.com
- GitHub Pages 文档：https://docs.github.com/pages

---

祝你部署成功，和家人一起享受美好的回忆时光！🎉
