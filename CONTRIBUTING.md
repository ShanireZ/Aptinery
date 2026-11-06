# Contributing to Aptinery

Use [GitHub Issues](https://github.com/ShanireZ/Aptinery/issues) for bugs and
proposed changes. Keep changes scoped to the requested skill or packaging task.

## Package contract

- A plugin contains one skill with the same name, or a family of skills from one
  source that are used together (`k12-teacher-skills`, `emil-skills`,
  `brave-search`). Each skill directory name matches its `name` frontmatter and
  is unique across the repository. The manifests, rather than a separately
  maintained count, define the installable catalog. Changing plugin IDs or
  grouping is a breaking change: document the migration in INSTALL.md and
  advance the synchronized version.
- `plugins/*/plugin.json` provides Agent Plugins v1 metadata;
  `plugins/*/.codex-plugin/plugin.json` and `.agents/plugins/marketplace.json`
  serve Codex/ChatGPT; `plugins/*/skills/` supports direct skill discovery.
- Claude uses `plugins/*/.claude-plugin/plugin.json`, the
  `.claude-plugins/emil-skills/.claude-plugin/plugin.json` adapter, and
  `.claude-plugin/marketplace.json`. Keep names, versions, source paths and
  skill entry points synchronized across these manifests.
- `pick-ui-library`, `prototype` and `review-animations` require
  `policy.allow_implicit_invocation: false` in `agents/openai.yaml`. Preserve
  their upstream Markdown bodies and documented frontmatter adaptations,
  including the explicit-only sentence in the review description.
- `.claude-plugins/emil-skills/skills/` holds all Emil skills byte-identical to
  the pinned source trees, so those three keep upstream
  `disable-model-invocation: true`. The Claude marketplace must point to this
  mirror, and its skill set must match `plugins/emil-skills/skills/`.

## Preserve sources and licenses

[NOTICE](NOTICE) records the exact upstream commits and intentional adaptations.
Keep root, plugin and skill attribution notices and applicable license copies.
Do not infer redistribution permission from a manifest or the repository GPL.

- The four K-12 skill trees remain verbatim Apache-2.0 imports, including their
  license frontmatter, SPDX references and NOTICE files. Any future local change
  needs a prominent modification notice and a NOTICE update. Optional upstream
  `.mcp.json` configuration is excluded; preserve the connector-free fallback.
- Emil Kowalski's skills retain MIT license copies at the plugin root and in each
  skill directory, and original frontmatter except for the three documented
  invocation adaptations.
- `landing-page-design` and the `brave-search` skills are verbatim MIT imports:
  each SKILL.md is byte-identical to the pinned upstream, with LICENSE copies at
  the plugin root and in each skill directory. Upstream READMEs, setup guides,
  tests, workflows, the `search` alias of `bx` and the ClawHub variant are not
  imported.
- `design-taste-frontend` preserves every upstream `skills/taste-skill/` file
  byte-for-byte under the renamed directory, with MIT licenses added at plugin
  and skill roots. Only the default skill is included. Its bundled photographs
  and brand/interface icons keep the licenses recorded in its own credits JSON
  files; do not relabel them.
- `figma-designer` is a verbatim MIT import of Elaya's upstream skill, with
  LICENSE copies and client manifests added locally. It depends on the Figma
  MCP and the official Figma skills, which are not bundled; keep that
  requirement documented in INSTALL.md.
- OneTake retains its PolyForm Noncommercial license at both roots, its Required
  Notice, and font licenses. Preserve the documented description/path note and
  eight whitespace transformations. Runtime libraries, scripts, references,
  templates, fonts, gallery and case README files are included; large example
  films and promotional media remain upstream.
- `punk-cover` retains its existing selected content and 34 style directories.
  `../../styles/{style-id}` is a live dependency. Its Taiwan Traditional Chinese
  localization and documented cover adaptations are not a verbatim upstream
  import. Keep their provenance distinction. The current upstream restricts
  redistribution; retain that limitation and require independently verifiable
  rights-holder evidence before making a new license claim. `punk-avatar` and
  `punk-ip-video-cover` are outside this distribution.
- `punk-poster-layout` is an Aptinery adaptation of the two attributed AdrianPunk
  articles, not an upstream source-tree copy. Preserve all 32 named systems,
  image-prompt and HTML/CSS guidance, review criteria, and its composition-only
  responsibility. The article archives are not package dependencies.
- `shanirez-style` is original GPL-3.0 material. Its frontmatter contains only
  `name` and `description`, its name matches its directory, and SKILL.md stays
  under 500 lines. Follow the [corpus method](docs/style-corpus-method.md) before
  adding, weakening or strengthening any measured claim.

## Verification

Run commands from the repository root. This package has no application build
or test entry point. State which checks were actually run and their limits.

| Check | Prerequisite and scope |
| --- | --- |
| `git diff --check` | Diagnoses whitespace; does not establish semantic or license correctness. |
| Parse JSON manifests and YAML metadata | Check matching names, versions, paths, skill entry points, explicit invocation policies, LICENSE/NOTICE files and required references/styles. |
| Check local Markdown links, anchors and metadata references | Check the actual files being distributed; distinguish omitted upstream case assets from missing package dependencies. |
| Compare vendor files to pinned upstream Git objects | Report missing source objects as unverified; JSON parsing does not replace this comparison. |
| `npx skills add . --list` | Requires the skills CLI; npx may download tools. Checks discovery, not each client's runtime behavior. |
| `claude plugin validate . --strict` | Requires Claude CLI and an environment where running it is authorized. Checks Claude manifests, not other clients or vendor identity. |

Keep static compatibility review distinct from client execution. Do not install
tools, adopt dependencies or invoke a model as a side effect of a static review.
For C++ template changes, compile the changed example with an available C++14
compiler and run hand-checked input; keep binaries outside the package.

`.gitattributes` fixes LF. The four K-12 trees disable trailing-space and
blank-at-EOF diagnostics, and the two copies of Emil's `write-swift/SKILL.md`
disable blank-at-EOF, to preserve upstream bytes; keep these exceptions narrow.
The no-blank-line/no-final-newline rule applies to generated OJ C++ solutions,
not to Markdown.
