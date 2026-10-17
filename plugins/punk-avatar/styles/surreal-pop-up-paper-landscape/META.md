# 立體人物扁平景色紙藝

```yaml
id: surreal-pop-up-paper-landscape
name: 立体人物扁平景色纸艺
input_modes: [image]
subjects: [person, scene]
outputs: [before_after, portrait, editorial_artwork]
default_ratio: mode-specific
required_fields: [上传人物照片, 输出模式]
optional_fields: [画幅比例]
source: licensor-authored prompt and licensor-provided reference image
modes:
  before-after:
    name: 前后对比图
    default_ratio: "3:2"
    reference: references/before-after.md
  final-artwork:
    name: 单张效果图
    default_ratio: "3:4"
    reference: references/final-artwork.md
style_anchors:
  - one photorealistic upright person rising from the original scene flattened onto paper
  - environment folded backward around the subject contact point by 75 to 85 degrees
  - non-person vertical height compressed to 10 to 20 percent
  - warm off-white fibrous art paper, broad negative space, and a short soft contact shadow
  - wide shallow oval or fan-shaped landscape with photographic detail and restrained paper-fiber edges
must_preserve:
  - recognizable identity, face, hair, expression, clothing, accessories, pose, gesture, body proportions, camera angle, lighting, and color
  - major scene elements and their original color relationships
  - a clear 90-degree spatial contrast between upright person and paper-parallel environment
avoid_when_applying_to_avatar:
  - redesigning, beautifying, cartoonizing, duplicating, or deforming the person
  - any upright car, building, tree, mountain, furniture, or other non-person element
  - ordinary background replacement, background blur, full-scene watercolor treatment, or a flat photo collage
  - long hard shadows, narrow pointed projections, cutout halos, text, borders, logos, or watermarks
```

## Style Intent

把一張人物環境照轉化為超現實紙藝裝置：人物保持真實、清晰、三維並垂直於紙面；照片中的其餘世界從人物腳下或身體接觸點向後翻倒，壓縮成貼在紙面上的寬淺二維景色。作品具有攝影真實感、立體書結構和高級編輯插圖氣質。

## Use For

- 人物與汽車、建築、道路、海面、山川、餐廳、樹木、桌椅等環境同時出現的照片
- 希望保留真人身分與動作，同時製造“人物從扁平現實中站起”效果的圖像
- 需要原圖與效果並排展示，或只需要一張最終藝術效果圖的任務

## Avoid

- 沒有人物主體、人物被嚴重遮擋或無法確認主要人物的輸入
- 需要重設計人物、改變服裝動作、卡通化或插畫化人物的任務
- 需要保留正常直立背景、複雜文字排版或多人物合成的任務
