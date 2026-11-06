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

## Plugins

Most skills install as a plugin with the same name. Skills from one source that
are used together are grouped into one plugin:

| Plugin | Skills |
| --- | --- |
| `k12-teacher-skills` | The four K-12 skills below |
| `emil-skills` | The 17 Emil Kowalski skills below |
| `brave-search` | The 12 Brave Search API skills below |

Marketplace commands take the plugin name; the skills CLI takes the skill name
and installs any single skill from a group.

## Skills

| Skill | Purpose | Source and license |
| --- | --- | --- |
| [`shanirez-style`](../plugins/shanirez-style/skills/shanirez-style/SKILL.md) | C++14 coding style for competitive-programming and online-judge solutions | Original Aptinery work; GPL-3.0 |
| [`k12-lesson-plan-creation`](../plugins/k12-teacher-skills/skills/k12-lesson-plan-creation/SKILL.md) | Create standards-aligned K-12 lesson plans, materials and assessments | Anthropic / Learning Commons; Apache-2.0 |
| [`k12-lesson-differentiation`](../plugins/k12-teacher-skills/skills/k12-lesson-differentiation/SKILL.md) | Adapt existing lessons for different proficiency levels and student needs | Anthropic / Learning Commons; Apache-2.0 |
| [`k12-lesson-prep`](../plugins/k12-teacher-skills/skills/k12-lesson-prep/SKILL.md) | Work through a lesson and produce teacher preparation notes | Anthropic / Learning Commons; Apache-2.0 |
| [`k12-check-for-understanding`](../plugins/k12-teacher-skills/skills/k12-check-for-understanding/SKILL.md) | Create misconception-based formative math checks | Anthropic / Learning Commons; Apache-2.0 |
| [`emil-design-eng`](../plugins/emil-skills/skills/emil-design-eng/SKILL.md) | Polish UI, component design and animation decisions | Emil Kowalski; MIT |
| [`animate`](../plugins/emil-skills/skills/animate/SKILL.md) | Build purposeful, interruptible web animations | Emil Kowalski; MIT |
| [`animate-expo`](../plugins/emil-skills/skills/animate-expo/SKILL.md) | Build performant React Native / Expo animations, gestures and haptics | Emil Kowalski; MIT |
| [`review-animations`](../plugins/emil-skills/skills/review-animations/SKILL.md) | Review animation code against a strict craft standard | Emil Kowalski; MIT |
| [`improve-animations`](../plugins/emil-skills/skills/improve-animations/SKILL.md) | Audit codebase animations and produce an actionable improvement plan | Emil Kowalski; MIT |
| [`find-animation-opportunities`](../plugins/emil-skills/skills/find-animation-opportunities/SKILL.md) | Find interface areas that benefit from motion | Emil Kowalski; MIT |
| [`animation-performance`](../plugins/emil-skills/skills/animation-performance/SKILL.md) | Diagnose frame drops, rendering costs, main-thread contention and React animation bottlenecks | Emil Kowalski; MIT |
| [`remove-animations`](../plugins/emil-skills/skills/remove-animations/SKILL.md) | Find animations an interface does not need and remove them, then clean up what they leave behind | Emil Kowalski; MIT |
| [`animation-vocabulary`](../plugins/emil-skills/skills/animation-vocabulary/SKILL.md) | Identify precise terms for vaguely described animation effects | Emil Kowalski; MIT |
| [`apple-design`](../plugins/emil-skills/skills/apple-design/SKILL.md) | Apply Apple interface and fluid-motion principles to the web | Emil Kowalski; MIT |
| [`write-swift`](../plugins/emil-skills/skills/write-swift/SKILL.md) | Write and review modern Swift, concurrency, performance and tests | Emil Kowalski; MIT |
| [`break-ui`](../plugins/emil-skills/skills/break-ui/SKILL.md) | Stress-test UI with realistic worst-case data and report fixes | Emil Kowalski; MIT |
| [`mobile-native`](../plugins/emil-skills/skills/mobile-native/SKILL.md) | Improve mobile web behavior through platform CSS and metadata | Emil Kowalski; MIT |
| [`pick-ui-library`](../plugins/emil-skills/skills/pick-ui-library/SKILL.md) | Choose a suitable frontend library from a curated list | Emil Kowalski; MIT |
| [`prototype`](../plugins/emil-skills/skills/prototype/SKILL.md) | Build distinct UI variants and compare them in a visual picker | Emil Kowalski; MIT |
| [`ask-sonner`](../plugins/emil-skills/skills/ask-sonner/SKILL.md) | Install, configure, style and troubleshoot Sonner toasts | Emil Kowalski; MIT |
| [`choreograph`](../plugins/emil-skills/skills/choreograph/SKILL.md) | Coordinate several animating elements into one intentional motion: order, overlap and what stays still | Emil Kowalski; MIT |
| [`punk-cover`](../plugins/punk-cover/skills/punk-cover/SKILL.md) | Create platform-sized article, social and editorial covers or reusable prompts | AdrianPunk and contributors; personal noncommercial terms, redistribution restricted |
| [`punk-poster-layout`](../plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md) | Choose among 32 compositions for standalone posters, flyers, key visuals or single-canvas editorial sections when structural control is explicitly requested; ordinary websites/UI, generic heroes and platform covers do not trigger it by default | Based on AdrianPunk articles; adapted and packaged by Aptinery; GPL-3.0 |
| [`onetake`](../plugins/onetake/skills/onetake/SKILL.md) | Create continuous launch films, trailers and narrated feature demos with continuity checks | Patrick / feitangyuan; PolyForm Noncommercial 1.0.0; commercial use requires a separate license |
| [`design-taste-frontend`](../plugins/design-taste-frontend/skills/design-taste-frontend/SKILL.md) | Build professional company websites with one page system, real product UI, vetted photographs, brand icons and real-browser consistency checks | Leonxlnx; MIT |
| [`landing-page-design`](../plugins/landing-page-design/skills/landing-page-design/SKILL.md) | Build high-converting landing pages with intake questions, page structure, conversion copy, SEO and a strict visual system | Elaya; MIT |
| [`figma-designer`](../plugins/figma-designer/skills/figma-designer/SKILL.md) | Design screens, components and design systems in Figma through the Figma MCP with real tokens and a fixed visual system | Elaya; MIT; needs the Figma MCP and the official Figma skills |
| [`answers`](../plugins/brave-search/skills/answers/SKILL.md) | Get AI-grounded answers with citations, from a single search to deep research | Brave Software; MIT; needs a Brave Search API key |
| [`bx`](../plugins/brave-search/skills/bx/SKILL.md) | Search the web with the Brave Search CLI: grounded context, answers, news, images, videos and places | Brave Software; MIT; needs a Brave Search API key |
| [`images-search`](../plugins/brave-search/skills/images-search/SKILL.md) | Search images with SafeSearch and up to 200 results | Brave Software; MIT; needs a Brave Search API key |
| [`llm-context`](../plugins/brave-search/skills/llm-context/SKILL.md) | Fetch pre-extracted web content tuned for RAG and LLM grounding | Brave Software; MIT; needs a Brave Search API key |
| [`local-descriptions`](../plugins/brave-search/skills/local-descriptions/SKILL.md) | Get AI-generated place descriptions from POI IDs | Brave Software; MIT; needs a Brave Search API key |
| [`local-place-search`](../plugins/brave-search/skills/local-place-search/SKILL.md) | Find businesses, addresses, cities and points of interest | Brave Software; MIT; needs a Brave Search API key |
| [`local-pois`](../plugins/brave-search/skills/local-pois/SKILL.md) | Get business details such as ratings, hours and contact data from POI IDs | Brave Software; MIT; needs a Brave Search API key |
| [`news-search`](../plugins/brave-search/skills/news-search/SKILL.md) | Search news articles with freshness and date filters | Brave Software; MIT; needs a Brave Search API key |
| [`spellcheck`](../plugins/brave-search/skills/spellcheck/SKILL.md) | Correct misspelled search queries | Brave Software; MIT; needs a Brave Search API key |
| [`suggest`](../plugins/brave-search/skills/suggest/SKILL.md) | Autocomplete queries with fast, typo-resilient suggestions | Brave Software; MIT; needs a Brave Search API key |
| [`videos-search`](../plugins/brave-search/skills/videos-search/SKILL.md) | Search videos with duration, view count and creator data | Brave Software; MIT; needs a Brave Search API key |
| [`web-search`](../plugins/brave-search/skills/web-search/SKILL.md) | Search the web with ranked results, freshness filters, Goggles and pagination | Brave Software; MIT; needs a Brave Search API key |

## Sources and licenses

Original repository material uses [GNU GPL v3.0](../LICENSE). Third-party
material retains its own licenses and attribution:

- The four Anthropic / Learning Commons K-12 skills use Apache-2.0.
- Emil Kowalski's design and engineering skills use MIT.
- Brave Software's Brave Search API skills use MIT. They call the Brave Search API
  and need your own API key; the `bx` skill also needs the `bx` command-line tool.
- Leonxlnx's `design-taste-frontend` (tasteskill 2.5.0) uses MIT. The
  photographs it bundles (Unsplash License, CC0-1.0) and its brand, interface
  and file-type icons (CC0-1.0, MIT) keep the licenses recorded in its own
  credits JSON files; brand marks remain trademarks. Pictures and fonts fetched
  at runtime retain their own licenses.
- Elaya's `landing-page-design` uses MIT. `figma-designer` also uses MIT; it
  designs through the Figma MCP and the official Figma skills, which this
  package does not include.
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
public redistribution permission. The Claude-only mirror under
`.claude-plugins/emil-skills/` preserves explicit invocation semantics for three
Emil skills; it adds no separate marketplace entry or license terms.
