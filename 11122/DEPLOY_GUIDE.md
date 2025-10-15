# Vercel 部署完整指南

## 🚀 方式一：使用 Vercel CLI（推荐）

### 1. 安装 Node.js

如果还没有安装 Node.js，请先安装：
- 访问 https://nodejs.org
- 下载并安装 LTS 版本

### 2. 安装 Vercel CLI

打开终端，运行：

```bash
npm install -g vercel
```

### 3. 登录 Vercel

```bash
vercel login
```

选择登录方式（GitHub, GitLab, Email 等）

### 4. 部署项目

```bash
# 进入项目目录
cd /Users/mac/Desktop/11122

# 开始部署
vercel
```

### 5. 回答部署问题

```
? Set up and deploy "~/Desktop/11122"? [Y/n] y
? Which scope do you want to deploy to? Your Username
? Link to existing project? [y/N] n
? What's your project's name? zhaoxiaoyao-resume
? In which directory is your code located? ./
```

### 6. 等待部署完成

几秒钟后，您会看到：

```
✅  Production: https://zhaoxiaoyao-resume.vercel.app [copied to clipboard]
```

点击链接即可访问！

---

## 🌐 方式二：通过 Vercel 网站（最简单）

### 1. 访问 Vercel

打开浏览器，访问：https://vercel.com

### 2. 注册/登录

- 点击 "Sign Up" 或 "Log In"
- 推荐使用 GitHub 账号登录

### 3. 创建新项目

- 点击 "Add New..." → "Project"
- 点击 "Browse" 或直接拖拽整个 `11122` 文件夹

### 4. 配置项目

- **Project Name**: zhaoxiaoyao-resume（或其他名称）
- **Framework Preset**: Other（保持默认）
- **Root Directory**: ./（保持默认）
- **Build Command**: 留空
- **Output Directory**: 留空

### 5. 部署

点击 "Deploy" 按钮，等待部署完成。

### 6. 访问网站

部署成功后，Vercel 会提供一个链接，例如：
```
https://zhaoxiaoyao-resume.vercel.app
```

---

## 📦 部署前准备清单

### 必需文件
- [x] `index.html` - 主页面（已有）
- [x] `vercel.json` - Vercel配置（已创建）
- [ ] `avatar.jpg` - 您的头像（需要添加）

### 可选文件（推荐添加）
- [ ] `portfolio/` 文件夹
  - [ ] `code-work-1.mp4` ~ `code-work-4.mp4` - 代码作品视频
  - [ ] `code-preview-1.jpg` ~ `code-preview-4.jpg` - 视频封面
  - [ ] `photo-1.jpg` ~ `photo-6.jpg` - 摄影作品

> 💡 即使这些文件暂时缺失，网站也能正常显示（会显示占位符）

---

## 🔄 更新已部署的网站

### 使用 CLI

```bash
cd /Users/mac/Desktop/11122
vercel --prod
```

### 使用网站

1. 登录 Vercel
2. 找到您的项目
3. 点击 "Deployments"
4. 点击 "Redeploy" 或上传新文件

---

## 🎨 自定义域名（可选）

### 1. 购买域名

从域名注册商购买（如 Namecheap, GoDaddy, 阿里云等）

### 2. 在 Vercel 添加域名

1. 进入项目设置
2. 点击 "Domains"
3. 输入您的域名
4. 按照提示配置 DNS

### 3. 等待 DNS 生效

通常需要几分钟到几小时

---

## 🐛 常见问题

### Q1: 部署后视频无法播放？

**原因**: 文件太大或格式不支持

**解决方案**:
1. 压缩视频到 50MB 以下
2. 使用 MP4 格式（H.264编码）
3. 或使用外部链接（YouTube, Bilibili等）

### Q2: 图片不显示？

**原因**: 文件路径错误或文件缺失

**解决方案**:
1. 确认 `portfolio` 文件夹已上传
2. 检查文件名是否正确（photo-1.jpg 等）
3. 如果文件缺失，网站会显示占位符（正常现象）

### Q3: 部署失败？

**原因**: 可能是文件太大或配置错误

**解决方案**:
1. 检查总文件大小是否超过 100MB
2. 确认 `vercel.json` 存在
3. 尝试删除 `.vercel` 文件夹后重新部署

### Q4: 想要更换头像？

**解决方案**:
1. 替换 `avatar.jpg` 文件
2. 重新部署：`vercel --prod`

### Q5: 网站显示404？

**原因**: 部署不完整或路由配置问题

**解决方案**:
1. 确认 `index.html` 在根目录
2. 检查 `vercel.json` 配置
3. 尝试重新部署

---

## 📊 查看访问统计

Vercel 提供免费的访问分析：

1. 登录 Vercel 控制台
2. 选择您的项目
3. 点击 "Analytics"
4. 查看访问量、地理位置等数据

---

## 💰 费用说明

**Vercel 免费版限制**:
- ✅ 免费托管
- ✅ 自动 HTTPS
- ✅ 全球 CDN
- ✅ 自动部署
- ⚠️ 带宽限制：100GB/月
- ⚠️ 部署次数：无限制

**何时需要升级**:
- 月访问量超过 100GB
- 需要团队协作功能
- 需要高级分析功能

---

## 🎓 进阶技巧

### 自动部署（使用 GitHub）

1. 将项目上传到 GitHub
2. 在 Vercel 连接 GitHub 仓库
3. 每次 push 代码，自动重新部署

### 环境变量

如果需要保密信息（API密钥等）:
1. Vercel 控制台 → Settings → Environment Variables
2. 添加变量
3. 在代码中使用 `process.env.VARIABLE_NAME`

### 预览部署

每次更新前，Vercel 会创建预览链接：
```
https://zhaoxiaoyao-resume-abc123.vercel.app
```
确认无误后再部署到生产环境。

---

## 📧 需要帮助？

- **Vercel 文档**: https://vercel.com/docs
- **Vercel 社区**: https://github.com/vercel/vercel/discussions
- **本项目问题**: 参考 README.md

---

## ✅ 快速检查清单

部署前检查：
- [ ] Node.js 已安装
- [ ] Vercel CLI 已安装（或使用网页版）
- [ ] 已登录 Vercel 账号
- [ ] `index.html` 在项目根目录
- [ ] `vercel.json` 已创建
- [ ] （可选）`avatar.jpg` 已添加
- [ ] （可选）`portfolio/` 文件夹已创建

部署后检查：
- [ ] 网站可以正常访问
- [ ] 所有页面导航正常
- [ ] 图片和视频加载正常
- [ ] 移动端显示正常
- [ ] 所有链接有效

---

🎉 **恭喜！您的个人简历网站已成功部署！**

分享您的网站链接：
```
https://zhaoxiaoyao-resume.vercel.app
```


