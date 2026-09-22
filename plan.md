# 壁纸实验室 · Web App 计划

## 项目概述
一个纯静态 PWA 壁纸生成器，可在 iOS Safari 中"添加到主屏幕"成为桌面 App。
核心功能：生成**纯色背景 + 纯色文字**的手机壁纸，支持自定义文字内容、图案装饰、
背景/文字配色自选或套用固定搭配模板，一键导出 PNG。

## 技术栈
- 纯 HTML + CSS + 原生 JS（无构建，轻量，适合 PWA 与"添加到主屏幕"）
- Canvas 2D 离屏渲染高分辨率壁纸
- PWA：manifest.json + Service Worker（离线可用）

## 核心功能
1. 尺寸选择：iPhone 主流机型 + 通用方形（4:3 / 16:9 / 9:19.5 等）
2. 背景色：颜色选择器 + 预设调色板
3. 文字：内容输入、文字颜色、字号、行数、位置（上/中/下）、对齐、加粗
4. 图案装饰：无 / 圆点 / 斜线 / 网格 / 波纹
5. 固定搭配模板：多组精心挑选的背景+文字配色一键应用
6. 实时预览（等比缩放） + 下载高清 PNG

## 目录结构
```
wallpaper-maker/
├── index.html
├── manifest.json
├── sw.js
├── README.md
├── css/style.css
├── js/app.js
└── icons/ (icon-192.png, icon-512.png, apple-touch-icon.png)
```
