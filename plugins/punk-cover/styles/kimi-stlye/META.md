# kimi風格

```yaml
id: kimi-stlye
name: kimi风格
input_modes: [text]
subjects: [concept, object, product, material, research, system, scene]
outputs: [cover, poster, editorial_page]
default_ratio: "5:2"
required_fields: [主题, 主标题, 画幅比例, 语言, 用途]
optional_fields: [副标题, 核心概念, 主视觉物件, 辅助物件, 补充背景, 不想出现的元素]
source: styles/kimi-stlye/STYLE.md
style_anchors:
  - top-down archival still-life photography on a large softly lit table
  - pale gray-green or light mint background with restrained low-saturation materials
  - one abstract topic translated into a small set of real, relevant objects
  - Swiss editorial layout with a clean title zone and generous negative space
  - realistic metal, glass, wood, ceramic, paper, textile, pigment, or prototype materials
cover_shape_adaptation:
  - choose or preserve the platform ratio and rebuild the object layout for each landscape, portrait, or square canvas
  - keep the title area clean and readable instead of filling the whole table
  - use a small number of objects with clear hierarchy, spacing, overlap, and natural shadows
  - change the object set and spatial relationship for each topic; do not reuse a fixed archive-desk template
must_preserve:
  - top-down still-life photography and soft diffused light
  - pale gray-green or light mint background with low-saturation supporting colors
  - one clear title, one core concept, and one coherent object system
  - every object has a visible relationship to the topic
  - real material texture and enough negative space for an editorial cover
avoid_when_applying_to_cover:
  - Kimi logos, wordmarks, interface elements, signatures, or copied official layouts
  - fixed object combinations, paper piles, file clutter, or meaningless decoration
  - neon technology style, cyberpunk, cheap futurism, complex UI, or excessive glow
  - unreadable title, garbled text, dense microtype, or a table filled edge to edge
```

## Style Intent

以 `kimi风格` 為識別名稱，把主題轉化為俯視角檔案桌靜物攝影。使用淡灰綠燈箱桌面、少量真實物件、編輯排版和大面積留白，形成專案檔案或設計研究桌的封面。名稱用於指代視覺方向，不復制 Kimi 的 Logo、字標、產品介面或固定官方版式。平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- AI、研究、知識、產品、材料、系統和創意專案主題
- X、公眾號、文章、產品介紹、教學和專案檔案封面
- 需要真實靜物攝影、概念物件和低飽和編輯排版的內容

## Avoid

- 需要人物敘事、複雜資訊圖、介面展示或動態場景的內容
- 無法轉化為少量相關物件、只能相依大量文字說明的主題
- 需要複製真實品牌介面、Logo 或廣告畫面的任務
