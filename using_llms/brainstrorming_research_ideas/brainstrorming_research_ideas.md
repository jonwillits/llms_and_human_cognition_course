# Brainstorming Research Ideas: From Curiosity to Testable Questions

## Background Info
### Purpose of this Assignment
In this assignment, you will start with a broad research curiosity and develop it into concrete, testable research questions. The main learning goal is to evaluate how different workflows (human-only, LLM-only one-shot, and interactive human+LLM scaffolding) change the quality of research-question development. Your primary comparisons are: novelty vs feasibility tradeoffs, theory-anchored vs no-theory prompting, and method-free vs method-locked question design.

### Quick Specs
- Target time: ~5-6 hours
- Model requirements: At least one LLM chat interface (you may use more than one model, but one is enough)
- Grading basis: Process quality, reproducibility, clear condition comparisons, and reflection
- Submission format: One document (`.pdf`, `.docx`, or `.md`) with required tables, prompt logs, and reflection

### Key Terms
- **Research curiosity**: A broad topic-level question you genuinely want to understand (for example, "How does phone use affect attention in class?").
- **Research question**: A specific question that narrows the curiosity into a concrete claim space.
- **Testable research question**: A question specific enough that a study could be designed to answer it using measurable variables.
- **Theory-anchored prompting**: Prompting that explicitly asks the model to generate ideas from a named theoretical perspective.
- **No-theory prompting**: Prompting without an explicit theory frame.
- **Method-free question**: A question that does not commit to a specific method.
- **Method-locked question**: A question explicitly tied to one method (for example, experiment, survey, text analysis, or secondary-data analysis).
- **One-shot prompt**: A single prompt with no follow-up turns.
- **Interactive scaffolding**: Multi-turn back-and-forth where you iteratively refine ideas.

### Required Rating Scales
Use these anchors in all rating tables.

**Novelty (1-5)**
- 1 = very common, obvious, or cliche
- 2 = somewhat common with minor variation
- 3 = moderately distinct from standard ideas
- 4 = clearly unconventional but plausible
- 5 = highly original for this topic

**Feasibility (1-5)**
- 1 = not realistically testable in a normal student-scale project
- 2 = testable only with major constraints, resources, or access
- 3 = testable with moderate scope control
- 4 = readily testable with available methods/resources
- 5 = straightforward to test with clear measures and manageable scope

### Optional Curiosity Starter Areas (Pick One if Helpful)
1. **Learning and memory in student life**
Starter examples:
- Does multitasking while studying reduce long-term retention?
- Do AI study tools improve transfer to new problems?
Optional constraints:
- Focus on undergraduates.
- Keep data collection under 4 weeks.

2. **Cognition and digital environments**
Starter examples:
- How do notification interruptions affect reading comprehension?
- Does phone proximity change sustained attention?
- How does digital vs. analog (i.e. paper-based) note-taking affect learning and memory?
Optional constraints:
- Use a non-clinical sample.
- Avoid invasive data collection.

3. **Social Media, Personality, and Psychological Well-Being**
Starter examples:
- How is short-form social media use related to daily anxiety, mood, or self-esteem in college students?
- Do personality traits (for example, neuroticism or extraversion) moderate how social media use affects well-being?
Optional constraints:
- Include at least one validated well-being measure.
- Define one personality dimension and one social media behavior measure.

4. **Decision-making and judgment**
Starter examples:
- Does AI advice change confidence calibration?
- Do people overweight fluent AI explanations?
Optional constraints:
- Include uncertainty/confidence ratings.
- Include at least one objective correctness measure.

5. **Pick your own curiosity**
If you choose this, define:
- target population
- key construct(s)
- at least 3 scope constraints

## Part 0 - Setup + Disclosure (20-25 min)
Complete this at the top of your submission.

- Model(s)/interface(s) used
- Model version/tier/settings (free/paid, fast/reasoning, temperature if available)
- Date/time window of work
- Tools/features used (browsing, file upload, memory, etc.)
- Disclosure statement:
  - what you asked the model to do
  - what text/ideas were copied directly
  - what was adapted
  - what was fully your own

### Reproducibility Rules (Required)
1. Save exact prompt text and representative output excerpts for all LLM conditions.
2. Use a **fresh chat thread** for each one-shot run in Part 2.
3. In one-shot runs, do **not** use follow-up prompts.
4. Record model settings and any notable defaults.

## Part 1 - Human-Only Research Question Development (65-80 min)
Goal: Build a human-only baseline from broad curiosity to concrete testable questions.

### Step 1: General Idea Description
Write:
- broad curiosity: describe a general topic that you are interested, at the level of detail of the examples above
- why this matters (2-3 sentences):
- target population:
- 3 scope constraints (such as the kinds of things listed as constraints above):
- one practical limitation (time, data access, measurement, or ethics):

### Step 2: Generate 15 method-free candidate questions (required)
- Produce exactly **10** distinct research questions. Take your general idea and turn it into smaller, more tractable questions. No bad ideas in a brainstorm!
- No LLM use in this step.
- 1 sentence per question.

What counts as a good candidate question:
- Specific enough to compare alternatives.
- Not yet necessarily tied to a specific method.
- Clearly connected to your general idea.

Example conversion:
- Too broad: "Does social media affect mental health?"
- Better method-free question: "How does daily short-form social media exposure relate to end-of-day stress among undergraduates?"

### Step 3: Rate all 15 questions
Create a table with:
- question ID
- question text
- novelty (1-5)
- feasibility (1-5)
- 1-sentence rationale for each rating

### Step 4: Make 4 questions testable
Select your top 4 and rewrite each as a testable version by specifying:
- measurable predictor(s)
- measurable outcome(s)
- target population/sample
- predicted direction or relationship

### If You Get Stuck
Use this fallback sequence:
1. Narrow population.
2. Narrow time window.
3. Replace abstract constructs with observable behaviors.
4. Add one concrete "because" mechanism.
5. Ask: "What would count as evidence against this?"

## Part 2 - LLM-Only One-Shot Comparisons (90-100 min)
Goal: Compare simple vs scaffolded one-shot prompting while testing theory/no-theory and method-free/method-locked conditions.

## Part 2A - Simple One-Shot Baseline (fresh thread)
Use one minimal prompt with no follow-up.

Example:
```text
Generate 20 research questions about this curiosity:
[insert your general question summary]
```
Requirements:
- exactly **20** questions
- no follow-up turns or questions

## Part 2B - Scaffolded One-Shot Matrix (fresh thread per condition)
Now we are going to run four more one-shot conditions that provide the LLM a little more scaffolding and constraint. No follow-up turns.
In these follow ups we are going to constrain the LLM in terms of theories they are using to make predictions and methods they can use.

### Choose one theory anchor
Pick one theory relevant to your topic (for example, predictive processing, working memory limits, dual-process theory, self-determination theory, signal detection theory). Briefly define it in 1-2 sentences.
If this is a domain about which you lack knowledge, have a conversation first with your LLM about what are some major theories used to explain behavior in this domain.
Use what you learn to pick a theory you want to explore more.

### Choose one method for method-locked conditions
Pick one:
1. **Behavioral experiment**
Scaffold: define manipulated variable(s), outcome variable(s), and comparison condition.
2. **Survey/correlational study**
Scaffold: define key measures and expected association.
3. **Text analysis/annotation study**
Scaffold: define corpus, coding dimensions, and expected pattern.
4. **Secondary-data analysis**
Scaffold: define dataset type, key variables, and expected relationship.

### Run these 4 one-shot conditions (exactly 8 questions each)
1. No-theory + method-free
2. Theory-anchored + method-free
3. No-theory + method-locked
4. Theory-anchored + method-locked

Use this template for each run:
```text
Generate exactly 10 distinct research questions.

Topic curiosity:
[insert]

Condition:
- Theory mode: [no-theory OR theory-anchored using: <theory name>]
- Method mode: [method-free OR method-locked using: <method name>]

Output constraints:
- One sentence per question
- Avoid near-duplicates
- Keep questions specific and testable
- Include at least 2 high-novelty options
```

### Part 2 analysis table
Compare Part 2A and all four Part 2B runs using:
- overlap count (near-duplicates)
- average novelty (1-5)
- average feasibility (1-5)
- count of clearly testable questions
- top 2 questions per condition
- short note on style/failure patterns

Then write one synthesis paragraph:
- What changed from simple to scaffolded one-shot?
- What changed under theory anchoring?
- What changed under method locking?

## Part 3 - Interactive Human+LLM Scaffolding (90-105 min)
Goal: Use iterative collaboration to develop your strongest ideas into concrete, defensible, testable questions.

Use one thread for this part. Minimum **8 turns**.

### Step 1: Seed selection
Choose 6 candidate questions total:
- 2 from Part 1
- 2 from Part 2A
- 2 from Part 2B (from different Part 2B conditions)

### Step 2: Required 8-turn scaffold
Complete these in order:
1. Ask the LLM to cluster the 6 seed questions by underlying mechanism.
2. Ask for 6 new variants that are maximally different from the largest cluster.
3. Ask for a theory-linked explanation of why the top 4 might work.
4. Ask for method-free rewrites of those 4 with sharper constructs.
5. Ask for method-locked versions of those 4 (using your chosen method).
6. Ask the LLM to identify confounds, missing controls, and feasibility risks.
7. Ask for revised versions that directly fix those issues.
8. Ask the model to self-rate each revision on novelty and feasibility and explain uncertainty.

### Step 3: Final selection
Select final **3 testable research questions**.

For each final question, include:
- final question text
- theory link (or reason for no-theory choice)
- method lock (or reason to remain method-free)
- variables/measures
- one likely confound and mitigation plan
- novelty rating (1-5) and feasibility rating (1-5)

### Part 3 mini-comparison (required)
For each of your final 3, show:
- original seed question
- final revised question
- what changed and why (2-3 sentences)

## Part 4 - Reflection and Summary (35-45 min)
Answer all prompts:

1. Where did your biggest improvement occur: Part 1, Part 2, or Part 3? Why?
2. Compare simple one-shot vs scaffolded one-shot: what was the largest quality difference?
3. Did theory anchoring improve question quality, or just narrow idea diversity?
4. Did method locking improve feasibility at the cost of novelty (or not)?
5. Which final question best balances novelty and feasibility, and why?
6. What did this assignment change about how you will use LLMs for research ideation?

## Discussion Prep (for class sharing)
Prepare a 2-minute summary:
- your starting curiosity
- one major Part 2 contrast
- one key Part 3 revision move
- your best final testable question

## What to Turn In
Submit one document containing all items below:

1. Part 0 Setup + Disclosure section.
2. Part 1 Curiosity Card.
3. Part 1 list of 15 human-only questions with novelty/feasibility ratings.
4. Part 1 rewritten 4 testable questions.
5. Part 2A simple one-shot prompt and full output (15 questions).
6. Part 2B four one-shot prompts and outputs (8 questions each).
7. Part 2 comparison table and synthesis paragraph.
8. Part 3 interactive prompt/output log for at least 8 turns.
9. Part 3 final 3 testable questions with required fields.
10. Part 3 seed-to-final mini-comparison notes.
11. Part 4 reflection responses.
12. Discussion prep summary bullets.
