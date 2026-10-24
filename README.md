# 漫游大学 / Paper Campus

纯 HTML、CSS、JavaScript 线上大学社区交互 Demo，无构建依赖。

## 启动

在项目目录运行 `python3 -m http.server 4173`，访问 `http://localhost:4173/dist/`。
也可直接打开 `dist/index.html`，浏览器的本地存储和文件预览能力可能受 file URL 限制。

## 内容

- 原创 SVG 手绘校园地图、建筑悬浮反馈、点击镜头放大、地图缩放
- 自习室：12 张可选桌子，25 分钟专注 / 5 分钟休息，暂停与重置，完成奖励
- 图书馆：推荐书架、原创阅读导览、收藏、本地 PDF 阅读、作业提交记录
- 食堂：本地规则菜谱匹配、菜单保存
- 课堂：公开课搜索与学科筛选，高校官方链接
- 研讨室：本地留言
- 小卖部：成长币兑换头像
- 娱乐室：记忆翻牌、反应测试、石头剪刀布
- 本地学习记录与合成雨声环境音

## 演示边界

没有后端。AI Agent、多用户同步、文件上传、支付未接入。作业仅保存文件名及时间。成长币与学习记录使用浏览器 localStorage。课程推荐为关键词过滤；菜谱为预设规则。128 位同学为示例数据。

## 视觉参考

https://github.com/abhishekmill/R3FSketchMaterial

参考其纸张、钢笔排线与镜头推进方向，建筑和交互为原创 SVG/CSS 实现，未使用其 Three.js 材质代码或第三方 3D 模型。

## GitHub Pages

在仓库的 Settings → Pages 中选择 Deploy from a branch，使用 `main` 分支的 `/ (root)` 目录。根目录入口会转到 `dist/`。所有资源采用相对路径，可部署在 GitHub Pages 项目子路径下。

## 纸团新版

首页提供真实 Three.js / cannon-es 揉纸交互：点击纸团展开，拖动后甩出，或使用七个文字入口选择空间。展开后点击“进入这个空间”。原校园街道地图可通过“校园地图”展开。

`dist/crumple/` 基于 [item-develop/paper-crumple-demo](https://github.com/item-develop/paper-crumple-demo)（MIT）改编，保留其 Houdini VAT 模型、动画纹理与物理交互。版权与许可见 `dist/crumple/LICENSE`。纸卡内容及校园功能由本项目改编。Three.js 和 cannon-es 通过 CDN 加载，需要网络；3D 不可用或系统减少动态效果时可直接使用文字入口。
