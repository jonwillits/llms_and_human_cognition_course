# LLM Debate Analysis

## Background Info

### Purpose of This Assignment

This assignment asks you to do a structured epistemic analysis of a real argument about LLMs. Not to win a debate, but to understand exactly what the argument claims, how strong its logic is, what evidence exists, and where genuine uncertainty lives. The goal is calibrated reasoning: ending the assignment with views that are more precise and better-grounded than where you started. You will work through a six-step framework that moves from formal argument structure to empirical evidence to value disagreements — the same progression covered in the first lecture on this topic.

You will do this work in three passes. In Part 1, you work through all six steps on your own, without LLM assistance. In Part 2, you use scaffolded LLM prompts to check and improve your work on each step, then update your answers based on what you learn. In Part 3, after Monday's group discussion, you write your final answer to each step. Each pass builds on the one before it, and the differences between them — what changed, and why — are as important as the final answers themselves.

### Quick Specs

- **Target time:** ~5–6 hours (prior to class for completing parts 0, 1 and 2) + in-class group discussion and updating your responses (Part 3, ~80 min) and group presentation (~6 min). Then ~30 minutes for Part 4 final reflection. 
- **Model requirements:** Any LLM you have access to (ChatGPT, Claude, Gemini, etc.; free tier is sufficient). Use the same model throughout Parts 1–3 if possible, and document which one.
- **Grading basis:** Effort, process quality, reasoning quality, and reflection — not whether your conclusions are "correct"
- **Submission format:** Edit and submit this `.md` file

### How to Download This File

1. On the GitHub page for this file, click the **Raw** button (top-right of the file view).
2. Right-click anywhere on the page and choose **Save As**.
3. Make sure the filename ends in `.md` and save it somewhere you can find it.
4. Open it in any text editor (VS Code, PyCharm, Notepad, TextEdit, etc.) to fill it in.
5. Submit the completed `.md` file to Canvas.

### The Six-Step Framework (Quick Reference)

These steps are covered in detail in the kickoff lecture slides. Review them before starting.

1. **Identify the argument** — Write out the premises and conclusion explicitly in standard form. Surface hidden premises.
2. **Evaluate validity and soundness** — Is the conclusion guaranteed by the premises (validity)? Are the premises well-supported (soundness)? Identify fallacies.
3. **Classify the premises** — For each premise, decide: empirical, normative, conceptual, or mixed?
4. **Evaluate the existing evidence** — For empirical premises, assess what evidence currently exists and how strong it is.
5. **Specify the missing data** — For unresolved empirical questions, describe concretely what data would be needed and whether it is feasible to obtain.
6. **Address non-empirical premises** — For normative and conceptual premises, apply consistency checks and clarify what the underlying value or conceptual disagreement actually is.

### Finding Your Starter Argument

Your topic's starter arguments are available in the course GitHub repository under `llm_debates/arguments/`. Open the file for your assigned topic (e.g., `5.md` for Topic 5). You will find several arguments, each written in natural language as it might appear in an op-ed, a policy document, or an online discussion. Read them, choose one that interests you, and paste the full text into Part 0A.

If you find an argument that interests you outside the provided set — in a reading, a news article, or elsewhere — you may use that instead, as long as you note the source and it is clearly relevant to your topic.

### How This Assignment Works

- **Before Monday class:** Complete Parts 0, 1, and 2 (individual analysis + LLM-assisted revision). This is the bulk of the out-of-class work.
- **Monday class:** Discuss your analyses with your group (Part 3 happens here). By the end of class, you should have final answers for all six steps.
- **After Monday, before Wednesday:** Complete Part 4 (reflection on position change) and the Presentation Prep section.
- **Wednesday class:** Your group presents a 5-minute summary. Each group member presents one step.

### If You Get Stuck

- **Step 1 (hidden premises):** Ask yourself: "Even if all the stated premises are true, what else would have to be true for the conclusion to follow?" Write those things down as premises.
- **Step 2 (validity):** Try the counterexample method: imagine a world where all the premises are true. Can you describe any scenario in which the conclusion would still be false? If yes, the argument is invalid.
- **Step 3 (empirical vs. normative):** Ask: "Could a well-designed study settle this, or would people with different values still disagree even if they agreed on all the facts?" If a study could settle it, it is empirical. If not, it is normative or conceptual.
- **Step 4 (evidence):** If you cannot think of relevant evidence on your own, use your Part 2 LLM prompt before writing your Part 1 answer for this step — but make sure you can explain and evaluate whatever the LLM tells you. Do not paste LLM output into Part 1.
- **Step 6 (non-empirical premises):** For each value claim, ask: "Does the person making this argument apply this principle consistently to other, analogous cases? If not, what makes LLMs different, and do they have an explicit argument for that distinction?"

---

## Part 0 – Setup and Initial Reaction (~20 min)

*Complete Parts 0A and 0B before beginning any analysis. Complete Part 0C before submitting.*

### Part 0A – Your Argument

**Your topic (name and number):**

> **[X POINTS]** *YOUR ANSWER HERE — e.g., "Topic 5: Cognitive Ecology and the Attention Economy".*

**Your chosen argument (paste the full text):**

> **[X POINTS]** *PASTE THE FULL TEXT OF YOUR CHOSEN ARGUMENT HERE. Include the source if it comes from outside the provided starter arguments.*

### Part 0B – Initial Reaction

*Write this before reading further or doing any analysis.* In 3–5 sentences, capture your gut response to the argument. Does it seem persuasive at first read? Do you find yourself wanting to agree or disagree? What strikes you as the most plausible or most questionable part?

**Initial reaction:**

> **[X POINTS]** *YOUR ANSWER HERE — 3–5 sentences, written before any analysis.*

### Part 0C – LLM Disclosure

*Fill this in before submitting.*

**Models/interfaces used:**

> **[X POINTS]** *YOUR ANSWER HERE — list each model and interface you used (e.g., "Claude Sonnet 3.7, claude.ai web interface").*

**Model version/tier/settings:**

> **[X POINTS]** *YOUR ANSWER HERE — specify free vs. paid, reasoning vs. standard mode, temperature if set, etc.*

**Date/time window:**

> **[X POINTS]** *YOUR ANSWER HERE — approximate date(s) and time range when you did the work.*

**Tools/features used:**

> **[X POINTS]** *YOUR ANSWER HERE — note any special tools (web browsing, file upload, deep research mode, etc.), or write "none".*

**Disclosure statement:**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences: describe generally how you used LLMs in this assignment. How much of your final Part 3 answers reflects your own reasoning versus what the LLM contributed?*

---

## Part 1 – Individual Analysis (~90–120 min)

Work through all six steps below **without using an LLM**. Your goal is to think through the argument carefully on your own before getting any outside help. There are no perfect answers at this stage — work carefully, be explicit about your reasoning, and make your best attempt.

### Step 1: Identify the Argument

Write out the argument in **standard logical form**. List each premise explicitly (P1, P2, P3, …) followed by the conclusion (C). Try not to leave premises implicit or unstated. If you detect that the argument requires a claim to be true in order for the conclusion to follow, state it as a premise — even if the original text did not state it directly. Your goal is the strongest, most complete reconstruction of the argument you can produce. Label the claims as whether they are stated or unstated.

Example format:
- P1: [claim 1] (stated)
- P2: [claim 2] (stated)
- P3: [claim 3] (unstated)
- C: Therefore, [conclusion]

**Your standard form (Part 1):**

> **[X POINTS]** *YOUR ANSWER HERE — list each premise and the conclusion explicitly. Flag any premises you identified as hidden by adding "[hidden]" after them.*

---

### Step 2: Evaluate Validity and Soundness

**Validity:** Does the conclusion follow necessarily from the premises? If you think the argument is invalid, describe a counterexample — a scenario in which all the premises could be true but the conclusion would still be false. You can also use a truth table to demonstrate validity if you know how to do that.

**Soundness:** Are the premises actually well-supported? For each premise, give a brief judgment: do you think it is likely true, uncertain, or likely false — and why? You do not need to cite sources at this stage; reason from what you know.

**Your validity assessment (Part 1):**

> **[X POINTS]** *YOUR ANSWER HERE — is the argument valid? If not, what is your counterexample?*

**Your soundness assessment (Part 1):**

> **[X POINTS]** *YOUR ANSWER HERE — for each premise (P1, P2, etc.), briefly state whether you think it is likely true, uncertain, or likely false, and why.*

---

### Step 3: Classify the Premises

Go through your premises from Step 1 and classify each one as:

- **Empirical** — a claim about how the world is that could in principle be tested with data
- **Normative** — a value claim about what should be done, what matters, or what is good
- **Conceptual** — a claim about what a term means or how a category should be defined
- **Mixed** — a premise with both empirical and non-empirical components (identify each part separately)

For each classification, give a brief explanation of your reasoning. A useful test: "Could a well-designed study settle this claim, or would people with different values still disagree even after seeing the data?"

**Your premise classifications (Part 1):**

> **[X POINTS]** *YOUR ANSWER HERE — list each premise, your classification, and a 1–2 sentence explanation.*

---

### Step 4: Evaluate the Existing Evidence

For each **empirical** premise you identified in Step 3, assess the current state of evidence. What do we actually know? Consider:

- What kinds of studies or data would bear on this claim?
- How strong is the existing evidence — in terms of sample size, replication, measurement validity, and generalizability?
- Does the evidence actually address the specific claim in the premise, or does it address something related but different?
- Are there common evidence quality problems present — such as cherry-picked examples, anecdotal evidence scaled to broad claims, or benchmark performance conflated with real-world capability?

Be accurate. Do not dismiss weak evidence as worthless, but do not overclaim from it either.

**Your evidence evaluation (Part 1):**

> **[X POINTS]** *YOUR ANSWER HERE — for each empirical premise, describe what evidence you are aware of and how strong you think it is.*

---

### Step 5: Specify the Missing Data

For any empirical premises that remain unresolved or poorly supported after Step 4, describe concretely what data would be needed to address them. "More research is needed" is not a sufficient answer. Be specific:

- What outcome or variable would be measured?
- In what population or context?
- Using what study design?
- Over what time scale?

Then assess feasibility: are there ethical, logistical, or temporal barriers that would make this data difficult or impossible to obtain? What does that mean for how confident anyone should be right now?

**Your missing data specification (Part 1):**

> **[X POINTS]** *YOUR ANSWER HERE — for each unresolved empirical premise, describe the specific data needed and note any feasibility constraints.*

---

### Step 6: Address Non-Empirical Premises

For each **normative or conceptual** premise from Step 3, do two things:

1. **Consistency check:** Identify other cases where the same principle would apply. Does the argument hold consistently across those analogous cases? If there are inconsistencies — situations where the argument's advocates would likely resist applying the same principle — name them explicitly.

2. **Clarify the disagreement:** Articulate what two well-informed people who disagree on this premise are actually disagreeing about. Is it a fundamental value difference, a conceptual dispute about what a word means, or a normative premise that actually contains a hidden empirical component?

**Your non-empirical premise analysis (Part 1):**

> **[X POINTS]** *YOUR ANSWER HERE — for each normative or conceptual premise, give your consistency check and clarify what the underlying disagreement is.*

---

## Part 2 – LLM-Assisted Revision (~90–120 min)

For each step, a scaffolded prompt is provided. Use it — adapting the bracketed sections to your specific argument and answers — to get LLM feedback on your Part 1 work. Read the response carefully and critically: LLMs can misstate findings, miss important premises, overstate certainty, or flag "problems" that are not actually problems. The LLM is a thinking partner, not an authority.

For each step you must provide:
1. The **exact prompt** you sent
2. A **representative excerpt** of the model's response
3. Your **revised answer** for that step
4. A brief explanation of **what changed** (or, if nothing changed, why your original answer held up)

---

### Step 1 Check: Identify the Argument

Use this prompt (fill in the bracketed sections):

```
Here is the argument I am analyzing:

[paste the full argument text]

Here is my attempt to write it in standard logical form, with explicit premises and conclusion:

[paste your standard form from Part 1, Step 1]

Please do the following:
1. Tell me whether my premises and conclusion accurately capture the argument.
   Are any premises incorrectly stated or imprecise?
2. Identify any hidden premises I may have missed — claims that must be true
   for the conclusion to follow from the premises but that are not explicitly stated.
3. For each hidden premise you identify, briefly explain why it is needed and
   why it might be questionable.
4. Do not rewrite the argument for me — give me specific feedback on what I
   got right and what I missed.
```

**Your exact prompt:**

> **[X POINTS]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative LLM response excerpt:**

> **[X POINTS]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE.*

**Your revised Step 1 answer:**

> **[X POINTS]** *YOUR ANSWER HERE — write your revised standard form, incorporating any new or corrected premises.*

**What changed and why:**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences. What did the LLM catch that you missed, or why did your original answer hold up?*

---

### Step 2 Check: Evaluate Validity and Soundness

Use this prompt:

```
Here is the argument in standard form that I am analyzing:

[paste your updated standard form from Part 2, Step 1]

Here is my assessment of its validity and soundness:

Validity: [paste your validity assessment from Part 1, Step 2]

Soundness: [paste your soundness assessment from Part 1, Step 2]

Please do the following:
1. Check my validity assessment. Is the argument structurally valid? If not,
   can you describe a counterexample — a scenario where all premises are true
   but the conclusion is still false?
2. Check my soundness assessment. Which premises do you think are most
   questionable, and why? Did I rate any too charitably or too harshly?
3. Identify any formal or informal fallacies present in the argument — for
   example: affirming the consequent, slippery slope, false dilemma, appeal
   to nature, or begging the question. Briefly explain each one you find.
4. Do not tell me what conclusion to draw — give me specific feedback on the
   quality of my analysis.
```

**Your exact prompt:**

> **[X POINTS]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative LLM response excerpt:**

> **[X POINTS]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE.*

**Your revised Step 2 answer:**

> **[X POINTS]** *YOUR ANSWER HERE — write your revised validity and soundness assessments.*

**What changed and why:**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences.*

---

### Step 3 Check: Classify the Premises

**Important:** Your Part 1 classifications must be written before you use this prompt. The LLM is checking your work, not doing it for you.

Use this prompt:

```
Here are the premises from the argument I am analyzing, along with my
classification of each as empirical, normative, conceptual, or mixed:

[paste your premises and classifications from Part 1, Step 3]

Please do the following:
1. For each premise, tell me whether you agree or disagree with my
   classification and briefly explain why.
2. If you think a premise I classified as empirical is actually normative or
   conceptual (or vice versa), explain what makes it so.
3. If any premise is "mixed," explain how you would separate the empirical
   component from the non-empirical component.
4. Do not reclassify everything for me — flag disagreements and explain
   your reasoning.
```

**Your exact prompt:**

> **[X POINTS]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative LLM response excerpt:**

> **[X POINTS]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE.*

**Your revised Step 3 answer:**

> **[X POINTS]** *YOUR ANSWER HERE — write your revised premise classifications. For each premise, note whether your classification changed and why.*

**What changed and why:**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences.*

---

### Step 4 Check: Evaluate the Existing Evidence

This step uses the LLM more heavily than the others. Surveying a debate's empirical landscape is genuinely time-consuming, and the LLM can help you find relevant research leads quickly. However, LLMs can misstate findings, describe studies inaccurately, or overstate how settled a literature is. Treat every specific claim it makes as a lead to think critically about, not a fact to accept.

You may use multiple turns for this step if needed — for example, asking a follow-up to probe a specific claim or to push for more specific study designs. Paste a representative sample of the exchange.

Use this prompt as a starting point:

```
I am analyzing an argument about [brief topic description — e.g., "whether
regular LLM use leads to cognitive skill decline over time"].

These are the empirical premises I identified:

[paste your empirical premises from Part 2, Step 3]

Here is my initial assessment of the existing evidence for each one:

[paste your evidence evaluation from Part 1, Step 4]

Please do the following:
1. For each empirical premise, describe what kinds of evidence currently
   exist that bear on it. What research domains, study types, or findings
   are most relevant?
2. Assess the quality and strength of this evidence: How well-replicated
   is it? How generalizable? Does it actually address the specific claim
   in the premise, or only a related but different question?
3. Flag any common evidence quality problems that apply here — such as
   cherry-picked examples, benchmark conflation, anecdotal evidence scaled
   to universal claims, or confounded study designs.
4. Where my initial assessment seems incomplete or off-base, point that
   out specifically.
```

**Your exact prompt(s):**

> **[X POINTS]** *PASTE YOUR EXACT PROMPT(S) HERE. If you used multiple turns, paste all of them.*

**Representative LLM response excerpt:**

> **[X POINTS]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE.*

**Your revised Step 4 answer:**

> **[X POINTS]** *YOUR ANSWER HERE — write your revised evidence evaluation, incorporating what you learned.*

**What changed and why:**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences.*

---

### Step 5 Check: Specify the Missing Data

Use this prompt:

```
Here are the empirical premises I identified as unresolved or insufficiently
supported after evaluating the existing evidence:

[paste the relevant empirical premises]

Here is my specification of what data would be needed to address each one:

[paste your Step 5 answer from Part 1]

Please do the following:
1. Assess whether my specifications are concrete enough. For any that are
   vague — such as "more research is needed" — help me make them specific:
   what would be measured, in what population, over what time period, and
   using what design?
2. Are there feasibility constraints I missed — ethical, logistical, or
   temporal barriers that would make this data difficult or impossible to
   collect?
3. Are there alternative study designs I haven't considered that might be
   more feasible while still addressing the question?
4. Do not rewrite my specifications — give me feedback on gaps and how to
   strengthen them.
```

**Your exact prompt:**

> **[X POINTS]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative LLM response excerpt:**

> **[X POINTS]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE.*

**Your revised Step 5 answer:**

> **[X POINTS]** *YOUR ANSWER HERE — write your revised missing data specification.*

**What changed and why:**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences.*

---

### Step 6 Check: Address Non-Empirical Premises

Use this prompt:

```
Here are the non-empirical premises from the argument I am analyzing, along
with my consistency checks and analysis of the underlying disagreements:

[paste your non-empirical premises and Step 6 analysis from Part 1]

Please do the following:
1. For each non-empirical premise, probe for inconsistencies I may have
   missed: are there analogous cases where the same principle would apply
   but where the argument's advocates would likely resist applying it?
   If so, what does that inconsistency reveal?
2. Help me identify the most fundamental underlying value or conceptual
   commitment at stake in each premise. What is the real disagreement about?
3. Are there any premises I treated as purely normative that actually contain
   hidden empirical components? If so, what are those components, and how
   does extracting them change the analysis?
4. Do not tell me what values to hold — help me see the logical structure of
   the value disagreements more clearly.
```

**Your exact prompt:**

> **[X POINTS]** *PASTE YOUR EXACT PROMPT HERE.*

**Representative LLM response excerpt:**

> **[X POINTS]** *PASTE A REPRESENTATIVE EXCERPT OF THE MODEL OUTPUT HERE.*

**Your revised Step 6 answer:**

> **[X POINTS]** *YOUR ANSWER HERE — write your revised non-empirical premise analysis.*

**What changed and why:**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences.*

---

## Part 3 – Final Answers After Group Discussion (in class, Monday)

After Monday's group discussion, write your final answer to each step below. This is your own considered view after hearing your group's analyses and working through any disagreements. It may align with group consensus, or it may diverge — both are fine. If your final answer on any step differs from your group's majority position, you are welcome (but not required) to note that briefly.

### Step 1 Final Answer: Identify the Argument

> **[X POINTS]** *YOUR FINAL ANSWER HERE.*

---

### Step 2 Final Answer: Evaluate Validity and Soundness

> **[X POINTS]** *YOUR FINAL ANSWER HERE.*

---

### Step 3 Final Answer: Classify the Premises

> **[X POINTS]** *YOUR FINAL ANSWER HERE.*

---

### Step 4 Final Answer: Evaluate the Existing Evidence

> **[X POINTS]** *YOUR FINAL ANSWER HERE.*

---

### Step 5 Final Answer: Specify the Missing Data

> **[X POINTS]** *YOUR FINAL ANSWER HERE.*

---

### Step 6 Final Answer: Address Non-Empirical Premises

> **[X POINTS]** *YOUR FINAL ANSWER HERE.*

---

## Part 4 – Reflection on Position Change (~20–30 min)

*Complete this section after Monday's group discussion, before Wednesday.*

Look back at your initial reaction in Part 0B. Answer the questions below based on everything you have done — the independent analysis, the LLM-assisted revision, and the group discussion.

**How has your initial reaction to the argument changed?**

Write 3–5 sentences. Do you now find the argument more or less persuasive than you did at first? What was most responsible for any change — or, if your view held steady, what reinforced it?

> **[X POINTS]** *YOUR ANSWER HERE — 3–5 sentences.*

**Which of the six steps was most influential in shaping your final view, and why?**

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 sentences.*

**What are you now more uncertain about than when you started?**

> **[X POINTS]** *YOUR ANSWER HERE — 2–3 sentences. Name something specific — a premise you thought was clear that turned out to be contested, or evidence you thought existed that turned out to be weak.*

**What is one question you would want answered before you felt confident in your overall assessment of this argument?**

> **[X POINTS]** *YOUR ANSWER HERE — 1–3 sentences.*

---

## Presentation Prep (~10 min)

On Wednesday, your group will present a 5-minute summary to the class. Each group member presents one of the six steps.

**Which step are you presenting?**

> **[X POINTS]** *YOUR ANSWER HERE — state the step number and name (e.g., "Step 4: Evaluate the Existing Evidence").*

**Your presentation notes (2–4 bullet points):**

What will you highlight? Aim for substance, not summary. Good presentation notes address questions like: What did your group find most interesting or surprising about this step? Where did members disagree? What would you need to know to feel more confident in your group's answer?

> **[X POINTS]** *YOUR ANSWER HERE — 2–4 bullet points.*

---

## What to Turn In

Submit your completed version of this `.md` file to Canvas. Before submitting, confirm:

- [ ] Part 0A: Your topic and chosen argument are identified; the full argument text is pasted in.
- [ ] Part 0B: Your initial reaction is written (before any analysis).
- [ ] Part 0C: LLM disclosure is complete.
- [ ] Part 1: All six steps are answered in your own words, without LLM use.
- [ ] Part 2: All six steps include an exact prompt, a response excerpt, a revised answer, and a "what changed" explanation.
- [ ] Part 3: All six final answers are written after group discussion.
- [ ] Part 4: All four reflection questions are answered.
- [ ] Presentation Prep: Your step and notes are filled in.
- [ ] All "YOUR ANSWER HERE" placeholders have been replaced.
