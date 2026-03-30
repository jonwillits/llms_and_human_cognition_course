# LLMs and the Feeling of Knowing

## Background Info

### Purpose of This Assignment

This assignment asks you to investigate the difference between using an LLM as a tool that supports genuine learning and using it in a way that produces correct-looking responses without building real understanding. You will choose a short, classic research paper in cognitive psychology (from our list), and study it on your own. You will then test yourself using five different ways of engaging with the material: 1) reading the paper without LLM help, 2) asking an LLM for a direct summary, 3) requesting a structured explanation, 4) asking for real-world examples, and 5) engaging in an interactive tutoring session. After each condition, you will test your retention and comprehension without looking at any sources by answering the same set of questions.

The core question is whether LLM assistance actually helps you learn, or whether it creates the feeling of understanding without the substance. To find out, you will complete short retention tests throughout the assignment that require you to explain the study's method, its key finding, and the broader concept it illustrates — all from memory. You will also track your confidence before and after each condition. By the end, you will have direct evidence of which forms of assistance produced durable understanding versus superficial performance, and you will reflect on where that distinction maps onto the intuitive difference between "learning support" and “false feeling of knowing."

### Quick Specs
- Target time: ~6 hours
- Model requirements: At least one LLM chat interface (any model, free or paid is fine)
- Grading basis: Effort, process quality, reproducibility, condition comparison, and reflection
- Submission format: Edit and submit this `.md` file

### How to Download This File
1. On the GitHub page for this file, click the **Raw** button (top-right of the file view).
2. Right-click anywhere on the page and choose **Save As**.
3. Make sure the filename ends in `.md` and save it somewhere you can find it.
4. Open it in any text editor (VS Code, PyCharm, Sublime Text, Notepad, TextEdit, etc.) to fill it in.
5. Submit the completed `.md` file to Canvas.

### Key Terms (Read Before Starting)
- **Learning**: A durable change in knowledge or skill that transfers to new contexts and persists after the learning opportunity ends.
- **Retention**: The ability to recall or apply information without referring back to the original source.
- **Cognitive offloading**: Using an external tool or artifact to handle information processing that would otherwise require mental effort — for example, using an LLM to summarize a paper instead of working through it yourself.
- **Confidence calibration**: The degree to which your confidence in your own knowledge matches your actual performance. Well-calibrated learners are confident when they know something and uncertain when they don't.
- **One-shot condition**: A single prompt with no follow-up turns, run in a fresh chat thread. In this assignment, Parts 2A, 2B, and 2C are one-shot conditions.
- **Interactive tutoring condition**: An extended multi-turn session in which you and the LLM go back and forth — you answer questions, signal confusion, generate examples, and the LLM responds and adjusts.
- **Primary research article**: A journal article reporting an original empirical study — with a specific method, participants, and results — as opposed to a review, meta-analysis, or theoretical essay.

### Scoring Dimensions for LLM Output Quality (Use in Part 2)

After each one-shot LLM condition, rate the output on the following dimensions (1–5 scale):

1. **Clarity**: How easy was this response to understand?
   - 1 = confusing, dense, or hard to follow
   - 3 = understandable with effort
   - 5 = immediately clear and well-organized

2. **Depth**: Did this response help you understand *why* the finding matters and *how* the experiment worked, not just *what* the result was?
   - 1 = surface-level summary only, no explanation of logic or mechanism
   - 3 = some explanation of the reasoning, but incomplete
   - 5 = clear account of the underlying logic, method rationale, and significance

3. **Accuracy**: How correct and well-grounded did the response seem?
   - 1 = contained clear errors or significant oversimplifications
   - 3 = mostly accurate with minor gaps or unexamined hedges
   - 5 = accurate, well-nuanced, and appropriately qualified

4. **Fit**: Was the response pitched at the right level for someone reading this paper for the first time?
   - 1 = assumed too much prior knowledge (confusing) or too little (condescending)
   - 3 = mostly appropriate for a first-time reader
   - 5 = well-calibrated to a novice audience, with no unnecessary jargon

### Retention Mini-Test Format (Used in Each Part Below)

After each study condition, you will take a short retention test without looking at any sources. Every mini-test asks the same four questions — two about the specific paper and two about the broader concept it illustrates:

1. **Key Finding** (paper-specific): State the main finding or result of the study in your own words (2–4 sentences). What did the researchers discover?
2. **Method** (paper-specific): Describe the core experimental method (2–4 sentences). What did the researchers actually do? Who were the participants, what was the task, and how was the key variable measured?
3. **Broader Concept** (concept-level): Explain the broader concept or principle this paper illustrates and why it matters beyond this one study (2–4 sentences).
4. **Apply** (concept-level): Answer your paper's application question (see `article_choices.md`).

Each mini-test is scored using an LLM grading tool. The `grading/` folder alongside this assignment contains two kinds of files:

- **`grading_skill.md`** — the grading instructions (same for all papers). This tells the LLM how to grade and in what format to respond.
- **One content file per paper** (e.g., `frederick_2005.md`) — the model answers and scoring criteria for your specific paper.

**How to score each mini-check:**
1. Create your answer file:
  - Create a file called `answers.md` (or `answers.txt`).
  - In that file, write your answers to all four questions, entirely from memory.
  - Make sure to clearly label your answers regarding what question they are answering.
  - Do not open any grading files before writing your answers.
  - As you complete each mini-check, you can update this file with your new answers — you do not need to start from scratch each time.

2. After completing your answer file, open a **fresh chat thread** in your LLM.
3. Upload **three files**: your answers file, `grading_skill.md`, and your paper's content file (e.g., `frederick_2005.md`).
4. In your next message, send this prompt: *”Please grade the answers in my answers file using the grading criteria provided. Provide scores only — no explanations.”*
5. The LLM will return scores only — no explanations. Record those scores in the table provided.

> **Note on free-tier LLMs:** Some LLMs limit the number of files you can upload per session on free accounts (often to one or two). If you run into this, you may need a paid account for the upload workflow. Alternatively, you can copy-paste: open each file in a text editor and paste the contents of `grading_skill.md` as your first message, your paper's content file as your second message, and your answers as your third message (see the format described in `grading_skill.md`). Although if you do this, try not to look too closely at the content of the grading file until after the last section.

**Score scale (for reference):** Each component is scored 0–2, for a maximum of 8 points per mini-test. A score of 2 means accurate and complete; 1 means partially correct; 0 means incorrect, missing, or too vague.

**How to find grading files:** All grading files are in the `grading/` folder in the same location as this assignment on GitHub. Download `grading_skill.md` (you only need this once) and the content file for your chosen paper. File names follow the pattern `wason_1968.md`, `bransford_johnson_1972.md`, etc. — author(s) and year, matching your paper's listing in `article_choices.md`.

### Choosing Your Paper

Open **`article_choices.md`** (in the same folder as this assignment on GitHub) and choose **one topic**, then **one paper** from within that topic. That document contains the full reference, DOI, download instructions, a brief description, and an **application question** for each paper. You will use the same paper and application question throughout this entire assignment.

---

### If You Get Stuck

Reminder: after each study or LLM condition below, you will take a short retention test without looking at any sources. Every mini-test asks four questions — two about the specific paper and two about the broader concept it illustrates.

If you're unable to complete a retention mini-test because you feel like you don't remember anything:

1. Write whatever you do remember, even if it's vague or incomplete. Partial answers are valuable data points.
2. Note specifically what is missing or unclear — is it the method? The finding? The broader concept?
3. Continue with the assignment. The point is to see where understanding fails, not to demonstrate perfect knowledge.
4. If you get stuck on the application question specifically, try restating it in your own words and answering a simpler version first.

---

## Part 0 — Setup + Disclosure (~20 min)

Complete this section before starting your work.

**Models/interfaces used:**
> **[1 POINT]** *YOUR ANSWER HERE — list each model and interface you used (e.g., "Claude Sonnet 3.7, claude.ai web interface").*

**Model version/tier/settings:**
> **[1 POINT]** *YOUR ANSWER HERE — specify free vs. paid, reasoning vs. fast mode, temperature if set, etc.*

**Date/time window:**
> **[1 POINT]** *YOUR ANSWER HERE — approximate date(s) and time range when you did the work.*

**Tools/features used:**
> **[1 POINT]** *YOUR ANSWER HERE — note any special tools (file upload, browsing, deep research, etc.), or write "none".*

**Disclosure statement:**
> **[1 POINT]** *YOUR ANSWER HERE — 2–4 sentences: what you asked the model to do, what text was copied vs. adapted vs. written yourself.*

### Reproducibility Rules

1. Use a **fresh chat thread** for each one-shot condition (Parts 2A, 2B, 2C) and for the interactive tutoring session (Part 3). That is four separate threads total.
2. In Parts 2A, 2B, and 2C: **one prompt only**, one response. No follow-up turns.
3. Record your exact prompt text for all conditions.
4. **Critical rule**: After each LLM condition, complete the retention mini-check **before re-reading the LLM output**. Close the LLM tab or scroll away before writing your answers.
5. Do not use LLM assistance of any kind during Part 1 (reading the paper) or during any retention mini-test.
6. **Do not upload or paste the paper** (or substantial portions of it) into the LLM. The point is to test what the LLM can provide from its training, not to have it summarize a document you feed it.

---

## Part 1 — Read the Paper Without LLM Help (~60-90 min)

Goal: Establish your baseline understanding of the paper and its broader concept before any LLM contact.

### Step 1: Choose and Log Your Paper

**Chosen topic and paper (e.g., "Reasoning and Decision Making — Frederick, 2005"):**
> **[1 POINT]** *YOUR ANSWER HERE.*

**Your application question** (paste the one from your paper's listing in `article_choices.md`):
> **[1 POINT]** *YOUR ANSWER HERE — paste the exact application question you will use in all retention mini-tests throughout this assignment.*

### Step 2: Pre-Study Confidence Rating

Before reading anything, rate your current familiarity with this paper and its topic.

**Pre-study confidence rating (1–5):**
> **[1 POINT]** *YOUR ANSWER HERE — use this scale:*
> - *1 = I don't feel like I know about or understand this topic at all*
> - *2 = I've heard of this topic but couldn't say much about it*
> - *3 = I'm vaguely familiar — I could describe it roughly but lack real detail*
> - *4 = I understand this topic reasonably well*
> - *5 = I could explain this study or concept clearly to someone else*
>
> *Add a brief note explaining your rating.*

### Step 3: Read the Paper (30–40 min)

Read the paper. You may also consult a textbook, internet sources, or encyclopedia entries about the broader topic if you want additional context, but the paper itself should be your primary source. But for this first step, do not use any LLMs to help you better understand the topic in any way. If you want, take brief notes as you read, but focus on understanding rather than transcribing. Generally speaking, this is a comparison for your own sake, so following whatever (non-LLM) process you would typically use to learn about something is a good baseline procedure to follow.

**Sources used:**
> **[1 POINT]** *YOUR ANSWER HERE — list the paper and any supplementary sources (e.g., "Frederick (2005) accessed via JSTOR; also skimmed the Wikipedia entry on the Cognitive Reflection Test").*

**Brief reading notes (your own words — optional but recommended):**
> **[1 POINT]** *YOUR ANSWER HERE — a short outline or notes in your own words (3–8 bullet points). This is for your benefit and will not be graded for accuracy.*

### Step 4: Retention Mini-Test 1 (Close the Paper First)

Close or put away the paper and all sources before completing this test. Do not look at anything while writing. Write these answers in your separate answers file that you will use for grading, but also include them here in the document you turn in.

**1. Key Finding** — state the main finding of the study in your own words (2–4 sentences):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**2. Method** — describe the core experimental method (2–4 sentences):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**3. Broader Concept** — explain the broader concept this paper illustrates and why it matters (2–4 sentences):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**4. Apply** — answer your application question:
> **[2 POINTS]** *YOUR ANSWER HERE.*

### Step 5: Score Mini-Test 1 (Using Grading Tool)

Update `answers.md` with your current answers, then open a fresh chat and upload the three files (`answers.md`, `grading_skill.md`, and your paper's content file). Send the grading prompt and record only the scores the LLM returns — do not request explanations.

| Component | Score (0–2) | Verdict |
|-----------|-------------|---------|
| Key Finding | | |
| Method | | |
| Broader Concept | | |
| Application | | |
| **Total** | **/8** | |

> **[1 POINT]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE — scores from grading tool only.*

**Post-test confidence rating (1–5):**
> **[1 POINT]** *YOUR ANSWER HERE — how confident are you in your mini-test answers? 1 = not at all confident, 5 = very confident.*

**Time spent on Part 1 (minutes):**
> **[1 POINT]** *YOUR ANSWER HERE.*

---

## Part 2 — Three LLM One-Shot Conditions (~60–75 min total)

In this part, you will ask an LLM about the same paper and concept using three different kinds of prompts — one at a time, each in a **fresh thread**, with **one prompt and one response and no follow-ups**. Do not upload or paste the paper into the LLM.

After each condition, complete the retention mini-check **before re-reading the LLM output**. Then go back, re-read the output, paste an excerpt, and fill in the output quality ratings.

---

### Part 2A — Direct Answer Condition (~20 min)

Use a minimal prompt that simply asks what the study found. No special framing or instructions.

**Required prompt template:**
```text
What did [Authors] ([Year]) find in their study "[Paper Title]"?
```

Open a fresh thread. Enter your prompt (filling in your paper's details). Read the response once. Then **close or scroll away from the output** and complete the mini-check below before doing anything else.

**Your exact 2A prompt:**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative 2A output excerpt** (paste this AFTER completing the mini-check below):
> **[1 POINT]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE (roughly 100–200 words).*

#### Retention Mini-Check 2A

Complete this BEFORE re-reading the output. Close the tab or scroll away first.

**1. Key Finding** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**2. Method** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**3. Broader Concept** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**4. Apply** (your application question):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**Mini-Check 2A scores (from grading tool):**

Update `answers.md` with your current answers, then open a fresh chat and upload the three files (`answers.md`, `grading_skill.md`, and your paper's content file). Send the grading prompt and record only the scores the LLM returns.

| Component | Score (0–2) | Verdict |
|-----------|-------------|---------|
| Key Finding | | |
| Method | | |
| Broader Concept | | |
| Application | | |
| **Total** | **/8** | |

> **[1 POINT]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE — scores from grading tool only.*

**Post-condition confidence rating (1–5):**
> **[1 POINT]** *YOUR ANSWER HERE.*

**2A output quality ratings** (rate the LLM output, not your own performance):

| Dimension | Score (1–5) | Notes |
|-----------|-------------|-------|
| Clarity | | |
| Depth | | |
| Accuracy | | |
| Fit | | |

> **[2 POINTS]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE.*

---

### Part 2B — Explanation Condition (~20 min)

Use a scaffolded prompt that asks for a structured explanation of both the study and its broader significance. Open a **fresh thread** (not the same one as 2A).

**Required prompt template:**
```text
I am reading [Authors] ([Year]), "[Paper Title]," for a course on cognition. I need to understand both the specific study and the broader concept it illustrates.

Please explain:
1. What the researchers did (the experimental method)
2. What they found (the key results)
3. Why this finding matters — what broader concept or principle does it demonstrate?
4. One important limitation or caveat

Assume I have a general psychology background but have not encountered this specific topic before.
```

Enter your prompt (filling in your paper's details). Read the response once. Then **close or scroll away** and complete the mini-check below.

**Your exact 2B prompt:**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative 2B output excerpt** (paste AFTER completing the mini-check below):
> **[1 POINT]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE (roughly 100–200 words).*

#### Retention Mini-Check 2B

Complete this BEFORE re-reading the output.

**1. Key Finding** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**2. Method** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**3. Broader Concept** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**4. Apply** (your application question):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**Mini-Check 2B scores (from grading tool):**

Update `answers.md` with your current answers, then open a fresh chat and upload the three files (`answers.md`, `grading_skill.md`, and your paper's content file). Send the grading prompt and record only the scores the LLM returns.

| Component | Score (0–2) | Verdict |
|-----------|-------------|---------|
| Key Finding | | |
| Method | | |
| Broader Concept | | |
| Application | | |
| **Total** | **/8** | |

> **[1 POINT]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE — scores from grading tool only.*

**Post-condition confidence rating (1–5):**
> **[1 POINT]** *YOUR ANSWER HERE.*

**2B output quality ratings:**

| Dimension | Score (1–5) | Notes |
|-----------|-------------|-------|
| Clarity | | |
| Depth | | |
| Accuracy | | |
| Fit | | |

> **[2 POINTS]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE.*

---

### Part 2C — Worked Examples Condition (~20 min)

Use a prompt focused entirely on real-world examples of the concept, not a summary of the study itself. Open a **fresh thread** (not the same as 2A or 2B).

**Required prompt template:**
```text
I am trying to understand the concept demonstrated by [Authors] ([Year]) in "[Paper Title]." Please do not summarize the study itself — instead, give me three concrete, real-world examples where this concept plays out in everyday life. For each example, briefly explain how it illustrates the key principle from the paper.
```

Enter your prompt. Read the response once. Then **close or scroll away** and complete the mini-check below.

**Your exact 2C prompt:**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative 2C output excerpt** (paste AFTER completing the mini-check below):
> **[1 POINT]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE (roughly 100–200 words).*

#### Retention Mini-Check 2C

Complete this BEFORE re-reading the output.

**1. Key Finding** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**2. Method** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**3. Broader Concept** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**4. Apply** (your application question):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**Mini-Check 2C scores (from grading tool):**

Update `answers.md` with your current answers, then open a fresh chat and upload the three files (`answers.md`, `grading_skill.md`, and your paper's content file). Send the grading prompt and record only the scores the LLM returns.

| Component | Score (0–2) | Verdict |
|-----------|-------------|---------|
| Key Finding | | |
| Method | | |
| Broader Concept | | |
| Application | | |
| **Total** | **/8** | |

> **[1 POINT]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE — scores from grading tool only.*

**Post-condition confidence rating (1–5):**
> **[1 POINT]** *YOUR ANSWER HERE.*

**2C output quality ratings:**

| Dimension | Score (1–5) | Notes |
|-----------|-------------|-------|
| Clarity | | |
| Depth | | |
| Accuracy | | |
| Fit | | |

> **[2 POINTS]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE.*

---

### Part 2 Cross-Condition Analysis

**Condition comparison summary table:**

| Condition | Mini-Check Total (/8) | Post-Condition Confidence (1–5) | Overall Impression of Output |
|-----------|-----------------------|---------------------------------|------------------------------|
| 2A — Direct answer | | | |
| 2B — Explanation | | | |
| 2C — Worked examples | | | |

> **[2 POINTS]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE.*

**Analysis paragraph:**
> **[3 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences. Which condition produced the best retention? Which produced the highest confidence? Were those the same condition? What does the pattern suggest about how these three forms of LLM assistance affect learning differently?*

---

## Part 3 — Interactive Tutoring Session (~60–90 min)

Goal: Test whether active back-and-forth interaction with an LLM produces better learning outcomes than any of the one-shot conditions.

Open a **fresh chat thread** for this part. Do not upload or paste the paper.

### Step 1: Opening Setup (~10 min)

Use the following template to establish a tutoring context. Fill in the bracketed parts honestly — your summary of what you currently understand should reflect your actual state of knowledge at this point.

**Required opening prompt template:**
```text
I am reading [Authors] ([Year]), "[Paper Title]," for a course on LLMs and human cognition. I've read the paper and received some summaries, but I don't feel fully confident in my understanding of either the specific study or the broader concept it illustrates.

Here is what I currently think I understand:
[Write 2–4 sentences summarizing your current understanding. Be honest — include what you're unsure about or confused by.]

Please act as a tutor helping me understand this paper and its broader significance. Do not give me a long explanation up front. Instead:
1. Ask me one question to check what I already understand about the study.
2. Based on my answer, correct any misconceptions and fill in the most important gap.
3. Then ask me to apply the concept to a new scenario.
4. Continue building my understanding through back-and-forth questions and brief explanations — do not just lecture.

Confirm you're ready to begin.
```

**Your exact opening prompt:**
> **[1 POINT]** *PASTE YOUR EXACT OPENING PROMPT HERE.*

**Model's response to your opening prompt:**
> **[1 POINT]** *PASTE THE MODEL'S FULL RESPONSE HERE.*

### Step 2: Interactive Tutoring Protocol (at least 8 turns)

Continue the tutoring session. Your goal is active engagement — answer the model's questions, ask your own, signal confusion, generate examples, and push back when something is unclear.

Your session must include at least one instance of each of the following:

- **Two follow-up questions** from you (asking for more explanation or a different angle)
- **One confusion signal** — explicitly tell the model you're not following something (e.g., "I'm not sure I understand — can you explain X differently?")
- **One self-generated example** — offer your own example of the concept and ask if it's correct
- **One answer to a model question** — respond to something the LLM asks you
- **One quiz request** — ask the LLM to quiz you or test your understanding

For each turn below, paste your exact prompt and a brief summary or excerpt (2–5 sentences) of the model's response.

**Turn 1:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

**Turn 2:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

**Turn 3:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

**Turn 4:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

**Turn 5:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

**Turn 6:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

**Turn 7:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

**Turn 8:**
> **[1 POINT]** *PASTE YOUR PROMPT AND A BRIEF EXCERPT OR SUMMARY OF THE MODEL'S RESPONSE.*

*Add more turn blocks if your session had more than 8 turns.*

### Step 3: Post-Tutoring Retention Mini-Check (Close the Thread First)

After completing the tutoring session, **close the LLM thread** or open a new tab so you cannot see the conversation. Then complete the mini-check from memory.

**1. Key Finding** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**2. Method** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**3. Broader Concept** (from memory):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**4. Apply** (your application question):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**Mini-Check Part 3 scores (from grading tool):**

Update `answers.md` with your current answers, then open a fresh chat and upload the three files (`answers.md`, `grading_skill.md`, and your paper's content file). Send the grading prompt and record only the scores the LLM returns.

| Component | Score (0–2) | Verdict |
|-----------|-------------|---------|
| Key Finding | | |
| Method | | |
| Broader Concept | | |
| Application | | |
| **Total** | **/8** | |

> **[1 POINT]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE — scores from grading tool only.*

**Post-tutoring confidence rating (1–5):**
> **[1 POINT]** *YOUR ANSWER HERE.*

**Time spent on Part 3 (minutes):**
> **[1 POINT]** *YOUR ANSWER HERE.*

---

## Part 4 — Final Retention Test + Confidence Calibration (~30–40 min)

**IMPORTANT:** Complete this section **without referring back to any LLM outputs, the paper, study notes, or any other sources.** Ideally, wait at least a few hours after completing Parts 1–3 before doing this section (overnight is even better). If that is not possible, take a short break — at least 15–30 minutes away from the material — before starting.

Goal: Assess what you have actually retained from the entire assignment, and compare your confidence predictions to your actual performance across all conditions.

### Step 1: Final Retention Test (No Sources)

Complete the four prompts below entirely from memory. This is the same format as the mini-checks, but you should aim for somewhat fuller and more precise answers.

**1. Key Finding** — state the main finding in your own words (3–5 sentences this time):
> **[2 POINTS]** *YOUR ANSWER HERE.*

**2. Method** — describe the experimental method, including details you may not have remembered in earlier tests:
> **[2 POINTS]** *YOUR ANSWER HERE.*

**3. Broader Concept** — explain the broader concept, including something about why it matters that is **different** from what you wrote in earlier mini-checks:
> **[2 POINTS]** *YOUR ANSWER HERE.*

**4. Apply** — answer your application question:
> **[2 POINTS]** *YOUR ANSWER HERE.*

**Final retention test scores (from grading tool):**

Update `answers.md` with your current answers, then open a fresh chat and upload the three files (`answers.md`, `grading_skill.md`, and your paper's content file). Send the grading prompt and record only the scores the LLM returns.

| Component | Score (0–2) | Verdict |
|-----------|-------------|---------|
| Key Finding | | |
| Method | | |
| Broader Concept | | |
| Application | | |
| **Total** | **/8** | |

> **[1 POINT]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE — scores from grading tool only.*

### Step 2: Confidence Calibration Summary

Fill in the table below using the confidence ratings and retention scores you recorded throughout the assignment.

| Condition | Post-Condition Confidence (1–5) | Retention Mini-Check Score (/8) |
|-----------|--------------------------------|---------------------------------|
| Part 1 — Read the paper | | |
| Part 2A — Direct answer | | |
| Part 2B — Explanation | | |
| Part 2C — Worked examples | | |
| Part 3 — Interactive tutoring | | |
| Part 4 — Final retention test | — | |

> **[2 POINTS]** *REPLACE THIS LINE WITH YOUR COMPLETED TABLE.*

**Calibration reflection:**
> **[3 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences. When were you most confident? When did you perform best? Did your confidence accurately predict your performance across conditions, or were there cases where you were overconfident or underconfident? What does this pattern suggest about how each form of LLM assistance affects your sense of understanding?*

---

## Part 5 — Final Reflection (~30–40 min)

Answer all questions below. Write 3–5 sentences per question.

**1. Which condition produced the best actual retention according to your mini-check scores? Why do you think that was the case?**
> **[3 POINTS]** *YOUR ANSWER HERE — 3–5 sentences.*

**2. Which condition felt most helpful in the moment? Did "feeling helpful" and "producing actual retention" point to the same condition?**
> **[3 POINTS]** *YOUR ANSWER HERE — 3–5 sentences.*

**3. Describe a specific moment in the assignment when it felt like the LLM was doing cognitive work that should have been yours. What were you doing, and what did you let the model do instead?**
> **[3 POINTS]** *YOUR ANSWER HERE — 3–5 sentences.*

**4. Try to articulate a principle for when LLM use in a learning situation feels like genuine support and when it feels like cheating or bypassing learning. State it specifically enough that someone else could apply it. Where is the line unclear even after thinking about it?**
> **[4 POINTS]** *YOUR ANSWER HERE — 3–5 sentences.*

**5. Would you use LLMs differently for learning tasks after doing this assignment? If so, how?**
> **[3 POINTS]** *YOUR ANSWER HERE — 3–5 sentences.*

**6. If you were to repeat this assignment, what is the one thing you would change first?**
> **[2 POINTS]** *YOUR ANSWER HERE — 2–4 sentences.*

---

## Discussion Prep (for class group sharing)

Prepare a 2-minute summary to share with your group. Fill in the items below.

**Which paper you read and which condition produced your best retention:**
> **[1 POINT]** *YOUR ANSWER HERE — 1–2 sentences.*

**Your most surprising result — a moment where performance and expectation diverged:**
> **[1 POINT]** *YOUR ANSWER HERE — 1–2 sentences.*

**Your current working principle for when LLM use supports learning vs. bypasses it:**
> **[1 POINT]** *YOUR ANSWER HERE — 1–2 sentences.*

**One question about learning and LLMs that you still don't know the answer to:**
> **[1 POINT]** *YOUR ANSWER HERE — 1 sentence.*

---

## What to Turn In

Submit your completed version of this `.md` file to Canvas. Before submitting, confirm:

- [ ] Part 0 Setup + Disclosure is filled in.
- [ ] Your chosen paper and application question are recorded (Part 1, Step 1).
- [ ] All three one-shot prompts (Parts 2A, 2B, 2C) and the opening tutoring prompt (Part 3) are pasted in.
- [ ] All three one-shot output excerpts (Parts 2A, 2B, 2C) are included.
- [ ] Part 3 tutoring session log (all 8+ turns) is included.
- [ ] All five retention mini-check score tables (Parts 1, 2A, 2B, 2C, 3) are completed with scores from the grading tool.
- [ ] The final retention test (Part 4, Step 1) is completed and scored using the grading tool.
- [ ] The confidence calibration summary table (Part 4, Step 2) is filled in.
- [ ] Final reflection (all 6 questions) is written.
- [ ] Discussion prep section is filled in.
- [ ] All "YOUR ANSWER HERE" placeholders have been replaced.
