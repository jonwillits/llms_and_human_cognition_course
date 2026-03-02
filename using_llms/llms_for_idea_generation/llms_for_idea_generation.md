# LLMs for Idea Generation

## Background Info
This assignment is designed to help you experience how hard creative idea generation can be, 
and how that process changes when you use LLMs in different ways. 
You will compare human-only ideation, one-shot LLM ideation, and interactive human+LLM ideation 
to evaluate tradeoffs in effort, quality, and fixation.

One key comparison is your perception of novelty across conditions, especially human-generated versus AI-generated ideas. 
The goal is to test whether LLMs actually expand your idea space or mainly produce fluent versions of familiar ideas.

### Quick Specs
- Target time: ~5-6 hours
- Model requirements: At least one LLM chat interface (you may use more than one model, but one is sufficient)
- Grading basis: Effort in demonstrating a process, reproducibility, comparison, and reflection
- Submission format: One document (`.pdf`, `.docx`, or `.md`) with required tables, prompt logs, and reflection

### Key Terms (Read Before Starting)
- **Idea**: A distinct, concrete proposal. It must be specific enough that another student could understand and evaluate it.
- **Idea cluster**: A group of ideas that share the same underlying concept.
- **Novelty**: How different an idea is from common or obvious solutions.
- **Fixation**: Getting anchored on early ideas and repeatedly producing close variants.
- **One-shot prompt**: A single prompt that asks the model to do the task in one response, with no follow-up turns.
- **Interactive prompting**: Multi-turn back-and-forth where you iteratively refine goals, constraints, and outputs.
- **Constraint stress test**: Re-evaluating ideas after adding new constraints to see which ideas survive and adapt.

### Topic Options (Pick One)
Choose one of the following as the general topics for which you will generate an idea for the full assignment.

1. **Campus Life Improvements**.
   Starter examples (pick one if helpful):
   - Improve how students find quiet study spaces during peak hours.
   - Improve navigation of campus academic support services.
   - Improve access to healthy, low-cost food options in high-traffic areas.
   Example constraints you can use:
   - Must be feasible within one semester.
   - Must be piloted in one building or one student population first.
   - Must not require construction of new physical spaces.

2. **Social Connection and Community Building**
   Starter examples (pick one if helpful):
   - Help first-year or transfer students build 1-2 meaningful connections early.
   - Increase recurring participation in small campus communities.
   - Improve inclusion for commuters or students with limited free time.
   Example constraints you can use:
   - Must be inclusive for students with jobs or caregiving responsibilities.
   - Must work with both in-person and low-effort online participation.
   - Must be implementable by a student org or one course team.

3. **Plan/Design (but not Program) a Phone App to Help With a Real Student Need**
   Starter examples (pick one if helpful):
   - An app concept for planning weekly study blocks and accountability check-ins.
   - An app concept for reducing procrastination and phone distraction at night.
   - An app concept for helping students coordinate peer study sessions.
   Example constraints you can use:
   - You are designing the app concept only (no coding/building).
   - Must include at least one non-notification feature.
   - Must be usable in under 5 minutes per day.

4. **Persuasion Ideas: Convince a Target Person/Group of or to do X**
   Suggested `X` options (pick one unless you propose your own):
   - Adopt one better weekly study habit
   - Attend office hours at least once this month
   - Reduce pre-sleep doomscrolling
   - Join one campus event per week
   - Use LLMs for learning support rather than direct answer substitution
   Example constraints you can use:
   - Persuasion must be ethical and non-manipulative.
   - You must define a specific audience and communication channel.
   - You must include one likely objection and how your approach addresses it.

5. **Pick Your Own Topic**

If you choose option 5, define:
- target audience
- concrete goal
- at least 3 constraints

## Part 0 - Setup + Disclosure (20-30 min)
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

### Reproducibility Rules
1. Save all prompts and representative sample of outputs for Parts 2 and 3.
2. Use a **fresh chat thread** for:
   - Part 2A (vague one-shot)
   - Part 2B (improved one-shot)
   - Part 3 (interactive condition)
3. Record your exact prompt text and any model settings.

## Part 1 - Human-Only Idea Generation (70-85 min)
Goal: Experience effortful idea generation without LLM assistance.

### Step 1: Build a Topic Card (required)
Write:
- Audience:
- Problem:
- Desired outcome:
- 3 hard constraints:
- 1 success metric:

### Step 2: Generate 10 human-only ideas
- Produce exactly **10 ideas**.
- Minimum: 1-2 sentences per idea.
- No LLM use in this part.
- You may discuss with your group for feedback, but do not use/share LLM outputs.

What counts as an idea in this assignment:
- An idea should be a specific, actionable proposal, not just a broad goal.
- It should clearly imply who it is for, what happens, and how it would help.
- Example (Campus Life Improvements): "Create a live 'quiet-seat map' using student check-ins so students can quickly find open study spots in the library during peak hours."
- Example (Persuasion Ideas): "Run a 2-week peer challenge in one dorm where students commit to one office-hours visit, with reminder cards and a short testimonial wall from students who found office hours useful."

### If You Get Stuck
Use one forced variation move every 3-5 minutes:
- change target user
- change delivery channel
- change time horizon
- change budget/resource level
- change individual vs group format

### Part 1 table (required)
For each of 10 ideas, include:
- idea ID
- short label
- 1-sentence description
- predicted novelty (1-5)
- predicted feasibility (1-5)

Predicted novelty guidance:
- This is your **before-testing estimate** of how original an idea is relative to common/obvious ideas in that topic.
- Why this matters: later you can compare your predictions to what happens in Parts 2 and 3, and see whether LLM use increased diversity or pushed you toward familiar clusters.
- Suggested scale:
  - 1 = very common, obvious, or cliche
  - 2 = somewhat common with minor variation
  - 3 = moderately different from standard ideas
  - 4 = clearly unconventional but still plausible
  - 5 = highly unusual/original for this topic (not just a reworded common idea)

## Part 2 - One-Shot LLM Comparison (90-105 min)
Goal: Compare a weak one-shot prompt versus a scaffolded one-shot prompt.

You will run two one-shot conditions. Each must return **20 ideas**.

## Part 2A: Vague One-Shot (fresh thread)
Use a minimal/underspecified prompt.

Example vague prompt:
> Give me 20 ideas about [your topic].

Do not add constraints or follow-up turns.

## Part 2B: Scaffolded One-Shot (fresh thread)
Use this template and fill it in:

```text
Generate exactly 20 distinct ideas for this goal:
[goal]

Audience:
[audience]

Constraints:
1) [constraint]
2) [constraint]
3) [constraint]

Success metric:
[metric]

Output requirements:
- One sentence per idea
- Each idea must be meaningfully different from the others
- Avoid generic/cliche suggestions
- Include at least 5 higher-risk or unconventional ideas
- Label each idea with a short title
```

No follow-up turns in Part 2B either.

### Part 2 analysis
Create a comparison table for Part 2A vs Part 2B:
- overlap count (how many ideas are near-duplicates)
- number of distinct idea clusters
- your top 5 ideas from each run
- novelty rating average (1-5)
- feasibility rating average (1-5)
- one paragraph: what changed and why

## Part 3 - Interactive Human+LLM Remix (120-145 min)
Goal: Use iterative collaboration to improve diversity and quality.

You will now co-create ideas with the model using back-and-forth.

### Step 1: Create a brief document first
Before prompting, write a short "Creative Brief":
- goal
- audience
- constraints
- taboo tropes to avoid (at least 5)
  - Meaning: common, predictable idea patterns you do **not** want repeated.
  - Example (Campus Life topic): "Do not suggest 'make a campus app,' 'send more reminder emails,' or 'just add more events' unless the idea includes a clearly novel mechanism."
- what "high novelty" means for this topic

### Step 2: Multi-turn protocol (same thread, at least 6 turns)
Required sequence. Do each one of these steps as separate prompts, as part of a "conversation":
1. Ask for 20 candidate ideas based on your brief.
2. Ask the model to cluster them and identify overlap/redundancy.
3. Ask for 10 new ideas that are maximally different from the largest cluster.
4. Ask for 5 hybrid ideas that recombine your favorite concepts.
5. Ask the model to critique weak points in the top ideas.
6. Ask for revised versions of your top 5 ideas after critique.

You may add extra turns after these 6 required turns.

### Step 3: Constraint Stress Test
Add **2 new constraints** and rerun refinement on your top 5 ideas.

Choose two:
- budget reduced by 50%
- must be launchable in 2 weeks
- must support commuter students
- must avoid collecting personal data
- must work without a mobile app
- must be inclusive for students with limited free time

### Step 4: Final shortlist
Select final **5 ideas** and justify each in 2-3 sentences.

### Part 3 analysis
Report:
- how many ideas were discarded due to overlap/fixation
- which prompt moves produced the largest novelty jump
- whether stress-test constraints improved or weakened quality
- confidence (1-5) that your final 5 are better than Part 1 and Part 2 outputs

## Part 4 - Reflection (45-60 min)
Answer all prompts:

1. Where did you feel the strongest fixation, and in which part?
2. Compare the three modes:
   - human-only
   - one-shot LLM
   - interactive human+LLM
3. Which mode felt easiest? Which produced your best ideas?
4. Did the model mostly expand your idea space or standardize it?
5. What did you learn about writing better prompts for creative work?
6. If you repeated this assignment, what would you change first?

## Discussion Prep (for class group sharing)
Prepare a 2-minute summary:
- your topic
- one surprise from Part 2A vs 2B
- one insight from Part 3 stress test
- your single best final idea and why

## What to Turn In
Submit one document containing all items below:

1. Part 0 Setup + Disclosure section.
2. Topic Card and topic choice.
3. Part 1 human-only list of 10 ideas with required ratings.
4. Part 2A vague one-shot prompt + full output (10 ideas).
5. Part 2B scaffolded one-shot prompt + full output (10 ideas).
6. Part 2 comparison table and analysis paragraph.
7. Part 3 Creative Brief.
8. Part 3 prompt/output log for all required turns.
9. Part 3 stress test details and final 5 ideas with justification.
10. Part 4 reflection responses.
11. Discussion prep summary (bullet points are fine).
