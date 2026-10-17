# 復古時代錯位編輯封面

```yaml
id: midcentury-surreal-editorial-cover
name: 复古时代错位编辑封面
input_modes: [text]
subjects: [concept, person, object, technology, scene, editorial_topic]
outputs: [cover, poster, editorial_page]
default_ratio: "auto"
required_fields: [主题或主标题, 画幅比例]
optional_fields: [副标题, 人物设定, 情感倾向, 语言, 用途, 补充背景, 不想出现的元素]
source: styles/midcentury-surreal-editorial-cover/STYLE.md
style_anchors:
  - modern minimal editorial cover composition with large warm-white negative space
  - 1940s-1960s American commercial illustration characters with varied faces, ages, roles, and actions
  - one contemporary or future object used as a clear era-displacement visual metaphor
  - vintage magazine collage edges, halftone dots, faded ink, paper fibers, and screen-print grain
  - restrained 3-5 color palette with black editorial typography and no generic AI-tech tropes
cover_shape_adaptation:
  - landscape covers reserve roughly 65-75 percent on the left for title and breathing room and 25-35 percent on the right for the visual event
  - portrait covers place title in the upper or upper-left area and the visual event in the lower or lower-right area
  - square covers remain visibly asymmetric rather than splitting the canvas into equal panels
  - dissolve illustration edges into the paper with feathered ink, dry-brush fade, collage erosion, or halftone disappearance instead of regular frames
must_preserve:
  - one topic, one action, one core object, one main metaphor, and one era-displacement relationship
  - clear, accurate, readable title with minimal supporting text
  - recognizable mid-century commercial illustration character without repeating a fixed face or gender pairing
  - modern object must serve the topic rather than exist as decorative technology
  - warm-white paper field, editorial hierarchy, and deliberate asymmetry
avoid_when_applying_to_cover:
  - generic AI imagery such as neon blue-purple gradients, cyberpunk glow, robots, AI brains, chips, holographic HUDs, code rain, or floating UI walls
  - photorealism, smooth modern digital painting, 3D CG, anime, or a generic beautiful recurring face
  - centered hero portrait, static people facing camera, equal left-right split, full-bleed busy scene, or hard rectangular collage frame
  - unnecessary props, multiple competing metaphors, feature lists, icons, logos, watermarks, dense labels, or fake magazine mastheads
```

## Style Intent

把今天或未來才會發生的主題，交給一位 1958 年的美國商業插畫師來描繪。用現代極簡編輯設計承載 1940s–1960s 復古商業插畫人物，讓人物正在使用一個當代或未來物件，並通過一次剋制的超現即時代錯位表達主題。該 style 只負責復古人物、時代錯位、視覺隱喻、紙張印刷質感和編輯留白；平台適配、長文提煉和通用封面流程由 `punk-cover` 負責。

## Use For

- AI、Coding、數字人、知識庫、創作工具、未來工作和技術改變人的主題
- 需要像獨立雜誌封面一樣有觀點、有故事、有復古質感的文章、X 頭圖、公眾號封面和海報
- 需要人物動作與現代物件共同承載抽象概念，而不是把主題畫成科技圖標的內容

## Avoid

- 只需要純文字、純幾何、攝影或嚴格資訊圖的任務
- 必須相依大量說明文字、多個功能模組或多步驟流程才能成立的主題
- 無法收束為一個動作、一個核心物體和一個時代錯位關係的內容
