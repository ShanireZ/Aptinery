# 極簡紙感丙烯色塊插畫

```yaml
id: minimal-paper-acrylic-block-illustration
name: 极简纸感丙烯色块插画
input_modes: [image, text]
subjects: [person, pet, object, scene, concept]
outputs: [avatar, portrait, editorial_page]
default_ratio: "1:1"
required_fields: [照片或主题]
optional_fields: [画幅比例, 名称或文字, 用途, 情绪倾向, 保留特征, 不想出现的元素]
source: styles/minimal-paper-acrylic-block-illustration/STYLE.md
style_anchors:
  - rough white paper with visible fibers and a quiet editorial field
  - highly simplified subject silhouette occupying roughly 10-20 percent of the canvas
  - thin, light, slightly unstable hand-drawn lines used only for structural hints
  - two to four clear acrylic paint color blocks with hand-painted uneven edges
  - large negative space, restrained childlike poetry, and symbolic scene extraction
subject_composition:
  - keep one primary subject or one symbolic scene and remove nonessential details
  - preserve the most recognizable pose, action, outline, structure, or visual mark
  - for profile-avatar use, keep the small subject readable at thumbnail size without turning it into a full-frame close-up
background_behavior:
  - use rough white paper as the default background
  - suggest the original environment with at most a few lines or one small color field when semantically necessary
color_material_texture_rules:
  - use no more than four main colors, selected from vivid red, yellow, blue, green, or a restrained subset
  - allow a small amount of black or dark gray for structural lines
  - visible paper grain, acrylic flat-paint coverage, slight pigment unevenness, and handmade edges
must_preserve:
  - one memorable visual moment rather than a miniature realistic copy
  - small subject, generous white space, clear color blocks, and strong recognition
  - paper texture and hand-made imperfection
avoid_when_applying_to_avatar:
  - colored-pencil, crayon, watercolor wash, pure line art, heavy oil paint, smooth digital illustration, 3D, or commercial cartoon gloss
  - crowded background, excessive perspective, more than four main colors, tiny faint color accents, or over-detailed realism
  - decorative elements that do not support the subject, repeated generic AI polish, or a fixed recurring composition
```

## Style Intent

把照片或主題提煉成一張極簡紙感手繪封面插畫。畫面像畫在略粗糙的白紙上：用細而輕的手繪線條提示結構，用少量但明確的丙烯色塊讓主體成立。預設主體只佔畫面約 10%–20%，大面積留白承擔安靜、剋制、童趣、輕鬆和詩意。該 style 只負責主體提煉、紙張媒介、線條、丙烯色塊和留白；頭像流程、比例、裁切安全和輸出規則由 `punk-avatar` 負責。

## Use For

- 人物、寵物、物品、建築或具有明確視覺符號的主題照片
- 需要把一個場景提煉成小型編輯插畫、頭像衍生圖或紙感視覺卡片的內容
- 需要少細節、強識別、明顯色塊和大量留白的輕量視覺表達

## Avoid

- 需要寫實相似度、完整場景重建、複雜資訊圖或滿版海報的任務
- 相依大量文字、多個主體或豐富背景才能說明的主題
- 無法歸納為一個清晰輪廓、動作、結構或視覺記憶點的素材
