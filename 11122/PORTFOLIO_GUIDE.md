# 作品集文件使用指南

## 📂 文件夹结构

请在项目根目录下创建 `portfolio` 文件夹：

```bash
mkdir portfolio
```

## 🎬 代码作品视频

### 文件命名规范
- `code-work-1.mp4` - 第一个代码项目视频
- `code-work-2.mp4` - 第二个代码项目视频  
- `code-work-3.mp4` - 第三个代码项目视频
- `code-work-4.mp4` - 第四个代码项目视频

### 视频封面（可选）
- `code-preview-1.jpg` - 视频1的封面图
- `code-preview-2.jpg` - 视频2的封面图
- `code-preview-3.jpg` - 视频3的封面图
- `code-preview-4.jpg` - 视频4的封面图

### 视频要求
- **格式**：MP4（H.264编码）
- **分辨率**：建议 1920x1080 或 1280x720
- **大小**：建议每个视频不超过50MB（Vercel免费版有限制）
- **时长**：建议30秒-2分钟
- **内容建议**：
  - 项目演示：展示项目的核心功能
  - 代码展示：关键代码片段和架构说明
  - 技术栈说明：使用的技术和工具
  - 效果展示：动画、交互效果等

## 📷 摄影作品

### 文件命名规范
- `photo-1.jpg` - 第一张摄影作品
- `photo-2.jpg` - 第二张摄影作品
- `photo-3.jpg` - 第三张摄影作品
- `photo-4.jpg` - 第四张摄影作品
- `photo-5.jpg` - 第五张摄影作品
- `photo-6.jpg` - 第六张摄影作品

### 图片要求
- **格式**：JPG 或 PNG
- **分辨率**：建议宽度至少 800px
- **比例**：4:3 最佳（如 1600x1200, 1200x900）
- **大小**：建议每张不超过 2MB
- **质量**：适当压缩，平衡质量和加载速度
- **内容建议**：
  - 城市风光
  - 自然景观
  - 人文纪实
  - 建筑摄影
  - 校园生活
  - 旅行记录

## 🛠️ 图片优化工具推荐

### 在线工具
- **TinyPNG** (tinypng.com) - 无损压缩PNG/JPG
- **Squoosh** (squoosh.app) - Google的图片压缩工具
- **ImageOptim** (imageoptim.com) - Mac专用

### 视频压缩工具
- **HandBrake** - 免费开源视频压缩
- **FFmpeg** - 命令行视频处理
- **Clipchamp** - 在线视频编辑和压缩

### FFmpeg 压缩示例

```bash
# 压缩视频到合适大小
ffmpeg -i input.mp4 -c:v libx264 -crf 23 -preset medium -c:a aac -b:a 128k output.mp4

# 提取视频封面
ffmpeg -i input.mp4 -ss 00:00:01 -vframes 1 output.jpg
```

## 📤 部署到 Vercel

### 文件大小限制
Vercel 免费版限制：
- 单个文件：最大 100MB
- 总项目大小：最大 100MB（无服务器函数时）

### 优化建议
如果文件太大，可以：
1. 将视频托管到外部（YouTube, Bilibili, 阿里云OSS等）
2. 使用视频链接而非本地文件
3. 进一步压缩视频质量

### 使用外部视频链接

如果您想使用外部链接，可以修改 HTML 中的视频标签：

```html
<!-- 替换这部分 -->
<video controls>
    <source src="./portfolio/code-work-1.mp4" type="video/mp4">
</video>

<!-- 改为 iframe（例如 YouTube） -->
<iframe 
    src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
    frameborder="0" 
    allowfullscreen>
</iframe>
```

## ✅ 检查清单

部署前请确认：
- [ ] 创建了 `portfolio` 文件夹
- [ ] 视频文件命名正确（code-work-1.mp4 等）
- [ ] 图片文件命名正确（photo-1.jpg 等）
- [ ] 所有文件大小合适（视频<50MB，图片<2MB）
- [ ] 文件格式正确（MP4, JPG/PNG）
- [ ] 测试本地是否能正常播放/显示

## 💡 提示

- 如果某些文件暂时缺失，网站会自动显示占位符，不影响使用
- 可以先部署，后续再逐步添加作品文件
- 建议先在本地测试好再部署到 Vercel
- 记得在 Vercel 部署时包含 `portfolio` 文件夹

## 🆘 常见问题

**Q: 视频无法播放？**
A: 检查视频格式是否为 MP4（H.264），浏览器可能不支持其他格式。

**Q: 图片不显示？**
A: 确认文件名和路径是否正确，检查文件是否存在。

**Q: 文件太大怎么办？**
A: 使用压缩工具或考虑外部托管（YouTube, 图床等）。

**Q: 可以添加更多作品吗？**
A: 可以，修改 HTML 中的相应部分，增加更多卡片即可。


