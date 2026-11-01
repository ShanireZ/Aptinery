# 古典油畫 · 極簡視覺隱喻

```yaml
id: classical-oil-minimal-metaphor
name: 古典油画 · 极简视觉隐喻
input_modes: [text]
subjects: [concept, person, object, relationship, culture, technology]
outputs: [cover, poster]
default_ratio: "5:2"
text_policy: none
required_fields: [主题, 核心意思]
optional_fields: [画面比例, 视觉方向]
source: styles/classical-oil-minimal-metaphor/STYLE.md
style_anchors:
  - Classical oil painting collage, Renaissance and Baroque aesthetics, Old Master painting texture, surreal editorial art, minimalist visual metaphor
  - pure white background (#FFFFFF) with oil-paint texture confined to the cutout subjects
  - warm richly layered painted figures and objects with authentic brushwork, classical clothing, and natural light
  - one poetic surreal event with one to three main elements and generous negative space
cover_shape_adaptation:
  - use the topic as semantic input only; render no title, subtitle, letters, labels, logo, or watermark
  - landscape emphasizes spatial relationships and horizontal narrative; portrait emphasizes gesture and focus
  - keep heads, limbs, and key objects complete with ample white margins on every side
  - if neither platform nor ratio is specified for this explicitly selected style, use the default requested ratio of 5:2, then apply the workflow ratio-resolution rule
must_preserve:
  - meaningful visual metaphor as the highest creative priority, expressed through action, scale, connection, substitution, or transformation
  - precise natural cutout edges and real Old Master painting texture inside subjects only
  - pure white untextured background, full-color subjects, restrained composition, and no visible text
  - fresh theme-specific figures, actions, and composition rather than a repeated template
avoid_when_applying_to_cover:
  - any text, title, letters, logos, watermarks, ornamental borders, or complex background
  - photography, modern people in historical costumes, 3D rendering, cartoon, or monochrome engraving
  - cyberpunk, neon, technology UI, stock AI robots, chips, circuits, or glowing brains
  - gratuitous religious symbols, repeated angels, symbol piles, clipped subjects, or overprocessed digital paint
```

## Style Intent

將當代思想轉化為從幾百年前的彩色油畫中剪下的一段故事：第一眼好奇，第二眼理解。主題和核心意思只用於構思，絕不作為畫面文字。

## Reference

上游提供的風格參考圖（上游儲存庫的 `screenshots/punk-cover-styles/classical-oil-minimal-metaphor.png`，未隨此套件散布）用於觀察油畫質感、白底、尺度與動作關係，不是固定人物或構圖模板。參考圖右側手部貼邊裁切不作為規範；生成時以主體完整、四周白色邊距為準。
