# Scenario Conversation Pattern

**Status:** Design Phase
**Created:** 2026-02-12
**Purpose:** Conversational workflow for creating UX scenario documents

---

## Philosophy

**Don't ask the user to produce scenario documents.**

Have exploratory conversations where you learn:
- What happens at each step
- What the user sees and thinks
- What interactions are available
- What triggers state changes

**Then YOU synthesize** the screen flow or storyboard document.

---

## When This Pattern Applies

**After Dream Up suggestions are approved:**
- User has approved scenario structure
- Agent creates each scenario document through conversation
- One scenario at a time, or all at once (user choice)

**Two conversation types:**
1. **Screen Flow Conversation** — Sequential pages
2. **Storyboard Conversation** — States within a view

---

## Screen Flow Conversation Pattern

### Prerequisites

Agent knows:
- Scenario title and purpose
- Pages included in this scenario
- Persona connection
- Whether user has wireframes/sketches

### Step 1: Open Conversation

**Agent opening:**
```
Let's walk through [Scenario Title] together.

This is about [user purpose] — [persona name] wants to [goal].

We'll go page by page. For each page, just describe what [persona] sees
and what they can do. Don't worry about perfect wording — just dump your
ideas, I'll structure them.

[If sketches exist]: "Want to share your sketches first, or just talk through it?"

Ready to start with the first page?
```

**Context-aware variation (if user has detailed notes):**
```
I see you have [wireframes/notes] for this scenario. Let me review those first...

[After reading]

I see you're envisioning [key elements]. Let's walk through this together
and I'll ask questions to fill in gaps. We'll start with [first page].
```

### Step 2: Explore Each Screen

**For each page in sequence:**

#### Opening Question (Natural Entry)
```
**Page: [Name]**

[Persona] just [action from previous page]. What do they see now?
```

#### Listen for Signals, Ask Follow-Ups

**If user mentions visual element:**
→ "What does that look like? Any specific wording?"

**If user mentions action/button:**
→ "What happens when they click that?"

**If user mentions decision point:**
→ "What if they choose [alternative]? Does that change the flow?"

**If user mentions persona thinking:**
→ "What are they worried about at this point?"

**If user mentions missing information:**
→ "Does [persona] need to see [X] before they can proceed?"

**If user describes vague state:**
→ "Let me check I'm picturing this right: [synthesis]. Is that what you mean?"

#### Capture Pattern

For each screen, agent mentally tracks:
- **Visual State:** What's on screen (heading, content, form fields, buttons, images)
- **User Context:** What persona is thinking/feeling
- **Interactions:** What actions are available
- **Transition:** What happens next (which action, which page)

### Step 3: Reflection Checkpoint

**After exploring all pages, agent synthesizes:**

```
Let me play back what I heard for [Scenario Title]:

**Screen 1: [Name]**
- [Persona] sees: [synthesis of visual state]
- They're thinking: [user context]
- They can: [interactions]
- Next: [transition to Screen 2]

**Screen 2: [Name]**
- [Persona] sees: [synthesis]
- They're thinking: [context]
- They can: [interactions]
- Next: [transition to Screen 3]

[Continue for all screens...]

Does this match what you were envisioning? Anything I got wrong or missed?
```

**User responds:**
- "Yes, that's it" → Proceed to documentation
- "Actually, Screen 2 should..." → Note corrections, resynthesize
- "We need to add..." → Explore additional screens

### Step 4: Document

**Agent creates:**
```markdown
## [Scenario Title]

**User Purpose:** [Why they're here]
**Persona:** [Name] — [Driving Force]

### Screen Flow

**Screen 1: [Page Name]**
**Object ID:** `[page-name]`

**User Context:** [Persona]'s thoughts/feelings at this point

**Visual State:**
- [Element 1] — [Description]
- [Element 2] — [Description]
- [CTA Button] — [Wording]

**Interactions:**
- [Action] → [Result]
- [Action] → [Result]

**Transition:** User clicks [button] → [Screen 2]

---

**Screen 2: [Page Name]**
[Same structure...]
```

**Agent says:**
```
✓ Created [scenario-name].md in C-UX-Scenarios/01-[Scenario-Name]/

Want to review the document, or move to the next scenario?
```

---

## Storyboard Conversation Pattern

### Prerequisites

Agent knows:
- Page/view being documented
- What triggers state changes
- User goal for this interaction
- Persona connection

### Step 1: Open Conversation

**Agent opening:**
```
Let's document [Page/View Name] together.

This is where [persona] [accomplishes goal]. I know this page has multiple
states depending on [triggering factors].

Let's start with the initial state — what does [persona] see when they
first arrive?
```

### Step 2: Explore Each State

**For each state:**

#### Opening Question
```
**State: [Name, e.g., "Empty", "Loading", "Active"]**

What does this state look like? What's visible on screen?
```

#### Listen for Signals, Ask Follow-Ups

**If user mentions visual change:**
→ "What causes that change? User action, timer, data load?"

**If user mentions interactive element:**
→ "What happens when [persona] clicks that?"

**If user mentions conditional display:**
→ "When does that appear vs stay hidden?"

**If user mentions state progression:**
→ "Can they go back to the previous state, or is this one-way?"

**If user mentions multiple triggers:**
→ "Which trigger has priority if both happen?"

**If unclear transition:**
→ "So if [condition], it goes to [State X], but if [condition], it goes to [State Y]?"

#### Capture Pattern

For each state, agent mentally tracks:
- **Visual:** What elements look like in this state (colors, text, icons, layout)
- **Triggers:** What causes entry to this state (user action, time, data)
- **Interactions:** What user can do in this state
- **Transitions:** What moves to next state (and which state)

### Step 3: Reflection Checkpoint

**After exploring all states, agent synthesizes:**

```
Let me play back the state flow for [Page Name]:

**State 1: [Name]**
- **Visual:** [synthesis of appearance]
- **Triggered by:** [what causes this state]
- **User can:** [available interactions]
- **Transitions to:** [State 2] when [condition]

**State 2: [Name]**
- **Visual:** [synthesis]
- **Triggered by:** [cause]
- **User can:** [interactions]
- **Transitions to:** [State 3] when [condition], OR [State 4] when [alternative]

[Continue for all states...]

Does this capture the interaction flow you're envisioning?
```

**User responds:**
- "Yes, exactly" → Proceed to documentation
- "State 2 should actually..." → Note corrections
- "There's another state when..." → Explore additional states

### Step 4: Document

**Agent creates:**
```markdown
## [Scenario Title]

**View:** [Page/Component Name]
**Object ID:** `[view-id]`

**User Purpose:** [What persona is trying to accomplish]
**Persona:** [Name] — [Driving Force]

### States

**State 1: [State Name]**
**Object ID:** `[view-id]-state-[name]`

**Visual:**
- [Element 1]: [Appearance in this state]
- [Element 2]: [Appearance in this state]
- [Visual indicator]: [Color/icon/text]

**Triggers:**
- Entry: [What causes this state]
- Duration: [How long this lasts, if applicable]

**Interactions:**
- [Action] → [Result]
- [Action] → [Result]

**Transitions:**
- → [State 2] when [condition]
- → [State 3] when [alternative condition]

---

**State 2: [State Name]**
[Same structure...]
```

**Agent says:**
```
✓ Created [scenario-name].md with [N] states documented

Want to review, or continue to the next scenario?
```

---

## Conversation Management

### If User Has Sketches/Wireframes

**Before conversation:**
```
Do you have sketches or wireframes I should look at first? That'll help
me understand the visual direction.
```

**After reviewing:**
```
I see the visual structure. Let's walk through the interaction flow —
I'll ask about things that aren't clear from the sketches.
```

### If User Is Uncertain

**When user says "I'm not sure yet":**
```
That's fine — let's think through it together.

What's the MAIN thing [persona] needs to accomplish here? Let's start
with that and work backwards.
```

**Offer options:**
```
I've seen this handled a few ways:
- Option A: [description]
- Option B: [description]

Which feels closer to what you're imagining?
```

### If Conversation Goes Off-Track

**Gently redirect:**
```
Good point about [tangent]. Let's capture that as a note and come back
to it. For now, let's finish [current screen/state] — what happens when
[persona] clicks [button]?
```

### If User Provides Too Much Detail

**Acknowledge and synthesize:**
```
Got it — lots of detail there. Let me capture the essentials for this
scenario. We can always add more detail later if needed.

The core interaction is: [synthesis]. Right?
```

---

## Multi-Scenario Sessions

### Agent Asks (After First Scenario Complete)

```
[Scenario 1] is done. We have [N-1] more scenarios to document.

Want to continue with [Scenario 2] now, or take a break and resume later?
```

**If continuing:**
```
Let's move to [Scenario 2]: [Purpose]

This covers [pages/states]. Ready to walk through it?
```

**If pausing:**
```
✓ Scenario 1 complete and documented
⏸ Scenarios 2-[N] pending

I'll save our progress. When you're ready to continue, just say
"Let's continue the scenarios" and I'll pick up where we left off.
```

---

## Context-Aware Adaptations

### Brownfield (Existing Site/App)

**Opening variation:**
```
I see you have an existing [page/feature]. Should we start with how it
works NOW, then discuss changes? Or redesign from scratch?
```

**During conversation:**
```
Currently this shows [X]. Are we keeping that, or changing to [Y]?
```

### Rebuild vs New Feature

**Rebuild existing:**
- Reference current implementation
- Focus on "what changes" vs "what stays"
- Ask about pain points with current version

**New feature:**
- Start from user need
- No existing reference points
- More exploratory questions

---

## Agent Responsibilities

### Before Scenario Conversations Start

1. Read approved Dream Up suggestions
2. List all scenarios to be created
3. Ask: "Want to do all scenarios now, or one at a time over multiple sessions?"
4. Create folder structure: `C-UX-Scenarios/`

### During Each Scenario Conversation

1. Open with context (purpose, persona, pages/states)
2. Explore screen-by-screen or state-by-state
3. Use signal-based follow-ups
4. Track visual, context, interactions, transitions
5. Synthesize at reflection checkpoint
6. Adjust based on corrections
7. Document in appropriate format
8. Confirm completion before moving to next

### After All Scenarios Complete

1. Create `00-scenario-overview.md` linking all scenarios
2. Update `design-log.md` with scenario completion
3. Update project outline: Phase 4 complete
4. Handoff note: "Ready for Phase 5 (Design System) or Phase 6 (Build)"

---

## Why This Pattern Matters

**Without conversational pattern:**
- User struggles to write scenario documents
- Details get missed
- Inconsistent structure
- Agent can't validate understanding

**With conversational pattern:**
- Natural exploration through dialogue
- Agent synthesizes (user doesn't produce artifact)
- Reflection checkpoints catch misunderstandings
- Consistent, complete scenario documentation

**User thinks out loud. Agent captures and structures.**

---

**Pattern Status:** Design phase complete
**Next:** Apply to first project scenario creation
**Integrates with:** Dream Up Pattern (suggestion phase)

---

_Pattern designed: 2026-02-12_
