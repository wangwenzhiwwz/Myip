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
- **多源 IP 智能竞速**：优先请求 `ipify`，仅在响应偏慢或失败时启动 `icanhazip`，成功后取消其余请求，兼顾速度与请求数量。
- **核心网络信息**：突出显示公网 IPv4、IPv6、运营商、ASN、时区与当地时间。
- **HTTP 连通性测试**：页面核心数据加载完成后再检测百度、Google、GitHub 的请求延迟，每 60 秒后台更新并支持手动刷新。
- **IP 安全度查询**：根据当前公网 IP 一键打开 Scamalytics 官方欺诈风险报告，无需在前端暴露 API 密钥。
- **按需地图**：不再自动加载嵌入式地图；点击主卡片后按语言跳转 Google Maps / 高德地图。

## 🛠️ 技术栈

* **Core**: HTML5, Vanilla JavaScript (ES6+)
* **Styling**: CSS3 Variables, Grid Layout, Flexbox
* **Typography**: 本地自托管并裁剪的 `WWZ Sans` 可变字体（基于 Inter，100–900），避免外部字体请求并减少传输体积
* **Icons**: Inline SVG (无额外的字体文件请求)
* **APIs**:
    * IP Detection: `ipify`, `icanhazip`
    * Geo Data: `ipwho.is`
    * IP Risk Report: `Scamalytics`
    * Map: `Google Maps` / `高德地图`

> Scamalytics 的结构化 API 需要账户和配额。当前纯静态版本使用官方报告页进行零密钥查询；如需在站内直接显示风险分数，应通过服务端代理安全保存 API 密钥。

## 📦 快速开始

本项目为**单文件应用 (Single-file Application)**，无需构建工具，无需 `npm install`。

### 方法 1: 直接运行
1. 下载 `index.html`。
2. 直接在浏览器中打开即可。

### 方法 2: 部署到静态托管
你可以直接将其部署到 GitHub Pages, Vercel, Netlify 或 Cloudflare Pages。

