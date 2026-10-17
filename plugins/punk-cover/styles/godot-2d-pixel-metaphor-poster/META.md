# Godot 2D 像素隱喻海報

```yaml
id: godot-2d-pixel-metaphor-poster
name: Godot 2D 像素隐喻海报
input_modes: [text]
subjects: [concept, character, environment, scene, system, world]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题原文, 图片比例, 用途]
optional_fields: [补充语境, 情绪倾向, 禁止元素]
source: styles/godot-2d-pixel-metaphor-poster/STYLE.md
style_anchors:
  - one abstract idea translated into one concrete level, one game mechanic, and one immediately legible visual metaphor
  - one main pixel character performing one clear action toward or against one symbolic goal or obstacle
  - handcrafted 16-bit or 32-bit pixel art with crisp edges, consistent sprite scale, coherent pixel grid, and tilemap world logic
  - indie-game promotional-poster finish with environmental storytelling, cinematic pixel lighting, strong focus, and deliberate negative space
  - complete original theme text integrated into the game world through pixel typography, architecture, terrain, light, or character interaction
cover_shape_adaptation:
  - wide formats should emphasize horizontal movement, complete world depth, and distance between character and target
  - vertical formats should emphasize ascent, descent, growth path, or a distant target along the vertical axis
  - square formats should compress the metaphor into one central symbol, loop, or compact level with strong thumbnail recognition
  - recompose title position, character scale, level space, movement path, and negative space for custom ratios instead of cropping
must_preserve:
  - exactly one core viewpoint, one main metaphor, one main character, one action, and one goal or obstacle
  - accurate and fully readable original theme text, with one to three keywords optionally emphasized
  - shared pixel resolution and grid logic across character, environment, text, lighting, particles, and shadows
  - game-world depth and level-design logic without looking like a screenshot or gameplay interface
avoid_when_applying_to_cover:
  - photorealism, 3D render, ordinary anime, vector illustration, pixel-filtered photography, or mixed-resolution assets
  - multiple protagonists, multiple stories, multiple metaphors, four-panel layouts, crowded text, or complex game UI
  - inventory bars, status panels, menus, random English, watermark, logo, fabricated game metadata, or misspelled Chinese
  - copied characters, maps, sprites, tiles, icons, logos, trademarks, or recognizable levels from existing games
  - blurry pixels, smoothing filters, inconsistent pixel scales, weak title hierarchy, or generic screenshot composition
```

## Style Intent

把一句主題提煉成一個可以被玩家體驗的 Godot 2D 像素關卡，通過角色動作、環境關係、遊戲機制和目標/阻礙表達單一核心觀點。該 style 負責像素網格、關卡世界、機制隱喻、標題入景、色彩氣質和比例重構；平台確認、文章摘要、檔案保存和生成工具呼叫由 `punk-cover` 負責。

## Use For

- 成長、長期主義、方向選擇、內耗、希望、專注力、資訊洪流和人與系統關係
- AI、工具、知識、時代變化、規則衝突和抽象觀點類內容
- 公眾號、X、小紅書、影片封面、獨立遊戲風宣傳海報和文章題圖
- 能被轉譯為一個角色動作、一套關卡機制和一個清楚目標或阻礙的主題

## Avoid

- 需要多個同權重人物、複雜劇情分鏡、完整遊戲 UI 或大量資料說明的資訊圖任務
- 純頭像、照片轉像素、寫實肖像或需要復刻具體遊戲資產的請求
- 無法容納主題原文、單一隱喻或清楚視覺焦點的密集排版任務
