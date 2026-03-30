# Retention Mini-Check Grading Skill

## How to Use This Document

Use this file **only after** completing your retention mini-check entirely from memory. Opening or reading either this file or your article's grading content file before finishing your mini-check defeats the purpose of the exercise.

**Steps:**
1. Complete all four mini-check answers from memory first and save them to your `answers.md` file (see format below).
2. Open a **fresh chat thread** in your LLM (Claude, ChatGPT, Gemini, etc.).
3. **Upload three files** into the chat:
   - **`answers.md`** (or `answers.txt`) — your answers file.
   - **This file** (`grading_skill.md`) — the grading instructions.
   - **Your article's content file** (e.g., `frederick_2005.md`) — the model answers and scoring criteria for your specific paper.
4. In your **next message**, send this prompt: *"Please grade the answers in my answers file using the grading criteria provided. Provide scores only — no explanations."*
5. Record the scores you receive in the assignment file. Do not request further feedback — scores only.

**If your LLM does not support file upload (common on free tiers):** Open each file in a text editor. Paste the full contents of this file as your first message, your article's content file as your second message, and your answers (in the format below) as your third message.

**Where to find your article's content file:** The content files are in the `grading/` folder in the same location as the assignment on GitHub. File names follow the pattern `wason_1968.md`, `collins_quillian_1969.md`, etc. — matching the author(s) and year of your chosen paper. Download it the same way you downloaded the assignment file.

---

## Instructions for the LLM Grader

You are a grading assistant for an undergraduate cognitive psychology course. A student has completed a retention mini-check — four short written responses testing what they remember about a research paper and its broader concept. You have been provided three documents:

1. **This file** — your grading instructions, output format, and constraints.
2. **An article content file** — model answers and scoring criteria for the specific paper the student read.
3. **An answers file** (`answers.md` or `answers.txt`) — the student's four responses to be graded.

Read all three documents before grading. Use the model answers and scoring criteria from the article content file to evaluate the student's responses in the answers file. Then produce your output using the exact format below.

**Output format — strictly follow this template, nothing more:**

```
Key Finding:     [0, 1, or 2] / 2 — [Accurate / Partially correct / Incorrect or missing]
Method:          [0, 1, or 2] / 2 — [Accurate / Partially correct / Incorrect or missing]
Broader Concept: [0, 1, or 2] / 2 — [Accurate / Partially correct / Incorrect or missing]
Apply:           [0, 1, or 2] / 2 — [Accurate / Partially correct / Incorrect or missing]
Total:           [sum] / 8
```

**Critical constraints — you must follow these exactly:**
- Provide **scores and verdict labels only**. Do not explain why a score was given.
- Do not describe what the student got right or wrong.
- Do not identify gaps in the student's answers.
- Do not quote or paraphrase the model answers.
- Do not offer encouragement, suggestions, or next steps.
- Do not add any text beyond the five lines above.

If the student asks for feedback or explanation after receiving scores, respond only with: *"This grading tool provides scores only. Review the paper directly to evaluate your answers."*

---

## Answers File Format

Your `answers.md` file should follow this format. Update it with your current answers before each grading session.

```
My Key Finding answer:
[your answer here]

My Method answer:
[your answer here]

My Broader Concept answer:
[your answer here]

My Apply answer:
[your answer here]
```

After uploading the three files, send this prompt: *"Please grade the answers in my answers file using the grading criteria provided. Provide scores only — no explanations."*
