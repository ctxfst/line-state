# line-state

> **Track the `Current State` (vs. `Desired State`) of your problem lines and 24h/3d external `news`—rendered as plain Markdown for Obsidian.**

`line-state` is the state and recent-signal engine in the [`ctxfst`](https://github.com/ctxfst) ecosystem, designed to pair with **[`skill-line-coach`](https://github.com/ctxfst/skill-line-coach)**:

- **[`skill-line-coach`](https://github.com/ctxfst/skill-line-coach)** (Write-time skill): Coaches you while writing diary entries or notes so each problem line (`問題線`) captures all four slots (**Actor / Action + Object / Concrete Blocker / Outcome**).
- **`line-state`** (Cron + on-demand state engine): Runs automatically via system `crontab` (or on-demand via CLI) to collect recent 24h / 3d external `news`, compute the **Current State** and **Delta** across your watches and problem lines, and write plain Markdown reports for Obsidian.

---

## Core Concepts

1. **Current State vs. Desired State**:
   Instead of letting AI rewrite your old notes into a static wiki, `line-state` keeps raw notes and observations append-only and computes a live snapshot of what is currently blocked, what just changed, and what moved closer to your desired state.
2. **24h / 3d `news` Collection + Probe Filtering**:
   Continuously ingests recent external items (last 24 hours / 3 days) across your watched topics, filters noise using Rocchio embedding probes (`confirmed examples − 0.5 × rejected examples`), and surfaces verified state changes (`rising`, `new`, `events`, `shifts`).
3. **Plain-Text & Obsidian Native**:
   All data lives in plain `JSONL` and `Markdown` files. Reports include simple `[x]` / `[-]` checkboxes that feed back into the probe on the next run.

---

## Documentation (Format Draft)

- **[中文格式草案 (`docs/zh-TW/`)](docs/zh-TW/README.md)**
  - [格式總覽 (Overview)](docs/zh-TW/格式總覽.md)
  - [觀測 / News (Observations)](docs/zh-TW/觀測.md)
  - [實體 (Entities)](docs/zh-TW/實體.md)
  - [狀態與變化 (State & Delta)](docs/zh-TW/狀態與變化.md)
  - [關注與回饋 (Watches & Feedback)](docs/zh-TW/關注與回饋.md)
  - [名詞對照 (Glossary)](docs/zh-TW/名詞對照.md)

## License

[MIT](LICENSE). Maintained by [ctxfst](https://github.com/ctxfst).
