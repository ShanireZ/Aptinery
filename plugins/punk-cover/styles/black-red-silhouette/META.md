# 黑紅剪影

```yaml
id: black-red-silhouette
name: 黑红剪影
input_modes: [text]
subjects: [concept, tool, scene, person, object]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 核心场景, 主体动作, 视觉隐喻, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/black-red-silhouette/STYLE.md
style_anchors:
  - strict red, black, and white color system
  - large flat red stage-like background with no gradients or textures
  - black silhouette subject as the dominant visual focus
  - sparse white title, highlights, and key accent points only
  - one clear scene, one subject action, and one direct metaphor
cover_shape_adaptation:
  - main subject should occupy the central, center-right, or lower center area with a strong black silhouette
  - title should stay readable but restrained, avoiding competition with the visual subject
  - horizontal covers should place text left or right while preserving the silhouette scene as first visual focus
  - vertical covers should keep title at the top or bottom and make the central silhouette the absolute focus
must_preserve:
  - red, black, and white only
  - clean flat shapes and strong silhouettes
  - subject-first composition
  - simple, direct, immediately legible metaphor
avoid_when_applying_to_cover:
  - blue, purple, green, brown, dirty gray, metallic colors, or extra hues
  - gradients, neon glow, cyber blue light, paper grain, distressing, grime, or retro wear
  - realistic photography, detailed faces, complex UI panels, or infographic layouts
  - typography becoming the only or dominant visual subject
```

## Style Intent

黑紅剪影是一種高衝擊、低資訊噪聲的極簡封面風格。畫面像一塊巨大的紅色舞臺螢幕，主體以黑色圖形剪影出現，白色只用於標題、少量高光和關鍵點睛。該 style 只負責三色剪影視覺、主體優先的圖文關係和直接隱喻；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 工具教學、產品教學、AI 工具和工作流主題
- 電影、人物關係、速度、金融、觀察者和行動隱喻
- 需要遠看抓眼、近看乾淨的公眾號封面、X 封面、影片封面和海報

## Avoid

- 需要複雜資訊密度、資料圖表或多層敘事的內容
- 需要真實攝影、人臉細節、復古質感或複雜光效的封面
- 相依大量文字說明才能理解的主題
