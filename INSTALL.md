# 安裝 Aptinery Skills


以下單項安裝命令均以 `animate` 為例，可替換為[技能目錄](docs/catalog.md)中的任一 skill 名稱。

### skills CLI：Codex、Claude Code、Cursor、OpenCode 等

全域安裝全部 skill：

```bash
npx skills add ShanireZ/Aptinery -g
```

單獨安裝目錄中的任一 skill：

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

每個 `plugins/<skill-name>/plugin.json` 都是獨立的 Agent Plugins v1 入口；可安裝名稱與[技能目錄](docs/catalog.md)完全一致。


## OneTake 執行需求

`onetake` 的安裝入口與其他技能相同，例如在儲存庫根執行 `npx skills add . --skill onetake`；
Claude Code 則先執行 `claude plugin marketplace add .`，再執行 `claude plugin install onetake@aptinery`。安裝技能不會
自動安裝其執行相依：需 Python 3、Playwright 與 Chromium、NumPy、SciPy、Pillow、
Matplotlib、fonttools、brotli、FFmpeg／ffprobe，以及 Node.js。參考片分析另需
opencv-python；旁白另需 faster-whisper、Kokoro（kokoro-onnx、soundfile），日語另需
misaki[ja] 與 unidic-lite。具體用法保留在技能及其 references 中。

套件包含執行函式庫、腳本、範本、字型及其授權、gallery 和案例拆解；大型範例影片與
宣傳素材留在[固定上游](https://github.com/feitangyuan/onetake/tree/013a61ac8d98883c73733f59c06e49e9ba444f14/cases)。
案例拆解提及的成片與歷史工作檔是上游案例資訊，不表示它們隨此套件散布。

## design-taste-frontend 執行需求

`design-taste-frontend` 的腳本不安裝相依，也不需 API 金鑰：需 Node.js 22 以上，以及已安裝的
Chrome、Edge 或 Chromium（位置特殊時設定 `CHROME_PATH`）；`assets.mjs` 搜尋與下載開放圖庫素材時需要網路。
工作檔寫入目標專案的 `.taste-skill/`，抽取紀錄寫入 `~/.taste-skill/history.json`（可用 `TASTE_SKILL_HISTORY` 移動）。
本包只收錄上游預設 skill；上游的 classic 風格 skill 與已遷出的生圖 skill 不在此散布。
