# 🤖 How to Use Claude Projects

> Claude Projects are persistent AI workspaces. You configure them once with a
> teaching prompt — and Claude remembers it across every session.
> This is the foundation of the entire preparation system in this repo.

---

## 🆚 Project vs Regular Chat

| Feature | 💬 Regular Chat | 📁 Claude Project |
|---------|:--------------:|:----------------:|
| Custom teaching instructions | ❌ | ✅ Saved permanently |
| Upload revision PDFs | Per chat only | ✅ Available always |
| Remembers past sessions | ❌ Resets | ✅ Persists |
| Best for | Quick questions | Structured study |

---

## 🛠️ Create a Claude Project (Step-by-Step)

### Step 1 — Open Claude.ai
Go to [https://claude.ai](https://claude.ai). Sign in or create a free account.

> 💡 **Recommendation:** Claude Pro (paid) gives higher message limits —
> important for long study sessions. Free tier works but may hit limits mid-session.
> Use **Claude Sonnet 4.5 or higher** for best results.

### Step 2 — Create a New Project
1. In the left sidebar, click **"Projects"**
2. Click **"+ New Project"**
3. Name it clearly — e.g., `C-CAT: C Language` or `C-CAT: MCQ Practice`
4. Click **"Create Project"**

### Step 3 — Add Custom Instructions
1. Inside the project, click **"Project Instructions"** (gear/settings icon)
2. You will see a large text box
3. Open the relevant `[Subject]-Project-Instructions.md` from this repo
4. Copy the full prompt block (marked `--- BEGIN PROMPT ---` to `--- END PROMPT ---`)
5. Paste it into the Custom Instructions box
6. Click **Save**

> ⚠️ This step is the most important. The custom instructions define how Claude
> behaves — as a teacher, not just a chatbot. Do not skip it.

### Step 4 — Upload the Revision PDF
1. Inside the project, click **"Add content"** or the upload/paperclip icon
2. Upload the revision PDF from the `C - CAT/Section B/` folder
3. Once uploaded, Claude references it in every conversation automatically

### Step 5 — Start a Session
Open a **New Chat** inside the project and use the trigger format shown in
the subject's `Project-Instructions.md` file.

---

## 📋 Recommended Project Setup

| 📁 Project Name | 📄 Instructions File | 📎 PDF to Upload |
|----------------|---------------------|-----------------|
| `C-CAT: English` | `Section A/1 - English/English-Project-Instructions.md` | None |
| `C-CAT: Quantitative Aptitude` | `Section A/2 - Quantitative Aptitude/Quantitative-Aptitude-Project-Instructions.md` | `Quant LRDI ECE Sample.pdf` |
| `C-CAT: Reasoning` | `Section A/3 - Reasoning/Reasoning-Project-Instructions.md` | `Blood_Relations_Marathi_Glossary.pdf` |
| `C-CAT: C Language` | `Section B/C Language/C-Language-Project-Instructions.md` | `CCAT_C_Revision (3).pdf` |
| `C-CAT: DSA` | `Section B/DSA/DSA-Project-Instructions.md` | `DSA_Revision_Bible_CCAT.pdf` |
| `C-CAT: OS` | `Section B/OS/OS-Project-Instructions.md` | `OS_Revision_Notes_CCAT_v2.pdf` |
| `C-CAT: Networking` | `Section B/Networking/Networking-Project-Instructions.md` | `Networking_Revision_CCA T_SectionB.pdf` |
| `C-CAT: Big Data` | `Section B/Big Data/BigData-Project-Instructions.md` | `BigData_Revision_Sheet_v2.pdf` |
| `C-CAT: AI` | `Section B/AI/AI-Project-Instructions.md` | `AI_Revision_CCAT.pdf` |
| `C-CAT: MCQ Practice` | `MCQ-Project-Setup.md` | None |

---

## 💬 How to Talk to Claude in a Learning Project

**Be specific. Claude responds to specifics, not generalities.**

| ❌ Too vague | ✅ Effective trigger |
|-------------|---------------------|
| `Teach me C` | `Teach me: Pointers — pointer arithmetic with arrays` |
| `I don't understand this` | `I understand malloc but not free — explain only that` |
| `Give me examples` | `Give me 3 correct examples and 2 that break the rule` |
| `Explain OS` | `Teach me: Round Robin scheduling — trace with 3 processes` |

---

## 🔧 Troubleshooting

**Claude is not following the teaching style.**
→ Open Project Settings and verify custom instructions are saved. Re-paste if empty.

**Claude says it cannot see my PDF.**
→ Re-upload inside the project under "Project Knowledge" — not in a regular chat.

**I hit the message limit.**
→ Free tier has daily limits. Wait for reset or upgrade to Pro.
→ Do not switch to regular chat — you will lose the project context.

**Claude gives a wrong answer.**
→ Cross-question it: *"Are you sure? Explain your reasoning."*
→ The project prompts are designed so Claude admits uncertainty — use that.
