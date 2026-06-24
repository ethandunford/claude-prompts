# claude-prompts

A collection of reusable Claude prompts for software engineering workflows — project discovery, auditing, technical review, and epic delivery.

## Prompts

### project-discovery.md
Runs a multi-discipline AI team (Business Analyst, Solutions Architect, DB Architect, Frontend/Backend Engineers, DevOps, QA, Security) through a structured discovery process for greenfield projects. Covers three phases: discovery questions → synthesis → full business analysis document output.

### project-audit.md
Deep codebase audit prompt for a Senior Software Architect role. Covers project overview, tech stack, architecture, core business logic, code quality, data flow, performance, security, technical debt, and improvement opportunities. Outputs to `docs/project-audit.md`.

### project-review.md
Daily delivery review prompt for a Senior Technical Project Reviewer role. Covers recent work validation, ticket closure, hygiene, roadmap updates, and generating a prioritised 10-ticket work queue for the session.

### technical-review.md
Variant of the daily project review that also includes a mandatory first step to read `docs/project-audit.md` before proceeding. Use this version on projects that maintain an audit document.

### review.md
Companion rules fragment for the daily review prompts. Defines the review file format: one entry per day, timestamped, append-only, with a fixed per-entry structure.

### senior-.net.md
Structured code review prompt for a Senior / Lead C# .NET Engineer role. Covers architecture, code quality, performance, security, ASP.NET Core best practices, error handling, testability, and prioritised actionable improvements.

### seo-epic.md
Full epic delivery prompt for SEO work. Acts as a Senior Full-Stack Developer, Technical SEO Consultant, and Software Architect. Covers audit, branch strategy, implementation, documentation (`docs/seo-audit.md`), and PR creation. Used as the reference style for all prompts in this repo.

### template.md
Generic epic implementation prompt derived from `seo-epic.md`. Swap the `{{PLACEHOLDER}}` tokens for your domain and use it to scaffold any new epic prompt.

## Template Placeholders

| Placeholder | Description |
|---|---|
| `{{EPIC_NAME}}` | Name of the epic (e.g. `SEO Epic`, `Auth Overhaul`) |
| `{{ROLE_1/2/3}}` | Engineering roles for the prompt persona |
| `{{DOMAIN}}` | The work domain (e.g. `SEO`, `Auth`, `Payments`) |
| `{{ISSUE_LABEL}}` | GitHub issue label to target (e.g. `seo`, `auth`) |
| `{{DOMAIN_AUDIT_DOC}}` | Audit doc filename without extension (e.g. `seo-audit`) |
| `{{BRANCH_NAME}}` | Feature branch name (e.g. `seo-epic`) |
| `{{TARGET_BRANCH}}` | PR target branch (e.g. `dev`, `main`) |
| `{{AUDIT_AREA_*}}` | Areas to audit in the repository |
| `{{REVIEW_CATEGORY_*}}` / `{{REVIEW_ITEM}}` | Domain-specific review categories and items |
| `{{VERIFY_CHECK_*}}` / `{{DOMAIN_CHECK_*}}` | Build/test/domain validation checklist items |
| `{{PR_TITLE_SUMMARY}}` | Short summary for the PR title |

## Conventions

All prompts follow a shared formatting convention:

- Single H1 title at the top
- Plain `You are a …` role declaration (no bold, no "acting as")
- `##` / `###` / `####` heading hierarchy — no emoji, no numbered prefixes
- `---` horizontal rules between top-level sections
- File paths and labels in ` ```text ``` ` blocks
