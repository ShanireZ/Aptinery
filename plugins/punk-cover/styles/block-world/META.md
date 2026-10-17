# 方塊世界

```yaml
id: block-world
name: 方块世界
input_modes: [text]
subjects: [concept, object, scene]
outputs: [cover, poster]
default_ratio: "3:4"
required_fields: [主题词, 画幅比例, 语言, 用途]
optional_fields: [副标题, 补充背景, 情绪倾向, 不想出现的元素]
source:
  - "licensor-authored private export: Prompt列表_导出_2026-06-16/04_像素创想/提示词.md"
  - "licensor-authored private export: Prompt列表_导出_2026-06-16/10_像素创世/提示词.md"
style_anchors:
  - Minecraft-like voxel world
  - high-saturation block materials and square geometry
  - title reconstructed as terrain, portal, building, road, island, or mission structure
  - small block characters, tools, paths, signs, maps, and item panels
  - clean layered lighting with playful exploratory space
cover_shape_adaptation:
  - main title should exist as real block architecture or voxel signage
  - subtitle and labels should appear as game UI, quest panels, signs, mini maps, or inventory items
  - visual metaphor should be built as a navigable voxel scene
must_preserve:
  - all major visual elements built from blocks, pixels, voxels, or grid materials
  - spatial depth and clear path back to the title
  - bright game-world clarity
avoid_when_applying_to_cover:
  - ordinary pixel filter over a flat poster
  - title pasted over a game illustration
  - cheap cartoon sticker collage or generic robot-tech imagery
```

## Style Intent

Minecraft 式高飽和方塊世界海報。主題文字被方塊化重構成建築、道路、傳送門、礦洞、階梯或場景結構，而不是後貼字幕。該 style 只負責方塊世界的場景、材質和空間結構；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 教學、工具、系統搭建、升級和學習內容
- 遊戲化表達、創造、探索、AI 工具和方法論
- 需要明亮、治癒、強傳播感的社媒封面

## Avoid

- 普通像素濾鏡或簡單遊戲插畫
- 標題與場景分離
- 廉價藍紫科技感、俗套機器人臉
