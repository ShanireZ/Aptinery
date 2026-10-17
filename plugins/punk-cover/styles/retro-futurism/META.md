# 復古未來主義

```yaml
id: retro-futurism
name: 复古未来主义
input_modes: [text]
subjects: [technology, infrastructure, systems, future, science, city, work, media, editorial_topic]
outputs: [cover, poster, editorial_page]
default_ratio: "21:9"
required_fields: [主题或主标题, 画幅比例]
optional_fields: [副标题, 视觉叙事, 时代设定, 系统隐喻, 人物角色, 语言, 用途, 色彩偏好, 补充背景, 不想出现的元素]
source: styles/retro-futurism/STYLE.md
style_anchors:
  - mid-century imagined future expressed through monumental analog infrastructure, world-fair modernism, industrial architecture, transit systems, tubes, conveyors, and orbital or civic megastructures
  - one coherent flow, sorting system, machine process, or public infrastructure used as the visual metaphor rather than a collection of futuristic objects
  - small but legible human figures acting as workers, editors, engineers, clerks, travelers, or witnesses inside the system, providing scale and narrative tension
  - physical paper, folders, tickets, diagrams, punched cards, labels, and printed forms integrated into the machinery as material evidence of information flow
  - aged editorial print treatment with parchment, rust red, ochre, charcoal, petrol teal, faded blue, halftone, paper fibers, ink wear, and restrained registration drift
  - cinematic wide perspective with a strong central axis, radial or converging structural lines, and layered foreground, middle ground, and background depth
cover_shape_adaptation:
  - wide landscape covers favor a monumental central or slightly off-center system with clear title breathing room in the upper band, side band, or negative-space corridor
  - 16:9 covers retain the central-axis infrastructure while reserving a readable title zone and a human-scale figure or action as the narrative anchor
  - portrait covers turn the system into a vertical shaft, tower, archive, launch column, or stacked transit section; preserve the same analog future language without simply cropping the panorama
  - square covers use a strong radial hub or central machine chamber with asymmetrical paper and architectural layers around it
  - title typography behaves like period signage, printed editorial type, architectural lettering, or a physical label attached to the system, never like a floating modern interface
must_preserve:
  - one imagined future system, one primary flow or process, one central metaphor, and one readable human-scale action
  - physical cause-and-effect between tubes, belts, rails, chambers, documents, vehicles, or other system components
  - a believable mid-century material world: painted metal, concrete, glass, paper, enamel, rivets, dust, and imperfect print surfaces
  - a restrained period palette with the visual hierarchy led by the title and the system's central movement
  - complete, accurate, readable title text with only a small amount of supporting copy
  - visible scale contrast between monumental infrastructure and small human figures
avoid_when_applying_to_cover:
  - modern cyberpunk, neon glow, blue-purple sci-fi gradients, holographic HUDs, floating UI panels, code rain, glowing circuit boards, or generic AI imagery
  - clean contemporary 3D renders, photorealistic concept art, glossy product visualization, anime, game key art, or a sterile sci-fi spaceship interior
  - a random collage of rockets, robots, planets, screens, and gadgets without one coherent system or physical flow
  - oversized heroic character portraits, centered headshots, empty futuristic city skylines, or humans posed without an action
  - excessive microtext, fake labels, unreadable pseudo-writing, logos, watermarks, modern brand UI, or promotional feature lists
  - flat single-layer composition, equal-weight visual centers, arbitrary decorative machinery, or a hard rectangular poster frame
```

## Style Intent

把一個今天或未來才會發生的主題，交給一位 1930s–1960s 的工業設計師、世界博覽會建築師和科幻雜誌美術編輯來想象。未來不是霓虹燈和懸浮 UI，而是一套宏大、可見、可觸摸、略顯過載的模擬基礎設施：輸送管道、分揀軌道、紙質檔案、機械艙室、環形大廳、軌道交通、公共服務機器或太空時代的市民建築。人物很小，但動作必須讓人理解系統正在如何工作。

該 style 只負責復古未來主義的模擬基礎設施、系統隱喻、人物尺度、復古印刷質感和編輯構圖；平台適配、長文提煉、語言模式、檔案保存與生圖工具呼叫由 `punk-cover` 負責。

## Use For

- AI、自動化、資訊過載、知識流動、組織系統、媒體、檔案、工作方式和技術改變社會的主題
- 需要把抽象議題轉化為“一個巨型系統正在處理某種東西”的文章、X 頭圖、微信公眾號封面、影片封面和海報
- 未來城市、公共基礎設施、科學傳播、太空時代想象、工業流程和檔案敘事

## Avoid

- 只需要極簡文字、純幾何、純攝影、現代 SaaS 產品介面或直接賽博朋克氣質的任務
- 必須相依多個互不相關的圖標、功能卡片、人物肖像或產品截圖才能成立的主題
- 無法收束為一個系統、一個流動過程、一個人類動作和一個核心隱喻的內容
