Open the file `HOW-TO-USE-CLAUDE-PROJECTS.md` in the root of the 
`C-CAT Preparation Guide` folder.


---

# 🤖 How to Use Claude Projects — Complete Guide

> This single file explains everything: what Claude Projects are, how to set up
> a learning project for any subject, and how to use the global MCQ practice project.
> Read this once. Then you are ready to use the entire repository.

---

## 📌 What Is a Claude Project?

A Claude Project is a persistent AI workspace on [claude.ai](https://claude.ai) where:

| Feature | What It Means for You |
|---------|----------------------|
| ✅ Custom instructions saved permanently | Claude behaves as a teacher every session — no re-explaining needed |
| ✅ Conversation history persists | Pick up exactly where you left off |
| ✅ No repeated setup | Configure once, study forever |

> 💡 Free account works. **Claude Pro recommended** for uninterrupted long sessions.
> Use **Claude Sonnet 4.5 or higher**.

---

## 🛠️ Part 1 — Setting Up a Learning Project (Per Subject)

Do this once for each subject you want to study.

### Step 1 — Create the Project
1. Go to [https://claude.ai](https://claude.ai) → click **Projects** in the left sidebar
2. Click **+ New Project**
3. Name it clearly: e.g. `C-CAT: C Language` or `C-CAT: Operating Systems`
4. Click **Create Project**

### Step 2 — Paste the Custom Instructions
1. Inside the project, click the **gear icon** or **"Project Instructions"**
2. Open the subject folder in this repo (e.g. `Section B/C Language/`)
3. Open `C-Language-Project-Instructions.md`
4. Copy everything between `--- BEGIN PROMPT ---` and `--- END PROMPT ---`
5. Paste it into the Custom Instructions box → click **Save**

> ⚠️ This is the most important step. The prompt turns Claude from a chatbot
> into a structured teacher that cross-questions you and identifies your gaps.

### Step 3 — Start a Session
Open a **New Chat** inside the project and use the trigger format from that subject's
instructions file. Examples:

| Subject | Example Trigger |
|---------|----------------|
| C Language | `Teach me: Pointers — pointer arithmetic with arrays` |
| DSA | `Teach me: Binary Search Tree — insertion and deletion` |
| OS | `Teach me: Round Robin scheduling — trace with 3 processes` |
| Networking | `Teach me: OSI Model — layer by layer with protocols` |
| Big Data | `Teach me: MapReduce — explain with a word count example` |
| AI | `Teach me: A* Search — with a traced example` |

**Be specific. Claude responds to specifics, not generalities.**

| ❌ Too vague | ✅ Effective |
|-------------|------------|
| `Teach me C` | `Teach me: Pointers — pointer arithmetic with arrays` |
| `I don't understand` | `I understand malloc but not free — explain only that part` |
| `Give me examples` | `Give me 3 correct examples and 2 that intentionally break the rule` |

### Step 4 — Generate Your Revision PDF
After completing all chapters in a subject, ask Claude at the end of your session: