# Aptinery

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=flat-square)](LICENSE)
![Type: Agent Skills marketplace](https://img.shields.io/badge/type-Agent%20Skills%20marketplace-success.svg?style=flat-square)
[![Spec: Agent Skills](https://img.shields.io/badge/spec-Agent%20Skills-blue.svg?style=flat-square)](https://agentskills.io)
[![Spec: Agent Plugins](https://img.shields.io/badge/spec-Agent%20Plugins-635BFF.svg?style=flat-square)](https://agent-plugins.org)
![Claude Code](https://img.shields.io/badge/Claude%20Code-compatible-D97757.svg?style=flat-square&logo=claude&logoColor=white)
![OpenAI Codex](https://img.shields.io/badge/Codex-compatible-412991.svg?style=flat-square&logo=openai&logoColor=white)

**Aptinery — A curated foundry for Agent Skills.**

精選、改造並跨用戶端發行 Agent Skills 的個人技能工坊與市場。儲存庫同時提供通用 Agent Skills、Agent Plugins、Codex/ChatGPT 外掛和 Claude Code marketplace 入口，當前收錄 22 個可獨立安裝的 skill；市場不把它們捆綁成一個聚合外掛。

## Skills

| Skill | 用途 | 來源與授權 |
| --- | --- | --- |
| [`shanirez-style`](plugins/shanirez-style/skills/shanirez-style/SKILL.md) | 結構清晰的演算法競賽 C++14 程式碼風格 | 原創，GPL-3.0 |
| [`k12-lesson-plan-creation`](plugins/k12-lesson-plan-creation/skills/k12-lesson-plan-creation/SKILL.md) | 建立符合教學標準的 K-12 課程方案、課堂材料與評估 | Anthropic / Learning Commons，Apache-2.0 |
| [`k12-lesson-differentiation`](plugins/k12-lesson-differentiation/skills/k12-lesson-differentiation/SKILL.md) | 將已有課程分層適配不同熟練度與學生需求 | Anthropic / Learning Commons，Apache-2.0 |
| [`k12-lesson-prep`](plugins/k12-lesson-prep/skills/k12-lesson-prep/SKILL.md) | 幫助教師內化已有課程的關鍵任務並生成課前準備筆記 | Anthropic / Learning Commons，Apache-2.0 |
| [`k12-check-for-understanding`](plugins/k12-check-for-understanding/skills/k12-check-for-understanding/SKILL.md) | 為數學主題建立基於常見誤解的形成性理解檢查 | Anthropic / Learning Commons，Apache-2.0 |
| [`emil-design-eng`](plugins/emil-design-eng/skills/emil-design-eng/SKILL.md) | 打磨 UI、元件設計和動畫決策 | Emil Kowalski，MIT |
| [`animate`](plugins/animate/skills/animate/SKILL.md) | 從零實作有目的、可中斷的 Web 動畫 | Emil Kowalski，MIT |
| [`animate-expo`](plugins/animate-expo/skills/animate-expo/SKILL.md) | 實作高效能 React Native / Expo 動畫、手勢與觸覺回饋 | Emil Kowalski，MIT |
| [`review-animations`](plugins/review-animations/skills/review-animations/SKILL.md) | 按嚴格工藝標準審查動畫程式碼 | Emil Kowalski，MIT |
| [`improve-animations`](plugins/improve-animations/skills/improve-animations/SKILL.md) | 稽核程式碼庫動畫效果並生成可執行改進計畫 | Emil Kowalski，MIT |
| [`find-animation-opportunities`](plugins/find-animation-opportunities/skills/find-animation-opportunities/SKILL.md) | 找出真正值得加入動畫效果的介面位置 | Emil Kowalski，MIT |
| [`animation-vocabulary`](plugins/animation-vocabulary/skills/animation-vocabulary/SKILL.md) | 將模糊的動畫效果描述定位到準確術語 | Emil Kowalski，MIT |
| [`apple-design`](plugins/apple-design/skills/apple-design/SKILL.md) | 將 Apple 的介面與流暢動畫效果原則應用到 Web | Emil Kowalski，MIT |
| [`write-swift`](plugins/write-swift/skills/write-swift/SKILL.md) | 編寫和審查現代 Swift、並行、效能與測試程式碼 | Emil Kowalski，MIT |
| [`break-ui`](plugins/break-ui/skills/break-ui/SKILL.md) | 用真實感最壞資料壓力測試 UI，報告斷裂點並給出修復 | Emil Kowalski，MIT |
| [`mobile-native`](plugins/mobile-native/skills/mobile-native/SKILL.md) | 用平台層 CSS/中繼資料修復讓 Web App 在手機上更像原生 | Emil Kowalski，MIT |
| [`pick-ui-library`](plugins/pick-ui-library/skills/pick-ui-library/SKILL.md) | 從精選清單中為前端任務選擇合適的庫 | Emil Kowalski，MIT |
| [`prototype`](plugins/prototype/skills/prototype/SKILL.md) | 建立多個差異化 UI 方案並通過可視選擇器比較 | Emil Kowalski，MIT |
| [`ask-sonner`](plugins/ask-sonner/skills/ask-sonner/SKILL.md) | 安裝、設定、樣式化和排查 Sonner toast | Emil Kowalski，MIT |
| [`punk-cover`](plugins/punk-cover/skills/punk-cover/SKILL.md) | 將文章、帖子和主題生成平台適配的封面圖或重複使用提示詞 | AdrianPunk 與貢獻者；上游未聲明授權條款 |
| [`punk-avatar`](plugins/punk-avatar/skills/punk-avatar/SKILL.md) | 將人物、寵物、物品照片或描述生成頭像與紀念卡 | AdrianPunk 與貢獻者；上游未聲明授權條款 |
| [`punk-poster-layout`](plugins/punk-poster-layout/skills/punk-poster-layout/SKILL.md) | 僅在明確要求結構構圖控制時，為獨立海報、傳單、主視覺或單畫布編輯版塊選擇 32 種構圖；普通網站/UI、通用 Hero 與未明確要求構圖控制的平台封面不預設觸發 | 原文 AdrianPunk；Agent Skill 由 Aptinery 貢獻者改編與包裝；GPL-3.0 |

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
- Emil Kowalski 的 14 個設計與工程 skill 使用 MIT，固定來源 commit 記錄在 [`NOTICE`](NOTICE)。
- `punk-cover` 與 `punk-avatar` 的固定來源 commit 記錄在 [`NOTICE`](NOTICE)。當前上游為 Punk Skill v2.0.0 雙軌授權：個人非商用免費，商業用途須事先書面授權並付費；其 `LICENSE-PERSONAL.md` §5 禁止向他人散布本體或修改版。Aptinery 不把該材料標為 MIT，也不推定或補充轉散布授權。`punk-poster-layout` 是另行歸屬的 Aptinery 改編包，使用 GPL-3.0。

已有明確授權的主外掛根目錄及其 skill 目錄包含適用的授權條款副本；`punk-cover` 與 `punk-avatar` 因上游 v2.0.0 禁止轉散布且未取得商業授權，不附加或推定任何授權，也不宣稱可公開再散布。Claude 專用鏡像僅用於保留 3 個 skill 的 `disable-model-invocation: true` 語義，不增加新的市場條目或授權條件。
