# {DATE} {Feature Name}

## Meta

| Field | Value |
|-------|-------|
| **Date** | {YYYY-MM-DD} |
| **Agent** | {Agent name, e.g., Freya (UX Designer)} |
| **Feature** | {Feature name} |
| **Specification** | [{Spec name}]({path-to-spec}) |
| **Status** | {Not Started / In Progress / Blocked / Complete} |

---

## Purpose

{1-3 sentences describing what this dialog accomplishes}

---

## Setup Context

{Everything an agent needs to understand the project and start working. Include:}

### Project Context

- **Project:** {Project name}
- **Tech Stack:** {e.g., React 19, Next.js 15, TypeScript, Tailwind CSS}
- **Repository:** {path or URL}

### Relevant Files

| File | Purpose |
|------|---------|
| `{path/to/file}` | {What this file does} |
| `{path/to/file}` | {What this file does} |

### Existing Patterns

{Describe any patterns the agent should follow, e.g.:}

- Component structure: {describe}
- Styling approach: {describe}
- State management: {describe}

### Current State

{What exists already that this work builds on}

---

## Scope

### In Scope

- {Feature/change 1}
- {Feature/change 2}
- {Feature/change 3}

### Out of Scope

- {Explicitly excluded item 1}
- {Explicitly excluded item 2}

### Dependencies

- {Dependency 1 — describe what must exist first}
- {Dependency 2}

---

## Steps Overview

| # | Step | Status | Notes |
|---|------|--------|-------|
| 1 | [{Step name}](steps/01-{step-name}.md) | 🔲 | |
| 2 | [{Step name}](steps/02-{step-name}.md) | 🔲 | |
| 3 | [{Step name}](steps/03-{step-name}.md) | 🔲 | |

**Status Legend:** 🔲 Not Started | 🔄 In Progress | ✅ Complete | ⏸️ Blocked | ❌ Skipped

---

## Progress Log

### {YYYY-MM-DD}

- Created dialog structure
- {Other activities}

<!--
Add entries as work progresses:

### {YYYY-MM-DD}
- Completed Step 1: {description}
- Started Step 2
- {Issues or discoveries}
-->

---

## Spec Changes Discovered

<!--
Document any specification changes or clarifications discovered during implementation.
These should be fed back to the specification files.
-->

_None yet._

<!--
Example:
| Issue | Resolution | Spec Updated? |
|-------|------------|---------------|
| Missing error state | Added to spec | ✅ |
| Unclear button label | Clarified as "Close" | 🔲 |
-->

---

## Learnings

<!--
Capture learnings for future dialogs.
-->

_None yet._

<!--
Example:
- Pattern X works well for this type of component
- Should have broken step 3 into smaller pieces
- Dependency on Y wasn't documented
-->

---

_Created using WDS Agent Dialog Workflow_
