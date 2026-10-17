# 法式極簡墨線海報

```yaml
id: french-minimal-ink-poster
name: 法式极简墨线海报
input_modes: [text]
subjects: [concept, essay, technology, relationship, emotion, system, choice]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 主标题, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 核心隐喻, 主体类型, 强调色, 不想出现的元素]
source: styles/french-minimal-ink-poster/STYLE.md
style_anchors:
  - warm ivory or old-paper background with 70%-85% negative space
  - sparse black hand-drawn ink lines, brush marks, broken edges, and slight bleeding
  - one precise visual metaphor derived from the topic's core judgment
  - French editorial poster typography with clear title hierarchy
  - at most one tiny restrained accent color on a word, line, node, or small detail
cover_shape_adaptation:
  - landscape ratios use asymmetric title and visual-subject placement with large open space between them
  - portrait ratios keep the main visual center small or partially cropped, leaving a calm editorial field for title and subtitle
  - title must remain one of the first visual anchors and may break into 2-3 lines when long
  - visual subject can be a person, object, abstract structure, distance, break, shadow, or digital trace depending on topic meaning
must_preserve:
  - one core metaphor, one main visual center, one readable main title
  - quiet French minimal editorial mood
  - hand-drawn ink texture, incomplete contours, and restrained paper warmth
  - sparse text: one title and at most 1-2 short subtitle lines
  - technology themes must include a subtle but clear digital trace without becoming tech UI
avoid_when_applying_to_cover:
  - using the topic noun directly as a generic icon
  - defaulting every topic to a face, hand, back view, heart, bird, cage, rope, road, moon, bulb, clock, or seedling
  - chips, robots, mechanical brains, glowing networks, dashboards, or data panels for AI and technology topics
  - photo realism, 3D rendering, commercial technology landing-page style, infographic layout, or icon stacks
  - multiple metaphors, crowded scenes, large blocks of text, watermarks, signatures, dates, URLs, or unrelated brand marks
```

## Style Intent

用法式編輯海報的剋制排版、大片留白和手繪墨線，把文章主題壓縮成一個準確的視覺隱喻。重點不是畫全主題，而是先理解核心觀點、矛盾、情緒和因果，再選擇人物、物體、結構、距離、遮擋或輕微數字痕跡作為唯一視覺中心。該 style 只負責墨線極簡海報的視覺語言；平台適配、長文提煉和通用封面結構由 `punk-cover` 負責。

## Use For

- AI、網際網路、演算法、數字世界等需要剋制科技聯想的觀點封面
- 愛情、關係、孤獨、信任、選擇、成長和告別等情緒或人生主題
- 制度、規則、效率、循環、資訊差、邊界、秩序和風險等抽象議題
- 需要安靜、高級、少文字、大留白、強隱喻的公眾號、X 頭圖和藝術海報

## Avoid

- 需要強營銷感、複雜敘事、產品功能展示或資訊圖說明的內容
- 需要鮮豔多色、照片質感、3D 質感、賽博科技光效或大面積裝飾背景的封面
- 主題必須展示多個概念、多個角色、完整場景或詳細流程時
