# Module 02: Installation & Setup

## Lesson 4: WDS Project Initialization

**Add WDS, create structure, activate Mimir**

---

## What You'll Do

- Clone WDS repository
- Add WDS to workspace
- Create docs structure (8 phases)
- Activate Mimir

**Time:** 15-20 minutes

---

## Step 1: Clone WDS Repository

**WDS lives separately from your project.**

In terminal (make sure you're in Projects folder):

```bash
# Navigate to Projects
cd ~/Projects  # Mac/Linux
cd C:\Projects # Windows

# Clone WDS
git clone https://github.com/whiteport-collective/whiteport-design-studio.git
```

**✅ Checkpoint:** WDS cloned successfully

---

## Step 2: Add WDS to Workspace

1. **File** → **Add Folder to Workspace**
2. Navigate to Projects folder
3. Select `whiteport-design-studio` folder
4. Click **"Add"**

**✅ Checkpoint:** Both folders in sidebar:
- your-project
- whiteport-design-studio

---

## Step 3: Create Docs Structure

**What is docs?** Where all WDS specifications live. Your design source of truth.

Navigate to YOUR project:

```bash
cd ~/Projects/your-project-name  # Use YOUR project name!
cd C:\Projects\your-project-name # Windows
```

Create 8-phase structure:

```bash
# Mac/Linux
mkdir -p docs/1-project-brief
mkdir -p docs/2-trigger-mapping
mkdir -p docs/3-prd-platform
mkdir -p docs/4-ux-design
mkdir -p docs/5-design-system
mkdir -p docs/6-design-deliveries
mkdir -p docs/7-testing
mkdir -p docs/8-ongoing-development
```

**Windows alternative:**
```bash
mkdir docs
cd docs
mkdir 1-project-brief
mkdir 2-trigger-mapping
mkdir 3-prd-platform
mkdir 4-ux-design
mkdir 5-design-system
mkdir 6-design-deliveries
mkdir 7-testing
mkdir 8-ongoing-development
cd ..
```

**✅ Checkpoint:** `docs/` folder with 8 numbered subfolders

---

## Step 4: Activate Mimir

### What is Mimir?

Your WDS guide and orchestrator. He'll:
- Assess your skill level
- Check your setup
- Guide your next steps
- Connect you with specialist agents

### Find Mimir

In IDE sidebar:
1. Expand `whiteport-design-studio`
2. Expand `src` → `modules` → `wds`
3. Find `MIMIR-WDS-ORCHESTRATOR.md`

### Open AI Chat

- **Windows/Linux:** Press **Ctrl+L**
- **Mac:** Press **Cmd+L**
- Or click chat icon

### Activate

1. Drag `MIMIR-WDS-ORCHESTRATOR.md` into chat
2. OR type: `@MIMIR-WDS-ORCHESTRATOR.md`
3. Type: "Hello Mimir! I just completed setup and I'm ready to start."
4. Press **Enter**

**✅ Checkpoint:** Mimir responds and welcomes you!

---

## Step 5: Answer Mimir's Questions

Be honest about:
- Your skill level
- Your project
- How you're feeling

Mimir will:
- Verify your installation
- Guide your next steps
- Connect you with specialists

**Remember:** `@wds-mimir [your question]` anytime!

---

## Quick Reference: File Structure

```
Projects/
├── your-project/                      ← YOUR PROJECT
│   ├── docs/                          ← Specifications
│   │   ├── 1-project-brief/
│   │   ├── 2-trigger-mapping/
│   │   ├── 3-prd-platform/
│   │   ├── 4-ux-design/
│   │   ├── 5-design-system/
│   │   ├── 6-design-deliveries/
│   │   ├── 7-testing/
│   │   └── 8-ongoing-development/
│   └── README.md
│
└── whiteport-design-studio/           ← WDS METHODOLOGY
    └── src/modules/wds/
        ├── agents/
        ├── workflows/
        ├── course/
        └── MIMIR-WDS-ORCHESTRATOR.md
```

---

## Troubleshooting

**Issue:** Can't find MIMIR file → Check WDS added to workspace
**Issue:** Drag doesn't work → Use `@MIMIR-WDS-ORCHESTRATOR.md`
**Issue:** mkdir fails → Make sure you're in your project folder

---

## Congratulations!

You've completed Module 02: Installation & Setup!

**What you accomplished:**
- ✅ GitHub account & repository
- ✅ IDE installed
- ✅ Project cloned
- ✅ WDS integrated
- ✅ Docs structure created
- ✅ Mimir activated

**You're ready to design with WDS!**

---

## What's Next?

- **[Module 03: Alignment & Signoff](../module-03-alignment-signoff/module-03-overview.md)**
- **[WDS Training Course](../00-course-overview/00-course-overview.md)**
- **Ask Mimir:** "What should I do next?"

---

*Part of Module 02: Installation & Setup*
*[← Back to Module Overview](module-02-overview.md)*
