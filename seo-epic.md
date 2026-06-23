# Claude SEO Epic Implementation Prompt

You are a Senior Full-Stack Developer, Senior Technical SEO Consultant, and Senior Software Architect working on this repository.

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
    * SEO-related discoveries
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

### SEO Epic Summary

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
seo
```

Treat these issues as a single coordinated epic.

The goal is to deliver all SEO improvements together in one release.

---

## Initial Project Audit

Before making changes:

### Read Documentation

Read and analyse:

```text
docs/project-audit.md
docs/seo-audit.md
```

Use both documents to understand:

* Existing architecture
* Previous SEO improvements
* Known limitations
* Existing patterns
* Technical debt
* Previous recommendations

### Repository Audit

Perform a complete audit of:

* Frontend application
* Backend/API
* Marketing website
* Build configuration
* Routing
* Metadata generation
* Sitemap generation
* Robots.txt configuration
* Structured data/schema markup
* Open Graph tags
* Twitter/X cards
* Canonical URLs
* Internal linking
* Page performance
* Accessibility issues impacting SEO
* Core Web Vitals opportunities
* Image optimisation
* SSR/SSG configuration
* Internationalisation/hreflang support

### GitHub Audit

Read all issues labelled:

```text
seo
```

Create a consolidated implementation plan covering all issues.

---

## Branch Strategy

Create a single branch:

```text
feature/seo-epic
```

Do not create separate branches.

All SEO work belongs in this branch.

---

## Implementation Requirements

For every issue:

### Analyse

* Understand the root cause.
* Identify affected areas.
* Look for overlapping SEO work.
* Check against findings in `project-audit.md`.

### Implement

* Follow project conventions.
* Reuse existing patterns.
* Build reusable SEO infrastructure where appropriate.
* Avoid duplication.
* Prefer scalable solutions.

### Verify

Ensure:

* Frontend builds
* Backend builds
* Tests pass
* Linting passes
* No TypeScript errors
* No C# warnings introduced
* No SEO regressions
* No accessibility regressions

---

## SEO Areas To Review

Review and improve where appropriate even if no issue exists.

### Technical SEO

* Meta titles
* Meta descriptions
* Canonical tags
* Robots directives
* Sitemap generation
* Structured data
* Breadcrumb schema
* FAQ schema
* Organisation schema
* Product schema
* Article schema

### Performance SEO

* Core Web Vitals
* Bundle size
* Lazy loading
* Image optimisation
* Critical rendering path
* Lighthouse SEO score

### Content SEO

* Heading hierarchy
* Duplicate titles
* Duplicate descriptions
* Internal linking
* Thin content

### Social SEO

* Open Graph
* Twitter Cards
* Social previews

### International SEO

* hreflang
* Locale handling
* Language metadata

---

## SEO Documentation Requirements

Update:

```text
docs/seo-audit.md
```

Do not overwrite existing content.

Append a new dated implementation log.

Required format:

```markdown
# SEO Epic Implementation Log

## Date
YYYY-MM-DD

## Branch
feature/seo-epic

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
## Additional SEO Improvements Identified

### Improvement
Reason
```

And:

```markdown
## Final Verification

- [ ] Frontend builds
- [ ] Backend builds
- [ ] Tests pass
- [ ] Lint passes
- [ ] Sitemap validated
- [ ] Robots validated
- [ ] Structured data validated
- [ ] Canonicals validated
- [ ] Open Graph validated
- [ ] No broken routes
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
dev
```

PR title:

```text
SEO Epic - Complete all SEO labelled issues
```

PR must include:

* Summary
* Issues completed
* Architectural changes
* SEO improvements
* Performance improvements
* Validation performed
* Risks
* Rollback considerations

---

## Definition of Done

The task is only complete when:

* All SEO labelled issues are completed
* `docs/seo-audit.md` has been updated
* `docs/project-audit.md` has been updated
* Frontend builds successfully
* Backend builds successfully
* Tests pass
* Linting passes
* PR has been created against `dev`

---

## Final Output

Provide:

1. Completed SEO issues.
2. Additional SEO improvements identified.
3. Architectural improvements made.
4. Files modified.
5. Validation results.
6. Remaining recommendations.
7. Pull request URL.
8. Confirmation that `docs/seo-audit.md` was updated.
9. Confirmation that `docs/project-audit.md` was updated.
