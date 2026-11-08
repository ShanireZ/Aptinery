# Badge URL catalog

Routes checked against the Shields.io service sources on 2026-11-08. Replace `OWNER`, `REPO`,
`PACKAGE` and the other placeholders; keep `style=flat-square`. A route that renders "not found",
"invalid" or "inaccessible" means the source is private, misspelled or unpublished — fix the source
or drop the badge.

## Distribution

| Fact | Badge URL | Link target |
|---|---|---|
| GitHub release | `https://img.shields.io/github/v/release/OWNER/REPO?sort=semver&display_name=tag&style=flat-square` | `https://github.com/OWNER/REPO/releases` |
| GitHub tag (no releases) | `https://img.shields.io/github/v/tag/OWNER/REPO?sort=semver&style=flat-square` | `https://github.com/OWNER/REPO/tags` |
| npm | `https://img.shields.io/npm/v/PACKAGE?style=flat-square` | `https://www.npmjs.com/package/PACKAGE` |
| PyPI | `https://img.shields.io/pypi/v/PACKAGE?style=flat-square` | `https://pypi.org/project/PACKAGE/` |
| crates.io | `https://img.shields.io/crates/v/CRATE?style=flat-square` | `https://crates.io/crates/CRATE` |
| Docker Hub | `https://img.shields.io/docker/v/USER/IMAGE?sort=semver&style=flat-square` | `https://hub.docker.com/r/USER/IMAGE` |
| Greasy Fork | `https://img.shields.io/greasyfork/v/SCRIPT_ID?style=flat-square` | `https://greasyfork.org/scripts/SCRIPT_ID` |
| Unpublished version | `https://img.shields.io/badge/version-1.2.3-blue.svg?style=flat-square` | the file that holds the version |

Use `include_prereleases` on the GitHub routes only when prereleases are what users install.

## Runtime support of a published package

| Fact | Badge URL |
|---|---|
| Node.js range from `engines` | `https://img.shields.io/node/v/PACKAGE?style=flat-square&logo=nodedotjs&logoColor=white` |
| Python versions from classifiers | `https://img.shields.io/pypi/pyversions/PACKAGE?style=flat-square&logo=python&logoColor=white` |

For an unpublished project, write the enforced minimum as a static badge (section 4 of the skill).

## Quality (public repositories only)

| Fact | Badge URL | Link target |
|---|---|---|
| GitHub Actions workflow | `https://img.shields.io/github/actions/workflow/status/OWNER/REPO/WORKFLOW.yml?branch=main&style=flat-square&label=ci` | `https://github.com/OWNER/REPO/actions/workflows/WORKFLOW.yml` |
| Codecov | `https://img.shields.io/codecov/c/github/OWNER/REPO?style=flat-square` | `https://app.codecov.io/gh/OWNER/REPO` |
| OpenSSF Scorecard | `https://img.shields.io/ossf-scorecard/github.com/OWNER/REPO?style=flat-square&label=openssf%20scorecard` | `https://scorecard.dev/viewer/?uri=github.com/OWNER/REPO` |

The old `github/workflow/status/...` route is retired; use `github/actions/workflow/status/...`
with the workflow **file name**. Pin `branch=` so pull-request runs do not color the badge.

## Docs and links

| Fact | Badge URL | Link target |
|---|---|---|
| docs.rs build | `https://img.shields.io/docsrs/CRATE?style=flat-square` | `https://docs.rs/CRATE` |
| Docs site | `https://img.shields.io/badge/docs-site-blue.svg?style=flat-square` | docs home |
| Live demo | `https://img.shields.io/badge/demo-HOST-blue.svg?style=flat-square` | live URL |

## Status

| Status | Badge URL |
|---|---|
| experimental | `https://img.shields.io/badge/status-experimental-orange.svg?style=flat-square` |
| beta | `https://img.shields.io/badge/status-beta-yellow.svg?style=flat-square` |
| maintenance | `https://img.shields.io/badge/status-maintenance-yellow.svg?style=flat-square` |
| deprecated | `https://img.shields.io/badge/status-deprecated-lightgrey.svg?style=flat-square` |
| archived | `https://img.shields.io/badge/status-archived-lightgrey.svg?style=flat-square` |

## Generated facts

When a project-specific number is worth a badge, have CI or a script write a Shields endpoint JSON
file (`{"schemaVersion": 1, "label": "lessons", "message": "37", "color": "blue"}`) to a public
URL and use `https://img.shields.io/endpoint?url=URL_ENCODED_JSON_URL&style=flat-square`. Never
hand-edit the number.

## Brand colors and logo slugs

From Simple Icons, checked 2026-11-08. Re-check when writing a new badge.

| Technology | Label | Hex | Slug | `logoColor` |
|---|---|---|---|---|
| Node.js | `Node.js` | `5FA04E` | `nodedotjs` | white |
| TypeScript | `TypeScript` | `3178C6` | `typescript` | white |
| JavaScript | `JavaScript` | `F7DF1E` | `javascript` | black |
| React | `React` | `61DAFB` | `react` | black |
| Next.js | `Next.js` | `000000` | `nextdotjs` | white |
| Vite | `Vite` | `9135FF` | `vite` | white |
| Vue.js | `Vue.js` | `4FC08D` | `vuedotjs` | white |
| Express | `Express` | `0A0A0A` | `express` | white |
| Python | `Python` | `3776AB` | `python` | white |
| Go | `Go` | `00ADD8` | `go` | white |
| Rust | `Rust` | `000000` | `rust` | white |
| C++ | `C++` | `00599C` | `cplusplus` | white |
| PostgreSQL | `PostgreSQL` | `4169E1` | `postgresql` | white |
| SQLite | `SQLite` | `003B57` | `sqlite` | white |
| Docker | `Docker` | `2496ED` | `docker` | white |
| Godot Engine | `Godot` | `478CBF` | `godotengine` | white |
| Cloudflare | `Cloudflare` | `F38020` | `cloudflare` | white |
| Tampermonkey | `userscript` | `00485B` | `tampermonkey` | white |
