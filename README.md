# IP Insight | Monochrome

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=flat&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=flat&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=flat&logo=javascript&logoColor=%23F7DF1E)

**IP Insight** 是一个极简、高性能的单页 IP 信息查询面板。采用极致的黑白（Monochrome）设计风格，提供详细的网络身份信息、地理位置、连通性测试及设备指纹。

它完全基于原生 HTML/CSS/JS 构建，**零外部依赖**（无 FontAwesome，无 Bootstrap），单文件即可运行。

## ✨ 主要特性

### 🎨 视觉与交互
- **极致黑白设计**：精心调校的黑白灰配色，专业且克制。
- **Bento 网格布局**：响应式栅格系统，自动适配桌面与移动端。
- **深色模式支持**：自动跟随系统偏好，亦可手动一键切换。
- **智能排版**：采用 `Grid Dense` 布局，当某些数据（如 IPv6 或 LAN IP）获取失败时，卡片会自动隐藏并由后续卡片补位，保持界面紧凑。
- **磨砂玻璃质感**：地图悬浮按钮采用 Glassmorphism 效果。

### 🚀 核心功能
- **多源 IP 并发检测**：使用 `Race` 竞速模式，同时请求 `ipify`, `myip.is`, `icanhazip` 等多个源，优先展示最快返回的结果，大幅提升 **IPv6** 识别率。
- **网络位置上下文**：显示时区、当地时间、经纬度、UTC 偏移、ASN 与运营商。
- **网络连通性测试**：检测到百度、Google、GitHub 的请求延迟，每 15 秒自动刷新，并在页面切回前台时更新。
- **IP 安全度查询**：根据当前公网 IP 一键打开 Scamalytics 官方欺诈风险报告，无需在前端暴露 API 密钥。
- **嵌入式地图**：集成 OpenStreetMap，根据日夜模式自动应用黑白滤镜，支持一键跳转 Google Maps / 高德地图。
- **设备指纹**：显示浏览器内核、操作系统及屏幕分辨率。

## 🛠️ 技术栈

* **Core**: HTML5, Vanilla JavaScript (ES6+)
* **Styling**: CSS3 Variables, Grid Layout, Flexbox
* **Icons**: Inline SVG (无额外的字体文件请求)
* **APIs**:
    * IP Detection: `ipify`, `myip.is`, `icanhazip`
    * Geo Data: `ipwho.is`
    * IP Risk Report: `Scamalytics`
    * Map: `OpenStreetMap`

> Scamalytics 的结构化 API 需要账户和配额。当前纯静态版本使用官方报告页进行零密钥查询；如需在站内直接显示风险分数，应通过服务端代理安全保存 API 密钥。

## 📦 快速开始

本项目为**单文件应用 (Single-file Application)**，无需构建工具，无需 `npm install`。

### 方法 1: 直接运行
1. 下载 `index.html`。
2. 直接在浏览器中打开即可。

### 方法 2: 部署到静态托管
你可以直接将其部署到 GitHub Pages, Vercel, Netlify 或 Cloudflare Pages。

