# 復古油墨點陣隱喻

```yaml
id: retro-ink-dot-matrix-metaphor
name: 复古油墨点阵隐喻
input_modes: [text]
subjects: [concept, technology, essay, object, system]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 主标题, 画幅比例, 语言, 用途]
optional_fields: [底部短词, 副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/retro-ink-dot-matrix-metaphor/STYLE.md
style_anchors:
  - fixed warm gray beige background #DED9CF
  - black retro ink letterpress title and restrained dark gray footer words
  - one small minimal dot-matrix metaphor illustration
  - fixed editorial layout by aspect ratio with generous negative space
  - old printer, lead type, archive title, and vintage technical magazine restraint
cover_shape_adaptation:
  - landscape ratios use a fixed left-text and right-illustration composition
  - square and portrait ratios use a fixed top-text, middle-lower illustration, bottom-footer composition
  - title remains at fixed size for each ratio and never scales up to fill space
  - illustration stays small and secondary, occupying roughly 22-26% width in landscape or 25-32% height in square and portrait
must_preserve:
  - background color #DED9CF without hue, brightness, gradient, paper stain, or texture drift
  - title and illustration color #111111, footer color #343434, no fourth color
  - same retro ink mechanical letterpress type family for all text
  - one readable main title, one optional footer word group, one simple metaphor illustration
  - fixed layout hierarchy, fixed title size, and strong whitespace
avoid_when_applying_to_cover:
  - extra explanatory text, labels, subtitles, watermarks, logos, QR codes, numbering, or prompt text
  - high-saturation color, gradient, glow, 3D, photography, complex background, or heavy aging stains
  - modern geometric sans, pixel font, Songti, calligraphy, handwriting, or decorative distressed type
  - oversized illustration, crowded scene, multiple metaphors, or decorative filler objects
```

## Style Intent

復古油墨機械列印與極簡點陣隱喻結合的封面海報。核心不是炫技插畫，而是穩定的舊式列印版式、固定色彩、固定字體和一個小而明確的黑色點陣主體。該 style 只負責復古油墨點陣視覺、固定構圖和資訊剋制；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- AI、科技、系統、認知、研究、未來感和抽象概念文章
- 需要安靜、理性、復古、剋制氣質的公眾號、X 頭圖和編輯海報
- 適合把複雜主題壓縮成一個簡單、直接、可識別視覺隱喻的封面

## Avoid

- 需要強營銷感、鮮豔配色、攝影質感或複雜敘事場景的內容
- 標題必須大幅變形、滿版衝擊或強裝飾化的封面
- 需要展示多人物、多步驟流程、產品介面細節或品牌 Logo 的封面
