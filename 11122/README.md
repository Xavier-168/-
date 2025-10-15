# 赵逍遥 - 个人简历网站

## 📁 项目结构

```
11122/
├── index.html          # 主页面文件
├── avatar.jpg          # 个人头像（您需要添加）
├── portfolio/          # 作品集文件夹（您需要创建）
│   ├── code-work-1.mp4    # 代码作品视频1
│   ├── code-work-2.mp4    # 代码作品视频2
│   ├── code-work-3.mp4    # 代码作品视频3
│   ├── code-work-4.mp4    # 代码作品视频4
│   ├── code-preview-1.jpg # 视频封面图1
│   ├── code-preview-2.jpg # 视频封面图2
│   ├── code-preview-3.jpg # 视频封面图3
│   ├── code-preview-4.jpg # 视频封面图4
│   ├── photo-1.jpg        # 摄影作品1
│   ├── photo-2.jpg        # 摄影作品2
│   ├── photo-3.jpg        # 摄影作品3
│   ├── photo-4.jpg        # 摄影作品4
│   ├── photo-5.jpg        # 摄影作品5
│   └── photo-6.jpg        # 摄影作品6
└── README.md           # 本文件
```

## 🚀 快速开始

### 1. 设置头像

请将您的头像图片保存为 `avatar.jpg`，并放在项目根目录下。

**步骤：**
1. 将您的头像图片（聊天中上传的动漫风格头像）保存到本地
2. 重命名为 `avatar.jpg`
3. 放在与 `index.html` 相同的目录下
4. 刷新浏览器即可看到头像

> 💡 如果没有头像图片，网站会自动显示 "WL" 字母作为占位符。

### 2. 添加作品集文件

在项目根目录下创建 `portfolio` 文件夹，并添加您的作品文件：

```bash
mkdir portfolio
```

**代码作品视频：**
- 将您的代码演示视频命名为 `code-work-1.mp4`, `code-work-2.mp4` 等
- （可选）为视频添加封面图：`code-preview-1.jpg`, `code-preview-2.jpg` 等

**摄影作品图片：**
- 将您的摄影作品命名为 `photo-1.jpg`, `photo-2.jpg` 等
- 推荐尺寸：宽度至少 800px，比例 4:3

> 💡 如果文件不存在，网站会自动显示占位符，不会影响页面正常显示。

## 🌐 部署到 Vercel（推荐）

### 方法一：通过 Vercel CLI

1. **安装 Vercel CLI**
```bash
npm install -g vercel
```

2. **登录 Vercel**
```bash
vercel login
```

3. **部署项目**
```bash
cd /Users/mac/Desktop/11122
vercel
```

4. **按照提示操作**
- Set up and deploy: Yes
- Which scope: 选择您的账号
- Link to existing project: No
- Project name: 输入项目名称（如：zhaoxiaoyao-resume）
- In which directory: 直接回车（当前目录）
- Override settings: No

### 方法二：通过 Vercel 网站

1. 访问 [vercel.com](https://vercel.com)
2. 登录或注册账号
3. 点击 "New Project"
4. 选择 "Import Git Repository" 或直接拖拽文件夹
5. 点击 "Deploy"

### 部署注意事项

✅ **所有文件路径都使用相对路径**，可以直接部署
- 头像：`avatar.jpg`
- 视频：`./portfolio/code-work-1.mp4`
- 图片：`./portfolio/photo-1.jpg`

✅ **建议部署前准备**：
1. 确保 `avatar.jpg` 已添加
2. 创建 `portfolio` 文件夹并添加您的作品文件
3. 如果文件暂时缺失也没关系，网站会显示占位符

✅ **部署后访问**：
- Vercel 会生成一个 URL，如：`https://zhaoxiaoyao-resume.vercel.app`
- 您可以在 Vercel 控制台中设置自定义域名

## 最新更新

### ✅ 第三版更新（作品集 + 软技能重设计）

1. **新增作品集模块** 🎨
   - **代码作品集**（神秘高级风格）：
     - 黑色背景 + 青色霓虹效果
     - 动态网格动画
     - 支持4个代码演示视频
     - 终端风格设计（红黄绿三色圆点）
     - 技术标签高亮显示
   
   - **摄影作品集**（简约大气风格）：
     - 白色背景 + 极简布局
     - 6张摄影作品展示
     - 图片hover放大效果
     - 底部渐变遮罩信息

2. **软技能布局重设计** 💎
   - 改为渐变色卡片设计
   - 每个技能配独特图标和颜色
   - 用小圆点表示熟练程度（5星制）
   - Hover时卡片浮起效果
   - 响应式3列布局（移动端2列）

3. **导航栏更新**
   - 新增"作品集"导航项
   - 桌面端和移动端菜单同步更新

### ✅ 第二版更新（优化版）

1. **背景渐变优化**
   - 降低了颜色饱和度
   - 使用柔和的淡色调（粉、蓝、青、米色等）
   - 25秒循环，更加优雅舒缓

2. **导航栏增强**
   - 增加了蓝色边框和阴影
   - 导航项添加了hover背景效果
   - 字体加粗，更加醒目

3. **标题样式统一**
   - 所有大标题改为纯黑色 (#1a1a1a)
   - 使用更优质的中文字体（PingFang SC / Microsoft YaHei）

4. **项目经历添加获奖展示** ⭐
   - 项目2（校园二手交易平台）：金色获奖徽章
   - 项目3（个人健康管理APP）：紫色获奖徽章

5. **头像支持**
   - 支持使用真实头像图片
   - 圆形蓝色边框效果

## 功能特性

- ✅ 动态渐变背景（柔和色调）
- ✅ 响应式设计
- ✅ 卡片点击放大功能
- ✅ 获奖项目醒目标识
- ✅ 纵向彩色技能柱状图
- ✅ 平滑滚动导航
- ✅ 所有交互效果

## 技术栈

- HTML5
- CSS3 (Tailwind CSS)
- JavaScript (原生)
- 无需任何依赖，直接打开即可使用

## 浏览器支持

- Chrome/Edge (推荐)
- Firefox
- Safari
- 移动端浏览器

---

© 2024 王磊. All rights reserved.

