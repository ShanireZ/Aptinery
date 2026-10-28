# Aptinery

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![Type: Agent Skills marketplace](https://img.shields.io/badge/type-Agent%20Skills%20marketplace-blue.svg?style=flat-square)

Agent Skills for coding, design, animation and teaching.

Install skills individually through compatible skill managers or native plugin
marketplaces. [The catalog](docs/catalog.md) lists every entry and its source/license.

## Install

For example, install `animate` with the skills CLI:

```bash
npx skills add ShanireZ/Aptinery -g --skill animate
```

[Installation instructions](INSTALL.md) cover Codex, Claude Code, Copilot CLI,
other compatible tools and skill-specific runtime requirements.

## Original work and adaptations

| Skill | Attribution and license |
| --- | --- |
| [`shanirez-style`](plugins/shanirez-style/skills/shanirez-style/SKILL.md) | Original Aptinery work; GPL-3.0. |
| [`punk-poster-layout`](plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md) | Based on AdrianPunk articles; skill adapted and packaged by Aptinery; GPL-3.0. |

Original repository material uses [GNU GPL v3.0](LICENSE). Third-party material
retains its own terms; see [NOTICE](NOTICE) and the [catalog](docs/catalog.md).
The `punk-cover` upstream restricts redistribution; no redistribution permission
is established by this repository's GPL declaration.

[Project documentation](docs/index.md) · [Contributing](CONTRIBUTING.md) · [Source and modification notices](NOTICE)
