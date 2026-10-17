# 諮詢報告視覺

```yaml
id: consulting-report-visual
name: 咨询报告视觉
input_modes: [text]
subjects: [concept, object, scene]
outputs: [cover, poster, editorial_page]
default_ratio: "2.35:1"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/consulting-report-visual/STYLE.md
style_anchors:
  - high-end management consulting report cover
  - typography-led Swiss grid with structured negative space, report header and footer, and a visible field of precise thin-line annotation
  - one short high-impact A-layer core phrase, with the complete source title preserved as a smaller B-layer report title
  - restrained regular-to-medium-weight Chinese typography, including thin-line, outlined, cut, hollow, or structurally rebuilt letterforms
  - one structured business metaphor such as a strategic path, threshold, fault line, coordinate, matrix boundary, or convergence point
  - the metaphor grows from, enters, cuts, frames, or extends the title letterforms instead of sitting beside them as an independent diagram
  - white, deep navy, cool gray, silver gray, and at most one very small controlled accent color
cover_shape_adaptation:
  - for a long source title, extract a 2-8 Chinese-character A-layer core phrase and keep the complete title in a smaller header, subtitle, or edge information band
  - the A-layer may be large but must not become extra-bold, dense, or oppressive
  - main title should be structurally rebuilt and interlock with a path, threshold, fault line, coordinate, matrix boundary, or strategic map
  - use only one core metaphor, one clear visual center, very few labels, and substantial negative space
  - negative space must remain designed rather than empty; use a restrained secondary field of perspective lines, contours, coordinates, thresholds, construction geometry, or analytic annotations behind and around the title
  - the complete B-layer title or subtitle must be visibly present whenever the user supplies one
  - subtitle and supporting text should look like report-cover deck labels, page furniture, and section indexing, not social-media decoration
  - keep the output unmistakably a cover; do not unfold the article into a process, framework explanation, dashboard, or full slide
must_preserve:
  - A-layer short core phrase remains the visual center while the complete source title remains readable at B-layer
  - restrained cover information density with visibly designed background structure rather than an empty canvas
  - readable B-layer title or subtitle, plus enough report furniture and fine-line geometry to establish a complete cover system
  - professional restraint, credible business structure, and clean boardroom-ready hierarchy
  - graphic structure is fused with the typography and remains subordinate to it
  - modern restrained type weight rather than heavy social-poster typography
avoid_when_applying_to_cover:
  - using the complete long source title as one giant extra-bold block when a short A-layer phrase can carry the visual
  - extra-bold, black-heavy, compressed, or oppressive title typography
  - three-or-more-step process flows, checkpoint timelines, complete funnels, full matrices, dashboards, or explanatory infographics
  - an independent icon, bubble, chart, or diagram placed beside the title without changing the title structure
  - too many labels, modules, badges, nodes, arrows, or content-page sections
  - an isolated core word floating on a nearly empty background with no subtitle, report hierarchy, or supporting structural field
  - fake detailed data, dense charts, or unreadable small text
  - PPT template feel or course-cover feel
  - generic office scene, handshake, or stock business people
```

## Style Intent

諮詢報告、管理框架和結構化商業分析風格。強調文字主導、標題結構重構、剋制但完整的封面資訊層次、圖形化秩序和可信的企業視覺。長標題必須先提煉短核心詞，再把完整標題降為清晰可見的報告式 B 層資訊。留白必須被網格、透視線、座標、輪廓或分析標註組織起來，不能只是空。該 style 只負責諮詢報告式視覺語言和商業結構隱喻；平台適配、文章摘要和通用輸出約束由 `punk-cover` 負責。

## Use For

- 商業策略、運營、產品分析、行業研究和方法論
- 公眾號封面、報告題圖、結構化商業文章頭圖
- 需要理性、清晰、剋制且由字體承擔主要隱喻的內容

## Avoid

- 虛假資料、複雜圖表堆疊
- 把長標題整塊放大、使用過粗字重或做成流程資訊圖
- 圖形與標題各自獨立、只在標題旁擺放泡沫或圖表
- 過度裝飾或社媒噪音
- 無關辦公場景和廉價商務人物
