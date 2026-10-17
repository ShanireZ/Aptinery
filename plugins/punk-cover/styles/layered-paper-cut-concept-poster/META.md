# 立體紙雕概念海報

```yaml
id: layered-paper-cut-concept-poster
name: 立体纸雕概念海报
input_modes: [text]
subjects: [concept, object, scene, typography]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题或主标题]
optional_fields: [副标题, 画幅比例, 输出尺寸, 输出模式, 用途, 语言, 文字模式, 情感倾向, 色彩倾向, 补充语境, 必须出现, 禁止出现]
source: styles/layered-paper-cut-concept-poster/STYLE.md
style_anchors:
  - physically believable layered cut paper with visible thickness, apertures, fibers, folds, curled edges, and soft contact shadows
  - one precise conceptual metaphor expressed through a single spatial relationship or transformation
  - generous negative space, one focal composition, and restrained editorial hierarchy
  - title integrated into the paper construction as a cutout, layer, window, path, enclosure, or interleaved structure
  - limited coherent palette and one unified studio light shared by image, typography, and paper layers
cover_shape_adaptation:
  - derive one high-impact core word for the first visual when the source title is long, while preserving the complete title as secondary information
  - recompose subject scale, title placement, whitespace, reading direction, paper-layer direction, and information density for every target ratio
  - for a requested multi-size suite, compile and generate one independently composed image per ratio while preserving the same metaphor, material, palette, and identity
  - reduce information in ultra-wide or ultra-tall formats and emphasize one simple visual relationship
must_preserve:
  - real paper-cut construction rather than a flat illustration with a paper texture filter
  - exactly one main visual metaphor and one clear focal point
  - shared lighting, perspective, materiality, and depth across text, image, and paper layers
  - accurate user text, premium negative space, controlled color, and natural paper shadows
avoid_when_applying_to_cover:
  - flat illustration, childish craft, simple cut-paper border, decorative clutter, multiple competing subjects, or dense information
  - plastic, foam, metal, neon technology, cheap CGI, hard black shadows, or overcomplicated backgrounds
  - fabricated editorial text, misspellings, gibberish, detached typography, or generic PPT and e-commerce layouts
  - crop, stretch, padding, mockup, contact sheet, grid, or one-size-fits-all adaptation for multiple ratios
```

## Style Intent

把主題中最重要的關係、矛盾或變化提煉為一個真實立體紙雕隱喻，以精確紙層、剋制留白、柔和光影和圖文一體的編輯排版完成高級概念海報。該 style 負責紙張材質、隱喻轉譯、空間關係、比例重構和視覺氣質；平台確認、文章摘要、檔案保存和生成工具呼叫由 `punk-cover` 負責。

## Use For

- 概念、方法論、知識、成長、連接、阻力、變化和關係主題
- 需要溫暖、安靜、剋制、理性、治癒、神秘或高級氣質的封面
- 小紅書、微信公眾號、X、展覽海報、品牌視覺和多尺寸傳播套圖
- 能被提煉成一個清楚空間動作或視覺關係的長文章與短標題

## Avoid

- 必須同時展示多個同權重主體、複雜資料或大量正文的資訊圖任務
- 相依寫實人物相似度、金屬機械結構或高飽和霓虹才能成立的主題
- 無法允許任何標題提煉、留白或視覺隱喻的純資訊排版任務
