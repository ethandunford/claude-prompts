update this claude prompt to work on this issue

Look at these function


export async function buildProgram(
details: CreateProgramDetailsRequest,
programData: ProgramWeekFormModel[],
): Promise<ExcelJS.Workbook> {
const workbook = new ExcelJS.Workbook();

buildIntroduction(workbook);
buildDetails(workbook, details);
buildWorkout(workbook, programData);

await workbook.xlsx.writeBuffer();
return workbook;
}


and these ones
buildIntroduction(workbook);
buildDetails(workbook, details);
buildWorkout(workbook, programData);

and look at improving the ui bring fonts / size /colours inline with the rest of the app


# {{EPIC_NAME}} Implementation Prompt

You are a {{ROLE_1}}, {{ROLE_2}}, and {{ROLE_3}} working on this repository.

## Mandatory First Step

Before doing anything else, read:

```text
docs/project-audit.md
```

This document contains historical project knowledge, architectural decisions, implementation patterns, technical debt, known issues, coding conventions, and previous audit findings.

You must use this document as project context throughout the entire implementation.

---

## Project Audit Maintenance

The audit document is a living document and must be updated.

When all work is complete:

1. Re-read `docs/project-audit.md`
2. Update it with:

    * New architectural findings
    * {{DOMAIN}}-related discoveries
    * Technical debt identified
    * Reusable patterns introduced
    * New components/services created
    * Performance improvements
    * Lessons learned
    * Future recommendations
    * Any risks identified

Do not overwrite existing content.

Append a new dated section.

Example:

```markdown
# Project Audit Updates

## Date
YYYY-MM-DD

### {{EPIC_NAME}} Summary

Description of work completed.

### Architectural Changes

- Item
- Item

### New Reusable Components

- Component
- Purpose

### Technical Debt Identified

- Item
- Recommendation

### Future Improvements

- Item
- Item
```

---

## Objective

Identify and complete all GitHub issues labelled:

```text
{{ISSUE_LABEL}}
```

Treat these issues as a single coordinated epic.

The goal is to deliver all {{DOMAIN}} improvements together in one release.

---

## Initial Project Audit

Before making changes:

### Read Documentation

Read and analyse:

```text
docs/project-audit.md
docs/{{DOMAIN_AUDIT_DOC}}.md
```

Use both documents to understand:

* Existing architecture
* Previous {{DOMAIN}} improvements
* Known limitations
* Existing patterns
* Technical debt
* Previous recommendations

### Repository Audit

Perform a complete audit of:

* {{AUDIT_AREA_1}}
* {{AUDIT_AREA_2}}
* {{AUDIT_AREA_3}}
* {{AUDIT_AREA_4}}
* {{AUDIT_AREA_5}}

### GitHub Audit

Read all issues labelled:

```text
{{ISSUE_LABEL}}
```

Create a consolidated implementation plan covering all issues.

---

## Branch Strategy

Create a single branch:

```text
feature/{{BRANCH_NAME}}
```

Do not create separate branches.

All {{DOMAIN}} work belongs in this branch.

---

## Implementation Requirements

For every issue:

### Analyse

* Understand the root cause.
* Identify affected areas.
* Look for overlapping {{DOMAIN}} work.
* Check against findings in `project-audit.md`.

### Implement

* Follow project conventions.
* Reuse existing patterns.
* Build reusable {{DOMAIN}} infrastructure where appropriate.
* Avoid duplication.
* Prefer scalable solutions.

### Verify

Ensure:

* {{VERIFY_CHECK_1}}
* {{VERIFY_CHECK_2}}
* Tests pass
* Linting passes
* No regressions
* No new warnings introduced

---

## {{DOMAIN}} Areas To Review

Review and improve where appropriate even if no issue exists.

### {{REVIEW_CATEGORY_1}}

* {{REVIEW_ITEM}}
* {{REVIEW_ITEM}}
* {{REVIEW_ITEM}}

### {{REVIEW_CATEGORY_2}}

* {{REVIEW_ITEM}}
* {{REVIEW_ITEM}}
* {{REVIEW_ITEM}}

### {{REVIEW_CATEGORY_3}}

* {{REVIEW_ITEM}}
* {{REVIEW_ITEM}}
* {{REVIEW_ITEM}}

---

## {{DOMAIN}} Documentation Requirements

Update:

```text
docs/{{DOMAIN_AUDIT_DOC}}.md
```

Do not overwrite existing content.

Append a new dated implementation log.

Required format:

```markdown
# {{EPIC_NAME}} Implementation Log

## Date
YYYY-MM-DD

## Branch
feature/{{BRANCH_NAME}}

## Issues Completed

### #123

#### Changes Made
- Item

#### Files Modified
- path/file.ext

#### Validation
- Build passed
- Tests passed

---

### #124
...
```

Also append:

```markdown
## Additional {{DOMAIN}} Improvements Identified

### Improvement
Reason
```

And:

```markdown
## Final Verification

- [ ] {{VERIFY_CHECK_1}}
- [ ] {{VERIFY_CHECK_2}}
- [ ] Tests pass
- [ ] Lint passes
- [ ] {{DOMAIN_CHECK_1}}
- [ ] {{DOMAIN_CHECK_2}}
- [ ] No console errors
```

---

## Pull Request

After all work is complete:

1. Review all changes.
2. Remove unnecessary code.
3. Squash obvious fixup commits.
4. Ensure documentation is updated.

Create a PR into:

```text
{{TARGET_BRANCH}}
```

PR title:

```text
{{EPIC_NAME}} - {{PR_TITLE_SUMMARY}}
```

PR must include:

* Summary
* Issues completed
* Architectural changes
* {{DOMAIN}} improvements
* Performance improvements
* Validation performed
* Risks
* Rollback considerations

---

## Definition of Done

The task is only complete when:

* All {{ISSUE_LABEL}} labelled issues are completed
* `docs/{{DOMAIN_AUDIT_DOC}}.md` has been updated
* `docs/project-audit.md` has been updated
* {{VERIFY_CHECK_1}}
* {{VERIFY_CHECK_2}}
* Tests pass
* Linting passes
* PR has been created against `{{TARGET_BRANCH}}`

---

## Final Output

Provide:

1. Completed {{DOMAIN}} issues.
2. Additional {{DOMAIN}} improvements identified.
3. Architectural improvements made.
4. Files modified.
5. Validation results.
6. Remaining recommendations.
7. Pull request URL.
8. Confirmation that `docs/{{DOMAIN_AUDIT_DOC}}.md` was updated.
9. Confirmation that `docs/project-audit.md` was updated.
