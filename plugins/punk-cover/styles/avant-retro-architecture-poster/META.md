# 先鋒復古建築海報

```yaml
id: avant-retro-architecture-poster
name: 先锋复古建筑海报
input_modes: [text]
subjects: [architecture, landmark, city, place]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 英文名称, 城市, 国家, 坐标, 补充背景, 情绪倾向, 不想出现的元素]
source: styles/avant-retro-architecture-poster/STYLE.md
style_anchors:
  - mid-century retro architectural travel poster
  - neo-constructivist spatial order and bold architectural massing
  - one recognizable core building as the sole visual center
  - large flat solid-color background with generous negative space
  - 2-3 complete color planes inside the building body
  - restrained archival or editorial typography with subtle screen-print texture
cover_shape_adaptation:
  - choose camera angle, crop, subject position, and composition from the building's silhouette, proportion, massing, and aspect ratio
  - building color planes should follow major structural faces, light and shadow, roof and wall, tower and base, or foreground and rear volume
  - title and optional metadata should sit in negative space or along the building's contour without overtaking the building
must_preserve:
  - one core building only, instantly recognizable at cover scale
  - adaptive viewpoint and composition instead of a fixed low-angle poster formula
  - solid pure-color background and open negative space
  - building body carries the richest color relationships
  - simplified hard-edged light, shadow, massing, and screen-print grain
avoid_when_applying_to_cover:
  - fixed yellow, teal, red-blue-cream, or repeated preset palette
  - decorative circles, triangles, sun disks, radial lines, random diagonal graphics, or complex collage
  - photorealistic architecture rendering, detailed windows, glass reflections, metallic highlights, or dense city skyline
  - invented coordinates, city names, countries, years, slogans, translations, or travel copy
```

## Style Intent

先鋒復古建築海報風格。以 20 世紀中期建築旅行海報、新構成主義秩序、現代編輯設計和絲網印刷質感，把一座建築轉譯成色塊完整、輪廓清晰、留白開闊的封面或海報。該 style 只負責建築視覺語言、構圖判斷、配色關係和圖文秩序；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 地標建築、城市建築、建築旅行、城市海報、展覽和活動海報
- 建築評論、城市觀察、空間設計、旅行目的地和文化地標文章封面
- 需要復古、先鋒、明亮、秩序感和高識別度建築主體的封面

## Avoid

- 不適合沒有明確建築主體的抽象觀點文或純人物主題
- 不適合需要照片寫實、建築效果圖、資訊圖或完整旅遊宣傳文案的任務
- 不適合同時展示多個同等重要建築或複雜城市天際線的場景
