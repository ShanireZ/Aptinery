# 巨型透視中文標題

```yaml
id: giant-perspective-chinese-title
name: 巨型透视中文标题
input_modes: [text]
subjects: [concept, object, scene]
outputs: [cover, poster]
default_ratio: "3:4"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/giant-perspective-chinese-title/STYLE.md
style_anchors:
  - enormous Chinese title as first visual
  - strong perspective, depth, speed, compression, or spatial pressure
  - title as architecture, road, wall, tunnel, sign, stage, or impact object
  - dramatic lighting, contrast color, motion lines, shadows, or event-poster energy
  - small scale references such as people, vehicles, signs, fragments, or urban edges
cover_shape_adaptation:
  - main title should occupy dominant cover space and become physical spatial structure
  - subtitle and labels should orbit the title as event-poster information hierarchy
  - visual subject should reinforce title scale, movement, conflict, or pressure
must_preserve:
  - readable correct Chinese title
  - strong perspective rather than ordinary flat title
  - title remains the main subject
avoid_when_applying_to_cover:
  - weak title hierarchy
  - ordinary title over background image
  - illegible distorted Chinese characters
```

## Style Intent

以超大中文標題和強透視空間作為第一視覺，製造速度、壓迫、衝突和事件海報感。適合中文標題主導的高衝擊封面。該 style 只負責巨型中文標題、透視空間和衝擊構圖；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 小紅書、活動、觀點、熱點和強傳播封面
- 需要標題一眼抓住注意力的內容
- 適合中文短標題、強情緒和視覺衝突主題

## Avoid

- 標題錯字、斷字或不可讀
- 弱化中文標題主體
- 普通標題加背景圖
