# 極簡輕科技

```yaml
id: minimal-light-tech
name: 极简轻科技
input_modes: [text, image]
subjects: [technology, product, tutorial, tool, brand, concept, essay]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [内容主题, 画面文字, 画幅比例, 渐变色系选择, 是否提供 logo]
optional_fields: [配色补充说明, 主视觉偏好, logo 使用说明, 参考图说明]
source: styles/minimal-light-tech/STYLE.md
style_anchors:
  - clean white, warm-white, or light gray background with large negative space
  - one single visual anchor only: lightly dimensionalized brand logo OR one abstract soft 3D glass/gradient form
  - soft refined gradients concentrated on the anchor, not filling the canvas
  - modern ultra-bold Chinese sans-serif title in black or near-black
  - quiet premium light-tech product cover feel without cyberpunk or dense UI
cover_shape_adaptation:
  - landscape ratios prefer left-title and right-anchor, or quiet asymmetric balance with generous breathing room
  - portrait ratios keep title in the upper or middle zone and the single anchor compact below or beside it
  - never print the aspect-ratio numbers into the image; ratio only controls composition
  - when 画面文字 is「无文字」, rely on the single visual anchor and leave typography out
must_preserve:
  - one visual center and one anchor only
  - large clean negative space on a light background
  - exact on-screen text when the user did not choose「无文字」
  - soft gradient or light dimensional treatment limited to the anchor
avoid_when_applying_to_cover:
  - cyberpunk neon, dense UI panels, dashboards, collage, or filling the frame
  - multiple anchors, multiple logos, icon grids, or competing decorations
  - heavy textures, loud marketing posters, people, product photography clutter, or hard metallic chrome
  - printing ratio labels, watermarks, or unrelated small supporting text blocks
```

## Style Intent

極簡輕科技是一種以大面積純白 / 暖白 / 淺灰留白為底、只用一個主視覺錨點的輕科技產品封面風格。錨點可以是輕微立體化的品牌 Logo，或一枚抽象的柔和 3D 玻璃 / 漸變形體；漸變只集中在錨點上，標題使用現代超粗黑體、黑色或近黑。該 style 只負責輕科技極簡視覺語言、單一錨點、漸變色系和排版氣質；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 科技產品、工具教學、品牌概念、輕科技主題和乾淨現代的文章 / 影片封面
- X 封面、公眾號封面、產品發佈頭圖、教學海報和品牌概念海報
- 需要純白留白、單一漸變錨點、現代黑體標題、剋制高級感的視覺

## Avoid

- 賽博朋克、霓虹、密集介面、資訊圖、拼貼或把畫面填滿的內容
- 需要人物故事、複雜場景敘事、多 Logo 生態圖或強營銷衝擊的封面
- 需要重金屬質感、硬科幻裝甲、大量標籤說明或多主視覺的任務
