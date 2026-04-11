# Git Rules / Git ルール

All rules are written as Yes/No checks. Every condition must be **Yes** before committing or pushing.  
すべてのルールはYes/Noで判定できる条件として記述。コミット・プッシュ前に全条件が **Yes** であること。

---

## Commit Message / コミットメッセージ

- [ ] Subject line is ≤ 72 characters?  
      件名は72文字以内か？
- [ ] Subject uses imperative mood? (`Add`, `Fix`, `Update`, `Remove`, `Rename`)  
      命令形を使っているか？（`Add`, `Fix`, `Update`, `Remove`, `Rename`）
- [ ] Subject does NOT end with a period?  
      件名の末尾にピリオドがないか？
- [ ] Body (if present) is separated from subject by a blank line?  
      本文がある場合、件名との間に空行があるか？

**Good examples / 良い例:**
```
Add bilingual bug report template
Fix typo in CONTRIBUTING.md
Update FUNDING.yml with new sponsor link
Remove unused discussion template
```

---

## Branch Naming / ブランチ命名

- [ ] Branch name matches the pattern `<tool>/<description>-<id>`?  
      ブランチ名が `<tool>/<description>-<id>` パターンに合っているか？
- [ ] Description uses lowercase kebab-case?  
      説明部分は小文字ケバブケースか？
- [ ] Never working directly on `main`?  
      `main` で直接作業していないか？

**Good examples / 良い例:**
```
claude/add-issue-templates-Vd2bk
claude/update-security-policy-X3mNq
```

---

## Push Workflow / プッシュ手順

- [ ] Using `git push -u origin <branch-name>` (never bare `git push`)?  
      `git push -u origin <branch-name>` を使っているか（裸の `git push` は不可）？
- [ ] Feature branch exists before pushing?  
      プッシュ前にフィーチャーブランチが存在するか？
- [ ] Never force-pushing to `main`?  
      `main` へのforce pushをしていないか？
