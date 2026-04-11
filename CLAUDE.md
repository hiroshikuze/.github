# CLAUDE.md

This file provides guidance for AI assistants working in this repository.

## Repository Overview

This is the **GitHub community profile repository** (`hiroshikuze/.github`). GitHub treats a repository named `.github` as a special account-level configuration store. Files placed here apply profile-wide defaults for the account.

**Owner:** Hiroshi Kuze (`hiroshikuze`)
**Purpose:** GitHub account-level configuration — funding links, default community health files, and profile metadata.

## Repository Structure

```
.github/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md       # Bug report template (EN/JA)
│   │   ├── feature_request.md  # Feature request template (EN/JA)
│   │   └── config.yml          # Disables blank issues
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── FUNDING.yml             # GitHub Sponsors / funding button configuration
├── CLAUDE.md                   # This file
├── CODE_OF_CONDUCT.md          # Contributor Covenant-based (EN/JA)
├── CONTRIBUTING.md             # Contribution guidelines (EN/JA)
├── README.md                   # Repository documentation
└── SECURITY.md                 # Vulnerability reporting process (EN/JA)
```

### File Purposes

| File | Purpose |
|------|---------|
| `.github/FUNDING.yml` | Configures the "Sponsor" button on all repositories. |
| `.github/ISSUE_TEMPLATE/bug_report.md` | Default bug report template applied to all repos without their own. |
| `.github/ISSUE_TEMPLATE/feature_request.md` | Default feature request template. |
| `.github/ISSUE_TEMPLATE/config.yml` | Disables blank (templateless) issues. |
| `.github/PULL_REQUEST_TEMPLATE.md` | Default PR checklist for all repositories. |
| `CODE_OF_CONDUCT.md` | Community behavior standards (Contributor Covenant 2.1). |
| `CONTRIBUTING.md` | How to report bugs, request features, and submit PRs. |
| `README.md` | Repository overview. |
| `SECURITY.md` | How to responsibly disclose security vulnerabilities. |

### Language Convention

All community health files are **bilingual (English / Japanese)**:
- English first, Japanese immediately below each section.
- Inline comments in templates use `<!-- EN / JA -->` format.

## Development Conventions

### Commit Style
Commits use short, descriptive imperative messages:
```
Add custom funding link to FUNDING.yml
Add funding information for GitHub
Initial commit
```

### Branch Workflow
Feature branches follow the pattern `<tool>/<description>-<id>`, e.g.:
```
claude/add-claude-documentation-Vd2bk
```

All work should be developed on a feature branch and pushed to `origin` before merging to `main`.

### Git Push
Always push with tracking:
```bash
git push -u origin <branch-name>
```

## What Belongs Here

Appropriate additions to this repository:

- **`.github/FUNDING.yml`** — funding/sponsor configuration
- **`.github/ISSUE_TEMPLATE/`** — default issue templates for all repos without their own
- **`.github/PULL_REQUEST_TEMPLATE.md`** — default PR template
- **`.github/DISCUSSION_TEMPLATE/`** — default discussion templates
- **`.github/workflows/`** — reusable workflow templates (prefix with `workflow-templates/`)
- **`profile/README.md`** — GitHub profile README (rendered on the user's GitHub profile page)
- **`CLAUDE.md`** — this file

## What Does Not Belong Here

- Application source code
- Build tooling, package managers, or dependency files
- Language-specific linting/formatting configs
- Test suites

## No Build or Test Commands

This is a configuration-only repository. There are no build steps, no test commands, and no CI/CD pipelines. Changes are validated by GitHub automatically when pushed.

## Funding Configuration

Current `.github/FUNDING.yml`:
```yaml
github: hiroshikuze
custom: ["https://www.amazon.jp/hz/wishlist/ls/5BAWD0LZ89V9?ref_=wl_share"]
```

Supported keys: `github`, `patreon`, `open_collective`, `ko_fi`, `tidelift`, `community_bridge`, `liberapay`, `issuehunt`, `otechie`, `lfx_crowdfunding`, `polar`, `buy_me_a_coffee`, `thanks_dev`, `custom`.
