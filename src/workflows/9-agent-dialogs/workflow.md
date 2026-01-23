---
name: Agent Dialog Workflow
description: Create structured agent dialog folders for implementation tasks with isolated context and reproducible instructions
web_bundle: true
---

# Agent Dialog Workflow

**Goal:** Create structured, documented agent dialog folders that enable isolated, reproducible implementation tasks.

**Your Role:** Guide the user through creating an agent dialog structure that captures scope, context, and step-by-step instructions for implementation work.

---

## OVERVIEW

Agent Dialogs solve these problems:

| Problem | Solution |
|---------|----------|
| Context window limits | Each step is a fresh agent dialog |
| Lost planning work | Everything documented in files |
| Handoff to others | Complete instructions, anyone can execute |
| Resumability | Pick up where you left off |
| Reproducibility | Same inputs → same outputs |

**Key Insight:** By structuring implementation work into documented dialog folders, we create:
- **Isolation** — Each step can run in a fresh context
- **Traceability** — Clear record of what was planned and executed
- **Replayability** — Instructions can be rerun if needed
- **Handoff** — Different agents or humans can continue the work

---

## WHEN TO USE

Use this workflow when:
- ✅ Implementing features from specifications
- ✅ Making changes across multiple files
- ✅ Work that benefits from step-by-step documentation
- ✅ Tasks that might need to be resumed later
- ✅ Work that could be handed off to another agent/person
- ✅ **Saving ideas for later** — Capture work when you don't have time now

Skip this workflow when:
- ❌ Simple one-file changes
- ❌ Quick fixes that don't need documentation
- ❌ Exploratory work where the path is unclear

---

## AGENT STARTUP PROTOCOL

**When an agent is awakened, it should check for pending dialogs.**

### Startup Check

```
1. Check: docs/F-Agent-Dialogs/
2. Find dialogs where:
   - Status = "Not Started" or "In Progress"
   - Agent matches the awakened agent
3. Present pending dialogs to user:
   "You have X pending dialogs:
    - [DATE] Feature Name (Status)
    - [DATE] Feature Name (Status)

    Would you like to continue one of these?"
```

### Dialog States

| Status | Meaning |
|--------|---------|
| **Not Started** | Dialog created but no steps executed |
| **In Progress** | Some steps complete, work ongoing |
| **Blocked** | Waiting on external dependency |
| **On Hold** | Deliberately paused |
| **Complete** | All steps finished |

This ensures no captured work is forgotten.

---

## CAPTURE DIALOGS

When you have an idea but no time to execute:

### Capture Flow

1. **Create minimal dialog** — Just the main file
2. **Capture the essence:**
   - What's the idea/task?
   - What specification is it based on?
   - Any initial thoughts on approach?
3. **Set status:** "Not Started"
4. **Done** — Pick it up later

### Minimal Dialog Structure

For "save for later" dialogs, you can skip step files initially:

```
F-Agent-Dialogs/
└── 2026-01-23-booking-details-drawer/
    └── 2026-01-23-booking-details-drawer-dialog.md  ← Just this file
```

When you return:
1. Agent startup check finds it
2. You continue with Step 2 (Analyze Scope)
3. Create step files as needed

---

## DIALOG TYPES

Choose the right template for your work. See [templates/dialog-types/INDEX.md](templates/dialog-types/INDEX.md).

| Type | Icon | Use When |
|------|------|----------|
| **Prototype Implementation** | 🔧 | Building UI from specifications |
| **Bug Fix** | 🐛 | Fixing issues and defects |
| **Design Exploration** | 🎨 | Exploring visual/UX directions |
| **Capture** | 💾 | Saving ideas for later |
| **Generic** | 📋 | Anything else |

Each type has a specialized template with relevant sections pre-configured.

---

## FOLDER STRUCTURE

```
docs/F-Agent-Dialogs/
└── {DATE}-{feature-name}/
    ├── {DATE}-{feature-name}-dialog.md    ← Main file (meta, purpose, setup, progress)
    └── steps/
        ├── 01-{step-name}.md              ← Self-contained step instructions
        ├── 02-{step-name}.md
        └── ...
```

**Naming Convention:**
- Date format: `YYYY-MM-DD`
- Feature name: lowercase, hyphenated (e.g., `booking-details-drawer`)
- Step files: numbered prefix with descriptive name

---

## THE DIALOG FILE

The main dialog file (`{DATE}-{feature-name}-dialog.md`) contains everything needed to understand and manage the implementation work.

### Required Sections

1. **Meta** — Date, agent, feature, specification reference, status
2. **Purpose** — What this dialog accomplishes
3. **Setup Context** — All context an agent needs to start fresh
4. **Scope** — What's in/out, dependencies
5. **Steps Overview** — Table tracking progress across all steps
6. **Progress Log** — Chronological record of work done

See template: [templates/dialog.template.md](templates/dialog.template.md)

---

## STEP FILES

Each step file is **self-contained** — an agent with no prior context can execute it.

### Required Sections

1. **Context** — Brief context (what exists, what we're adding)
2. **Specification Reference** — Relevant excerpt from the spec
3. **Task** — Clear description of what to implement
4. **Files to Modify** — Explicit list of files
5. **Implementation Details** — Specific guidance, patterns to follow
6. **Acceptance Criteria** — Checklist for "done"
7. **Test Instructions** — How to verify the implementation

See template: [templates/step.template.md](templates/step.template.md)

---

## WORKFLOW PHASES

### Phase 1: Dialog Initialization

**What:** Create the dialog folder and main file

**Steps:**
1. Determine the feature/implementation to work on
2. Create folder: `docs/F-Agent-Dialogs/{DATE}-{feature-name}/`
3. Create main dialog file from template
4. Fill in Meta, Purpose, and Setup Context sections

**Go to:** [steps/step-01-initialize-dialog.md](steps/step-01-initialize-dialog.md)

---

### Phase 2: Scope Analysis

**What:** Analyze the specification and determine scope

**Steps:**
1. Read the relevant specification(s)
2. Identify what needs to be implemented
3. Note any spec changes or clarifications needed
4. Document in the Scope section

**Go to:** [steps/step-02-analyze-scope.md](steps/step-02-analyze-scope.md)

---

### Phase 3: Step Breakdown

**What:** Break the work into discrete, implementable steps

**Steps:**
1. Identify logical sections/features to implement
2. Order them by dependencies (what must come first)
3. Create step files for each
4. Update Steps Overview table in dialog file

**Go to:** [steps/step-03-create-steps.md](steps/step-03-create-steps.md)

---

### Phase 4: Step Execution

**What:** Execute each step (can be in fresh agent dialogs)

**Steps:**
1. Open step file
2. Execute the instructions
3. Verify against acceptance criteria
4. Update status in dialog file
5. Log progress
6. Repeat for next step

**Go to:** [steps/step-04-execute-steps.md](steps/step-04-execute-steps.md)

---

### Phase 5: Completion

**What:** Finalize the dialog and capture learnings

**Steps:**
1. Verify all steps complete
2. Document any spec changes discovered
3. Note learnings for future dialogs
4. Update final status

**Go to:** [steps/step-05-complete-dialog.md](steps/step-05-complete-dialog.md)

---

## INITIALIZATION

### First Step Execution

To begin, load and execute [steps/step-01-initialize-dialog.md](steps/step-01-initialize-dialog.md).

**User Input Needed:**
- What feature/implementation are we working on?
- Which specification(s) are relevant?
- What's the target location for the dialog folder?

---

## BEST PRACTICES

### Dialog Files

- **Be thorough in Setup Context** — Assume the agent has zero prior knowledge
- **Include file paths** — Always use absolute or project-relative paths
- **Reference specifications** — Link to the source specs, don't duplicate
- **Track progress** — Update the Steps Overview table after each step

### Step Files

- **One clear task** — Each step should accomplish one thing
- **Self-contained** — Include all context needed to execute
- **Specific criteria** — Acceptance criteria should be verifiable
- **Test instructions** — Always include how to verify the work

### Execution

- **Fresh context is fine** — Steps are designed to work in isolation
- **Update as you go** — Don't wait to update progress
- **Capture discoveries** — Note spec changes or issues found

---

## EXAMPLES

### Example: Feature Implementation Dialog

```
2026-01-23-booking-details-drawer/
├── 2026-01-23-booking-details-drawer-dialog.md
└── steps/
    ├── 01-drawer-shell.md
    ├── 02-date-display.md
    ├── 03-dog-info-section.md
    ├── 04-status-badge.md
    ├── 05-action-buttons.md
    └── 06-state-transitions.md
```

### Example: Bug Fix Dialog

```
2026-01-23-calendar-scroll-fix/
├── 2026-01-23-calendar-scroll-fix-dialog.md
└── steps/
    ├── 01-reproduce-issue.md
    ├── 02-implement-fix.md
    └── 03-verify-fix.md
```

### Example: Capture Dialog

```
2026-01-23-user-settings-page/
└── 2026-01-23-user-settings-page-dialog.md   ← Just this file, expand later
```

---

## INTEGRATION WITH OTHER WORKFLOWS

Agent Dialogs can be created from:

- **Interactive Prototypes Workflow** — Each section becomes a step
- **UX Design Workflow** — Specification implementation becomes a dialog
- **Design System Workflow** — Component creation becomes a dialog

The Agent Dialog structure provides a consistent way to document and execute implementation work from any source.

---

_Agent Dialog Workflow — Structured, reproducible implementation with isolated context_
