# 極簡視覺隱喻風

```yaml
id: minimal-visual-metaphor
name: 极简视觉隐喻风
input_modes: [text]
subjects: [concept, business, technology, system, object, person, scene]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [核心动作, 抽象实体, 人物动作, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/minimal-visual-metaphor/STYLE.md
style_anchors:
  - premium business and technology editorial cover with modern Swiss restraint
  - one readable but indirect abstract physical apparatus expressing a single action or change
  - warm white paper-textured background with generous negative space
  - graphite black, charcoal gray, and one low-saturation translucent ink-green accent
  - matte graphite metal, precise black modules, frosted green glass, and soft natural shadows
  - exact readable title in a clean Chinese sans-serif with at most one key word or number highlighted in ink green
cover_shape_adaptation:
  - for landscape ratios, place the exact title on the left in roughly 50-55 percent of the canvas and the metaphor apparatus on the right in roughly 40-45 percent
  - for portrait ratios, place the exact title above and the metaphor apparatus below while retaining one visual center and ample negative space
  - translate the topic into one core action such as connecting, converging, aligning, advancing, dismantling, penetrating, folding, balancing, transforming, growing, or crossing
  - use only a few precise objects; an optional small realistic person may perform the decisive action and provide scale
must_preserve:
  - one single visual story with a clear action, relationship, and result
  - quiet gallery-like composition, precise spacing, and substantial warm-white negative space
  - restrained palette limited to warm white, graphite black, charcoal gray, and low-saturation translucent ink green
  - exact, complete, clearly readable title with no other readable text
  - material realism, soft natural shadows, and premium editorial sculpture quality
avoid_when_applying_to_cover:
  - literal icons, explainer diagrams, instruction-manual illustration, dashboards, or multiple competing concepts
  - cyberpunk, neon, blue-purple gradients, robots, AI brains, chips, sci-fi cities, or screen-filled UI
  - cartoons, home-interior styling, cheap 3D, exaggerated lighting, logos, watermarks, subtitles, borders, or decorative microtext
  - unnecessary people, theatrical poses, visual clutter, or decorative lines without semantic purpose
```

## Style Intent

把商業、科技、組織和系統主題轉譯為一個“可讀但不直白”的抽象實體裝置。通過單一核心動作、少量精確物體和可選的小比例人物，表達連接、匯聚、推進、轉化或跨越等關係變化。畫面像一件置於畫廊中的編輯雕塑，剋制、高級、清楚，而不是圖標化說明或科技概念堆砌。平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- AI、商業科技、產品、組織、工作流、系統變化和趨勢分析
- 需要把抽象關係或變化做成實體隱喻的公眾號、X、文章和報告封面
- 需要高級、極簡、易讀、留白充分的編輯視覺

## Avoid

- 主題只能相依複雜資料、介面截圖或多步驟流程才能說明
- 需要熱鬧、卡通、霓虹、強娛樂化或多人物敘事的內容
- 無法收束為一個核心動作和一組清楚物體關係的主題
