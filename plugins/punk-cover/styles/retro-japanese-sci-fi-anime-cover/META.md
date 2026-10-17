# 復古日本科幻動畫

```yaml
id: retro-japanese-sci-fi-anime-cover
name: 复古日本科幻动画
input_modes: [text]
subjects: [concept, person, machine, interface, system, code, product, object, scene]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 主标题, 画幅比例, 用途]
optional_fields: [主题说明, 主体类型, 人物设定, 副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/retro-japanese-sci-fi-anime-cover/STYLE.md
style_anchors:
  - 1990s Japanese sci-fi cel animation keyframe energy
  - title-card-like high-contrast serif typography as the first visual
  - saturated hard-edge color blocks with strict limited palette
  - sharp hand-drawn linework, cel shadows, exaggerated perspective, and dramatic contrast
  - one metaphor, one main subject, one active transformation or conflict
  - light film grain and retro animation still texture
cover_shape_adaptation:
  - wide covers should use left-title-right-visual or right-title-left-visual tension with horizontal motion and depth
  - square and 4:3 covers should use offset, diagonal, or layered title-image composition rather than equal split blocks
  - vertical covers should use top-title-bottom-visual, side vertical title, or vertical subject movement
  - redesign composition for each ratio instead of cropping a single layout
must_preserve:
  - accurate, complete, readable main title as the first visual
  - one visual center, one core metaphor, and one main action
  - strict palette selected from the defined colors with uneven color area distribution
  - retro cel animation keyframe feeling with hard shadows and high contrast
  - safe margins for title, key action, and auxiliary text
avoid_when_applying_to_cover:
  - copied characters, mecha designs, logos, titles, or scenes from existing anime works
  - 3D render, photorealism, modern cyberpunk, flat corporate tech illustration, or generic UI style
  - average use of all palette colors or large gradients
  - static posing, decorative symbols, crowded UI, multiple metaphors, or multiple visual centers
  - ordinary sans-serif, rounded, or modern UI typography
```

## Style Intent

以 90 年代日本科幻賽璐璐動畫和標題卡氣質為視覺骨架，用高飽和限色色塊、鋒利線稿、硬邊陰影、誇張透視和高對比標題製造緊張、決斷、啟動與重組感。該 style 只負責復古科幻動畫封面的視覺語言、限色系統、標題氣質、主體動作和構圖適配；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- AI、工具、系統、程式碼、產品、方法論、知識類主題的高衝擊封面
- 心理、成長、關係、社會衝突和情緒類主題的動作隱喻封面
- X 封面、公眾號封面、影片封面、海報和文章插圖

## Avoid

- 復刻具體動畫作品的角色、機體、標誌、標題或經典場景
- 現代賽博朋克、攝影寫實、3D 機甲、企業科技風和普通扁平插畫
- 資訊卡片、步驟列表、大量小字、條形碼、日期、版本號或複雜 UI
