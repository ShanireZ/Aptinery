# Aptinery

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![Type: Agent Skills marketplace](https://img.shields.io/badge/type-Agent%20Skills%20marketplace-blue.svg?style=flat-square)

[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文(TW)](README.zh-TW.md) | [日本語](README.ja.md)

面向程式開發、設計、動畫與教學的 Agent Skills。

透過相容的 skill 管理器或原生外掛市場逐項安裝。[技能目錄](docs/catalog.md)列出全部項目及其來源與授權。

## 安裝

例如，使用 skills CLI 安裝 `animate`：

```bash
npx skills add ShanireZ/Aptinery -g --skill animate
```

[安裝說明](INSTALL.md)包含 Codex、Claude Code、Copilot CLI、其他相容工具，以及各 skill 的執行相依。

## 原創與改編

| Skill | 署名與授權 |
| --- | --- |
| [`shanirez-style`](plugins/shanirez-style/skills/shanirez-style/SKILL.md) | Aptinery 原創，GPL-3.0。 |
| [`punk-poster-layout`](plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md) | 以 AdrianPunk 文章為基礎，Skill 由 Aptinery 改編與封裝；GPL-3.0。 |

儲存庫原創內容採用 [GNU GPL v3.0](LICENSE)。第三方內容保留各自條款，見 [NOTICE](NOTICE) 與[技能目錄](docs/catalog.md)。
`punk-cover` 上游限制再散布；本儲存庫的 GPL 聲明不構成其再散布授權。

[專案文件](docs/index.md) · [貢獻指南](CONTRIBUTING.md) · [來源與修改說明](NOTICE)
