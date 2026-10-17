# 超大標題圖文穿插

```yaml
id: interleaved-title-editorial-poster
name: 超大标题图文穿插
input_modes: [text]
subjects: [person, sculpture, product, object, architecture, animal, abstract, concept]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词或原文, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/interleaved-title-editorial-poster/STYLE.md
style_anchors:
  - one theme-matched high-recognition subject with a clean silhouette, without defaulting to sculpture, metal, robots, or futuristic mannequins
  - one enormous short title integrated into the composition
  - explicit back-title, subject, and front-title layers with controlled mutual occlusion and at least two visible depth-order switches inside the title
  - bold geometric sans-serif typography with clean edges and preserved readability
  - restrained editorial details, visible breathing room, and a theme-derived 2-4 color palette
cover_shape_adaptation:
  - derive a 2-8 character Chinese title or 1-4 word English title when the source is long-form
  - choose photography, a real-life subject, illustration, collage, silhouette, or abstraction according to the topic instead of repeating one material language
  - recompose title lines, subject placement, layering, and whitespace for each requested aspect ratio
  - keep no more than three information levels: main title, central subject, and minimal support text
  - place occlusion away from a person's eyes, nose, mouth, and other critical identifying features
must_preserve:
  - exactly one core subject and one clear focal point
  - readable accurate main title despite partial cropping and occlusion
  - visible typography-subject interleaving in both directions within the core overlap zone, not text pasted over an image or a subject placed in front of one whole title row
  - obvious negative space and visual pauses around the main title-subject relationship
  - modern magazine, exhibition, or brand-campaign editorial finish
avoid_when_applying_to_cover:
  - multiple unrelated subjects or noun-by-noun illustration
  - whole-line translucent type, mechanical top-background and bottom-foreground splits, random overlap, or unreadable letterforms
  - repetitive chrome people, sculptural heads, robots, mechanical faces, or futuristic mannequins used as a generic shortcut for design
  - blocked facial features, malformed typography, misspelled Chinese, or decorative gibberish
  - PPT, e-commerce, feed-ad, cheap template, or complex technology-dashboard aesthetics
```

## Style Intent

以一個由主題決定表現語言的單一主體和一個超大短標題共同建立構圖，通過標題內部多次換層、主體遮字與文字壓主體的雙向咬合形成明確空間層次，同時保留可見留白和呼吸感。適合需要強編輯感、雜誌封面感、展覽海報感和品牌主視覺衝擊力的內容。該 style 負責主體選擇、標題尺度、圖文穿插、比例適配和剋制編輯細節；平台適配、文章摘要和通用輸出規則由 `punk-cover` 負責。

## Use For

- 中文或英文短標題主導的社交封面、橫幅和豎版海報
- 真實人物、生活場景中的人或物、插畫、拼貼、剪影、產品、物件、建築或抽象圖形作為單一主視覺的內容
- 需要標題本身參與構圖，而不是簡單“圖片上加字”的主題
- 適合 X、微信公眾號、小紅書、展覽視覺和品牌 campaign

## Avoid

- 多主體敘事、資訊密集型圖表或需要展示大量正文的內容
- 標題無法縮短且必須逐字完整佔據主視覺的場景
- 低對比、弱層級、隨機遮擋或普通範本式圖文疊加
