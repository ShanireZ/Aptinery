---
name: readme-badges
description: >-
  Standard for README badges: which badges a repository should carry, how to build them with
  Shields.io, their order, wording, colors and links, and which badges to delete. Use when writing
  or editing a README header, adding, auditing, fixing or removing badges (license, version,
  package, runtime, CI, coverage, security, docs, demo, status), or reviewing a badge block across
  a repository's language editions. Not for logo design or for README prose outside the badge block.
---

# README badges

A badge block is a compact summary of facts a reader needs before reading on:

1. **May I use it?** — license
2. **How do I get it?** — release, package or install channel
3. **Will it run for me?** — runtime, language, framework or platform
4. **Is it healthy?** — CI, coverage, security
5. **Where is it?** — docs, live site or demo
6. **Is it alive?** — lifecycle status, only when it is not plain active development

A badge that answers none of these is decoration. Delete it.

---

## 1. Placement

```md
# ProjectName

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
[![CI](https://img.shields.io/github/actions/workflow/status/OWNER/REPO/ci.yml?branch=main&style=flat-square&label=ci)](https://github.com/OWNER/REPO/actions/workflows/ci.yml)
![Node.js 22+](https://img.shields.io/badge/Node.js-22%2B-5FA04E.svg?style=flat-square&logo=nodedotjs&logoColor=white)

One-sentence summary.
```

- The block sits directly under the H1, separated by one blank line on each side. If the README
  has YAML frontmatter, the frontmatter stays first and the badges still follow the H1.
- **One badge per line**, so diffs and reviews stay readable. No HTML `<p align="center">` wrappers,
  no tables of badges, no badges after the summary or at the end of the file.
- A language switcher line (`[English](README.md) | [日本語](README.ja.md)`) goes after the badge
  block and before the summary.
- **Every language edition carries the same badge block, byte for byte.** Badge text stays in
  English; only the prose around it is translated.

---

## 2. What to include — six slots, in this order

| Slot | Badge | Source of truth | Include when |
|---|---|---|---|
| 1 License | static `license` badge with the SPDX id | license metadata, then the `LICENSE` file | a license or distribution file exists — always first |
| 2 Distribution | version from the registry or releases; install channel | npm, PyPI, crates.io, Greasy Fork, GitHub Releases | the project is published or released |
| 3 Runtime | language, runtime, framework or platform with the version the project enforces | `engines`, `requires-python`, `rust-version`, compiler flags, lockfile | it changes whether the reader can run or build it — at most 3 |
| 4 Quality | CI status, coverage, security score | the live service | the repo is public and the workflow or report really runs |
| 5 Links | docs, live site, demo | the URL itself | a stable public URL exists |
| 6 Status | `experimental`, `beta`, `maintenance`, `deprecated`, `archived` | project decision | the project is *not* in plain active development |

**Budget: 6 badges by default, 8 at most.** A private application typically needs only license,
two runtime badges and maybe a status. When over budget, drop from slot 3 first, never slot 1.

Prefer **dynamic badges** wherever a service publishes the fact (versions, CI, coverage, scores,
supported runtimes of a published package). Use a **static badge** only for facts that have no
service — license, runtime minimums of an unpublished app, platform, docs and demo links, status.
The URL catalog is in [`references/catalog.md`](references/catalog.md).

---

## 3. Delete these

- **Social and vanity:** stars, forks, watchers, followers, profile views, visitor counters,
  "made with ❤", "PRs welcome", "awesome", "open source", "maintained: yes", "contributions welcome".
- **Facts the hosting page already shows:** last commit, commit activity, repo or code size, top
  language, language count, contributors, open issues or pull requests, release date.
- **`type:` badges that restate the summary sentence** ("type: learning platform", "type: web app").
  The summary line says it better. Keep a type-like badge only when it is the install channel
  (`userscript: Tampermonkey`, `Agent Skill`).
- **Hand-counted progress:** "lessons 37/37", "milestone M1 closed", "stage 1–6 complete",
  "archived 26 courses". They drift silently. Use the status slot, or an `endpoint` badge fed by a
  file that CI or a script regenerates.
- **Toolchain minutiae:** package-manager, linter, formatter, bundler or test-runner versions. They
  belong in the install or contributing section.
- **Internal documents dressed as badges** ("method: SOP.md"). Use a normal link in the prose.
- **Dynamic badges on private repositories.** Shields.io cannot read them, so they render
  "repo not found" or "invalid" for every reader. Use a static badge or none.
- **Duplicates and conflicts:** two license badges, `Node` next to `Node.js`, a static version
  next to a dynamic one.
- **Anything you cannot verify right now.** A missing badge is better than a wrong one.

---

## 4. Building the URL

**Static:**

```txt
https://img.shields.io/badge/<label>-<message>-<color>.svg?style=flat-square
https://img.shields.io/badge/<label>-<message>-<color>.svg?style=flat-square&logo=<slug>&logoColor=white
```

Escape the label and message in the path:

| Character | Write |
|---|---|
| `-` | `--` |
| `_` | `__` |
| space | `%20` |
| `/` `+` `#` `?` `%` | `%2F` `%2B` `%23` `%3F` `%25` |

So `GPL-3.0-or-later` becomes `GPL--3.0--or--later`, and `22+` becomes `22%2B`.

**Dynamic:** use the documented route and append `style=flat-square` to its query string, e.g.
`https://img.shields.io/npm/v/PACKAGE?style=flat-square`. Use `label=` only to shorten a long
default label (`label=ci`). Do not override the color of a dynamic badge.

**Style:** `flat-square` on every badge, static and dynamic. Mixed styles look broken.

**Logos:** only on runtime and platform badges, using the [Simple Icons](https://simpleicons.org/)
slug (`nodedotjs`, `cplusplus`, `nextdotjs`). Use `logoColor=white`, or `logoColor=black` when the
brand color is light (React `61DAFB`, JavaScript `F7DF1E`). No logos on license, status or link
badges.

---

## 5. Wording

- **Labels:** generic labels are lowercase — `license`, `distribution`, `version`, `ci`,
  `coverage`, `docs`, `site`, `demo`, `status`, `platform`. Technology names keep their official casing — `Node.js`,
  `TypeScript`, `C++`, `PostgreSQL`. Labels stay under about 12 characters.
- **Messages:** under about 20 characters. A runtime badge shows the major version or the
  enforced minimum (`19`, `22+`, `3.11+`, `14` for C++14) — never a full patch version unless the
  project really depends on it. No marketing words (`fast`, `best`, `modern`).
- **Alt text** states the badge on its own: `![Node.js 22+](...)`,
  `[![License: MIT](...)](LICENSE)`, `[![CI](...)](...)`. Never empty, never shared by two badges.

---

## 6. Colors

| Meaning | Color |
|---|---|
| License, version, docs, site, demo, platform and other neutral facts | `blue` |
| Restricted distribution, experimental, beta, maintenance | `yellow` or `orange` |
| Deprecated, archived | `lightgrey` |
| Runtime and framework badges | the brand hex from Simple Icons |

- **Green and red belong to live status.** A static badge is never `success`/`brightgreen` or
  `critical`/`red`, because it cannot know whether anything is passing or deployed. Dynamic CI,
  coverage and score badges compute their own colors.
- Take brand hex values from Simple Icons when you write the badge; they change (Vite moved from
  `646CFF` to `9135FF`). The table in the catalog was checked on 2026-11-08.
- No random palettes, no gradients, nothing louder than the title.

---

## 7. License badge

1. Take the identifier from machine-readable metadata first: `package.json` `license`,
   `pyproject.toml`, `Cargo.toml`, a userscript `@license` line, SPDX headers.
2. If there is only a `LICENSE` file, read it. When GPL text gives no `only` / `or-later`
   choice, write the generic `GPL-3.0`; never mix `GPL-3.0-only` and `GPL-3.0-or-later`.
3. A proprietary project with a `LICENSE` file stating it uses `license-Proprietary-blue` linked to
   that file. Non-SPDX distribution terms link to the README section that states them.
4. No license file and no stated terms → no license badge. Never infer MIT, proprietary,
   restricted or third-party terms from a template.
5. A project that deliberately has no license (for example, one built on third-party IP) may
   show its stated terms with a `distribution` label in `orange` linked to that README section —
   never a `license` label, which would read as a grant.

```md
[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![License: Proprietary](https://img.shields.io/badge/license-Proprietary-blue.svg?style=flat-square)](LICENSE)
```

---

## 8. Links

Badges with a verifiable target are links; runtime and platform badges are not.

| Badge | Target |
|---|---|
| License | `LICENSE` |
| Version / package | the release list, package page or the versioned file |
| CI | the workflow's runs page |
| Coverage | the coverage report |
| Security score | the scorecard viewer |
| Docs / site / demo | the docs home or live URL |
| Status | the README section that explains it, if any |

---

## 9. Examples

**Published library:**

```md
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![npm](https://img.shields.io/npm/v/PACKAGE?style=flat-square)](https://www.npmjs.com/package/PACKAGE)
![Node.js](https://img.shields.io/node/v/PACKAGE?style=flat-square&logo=nodedotjs&logoColor=white)
[![CI](https://img.shields.io/github/actions/workflow/status/OWNER/REPO/ci.yml?branch=main&style=flat-square&label=ci)](https://github.com/OWNER/REPO/actions/workflows/ci.yml)
[![Coverage](https://img.shields.io/codecov/c/github/OWNER/REPO?style=flat-square)](https://app.codecov.io/gh/OWNER/REPO)
```

**Private application:**

```md
[![License: Proprietary](https://img.shields.io/badge/license-Proprietary-blue.svg?style=flat-square)](LICENSE)
![Node.js 22+](https://img.shields.io/badge/Node.js-22%2B-5FA04E.svg?style=flat-square&logo=nodedotjs&logoColor=white)
![Next.js 16](https://img.shields.io/badge/Next.js-16-000000.svg?style=flat-square&logo=nextdotjs&logoColor=white)
![Status: beta](https://img.shields.io/badge/status-beta-yellow.svg?style=flat-square)
```

**Userscript without a registry listing:**

```md
[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![Userscript: Tampermonkey](https://img.shields.io/badge/userscript-Tampermonkey-00485B.svg?style=flat-square&logo=tampermonkey&logoColor=white)
[![Version: 2.14.6](https://img.shields.io/badge/version-2.14.6-blue.svg?style=flat-square)](PROJECT.user.js)
```

**Code archive:**

```md
[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![C++14](https://img.shields.io/badge/C%2B%2B-14-00599C.svg?style=flat-square&logo=cplusplus&logoColor=white)
```

---

## 10. Maintenance

- A static badge changes in the same commit as the fact it states (version bump, runtime
  minimum, license change, status change).
- When you touch a README with an older badge block, bring the whole block to this standard:
  remove section 3 badges, reorder to section 2, fix style, escaping, colors and alt text, and keep
  every language edition identical.
- Report every badge you removed and why.

## 11. Review checklist

- [ ] Block directly under the H1, one badge per line, same block in every language edition.
- [ ] License first, SPDX id taken from metadata, linked to `LICENSE`; no `only`/`or-later` mix-up.
- [ ] Slot order from section 2; at most 6 badges (8 with reason).
- [ ] Nothing from section 3.
- [ ] Every badge `style=flat-square`; static paths escaped; dynamic routes from the catalog.
- [ ] Dynamic badges only for public sources; each one renders a value, not "not found" or "invalid".
- [ ] No green or red on a static badge; brand colors match Simple Icons.
- [ ] Alt text readable on its own; every link opens.
