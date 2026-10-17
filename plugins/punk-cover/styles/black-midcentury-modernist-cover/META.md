# 黑色復古現代主義封面

```yaml
id: black-midcentury-modernist-cover
name: 黑色复古现代主义封面
input_modes: [text]
subjects: [concept, person, product, architecture, animal, technology, service_scene, object]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 辅助短句, 核心主体, 点缀色, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/black-midcentury-modernist-cover/STYLE.md
style_anchors:
  - black-dominant mid-century modern editorial illustration
  - retro book cover, vintage magazine, noir, and geometric graphic design language
  - strict three-color system with black, warm white, and one vivid accent color
  - one simplified core subject, one visual center, and one main title group
  - flat geometric shapes, silhouette-like light and shadow, restrained screen-print grain
cover_shape_adaptation:
  - adapt layout to the selected aspect ratio, including image-left text-right, text-left image-right, centered subject, upper-lower split, or single-subject poster composition
  - keep one core subject and one accent-color focus, with generous black negative space where useful
  - horizontal covers may use strong side-by-side subject and typography balance
  - vertical covers should prioritize a compact poster-like hierarchy with the title and subject clearly separated
must_preserve:
  - black as the dominant color across background or subject
  - no more than three colors: black, white or warm ivory, and one vivid accent
  - mid-century modern retro editorial illustration character
  - strong, readable title and concise supporting text
  - full-bleed edges with no card frame, border, rounded white margin, or outer pale band
avoid_when_applying_to_cover:
  - neon cyberpunk, modern blue-purple technology gradients, glass effects, metallic 3D, or complex lighting
  - multicolor palettes, multiple bright accents, complex gradients, or high-saturation colorful poster treatment
  - photorealism, anime style, 3D rendering, dense mechanical detail, busy icon systems, or internet-ad clutter
  - information overload, many labels, parameter panels, serial numbers, or explanatory text
```

## Style Intent

黑色復古現代主義封面是一種黑色主導、三色剋制、圖形化強的復古編輯插畫風格。它融合 20 世紀中期現代主義書封、復古雜誌封面、黑色電影氣質和幾何平面設計語言，把主題提煉成一個清晰主體、一個色彩重點和一組醒目標題。該 style 只負責視覺語言、配色、主體概括、圖文秩序和邊緣約束；平台適配、長文提煉和通用封面結構由 `punk-cover` 負責。

## Use For

- 觀點文章、服務介紹、產品主題、人物專題、城市建築、科技設備和抽象概念封面
- 需要復古高級、理性剋制、黑色主導、標題醒目和強封面感的公眾號、X、影片封面和海報
- 適合希望主題清楚但不落入普通網際網路宣傳海報的內容

## Avoid

- 需要照片寫實、3D 產品繪製、賽博科技感、複雜資訊圖或多主體敘事的封面
- 需要大面積彩色漸變、華麗光效、玻璃質感、金屬質感或高飽和多彩視覺的任務
- 相依大量小字、標籤、編號和說明文字才能成立的內容
