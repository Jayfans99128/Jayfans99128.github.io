# 罗卓聪 · 个人主页

纯静态个人网页（HTML + CSS + 原生 JS），双击 `index.html` 即可本地打开预览，无需任何构建工具。

## 目录结构

```
个人网页/
├── index.html          # 主页面
├── css/style.css       # 样式
├── js/main.js          # 交互（导航、滚动动画、复制提示等）
├── assets/
│   ├── video-poster.jpg        # 视频封面（从演示视频抽取的一帧）
│   └── zhixiaozhu-demo.mp4     # 职小猪项目演示视频（2026.06.09，约 3 分钟，原「6月9日(2).mp4」）
├── 测试岗位简历.pdf / .docx
└── 车辆岗位简历.pdf / .docx
```

## 页面内容

- **首屏**：姓名、专业方向、邮箱、两个岗位简历下载入口
- **关于我**：教育经历（广东技术师范大学 · 车辆工程 · 2023.9–2027.7）、个人简介
- **项目经历**（整合自两份简历）：
  - ⭐ 职小猪 · 智能求职 Agent —— 重点展示，含演示视频
  - 智能陪伴交互系统
  - 轮胎-颗粒土壤相互作用仿真
  - 弓箭发射过程动态仿真
- **专业技能**：测试开发 / AI 应用 与 车辆工程 / 仿真分析 两个方向
- **联系方式**：邮箱、GitHub、简历

## 修改内容

- 改文字：直接编辑 `index.html` 对应区块
- 改配色：`css/style.css` 顶部 `:root` 变量（`--brand` 为主色）
- 换视频：覆盖 `assets/zhixiaozhu-demo.mp4`（或改 `index.html` 中 `<source>` 的路径）

## 部署提示

- 视频约 88MB，本地打开流畅；如需上线（如 GitHub Pages），建议先压缩：
  `ffmpeg -i zhixiaozhu-demo.mp4 -vf scale=1280:-2 -crf 28 -preset slow -an demo-small.mp4`
  压缩后体积可降到几 MB，网页加载会快很多。
