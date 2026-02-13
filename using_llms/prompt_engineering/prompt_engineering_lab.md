# Prompt Engineering Lab

**Target time:** ~5 hours total  
**Models required:** ChatGPT + Gemini (optional: third model)  
**Grading:** effort-based  
**Submission:** one document (3–5 pages) *or* the completed template tables below. PDF, Microsoft Word (.docx), or Markdown (.md) is fine)
---

## Part 0 — Setup + disclosure (10–15 min)

Include, at the top of your submission:
- **Models/interfaces used:** choose two different models. This can be ChatGPT, Gemini, others of your choice, or two versions of the same model (e.g. Gemini "Fast" vs. Gemini "Thinking". 
- **Model Version:** For each model you use, specify whether you are using the free or a paid version, and what settings you used (e.g., "fast", "thinking", "pro", "deep research", etc.
- **Date/time window:** (approximate is fine)
- **Any special settings/tools:** (files uploaded, browsing mode, “deep research,” etc.)
- **Disclosure statement:** 2–4 sentences describing how you used LLMs in completing the assignment (what you asked, what you copied/adapted, what you wrote yourself).
---

## Part 1 — Minimal-pairs prompt experiment (core; ~2.5 hours)
In this exercise you will be prompting LLMs 16 times, and analyzing and comparing the output.
Pick **one** domain below and run **8 minimal prompt pairs** in **both** ChatGPT and Gemini (total of 16).

### Choose one domain
1. Explaining one of the topics we've covered so far (language models, distributional semantics, artificial neural networks, large language models).
2. Explaining the cultural significance of a movie, TV show, or musical artist you enjoy.
3. Explaining the health benefits or risks of something of your choice (a diet, a food, an activity, a substance...).
4. Explaining some other topic that you want to talk to the LLMs about (such as a topic related to research you are involved in doing or are interested in).

Remember, you will be sharing this with your group, and possibly the whole class, so don't pick a topic that would make you or others uncomfortable.

### Rules
You are going to construct 8 versions of the same prompt for each model. These prompts will combine your topic of choice with additional context determined by 4 binary variables below.
- **Minimal pair rule:** For each variable, the prompt will differ by *one targeted change* (one instruction, one constraint, one sentence).
- **Control the context:** Start a **new chat** (fresh context) for each run when possible. If you have a paid account with ChatGPT or Gemini, create each new prompt within a "Temporary "
- **Keep everything else constant:** copy/paste the exact same text into each model for each prompt.
- **Record short excerpts:** For each prompt, save the output into a file. You don't need to turn in all outputs, just your summary of the differences. But please save them so you can reference them, and possibly use them in a future assignment.

### Base Prompt
1. **Base (Control) Prompt:** 
Your first prompt will be a simple vague prompt.
For example, perhaps you want to "Explain the cultural significance of the US TV show Arrested Development". 
Please feel encouraged to make that base prompt a little more complex and interesting, and not just simple copy of my four domain questions above. 
Make it a little more detailed and specific to your interests.

### 7 Experimental Prompts. 
Next, create 7 more versions of your prompt, by modifying it in the ways described below:
<br>

2. **Goal specificity:** This manipulation will transform your base prompt's vague/unspecificed goal to an explicit success criteria. For example:
```
Explain the cultural significance of the US TV show Arrested Development.
Success criteria:
1. State a clear thesis in 1–2 sentences.
2. Give three distinct reasons it mattered culturally (e.g., comedy style, TV industry influence, internet/meme culture, politics/class satire, etc.).
3. For each reason, include one concrete example (a recurring bit, character dynamic, narrative technique, or reception fact) and explain how it supports the reason.
4. Include one limitation/counterpoint (e.g., niche audience, timing, mixed reception) and how it affects its legacy.
5. Keep it 250–350 words and end with a one-sentence takeaway.
```

3. **Audience framing:** This will add the addition of additional context telling the model who the target audience of the output is.
Feel free to make this whatever you want. But please make it as detailed as possible. Example:

```
Explain the cultural significance of the US TV show Arrested Development to a high school student who hasn’t seen it.
Assume they know what a sitcom is, but don’t assume they know early-2000s TV history.
Write in a friendly, accessible tone and define any term you think could be unfamiliar.
```

4. **Output format constraint:** This will specify the structure of the output (e.g., freeform, in a table, in a bulleted list, JSON). Example:

```
Explain the cultural significance of the US TV show Arrested Development.
Output format constraint: Use exactly 6 bullet points, in this order, 
with each bullet labeled with these terms in bold, followed by the content:
1. One-sentence thesis (what makes it culturally significant)
2. Comedy innovations (2–3 sentences)
3. Narrative/structural innovations (2–3 sentences)
4. Industry/TV history impact (2–3 sentences)
5. Internet/meme/quotation culture (2–3 sentences)
6. One limitation/counterpoint (1–2 sentences)
```

5. **Context provision:** This will give additional context and/or added background/assumptions, that help constrain the answer the model gives:
```
Explain the cultural significance of the US TV show Arrested Development.
Context/assumptions: For this question, treat “cultural significance” as a combination of:
• Influence on later TV comedy (style, structure, production norms)
• How it reflected or shaped public discourse (class, politics, celebrity, family)
• How audiences interacted with it (quoting, memes, fandom, rewatch culture)
You can assume the reader knows what a sitcom is but has not seen the show.
```
6. **Decomposition:** This will provide context to the model about how it should approach answering the question. 
How "off the cuff" should it's answer be, versus how much should it plan its answer or get feedback first? Example:
```
Explain the cultural significance of the US TV show Arrested Development.
Before writing the answer, write a brief plan (3–5 bullets) for how you will structure your explanation. 
Then write the answer.
```
Alternatively,
```
Explain the cultural significance of the US TV show Arrested Development.
Before writing the answer, ask me three follow up questions about how to structure the answer.
Then, provide an answer based on those questions.
```
7. **Verification step:** Here, we will add instructions that guide the LLM to check its answer, and give some info on how it would verify its claim. Example:
```
Explain the cultural significance of the US TV show Arrested Development.
After your explanation, add a section titled “Self-check” with:
1. Three specific claims you made that might be fact-dependent (e.g., dates, awards, influence claims).
2. For each claim, label your confidence high/medium/low and briefly say what would verify it (type of source, not a URL).
```

8. **Tradeoff constraint:** In this prompt, you can consider some tradeoffs you could give the model, to constrain how it answers. “be brief” vs “be thorough,” or “optimize for creativity” vs “optimize for accuracy”.
Tradeoff constraints can be things like:
- Brevity ↔ completeness
- Accuracy/calibration ↔ coverage
- Depth ↔ accessibility
- Neutrality ↔ persuasion
- Creativity ↔ factual grounding
- Specificity ↔ generality
- Structure ↔ spontaneity
- Safety/caution ↔ helpfulness/actionability
- Speed ↔ quality
- Engagement ↔ study value
Prompt example:
```
Explain the cultural significance of Arrested Development.
Optimize for accuracy: avoid speculative claims, avoid exaggeration, and clearly separate what’s widely agreed from what’s interpretive.
```

### What to turn in for Part 1

For each of your 8 prompts in both models, turn in:
- the prompt itself that you used
- A short excerpt from the two models' output (enough to show the difference)
- A brief note: **what changed** (structure, factuality, hedging, refusal, creativity, specificity, etc.), both between the models and from the base prompt to the experimental prompt


## Part 2 — Prompt Repair Clinic (practical skills; ~1.5 hours)

In Part 1, you will probably see some outputs that are disappointing (too vague, too long, off-topic, poorly structured, confidently wrong, biased/one-sided, etc.). In Part 2, you will practice **repairing the prompt** so the model produces a more useful result.

### Step 1: Choose 2 “worst” cases (from Part 1)
Pick **two** prompt runs where the output was clearly not what you wanted. Examples of “worst” outcomes:
- The model **ignored** your requested format (e.g., you asked for a table and got paragraphs).
- The answer is **generic** (sounds plausible but says little).
- The answer is **overconfident** or makes questionable factual claims without flagging uncertainty.
- The answer is **one-sided** or frames an issue in a biased way.
- The answer is **incomplete** (misses key aspects you expected).
- The answer is **hard to use** (no structure, no actionable next steps).

For each chosen case, you will do a **3-version repair sequence** in **both of the models you are using**.

---

## What you do for each case: v0 → v1 → v2

### v0 (baseline): the original prompt
This is the exact prompt you originally used in Part 1 that produced the bad result.

**You include:**
- The exact prompt text
- A short excerpt of the output (enough to show what went wrong)
- 1–2 sentences describing the problem

**Example v0 problem statements (pick what fits):**
- “Output was too vague; it never gave concrete examples.”
- “It wrote a plot summary instead of cultural significance.”
- “It ignored my request for JSON and added extra commentary.”
- “It made strong claims but I’m not sure they’re true.”

---

### v1 (structured repair): rewrite the prompt using the checklist
For v1, you keep the **same task**, but you rewrite the prompt so it is **much harder for the model to misunderstand**. You do this by explicitly adding the following elements (you can use short lines or mini-headings inside the prompt):

**v1 Checklist (include all 5):**
1) **Goal**: What do you want the model to produce?
2) **Audience**: Who is this for? What do they already know?
3) **Constraints**: Length, tone, what to avoid (e.g., “no spoilers”), number of points, etc.
4) **Context/assumptions**: Any background that changes what counts as a good answer.
5) **Success criteria**: A mini “definition of done” (what must be present for you to consider it successful).

#### v1 Example (based on the Arrested Development topic)
*(This is just an illustration of what “v1” looks like. Your topic can be different.)*

> Explain the cultural significance of the US TV show *Arrested Development*.  
> **Audience:** A college student who has not seen the show and doesn’t know early-2000s TV history.  
> **Goal:** Help them understand why people consider it culturally important.  
> **Context:** Focus on comedic technique, narrative structure, and influence/reception (not plot summary).  
> **Constraints:** 250–300 words; avoid spoilers; define any jargon in plain language.  
> **Success criteria:** Include (1) a 1–2 sentence thesis, (2) 3 distinct reasons it mattered, (3) one concrete example for each reason, and (4) one counterpoint/limitation.

**What you write after running v1 in both models:**
- Did v1 fix the original problem? How?
- What did it still do poorly?

---

### v2 (advanced repair): add ONE advanced tactic to your v1 prompt
For v2, start with your v1 prompt and add **exactly one** advanced tactic below. The goal is to push the model from “better” to “reliably good” or “more usable.”

Choose ONE:

#### Option A — One-shot example (show the model the format you want)
You provide a tiny example of the *shape* of a good answer so the model imitates it.

**Example add-on (generic):**
> **Example of the level of specificity I want (not about this show):**  
> “Thesis: X mattered because it changed Y.  
> Reason 1: It used Z technique (example: …) which influenced …”

Key idea: your example should demonstrate **structure and specificity**, not dump lots of content.

#### Option B — Rubric/table for evaluation (force explicit quality criteria)
You require the model to output a table that makes it harder to be vague.

**Example add-on (generic):**
> After the answer, include a table with 3 rows (one per main reason) and columns:  
> **Claim | Concrete example | Why it supports the claim | Confidence (high/med/low)**

This often improves organization, but it can also tempt the model to invent examples—note that if it happens.

#### Option C — Step-by-step plan with checkpoints (decompose the task)
You force the model to plan first and then produce the answer.

**Example add-on:**
> Before writing the answer:  
> 1) List the 3 reasons you will use.  
> 2) For each reason, list one concrete example you will mention.  
> 3) Then write the final answer following that plan.

This can reduce tangents and make the structure more consistent.

#### Option D — Ask clarifying questions first (make uncertainty explicit)
You require the model to ask questions that would change the answer.

**Example add-on:**
> First ask exactly 2 clarifying questions about what angle I want (e.g., industry impact vs cultural memes).  
> Then, without waiting for my response, answer twice:  
> - Version 1: assuming I care most about industry/TV history  
> - Version 2: assuming I care most about internet culture and quotes

This can reveal what the model thinks is ambiguous and how it adapts.

---

## What you write up for each case (short, but explicit)

For each of your 2 cases, include:

1) **What was wrong with v0** (1–2 sentences)  
2) **Your v1 prompt** + brief note: what checklist items you added and why  
3) **Your v2 prompt** + which advanced tactic you chose and why  
4) **Compare outputs across v0/v1/v2** for ChatGPT and Gemini:
   - What improved?
   - What did not improve?
   - Did the two models respond differently to the same repair?

**Important:** You do not have to “solve” the prompt perfectly. The goal is to show that you can **diagnose a failure** and make targeted repairs that measurably change the output.


## Part 3 — What you learned (closing; ~45–60 min)

### 3A. Your “Top 10 prompt principles” cheat sheet

Write 10 actionable rules-of-thumb you learned from your results.

- At least **3** principles must be **domain-specific** to the domain you chose (e.g., creativity vs data analysis prompting).

**Top 10 principles:**
1.  
2.  
3.  
4.  
5.  
6.  
7.  
8.  
9.  
10.  

### 3B. Model comparison paragraph

In one paragraph, answer:

- Where did your two models behave similarly?
- Where did they reliably diverge (format adherence, caution/hedging, creativity, refusal style, etc.)?
- Give **one concrete example** for each claim (you can reference your tables by pair/case number).

---
