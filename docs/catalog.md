---
type: catalog
title: Skills catalog
description: Lists installable skills, their uses and their individual source and license notices.
tags: [skills, catalog, licensing]
status: stable
sources:
  - id: marketplace
    resource: ../.claude-plugin/marketplace.json
    title: Canonical marketplace entries
  - id: notice
    resource: ../NOTICE
    title: Source attribution and local adaptations
---

# Skills catalog

Each entry can be installed independently. See [INSTALL.md](../INSTALL.md) for
commands and [NOTICE](../NOTICE) for pinned sources and adaptations.

| Skill | Purpose | Source and license |
| --- | --- | --- |
| [`shanirez-style`](../plugins/shanirez-style/skills/shanirez-style/SKILL.md) | C++14 coding style for competitive-programming and online-judge solutions | Original Aptinery work; GPL-3.0 |
| [`k12-lesson-plan-creation`](../plugins/k12-lesson-plan-creation/skills/k12-lesson-plan-creation/SKILL.md) | Create standards-aligned K-12 lesson plans, materials and assessments | Anthropic / Learning Commons; Apache-2.0 |
| [`k12-lesson-differentiation`](../plugins/k12-lesson-differentiation/skills/k12-lesson-differentiation/SKILL.md) | Adapt existing lessons for different proficiency levels and student needs | Anthropic / Learning Commons; Apache-2.0 |
| [`k12-lesson-prep`](../plugins/k12-lesson-prep/skills/k12-lesson-prep/SKILL.md) | Work through a lesson and produce teacher preparation notes | Anthropic / Learning Commons; Apache-2.0 |
| [`k12-check-for-understanding`](../plugins/k12-check-for-understanding/skills/k12-check-for-understanding/SKILL.md) | Create misconception-based formative math checks | Anthropic / Learning Commons; Apache-2.0 |
| [`emil-design-eng`](../plugins/emil-design-eng/skills/emil-design-eng/SKILL.md) | Polish UI, component design and animation decisions | Emil Kowalski; MIT |
| [`animate`](../plugins/animate/skills/animate/SKILL.md) | Build purposeful, interruptible web animations | Emil Kowalski; MIT |
| [`animate-expo`](../plugins/animate-expo/skills/animate-expo/SKILL.md) | Build performant React Native / Expo animations, gestures and haptics | Emil Kowalski; MIT |
| [`review-animations`](../plugins/review-animations/skills/review-animations/SKILL.md) | Review animation code against a strict craft standard | Emil Kowalski; MIT |
| [`improve-animations`](../plugins/improve-animations/skills/improve-animations/SKILL.md) | Audit codebase animations and produce an actionable improvement plan | Emil Kowalski; MIT |
| [`find-animation-opportunities`](../plugins/find-animation-opportunities/skills/find-animation-opportunities/SKILL.md) | Find interface areas that benefit from motion | Emil Kowalski; MIT |
| [`animation-performance`](../plugins/animation-performance/skills/animation-performance/SKILL.md) | Diagnose frame drops, rendering costs, main-thread contention and React animation bottlenecks | Emil Kowalski; MIT |
| [`animation-vocabulary`](../plugins/animation-vocabulary/skills/animation-vocabulary/SKILL.md) | Identify precise terms for vaguely described animation effects | Emil Kowalski; MIT |
| [`apple-design`](../plugins/apple-design/skills/apple-design/SKILL.md) | Apply Apple interface and fluid-motion principles to the web | Emil Kowalski; MIT |
| [`write-swift`](../plugins/write-swift/skills/write-swift/SKILL.md) | Write and review modern Swift, concurrency, performance and tests | Emil Kowalski; MIT |
| [`break-ui`](../plugins/break-ui/skills/break-ui/SKILL.md) | Stress-test UI with realistic worst-case data and report fixes | Emil Kowalski; MIT |
| [`mobile-native`](../plugins/mobile-native/skills/mobile-native/SKILL.md) | Improve mobile web behavior through platform CSS and metadata | Emil Kowalski; MIT |
| [`pick-ui-library`](../plugins/pick-ui-library/skills/pick-ui-library/SKILL.md) | Choose a suitable frontend library from a curated list | Emil Kowalski; MIT |
| [`prototype`](../plugins/prototype/skills/prototype/SKILL.md) | Build distinct UI variants and compare them in a visual picker | Emil Kowalski; MIT |
| [`ask-sonner`](../plugins/ask-sonner/skills/ask-sonner/SKILL.md) | Install, configure, style and troubleshoot Sonner toasts | Emil Kowalski; MIT |
| [`punk-cover`](../plugins/punk-cover/skills/punk-cover/SKILL.md) | Create platform-sized article, social and editorial covers or reusable prompts | AdrianPunk and contributors; personal noncommercial terms, redistribution restricted |
| [`punk-poster-layout`](../plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md) | Choose among 32 compositions for standalone posters, flyers, key visuals or single-canvas editorial sections when structural control is explicitly requested; ordinary websites/UI, generic heroes and platform covers do not trigger it by default | Based on AdrianPunk articles; adapted and packaged by Aptinery; GPL-3.0 |
| [`onetake`](../plugins/onetake/skills/onetake/SKILL.md) | Create continuous launch films, trailers and narrated feature demos with continuity checks | Patrick / feitangyuan; PolyForm Noncommercial 1.0.0; commercial use requires a separate license |
| [`design-taste-frontend`](../plugins/design-taste-frontend/skills/design-taste-frontend/SKILL.md) | Art direction for websites, product pages, dashboards and app screens, using researched directions, real stock images and browser checks | Leonxlnx; MIT |

## Sources and licenses

Original repository material uses [GNU GPL v3.0](../LICENSE). Third-party
material retains its own licenses and attribution:

- The four Anthropic / Learning Commons K-12 skills use Apache-2.0.
- Emil Kowalski's design and engineering skills use MIT.
- Leonxlnx's `design-taste-frontend` (tasteskill v2) uses MIT. Pictures, footage
  and fonts fetched at runtime retain their own licenses.
- OneTake uses [PolyForm Noncommercial 1.0.0](../plugins/onetake/LICENSE), with
  separate font licenses. Commercial use requires an upstream commercial license;
  the repository GPL does not apply to this imported material.
- The current `punk-cover` upstream uses Punk Skill v2.0.0 dual-track terms:
  free personal noncommercial use, with commercial use requiring prior written
  authorization and a paid fee. `LICENSE-PERSONAL.md` §5 prohibits distributing
  the work or modifications to another person. Aptinery does not label this
  material MIT or infer redistribution rights. `punk-poster-layout` is a
  separately attributed adaptation with an existing GPL-3.0 declaration; its
  notice does not establish a GPL adaptation grant for the source articles.

Exact source commits and local adaptations are recorded in [NOTICE](../NOTICE).
Applicable license copies are included at plugin and skill roots where a clear
license exists. `punk-cover` has no added or inferred license and no claim of
public redistribution permission. The three Claude-only mirrors preserve
explicit invocation semantics; they add no marketplace entries or license terms.
