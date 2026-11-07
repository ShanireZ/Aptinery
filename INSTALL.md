# Install Aptinery skills

The skills CLI takes a skill name; plugin marketplaces take a plugin name. Most
skills install as a plugin with the same name. `k12-teacher-skills`,
`emil-skills` and `brave-search` each group several skills, and the
[catalog](docs/catalog.md) lists their members. The examples below use `animate` for the skills CLI and `emil-skills`
for plugin marketplaces; replace them with any name from the catalog.

## skills CLI

For Codex, Claude Code, Cursor, OpenCode and other compatible tools:

```bash
npx skills add ShanireZ/Aptinery -g --skill animate
```

To install all skills globally, omit `--skill animate`.

## Claude Code marketplace

```bash
claude plugin marketplace add ShanireZ/Aptinery
claude plugin install emil-skills@aptinery
```

`pick-ui-library`, `prototype` and `review-animations` retain their upstream
explicit invocation contract. Invoke them with `/emil-skills:pick-ui-library`,
`/emil-skills:prototype` and `/emil-skills:review-animations`, respectively.

## Codex / ChatGPT marketplace

```bash
codex plugin marketplace add ShanireZ/Aptinery
codex plugin add emil-skills@aptinery
```

The same three skills disable implicit invocation through `agents/openai.yaml`.
Invoke them explicitly with `$pick-ui-library`, `$prototype` and `$review-animations`.

## GitHub Copilot CLI marketplace

```bash
copilot plugin marketplace add ShanireZ/Aptinery
copilot plugin install emil-skills@aptinery
```

## Agent Plugins clients

Each `plugins/<plugin-name>/plugin.json` is an independent Agent Plugins v1
entry. Installable names match the plugin names in the [catalog](docs/catalog.md).

## Moving from per-skill plugins

Before 0.6.0, each of these skills was its own plugin. The four K-12 plugins
(`k12-lesson-plan-creation`, `k12-lesson-differentiation`, `k12-lesson-prep` and
`k12-check-for-understanding`) are now the skills of `k12-teacher-skills`. Each
Emil Kowalski skill was also its own plugin: `emil-design-eng`,
`animate`, `animate-expo`, `review-animations`, `improve-animations`,
`find-animation-opportunities`, `animation-performance`, `animation-vocabulary`,
`apple-design`, `write-swift`, `break-ui`, `mobile-native`, `pick-ui-library`,
`prototype` and `ask-sonner`. Those plugin IDs no longer exist. Remove them and
install `k12-teacher-skills` or `emil-skills`, which contain all of these skills
(`emil-skills` also adds `remove-animations`, and 0.7.0 adds `choreograph`).
Installing through the skills CLI by skill name is unaffected.

`punk-avatar` left the distribution in 0.4.0, and Aptinery no longer updates
it. If `punk-avatar@aptinery` is still installed, uninstall it; `punk-cover` and
`punk-poster-layout` remain available.

## OneTake runtime requirements

`onetake` uses the same installation entry points. From a repository checkout,
use `npx skills add . --skill onetake`, or add the local Claude marketplace with
`claude plugin marketplace add .` and install `onetake@aptinery`.

Installing a skill does not install its runtime dependencies. OneTake requires
Python 3, Playwright and Chromium, NumPy, SciPy, Pillow, Matplotlib, fonttools,
brotli, FFmpeg/ffprobe and Node.js. Reference-film analysis also needs
opencv-python. Narration also needs faster-whisper and Kokoro
(`kokoro-onnx`, `soundfile`); Japanese narration additionally needs `misaki[ja]`
and `unidic-lite`. Usage remains in the skill and its references.

The package includes runtime libraries, scripts, templates, fonts and their
licenses, the gallery and case breakdowns. Large example films and promotional
assets remain at the [pinned upstream](https://github.com/feitangyuan/onetake/tree/abb6d17279cdc749e27e99aa534a062d8fd01ced/cases).
Films and historical working files mentioned in a case breakdown are upstream
case information, and are not necessarily included in this package.

## design-taste-frontend runtime requirements

tasteskill 2.5.0 requires Node.js 22 or later and an installed Chrome, Edge or
Chromium browser; an existing `CHROME_PATH` selects a nonstandard browser
location. The scripts drive the browser over the DevTools protocol and install
nothing, and `ffmpeg` enables the photograph crops and WebP conversion. Pages
load their fonts from Google Fonts at run time.

The skill ships its assets: a starter page, the system CSS and JS, and the
layout, effect, component, diagram, photograph, icon, moment, scene and
product-render packs. Dealt working files and the deal history go into the
target project's `.taste-skill/` folder. Bundled photographs and icons keep the
licences recorded in the skill's own credits JSON files.

This distribution includes only the upstream default skill; classic variants
and moved or retired image-generation stubs are excluded.

## figma-designer requirements

`figma-designer` works through the Figma MCP and adds design rules on top of
the official Figma skills (`figma-use`, `figma-generate-design`,
`figma-generate-library`), which are not bundled here. It installs nothing; a
Figma MCP session and those skills must be available before it can edit a file.

## brave-search runtime requirements

The skills call the Brave Search API and need your own API key from
[api.search.brave.com](https://api.search.brave.com) in `BRAVE_SEARCH_API_KEY`;
which endpoints work depends on your Brave plan, and search queries are sent to
Brave. The `bx` skill also uses the `bx` command-line tool. This package does not
install it; the skill's own text gives the upstream install command, which pipes
a downloaded script to `sh`. Upstream's `search` alias of `bx`, its ClawHub
variant and its setup guide are not included.
