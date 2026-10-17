# 復古手撕拼貼

```yaml
id: retro-torn-collage
name: 复古手撕拼贴
input_modes: [text]
subjects: [concept, person, object, scene]
outputs: [cover, poster]
default_ratio: "3:4"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/retro-torn-collage/STYLE.md
style_anchors:
  - irregular torn paper edges
  - layered old newspaper and magazine scraps
  - visible tape strips, stickers, and paper shadows
  - photocopy grain, halftone dots, and ink misregistration
  - handwritten editorial marks and cutout headline pieces
cover_shape_adaptation:
  - main title should live on torn paper, cutout headline pieces, or rough printed scraps
  - subtitle and labels should appear as tape, notes, stamps, newspaper captions, or handwritten annotations
  - visual metaphor should be built from layered documents, photos, receipts, tags, and paper fragments
must_preserve:
  - handmade collage materiality with real paper fibers, tears, folds, shadows, and overlap
  - strong readable title hierarchy inside the collage
  - designed editorial balance rather than random asset pileup
avoid_when_applying_to_cover:
  - clean flat poster without torn edges
  - generic magazine layout with no handmade paper layering
  - smooth digital cards, flat red panels, or infographic templates
```

## Style Intent

手撕紙、舊報紙、膠帶、半調網點和強標題排版組成的復古編輯拼貼。適合需要故事感、衝突感、街頭感和社交傳播力的內容。該 style 只負責拼貼材質、復古編輯氣質和圖文敘事；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 小紅書、活動海報、文化議題、觀點內容
- 成長、自我、社會現象、城市和社群主題
- 需要雜誌感、手動感和視覺衝擊的封面

## Avoid

- 素材無序堆疊
- 乾淨向量拼圖感，缺少撕裂和印刷痕跡
- 過度裝飾導致主題不清
