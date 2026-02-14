# Trigger Map Initiation Pattern

**Status:** Design Phase
**Created:** 2026-02-12
**Purpose:** How completed Trigger Map initiates scenario creation through Dialog, Suggest, or Dream modes

**Part of:** Dream It Up project (ultimate goal: agent-driven scenario generation)

---

## The Problem

After completing Product Brief and Trigger Map, designers face a blank canvas:
- Which scenarios should we document?
- How do we ensure complete page coverage?
- Should this be screen flow or storyboard?
- How do personas map to scenarios?

**Current state:** Designer manually decides what to document
**Result:** Pages get missed, scenarios feel arbitrary, coverage is incomplete

---

## The Solution: Trigger Map Initiation

**Core Principle:** Scenarios are **visual walkthroughs** that expose all pages for scrutiny.

When Trigger Map completes, the agent initiates scenario creation through one of three conversation modes:

1. **Dialog** — Collaborative discovery (large products, strategic scoping needed)
2. **Suggest** — Propose then execute (medium complexity, needs validation)
3. **Dream** — Autonomous execution (simple/obvious structure)

**All modes ensure:**
- Complete page coverage (small sites) or strategic focus (large products)
- Appropriate format (screen flow vs storyboard)
- Natural mapping to persona driving forces
- Clear rationale for organization

**User's role:** Collaborate (Dialog), approve structure (Suggest), or review result (Dream).

---

## When Trigger Map Initiation Runs

**Trigger:** Immediately after Trigger Map (Phase 2) completion

**Prerequisites:**
- ✅ Product Brief complete (Phase 1)
- ✅ Trigger Map complete with aligned personas and driving forces (Phase 2)
- ✅ Site/app type identified (presentation site vs dynamic app)

**Workflow Position:**
```
Phase 1: Product Brief
    ↓
Phase 2: Trigger Map
    ↓
Phase 3: Trigger Map Initiation  ← Initiates scenarios (Dialog/Suggest/Dream)
    ↓
Phase 4: UX Scenarios  ← Documents approved/created scenarios
```

---

## Purpose of Scenarios

**Scenarios are visual walkthroughs that force detailed thinking.**

### Core Functions

1. **Expose pages for scrutiny** — Code hides pages, scenarios reveal them all
2. **Force detailed thinking** — Can't skip details when walking through interactions
3. **Learning mechanism** — Designer discovers system patterns through deep work on critical flows
4. **Create shared understanding** — Walkable artifact for validation with stakeholders

**The Learning Effect:** When designer works deeply on business-critical flows, patterns emerge that make the rest of the product easier to design. Deep work on 20% reveals insights for the other 80%.

---

## Product Scale Strategy

### Small Sites (20-50 pages)
**Approach:** Comprehensive coverage

- Document all pages across scenarios
- Natural groupings by navigation, service types, content categories
- Complete visibility of entire site

**Example:** Källa Fordonservice (13 vehicle pages + services + info)

### Large Products (100s+ pages)
**Approach:** Selective ignorance

- Focus on single most valuable workflow
- Ignore less critical pages strategically
- Learning effect: Deep work on core flow reveals patterns for rest

**Example:** Complex SaaS with admin, user, reporting, settings → Focus on primary user workflow only

**Why this works:** You can't document everything in a 1000-page enterprise app. But documenting the most business-critical flow deeply teaches you the system's patterns.

---

## Three Conversation Modes

Trigger Map Initiation adapts its autonomy level through three conversation modes, selected based on product complexity and strategic clarity needed.

### Mode 1: Dialog (Collaborative Discovery)

**Use when:**
- Large products where selective ignorance is needed
- Strategic clarity required upfront (which flow matters most?)
- Product type demands careful scoping

**Opening:**
"What's the most important flow for this type of product?"

**Process:**
1. Agent asks strategic question about most valuable workflow
2. Collaborative discussion identifies critical scenario(s)
3. Walk through screen-by-screen together
4. Designer learns system through exploration
5. Document critical flow
6. Rest becomes easier due to patterns learned

**Example:** Enterprise SaaS → Start with "Which workflow drives the most business value?"

### Mode 2: Suggest (Propose Then Execute)

**Use when:**
- Medium complexity (clear structure, but needs validation)
- Natural groupings exist but user should approve organization
- Standard presentation sites

**Opening:**
"Based on your Trigger Map, I'm imagining [N] scenarios: [list with rationale]. Does this make sense?"

**Process:**
1. Agent analyzes Trigger Map
2. Proposes scenario structure with coverage rationale
3. User approves/adjusts
4. Agent documents approved scenarios

**Example:** Service business site → Agent suggests grouping by service type + info pages

### Mode 3: Dream (Autonomous Execution)

**Use when:**
- Simple, clear structure
- Pattern is obvious from Trigger Map
- User trusts agent autonomy

**Opening:**
"I've created [N] scenarios covering [coverage summary]. Here's what I documented..."

**Process:**
1. Agent analyzes Trigger Map
2. Creates scenarios autonomously
3. Presents result for review/adjustment

**Example:** Simple portfolio site with obvious structure

**Mode Selection:** Agent determines appropriate mode based on:
- Product scale (small vs large)
- Structural clarity (obvious vs ambiguous)
- Strategic importance (high-stakes vs straightforward)

---

## Two-Step Process

### Step 1: Suggest Scenarios

**Agent presents:**
- Scenario title (user's purpose)
- Which pages it covers
- Why this scenario matters (persona driving force connection)
- How many scenarios total (ensure coverage)

**Agent format:**
```markdown
Based on your Trigger Map, I'm imagining [N] scenarios:

**Scenario 1: [Purpose Title]**
- **Purpose:** [User's reason for visiting]
- **Pages:** [List of pages covered]
- **Persona:** [Name] ([Driving Force])
- **Why:** [Rationale for this grouping]

**Scenario 2: [Purpose Title]**
- **Purpose:** [User's reason for visiting]
- **Pages:** [List of pages covered]
- **Persona:** [Name] ([Driving Force])
- **Why:** [Rationale for this grouping]

**Coverage:** All pages exposed across [N] scenarios, no repetition
**Format:** [Screen flow / Storyboard / Mixed]
```

**User response:** Approve all, adjust specific scenarios, or suggest different organization

### Step 2: Add Screen Flow Details (After Approval)

**For each approved scenario, agent adds:**
- Screen-by-screen flow with visual state descriptions
- Interactions and transitions
- Object IDs for elements
- Persona context at each step

**Agent asks:** "Should I add the screen flow details for all scenarios, or start with one?"

---

## Site Type Detection

### Presentation Site (Static Pages)

**Characteristics:**
- Marketing/brochure sites
- Service catalogs
- Company profiles
- Portfolio sites

**Scenario Approach:**
- **Format:** Screen flow (page-to-page navigation)
- **Coverage:** Expose all pages if possible
- **Storyboarding:** Minimal (hover states, accordion opens)
- **Organization:** Group by navigation patterns, service types, content categories

### Dynamic App (Interactive States)

**Characteristics:**
- SaaS applications
- Booking systems
- Social platforms
- Productivity tools

**Scenario Approach:**
- **Format:** Storyboard primary (document states within views)
- **Coverage:** Single most important workflow
- **Screen Flow:** For onboarding, checkouts, multi-step processes
- **Organization:** Focus on core workflow, defer secondary features

---

## Scenario Design Principles

### 1. Scenario = User's Purpose

**Not:** Persona narrative or user story
**Yes:** Why user is visiting right now

**Bad:** "Stressed parent struggles with coordination..."
**Good:** "Verify service availability before booking"

### 2. Complete Page Coverage

**Goal:** Expose all pages for design scrutiny

**Why:** Code hides pages. Scenarios reveal them all.

**Approach:**
- List all pages first
- Organize into natural groupings
- Assign to scenarios without repetition
- Validate: Did we miss any pages?

### 3. No Page Repetition

**Rule:** Each page appears in exactly ONE scenario

**Exception:** Shared features (navigation, footer, chat widget) documented separately

### 4. Persona Mapping (Secondary)

**Primary:** Page coverage through natural purposes
**Secondary:** Connect to persona driving forces for context

**Don't force:** All personas into all scenarios
**Do map:** Scenarios to relevant persona needs

### 5. Page Documentation Strategy

**Agent judgment based on scale and variation:**

**Few pages + high variation → Separate pages**
- Each page substantially different in structure, content, or purpose
- Unique layouts, images, value propositions
- **Example:** 13 vehicle pages with different positioning and service emphasis
- **Why:** Honors uniqueness, supports distinct content management

**Many pages + low variation → Template with content variations**
- Structurally identical pages
- Only content differences (names, numbers, images)
- **Example:** 500 product pages with same template, different product data
- **Why:** Efficient documentation, avoids repetitive work

**Consider:**
- **Scale:** How many pages? (10 vs 100)
- **Variation degree:** How different? (unique structure vs content swaps)
- **Context:** CMS capabilities, SEO needs, maintenance approach

**Agent adapts strategy based on project specifics through Dialog mode.**

---

## Scenario Formats

### Screen Flow

**Use when:** Sequential pages, linear navigation

**Structure:**
```markdown
## [Scenario Title]

**User Purpose:** [Why they're here]
**Persona:** [Name] — [Driving Force]

### Screen Flow

**Screen 1: [Page Name]**
- **User Context:** [What they're thinking/feeling]
- **Visual State:** [What they see]
- **Interactions:** [What they can do]
- **Transition:** [What action leads to next screen]

**Screen 2: [Page Name]**
- **User Context:** [What they're thinking/feeling]
- **Visual State:** [What they see]
- **Interactions:** [What they can do]
- **Transition:** [What action leads to next screen]
```

### Storyboard

**Use when:** States within dynamic view, non-linear interactions

**Structure:**
```markdown
## [Scenario Title]

**View:** [Page/Component Name]
**User Purpose:** [What they're trying to accomplish]
**Persona:** [Name] — [Driving Force]

### States

**State 1: [State Name]**
- **Visual:** [What elements look like]
- **Triggers:** [What causes this state]
- **Interactions:** [What user can do]
- **Transitions:** [What moves to next state]

**State 2: [State Name]**
- **Visual:** [What elements look like]
- **Triggers:** [What causes this state]
- **Interactions:** [What user can do]
- **Transitions:** [What moves to next state]
```

---

## Dream Up Workflow Steps

### Analyze Phase

**Agent reads:**
1. **Product Brief** — Site type, business goals, technical constraints
2. **Trigger Map** — Personas with driving forces and psychological needs
3. **Project outline** — Phase status, folder structure

**Agent determines:**
- Site type (presentation vs dynamic app)
- Total page/view count
- Scenario format needed (screen flow vs storyboard)
- Natural groupings for page coverage

### Suggest Phase

**Agent presents:**
```markdown
## Scenario Suggestions

Based on your Trigger Map, here's what I'm imagining:

### Site Analysis
- **Type:** [Presentation site / Dynamic app / Mixed]
- **Total Pages:** [Count]
- **Format:** [Screen flow / Storyboard / Mixed]
- **Storyboarding Needed:** [Yes/No + Where]

### Suggested Scenarios ([N] total)

**Scenario 1: [Purpose]**
- **Pages:** [List]
- **Persona Connection:** [Name] ([Driving Force])
- **Rationale:** [Why this grouping makes sense]

**Scenario 2: [Purpose]**
- **Pages:** [List]
- **Persona Connection:** [Name] ([Driving Force])
- **Rationale:** [Why this grouping makes sense]

### Coverage Check
✅ All pages exposed: [Yes/No]
✅ No repetition: [Yes/No]
✅ Natural groupings: [Yes/No]

**Next:** Should I proceed with these scenarios, or would you like to adjust?
```

**User reviews and responds:**
- "Looks good, proceed"
- "Combine scenarios X and Y"
- "Add a scenario for [specific purpose]"
- "Actually, let's focus on just the most important workflow"

### Detail Phase (After Approval)

**For each approved scenario:**
1. Create folder: `C-UX-Scenarios/[NN]-[Scenario-Name]/`
2. Create file: `[NN]-[Scenario-Name].md`
3. Document using screen flow or storyboard format
4. Add Object IDs for key elements
5. Link from scenario overview file

---

## Agent Responsibilities

### On Trigger Map Completion

1. **Read prerequisite artifacts:**
   - Product Brief (site type, constraints)
   - Trigger Map (personas, driving forces)
   - Project outline (folder structure)

2. **Analyze for scenario suggestion:**
   - Detect site type (presentation vs dynamic)
   - List all pages/views
   - Assess product scale (small site vs large product)
   - Determine appropriate conversation mode (Dialog/Suggest/Dream)

3. **Select conversation mode:**
   - **Dialog:** Large products needing strategic scoping
   - **Suggest:** Medium complexity, propose structure first
   - **Dream:** Simple/obvious structure, execute autonomously

4. **Execute in chosen mode:**
   - **Dialog:** Start with strategic question about most valuable flow
   - **Suggest:** Present scenario suggestions with rationale, await approval
   - **Dream:** Create scenarios, present result for review

5. **After approval (Suggest/Dream) or discussion (Dialog):**
   - Document scenario details (screen flow or storyboard)
   - Create folder structure
   - Update progress tracking

### During Scenario Documentation

1. **Create scenario folder structure:**
   ```
   C-UX-Scenarios/
   ├── 00-scenario-overview.md  ← Links to all scenarios
   └── 01-[Scenario-Name]/
       └── 01-[Scenario-Name].md
   ```

2. **Document each scenario:**
   - User purpose header
   - Persona connection
   - Screen flow or storyboard (based on site type)
   - Object IDs for key elements

3. **Update progress tracking:**
   - Mark scenarios complete
   - Link from design-log.md
   - Update project outline status

---

## Implementation Checklist

When implementing Dream Up for a project:

- [ ] Trigger Map complete with aligned personas
- [ ] Site type identified (presentation vs dynamic)
- [ ] All pages/views listed
- [ ] Natural groupings determined
- [ ] Scenario suggestions presented with rationale
- [ ] User approved scenario structure
- [ ] Screen flow/storyboard format chosen per scenario
- [ ] Folder structure created in C-UX-Scenarios/
- [ ] Scenarios documented with Object IDs
- [ ] Coverage validated (no pages missed)
- [ ] Progress tracking updated

---

## Why Trigger Map Initiation Matters

**Before Trigger Map Initiation:**
- Designer stares at blank canvas after Trigger Map
- Arbitrary scenario choices
- Pages get missed, especially in large products
- No clear rationale or strategic focus
- Inconsistent coverage
- Paralysis with 100s of pages

**After Trigger Map Initiation:**
- Agent proactively initiates scenarios with rationale
- **Strategic scoping** for large products (Dialog mode)
- **Selective ignorance** applied appropriately (focus on critical flows)
- **Learning effect** leveraged (deep work on 20% informs 80%)
- Complete coverage for small sites, focused workflow for large products
- Mode adapts to complexity (Dialog/Suggest/Dream)
- User collaborates, approves, or reviews based on mode

**Small site (Suggest mode):** "Here are 3 scenarios covering all 15 pages. Does this make sense?"

**Large product (Dialog mode):** "What's the most important workflow we should focus on? Let's document that deeply first."

**Simple site (Dream mode):** "I've created 4 scenarios covering your entire site structure. Here's what I documented..."

---

**Pattern Status:** Design phase complete
**Next:** Apply to first project (test case)
**Future:** Integrate into Phase 3 workflow

---

_Pattern designed: 2026-02-12_
