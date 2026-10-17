# 品牌協同連接

```yaml
id: brand-collaboration-connection
name: 品牌协同连接
input_modes: [text, image]
subjects: [brand, tool, integration, workflow, product, technology, tutorial]
outputs: [cover, poster]
default_ratio: "5:2"
required_fields: [Logo A, Logo B, 主标题, 画幅比例, 语言, 用途]
optional_fields: [副标题, 品牌名称, 补充背景, 情绪倾向, 重点字符, 不想出现的元素]
source: styles/brand-collaboration-connection/STYLE.md
style_anchors:
  - two uploaded logos transformed into soft 3D rounded-square app icons
  - smooth bidirectional gradient connection line with a small center node
  - light gray-white minimal background with generous negative space
  - restrained enterprise product cover typography below the connection
  - logo-derived left and right color accents unified through the connector
cover_shape_adaptation:
  - landscape ratios should place Logo A on the left and Logo B on the right with the connector running horizontally between them
  - title and subtitle sit in the lower middle area, clearly separated from the logo connector
  - 5:2 and 16:9 ratios should preserve wide breathing room and avoid filling the canvas with interface details
  - title emphasis may use subtle two-color accents derived from the logos, especially on key symbols, plus signs, numbers, or short keywords
must_preserve:
  - two distinct brand/tool icons with recognizable logo cues
  - one smooth connector line, one small center node, and a clear collaboration/integration relationship
  - clean modern enterprise product feel with premium soft-neumorphic depth
  - restrained palette derived from the two input logos
avoid_when_applying_to_cover:
  - infographic diagrams, complex workflows, many arrows, charts, dashboards, or dense labels
  - extra logos, fake UI panels, device mockups, people, mascots, or decorative illustrations
  - loud gradients, cyberpunk glow, excessive shadows, glossy toy-like icons, or crowded text
```

## Style Intent

品牌協同連接是一種用於表達兩個品牌、工具或產品互相連接的極簡橫版封面風格。它把兩個輸入 Logo 轉譯成左右兩枚高級輕擬物 3D 圓角圖標，用一條絲滑漸變連串接和中心節點表現協同、集成、自動化或工作流打通。該 style 只負責雙品牌連接的視覺語言、圖標質感、色彩關係和橫版構圖；平台適配、長文提煉和通用封面約束由 `punk-cover` 負責。

## Use For

- 教學封面、公眾號封面、X 封面、PPT 頭圖和產品宣傳封面
- 兩個工具、兩個品牌、兩個應用之間的集成、協同、連接、自動化和工作流主題
- 需要科技感、企業級、乾淨現代、剋制高級視覺的產品內容

## Avoid

- 單品牌宣傳、人物故事、複雜流程圖、資訊圖或多工具生態圖
- 需要大量步驟說明、截圖講解、表格資料或真實 UI 展示的封面
- 需要強衝擊營銷、炫彩賽博、複雜 3D 場景或重裝飾視覺的內容
