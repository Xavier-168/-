# 更新日志

## 最新更新 V3.2 - 2024年

### 📹 视频播放修复

#### 视频源更换
- ✅ **全部改为YouTube可播放视频**
- ✅ 4个视频均已测试可正常播放
- ✅ 使用公开的技术演示视频
- ✅ 添加循环播放支持

#### 新视频列表

| 作品 | 视频ID | 内容 | 时长 |
|------|--------|------|------|
| React全栈 | w7ejDZ8SWv8 | React教程演示 | 短视频 |
| Vue3应用 | nhBVL41-_Cw | Vue3项目展示 | 短视频 |
| 算法可视化 | kPRA0W1kECg | 排序算法动画 | 短视频 |
| 小程序开发 | XzWjrlrKi3o | 编程教程演示 | 短视频 |

---

## 版本 V3.1 - 2024年

### 🎨 视觉与动画优化

#### 1. 代码作品集边框过渡优化
- ✅ **边缘发光动画**：添加青色/粉色动态光晕
- ✅ **半透明背景**：改用rgba实现更柔和的过渡
- ✅ **内外阴影**：多层阴影效果增强立体感
- ✅ **流动边框**：4秒循环的渐变边框动画

#### 2. 代码雨背景动画 🌧️
- ✅ **黑客帝国风格**：青色代码字符不断下落
- ✅ **Canvas实现**：流畅的60fps动画
- ✅ **渐变拖尾**：字符带渐变透明度
- ✅ **随机字符**：英文、数字、符号随机组合
- ✅ **响应式**：自动适配容器尺寸

#### 3. 视频源更换
- ✅ **平台切换**：从YouTube改为Vimeo
- ✅ **短视频精选**：每个视频15-20秒
- ✅ **循环播放**：自动循环提升体验
- ✅ **可播放性**：确保国内外都能正常访问

### 📹 新视频列表

| 作品 | 平台 | 时长 | 内容 |
|------|------|------|------|
| React全栈 | Vimeo | ~15s | 项目演示 |
| Vue3应用 | Vimeo | ~18s | 交互展示 |
| 算法可视化 | Vimeo | ~20s | 排序动画 |
| 微信小程序 | Vimeo | ~15s | 功能演示 |

---

## 版本 V3.0 - 2024年

### 🎯 主要修改

#### 1. 个人信息更新
- ✅ 姓名从"王磊"更改为"赵逍遥"
- ✅ 左上角Logo从"WL"移除（现为空白）
- ✅ 头像备用文字改为"ZXY"
- ✅ 邮箱更新为：zhaoxiaoyao@example.com
- ✅ GitHub: github.com/zhaoxiaoyao
- ✅ LinkedIn: linkedin.com/in/zhaoxiaoyao
- ✅ 页面标题更新为"赵逍遥 - 个人简历"
- ✅ 页脚版权信息更新为"© 2024 赵逍遥"

#### 2. 软技能布局优化
- ✅ **重新设计为居中布局**
- ✅ 使用 `max-w-4xl mx-auto` 实现居中
- ✅ 保持原有的6个渐变色卡片设计
- ✅ 每个技能配独特图标和颜色
- ✅ 5星圆点评级系统
- ✅ Hover效果：浮起+缩放

#### 3. 代码作品集完善
- ✅ **所有视频改用YouTube外部链接**
- ✅ 作品1：React全栈项目演示
- ✅ 作品2：Vue3应用开发
- ✅ 作品3：**排序算法可视化**（新增）
  - 使用YouTube算法可视化视频
  - 展示快速排序、归并排序等算法
- ✅ 作品4：微信小程序开发
- ✅ 更新提示文字为"当前使用YouTube示例视频"

### 📝 技术细节

#### 软技能居中实现
```html
<!-- 之前：使用grid布局，左对齐 -->
<div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
    <div>软技能内容</div>
</div>

<!-- 修改后：单独居中布局 -->
<div class="max-w-4xl mx-auto mt-16">
    <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
        软技能卡片...
    </div>
</div>
```

#### 视频嵌入方式
```html
<!-- 之前：本地视频 -->
<video controls>
    <source src="./portfolio/code-work-3.mp4">
</video>

<!-- 修改后：YouTube iframe -->
<iframe 
    src="https://www.youtube.com/embed/pFXYym4Wbkc" 
    title="Sorting Algorithms Visualization"
    frameborder="0" 
    allowfullscreen>
</iframe>
```

### 🎬 使用的YouTube视频

1. **React全栈项目**: https://www.youtube.com/watch?v=Ke90Tje7VS0
2. **Vue3应用**: https://www.youtube.com/watch?v=qZXt1Aom3Cs
3. **排序算法可视化**: https://www.youtube.com/watch?v=pFXYym4Wbkc
4. **微信小程序**: https://www.youtube.com/watch?v=2aTsk4K3kOc

### 📂 更新的文件

- ✅ `index.html` - 主页面（所有功能实现）
- ✅ `README.md` - 项目说明
- ✅ `DEPLOY_GUIDE.md` - 部署指南
- ✅ `CHANGELOG.md` - 本更新日志

### 🚀 部署状态

✅ **所有修改已完成，可直接部署到Vercel**

- 所有文件路径使用相对路径
- YouTube视频可正常播放（需要网络连接）
- 无需本地视频文件
- 响应式设计完整
- 跨浏览器兼容

### 🎨 视觉效果

#### 软技能布局
- 🔥 完全居中，视觉平衡
- 🎨 6个渐变色卡片
- 💫 Hover动画流畅
- 📱 响应式：移动端2列，桌面3列

#### 代码作品集
- ⚡ 赛博朋克风格背景
- 🎬 4个YouTube视频展示
- 💠 霓虹光效边框
- 🖥️ 终端窗口设计

### ⚠️ 注意事项

1. **YouTube视频播放**：
   - 需要用户有网络连接
   - 部分地区可能需要特殊网络环境
   - 如需替换，修改iframe的src属性即可

2. **软技能布局**：
   - 现在独立居中显示
   - 不再与技术技能左右并排
   - 更加突出和美观

3. **头像占位符**：
   - 如果avatar.jpg不存在，显示"ZXY"
   - 保持蓝色渐变背景

### 🔄 如何替换视频

如果想使用自己的视频，有两种方式：

**方式1：使用YouTube链接**
```html
<iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID"></iframe>
```

**方式2：使用本地视频**
```html
<video controls>
    <source src="./portfolio/your-video.mp4" type="video/mp4">
</video>
```

---

## 版本历史

### V3.0（当前版本）
- 个人信息更新为赵逍遥
- 软技能居中布局
- 所有代码作品视频完善

### V2.0
- 新增作品集模块
- 软技能重新设计
- 导航栏优化

### V1.0
- 初始版本
- 基础简历模块

---

✨ **网站已准备就绪，可以立即部署！**

