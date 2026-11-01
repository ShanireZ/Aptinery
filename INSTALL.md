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
(`emil-skills` also adds `remove-animations`).
Installing through the skills CLI by skill name is unaffected.

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
assets remain at the [pinned upstream](https://github.com/feitangyuan/onetake/tree/013a61ac8d98883c73733f59c06e49e9ba444f14/cases).
Films and historical working files mentioned in a case breakdown are upstream
case information, and are not necessarily included in this package.

## design-taste-frontend runtime requirements

The scripts require Node.js 22 or later and an installed Chrome, Edge or
Chromium browser. Set `CHROME_PATH` for a nonstandard browser location.
The scripts do not install dependencies or require API keys; `assets.mjs`
needs network access to search for and download stock images.

Working files go into the target project's `.taste-skill/`. Draw history goes
into `~/.taste-skill/history.json`, configurable with `TASTE_SKILL_HISTORY`.
This distribution includes only the upstream default skill; classic variants
and moved or retired image-generation stubs are excluded.

## brave-search runtime requirements

The skills call the Brave Search API and need your own API key from
[api.search.brave.com](https://api.search.brave.com) in `BRAVE_SEARCH_API_KEY`;
which endpoints work depends on your Brave plan, and search queries are sent to
Brave. The `bx` skill also uses the `bx` command-line tool. This package does not
install it; the skill's own text gives the upstream install command, which pipes
a downloaded script to `sh`. Upstream's `search` alias of `bx`, its ClawHub
variant and its setup guide are not included.
