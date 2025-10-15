# 视频替换完整指南

## 🎬 三种替换方式

### 方式一：使用本地视频文件（推荐用于小文件）

#### 步骤1：准备视频文件

1. **视频要求**：
   - 格式：MP4（H.264编码）
   - 大小：建议 < 10MB（Vercel免费版限制）
   - 时长：15-30秒最佳
   - 分辨率：1280x720 或 1920x1080

2. **压缩视频**（如果文件太大）：
   
   **在线工具**：
   - https://www.freeconvert.com/video-compressor
   - https://www.videosmaller.com
   
   **命令行工具（FFmpeg）**：
   ```bash
   ffmpeg -i input.mp4 -c:v libx264 -crf 28 -preset fast -c:a aac -b:a 96k output.mp4
   ```

#### 步骤2：放置文件

```bash
# 创建portfolio文件夹（如果不存在）
mkdir portfolio

# 将视频文件命名并放入
# 例如：
portfolio/
  ├── my-react-project.mp4
  ├── my-vue-app.mp4
  ├── my-algorithm.mp4
  └── my-miniapp.mp4
```

#### 步骤3：修改HTML代码

打开 `index.html`，找到对应的视频位置，替换iframe为video标签：

**修改前**：
```html
<div class="video-container mb-4">
    <iframe 
        src="https://player.vimeo.com/video/336812660?autoplay=0&loop=1" 
        title="React Full Stack Project"
        frameborder="0" 
        allow="autoplay; fullscreen; picture-in-picture" 
        allowfullscreen>
    </iframe>
</div>
```

**修改后**：
```html
<div class="video-container mb-4">
    <video controls loop preload="metadata">
        <source src="./portfolio/my-react-project.mp4" type="video/mp4">
        您的浏览器不支持视频播放
    </video>
</div>
```

---

### 方式二：使用YouTube视频

#### 步骤1：获取YouTube视频ID

1. 打开您的YouTube视频
2. 复制视频URL，例如：
   ```
   https://www.youtube.com/watch?v=dQw4w9WgXcQ
   ```
3. 提取视频ID（问号后面的部分）：`dQw4w9WgXcQ`

#### 步骤2：修改HTML代码

```html
<div class="video-container mb-4">
    <iframe 
        src="https://www.youtube.com/embed/dQw4w9WgXcQ?rel=0&modestbranding=1" 
        title="我的项目演示"
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
    </iframe>
</div>
```

**YouTube参数说明**：
- `rel=0` - 不显示相关视频
- `modestbranding=1` - 最小化YouTube品牌
- `autoplay=1` - 自动播放（不推荐）
- `loop=1` - 循环播放
- `controls=0` - 隐藏控制条

---

### 方式三：使用Vimeo视频（当前使用）

#### 步骤1：上传到Vimeo

1. 注册Vimeo账号：https://vimeo.com
2. 点击"上传"按钮
3. 上传您的视频文件
4. 等待处理完成

#### 步骤2：获取视频ID

1. 打开您上传的视频
2. 查看URL，例如：
   ```
   https://vimeo.com/123456789
   ```
3. 提取数字部分：`123456789`

#### 步骤3：修改HTML代码

```html
<div class="video-container mb-4">
    <iframe 
        src="https://player.vimeo.com/video/123456789?autoplay=0&loop=1&title=0&byline=0&portrait=0" 
        title="我的项目演示"
        frameborder="0" 
        allow="autoplay; fullscreen; picture-in-picture" 
        allowfullscreen>
    </iframe>
</div>
```

**Vimeo参数说明**：
- `autoplay=0` - 不自动播放
- `loop=1` - 循环播放
- `title=0` - 隐藏标题
- `byline=0` - 隐藏作者
- `portrait=0` - 隐藏头像

---

### 方式四：使用Bilibili视频（国内推荐）

#### 步骤1：获取Bilibili视频BV号

1. 打开您的B站视频
2. 复制URL，例如：
   ```
   https://www.bilibili.com/video/BV1xx411c7XZ
   ```
3. 提取BV号：`BV1xx411c7XZ`

#### 步骤2：修改HTML代码

```html
<div class="video-container mb-4">
    <iframe 
        src="//player.bilibili.com/player.html?bvid=BV1xx411c7XZ&page=1&high_quality=1&danmaku=0" 
        title="我的项目演示"
        frameborder="0" 
        scrolling="no" 
        allowfullscreen>
    </iframe>
</div>
```

**Bilibili参数说明**：
- `bvid=` - 视频BV号
- `page=1` - 第几个分P
- `high_quality=1` - 高清画质
- `danmaku=0` - 关闭弹幕
- `autoplay=0` - 不自动播放

---

## 📍 具体修改位置

在 `index.html` 文件中，有4个视频需要替换：

### 视频1：React全栈项目
**位置**：约第886-895行
```html
<!-- 搜索这段注释 -->
<!-- 代码作品1 -->
```

### 视频2：Vue3应用
**位置**：约第915-924行
```html
<!-- 搜索这段注释 -->
<!-- 代码作品2 -->
```

### 视频3：算法可视化
**位置**：约第944-953行
```html
<!-- 搜索这段注释 -->
<!-- 代码作品3 -->
```

### 视频4：微信小程序
**位置**：约第973-982行
```html
<!-- 搜索这段注释 -->
<!-- 代码作品4 -->
```

---

## 🛠️ 完整示例

### 示例1：混合使用（本地 + 在线）

```html
<!-- 视频1：本地文件 -->
<div class="video-container mb-4">
    <video controls loop preload="metadata">
        <source src="./portfolio/react-demo.mp4" type="video/mp4">
        您的浏览器不支持视频播放
    </video>
</div>

<!-- 视频2：YouTube -->
<div class="video-container mb-4">
    <iframe 
        src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
        frameborder="0" 
        allowfullscreen>
    </iframe>
</div>

<!-- 视频3：Vimeo -->
<div class="video-container mb-4">
    <iframe 
        src="https://player.vimeo.com/video/YOUR_VIDEO_ID?loop=1" 
        frameborder="0" 
        allowfullscreen>
    </iframe>
</div>

<!-- 视频4：Bilibili -->
<div class="video-container mb-4">
    <iframe 
        src="//player.bilibili.com/player.html?bvid=YOUR_BV_ID&danmaku=0" 
        frameborder="0" 
        allowfullscreen>
    </iframe>
</div>
```

### 示例2：全部使用本地视频

```bash
# 1. 准备文件结构
portfolio/
  ├── project1.mp4
  ├── project2.mp4
  ├── project3.mp4
  └── project4.mp4
```

```html
<!-- 然后在HTML中统一替换为 -->
<div class="video-container mb-4">
    <video controls loop preload="metadata" poster="./portfolio/project1-cover.jpg">
        <source src="./portfolio/project1.mp4" type="video/mp4">
        您的浏览器不支持视频播放
    </video>
</div>
```

---

## 🎨 添加视频封面图（可选）

如果使用本地视频，可以添加封面图：

### 步骤1：创建封面图

**方式A：从视频提取**
```bash
ffmpeg -i input.mp4 -ss 00:00:02 -vframes 1 cover.jpg
```

**方式B：使用截图工具**
- 播放视频到精彩画面
- 截图保存为JPG格式

### 步骤2：添加poster属性

```html
<video controls loop preload="metadata" poster="./portfolio/cover1.jpg">
    <source src="./portfolio/video1.mp4" type="video/mp4">
</video>
```

---

## ⚡ 性能优化建议

### 1. 压缩视频

**目标**：
- 文件大小：< 10MB
- 码率：1000-2000 kbps
- 分辨率：720p或1080p

**FFmpeg压缩命令**：
```bash
# 高质量（约2MB/分钟）
ffmpeg -i input.mp4 -c:v libx264 -crf 23 -preset medium -c:a aac -b:a 128k output.mp4

# 中等质量（约1MB/分钟）
ffmpeg -i input.mp4 -c:v libx264 -crf 28 -preset fast -c:a aac -b:a 96k output.mp4

# 低质量（约0.5MB/分钟）
ffmpeg -i input.mp4 -c:v libx264 -crf 32 -preset fast -c:a aac -b:a 64k output.mp4
```

### 2. 使用懒加载

```html
<video controls loop preload="none" loading="lazy">
    <source src="./portfolio/video.mp4" type="video/mp4">
</video>
```

**preload选项**：
- `none` - 不预加载（推荐）
- `metadata` - 只加载元数据
- `auto` - 自动预加载（不推荐）

### 3. 使用CDN（推荐）

如果视频较大，建议上传到：
- **阿里云OSS**：https://www.aliyun.com/product/oss
- **七牛云**：https://www.qiniu.com
- **腾讯云COS**：https://cloud.tencent.com/product/cos

然后使用CDN链接：
```html
<video controls loop>
    <source src="https://your-cdn.com/video.mp4" type="video/mp4">
</video>
```

---

## 🔍 快速查找替换

### 使用查找功能

1. 打开 `index.html`
2. 按 `Cmd+F`（Mac）或 `Ctrl+F`（Windows）
3. 搜索：`player.vimeo.com`
4. 逐个替换为您的视频源

### 批量替换（高级）

如果您熟悉代码编辑器，可以使用"查找并替换"功能：

**查找**：
```
src="https://player.vimeo.com/video/\d+\?autoplay=0&loop=1"
```

**替换为**：
```
src="./portfolio/video-{编号}.mp4"
```

---

## 📋 检查清单

替换视频前，请确认：

- [ ] 视频格式为MP4（H.264）
- [ ] 文件大小合适（< 10MB）
- [ ] 视频时长15-30秒
- [ ] 文件已放在portfolio文件夹
- [ ] HTML代码已正确修改
- [ ] 本地测试播放正常
- [ ] （可选）添加了封面图

---

## 🐛 常见问题

### Q1: 视频无法播放？

**原因**：
- 格式不支持（使用MP4 H.264）
- 文件路径错误
- 文件不存在

**解决**：
```bash
# 检查文件是否存在
ls portfolio/

# 转换视频格式
ffmpeg -i input.mov -c:v libx264 -c:a aac output.mp4
```

### Q2: Vercel部署后视频404？

**原因**：
- portfolio文件夹未上传
- 文件名大小写不匹配

**解决**：
- 确保portfolio文件夹包含在部署中
- 检查文件名大小写

### Q3: 视频文件太大？

**解决方案**：
1. 使用FFmpeg压缩
2. 使用在线视频平台（YouTube/Vimeo）
3. 使用CDN托管

### Q4: 想要自动播放？

**不推荐**，但如果需要：
```html
<video autoplay muted loop>
    <source src="./portfolio/video.mp4">
</video>
```
**注意**：必须添加 `muted` 属性，否则浏览器会阻止自动播放。

---

## 📞 需要帮助？

如果遇到问题：

1. 检查浏览器Console是否有错误
2. 确认文件路径正确
3. 测试视频在其他播放器能否播放
4. 查看本文档的常见问题部分

---

## 🎉 快速开始模板

### 方案A：全部使用本地视频

```bash
# 1. 创建文件夹
mkdir portfolio

# 2. 复制视频文件
cp my-videos/*.mp4 portfolio/

# 3. 重命名为统一格式
mv portfolio/video1.mp4 portfolio/react-project.mp4
mv portfolio/video2.mp4 portfolio/vue-app.mp4
mv portfolio/video3.mp4 portfolio/algorithm.mp4
mv portfolio/video4.mp4 portfolio/miniapp.mp4

# 4. 修改HTML中所有的iframe为video标签
```

### 方案B：使用YouTube链接

```html
<!-- 只需替换视频ID即可 -->
src="https://www.youtube.com/embed/YOUR_VIDEO_ID_HERE"
```

### 方案C：使用Bilibili（国内最佳）

```html
<!-- 只需替换BV号即可 -->
src="//player.bilibili.com/player.html?bvid=YOUR_BV_ID_HERE&danmaku=0"
```

---

✨ **选择最适合您的方式，开始替换视频吧！**

