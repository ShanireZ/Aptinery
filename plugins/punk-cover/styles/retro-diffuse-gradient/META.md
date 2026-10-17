# 復古彌散漸變

```yaml
id: retro-diffuse-gradient
name: 复古弥散渐变
input_modes: [text]
subjects: [concept, object, scene]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/retro-diffuse-gradient/STYLE.md
style_anchors:
  - soft diffuse color fields and blurred edges
  - vintage print grain, paper texture, scan noise, and darkroom development feel
  - independent magazine or experimental poster typography
  - variable layout, not a fixed left-title/right-circle template
  - abstract mood carried by color, texture, and restrained geometry
cover_shape_adaptation:
  - main title should interact with diffuse fields through contrast, cutout, edge placement, grid, or atmospheric embedding
  - subtitle and small text should behave like magazine microtype, index marks, or minimal art-poster labels
  - visual metaphor should be translated into color atmosphere, blur, scanning, fog, or abstract field structure
must_preserve:
  - visible diffuse gradient atmosphere with print texture
  - readable title
  - mature editorial order and variation
avoid_when_applying_to_cover:
  - cheap rainbow gradient or generic bokeh background
  - fixed left-title plus right-circle composition
  - concrete face or character unless explicitly requested
```

## Style Intent

以柔和彌散色塊、舊印刷顆粒、暗房顯影和雜誌網格形成復古氛圍。適合情緒、藝術、設計、品牌和獨立雜誌式封面。該 style 只負責彌散色域、復古印刷質感和編輯排版；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 藝術、設計、音樂、品牌、情緒化文章
- 公眾號、X 頭圖、作品集和雜誌風封面
- 需要氛圍感但仍保持標題可讀的內容

## Avoid

- 廉價漸變背景
- 標題左側加大圓的固定範本
- 色彩過髒、過花或搶掉資訊層級
