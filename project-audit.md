# Project Audit

You are a Senior Software Architect and Principal Engineer working on this repository.

At the start of this session, you must perform a deep, structured audit of the entire codebase to build strong context for all future work.

This audit is not optional. It is the foundation for all subsequent tasks.

---

## Task: Full Project Audit

You must explore the repository thoroughly and produce a comprehensive technical audit covering:

### Project Overview
- What is this project?
- Primary purpose and domain
- High-level architecture summary

### Tech Stack Identification
- Frontend frameworks and libraries
- Backend technologies
- Build tools and tooling (Vite, Webpack, etc.)
- Database and ORM (if applicable)
- Deployment / infrastructure hints

### Folder & Architecture Analysis
- Explain the folder structure
- Identify key modules/domains
- Highlight any architectural patterns (MVC, Clean Architecture, modular, etc.)
- Identify any inconsistencies or unclear structure

### Core Business Logic
- Identify main features and flows
- Key services, APIs, or domains
- Critical business rules embedded in code

### Component / Module Quality Review
- Reusable patterns vs duplicated logic
- Opportunities for shared base components/services
- Signs of tight coupling or poor separation of concerns

### Data Flow Analysis
- How data moves through the system
- State management approach (if frontend)
- API communication patterns

### Code Quality Observations
- Consistency of patterns
- Naming conventions
- Error handling approach
- Type safety (if TypeScript etc.)
- Test coverage presence/absence

### Performance & Scalability Risks
- Potential bottlenecks
- Inefficient rendering / queries / loops
- API inefficiencies
- Frontend performance concerns

### Security Considerations
- Authentication / authorization approach
- Any exposed secrets or risky patterns
- Input validation concerns

### Technical Debt & Risks
- Areas likely to break or scale poorly
- Legacy or hacky implementations
- TODO/FIXME hotspots

### Improvement Opportunities
- High-impact refactors
- Architecture improvements
- Reusability improvements
- Suggested component/service abstractions

---

## Output Requirements

You must:

1. Produce a single markdown document called:

   `docs/project-audit.md`

2. Structure it exactly as:

```md
# Project Audit

## Overview
...

## Tech Stack
...

## Architecture
...

## Core Business Logic
...

## Component & Module Review
...

## Data Flow
...

## Code Quality
...

## Performance & Scalability
...

## Security
...

## Technical Debt
...

## Recommendations
...
```