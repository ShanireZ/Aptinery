# 構圖詳表 17–32：分區、網格、圖文與密度

以下詳細提示詞中的色彩、字體、材質、電影感及平面／編輯風格詞，是為忠實保留源文而收錄的示例；只有使用者或上游提供相應風格時才攜帶，否則只保留構圖結構並將風格欄位參數化或省略，不得自行選擇外部 style atom。

本表用於多類資訊共存、精確網格、圖文主次、連續畫幅和實驗構圖。圖像模型只能把網格當作結構趨勢；HTML/CSS 應把欄數、行數、跨度、溝槽、對齊線和裁切焦點直接編碼。

表中的 `3:4`、`4×6`、`5 栏`、`62/38`、具體溝槽和跨度都是可調的起始示例，不是不可變規範。按使用者給定畫幅、內容量、最小字號、最小單元寬度、裁切安全和媒介約束調整，並在交付中說明實際採用的值。

## 17｜上下分屏 Horizontal Split

用水平分界把圖像與文字或兩個場景疊放，天然形成先後和上下文關係。

- 視線路徑：通常從上方主視覺下落到下方解釋，也可反向用文字引出圖像。
- 適合：電影、旅行、講座、產品說明、資料 + 圖像。
- 避坑：分界不要卡在主體臉部或文字中線；上下比例體現主次。
- 標籤：`上下分屏` `地平线分割` `图文两层` `horizontal split` `stacked panels` `image-text division`

圖像模型提示：

```text
3:4 竖版海报，使用上下分屏构图：上方约 62% 为主视觉[对象/场景]，下方 38% 为纯色信息区，承载标题“[主标题]”、日期和说明；分界线清晰并与图像地平线或结构线呼应。避免分界切过关键主体。
Keywords: horizontal split composition, stacked panels, image-text division, 62/38 layout.
```

HTML/CSS 提示：

```text
容器 display:grid，grid-template-rows:62% 38%；图像区 overflow:hidden + object-fit:cover；信息区用内部 2 列网格；标题可轻微跨越分界但须有对比底。
```

## 18｜水平帶狀 Horizontal Bands

用多個橫向色帶或內容帶分層，產生節拍、章節感與橫向速度。

- 視線路徑：從最強色帶開始，按頻寬、顏色或編號逐層移動。
- 適合：音樂、交通、體育、時間表、系列活動、資訊密集海報。
- 避坑：每條帶不能同等搶眼；避免把段落擠成過窄行長。
- 標籤：`水平色带` `分层条带` `章节节奏` `horizontal bands` `striped layout` `stacked information bars`

圖像模型提示：

```text
竖版海报由 4–6 条宽度不等的水平内容带构成；主标题“[主标题]”占最宽且对比最强的一带，主视觉[对象]跨越相邻两带，日期、地点、编号分布在较窄带中；形成节拍与横向速度。避免所有条带等宽等强。
Keywords: horizontal band composition, striped layout, stacked information bars, rhythmic widths.
```

HTML/CSS 提示：

```text
使用 grid-template-rows:10% 24% 12% 36% 18% 等不等比例；每一带设置独立背景与对齐；主视觉通过 grid-row 跨带；文本行高随带高用 clamp() 调整。
```

## 19｜單欄手稿網格 Single-Column Grid

所有資訊落在一個連續主欄中，靠邊距、段落間距與字號建立清晰閱讀秩序。

- 視線路徑：從欄頂到欄底線性閱讀，把內容當成一篇短文字。
- 適合：宣言、文學、學術、演講、極簡產品說明。
- 避坑：海報不是論文頁；行長、段落數和字號必須適合遠讀。
- 標籤：`单栏网格` `线性阅读` `大边距` `single-column grid` `manuscript grid` `linear reading`

圖像模型提示：

```text
竖版文字海报，使用单栏手稿网格：一条窄而明确的主栏贯穿页面，标题“[主标题]”在栏顶占 2–4 行，短正文与日期沿同一左边线向下排列；四周大边距、基线节奏一致、安静理性。避免长段小字和过宽行长。
Keywords: single-column grid, manuscript grid, linear reading, generous margins.
```

HTML/CSS 提示：

```text
海报内部 max-inline-size:62%，margin-inline:auto；display:flex; flex-direction:column；所有文本共用左边线；正文 max-width:28ch，使用固定 line-height 建立基线节奏。
```

## 20｜多欄編輯網格 Multi-Column Grid

多條縱向欄提供靈活跨度，圖像與文字可佔一欄或跨欄，適合複雜資訊層級。

- 視線路徑：大跨欄元素先定級，再按欄線讀取細分資訊。
- 適合：編輯海報、會議、課程表、展覽目錄、資料與說明。
- 避坑：不要讓所有元素佔不同的隨機跨度；重複欄寬和溝槽。
- 標籤：`多栏网格` `跨栏` `编辑布局` `multi-column grid` `column span` `editorial layout`

圖像模型提示：

```text
3:4 竖版编辑海报，建立 4 栏等宽网格与清晰沟槽；标题“[主标题]”跨 3 栏，主视觉[对象]跨 2–4 栏，日期和说明分别占 1 栏；通过跨栏数量建立层级，左对齐、节奏严谨。避免每个元素随机跨栏。
Keywords: multi-column grid, editorial layout, column span, consistent gutters.
```

HTML/CSS 提示：

```text
display:grid; grid-template-columns:repeat(4,1fr); column-gap:clamp(8px,2vw,20px)；标题 grid-column:1/4，主视觉可用 2/5，元信息各占 1 栏；统一使用网格线编号。
```

## 21｜模組網格 Modular Grid

縱欄與橫行交叉成可重複使用模組，圖像、文字和編號按模組組合，適合高密度系統化資訊。

- 視線路徑：先看跨模組的大元素，再按模組群組掃描局部資訊。
- 適合：瑞士風格、資訊設計、活動日程、展覽、系列視覺。
- 避坑：網格是底層關係，不必把每條線都畫出來。
- 標籤：`模块网格` `矩阵` `跨模块` `modular grid` `matrix layout` `grid modules`

圖像模型提示：

```text
竖版信息海报，使用 4 列 × 6 行模块网格；标题“[主标题]”跨 3×2 模块，主视觉[对象]占 2×3 模块，编号和详情填入较小模块；重复边距与沟槽，系统感强，可局部越界形成层级。不要显示全部辅助线。
Keywords: modular grid, matrix layout, spanning modules, systematic hierarchy.
```

HTML/CSS 提示：

```text
display:grid; grid-template-columns:repeat(4,1fr); grid-template-rows:repeat(6,1fr); gap:10px；用 grid-area 明确每个内容块；调试态显示网格，发布态仅保留少量分隔线。
```

## 22｜瑞士非對稱網格 Swiss Grid

嚴格網格、左對齊無襯線字、非對稱留白與客觀攝影共同形成清晰理性的國際主義語氣。

- 視線路徑：大字號無襯線標題進入，沿左對齊線和模組關係讀取。
- 適合：設計展、建築、音樂會、文化機構、理性科技品牌。
- 避坑：加紅圓和 Helvetica 不等於瑞士風格；關鍵是結構與層級。
- 標籤：`瑞士风格` `左齐右不齐` `客观排印` `Swiss style` `International Typographic Style` `flush left ragged right`

圖像模型提示：

```text
竖版文化海报，采用瑞士国际主义非对称网格：无衬线标题“[主标题]”左齐右不齐，严格对齐到 4–6 栏网格；一个高对比几何形或客观主视觉偏置放置，红/黑/米白克制配色，信息清晰、功能优先。避免居中排满、避免把装饰当结构。
Keywords: Swiss grid, International Typographic Style, flush left ragged right, asymmetric grid.
```

HTML/CSS 提示：

```text
建立 6 栏网格；所有文本 text-align:left，主标题跨 4 栏，元信息占 2 栏；用单一强调色与 1px 规则线；字体使用系统无衬线并限制字重数量。
```

## 23｜層級卡片網格 Bento / Hierarchical Grid

不同尺寸的矩形區塊共享統一間距與圓角，通過卡片面積表達資訊優先級。

- 視線路徑：最大卡片先讀，隨後按相鄰關係在小卡片間跳轉。
- 適合：科技、產品功能、資料、服務組合、HTML 完成實作頁。
- 避坑：不是隨意拼方塊；同層卡片需要一致語義和間距。
- 標籤：`Bento 网格` `层级卡片` `不等模块` `bento grid` `hierarchical cards` `variable-span grid`

圖像模型提示：

```text
竖版科技海报，使用 Bento 层级卡片网格：最大卡片承载主标题“[主标题]”与主视觉[对象]，3–5 个较小卡片承载卖点、数字、日期和 CTA；卡片跨度不等但沟槽一致，信息像仪表盘一样清晰。避免十几个同权小格。
Keywords: bento grid, hierarchical cards, variable-span modules, dashboard composition.
```

HTML/CSS 提示：

```text
display:grid; grid-template-columns:repeat(4,1fr); grid-auto-rows:1fr；主卡 grid-column:span 3; grid-row:span 3，副卡使用 span 1/2；统一 gap、border-radius 与内边距 token。
```

## 24｜棋盤交替 Checkerboard

圖像與文字在規則矩陣中交替出現，利用反轉、重複和對應關係形成節奏。

- 視線路徑：在深淺或圖文單元間跳讀，整體先於局部被感知。
- 適合：系列產品、作品集、活動陣容、對照概念、時尚。
- 避坑：矩陣過細會像社交媒體九宮格；需要一個破格焦點。
- 標籤：`棋盘` `图文交替` `反转节奏` `checkerboard layout` `alternating tiles` `image-text rhythm`

圖像模型提示：

```text
竖版海报使用 3×4 棋盘式模块，图像、色块与文字交替出现；标题“[主标题]”占据或打破其中 2–3 个相邻格，其他格维持深浅反转与重复节奏；整齐但有一个明确破格焦点。避免所有格同等复杂。
Keywords: checkerboard composition, alternating tiles, image-text rhythm, one deliberate break.
```

HTML/CSS 提示：

```text
使用 3 列 × 4 行网格；通过 :nth-child(even) 反转前景/背景；主标题块 grid-column:span 2。小屏仅在每格满足最小单元宽度、最小字号和可读行长时保留 3 列；否则减少列数或顺序重排，同时保留图文交替、对应关系、语义 DOM 顺序和主焦点。
```

## 25｜滿版主視覺 Full-Bleed Hero

單張圖像鋪滿畫布，文字疊加或放入局部安全區，以情緒與沉浸感優先。

- 視線路徑：先感受整體圖像，再由高對比標題進入具體資訊。
- 適合：電影、旅行、時尚、攝影、產品氛圍、人物。
- 避坑：文字不能壓在複雜紋理上；裁切焦點需要跨尺寸管理。
- 標籤：`满版图像` `沉浸主视觉` `文字叠图` `full-bleed image` `hero image` `type overlay`

圖像模型提示：

```text
3:4 竖版海报，一张高质感主视觉[场景/对象]满版铺设并延伸到四边；标题“[主标题]”放在图像中低纹理、高对比的安全区域，辅文控制在一个紧凑信息簇；电影感、沉浸、裁切明确。避免文字压在主体脸部或杂乱纹理上。
Keywords: full-bleed hero image, immersive poster, type overlay, controlled crop.
```

HTML/CSS 提示：

```text
容器内 img 使用 position:absolute; inset:0; width:100%; height:100%; object-fit:cover；用 object-position 自定义焦点；增加局部渐变遮罩而非整图变暗；文字置于安全区并设置 max-width。
```

## 26｜大字主導 Typographic Dominant

把標題本身當作主視覺，靠尺度、字重、字距、斷行和裁切建立圖像感。

- 視線路徑：先識別巨型關鍵詞，再在字形縫隙或邊緣找到細節資訊。
- 適合：觀點、宣言、音樂、促銷、社會議題、無圖素材。
- 避坑：大字不等於全部加粗；斷行必須保留語義與辨識度。
- 標籤：`大字海报` `字体主视觉` `超尺度标题` `big type poster` `typographic dominant` `oversized headline`

圖像模型提示：

```text
竖版纯文字海报，让标题“[主标题]”成为唯一主视觉，使用超大无衬线或展示字体，占画面 60%–85%，允许部分字形越界裁切；副标题、日期以极小字号贴合字形空隙；高对比、强节奏。避免随机断词、避免过多字体。
Keywords: big type poster, typographic dominant composition, oversized headline, cropped letterforms.
```

HTML/CSS 提示：

```text
标题使用 font-size:clamp(72px,24vw,260px)、line-height:.78、letter-spacing:-.07em；容器 overflow:hidden；用 max-inline-size 与手动 <br> 控制断行，元信息绝对定位到负空间。
```

## 27｜圖上疊字 Type over Image

文字與圖像共享同一空間，通過遮擋、穿插和對比建立一體化主視覺。

- 視線路徑：圖像與標題幾乎同時進入，再通過前後層級辨認關係。
- 適合：時尚、人像、雜誌、電影、音樂、文化活動。
- 避坑：明確字在前、字在後或字穿插；半透明一蓋了之通常發灰。
- 標籤：`图上叠字` `图文穿插` `前后层级` `type over image` `interleaved typography` `foreground-background layering`

圖像模型提示：

```text
竖版海报，主视觉[人物/对象]占据中央，超大标题“[主标题]”跨越图像；让部分字在主体前、部分字被主体遮挡，形成明确的图文穿插与空间层级；文字仍可读，边缘干净。避免整行半透明文字、避免遮住脸和关键信息。
Keywords: type over image, interleaved typography, foreground-background layering, editorial poster.
```

HTML/CSS 提示：

```text
建立背景文字层、图像层、前景文字层三个 z-index；同一标题使用两个视觉副本，但只保留一个可访问副本，并给装饰副本 aria-hidden="true"；主体可用透明 PNG 或 clip-path，避免仅靠 opacity。
```

## 28｜雙聯／三聯 Diptych / Triptych

把一個主題拆成兩個或三個連續畫幅，利用重複與變化表現時間、對比或多視角。

- 視線路徑：從第一畫幅橫向或縱向移動，在相似結構中比較變化。
- 適合：敘事、前後、系列產品、人物組、電影、攝影展。
- 避坑：每格要有共同變數；三張無關圖片並排不構成三聯。
- 標籤：`双联` `三联` `连续画幅` `diptych` `triptych` `sequential panels`

圖像模型提示：

```text
竖版海报分成三个连续窄画幅，分别呈现[同一主题]的三个时刻/视角/状态；三格裁切、色调与视平线保持共同规则，标题“[主标题]”跨越三格或置于统一底栏；重复中有变化。避免三张无关图片简单拼接。
Keywords: triptych composition, sequential panels, repeated framing, variation within a system.
```

HTML/CSS 提示：

```text
使用 grid-template-columns:repeat(3,1fr) 与统一 gap；每格 img 使用相同 aspect-ratio、object-position 规则；标题可 grid-column:1/-1；用 data-state 标记三个状态。
```

## 29｜拼貼層疊 Overlapping Collage

圖像、紙片、紋理和文字以遮擋與旋轉疊加，製造手動、記憶與亞文化語氣。

- 視線路徑：從最高對比層進入，在遮擋邊緣間跳讀，依靠層級而非網格推進。
- 適合：音樂、青年文化、雜誌、藝術、復古、手動品牌。
- 避坑：隨機旋轉不是拼貼；需要統一的材質、色彩或敘事線索。
- 標籤：`拼贴` `层叠` `撕纸` `遮挡` `overlapping collage` `torn paper` `layered ephemera`

圖像模型提示：

```text
竖版拼贴海报，用 4–7 层照片、撕纸、色块、印章与标题“[主标题]”相互遮挡，角度控制在少数几个方向；保持一个主图层最大、其他层辅助，统一纸张颗粒与有限配色。避免每层同等抢眼、避免无主题素材堆砌。
Keywords: overlapping collage, torn paper layers, controlled rotation, layered ephemera.
```

HTML/CSS 提示：

```text
容器 position:relative；每层 absolute + transform:translate/rotate，旋转角度限定为 -8deg/0deg/6deg；用 box-shadow、mix-blend-mode 谨慎模拟纸层；明确 z-index token。
```

## 30｜破格網格 Broken Grid

先建立可感知的網格，再讓少數關鍵元素跨線、錯位或越界，以破壞製造強調。受控破格通常由一個主破格元素或焦點簇承擔；源文示例中的標題和主視覺可以是服務同一層級的兩個相關破格。

- 視線路徑：規則網格建立預期，破格元素因違背預期成為焦點。
- 適合：先鋒文化、設計展、科技、實驗編輯、作品集。
- 避坑：沒有底層網格就沒有破格；每個元素都錯位只會混亂。
- 標籤：`破格网格` `跨线` `错位` `控制性破坏` `broken grid` `intentional misalignment` `grid disruption`

圖像模型提示：

```text
竖版实验海报，先建立清晰的 5 栏网格与重复对齐线，再让标题“[主标题]”跨出两条栏线、主视觉[对象]越过一个模块边界；两者形成一个相关焦点簇，其余信息严格归位，用少量控制性错位制造焦点。避免所有元素随机漂浮。
Keywords: broken grid, intentional misalignment, controlled disruption, visible underlying structure.
```

HTML/CSS 提示：

```text
底层使用 5 栏 Grid；约 80% 元素遵守 grid lines，主破格元素或相关焦点簇通过 grid-column 跨栏并 translateX(8%–15%)；避免全部使用 absolute；调试时显示网格覆盖层。
```

## 31｜重複節奏 Repetition & Pattern

重複同一形狀、圖像或文字建立節拍，再以一個差異項形成焦點。

- 視線路徑：先感知整體模式，隨後立刻捕捉破例元素。
- 適合：系列產品、群體、音樂、運動、資料、概念傳播。
- 避坑：重複項過多且無變化會成為背景噪聲；差異必須服務主題。
- 標籤：`重复` `模式` `节奏` `破例焦点` `repetition` `pattern` `one anomaly` `rhythmic grid`

圖像模型提示：

```text
竖版海报，以同一[形状/对象/词语]按规则阵列重复 12–30 次，保持相同间距与尺度；其中一个元素用颜色、方向或大小打破模式，并与标题“[主标题]”建立关系；整体节奏强、焦点明确。避免多个同时破例。
Keywords: repetition and pattern, rhythmic grid, one anomaly, pattern interruption.
```

HTML/CSS 提示：

```text
使用 CSS Grid + repeat(auto-fit,minmax()) 生成阵列；所有单元继承统一样式，仅用 .is-anomaly 改一个变量；标题与异常单元共享 accent color。
```

## 32｜密集全鋪 Dense All-Over

高密度元素覆蓋整個畫面，通過整體紋理、局部對比與多尺度層級製造最大主義衝擊。

- 視線路徑：先感知整體密度，再由最大尺度或最強色差的元素抓住局部入口。
- 適合：節日、地下音樂、潮流、復古廣告、陣容很多的活動。
- 避坑：密集不等於沒有層級；標題、日期與 CTA 仍需至少一個清晰入口。
- 標籤：`密集全铺` `最大主义` `多尺度` `纹理化信息` `dense all-over` `maximalist poster` `horror vacui` `multi-scale hierarchy`

圖像模型提示：

```text
竖版最大主义海报，图形、纹理、短词和信息密集覆盖整个画面，但保留明确多尺度层级：超大标题“[主标题]”为入口，中型主视觉[对象]为第二层，小字与图案形成底层纹理；使用有限色盘统一复杂度。避免所有元素同尺寸、避免关键日期不可读。
Keywords: dense all-over composition, maximalist poster, multi-scale hierarchy, controlled visual density.
```

HTML/CSS 提示：

```text
使用多层 CSS Grid/absolute 混合：背景 pattern 层、信息矩阵层、超大标题层；限定 3 个字号级别与 4 色以内；为关键文字设置实色底或 outline，保证 WCAG 对比。
```
