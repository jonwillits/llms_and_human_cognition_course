# Verification & Calibration Lab  
**Target time:** ~5-6 hours 
**Models required:** Any LLM of your choice (Gemini, Claude, Copilot, Perplexity, etc.)  
**Web browsing:** strongly encouraged (and treated as something you also evaluate)  
**Grading:** effort- and process-based  
**Submission:** one document (4–7 pages) *or* the completed templates below. PDF, Word (.docx), or Markdown (.md) is fine.

---

## Part 0 — Setup + disclosure (15 min)

Include, at the top of your submission:

1) **Models/interface used:**  
- Model:
- Version (e.g. free vs. paid, thinking vs. fast, etc):
- Date/time window (approximate is fine):

2) **Disclosure statement (3–6 sentences):**  
Describe how you used LLMs while completing this lab.  
- What did you ask the models to do?  
- What did you copy vs. adapt vs. write yourself?  
- Did you use any model to help with verification or source-finding?

3) **A note on web verification (1–3 sentences):**  
State one risk of “web verification” (e.g., circular sourcing, outdated pages, SEO spam, copied claims) and how you tried to mitigate it.
---

## Part 1 — Verification across task types, and the timing of justification (core; ~4 hours)

### Goal
You will test how LLM **accuracy** and **confidence/calibration** vary across different task types, and (most importantly) how the **timing of justification** changes:
- the answer itself
- the model's confidence in its answer
- the quality/nature of the model’s “reasons,” and
- how easy it is for a human to verify the result.

You will complete **4 tasks total**, each in **3 prompt conditions**, for **12 total model outputs**.

---

## Part 1A — The four prompt conditions (you will use all three for every task)

For each task, you will run 4 prompts:

### v1 — Base prompt (no justification request)
You ask for the answer to your question.

### v2 — Post-hoc justification (second prompt)
You first run **v0**, then (in the same thread but in a second prompt) you send a standardized follow-up asking for justification.

### v3 — Justification built into the initial prompt
You start a new thread and ask for the answer **with justification requirements included up front, in the initial prompt**.

##### Suggested justification addition for v2 and v3
> Also include a justification using this format:  
> (1) Rationale (why this answer),  
> (2) Evidence/sources you rely on (or would rely on),  
> (3) 2–3 failure modes or ways you might be wrong (and what would change the answer),  
> (4) Confidence estimate and what would increase confidence.

If you have a particular way you want to alter the justification addition, please feel free to do so with a brief justification of your changes.

---

## Part 1B — Choose your four tasks (20 min)

You must do **all four** task categories below. You will run **v0, v1, and v2** for each task.

### Task 1: Your *expert-domain* “LLM blind spot”
Pick something you personally know well *and* that is plausibly outside typical LLM strength because it’s niche, rapidly changing, community-specific, poorly documented, or requires hands-on experience.

**You do NOT need to reveal private info.** If your topic is sensitive or involves personal/work details, anonymize it and describe it at a high level.

**Examples (choose your own; do not copy these as-is):**  
- A niche game meta/build *for a specific patch version*  
- A small fandom/canon detail not widely documented  
- A specialized workflow/tool used in a lab or hobby community  
- A very local policy/practice in an organization (describe at a high level)  
- An obscure product line/version history in fashion/audio/mechanical keyboards/etc.

#### Expert-task viability checklist (complete before committing)
Answer these briefly (1–2 sentences each):
1. What makes you an “expert” here (experience, time invested, direct knowledge)?  
2. Why is this plausibly hard for an LLM (niche, low coverage, fast-changing, etc.)?  
3. What would count as “correct” vs. “wrong” in this domain?  
4. What is at least one *primary-ish artifact* you could use to verify (official patch notes, a manual, a dataset, a screenshot, a changelog, etc.)? If none exist, say so.

---

### Task 2: Concrete factual claim (web-verifiable)
Choose one prompt that elicits multiple checkable facts (dates, names, definitions, “who did what when,” etc.).
For example, you could pick one of these:
- 2A. A definition + provenance (who coined it / earliest use / canonical source)  
- 2B. A “current policy/requirement” claim (must be something publicly documented)  
- 2C. A historical/timeline claim with at least 3 distinct facts  

**Avoid:** easy trivia (you want something that can be subtly wrong).

---

### Task 3: Quantitative / statistical reasoning
Choose one prompt that forces explicit calculation or interpretation.

Pick one:
- 3A. Recompute a statistic from provided numbers (you provide the numbers)  
- 3B. Interpret a CI/p-value/Bayes factor from a scientific journal article of your choice  
- 3C. Solve a mathematical word problem that you invent, like one you might have had in school. *DO NOT* just copy one verbatim from the internet!
---

### Task 4 (required): Explanation / causal / synthesis
Choose one prompt where correctness is not just “a fact,” but depends on mechanism, interpretation, or summarizing viewpoints.

Pick one:
- 4A. Causal explanation: “Why/how does X lead to Y?”  
- 4B. Synthesis: “What do researchers argue about X?”  
- 4C. Compare theories: “Compare A vs B and what evidence would discriminate them”  

---

## Part 1C — Rules (read carefully)

1) **You will generate 12 model outputs total.**  
4 tasks × (v1, v2, v3) = 12 outputs.

2) **Start fresh threads/chat when required.**  
- v1 and v2 happen in the same thread.  
- v3 must be a new thread (fresh context).

3) **Keep the task prompt itself consistent across conditions.**  
For v3, the only change should be adding the required justification instruction. The substantive task must remain the same.

4) **Do not “repair” prompts mid-task.**  
If the model asks clarifying questions, answer them—but don’t rewrite the task prompt to make it easier. We want to see failure modes.

5) **Verification is required.**  
Do your best to verify the model's output for each prompt. 
Web browsing is encouraged, but you must evaluate the *web information itself* (not all sources are equal; multiple sources may not be independent).

---

## Part 1D — Documentation + verification workflow (do this for each task)

To keep the workload reasonable, you will write **one Full Verification Log per task** (4 total).  
Each log will compare **v1 vs v2 vs v3** for that task.

You will still paste all **three outputs** (v0, v1, v2) into the log.

---

### Full Verification Log Template (copy 4 times: one per task)

#### 1) Task overview
- Task number: (1 / 2 / 3 / 4)  
- Task type: (expert blind spot / factual / quantitative / causal-synthesis)  
- Your prompt (paste exact v0 prompt):  

#### 2) The three outputs (paste)
**v1 output (base):**  
(paste)

**v2 output (post-hoc justification):**  
(paste the justification response you got after the v1 follow-up prompt)

**v3 output (justification in initial prompt):**  
(paste)

#### 3) Pre-verification self-assessment
- My background knowledge for this task (0–3):  
  - 0 = none  
  - 1 = basic familiarity  
  - 2 = moderate knowledge  
  - 3 = strong knowledge / expert  
- If I stopped at **v1**, how much would I trust it? (1–7):  
- Did **v2** or **v3** change my trust *before* checking anything? Why? (2–4 bullets)

#### 4) Claim extraction
A “claim” is any **checkable commitment** the outputs make (facts, numbers, causal links, recommendations, “consensus” statements, or implied assumptions).

First, extract **3–8 atomic, load-bearing claims** from the three outputs combined.  
For each claim, label the claim type and note which condition(s) assert it.

Template:
- Claim 1: … (factual / quantitative / causal / recommendation / citation) — appears in: v1 / v2 / v3  
- Claim 2: … — appears in: v1 / v2 / v3  
- Claim 3: … — appears in: v1 / v2 / v3  
(etc.)

#### 5) Verification plan (choose at least 3 moves)
Pick **at least 3** verification moves below and justify briefly why they fit this task:

Verification moves (choose 3+):
- Triangulate across independent sources  
- Trace to a primary source (official doc, paper, dataset, manual, patch notes, etc.)  
- Recompute / re-derive (math, logic, statistics)  
- Counterexample / boundary-case probing  
- Internal consistency checks (contradictions, constraint violations)  
- Evidence audit (are citations real? are quoted facts supported?)  
- Alternative formulation (ask the same thing differently, or ask for failure cases)

Your chosen moves + justification:
- Move 1: …  
- Move 2: …  
- Move 3: …  
(Optional Move 4: …)

#### 6) Evidence record (what you actually did)
For each key check, record:
- What you checked  
- What you found  
- Whether it supports/refutes the relevant claim(s)

If you used web sources, include a mini “source audit” for key sources:
- Source name + author/organization:  
- Type: primary / secondary / tertiary  
- Date/version (if relevant):  
- Independence: is it copying another source? unclear?  
- Why you trust it (or why not):

#### 7) Results: accuracy + calibration (by condition)
Fill out for each condition:

**v1**
- Accuracy: correct / partially correct / incorrect / cannot verify  
- Calibration: overconfident / underconfident / appropriately calibrated  
- One “novice trap”: what might sound right to a non-expert but is wrong/misleading?

**v2**
- Accuracy: correct / partially correct / incorrect / cannot verify  
- Calibration: overconfident / underconfident / appropriately calibrated  
- One “novice trap”:

**v3**
- Accuracy: correct / partially correct / incorrect / cannot verify  
- Calibration: overconfident / underconfident / appropriately calibrated  
- One “novice trap”:

#### 8) Justification comparison (the manipulation)
Compare v2 vs v3 in 6–12 sentences total:
- Are the justifications substantively different, or mostly “story-like” after the fact?  
- Did either justification introduce **new claims** not present in v1? If so, were they verifiable?  
- Did justification make errors easier to catch—or harder (more persuasive)?  
- Did either condition better acknowledge uncertainty in a useful way?

#### 9) Safer rewrite (what you would actually tell a user)
Write a final evaluation, incorporating what you verified:
- separate verified vs uncertain points  
- include what evidence would settle remaining uncertainties  
- keep it useful (not just “I’m not sure”)


## Part 2 — Cross-task synthesis: verification strategies, calibration, and “web verification” ( ~60-90 min )

### Goal
Step back from individual tasks and look for patterns across the **four tasks** and the **three prompt conditions (v1/v2/v3)**. 
Your job is to extract general lessons about:
- which task types are easiest/hardest to verify,
- when “justification” helps vs. hurts,
- how your own expertise changes what you can detect,
- and how web browsing can both **improve** and **mislead** verification.

### What to do
Write a synthesis (recommended **~1000 words**) answering the questions below. You may use headings and bullet points.

#### 2A) Verification strategy by task type
For each task type (expert blind spot, factual, quantitative, causal/synthesis):
- What verification moves were most effective? Why?
- What verification moves were *tempting but weak* (e.g., “found a blog that repeats the claim”)?
- What would a **minimum viable verification protocol** look like for a non-expert with limited time?  
  (Write 4–6 bullets per task type.)

#### 2B) The justification manipulation: what changed and why?
Across tasks, compare v2 vs v3:
- Did justification change the **final answer** more in some task types than others?
- Did justification add **new claims**? Were they usually verifiable?
- Did justification make mistakes easier to catch—or harder (more persuasive)?
- Did the model’s confidence language track real difficulty?

Be explicit about at least **one** case where justification was helpful and **one** case where it was harmful or misleading.

#### 2C) Expertise as a confound
Reflect on your expert-domain task vs the others:
- What did you detect quickly because you had “taste”/intuition in the domain?
- What might a novice miss even after trying to verify via web browsing?
- If you had *not* been an expert, what verification strategy would you have tried—and would it have worked?

#### 2D) Web verification: when “checking sources” fails
Describe at least **one** situation in your work where web browsing:
- increased confidence *without actually increasing truth* (circular sourcing, outdated pages, SEO spam, vague summaries), **or**
- presented conflicting claims that required you to trace to a primary source.

In 4–8 sentences, state your rule-of-thumb for evaluating:
- source quality,
- source independence,
- and version/date relevance.

#### 2E) Takeaways
Give **5 takeaways** total, each in 1–2 sentences:
- 2 takeaways about verification as a process
- 2 takeaways about justification (v2 vs v3)
- 1 takeaway about your own expertise and how it shaped your trust


---

## What to turn in

For Part 1:
1) Your completed **Task selection** (4 tasks) with short descriptions  
2) **4 Full Verification Logs** (each containing v1, v2, v3 outputs + verification + comparison)  
3) Any appendices you need (full outputs, screenshots, calculation work, etc.)

For Part 2:
- Your synthesis as described above
