# Aptinery

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![Type: Agent Skills marketplace](https://img.shields.io/badge/type-Agent%20Skills%20marketplace-blue.svg?style=flat-square)

[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文(TW)](README.zh-TW.md) | [日本語](README.ja.md)

面向编程、设计、动画和教学的 Agent Skills。

通过兼容的 skill 管理器或原生插件市场逐项安装。[技能目录](docs/catalog.md)列出全部项目及其来源与许可。

## 安装

例如，使用 skills CLI 安装 `animate`：

```bash
npx skills add ShanireZ/Aptinery -g --skill animate
```

[安装说明](INSTALL.md)包含 Codex、Claude Code、Copilot CLI、其他兼容工具，以及各 skill 的运行依赖。

## 原创与改编

| Skill | 署名与许可 |
| --- | --- |
| [`shanirez-style`](plugins/shanirez-style/skills/shanirez-style/SKILL.md) | Aptinery 原创，GPL-3.0。 |
| [`punk-poster-layout`](plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md) | 根据 AdrianPunk 文章，Skill 由 Aptinery 改编包装；GPL-3.0。 |

仓库原创内容采用 [GNU GPL v3.0](LICENSE)。第三方内容保留各自条款，见 [NOTICE](NOTICE) 与[技能目录](docs/catalog.md)。
`punk-cover` 上游限制再分发；本仓库的 GPL 声明不构成其再分发授权。

[项目文档](docs/index.md) · [来源与修改说明](NOTICE)
