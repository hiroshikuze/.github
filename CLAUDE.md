# CLAUDE.md

> **Session Start / セッション開始:** Read `.claude/revision_log.md` before any work.
> 作業を始める前に必ず `.claude/revision_log.md` を読むこと。

---

## 6 Core Principles / 6つの中核原則

### 1. Plan Mode Default
**EN:** If a task has ≥ 3 steps, present a numbered plan and get approval before implementing.  
**JA:** タスクが3ステップ以上なら、番号付きの計画を提示してユーザーの承認を得てから実装する。

> **Check:** Does this task have ≥ 3 steps? → Present plan first, then wait for approval.

---

### 2. Self-Improvement Loop
**EN:** Log every mistake pattern in `.claude/revision_log.md`. Re-read at every session start.  
**JA:** ミスのパターンを `.claude/revision_log.md` に記録し、毎セッション冒頭で読み返す。

> **Check:** Did an error occur this session? → Add an entry to `revision_log.md` before closing.

---

### 3. Verification Before Done
**EN:** Before reporting complete, ask: "Would a staff engineer approve this without changes?"  
**JA:** 完了報告の前に「スタッフエンジニアが修正なく承認するか」を自問する。

> **Check:** Is the output staff-engineer quality? → If no, iterate before reporting done.

---

### 4. Subagent Strategy
**EN:** Delegate research and analysis to subagents to preserve the main context window.  
**JA:** リサーチ・分析はサブエージェントに委譲し、メインコンテキストを保全する。

> **Check:** Is this primarily research or large-scale analysis? → Use a subagent.

---

### 5. Demand Elegance
**EN:** For design-level changes, compare 2–3 approaches before choosing. Minor fixes are exempt.  
**JA:** 設計判断を含む変更では、力技の前に2〜3のアプローチを比較検討する（細かい修正は除く）。

> **Check:** Does this change involve a design decision? → Compare ≥ 2 approaches first.

---

### 6. Autonomous Bug Fixing
**EN:** On bug reports, investigate and fix autonomously. Ask only for design-level decisions.  
**JA:** バグ報告時はまず自律的に調査・修正し、設計判断のみユーザーに確認を取る。

> **Check:** Is this a bug fix (not a design question)? → Fix without asking first.

---

## Repository Overview / リポジトリ概要

**Repo:** `hiroshikuze/.github` — GitHub account-level community profile  
**Owner:** Hiroshi Kuze (`hiroshikuze`)  
**Purpose:** Profile-wide defaults applied to all repositories in the account.

### Structure / 構造

```
.github/
├── .claude/
│   ├── rules/              # Detailed Yes/No rule checklists
│   │   ├── git.md          # Commit style, branch naming, push workflow
│   │   ├── content.md      # Allowed file types, repo scope
│   │   └── bilingual.md    # EN/JA language conventions
│   ├── revision_log.md     # Session mistake log (read at session start)
│   └── settings.json       # Auto-triggered hooks
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   ├── feature_request.md
│   │   └── config.yml
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── FUNDING.yml
├── CLAUDE.md               # This file — decision quality rules only
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── README.md
└── SECURITY.md
```

### What Belongs Here / 追加してよいもの
- `.github/FUNDING.yml`, `ISSUE_TEMPLATE/*`, `PULL_REQUEST_TEMPLATE.md`
- `.github/DISCUSSION_TEMPLATE/*`, `.github/workflows/workflow-templates/*`
- `profile/README.md`, community health files (`CODE_OF_CONDUCT`, `CONTRIBUTING`, `SECURITY`)
- `CLAUDE.md`, `.claude/*`

### What Does Not Belong / 追加してはいけないもの
- Application source code, build tooling, package managers, test suites
- Language-specific linting/formatting configs (`.eslintrc`, `.prettierrc`, etc.)

> No build or test commands — this is a configuration-only repository.  
> ビルド・テストコマンドなし — 設定ファイルのみのリポジトリ。

---

## Detailed Rules / 詳細ルール → `.claude/rules/`

| File | Contents |
|------|----------|
| `git.md` | Commit style, branch naming, push workflow |
| `content.md` | Allowed files, funding config, repo scope |
| `bilingual.md` | EN/JA structure and formatting |
