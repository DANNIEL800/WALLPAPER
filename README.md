# 壁纸实验室 · 纯色壁纸生成器

生成**纯色背景 + 纯色文字**的手机壁纸，支持自定义文字内容、图案装饰、背景/文字配色自选或一键套用固定搭配模板。是一个可离线使用的 PWA，可添加到 iOS / Android 桌面成为 App。

## 功能

- 画布尺寸：iPhone 全屏、1080×2340、iPhone Pro、16:9、1:1、iPad
- 背景：纯色 / 线性渐变（4 方向）/ 径向渐变，背景色 + 渐变色 2 + 12 色板
- 文字：内容输入、颜色、字号、垂直位置、粗体/斜体、字间距
- 文字自由拖拽：在预览上直接拖动到任意位置
- 对比度检测：实时显示背景与文字的 WCAG 对比度等级
- 图案装饰：圆点 / 斜线 / 网格 / 同心圆 / 对角块，可独立配色、调透明度
- 配色模板：12 组精选背景+文字搭配，一键应用
- 随机灵感：一键换一组配色
- 参数持久化：自动保存设置，重开不丢（localStorage）
- 下载：当前尺寸高清 PNG，或一键导出全部 6 种尺寸（打包 zip）

## 快速开始

### 环境要求
- 无需构建、无需 Node.js。纯静态文件，任意静态服务器即可运行。

### 运行方式

方式一（本地预览，任选其一）：
```bash
# Python
cd wallpaper-maker && python3 -m http.server 8080
# 浏览器打开 http://localhost:8080
```

方式二（部署到服务器/对象存储/CDN）：直接把整个 `wallpaper-maker/` 目录上传即可。

### 安装到手机桌面
- **iOS**：用 Safari 打开站点 → 点分享按钮 → 添加到主屏幕。
- **Android**：用 Chrome 打开 → 右上角菜单 → 安装应用（或点击页面顶部"安装"按钮）。

安装后即为独立 App，离线可用。

## 目录结构
```
wallpaper-maker/
├── index.html      # 主页面
├── css/style.css   # 样式
├── js/app.js       # 渲染与交互逻辑
├── manifest.json   # PWA 清单
├── sw.js           # Service Worker（离线缓存）
├── icons/          # 应用图标
└── README.md
```

## 技术栈
- 原生 HTML + CSS + JavaScript（Canvas 2D 离屏渲染）
- PWA：manifest.json + Service Worker
