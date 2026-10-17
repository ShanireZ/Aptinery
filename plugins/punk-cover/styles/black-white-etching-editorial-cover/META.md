# 黑白復古蝕刻版畫封面

```yaml
id: black-white-etching-editorial-cover
name: 黑白复古蚀刻版画封面
input_modes: [text, image]
subjects: [concept, typography, object, scene, mechanism, surreal_editorial]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [标题或主题, 核心意思]
optional_fields: [画幅比例, 视觉方向, 副标题, 输出尺寸, 输出模式, 用途, 语言, 文字模式, 情绪倾向, 必须出现, 禁止出现]
source: styles/black-white-etching-editorial-cover/STYLE.md
style_anchors:
  - strict black, white, and line-made gray values with strong tonal contrast
  - 19th-century copperplate engraving, etching, wood engraving, and antique scientific-illustration marks
  - fine parallel hatching, cross-hatching, stippling, engraved contours, and visible handmade print texture
  - one dominant conceptual or surreal editorial metaphor rather than a literal keyword collage
  - clear silhouette and visual center from a distance, with dense craft detail revealed up close
  - intentionally uneven information density: refined focal detail, simplified support areas, and controlled pure-black fields
cover_shape_adaptation:
  - let the ratio determine the scene, perspective, subject scale, and reading path; never crop or stretch a finished composition
  - use wide ratios for environmental narrative and horizontal motion, portrait ratios for vertical scale and descent/ascent, and square ratios for a concentrated emblematic encounter
  - if text is requested, render the complete title as restrained engraved editorial type integrated into the print; if the user explicitly requests a pure-image cover or `文字模式: 无文字`, use the title only to guide the metaphor and do not render text
  - preserve one strong visual memory point while allowing the metaphor, viewpoint, scale, material, quantity, and physical logic to change from cover to cover
must_preserve:
  - monochrome print language with no color accents, neon, glow, or smooth digital gradients
  - one legible core silhouette and one primary metaphor with a clear spatial relationship
  - authentic engraved marks: hatching, cross-hatching, stippling, etched contours, and tactile paper/ink irregularity
  - high contrast, deliberate negative space, and non-uniform detail density
  - a restrained, mysterious, rational, philosophical, and surreal editorial temperament
avoid_when_applying_to_cover:
  - obvious modern 3D rendering, plastic surfaces, glossy CGI, cheap cyberpunk, or generic AI concept-art polish
  - keyword-object piles, multiple unrelated symbols, stock illustration composition, or decorative filler
  - flat black-and-white vector art, comic-book inking, smooth airbrush shading, watercolor, or colored printmaking
  - unreadable title lettering, fabricated editorial filler, excessive small text, logos, watermarks, grids, contact sheets, or e-commerce layout
```

## Style Intent

把標題、主題和核心意思轉譯成一張具有強烈概念感的純黑白封面。畫面借用十九世紀銅版畫、蝕刻版畫、木口木刻、古典科學插圖和超現實編輯插畫的視覺語法：灰階不相依數字漸變，而由排線、交叉排線、點描和雕刻線條生成。該 style 負責版畫媒介、概念隱喻、黑白層次、構圖密度和氣質；平台適配、標題提煉、檔案保存與生成工具呼叫由 `punk-cover` 負責。

## Use For

- 哲學、批判性觀點、未來議題、機制解釋、社會觀察和具有思考感的主題
- 需要一眼形成視覺懸念、細看發現敘事關係的編輯封面、書封和展覽海報
- 使用者已指定黑白、復古蝕刻、銅版畫、木刻、古典科學插圖或超現實版畫方向的封面
- 需要把抽象矛盾轉化成一個場景、動作、尺度關係、空間結構或物理隱喻的內容

## Avoid

- 相依彩色品牌識別、攝影寫實、產品介面或複雜資訊圖才能成立的任務
- 必須同時展示多個同等重要主體、步驟或資料關係的內容
- 需要霓虹、發光、光滑 3D、賽博朋克、卡通或鮮豔商業廣告質感的內容

## Visual Translation

- 先理解主題真正要表達的觀點、矛盾、關係或問題，再選擇一個能承載它的畫面，而不是把名詞逐個畫成物件。
- 優先使用一個強核心概念。人物、環境、建築、機械、生物、自然、抽象結構或超現實空間都可以成為主體，但必須服務於同一條視覺敘事。
- 可以改變現實中的尺度、數量、空間、方向、功能、材質、位置和因果邏輯，讓熟悉的事物產生陌生感；只要視覺關係仍然能回扣核心意思。
- 避免機械套用機器人、芯片、大腦、書本等慣用符號。是否使用某個元素由具體內容決定。

## Engraved Print Language

- 畫面固定為純黑、純白和由黑白線條形成的灰階。不要出現任何彩色、棕褐色、藍色或局部染色。
- 使用細密平行排線表現平面和方向，用交叉排線建立深色體積，用點描處理霧、皮膚、石材、紙張和遠景，用粗細變化的雕刻線勾勒結構與輪廓。
- 線條要有銅版雕刻和手動印刷留下的微小不均勻：局部斷裂、墨量變化、紙面顆粒、輕微套印誤差都可以存在，但不能變成髒亂噪點。
- 明暗應有清晰的黑白對照。允許大面積純黑作為背景、洞口、陰影或未知區域，也允許主體附近出現極高密度的精細版畫細節。
- 材質通過線條方向、密度、間距、斷續和刻痕來區分，不使用塑料高光、平滑漸變或照片濾鏡。

## Composition and Density

- 先建立遠看可識別的整體輪廓、視覺中心和主次關係，再把近看細節集中到主體、動作、關鍵結構或隱喻發生的位置。
- 根據目標比例重新設計空間：橫向畫幅適合展開環境敘事、水平運動和左右關係；縱向畫幅適合巨大主體、深井、上升、墜落和垂直尺度；方形畫幅適合集中衝突、局部特寫和象徵性構圖。
- 讓不同區域擁有不同資訊密度。主體和關鍵區域精細刻畫，次要區域適當簡化、淡出或留黑，不要把每個角落平均填滿。
- 可以使用中心、偏心、對稱、非對稱、俯視、仰視、平視、強透視、近景或遠景，但必須保持一個明確的視覺主軸。
- 不要為了“豐富”堆放第二套符號系統。輔助元素只有在幫助理解空間、動作或主題關係時才出現。

## Title and Pure-Image Mode

- 標題、主題和核心意思先作為創作輸入，幫助確定畫面敘事和視覺隱喻。
- 只有在使用者要求文字封面、提供文字模式或 `punk-cover` 的平台任務需要標題時，才把文字納入畫面；文字應像版畫中的編輯標題、圖注或刻印標識，和主體共享同一套黑白紙墨質感。
- 當使用者明確要求“純圖封面”或“無文字”，禁止加入標題、解釋句、標籤、品牌、頁碼或偽造的小字；畫面只用視覺關係表達主題。
- 文字模式未明確時，遵循 `punk-cover` 的通用標題可讀性要求，不讓蝕刻紋理破壞標題識別，不用大段小字填充空白。

## Atmosphere and Final Standard

整體保持克制、神秘、深邃、理性、超現實和具有思考感，可根據主題進一步偏向宏大、孤獨、壓迫、未知、荒誕、詩意、冷靜、莊嚴或探索感。最終畫面應介於編輯插畫、哲學書籍插圖、復古科學版畫和超現實藝術之間：遠看輪廓清晰、黑白關係有力；近看排線、點描、刻痕和紙墨紋理豐富；畫面乾淨有秩序，概念明確但不把答案全部說盡。

不要輸出分析、解釋、備選方案、網格、拼圖、聯繫表或多張成圖。每個目標比例只生成一張獨立最終封面。
