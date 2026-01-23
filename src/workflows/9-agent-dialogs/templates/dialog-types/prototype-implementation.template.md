# {DATE} {Feature Name} — Prototype Implementation

## Meta

| Field | Value |
|-------|-------|
| **Date** | {YYYY-MM-DD} |
| **Type** | 🔧 Prototype Implementation |
| **Agent** | Freya (UX Designer) |
| **Feature** | {Feature name} |
| **Specification** | [{Spec name}]({path-to-spec}) |
| **Target** | {Where to implement: app path or prototype folder} |
| **Status** | Not Started |

---

## Purpose

Implement {feature name} from specification into working code, following the section-by-section approach with approval gates.

---

## Setup Context

### Project Context

- **Project:** {Project name}
- **Tech Stack:** {e.g., React 19, Next.js 15, TypeScript, Tailwind CSS}
- **Repository:** {path}

### Specification Summary

**Page/Feature:** {Name from spec}

**States/Variants:**
- {State 1}
- {State 2}
- {etc.}

**Key Sections:**
| Section | Object IDs | Priority |
|---------|------------|----------|
| {Section 1} | `{object-id-1}`, `{object-id-2}` | High |
| {Section 2} | `{object-id-3}` | Medium |

### Existing Code

| File | Purpose | Status |
|------|---------|--------|
| `{path/to/file}` | {What it does} | {Exists / To Create} |

### Design System Components

| Component | Path | Notes |
|-----------|------|-------|
| [{Component}]({path}) | `{import path}` | {Usage notes} |

---

## Scope

### In Scope

- {Section/feature 1}
- {Section/feature 2}
- Translations (SE/EN)
- Accessibility (WCAG AA)

### Out of Scope

- {Explicitly excluded}
- Backend/API changes (unless specified)

### Dependencies

- [ ] {Dependency 1} — {status}
- [ ] {Dependency 2} — {status}

---

## Implementation Approach

### Section-by-Section

Each section is implemented and approved before moving to the next:

1. **Build section** — Implement the code
2. **Test section** — Verify against spec
3. **User approval** — Confirm it's correct
4. **Next section** — Move forward

### Approval Criteria

- [ ] Matches specification visually
- [ ] All Object IDs present
- [ ] Translations work (SE/EN toggle)
- [ ] Accessibility requirements met
- [ ] No TypeScript errors

---

## Steps Overview

| # | Section | Status | Approved |
|---|---------|--------|----------|
| 1 | [{Section name}](steps/01-{section}.md) | 🔲 | 🔲 |
| 2 | [{Section name}](steps/02-{section}.md) | 🔲 | 🔲 |
| 3 | [{Section name}](steps/03-{section}.md) | 🔲 | 🔲 |

**Status:** 🔲 Not Started | 🔄 In Progress | ✅ Complete | ⏸️ Blocked
**Approved:** 🔲 Pending | ✅ Approved | 🔁 Needs Changes

---

## Progress Log

### {YYYY-MM-DD}

- Created dialog from specification
- Identified {N} sections to implement

<!--
### {YYYY-MM-DD}
- Completed Section 1: {name}
- User approved ✅
- Started Section 2
-->

---

## Spec Changes Discovered

<!--
Document any issues with the specification found during implementation.
-->

| Issue | Resolution | Spec Updated? |
|-------|------------|---------------|
| _None yet_ | | |

---

## Testing Checklist

### Per-Section Testing

- [ ] Visual match to specification
- [ ] Object IDs present and correct
- [ ] Translations toggle correctly
- [ ] Touch targets ≥ 44px
- [ ] Keyboard navigation works

### Final Integration Testing

- [ ] All sections work together
- [ ] State transitions correct
- [ ] No console errors
- [ ] Responsive (if applicable)

---

## Learnings

<!--
Capture learnings for future prototype implementations.
-->

_None yet._

---

_Prototype Implementation Dialog — WDS Agent Dialog Workflow_
