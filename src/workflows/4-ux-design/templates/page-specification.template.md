### {page-number}-{page-name}

**Previous Step:** ← [{previous-page-name}]({previous-page-path})
**Next Step:** → [{next-page-name}]({next-page-path})

![{Page Name}](Sketches/{page-number}-{page-name}.jpg)

# {page-number}-{page-name}

## Page Metadata

| Property | Value |
|----------|-------|
| **Scenario** | {scenario-name} |
| **Page Number** | {page-number} |
| **Platform** | {Mobile web / Desktop / PWA / Native} |
| **Page Type** | {Full Page / Modal / Drawer / Popup} |
| **Viewport** | {Mobile-first / Desktop-first} |
| **Interaction** | {Touch-first / Mouse+keyboard} |
| **Visibility** | {Public / Authenticated / Admin} |

---

## Overview

**Page Purpose:** {What job must this page accomplish?}

**User Situation:** {What brings the user here?}

**Success Criteria:** {How will we know this page succeeded?}

**Entry Points:**
- {How users arrive}

**Exit Points:**
- {Where users go next}

---

## Reference Materials

**Strategic Foundation:**
- [Product Brief]({path}) - {brief description}
- [Trigger Map]({path}) - {brief description}

**Related Pages:**
- [{Related Page}]({path})

**Design System:**
- [{Component}]({path})

---

## Layout Structure

{High-level description of page layout}

```
[ASCII layout diagram]
+------------------+
| Header           |
+------------------+
| Main Content     |
+------------------+
| Footer           |
+------------------+
```

---

## Page Sections

### Section: {Section Name}

**OBJECT ID:** `{page-name}-{section-name}`

| Property | Value |
|----------|-------|
| Purpose | {What this section does} |
| Component | [{Design System Component}]({path}) |

---

#### {Object Name}

**OBJECT ID:** `{page-name}-{object-name}`

| Property | Value |
|----------|-------|
| Component | [{Component}]({path}) |
| Translation Key | `{translation.key}` |
| SE | "{Swedish text}" |
| EN | "{English text}" |
| Behavior | {onClick / onChange / etc.} |

---

#### {Group Name} (Container)

**OBJECT ID:** `{page-name}-{group-name}`

| Property | Value |
|----------|-------|
| Component | [{Container Component}]({path}) |
| Purpose | {Groups related objects} |
| Layout | {Horizontal / Vertical / Grid} |

##### {Object in Group}

**OBJECT ID:** `{page-name}-{group-name}-{object}`

| Property | Value |
|----------|-------|
| Component | [{Component}]({path}) |
| Translation Key | `{translation.key}` |
| SE | "{Swedish text}" |
| EN | "{English text}" |

##### {Object in Group 2}

**OBJECT ID:** `{page-name}-{group-name}-{object-2}`

| Property | Value |
|----------|-------|
| Component | [{Component}]({path}) |
| Translation Key | `{translation.key}` |
| SE | "{Swedish text}" |
| EN | "{English text}" |

---

## Page States

| State | When | Appearance | Actions |
|-------|------|------------|---------|
| Default | {condition} | {description} | {available actions} |
| Loading | {condition} | {description} | {available actions} |
| Empty | {condition} | {description} | {available actions} |
| Error | {condition} | {description} | {recovery actions} |
| Success | {condition} | {description} | {next steps} |

---

## Conditional Sections

Include these micro-instructions when applicable:

| Condition | Include |
|-----------|---------|
| Public page (SEO needed) | → [meta-content.instructions.md](instructions/meta-content.instructions.md) |
| Has forms/inputs | → [form-validation.instructions.md](instructions/form-validation.instructions.md) |
| Needs API data | → [data-api.instructions.md](instructions/data-api.instructions.md) |
| Multiple breakpoints | → [responsive.instructions.md](instructions/responsive.instructions.md) |
| Final review | → [accessibility.instructions.md](instructions/accessibility.instructions.md) |
| Multiple sketches | → [storyboard-specification.template.md](storyboard-specification.template.md) |

---

## Technical Notes

{Any constraints, performance requirements, or implementation notes}

---

## Checklist

- [ ] Page purpose clear
- [ ] All Object IDs assigned
- [ ] Components reference design system
- [ ] Translations complete (SE/EN)
- [ ] States documented
- [ ] Conditional sections included where needed

---

**Previous Step:** ← [{previous-page-name}]({previous-page-path})
**Next Step:** → [{next-page-name}]({next-page-path})

---

_Created using Whiteport Design Studio (WDS) methodology_
