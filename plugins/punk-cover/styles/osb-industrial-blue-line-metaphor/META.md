# OSB 工業藍線條隱喻

```yaml
id: osb-industrial-blue-line-metaphor
name: OSB 工业蓝线条隐喻
input_modes: [text]
subjects: [concept, relationship, action, object, typography, line_art]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [主题, 主标题, 画幅比例, 用途]
optional_fields: [副标题, 禁止元素]
source: styles/osb-industrial-blue-line-metaphor/STYLE.md
style_anchors:
  - full-bleed front-facing authentic warm honey OSB board with irregular compressed wood strands and optional tiny black corner screws
  - one exact industrial blue selected from #087FBE, #007FC4, or #006FC0 and reused consistently for all text, lines, and graphics
  - heavy geometric sans-serif title fixed in the upper-left as matte acrylic or thin metal signage with minimal contact shadow
  - one simplified continuous-line metaphor in the lower or lower-right area using no more than three core graphic elements
  - at least 55 percent visible board negative space and no more than 30 percent line-art area
cover_shape_adaptation:
  - preserve the upper-left title and lower-right metaphor balance across every ratio while recomposing scale, line path, and whitespace
  - landscape formats should use a long horizontal or diagonal visual path across generous board space
  - square formats should shorten the path while keeping clear corner-to-corner balance and one focal relationship
  - vertical formats should redirect the line downward toward the lower-right without crowding the title or reducing negative space
must_preserve:
  - authentic OSB strand-board material rather than generic wood, plywood, cork, paperboard, or smooth furniture
  - one unified industrial blue and one coherent line language across title and metaphor
  - exact readable user-provided text only, with no fabricated labels, numbers, English, dates, brands, logos, or watermarks
  - one core concept, no more than three core graphic elements, line-art area at or below 30 percent, and negative space at or above 55 percent
avoid_when_applying_to_cover:
  - room, wall, desk, people, environmental context, realistic scene, cartoon stickers, photos, screenshots, UI, flowcharts, or infographics
  - real or colored logos, traced trademarks, stock icons, multiple icon sets, dense small symbols, or several competing metaphors
  - neon, glow, gradient, liquid text, mirrored metal, strong 3D extrusion, colored lighting, hard shadows, or decorative clutter
  - inconsistent blue shades, extra text, random English, fabricated metadata, mechanical cropping, stretching, or padding
```

## Style Intent

以真實 OSB 刨花板的天然粗糲紋理承載一組高度理性的工業藍標識字與連續線隱喻，通過左上標題、右下圖形和大面積木板留白表達一個核心關係、動作或結果。該 style 負責固定材質、顏色、字體物性、線稿語言、構圖錨點和留白比例；平台確認、文章摘要、檔案保存和生成工具呼叫由 `punk-cover` 負責。

## Use For

- 職場、組織、效率、關係、工具、方法、連接、阻力、流程變化和抽象觀點
- 文章封面、X 或社交媒體封面、影片封面、建築或創意工作室風海報
- 能壓縮成一條路徑、一個連接關係或一個結構變化的主題
- 需要粗糲真實材質與現代工業導視秩序形成反差的內容

## Avoid

- 相依人物故事、產品攝影、複雜場景、資料圖表或大量正文才能成立的主題
- 需要真實品牌 Logo、軟體截圖、彩色圖標或多步驟流程圖的內容
- 無法保留大面積留白、左上標題或單一藍色線稿隱喻的密集排版任務
