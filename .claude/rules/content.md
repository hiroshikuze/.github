# Content Rules / コンテンツルール

All rules are written as Yes/No checks.  
すべてのルールはYes/Noで判定できる条件として記述。

---

## Allowed File Types / 追加してよいファイル

Before adding any file, answer: **Is this file one of the following?**  
ファイルを追加する前に確認：**以下のいずれかに該当するか？**

- [ ] `.github/FUNDING.yml`
- [ ] `.github/ISSUE_TEMPLATE/*.md` or `.github/ISSUE_TEMPLATE/config.yml`
- [ ] `.github/PULL_REQUEST_TEMPLATE.md`
- [ ] `.github/DISCUSSION_TEMPLATE/*.md`
- [ ] `.github/workflows/workflow-templates/*`
- [ ] `profile/README.md`
- [ ] Community health file in repo root: `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`, `SUPPORT.md`
- [ ] `CLAUDE.md` or `.claude/*`

> If none of the above → **Do not add the file.**  
> どれにも該当しない → **ファイルを追加しない。**

---

## Prohibited Content / 禁止コンテンツ

- [ ] No application source code added? (`.js`, `.ts`, `.py`, `.go`, `.rs`, etc.)  
      アプリケーションのソースコードを追加していないか？
- [ ] No package manager files? (`package.json`, `Gemfile`, `requirements.txt`, `go.mod`, etc.)  
      パッケージマネージャファイルを追加していないか？
- [ ] No linting/formatting configs? (`.eslintrc`, `.prettierrc`, `pyproject.toml`, etc.)  
      リント・フォーマット設定ファイルを追加していないか？
- [ ] No test files or test infrastructure?  
      テストファイルやテスト基盤を追加していないか？
- [ ] No CI/CD pipeline files? (`.github/workflows/*.yml` — except reusable workflow templates)  
      CI/CDパイプラインファイルを追加していないか？（再利用可能なワークフローテンプレートを除く）

---

## FUNDING.yml Rules / FUNDING.yml ルール

- [ ] Only uses supported keys? (`github`, `patreon`, `open_collective`, `ko_fi`, `tidelift`,  
      `community_bridge`, `liberapay`, `issuehunt`, `otechie`, `lfx_crowdfunding`,  
      `polar`, `buy_me_a_coffee`, `thanks_dev`, `custom`)  
      サポートされているキーのみ使用しているか？
- [ ] `custom` value is a YAML list even if there is only one URL?  
      URLが1つでも `custom` の値はYAMLリスト形式か？

**Current config / 現在の設定:**
```yaml
github: hiroshikuze
custom: ["https://www.amazon.jp/hz/wishlist/ls/5BAWD0LZ89V9?ref_=wl_share"]
```
