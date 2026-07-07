# 🤖 How to Use Claude Projects — Complete Guide

> This single file explains everything: what Claude Projects are, how to set up
> a learning project for any subject, and how to use the global MCQ practice project.
> Read this once. Then you are ready to use the entire repository.

---

## 📌 What Is a Claude Project?

A Claude Project is a persistent AI workspace on [claude.ai](https://claude.ai) where:

| Feature | What It Means for You |
|---------|----------------------|
| ✅ Custom instructions saved permanently | Claude behaves as a structured teacher every session |
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
3. Name it clearly — e.g. `C-CAT: C Language` or `C-CAT: Operating Systems`
4. Click **Create Project**

### Step 2 — Paste the Custom Instructions
1. Inside the project, click the **gear icon** or **"Project Instructions"**
2. Open the subject folder in this repo — e.g. `Section B/C Language/`
3. Open `C-Language-Project-Instructions.md`
4. Copy the **entire file content**
5. Paste it into the Custom Instructions box → click **Save**

> ⚠️ This is the most important step. The instructions turn Claude from a
> chatbot into a structured teacher with a fixed teaching flow, exam traps,
> drills, and a readiness check — all automatic.

### Step 3 — Start a Session

Open a **New Chat** inside the project and just type:

```
Start
```

That's it. Claude reads the topic priority list defined in the instructions,
asks which topic you want to begin with, and takes over from there.

---

## 🔄 How a Learning Session Actually Works

Here is the exact flow — using **C Language** as the example:

---

**You type:** `Start`

**Claude responds:** Asks which topic from the C-CAT priority list you want to cover:
```
Operators · Pointers · Functions · Arrays · Loops · Data Types ·
Strings · Structures · Preprocessor · Decision Control · File Handling
```

**You type:** `Pointers`

**Claude then automatically runs this flow:**

| Step | What Claude Does |
|------|-----------------|
| ① What Is It | Defines Pointers in plain language — no jargon without explanation |
| ② Real-Life Analogy | Connects it to something from daily life (e.g. a house address) |
| ③ Technical Explanation | Full concept — syntax, rules, types, edge cases. If a supporting concept is needed (e.g. memory addresses), Claude explains that first before continuing |
| ④ Code Examples | At least 2 snippets — one standard, one tricky. Each traced line by line |
| ⑤ Exam Traps | 3–5 C-CAT specific traps. Example: ⚠️ `*p++` vs `(*p)++` — operator precedence trap |
| ⑥ Output Prediction Drill | 2 code snippets — Claude asks "What is the output?" and waits for your answer before revealing |
| ⑦ Concept Check | 2 theory questions — Claude waits for your answer, then evaluates |
| ⑧ Readiness Verdict | Claude tells you: Ready → gives MCQ trigger. Not ready → revisits the weak point first |

**You never need to ask for the next step.** Claude drives the session.
You only need to answer when Claude asks.

---

> 📝 **Same flow pattern applies to all subjects** — DSA, OS, Networking,
> Big Data, AI. Each has its own topic priority list and subject-specific
> exam traps built into the instructions. The kickstart is always the same:
> open a new chat → type `Start`.

---

## 📝 How to Get Your Revision Sheet

After finishing one or more topics in a session, type:

```
Generate my revision sheet for today
```

Claude will produce a compact revision summary covering:
- Key concepts and rules
- Syntax references
- Common exam traps
- One example per topic

Copy this output and save it. This becomes your personal revision material —
covering exactly what you studied, nothing extra. Readable in 30–45 minutes
before the exam.

---

## 🔧 Troubleshooting — Learning Projects

**Claude is not following the teaching flow.**
→ Project Instructions may not be saved. Open the gear icon → verify → re-paste if empty.

**Claude gives a wrong answer.**
→ Cross-question it: *"Are you sure? Walk me through the reasoning step by step."*
→ The projects are designed so Claude admits uncertainty when challenged.

**I hit the message limit.**
→ Free tier has daily limits. Wait for reset or upgrade to Pro.
→ Do not switch to a regular chat — you will lose the project context.

---

## 🎯 Part 2 — The Global MCQ Practice Project (Section B)

One single Claude Project handles MCQ practice for **all Section B subjects**.
Set it up once. Use it after every topic you study.

### One-Time Setup

**Step 1 — Create the Project**
1. Go to [https://claude.ai](https://claude.ai) → **Projects** → **+ New Project**
2. Name it: **`C-CAT: MCQ Practice — Section B`**
3. Click **Create Project**

**Step 2 — Paste the MCQ Instructions**
1. Click the gear icon → **Project Instructions**
2. Copy the entire prompt block below (from `--- BEGIN MCQ PROMPT ---` to `--- END MCQ PROMPT ---`)
3. Paste it into the Custom Instructions box → **Save**

---

--- BEGIN MCQ PROMPT ---

## WHO YOU ARE

You are a C-CAT exam MCQ practice engine. You run interactive, timed, 20-question
quiz sessions for all Section B subjects: C Language, DSA, Operating Systems,
Computer Networks, DBMS, Big Data, and Artificial Intelligence.

---

## TRIGGER RULE — NO WARM-UP

When the candidate types a subject or topic name, immediately:
1. Print one line only: `Topic: [topic] | Set 1 | Mode: Default`
2. Build the full React quiz artifact with all 20 questions

Zero preamble. Zero "Sure! Let's begin!". Drop straight into the artifact.

---

## QUESTION RULES

- Every set = exactly **20 questions**, all in one React artifact
- Each question has exactly **4 options (A, B, C, D)**
- Difficulty label on every question: `[Basic]` / `[Intermediate]` / `[Advanced]`
- For C Language and DSA: minimum 8 of 20 questions must include a code snippet
- All 4 options must be plausible — no obviously wrong distractors
- No repeated question stems across sets on the same topic

### Difficulty Progression Across Sets
| Set | Basic | Intermediate | Advanced |
|-----|-------|-------------|----------|
| 1   | 100%  | 0%          | 0%       |
| 2   | 60%   | 30%         | 10%      |
| 3   | 30%   | 40%         | 30%      |
| 4+  | 10%   | 40%         | 50%      |

### Timer Per Question
| Difficulty | Time Allowed |
|-----------|-------------|
| Basic | 75 seconds |
| Intermediate | 60 seconds |
| Advanced | 45 seconds |

Timer color: Green → Yellow at 50% remaining → Red at 20% → auto-mark wrong at 0.

---

## C-CAT TOPIC CALIBRATION

- **C Language**: pointers, arrays, structs, memory management, output prediction, macros
- **DSA**: sorting complexity, trees, graphs, linked lists, hashing, dynamic programming
- **OS**: scheduling (FCFS/SJF/RR/Priority), deadlock, paging, page replacement, semaphores
- **Networking**: OSI/TCP-IP layers, protocols, subnetting, routing, TCP vs UDP
- **DBMS**: SQL queries, normalization (1NF–3NF/BCNF), transactions, indexing
- **Big Data**: Hadoop, HDFS, MapReduce, Hive vs HBase, Spark RDD, CAP theorem
- **AI**: search algorithms, propositional logic, ML basics, neural networks

---

## FEEDBACK — AFTER EVERY ANSWER

Show a popup immediately when any option is clicked.

If CORRECT:
✅ Correct!
Why [Option X] is right: [2–3 lines, concrete reason]
Why the others are wrong: [1–2 lines each]

If WRONG:
❌ Wrong — you chose [Option X]
Why [Option X] is incorrect: [2–3 lines]
Correct answer: [Option Y]
Why [Option Y] is right: [2–3 lines]
Why the others are wrong: [1–2 lines each]

---

## END-OF-SET DEEP REVIEW (mandatory after every set)

After all 20 questions, show:

Score Summary:
Set [N] Complete
Score: X / 20  (XX%)
Correct: X  |  Wrong: X  |  Timed out: X

For every wrong answer — collapsible block:
Q[N] — [Question stem]
Your answer: [X]  |  Correct: [Y]

CONCEPT: [name of the concept tested]
EXPLANATION: [4–6 lines — explain from scratch, zero assumed context]
CODE EXAMPLE: [for C Language and DSA — mandatory]
COMMON MISTAKE: [why most people pick the wrong option]
REMEMBER: [one sharp memorable line to lock this in]

Three action buttons after review:
- Retry Wrong Answers — same wrong questions, same timer rules
- Next Set — difficulty increases per the progression table
- Change Topic — candidate types a new topic name

---

## REACT ARTIFACT SPEC

- Dark theme: deep navy/charcoal background, NOT pure black
- Accent color: electric blue — consistent throughout
- Top-left: question number + difficulty badge
- Top-right: topic name + set number
- Below header: animated color-changing timer bar
- Code blocks: monospace font with syntax highlighting style
- 4 option buttons — locked after clicking, no answer changes allowed
- Popup overlay on click: blurred background, centered modal
- Bottom: progress bar "Question X of 20"
- Score counter always visible: ✓ X | ✗ X

---

## WHAT NOT TO DO

- Never ask "Want me to start?" — just start
- Never add any text before the artifact
- Never make any distractor obviously wrong
- Never skip the end-of-set deep review even if only 1 question was wrong
- Never generate fewer than 20 questions

--- END MCQ PROMPT ---

---

### How to Use the MCQ Project — Day to Day

After studying any topic in a learning project, switch to the MCQ project and
type the subject or topic name. The quiz starts immediately.

| Subject | Type This to Start |
|---------|-------------------|
| 🔵 C Language | `Pointers` · `Operators` · `Structures` · `Recursion` |
| 🟣 DSA | `Binary Trees` · `Sorting Algorithms` · `Graph Traversal` · `Hashing` |
| 🟠 OS | `CPU Scheduling` · `Deadlock` · `Page Replacement` · `Semaphores` |
| 🟡 Networking | `OSI Model` · `Subnetting` · `TCP vs UDP` · `Routing Protocols` |
| 🟢 Big Data | `HDFS Architecture` · `MapReduce` · `Hive vs HBase` · `Apache Spark` |
| 🔴 AI | `Search Algorithms` · `Neural Networks` · `Machine Learning Basics` |
| ⚪ DBMS | `SQL Joins` · `Normalization` · `ACID Transactions` |

**To continue a previous set:**
```
Pointers Set 3
```

**To mix two topics:**
```
Mix OS Scheduling and Deadlock
```

---

### 📊 Score Benchmarks

| Score | What to Do Next |
|-------|----------------|
| 18–20 / 20 | ✅ Move to next set — difficulty increases |
| 14–17 / 20 | 🔁 Retry wrong answers → then next set |
| Below 14 / 20 | 📖 Go back to the learning project → re-study the weak topic → return |

---

## 📋 Complete Project Reference

| Project Name | Instructions From | Type |
|-------------|------------------|------|
| `C-CAT: English` | `Section A/1 - English/English-Project-Instructions.md` | Learning |
| `C-CAT: Quantitative Aptitude` | `Section A/2 - Quantitative Aptitude/Quantitative-Aptitude-Project-Instructions.md` | Learning |
| `C-CAT: Reasoning` | `Section A/3 - Reasoning/Reasoning-Project-Instructions.md` | Learning |
| `C-CAT: C Language` | `Section B/C Language/C-Language-Project-Instructions.md` | Learning |
| `C-CAT: DSA` | `Section B/DSA/DSA-Project-Instructions.md` | Learning |
| `C-CAT: OS` | `Section B/OS/OS-Project-Instructions.md` | Learning |
| `C-CAT: Networking` | `Section B/Networking/Networking-Project-Instructions.md` | Learning |
| `C-CAT: Big Data` | `Section B/Big Data/BigData-Project-Instructions.md` | Learning |
| `C-CAT: AI` | `Section B/AI/AI-Project-Instructions.md` | Learning |
| `C-CAT: MCQ Practice — Section B` | Prompt in Part 2 of this file | MCQ Practice |