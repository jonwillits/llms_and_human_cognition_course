# LLM Debates Unit — Lecture Development Progress

**Last updated:** April 6, 2026
**Instructor:** Jon Willits
**Course:** PSYC 496 / PSYC 590

---

## What We Have Done

### Restructured the Debate Unit

The original syllabus had students rotating through individual debate topics each week in groups. This has been replaced with a thematic cluster structure over 5 weeks:

| Dates | Theme | Topics |
|-------|-------|--------|
| 4/8, 4/13, 4/15 | What Do LLMs Tell Us About the Nature of Intelligence? | 13, 14, 15, 16, 18, 19, 20 |
| 4/20, 4/22 | Impact of LLMs and AI on Human Cognition | 1, 3, 4, 5, 7 |
| 4/27, 4/29 | Ethical Issues Involving LLMs and AI | 2, 6, 8, 9, 10 |
| 5/4, 5/6 | Are LLMs Dangerous to Humanity? | 11, 12, 17 |

Each week: Instructor gives a brief intro, groups self-select a sub-topic (with option to switch groups), then perform an epistemic analysis. Wednesday: each group presents a 5-minute summary.

### Designed the Unit 3 Kickoff Lecture (April 6, 2026)

A 45–60 minute lecture introducing the debate unit and the epistemic analysis framework. Slides will be light on text with rich speaker notes.

#### Agreed Slide Outline (25 slides)

**Part 1: Transition & Orientation**
1. Title slide
2. The Course Arc — Units 1, 2, 3 in brief
3. How This Unit Is Different — discussion-based, attendance matters, group format
4. The Semester Plan — the 4 debate clusters with dates

**Part 2: How Class Works**
5. The Weekly Structure — individual pre-work before Monday, group discussion Monday, group presentations Wednesday
6. Choosing Your Sub-Topic — groups self-select, can switch
7. Starter Arguments — Jon provides a couple of arguments per topic; students may use their own

**Part 3: Why Epistemic Analysis?**
8. The Problem With Most AI Debates — polarized, tribal, hype vs. fear
9. A Better Goal — calibrated reasoning under uncertainty, not winning

**Part 4: The Framework — 6 Steps**
10. Overview — all 6 steps as a visual map (labels only, light)
11. Step 1 — Identify the Argument: write out premises and conclusion, diagram the structure
12. Step 2 — Validity vs. Soundness: definitions and a worked example
13. Step 2 — What Makes an Argument Invalid: the counterexample method
14. Step 2 — What Makes an Argument Invalid: truth table
15. Step 2 — Two Kinds of Fallacies: formal (invalidity) vs. informal (soundness problems); soundness is what we care about in this course
16. Step 2 — Formal Fallacy in LLM Debates: affirming the consequent with an LLM example
17. Step 2 — Informal Fallacies in LLM Debates: slippery slope, false dilemma, appeal to nature, begging the question — framed as premise/soundness problems
18. Step 3 — Classify the Premises: empirical vs. non-empirical, with example
19. Step 4 — Evaluate Empirical Support: what evidence exists, what would count as evidence
20. Step 5 — Specify Missing Data: what we'd need and how we'd get it
21. Step 6 — Addressing Non-Empirical Premises: acknowledge disagreement, check internal consistency, agree to disagree
22. Step 6 — When Moral Claims Hide Empirical Premises: e.g., "it would be immoral because it would cause suffering" — the suffering premise is empirical

**Part 5: What's Coming**
23. First Cluster Preview — intelligence/cognition topics, 4/8–4/15
24. What To Do Before Thursday
25. Questions / closing

#### Key Design Decisions

- **Slides:** Light on text. Speaker notes carry the depth. Students will have access to both.
- **Logic grounding:** Steps 1–2 anchor the framework in formal logic (validity, soundness, argument diagramming). Students are assumed to have some prior exposure; logic lectures 1–3 and readings (Logic CH1–3.pdf) are available as reference in `background_readings_and_lectures/`.
- **Fallacies:** Five highlighted — affirming the consequent (formal/invalidity), and slippery slope, false dilemma, appeal to nature, begging the question (informal/soundness). The distinction between formal and informal fallacies is explicitly taught.
- **Non-empirical premises (Step 6):** Treated as genuinely hard. Key insight: moral claims sometimes contain hidden empirical premises that can be extracted and evaluated.
- **Invalidity illustration:** Counterexample method first, then truth table for clarity.

---

## What Is Left To Do

### Immediate: Build the Lecture Slides
- Write full slide content and speaker notes for all 25 slides
- Generate `.pptx` file using PptxGenJS
- Visual QA (convert to images, inspect, fix)
- Save to `course_content/llm_debates/` (or a `lecture/` subfolder — TBD)

### Per-Week: Starter Arguments
For each of the 4 debate clusters, Jon will provide 2–3 "starter arguments" (written out in P1, P2, C form) that students can use as their starting point for epistemic analysis. These need to be drafted. Suggested location: a file within each cluster's folder or as a single document in `performing_epistemic_analyses/`.

### Ongoing: The `llm_debate_topics.md` File
The 6 epistemic analysis questions in that file (Map the Debate, State Your Position, etc.) were the original framework. The new framework taught in this lecture is more logic-grounded (argument structure → validity → classify premises → evaluate evidence → specify missing data → address non-empirical claims). These two documents should be reconciled — either updating `llm_debate_topics.md` to reflect the new framework, or noting the relationship explicitly.

### Future Lectures
Jon plans to open each debate week with a brief (~10 min) intro to the cluster topic. Those mini-lectures/talking points still need to be developed for each of the 4 clusters.
