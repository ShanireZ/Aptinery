# 科研期刊概念

```yaml
id: research-journal-concept
name: 科研期刊概念
input_modes: [text]
subjects: [concept, object, scene]
outputs: [cover, poster, editorial_page]
default_ratio: "2.35:1"
required_fields: [主题, 画幅比例]
optional_fields: [副标题, 学科方向, 核心机制, 文字需求, 配色方案, 版式偏好]
source: styles/research-journal-concept/STYLE.md
style_anchors:
  - top-tier research journal cover mood
  - original scientific main visual with mechanism implication
  - microscopic or macroscopic scientific metaphor
  - advanced color system with depth and precision
  - sparse editorial text integrated into scientific composition
cover_shape_adaptation:
  - main title should be treated as journal-cover title or restrained editorial text around the scientific visual
  - subtitle should be minimal and placed with scientific margins or grid logic
  - visual metaphor should become a scientific object, structure, field, network, mechanism, or section
must_preserve:
  - scientific subject or mechanism relevance
  - non-template journal-cover sophistication
  - no copied real journal identity
avoid_when_applying_to_cover:
  - real journal names, logos, or fixed official layouts
  - random DNA, chips, lab equipment, or blue-purple tech background
  - dense explanatory mechanism diagram
```

## Style Intent

科研期刊封面式概念視覺，強調機制、材料、醫學、生物、工程和實驗室語境。用專業但可傳播的科學隱喻組織畫面。該 style 只負責科研期刊封面氣質、科學主體和機制暗示；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 科研、醫學、材料、生物、工程和機制解釋
- 學術文章、技術報告、公眾號深度內容
- 需要權威感和概念視覺化的封面

## Avoid

- 科幻化過度、廉價實驗室素材
- 不準確或無關的科學符號
- 隨機科研符號和主題機制脫節
