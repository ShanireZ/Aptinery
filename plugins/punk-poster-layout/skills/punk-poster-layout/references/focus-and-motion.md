# 構圖詳表 01–16：焦點、平衡、幾何與動勢

以下詳細提示詞中的色彩、字體、材質、電影感及平面／編輯風格詞，是為忠實保留源文而收錄的示例；只有使用者或上游提供相應風格時才攜帶，否則只保留構圖結構並將風格欄位參數化或省略，不得自行選擇外部 style atom。

本表用於單一主角、強符號骨架、明確視線路徑和雙區域分割。每項都提供圖像模型與 HTML/CSS 的結構表達；替換方括號內容，並把所選條目融合進完整任務提示詞。

表中的 `3:4`、`5×6`、欄數、比例、偏移和具體尺寸都是可調的起始示例，不是不可變規範。按使用者給定畫幅、內容量、最小字號、最小單元寬度、裁切安全和媒介約束調整，並在交付中說明實際採用的值。

## 01｜中軸對稱 Axial Symmetry

所有主要元素圍繞一條中軸組織，左右視覺重量接近，產生莊重、穩定與儀式感。

- 視線路徑：上方標題 → 中央主視覺 → 底部資訊；沿中軸下行。
- 適合：品牌發佈、展覽、奢侈品、典禮、單一主角。
- 避坑：不要機械鏡像每個小元素；資訊很多時容易僵硬。
- 標籤：`中轴` `镜像平衡` `中央焦点` `庄重` `axial symmetry` `centered composition` `mirrored balance`

圖像模型提示：

```text
竖版 3:4 海报，主题为[主题]。
采用中轴对称构图：主标题“[主标题]”居上且居中，主视觉[对象]精确落在垂直中轴，副标题、日期与署名沿中线分层排列；左右视觉重量近似镜像，边距与留白均衡；高对比、清晰三层层级、平面设计。避免多焦点、随机偏移和无意义装饰。
Keywords: axial symmetry, centered composition, mirrored balance, central focal point.
```

HTML/CSS 提示：

```text
使用 aspect-ratio:3/4 的海报容器；display:grid，单列三行，place-items:center；用 ::before 绘制可隐藏的垂直中轴；标题、主视觉、元信息都以 inline-size 居中约束；左右 padding 相同。
```

## 02｜非對稱平衡 Asymmetrical Balance

左右形狀不同，但通過大小、明度、密度與距離交換視覺重量，形成有張力的穩定。

- 視線路徑：大形體先進入，小而高對比的資訊塊在另一側完成配重。
- 適合：文化海報、設計展、時尚、科技、當代品牌。
- 避坑：偏左不等於平衡；另一側必須有足夠對比或密度回應。
- 標籤：`非对称` `视觉配重` `偏置焦点` `动态稳定` `asymmetrical balance` `visual counterweight` `offset focal point`

圖像模型提示：

```text
竖版海报，主题[主题]，采用非对称平衡构图。将大尺度主视觉[对象]偏置于画面一侧，在对侧以更小但更高对比的标题“[主标题]”和信息组完成视觉配重；对齐线清晰、留白不等量但视觉重量稳定，现代编辑设计感。避免随意散落、两侧同等抢眼。
Keywords: asymmetrical balance, visual counterweight, offset focal point, dynamic equilibrium.
```

HTML/CSS 提示：

```text
使用 5×6 隐形 CSS Grid；主视觉跨 3 列 4 行，文本块占对角侧 2 列；通过 clamp() 控制尺度差，使用 align-self:end 与 justify-self:start 制造偏置；保留一条共同对齐线。
```

## 03｜三分法焦點 Rule of Thirds

把畫面橫豎各分三份，將焦點放在分割線或交點附近，兼顧穩定與自然偏移。

- 視線路徑：先到三分交點的主視覺，再沿分割線進入標題和資訊。
- 適合：攝影主導海報、人物、產品、活動、網頁 Hero。
- 避坑：不要為卡交點犧牲主體朝向、文字空間或裁切。
- 標籤：`三分法` `交点焦点` `偏心留白` `rule of thirds` `thirds intersection` `off-center subject`

圖像模型提示：

```text
3:4 竖版海报，使用三分法构图。将主视觉[对象]的视觉中心放在右上三分交点附近，标题“[主标题]”沿左侧三分线对齐，保留与主体视线方向一致的大块留白；信息层级清楚、裁切有意图。避免把所有内容塞进交点、避免边距失衡。
Keywords: rule of thirds, thirds intersection, off-center focal point, directional negative space.
```

HTML/CSS 提示：

```text
容器使用 3 列 × 3 行 CSS Grid；主视觉以 grid-column:2/4、grid-row:1/3 定位，标题沿第 1 条纵向分割线对齐；调试时用 repeating-linear-gradient 显示三分线，完成后关闭。
```

## 04｜黃金螺旋 Golden Spiral

以逐級縮小的矩形與弧線組織焦點和節奏；把它作為比例草圖，而不是必須服從的美學定律。

- 視線路徑：從寬闊區域沿弧線逐漸收緊，最終落到內圈焦點。
- 適合：藝術、自然主題、電影、敘事型產品、概念海報。
- 避坑：不要把螺旋線貼在成品上；內容層級仍優先。
- 標籤：`黄金螺旋` `比例递进` `收束焦点` `golden spiral` `Fibonacci layout` `progressive scale`

圖像模型提示：

```text
竖版概念海报，主题[主题]，使用隐性的黄金螺旋组织画面：大面积主视觉从外圈进入，标题“[主标题]”与辅助元素按逐级缩小的比例沿弧形轨迹排列，最终焦点落在内圈的[关键对象]；节奏由宽到紧。不要显示数学辅助线，不要牺牲可读性。
Keywords: golden spiral composition, Fibonacci proportion, progressive scale, converging focal point.
```

HTML/CSS 提示：

```text
使用嵌套的绝对定位矩形，每一级尺寸约为前一级的 61.8%；用 border-radius 与伪元素暗示弧线，内容锚点放在最小矩形附近；把比例做成 CSS 自定义属性，勿硬编码为装饰线。
```

## 05｜大留白單點 Isolated Focal Point

用大面積主動留白隔離一個小而明確的焦點，讓稀疏本身成為語氣。

- 視線路徑：被孤立度直接拉向單點，再讀取附近的少量文字。
- 適合：高端品牌、藝術展、詩歌、香氛、安靜的產品傳播。
- 避坑：留白不是把內容縮小；焦點需要足夠對比、質感或語義。
- 標籤：`大留白` `孤立焦点` `低密度` `克制` `macro white space` `isolated focal point` `minimal composition`

圖像模型提示：

```text
竖版极简海报，主题[主题]。保留 65%–80% 的主动留白，只设置一个小尺度但高辨识度的主视觉[对象]，位于下方或偏心位置；标题“[主标题]”靠近焦点，元信息极少、字号克制；安静、高级、精确。避免把留白填满、避免多个装饰点。
Keywords: macro white space, isolated focal point, low-density layout, restrained typography.
```

HTML/CSS 提示：

```text
使用单一相对定位容器；主视觉 inline-size:18%–28%，绝对定位在 60%–75% 高度；文本与主视觉组成一个小型内容簇，其余区域保持空；设置 generous padding 与 max-width。
```

## 06｜邊緣錨定 Edge-Anchored

將主體推向畫面邊緣並允許裁切，通過屏外延伸感製造尺度與張力。

- 視線路徑：從被裁切的大形體進入，沿其朝向或邊緣移動到文字。
- 適合：時尚、人像、產品特寫、社交媒體封面、強態度傳播。
- 避坑：不要誤裁臉、關節、文字或產品關鍵結構；必須留安全區。
- 標籤：`边缘锚定` `越界裁切` `屏外延伸` `edge-anchored` `cropped subject` `off-canvas continuation`

圖像模型提示：

```text
3:4 竖版海报，将主视觉[对象]锚定在右侧边缘并有意越界裁切，主体约占画面 55%–70%；标题“[主标题]”在相反边缘形成细长信息带，留出明确安全区；产生屏外延伸与大尺度感。避免误切关键部位、避免四边同时拥挤。
Keywords: edge-anchored composition, intentional crop, off-canvas continuation, edge tension.
```

HTML/CSS 提示：

```text
海报容器 overflow:hidden；主视觉 position:absolute，inline-size:70%，inset-inline-end:-16%；文字固定在相反侧安全区；响应式时用 object-position 控制裁切焦点。
```

## 07｜三角／金字塔 Triangular Hierarchy

元素構成穩定三角，頂點負責強調，底邊負責承重，天然適合三層層級。

- 視線路徑：頂點焦點 → 兩側下行 → 底邊資訊，或從底部匯聚到頂點。
- 適合：人物群像、電影、論壇、權威主題、層級明確的發佈。
- 避坑：三角外的元素不能成為更強焦點，否則骨架會塌。
- 標籤：`三角构图` `金字塔层级` `稳定底座` `triangular composition` `pyramid hierarchy` `stable base`

圖像模型提示：

```text
竖版海报，主题[主题]，用稳定的三角/金字塔构图组织[主视觉或人物组]：最高点放置核心对象或标题“[主标题]”，两侧元素向下展开，底边承载日期与地点；三层尺度递减、重心低、整体庄重。避免三角外出现更强焦点。
Keywords: triangular composition, pyramid hierarchy, stable base, apex focal point.
```

HTML/CSS 提示：

```text
用 CSS Grid 3 列 4 行，核心元素置于中列第 1–2 行，次要元素位于左右第 3 行，元信息横跨底行；可用 clip-path:polygon() 绘制辅助三角形。
```

## 08｜倒三角懸置 Inverted Triangle

上寬下窄的倒三角把重量懸在上方，製造不穩定、壓迫、速度或危險感。

- 視線路徑：上方寬區域收束到下方尖點，像漏斗一樣壓向結論。
- 適合：先鋒藝術、音樂、懸疑、警示、反傳統文化活動。
- 避坑：不適合強調可靠與舒適的主題；底部文字避免被尖點擠壓。
- 標籤：`倒三角` `悬置重心` `漏斗收束` `inverted triangle` `unstable balance` `downward convergence`

圖像模型提示：

```text
实验性竖版海报，采用倒三角构图：宽大的标题“[主标题]”与图形占据上半部，向下逐级收窄，最终尖点指向底部的[日期/CTA]；高重心、压迫、紧张、有下坠感。避免底部信息拥挤，避免使用安稳温和的品牌语气。
Keywords: inverted triangle composition, top-heavy balance, downward convergence, suspended tension.
```

HTML/CSS 提示：

```text
顶部内容区宽 100%，中段 66%，底部焦点 20%；用 grid-template-rows 与 justify-self:center 逐级收窄，背景图形使用 clip-path:polygon(0 0,100% 0,50% 100%)。
```

## 09｜同心環繞 Concentric

多箇中心相同的環、框或形狀反覆包圍焦點，強調聚焦、回聲與層層深入。

- 視線路徑：外圈先建立場域，向內層層收束到中心。
- 適合：音樂、科技、聲波、社群、週年、抽象主題。
- 避坑：中心文字與環線錯開；環太多會產生噪聲或眩暈。
- 標籤：`同心` `环绕焦点` `层层收束` `concentric composition` `nested rings` `central convergence`

圖像模型提示：

```text
竖版海报，围绕中央[主视觉]使用 4–7 层同心圆或同心框，尺寸与线宽有节奏变化；标题“[主标题]”置于中心或切入其中一层，辅助信息沿外环分布；形成聚焦、声波、回声感。避免环线遮挡文字、避免所有环同样粗。
Keywords: concentric composition, nested rings, central convergence, rhythmic intervals.
```

HTML/CSS 提示：

```text
海报使用 place-items:center；创建多个绝对定位元素，inset 按等比递增，border-radius:50% 或矩形；用 CSS 变量控制每环尺寸、线宽与透明度；文字层 z-index 最高。
```

## 10｜框中框 Frame within Frame

利用邊框、視窗或嵌套容器反覆限定觀看範圍，形成展陳感和縱深。

- 視線路徑：先識別外框，再穿過內框進入主體，最後讀取框外註解。
- 適合：藝術展、建築、檔案、攝影、復古印刷、畫冊封面。
- 避坑：框線層級不能與文字層級競爭；內框太小會像縮略圖。
- 標籤：`框中框` `嵌套边界` `窗口焦点` `frame within frame` `nested borders` `contained focal area`

圖像模型提示：

```text
竖版文化海报，使用框中框构图：外层细边框定义安全区，中层偏置窗口裁切主视觉[对象]，内层小框锁定标题“[主标题]”；框外保留编号和注释，形成档案与展陈感。避免所有边框同粗、避免边框压迫正文。
Keywords: frame within frame, nested borders, contained focal area, gallery layout.
```

HTML/CSS 提示：

```text
使用三层嵌套容器，每层独立 padding 与 border；中层可偏离中心 4%–8%；主视觉 object-fit:cover；用 outline-offset 而非堆叠 box-shadow 保持边界清晰。
```

## 11｜對角線動勢 Diagonal Tension

強斜軸貫穿畫面，打破水平穩定，快速建立速度、衝突和方向。

- 視線路徑：沿斜軸從一角穿向對角；資訊依附或反向切斷斜軸。
- 適合：體育、音樂、促銷、科技、行動號召、青年文化。
- 避坑：正文不要全部傾斜；斜線必須指向有效資訊而非畫外。
- 標籤：`对角线` `斜轴` `速度` `切割` `diagonal composition` `dynamic axis` `directional tension`

圖像模型提示：

```text
竖版海报，以一条从左下穿向右上的强对角轴组织画面；主视觉[对象]压在线上，标题“[主标题]”沿斜轴或与其形成反向切割，次要信息保持水平以保证可读；高速度、高张力。避免所有文字同时旋转、避免斜轴把视线带离关键信息。
Keywords: diagonal composition, dynamic axis, directional tension, kinetic layout.
```

HTML/CSS 提示：

```text
用 ::before 创建宽色带，position:absolute，transform:rotate(-24deg) scale(1.4)；关键元素沿对角的多个锚点绝对定位；正文保持 transform:none。
```

## 12｜放射爆發 Radial Burst

線條、形狀或人物從共同中心向外輻射，形成能量爆發與集中傳播。

- 視線路徑：中心先被鎖定，隨後向四周擴散，再回到中心文字。
- 適合：音樂節、促銷、慶典、運動、宣言、強情緒活動。
- 避坑：放射中心必須唯一；細密射線會干擾小字號。
- 標籤：`放射` `爆发中心` `向外扩散` `radial burst` `radiating lines` `explosive focal point`

圖像模型提示：

```text
3:4 竖版海报，以[主视觉/标题]为唯一放射中心，使用粗细相间的射线、文字或图形向四周扩散；中心标题“[主标题]”高对比、紧凑，边缘信息较弱；能量强、节庆或宣言感。避免多个放射中心、避免射线穿过小字。
Keywords: radial burst composition, radiating lines, explosive focal point, centrifugal energy.
```

HTML/CSS 提示：

```text
背景使用 repeating-conic-gradient() 生成射线；中心内容用 place-items:center；射线层降低 opacity 并放在文字之下，给中心文字增加纯色底或 isolation:isolate。
```

## 13｜Z 型路徑 Z-Path

用左上、右上、左下、右下四個錨點構成折線路徑，適合少量資訊的順序閱讀。

- 視線路徑：左上標題 → 右上主視覺 → 左下說明 → 右下 CTA。
- 適合：活動、產品頁首屏、課程、發佈會、社交媒體廣告。
- 避坑：Z 只是編排腳手架，不是所有觀眾固定的眼動規律。
- 標籤：`Z 型路径` `四角锚点` `顺序阅读` `Z-pattern layout` `corner anchors` `sequential scan`

圖像模型提示：

```text
竖版信息海报，使用清晰的 Z 型阅读路径：左上放主标题“[主标题]”，右上放主视觉[对象]，左下放简短说明，右下放日期/CTA；用对比、细线或视线方向暗示两条水平线与中间斜线，但不要画出字母 Z。避免四角同等强。
Keywords: Z-pattern composition, corner anchors, sequential visual path, diagonal handoff.
```

HTML/CSS 提示：

```text
使用 2 列 × 2 行网格，四个内容簇分别占四角；用伪元素绘制低对比折线或通过元素朝向建立交接；右下 CTA 设置最高色彩对比但不超过主标题尺度。
```

## 14｜S 型曲線 S-Curve

以柔和的反向曲線連接多個焦點，產生流動、優雅和漸進敘事。

- 視線路徑：從上方一側切入，沿曲線越過中央，最終到達下方另一側。
- 適合：美妝、時尚、舞蹈、自然、飲品、優雅敘事。
- 避坑：不要讓曲線成為無關裝飾；每次轉彎應有資訊節點。
- 標籤：`S 曲线` `蛇形路径` `柔性动势` `S-curve composition` `serpentine flow` `graceful movement`

圖像模型提示：

```text
竖版海报，围绕一条隐性的 S 型曲线安排[主视觉]与 3 个信息节点；标题“[主标题]”在上方入口，中段元素跨越画面中心，日期/CTA 位于下方反侧终点；流动、优雅、连续，空间张弛交替。避免无节点的装饰曲线。
Keywords: S-curve composition, serpentine flow, graceful movement, sequential nodes.
```

HTML/CSS 提示：

```text
用 SVG path 或两个大圆弧伪元素构成 S 曲线；三个内容节点用 absolute + 百分比坐标附着路径；正文保持水平。窄屏或 200% 缩放时，只有在最小字号、裁切安全和交互尺寸仍满足时才整体等比缩放；否则按语义 DOM 顺序重排节点，同时保留入口、转折、终点及相邻关系，不强求同一几何曲线。
```

## 15｜L 型錨定 L-Shaped Anchor

一條豎向與一條橫向資訊帶在角落相交，像支架一樣托住主視覺。

- 視線路徑：沿豎邊下行，在角點轉向橫邊，最後進入被框住的主視覺。
- 適合：建築、展覽、目錄、理性品牌、空間與工業主題。
- 避坑：L 的兩臂需要明顯長短關係；四邊都封閉會變成框中框。
- 標籤：`L 型` `角落锚点` `边栏` `L-shaped layout` `corner anchor` `edge rails`

圖像模型提示：

```text
竖版海报，使用 L 型构图：左侧竖向信息栏与底部横向标题带在左下角相交，形成视觉支架；主视觉[对象]占据右上开放区域，标题“[主标题]”沿底边展开；理性、建筑感、边缘对齐明确。避免四边全部封闭。
Keywords: L-shaped composition, corner anchor, edge rails, open field.
```

HTML/CSS 提示：

```text
容器 grid-template-columns:18% 1fr；grid-template-rows:1fr 18%；竖栏占第 1 列，底栏跨两列，主视觉占右上；文字可用 writing-mode:vertical-rl。
```

## 16｜左右分屏 Vertical Split

畫面垂直分成兩個對等或主次區域，用於對比、問答、前後或雙主題。

- 視線路徑：先讀對比更強的一側，再跨越中縫讀取另一側關係。
- 適合：對比型產品、雙人、前後變化、觀點碰撞、聯名。
- 避坑：兩側必須有明確關係；50/50 分割可能缺乏主次。
- 標籤：`左右分屏` `双主题` `并置对比` `vertical split` `dual-panel composition` `juxtaposition`

圖像模型提示：

```text
竖版海报采用左右分屏构图，左侧呈现[对象 A]，右侧呈现[对象 B]，通过色彩/材质形成鲜明对比；标题“[主标题]”跨越中缝或分别拆分在两侧，设置 60/40 主次比例；强调并置关系。避免两侧毫无关联、避免完全同权导致无焦点。
Keywords: vertical split composition, dual-panel layout, juxtaposition, 60/40 balance.
```

HTML/CSS 提示：

```text
使用 5 列 CSS Grid，左区 3 列、右区 2 列；两侧独立背景与 content wrapper；跨缝标题设置 grid-column:2/5、z-index:2。窄屏时仅在两侧都满足最小单元宽度、最小字号和安全裁切时保留并排；否则可改为上下或顺序分区，但保持 A/B 的语义顺序、对比关系和 60/40 主次。
```
