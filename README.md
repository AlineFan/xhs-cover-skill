# 小红书封面生成 Skill

一个 Claude Code Skill，帮你自动生成小红书爆款封面。

把视频字幕、文章或内容描述发给 AI，一键生成高清封面 HTML，浏览器打开即是成品。

---

## 功能特性

- **4 种视觉风格**：干货图文 / 图文卡片 / 人物出镜 / 全图出镜
- **5 种主题配色**（图文卡片）+ 4 种排版布局
- **3 种封面比例**：3:4 / 1:1 / 4:3
- **9 款字体**可选：默认、思源宋体、思源黑体、站酷快乐、Sansita、Barrio、Sigmar、Bad Script、Bangers
- **点击文字直接编辑**，所见即所得
- **一键导出 3× 高清 PNG**（约 1080×1440）
- 图片支持拖拽移动 + 滚轮缩放

---

## 安装

将 `SKILL.md` 和 `assets/` 目录复制到 Claude Code skills 目录：

```bash
cp -r . ~/.claude/skills/xiaohongshu-cover/
```

---

## 使用

在 Claude Code 对话中说：

> "帮我做封面" / "生成小红书封面" / "做封面图"

然后粘贴视频字幕或内容描述，Claude 会自动分析内容、生成爆款标题，并输出一个完整的 `小红书封面.html` 文件。

双击打开 HTML，在浏览器中微调后导出 PNG 上传小红书。

---

## 文件结构

```
xiaohongshu-cover/
├── SKILL.md              # Claude skill 定义
└── assets/
    └── cover-scene1.html # 封面工具（含 4 种风格、导出功能）
```

---

## 技术说明

- 纯 HTML / CSS / JavaScript，无需任何依赖或构建步骤
- 图片导出使用 [html-to-image](https://github.com/bubkoo/html-to-image)
- 字体通过 Google Fonts 加载，导出时自动内联（解决跨域字体导出问题）
