# 商業雜誌頭版

```yaml
id: business-magazine-front-page
name: 商业杂志头版
input_modes: [text]
subjects: [concept, person, object, scene]
outputs: [cover, poster, editorial_page]
default_ratio: "2.35:1"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/business-magazine-front-page/STYLE.md
style_anchors:
  - business and technology magazine front-page structure
  - bold sharp title with trend-report energy
  - one strong commercial metaphor object or scene
  - editorial bars, section labels, data-news cues, and high-contrast blocks
  - confident media-like visual hierarchy without real publication branding
cover_shape_adaptation:
  - main title should integrate with a market curve, maze, warning sign, strategic map, funnel, price tag, or system node
  - subtitle and labels should behave like magazine deck, column labels, short conclusion, or issue tags
  - visual metaphor should make the business judgment visible at cover scale
must_preserve:
  - magazine front-page authority and strong editorial hierarchy
  - one memorable commercial metaphor
  - limited but credible supporting information
avoid_when_applying_to_cover:
  - fake real media masthead, logo, or trademark
  - stock market screen, handshake photo, or unrelated office person
  - dense fake columns or cheap finance template
```

## Style Intent

商業科技雜誌頭版式封面。強調銳利標題、編輯欄、主視覺人物或概念物、趨勢報道感和高級商業傳播氣質。該 style 只負責商業雜誌頭版結構、媒體感和商業隱喻；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- AI、創業、投資、商業趨勢、產品和公司分析
- 公眾號封面、X 頭圖、行業報道題圖
- 需要媒體感、權威感和觀點張力的內容

## Avoid

- 假新聞式噪音、廉價財經範本
- 過多欄目文字
- 仿冒真實媒體刊名、Logo 或商標
