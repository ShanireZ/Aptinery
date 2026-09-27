# AGENTS.md — Aptinery

> 继承 [`../AGENTS.md`](../AGENTS.md)；勿假定自动加载。这里只写项目合同。

## 分发与权威

Aptinery 是公开 Agent Skills 市场；机器标识 `aptinery`、显示名/目录/仓库名 `Aptinery`。GitHub `ShanireZ/Aptinery` 是权威，CNB `Round1/Aptinery` 由 [`../sync-github-cnb.ps1`](../sync-github-cnb.ps1) 镜像同步。

- 每插件恰含一个同名 skill；名单以 `.claude-plugin/marketplace.json` 与各 `plugin.json` 为准，不在此维护数量快照。
- `plugins/*/plugin.json` 是 Agent Plugins v1；`plugins/*/.codex-plugin/plugin.json` 与 `.agents/plugins/marketplace.json` 面向 Codex/ChatGPT；`plugins/*/skills/` 供 skills CLI/直接发现。
- Claude 适配在 `plugins/*/.claude-plugin/plugin.json`、`.claude-plugins/*/.claude-plugin/plugin.json` 和 `.claude-plugin/marketplace.json`。`.claude-plugins/{pick-ui-library,prototype,review-animations}/` 是适配源镜像，不是额外产品。
- 版本在所有插件与 marketplace/客户端 manifest 间同步；路径、名称及 skill 入口也须一致。

## 来源、许可与不可变边界

| 内容 | 来源与必须保留的约束 |
|---|---|
| `plugins/shanirez-style/` | 一方 GPL-3.0；SKILL 的统计依据为 [`../OJCode`](../OJCode)，未复算不得新增、削弱或强化断言。方法见 [`docs/style-corpus-method.md`](docs/style-corpus-method.md) |
| 四个 `k12-*` skill | `anthropics/k12-teacher-skills` commit `281eb8d41fe2837d911541c9bbb870b58add804c`，Apache-2.0，逐字保留；目录为 lesson-plan-creation、lesson-differentiation、lesson-prep、check-for-understanding |
| Emil Kowalski skill | `emilkowalski/skills` commit `d23d7f88a2e21c9e4b1418c7abe420f5c1052ba7`，MIT；除下述调用适配外保持上游相同 |
| punk-cover / punk-avatar | `adrianpunk/Punk-Skill` commit `a52e4456b8a4ccd4312069d6bc3755e2894dbc93`，上游未声明许可，转分发许可未确立；不得推断、补发许可或恢复已移除的 GPLv3 文件/声明 |
| punk-poster-layout | 改编自 AdrianPunk 的两篇 Punk Space 文章，不是上述 commit 的原样树；来源与署名在 `NOTICE`，本改编 GPL-3.0 |

- K-12 保留各目录 LICENSE、SPDX、引用 NOTICE 与根 NOTICE 署名；本地修改须有 Apache 要求的醒目修改说明并记 NOTICE。不引入上游可选 `.mcp.json`，保留无 connector 回退。
- Emil 保留根 NOTICE 及插件/skill 两层 MIT LICENSE；任何适配记 NOTICE。K-12 的 license frontmatter、Emil 的原 frontmatter 均保留，只有已记录的三处调用翻译例外。
- `pick-ui-library` / `prototype` / `review-animations` 的 `agents/openai.yaml` 必须 `policy.allow_implicit_invocation: false`；Markdown body 保持上游一致，仅翻译调用 frontmatter，并给 review-animations description 加 explicit-only 句。
- 三份 `.claude-plugins/` 源镜像由 Claude marketplace 使用，保留 `disable-model-invocation: true`，须与固定上游树逐字节一致。
- Punk 保留 SKILL、openai.yaml、references、选定 style atoms 原文；有意适配记 NOTICE。恢复/新增许可须有权利人独立可验证证据，不从历史/缓存恢复无依据声明。
- punk-cover 只带 30 个封面 atoms；punk-avatar 带 7 个头像 atoms，包括 surreal-pop-up-paper-landscape 的两个 mode references。`../../styles/{style-id}` 依赖插件根 styles，不能当附件删除。上游截图/仓级验证脚本有意不 vendored。
- punk-poster-layout 保留 32 个具名构图系统、image-prompt 与 HTML/CSS 表达、评审标准；只负责结构与焦点/层级/栅格/密度，不接管 punk-cover 的风格 atoms。原 MHTML 是包外资料，不引入不完整网页存档或远端懒加载图。

## 命令与验收

从仓库根执行；本仓是分发包，没有应用级 build/test 入口。下表为定义与验收要求，不代表本轮已跑过。

| 何时 | 命令 / 前置 | 能证明什么 / 边界 |
|---|---|---|
| skill/分发变更 | `npx skills add . --list`；skills CLI 可用 | 发现入口；npx 可能获取工具，不当作离线静态检查，也不证明各客户端行为 |
| Claude 适配变更 | `claude plugin validate . --strict`；Claude CLI 可用 | 严格 manifest 验证；不代替其他客户端或 vendor 一致性 |
| 任意文档/分发变更 | `git diff --check` | 空白诊断；不证明语义或许可合规 |
| C++ 模板变更 | `g++ -std=c++14 -O2 -Wall -m64 -static-libgcc <模板.cpp> -o <临时输出>`；g++ 可用 | 编译后还须手算输入运行核对，产物不入包 |

此外必须解析所有 JSON manifests；对照各客户端名称/版本/路径/入口，检查上述显式调用策略、LICENSE/NOTICE 和必需 styles/references。未有意修改的 vendor 与固定上游 commit 比对；本地缺上游对象时明确未验，不以 JSON 可解析替代。记录实际命令、退出码及未覆盖客户端。

## 格式与记录

- shanirez-style SKILL frontmatter 仅 name/description，name 等于目录名，文件少于 500 行。
- `.gitattributes` 固定 LF；只对四个 K-12 目录关闭 whitespace 诊断以保上游原文，不扩大例外。无空行/末尾不换行只约束生成 OJ .cpp 与 C++ 示例，不约束 Markdown。
- 不创建或恢复 `docs/research/`、独立研究/审计报告；临时研究回对话。核实的许可/来源变更只回写 AGENTS、README 或 NOTICE 的有效事实，不从历史/存档/缓存重建已删除报告。
- Issue tracker：本仓 GitHub Issues；triage、domain、OKF 沿用 [`docs/agents/index.md`](docs/agents/index.md)。
