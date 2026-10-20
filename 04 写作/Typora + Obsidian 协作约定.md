---
title: Typora + Obsidian 协作约定
tags:
  - 工作流
  - 元信息
created: 2026-10-16
---

# Typora + Obsidian 协作约定

> 这份文档是给自己看的操作手册，不是给别人看的说明。

## 一句话分工

**Typora 写长文，Obsidian 管知识库。同一份文件，不产生副本。**

## 目录约定

Typora 只在`04 写作/` 里活动，Obsidian 管整个库。

| 目录 | 谁写| 用途 |
| --- | --- | --- |
| `04 写作/长文/` | Typora | 正在写的稿子 |
| `04 写作/已发布/` | Typora | 发完归档的稿子 |
| `04 写作/素材/` | 两者都行 | 灵感片段、随手记 |
| `00 收集箱/` | Obsidian | 网页剪藏、AI 剪藏插件落点 |
| `02 专题研究/` | Obsidian | 深度研究笔记 |
| `03 我的观点/` | Obsidian | 观点类笔记 |
| `05 金融市场/` | Obsidian | 金融相关 |
| `000 AI工程化/` | Obsidian | 技术沉淀 |

## Typora 一次性设置

`Typora → 偏好设置 → 保存`：

- **默认保存目录**设为 `/Users/young/Documents/obsidian-work/04 写作/长文`
- 这样每次新建文稿都直接落在 Obsidian 库内，不用手动挪

配好之后，Typora 里写完一篇，Obsidian 里立刻就能看到，**不需要导入、不需要复制、不需要同步**。

## Obsidian 侧的两处配置（已完成）

1. **CSS snippet 已启用**：`.obsidian/snippets/typora-github-style.css`
   把阅读视图调成 Typora GitHub 主题的观感（标题横线、代码块样式、表格斑马纹、行内代码配色），并修了中文表格错位。
   开关位置：设置 → 外观 → CSS snippets

2. **中文字体**：设置 → 外观 → 字体，建议改成**更纱黑体 Sarasa Mono SC** 或 `PingFang SC`
   这是解决中文表格对不齐的根治办法（snippet 里也做了等宽兜底）

## 日常流程

```
选题/灵感  →  Obsidian 的 00 收集箱 或 04 写作/素材
    ↓
开写→  Typora 打开 04 写作/长文 里的稿子，专注模式
    ↓
写完      →  稿子已在 Obsidian 库里
    ↓
发布      →  md 走排版转换 → 公众号编辑器
    ↓
归档      →  移到 04 写作/已发布/
```

## 几条硬规矩

1. **同一篇稿子不要在两个软件里同时打开编辑**。会互相覆盖，以最后保存的为准。
2. **图片用相对路径**。Typora 默认就是相对的，Obsidian 也认同一套规则，不要在Obsidian 里改成绝对路径。
3. **不要在 Obsidian 里用 Live Preview 改长文正文**。要改就去 Typora 改——这正是分工具的意义。
4. **Typora 那边记得开「严格换行符」**（偏好设置 → 排版），跟 Obsidian 行为对齐，避免空行语义不同。

## 还没做的

- [ ] Typora 默认保存目录改到 `04 写作/长文`（需要你在 GUI 里点，我改不了）
- [ ] 试一篇真实稿子走完整个流程
- [ ] Obsidian 升到 1.14.4（为了「打开库外文件」，可选）

## 相关

- [[公众号定位三件套]] —— 账号定位与内容方向
- 对比页面：`/Users/young/WorkBuddy/2026-10-16-02-22-44/obsidian-typora/render-comparison.html`