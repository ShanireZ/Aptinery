# Anthropic Research 風格

```yaml
id: anthropic-research-style
name: Anthropic Research 风格
input_modes: [text]
subjects: [concept, essay, research, technology, knowledge, system]
outputs: [cover, poster, editorial_page]
default_ratio: "5:2"
required_fields: [主题, 主标题, 核心表达, 画幅比例, 用途]
optional_fields: [副标题, 背景方案, 强调色, 不想出现的元素]
source: styles/anthropic-research-style/STYLE.md
style_anchors:
  - restrained AI research-lab editorial cover with a large flat color field
  - one readable serif main title as the primary visual center
  - one abstract hand-drawn line metaphor derived from the topic's core value
  - substantial negative space with 2-4 small organic balancing shapes
  - fixed low-saturation palette using terracotta, black, warm gray, sage green, or haze blue
cover_shape_adaptation:
  - landscape ratios place the title and abstract metaphor in an asymmetric editorial composition with large open space
  - portrait ratios keep the title dominant and the metaphor compact, with decoration occupying no more than 5% of the canvas
  - show only the main title by default; when the user supplies a subtitle, keep it to one short supporting line
  - convert the topic into a conceptual structure, path, node system, outline, or spatial relation instead of drawing the topic object literally
must_preserve:
  - one main title, one core metaphor, and one visual center
  - flat background selected from the fixed color system without gradients
  - serif-led editorial typography with restrained sans-serif or monospace support text
  - sparse hand-drawn linework and stable negative space
avoid_when_applying_to_cover:
  - Anthropic logos, wordmarks, signatures, or copied official layouts
  - marketing-poster hierarchy, product-launch visuals, or commercial template feel
  - robots for AI, ordinary computers for web topics, or book piles for knowledge topics
  - cyberpunk, neon, blue glow, 3D rendering, gradients, dense infographics, or large text blocks
```

## Style Intent

以 Anthropic Research 風格為識別名稱，使用純色背景、襯線主標題、手繪線稿、抽象隱喻和大面積留白形成研究報告式封面。名稱用於指代視覺方向，不復制 Anthropic 的 Logo、品牌署名、字標或固定版式。平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- AI、研究、知識、系統、網頁和設計方法主題
- X 封面、文章封面、產品介紹和教學海報
- 需要少量文字、抽象隱喻和純色背景的編輯封面

## Avoid

- 營銷海報、科技發佈會和商業範本
- 需要複雜資料圖表、產品介面或多場景敘事的內容
- 需要複製真實品牌視覺識別的任務
