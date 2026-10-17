# 紙面擊凸壓凹封面

```yaml
id: paper-emboss-deboss-cover
name: 纸面击凸压凹封面
input_modes: [text]
subjects: [concept, typography, object, scene]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题或主标题]
optional_fields: [副标题, 画幅比例, 输出尺寸, 输出模式, 用途, 语言, 文字模式, 情感倾向, 色彩倾向, 补充语境, 必须出现, 禁止出现]
source: styles/paper-emboss-deboss-cover/STYLE.md
style_anchors:
  - authentic cotton or art-paper surface with visible fiber, tooth, and studio side-lighting
  - letterpress-like emboss and deboss as the only physical relief, not cut-paper layers or plastic 3D type
  - one restrained visual metaphor expressed as a single paper-relief graphic
  - editorial typography that participates in composition through split lines, offset, edge placement, mixed orientation, or embedding into the graphic
  - 1-2 main colors plus optional micro accent, with large negative space as a compositional actor
cover_shape_adaptation:
  - derive one high-impact visual title when the source title is long, while preserving the complete title as secondary microtype
  - randomly recombine typeface family, type hierarchy, title placement, composition logic, metaphor, palette, and emboss/deboss assignment for each new cover
  - recompose title scale, graphic placement, whitespace, reading path, and relief direction for every target ratio
  - for a requested multi-size suite, keep metaphor, paper material, and palette identity consistent, but invent a new editorial layout for each ratio instead of cropping
must_preserve:
  - real paper relief with crisp impression edges, natural paper thickness, and soft side-light shadows
  - exactly one main graphic metaphor and a clear three-level type hierarchy
  - text-image inseparability: title, graphic, and whitespace must form one editorial sentence
  - quiet independent-magazine / art-book-cover temperament rather than a generic poster template
avoid_when_applying_to_cover:
  - plastic 3D modeling, metal engraving, foil stamping as the main look, neon, glossy CGI, or exaggerated extrusion
  - layered paper-cut diorama, collage, illustration clutter, or multiple competing subjects
  - always-left or always-centered title templates, PPT covers, e-commerce ads, and fabricated editorial filler
  - misspellings, unreadable titles, dense gradients, or more than two dominant colors plus one accent
```

## Style Intent

把主題提煉成一個剋制的紙面隱喻，再用真實紙張質感、擊凸與壓凹工藝、靈活編輯排版和大量留白做成藝術畫冊封面或獨立雜誌封面。該 style 負責紙張工藝、文字構圖、隱喻圖形、隨機版式實驗和視覺氣質；平台確認、文章摘要、檔案保存和生成工具呼叫由 `punk-cover` 負責。

## Use For

- 設計、藝術、方法論、品牌、寫作、哲學、關係和抽象概念主題
- 需要安靜、現代、剋制、聰明、高級氣質的封面或海報
- 小紅書、微信公眾號、X、書封、展覽海報和設計畫冊視覺
- 標題本身可以成為構圖，而不是貼在畫面上的說明文字

## Avoid

- 必須同時展示多個同權重主體、複雜資料或大量正文的資訊圖任務
- 相依寫實人物、產品攝影、金屬機械或高飽和霓虹才能成立的主題
- 需要兒童插畫、剪紙層疊、拼貼、賽博朋克或誇張立體字的任務
