# Install Aptinery skills

The individual commands below use `animate` as an example. Replace it with any
skill name in the [catalog](docs/catalog.md).

## skills CLI

For Codex, Claude Code, Cursor, OpenCode and other compatible tools:

```bash
npx skills add ShanireZ/Aptinery -g --skill animate
```

To install all skills globally, omit `--skill animate`.

## Claude Code marketplace

```bash
claude plugin marketplace add ShanireZ/Aptinery
claude plugin install animate@aptinery
```

`pick-ui-library`, `prototype` and `review-animations` retain their upstream
explicit invocation contract. Invoke them with `/pick-ui-library:pick-ui-library`,
`/prototype:prototype` and `/review-animations:review-animations`, respectively.

## Codex / ChatGPT marketplace

```bash
codex plugin marketplace add ShanireZ/Aptinery
codex plugin add animate@aptinery
```

The same three skills disable implicit invocation through `agents/openai.yaml`.
Invoke them explicitly with `$pick-ui-library`, `$prototype` and `$review-animations`.

## GitHub Copilot CLI marketplace

```bash
copilot plugin marketplace add ShanireZ/Aptinery
copilot plugin install animate@aptinery
```

## Agent Plugins clients

Each `plugins/<skill-name>/plugin.json` is an independent Agent Plugins v1
entry. Installable names match the [catalog](docs/catalog.md).

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
