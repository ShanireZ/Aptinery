# AGENTS.md — Aptinery

> 繼承 [`../AGENTS.md`](../AGENTS.md)；勿假定自動載入。這裡只寫專案合同。

## 散布與權威

Aptinery 是公開 Agent Skills 市場；機器標識 `aptinery`、顯示名/目錄/儲存庫名 `Aptinery`。GitHub `ShanireZ/Aptinery` 是權威，CNB `Round1/Aptinery` 由 [`../sync-github-cnb.ps1`](../sync-github-cnb.ps1) 鏡像同步。

- 每外掛恰含一個同名 skill；名單以 `.claude-plugin/marketplace.json` 與各 `plugin.json` 為準，不在此維護數量快照。
- `plugins/*/plugin.json` 是 Agent Plugins v1；`plugins/*/.codex-plugin/plugin.json` 與 `.agents/plugins/marketplace.json` 面向 Codex/ChatGPT；`plugins/*/skills/` 供 skills CLI/直接發現。
- Claude 適配在 `plugins/*/.claude-plugin/plugin.json`、`.claude-plugins/*/.claude-plugin/plugin.json` 和 `.claude-plugin/marketplace.json`。`.claude-plugins/{pick-ui-library,prototype,review-animations}/` 是適配源鏡像，不是額外產品。
- 版本在所有外掛與 marketplace/用戶端 manifest 間同步；路徑、名稱及 skill 入口也須一致。

## 來源、授權與不可變邊界

| 內容 | 來源與必須保留的約束 |
|---|---|
| `plugins/shanirez-style/` | 一方 GPL-3.0；SKILL 的統計依據為 [`../OJCode`](../OJCode)，未復算不得新增、削弱或強化斷言。方法見 [`docs/style-corpus-method.md`](docs/style-corpus-method.md) |
| 四個 `k12-*` skill | `anthropics/k12-teacher-skills` commit `31fd6dbb0c07cb50bb3ce7f62a4135a393bd0e8c`，Apache-2.0，逐字保留；目錄為 lesson-plan-creation、lesson-differentiation、lesson-prep、check-for-understanding |
| Emil Kowalski skill | `emilkowalski/skills` commit `2d228630ba1446365f614a108cb8252f1feda202`，MIT；除下述呼叫適配外保持上游相同 |
| punk-cover | `adrianpunk/Punk-Skill` commit `c9ad7a3745e07060c50270141efed418a0cd04d6`（此前 pin `a52e4456b8a4ccd4312069d6bc3755e2894dbc93`）。上游 v2.0.0 雙軌：個人非商用 LICENSE-PERSONAL，商業須書面授權付費；§5 禁止向他人散布。不得標為 MIT、不得推斷轉散布授權或恢復已移除的 GPLv3 檔案/聲明 |
| `onetake` | `feitangyuan/onetake` commit `415758128aa45cc54340df40d8109363447f582e`；PolyForm Noncommercial 1.0.0，保留兩層 LICENSE 與 Required Notice；字型另依 `looks/fonts/LICENSES.txt`。適配 description、套件路徑說明、散布中繼資料，並對新匯入的八個檔案移除行尾空白及末尾多餘空行（名單見外掛 NOTICE）；不重新授權 |
| punk-poster-layout | 改編自 AdrianPunk 的兩篇 Punk Space 文章，不是上述 commit 的原樣樹；來源與署名在 `NOTICE`，本改編 GPL-3.0 |

- K-12 保留各目錄 LICENSE、SPDX、引用 NOTICE 與根 NOTICE 署名；本機修改須有 Apache 要求的醒目修改說明並記 NOTICE。不引入上游可選 `.mcp.json`，保留無 connector 退回。
- Emil 保留根 NOTICE 及外掛/skill 兩層 MIT LICENSE；任何適配記 NOTICE。K-12 的 license frontmatter、Emil 的原 frontmatter 均保留，只有已記錄的三處呼叫翻譯例外。
- `pick-ui-library` / `prototype` / `review-animations` 的 `agents/openai.yaml` 必須 `policy.allow_implicit_invocation: false`；Markdown body 保持上游一致，僅翻譯呼叫 frontmatter，並給 review-animations description 加 explicit-only 句。
- 三份 `.claude-plugins/` 源鏡像由 Claude marketplace 使用，保留 `disable-model-invocation: true`，須與固定上游樹逐位元組一致。
- `onetake` 保留 lib、scripts、references、templates、looks/fonts、gallery 與案例 README；大型範例影片與宣傳素材留在固定上游連結。執行相依見 README；不把影片案例提到的歷史工作檔視為隨包提供。
- Punk 保留 SKILL、openai.yaml、references、選定 style atoms 原文；有意適配記 NOTICE。恢復/新增授權須有權利人獨立可驗證證據，不從歷史/快取恢復無依據聲明。
- 已核實既有 Punk 臺灣繁體在地化與上述原文約定有差異；本次保留已提交內容，未擴大改動。與固定上游的比較範圍及差異見 NOTICE，不宣稱整份 Punk 匯入逐位元組相同。
- `punk-avatar` 與 `punk-ip-video-cover` 依使用者 2026-10-18 指示不收錄；Punk 僅保留 punk-cover 及其既有 style 選集。
- punk-cover 只帶 33 個封面 atoms。`../../styles/{style-id}` 相依外掛根 styles，不能當附件刪除。上游截圖/倉級驗證指令碼有意不 vendored。
- punk-poster-layout 保留 32 個具名構圖系統、image-prompt 與 HTML/CSS 表達、評審標準；只負責結構與焦點/層級/柵格/密度，不接管 punk-cover 的風格 atoms。原 MHTML 是包外資料，不引入不完整網頁存檔或遠端懶載入圖。

## 命令與驗收

從儲存庫根執行；本儲存庫是散布包，沒有應用級 build/test 入口。下表為定義與驗收要求，不代表本輪已跑過。

| 何時 | 命令 / 前置 | 能證明什麼 / 邊界 |
|---|---|---|
| skill/散布變更 | `npx skills add . --list`；skills CLI 可用 | 發現入口；npx 可能獲取工具，不當作離線靜態檢查，也不證明各用戶端行為 |
| Claude 適配變更 | `claude plugin validate . --strict`；Claude CLI 可用 | 嚴格 manifest 驗證；不代替其他用戶端或 vendor 一致性 |
| 任意文件/散布變更 | `git diff --check` | 空白診斷；不證明語義或授權合規 |
| C++ 範本變更 | `g++ -std=c++14 -O2 -Wall -m64 -static-libgcc <模板.cpp> -o <临时输出>`；g++ 可用 | 編譯後還須手算輸入執行核對，產物不入包 |

此外必須解析所有 JSON manifests；對照各用戶端名稱/版本/路徑/入口，檢查上述顯式呼叫策略、LICENSE/NOTICE 和必需 styles/references。未有意修改的 vendor 與固定上游 commit 比對；本機缺上游物件時明確未驗，不以 JSON 可解析替代。記錄實際命令、結束代碼及未覆蓋用戶端。

## 格式與記錄

- shanirez-style SKILL frontmatter 僅 name/description，name 等於目錄名，檔案少於 500 行。
- `.gitattributes` 固定 LF；只對四個 K-12 目錄關閉 whitespace 診斷以保上游原文，不擴大例外。無空行/末尾不換行只約束生成 OJ .cpp 與 C++ 範例，不約束 Markdown。
- 不建立或恢復 `docs/research/`、獨立研究/稽核報告；臨時研究回對話。核實的授權/來源變更只回寫 AGENTS、README 或 NOTICE 的有效事實，不從歷史/存檔/快取重建已刪除報告。
- Issue tracker：本儲存庫 GitHub Issues；triage、domain、OKF 沿用 [`docs/agents/index.md`](docs/agents/index.md)。
