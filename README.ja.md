# Aptinery

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![Type: Agent Skills marketplace](https://img.shields.io/badge/type-Agent%20Skills%20marketplace-blue.svg?style=flat-square)

[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文(TW)](README.zh-TW.md) | [日本語](README.ja.md)

コーディング、デザイン、アニメーション、教育向けの Agent Skills です。

対応するスキルマネージャーや標準プラグインマーケットプレイスから個別にインストールできます。[カタログ](docs/catalog.md)で全スキルの出典とライセンスを確認できます。

## インストール

例として、skills CLI で `animate` をインストールします。

```bash
npx skills add ShanireZ/Aptinery -g --skill animate
```

[インストール手順](INSTALL.md)には Codex、Claude Code、Copilot CLI、その他の対応ツール、およびスキルごとの実行依存関係を記載しています。

## オリジナルと翻案

| Skill | 帰属とライセンス |
| --- | --- |
| [`shanirez-style`](plugins/shanirez-style/skills/shanirez-style/SKILL.md) | Aptinery のオリジナル作品。GPL-3.0。 |
| [`punk-poster-layout`](plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md) | AdrianPunk の記事を基に Aptinery がスキル化・パッケージ化。GPL-3.0。 |

リポジトリのオリジナル部分は [GNU GPL v3.0](LICENSE) です。第三者の資料には個別の条件が適用されます。[NOTICE](NOTICE) と[カタログ](docs/catalog.md)を参照してください。
`punk-cover` の上流は再配布を制限しており、このリポジトリの GPL 宣言はその再配布許諾を意味しません。

[プロジェクト文書](docs/index.md) · [出典と変更記録](NOTICE)
