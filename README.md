# Aptinery

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![Type: Agent Skills marketplace](https://img.shields.io/badge/type-Agent%20Skills%20marketplace-success.svg?style=flat-square)
[![Spec: Agent Skills](https://img.shields.io/badge/spec-Agent%20Skills-blue.svg?style=flat-square)](https://agentskills.io)
[![Spec: Agent Plugins](https://img.shields.io/badge/spec-Agent%20Plugins-635BFF.svg?style=flat-square)](https://agent-plugins.org)
![Claude Code](https://img.shields.io/badge/Claude%20Code-compatible-D97757.svg?style=flat-square&logo=claude&logoColor=white)
![OpenAI Codex](https://img.shields.io/badge/Codex-compatible-412991.svg?style=flat-square&logo=openai&logoColor=white)

**Aptinery — A curated foundry for Agent Skills.**

精選、改造並跨用戶端發行 Agent Skills 的個人技能工坊與市場。儲存庫同時提供通用 Agent Skills、Agent Plugins、Codex/ChatGPT 外掛和 Claude Code marketplace 入口，當前收錄 24 個可獨立安裝的 skill；市場不把它們捆綁成一個聚合外掛。

## Skills

| Skill                                                                                                               | 用途                                                                                                                                                | 來源與授權                                                                    |
| ------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [`shanirez-style`](plugins/shanirez-style/skills/shanirez-style/SKILL.md)                                           | 結構清晰的演算法競賽 C++14 程式碼風格                                                                                                               | 原創，GPL-3.0                                                                 |
| [`k12-lesson-plan-creation`](plugins/k12-lesson-plan-creation/skills/k12-lesson-plan-creation/SKILL.md)             | 建立符合教學標準的 K-12 課程方案、課堂材料與評估                                                                                                    | Anthropic / Learning Commons，Apache-2.0                                      |
| [`k12-lesson-differentiation`](plugins/k12-lesson-differentiation/skills/k12-lesson-differentiation/SKILL.md)       | 將已有課程分層適配不同熟練度與學生需求                                                                                                              | Anthropic / Learning Commons，Apache-2.0                                      |
| [`k12-lesson-prep`](plugins/k12-lesson-prep/skills/k12-lesson-prep/SKILL.md)                                        | 幫助教師內化已有課程的關鍵任務並生成課前準備筆記                                                                                                    | Anthropic / Learning Commons，Apache-2.0                                      |
| [`k12-check-for-understanding`](plugins/k12-check-for-understanding/skills/k12-check-for-understanding/SKILL.md)    | 為數學主題建立基於常見誤解的形成性理解檢查                                                                                                          | Anthropic / Learning Commons，Apache-2.0                                      |
| [`emil-design-eng`](plugins/emil-design-eng/skills/emil-design-eng/SKILL.md)                                        | 打磨 UI、元件設計和動畫決策                                                                                                                         | Emil Kowalski，MIT                                                            |
| [`animate`](plugins/animate/skills/animate/SKILL.md)                                                                | 從零實作有目的、可中斷的 Web 動畫                                                                                                                   | Emil Kowalski，MIT                                                            |
| [`animate-expo`](plugins/animate-expo/skills/animate-expo/SKILL.md)                                                 | 實作高效能 React Native / Expo 動畫、手勢與觸覺回饋                                                                                                 | Emil Kowalski，MIT                                                            |
| [`review-animations`](plugins/review-animations/skills/review-animations/SKILL.md)                                  | 按嚴格工藝標準審查動畫程式碼                                                                                                                        | Emil Kowalski，MIT                                                            |
| [`improve-animations`](plugins/improve-animations/skills/improve-animations/SKILL.md)                               | 稽核程式碼庫動畫效果並生成可執行改進計畫                                                                                                            | Emil Kowalski，MIT                                                            |
| [`find-animation-opportunities`](plugins/find-animation-opportunities/skills/find-animation-opportunities/SKILL.md) | 找出真正值得加入動畫效果的介面位置                                                                                                                  | Emil Kowalski，MIT                                                            |
| [`animation-performance`](plugins/animation-performance/skills/animation-performance/SKILL.md)                      | 診斷 Web 動畫掉幀、繪製成本、主執行緒競爭與 React 動畫瓶頸                                                                                          | Emil Kowalski，MIT                                                            |
| [`animation-vocabulary`](plugins/animation-vocabulary/skills/animation-vocabulary/SKILL.md)                         | 將模糊的動畫效果描述定位到準確術語                                                                                                                  | Emil Kowalski，MIT                                                            |
| [`apple-design`](plugins/apple-design/skills/apple-design/SKILL.md)                                                 | 將 Apple 的介面與流暢動畫效果原則應用到 Web                                                                                                         | Emil Kowalski，MIT                                                            |
| [`write-swift`](plugins/write-swift/skills/write-swift/SKILL.md)                                                    | 編寫和審查現代 Swift、並行、效能與測試程式碼                                                                                                        | Emil Kowalski，MIT                                                            |
| [`break-ui`](plugins/break-ui/skills/break-ui/SKILL.md)                                                             | 用真實感最壞資料壓力測試 UI，報告斷裂點並給出修復                                                                                                   | Emil Kowalski，MIT                                                            |
| [`mobile-native`](plugins/mobile-native/skills/mobile-native/SKILL.md)                                              | 用平台層 CSS/中繼資料修復讓 Web App 在手機上更像原生                                                                                                | Emil Kowalski，MIT                                                            |
| [`pick-ui-library`](plugins/pick-ui-library/skills/pick-ui-library/SKILL.md)                                        | 從精選清單中為前端任務選擇合適的庫                                                                                                                  | Emil Kowalski，MIT                                                            |
| [`prototype`](plugins/prototype/skills/prototype/SKILL.md)                                                          | 建立多個差異化 UI 方案並通過可視選擇器比較                                                                                                          | Emil Kowalski，MIT                                                            |
| [`ask-sonner`](plugins/ask-sonner/skills/ask-sonner/SKILL.md)                                                       | 安裝、設定、樣式化和排查 Sonner toast                                                                                                               | Emil Kowalski，MIT                                                            |
| [`punk-cover`](plugins/punk-cover/skills/punk-cover/SKILL.md)                                                       | 將文章、貼文和主題生成平台適配的封面圖或重複使用提示詞                                                                                              | AdrianPunk 與貢獻者；個人非商用                                               |
| [`punk-poster-layout`](plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md)                               | 僅在明確要求結構構圖控制時，為獨立海報、傳單、主視覺或單畫布編輯版塊選擇 32 種構圖；普通網站/UI、通用 Hero 與未明確要求構圖控制的平台封面不預設觸發 | 原文 AdrianPunk；Agent Skill 由 Aptinery 貢獻者改編與包裝；GPL-3.0            |
| [`onetake`](plugins/onetake/skills/onetake/SKILL.md)                                                                | 製作一鏡到底的產品發布片、預告與旁白功能演示，包含鏡頭連續性檢查                                                                                    | Patrick / feitangyuan，PolyForm Noncommercial 1.0.0；非商用，商用須另取得授權 |
| [`design-taste-frontend`](plugins/design-taste-frontend/skills/design-taste-frontend/SKILL.md)                      | 為網站、產品頁、儀表板與 App 畫面提供藝術指導：抽取研究過的設計方向、取用開放圖庫真實圖片，並以真實瀏覽器檢查擺脫千篇一律的 AI 頁面                 | Leonxlnx，MIT                                                                 |

## 安裝

以下單項安裝命令均以 `animate` 為例，可替換為上表中的任一 skill 名稱。

### skills CLI：Codex、Claude Code、Cursor、OpenCode 等

全域安裝全部 skill：

```bash
npx skills add ShanireZ/Aptinery -g
```

單獨安裝表格中的任一 skill：

```bash
npx skills add ShanireZ/Aptinery -g --skill animate
```

### Claude Code marketplace

```bash
claude plugin marketplace add ShanireZ/Aptinery
claude plugin install animate@aptinery
```

`pick-ui-library`、`prototype` 和 `review-animations` 保留上游的 Claude 顯式呼叫契約；安裝後分別通過 `/pick-ui-library:pick-ui-library`、`/prototype:prototype` 和 `/review-animations:review-animations` 呼叫。

### Codex / ChatGPT marketplace

```bash
codex plugin marketplace add ShanireZ/Aptinery
codex plugin add animate@aptinery
```

上述 3 個顯式呼叫 skill 在 Codex 中通過各自的 `agents/openai.yaml` 禁止隱式呼叫，可用 `$pick-ui-library`、`$prototype` 和 `$review-animations` 顯式呼叫。

### GitHub Copilot CLI marketplace

```bash
copilot plugin marketplace add ShanireZ/Aptinery
copilot plugin install animate@aptinery
```

### Agent Plugins 用戶端

每個 `plugins/<skill-name>/plugin.json` 都是獨立的 Agent Plugins v1 入口；可安裝名稱與上表完全一致。

## 來源與授權

本儲存庫原創內容採用 [GNU General Public License v3.0](LICENSE) 發佈。

第三方內容繼續採用各自的 `LICENSE` 和歸屬聲明：

- Anthropic / Learning Commons 的四個 K-12 skill 使用 Apache-2.0，固定來源 commit 記錄在 [`NOTICE`](NOTICE)。
- Emil Kowalski 的 15 個設計與工程 skill 使用 MIT，固定來源 commit 記錄在 [`NOTICE`](NOTICE)。
- Leonxlnx 的 `design-taste-frontend`（tasteskill v2，上游 [`Leonxlnx/taste-skill`](https://github.com/Leonxlnx/taste-skill)）使用 MIT，固定來源 commit 記錄在 [`NOTICE`](NOTICE)；技能執行時下載的圖片、影片與字型保留各自授權。
- `onetake` 固定來源 commit 與打包適配記錄在 [`NOTICE`](NOTICE)，上游材料使用 [PolyForm Noncommercial 1.0.0](plugins/onetake/LICENSE)，不適用本儲存庫原創內容的 GPL；字型保留各自授權。商業用途須另取得上游商業授權。
- `punk-cover` 的固定來源 commit 記錄在 [`NOTICE`](NOTICE)。當前上游為 Punk Skill v2.0.0 雙軌授權：個人非商用免費，商業用途須事先書面授權並付費；其 `LICENSE-PERSONAL.md` §5 禁止向他人散布本體或修改版。Aptinery 不把該材料標為 MIT，也不推定或補充轉散布授權。`punk-poster-layout` 是另行歸屬的 Aptinery 改編包，使用 GPL-3.0。

已有明確授權的主外掛根目錄及其 skill 目錄包含適用的授權條款副本；`punk-cover` 因上游 v2.0.0 禁止轉散布且未取得商業授權，不附加或推定任何授權，也不宣稱可公開再散布。Claude 專用鏡像僅用於保留 3 個 skill 的 `disable-model-invocation: true` 語義，不增加新的市場條目或授權條件。

## OneTake 執行需求

`onetake` 的安裝入口與其他技能相同，例如在儲存庫根執行 `npx skills add . --skill onetake`；
Claude Code 則先執行 `claude plugin marketplace add .`，再執行 `claude plugin install onetake@aptinery`。安裝技能不會
自動安裝其執行相依：需 Python 3、Playwright 與 Chromium、NumPy、SciPy、Pillow、
Matplotlib、fonttools、brotli、FFmpeg／ffprobe，以及 Node.js。參考片分析另需
opencv-python；旁白另需 faster-whisper、Kokoro（kokoro-onnx、soundfile），日語另需
misaki[ja] 與 unidic-lite。具體用法保留在技能及其 references 中。

套件包含執行函式庫、腳本、範本、字型及其授權、gallery 和案例拆解；大型範例影片與
宣傳素材留在[固定上游](https://github.com/feitangyuan/onetake/tree/415758128aa45cc54340df40d8109363447f582e/cases)。
案例拆解提及的成片與歷史工作檔是上游案例資訊，不表示它們隨此套件散布。

## design-taste-frontend 執行需求

`design-taste-frontend` 的腳本不安裝相依，也不需 API 金鑰：需 Node.js 22 以上，以及已安裝的
Chrome、Edge 或 Chromium（位置特殊時設定 `CHROME_PATH`）；`assets.mjs` 搜尋與下載開放圖庫素材時需要網路。
工作檔寫入目標專案的 `.taste-skill/`，抽取紀錄寫入 `~/.taste-skill/history.json`（可用 `TASTE_SKILL_HISTORY` 移動）。
本包只收錄上游預設 skill；上游的 classic 風格 skill 與已遷出的生圖 skill 不在此散布。
