[README.md](https://github.com/user-attachments/files/31016883/README.md)
# 🎬 B站关注UP主收藏夹

> 一个纯前端的 Bilibili 关注 UP 主收藏与展示页面，支持搜索、分类筛选、分组收藏、主题切换等功能，数据来源于 B 站关注列表。

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

## 📖 项目简介

本项目是一个**单页静态网页**，将你在 B 站关注的 UP 主以「卡片墙」的形式集中展示。每张卡片包含 UP 主头像、昵称、认证标签、大会员标识、个人简介与 UID，点击即可跳转到对应的 B 站空间主页。

无需任何后端与构建工具，直接双击 `index.html` 即可在浏览器中打开使用，也可以部署到 GitHub Pages 等任意静态托管平台。

## ✨ 功能特性

- 🔍 **实时搜索** — 按 UP 主昵称、简介、UID 关键字快速过滤
- 🏷️ **分类筛选** — 百大UP主、影视、美食、运动、科技、出行/旅行、官方账号、大会员等维度一键筛选
- 📁 **自定义分组** — 自由新建/删除分组，将喜欢的 UP 主收藏进分组，支持**导入 / 导出**分组数据（JSON）
- ⭐ **卡片收藏** — 卡片右上角星标收藏热区，动效反馈
- 🎨 **多主题切换** — 内置晨曦粉、星夜紫、晴空青、青葱绿、晚霞橙 5 套配色
- 🌗 **时段自动配色** — 根据当前访问时间自动匹配推荐主题（清晨/正午/黄昏/夜晚）
- 📄 **分页浏览** — 大列表自动分页，支持上一页 / 下一页 / 页码跳转
- ⬆️ **返回顶部** — 一键回到页面顶端
- 📱 **响应式布局** — 自适应桌面端与移动端屏幕
- 🕐 **实时时钟** — 顶部显示当前时间与主题名

## 📂 项目结构

```
bilibili_up/
├── index.html          # 主页面（页面结构与样式、逻辑均内嵌于此单文件）
├── followings.json     # B站关注列表原始数据（B站 API 导出）
└── README.md           # 项目说明
```

## 🚀 使用方法

### 在线预览 / 部署

将本目录内容推送至 GitHub 后，开启仓库的 **GitHub Pages**（Settings → Pages → 选择分支），即可通过 `https://<用户名>.github.io/<仓库名>/` 访问。

### 本地打开

直接双击 `index.html`，或使用 VS Code 的 Live Server 插件启动。

## 🔄 如何更新关注数据

1. 登录 B 站网页版，通过关注接口（`https://api.bilibili.com/x/relation/followings?vmid=你的UID`）导出最新的关注列表为 `followings.json`。
2. 更新 `followings.json` 后，重新生成 `index.html` 中的卡片数据即可。

## 🛠️ 技术栈

- 原生 **HTML5 + CSS3 + JavaScript**（无任何外部依赖、无框架、无构建步骤）
- 数据存储：`localStorage` + `Cookie` 双写（分组与主题偏好）
- 界面风格参考 B 站品牌色（`#FB7299`）

## ⚠️ 免责声明

- 本项目仅用于个人学习与收藏展示，**不抓取、不存储、不传播任何视频内容**。
- UP 主头像、昵称、简介等公开信息版权归 B 站及对应 UP 主所有，请勿用于商业用途。
- 若涉及侵权，请联系作者删除相关内容。

## 📄 License

[MIT](./LICENSE)
