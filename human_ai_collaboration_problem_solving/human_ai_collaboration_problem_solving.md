# Human-AI Collaboration in Problem Solving

## Background Info
This assignment is designed to help you test how problem solving changes across three modes: human-only, AI-only, and interactive human+AI collaboration. 
You will use the same problem context across all modes and compare quality, time, errors, and confidence.
At the end of the exercise, you will provide a final evaluation of the solutions you produced.

The core goal is to evaluate collaboration as a joint cognitive system: when dividing labor with an LLM helps, when it hurts, and why. 
A key comparison is whether the model works best as a planner, checker, explainer, or tool in your specific case.

### Quick Specs
- Target time: ~5-6 hours
- Model requirements: At least one LLM chat interface (you may use more than one model, but one is sufficient)
- Grading basis: Effort, process quality, reproducibility, condition comparison, and reflection
- Submission format: One document (`.pdf`, `.docx`, or `.md`) with required tables, prompt logs, and reflection

### Key Terms (Read Before Starting)
- **Problem-solving task**: A task with a goal, constraints, and a need to choose or design a solution path.
- **Well-defined problem**: Clear start state, goal state, and rules (for example, a formal puzzle).
- **Ill-defined problem**: Ambiguous goals/constraints with multiple plausible solutions (for example, relationship or ethical dilemmas).
- **Task decomposition**: Breaking a larger problem into smaller subproblems with ordered dependencies.
- **Role assignment**: Deliberately assigning the model a function (planner, checker, explainer, executor).
- **Overreliance**: Accepting model output too quickly without adequate verification.
- **Underuse**: Ignoring useful model help that could improve the result.
- **Division of labor**: Which cognitive steps are done by you versus the model.

### Scoring Dimensions (Use in Parts 1-3)
When you have completed each problem, you will rate each final solution 1-5 on:
- **Goal attainment**: How well the solution addresses the stated goal.
  - 1 = does not address the core goal
  - 3 = partially addresses goal with notable gaps
  - 5 = strongly addresses goal with clear linkage to the target outcome
- **Constraint satisfaction**: How well the solution respects stated constraints.
  - 1 = violates multiple hard constraints
  - 3 = satisfies most constraints with minor misses
  - 5 = satisfies all required constraints
- **Reasoning quality**: Clarity and coherence of explanation for why the solution should work.
  - 1 = mostly unsupported claims
  - 3 = mixed reasoning with some unsupported steps
  - 5 = clear chain of reasoning with explicit assumptions
- **Risk awareness**: Identification and handling of likely failure modes (predictable ways a plan could break down or fail).
  - 1 = risks ignored
  - 3 = obvious risks identified, weak mitigation
  - 5 = risks identified with concrete mitigation/fallbacks
- **Practicality**: Realistic feasibility for the chosen context.
  - 1 = not realistically actionable
  - 3 = partially actionable
  - 5 = immediately actionable with clear next steps

### Problem Context Options (Pick One)
Choose a problem that you are going to describe and then try to solve.
You must state a specific problem, and also a set of constraints on the solution to the problem.
Use the same problem context in Parts 1 (self-generated solution), 2 (LLM solo solution), and 3 (human-LLM collaboration).

1. **Personal Relationship Problem (Real or Hypothetical)**
   Starter examples (pick one if helpful, but feel free to choose your own):
   - Repeated conflict with roommate/teammate over expectations
   - Setting a boundary with a friend or family member
   - Repairing communication after a misunderstanding
   Example constraints you can use:
   - Must represent both perspectives fairly
   - Must include one concrete conversation plan/script
   - Must include at least one low-risk alternative if the first approach fails

2. **Planning/Organizational Problem (Real or Hypothetical)**
   Starter examples (pick one if helpful, but feel free to choose your own):
   - Weekly schedule redesign under time/energy constraints
   - Organizing a group project timeline with dependencies
   - Planning exam prep across multiple courses and deadlines
   Example constraints you can use:
   - Must include at least 3 fixed constraints (time, resources, deadlines)
   - Must include a contingency plan for one disruption
   - Must include a prioritization rule (what gets dropped first if needed)

3. **Ethical Decision Case (Personal or Interpersonal)**
   Starter examples (pick one if helpful, but feel free to choose your own):
   - Whether to disclose sensitive information to protect someone
   - Whether to confront/report a questionable behavior
   - Whether to prioritize loyalty to a person versus fairness to a group
   Example constraints you can use:
   - Must identify stakeholders and likely harms/benefits
   - Must compare at least 2 plausible actions
   - Must include uncertainty and a revision trigger (when to reconsider)

4. **Choose Your Own Problem Context**

If you choose option 4, define:
- target outcome
- at least 3 hard constraints
- at least 2 plausible solution paths

### If You Get Stuck
Use this fallback sequence:
1. Re-state the problem in one sentence.
2. List 3 constraints and 2 failure modes (predictable ways the plan could break down or fail).
3. Break into at least 4 subproblems.
4. Solve only subproblem 1 first, then continue.

## Part 0 - Setup + Disclosure (20-30 min)
Complete this at the top of your submission.

- Model(s)/interface(s) used
- Model version/tier/settings (free/paid, fast/reasoning, temperature if available)
- Date/time window of work
- Tools/features used (browsing, file upload, memory, etc.)
- Disclosure statement:
  - what you asked the model to do
  - what text/solutions were copied directly
  - what was adapted
  - what was fully your own

### Reproducibility Rules
1. Save all prompts and representative outputs for Parts 2 and 3.
2. Use a **fresh chat thread** for:
   - Part 2A (AI-only naive run)
   - Part 2B (AI-only structured run)
   - Part 3 (collaborative run)
3. Record exact prompt text and model settings.
4. In Part 2, do not paste your full Part 1 solution into the model.

## Part 1 - Human-Only Problem Solving (60-90 min)
Goal: Establish a human baseline for quality, speed, and confidence.

### Step 1: Build a Problem Brief (required)
Write:
- Context option chosen (1-4):
- Problem statement (2-4 sentences):
- Desired outcome:
- 3-5 hard constraints:
- Who is impacted:
- 1 success metric:

### Step 2: Task Decomposition (required)
Break the problem into at least **6 subproblems**.
For each subproblem, include:
- subproblem ID number (to keep track of when logging your results later)
- why the subproblem matters
- dependency (what prerequisites must occur before the subproblem can be solved)

### Step 3: Human-Only Solution Draft
Without LLM help, produce:
- an attempt at a complete solution or action plan
- rationale for major choices
- at least 2 anticipated failure modes (predictable ways your plan could break down or fail)
- fallback plan if the first attempt fails

### Step 4: Self-Evaluation Table (required)
Rate your Part 1 solution (1-5 on each scoring dimension described above):
- goal attainment
- constraint satisfaction
- reasoning quality
- risk awareness
- practicality
- confidence that your solution would work (1-5)

Record time spent in minutes.

## Part 2 - AI-Only Problem Solving (30-60 min)
Goal: Evaluate what the model does on its own with low versus high prompt structure.

Run two AI-only conditions. Both must be one-shot (no follow-up turns).

### Part 2A - Naive AI-Only Run (fresh thread)
Use a minimal prompt.

Example template:

```text
Solve this problem:
[problem brief]
```

Rules:
- One prompt, one response.
- No follow-up clarifications.

### Part 2B - Structured AI-Only Run (fresh thread)
Use this scaffolded one-shot template and fill it in:

```text
You are solving a problem in one response.

Problem:
[problem statement]

Desired outcome:
[outcome]

Constraints:
1) [constraint]
2) [constraint]
3) [constraint]

Required output sections:
1) Task decomposition (at least 6 subproblems with order)
2) Proposed solution plan
3) Risk analysis (at least 3 failure modes: predictable ways the plan could break down or fail)
4) Verification/check procedure
5) Fallback plan if main plan fails

Output requirements:
- Be concrete and specific
- Explicitly reference constraints
- Do not skip tradeoffs
```

Rules:
- One prompt, one response.
- No follow-up clarifications.

### Part 2 Analysis (required)
Create a Part 2 comparison table with:
- solution quality summary (2A vs 2B)
- missing constraints count
- major errors or weak assumptions
- scored ratings (1-5) for each scoring dimension
- confidence rating (1-5) for each run
- one paragraph: what changed between 2A and 2B, and why

## Part 3 - Interactive Human+AI Collaboration (120 min)
Goal: Test collaboration dynamics, role assignment, trust calibration, and division of labor.

### Step 1: Collaboration Setup
This step is where you will collaborate with the LLM on a solution.
The first step is to outline a collaboration procedure before content generation starts.
Start a fresh thread and paste your full problem prompt, as you did in Part 2B.
Then establish an interaction procedure where the LLM occupies a set of distinct roles.
You will explicitly tell the model that it must use only the role you request each turn.

Required role sequence:
1. Model as **Planner**: propose decomposition and first-pass plan.
2. Model as **Checker**: critique the plan against constraints.
3. Model as **Explainer**: explain tradeoffs and alternatives.
4. Model as **Executor**: draft a concrete final action sequence.

Use something like the following as your first message template:

```text
We are solving a problem collaboratively.
Use the problem description below and follow my role instructions exactly.

[Paste your full problem description]

Collaboration rules:
- Only perform the role I name in each turn.
- Start each response with: Role used: [role]
- Keep recommendations concrete and tied to the listed constraints.
- If a constraint is not satisfied, flag it explicitly.
- Do not finalize the plan until I request Executor mode.

Role sequence for this thread:
1) Planner
2) Checker
3) Explainer
4) Executor

Following each response you give following a certain role, I may ask follow up questions.
Unless otherwise specified, assuming you are still following the previously stated role, 
and continue to respond using that role and role response format, until I explicitly tell you we have moved on to the next role.

For now:
- Confirm you understand the role sequence and collaboration rules.
- Wait for my Role 1 (Planner) prompt before generating content.
```

Mini example (planning/organizational case):
- Problem brief includes: "I need a 2-week study plan across 3 courses, with work shifts on Tue/Thu nights, and one rest evening."
- Good Planner output should include:
  - explicit subproblems (deadline map, task estimation, schedule blocks, contingency triggers)
  - dependency order (estimate tasks before time-blocking)
  - assumptions (for example, "reading speed estimate may be wrong")
  - first-pass plan tied to constraints (for example, no study blocks on Tue/Thu nights)

### Step 2: Guided Interactive Role Cycle (at least 10 turns)
The goal is not just to run four role prompts. The goal is to actively steer, critique, and update the plan as you go.
Use one thread and complete the cycle below.

Required interaction rules:
1. After each role response, write a response to the LLM giving a short reaction (2-4 sentences): what you accept, what you reject, and why.
2. Before moving to the next role, ask at least one follow-up question that forces revision or clarification.
3. Across Step 2, include at least two moments where your feedback changes the plan.

Role cycle:
1. **Role: Planner**
   - Ask for decomposition, dependency order, and first-pass plan.
   - Human checkpoint: look for missing constraints, vague steps, and hidden assumptions.
   - Sample prompt:

```text
Role used: Planner

Using my problem brief and constraints, provide:
1) A decomposition into at least 6 subproblems in dependency order
2) A first-pass plan tied explicitly to each constraint
3) Two assumptions that are most likely to fail

Be concrete. Do not move to other roles.
```
Following the LLM response, ask at least one follow-up question while it is still in the Planner role, asking it 
to clarify or improve something about what it has done.
   - Follow-up prompt examples:
     - "Revise the plan so each subproblem has a concrete output and owner."
     - "Which assumptions are most fragile, and how would we test them quickly?"

You may add extra interactive response turns beyond this first one, to improve the result at this stage.

2. **Role: Checker**
   - Ask for critique of the latest plan against all constraints.
   - Human checkpoint: decide whether each criticism is valid, partially valid, or not valid for your context.
   - Sample prompt:

```text
Role used: Checker

Critique the current plan against every stated constraint.
For each issue, report:
- what fails
- why it matters
- severity (high/medium/low)
- the smallest fix that would resolve it

Do not generate a new full plan yet. Focus on diagnosis.
```
Following the LLM response, ask at least one follow-up question while it is still in the Checker role, asking it 
to clarify or improve something about what it has done.
   - Follow-up prompt examples:
     - "Prioritize the top 3 risks by likelihood and impact."
     - "Which criticisms depend on assumptions that may not hold in my case?"

You may add extra interactive response turns beyond this first one, to improve the result at this stage.

3. **Role: Explainer**
   - Ask for tradeoffs across at least two alternative solution paths.
   - Human checkpoint: identify one tradeoff the model underweighted (for example, relationship trust, time burden, fairness).
   - Sample prompt:

```text
Role used: Explainer

Compare at least two solution paths for this problem.
For each path, explain:
- expected benefits
- expected costs
- key tradeoffs
- conditions under which this path is best

Include a brief recommendation with reasoning, but do not finalize execution steps yet.
```
Following the LLM response, ask at least one follow-up question while it is still in the Explainer role, asking it 
to clarify or improve something about what it has done.
   - Follow-up prompt examples:
     - "Recompare these options with [your priority] weighted highest."
     - "What evidence would make us switch from Option A to Option B?"

You may add extra interactive response turns beyond this first one, to improve the result at this stage.

4. **Role: Executor**
   - Ask for final integrated plan with risks, verification checks, and fallback path.
   - Human checkpoint: confirm the final plan reflects your corrections and values.
   - Sample prompt:

```text
Role used: Executor

Produce the final integrated plan using all prior revisions.
Required sections:
1) Step-by-step action sequence
2) Decision points (if-then triggers)
3) Verification checks after key steps
4) Top risks and mitigations
5) Fallback path if the main approach fails

Keep it practical and aligned with my stated constraints and priorities.
```
Following the LLM response, ask at least one follow-up question while it is in the Executor role, asking it 
to clarify or improve something about what it has done.
   - Follow-up prompt examples:
     - "Convert this into a step-by-step action sequence with decision points."
     - "Add 'if-then' triggers for when to switch to the fallback plan."

You may add extra interactive response turns beyond this first one, to improve the result at this stage.

### Step 3: Final Collaborative Solution + Ratings
Submit your final collaborative solution.
Then rate it (1-5) on all scoring dimensions and confidence.
Also report:
- where collaboration improved quality most
- where collaboration introduced risk/noise
- estimated minutes saved or lost vs Part 1

## Part 4 - Reflection (35-45 min)
Answer all prompts:

1. Which mode produced your strongest final solution, and why?
   - human-only
   - AI-only
   - interactive human+AI
2. Where did overreliance appear, and what was the consequence?
3. Where did underuse appear, and what opportunity was missed?
4. Which assigned role (planner/checker/explainer/executor) was most useful in your case?
5. How did your division of labor shift from early to late collaboration?
6. What is one concrete rule you will use in future human-AI problem solving?

## Discussion Prep (for class group sharing)
Prepare a 2-minute summary:
- your problem context
- one major difference between Part 2A and 2B
- one result from the Part 3 overreliance probe
- your final recommendation for how to divide labor in similar tasks

## What to Turn In
Submit one document containing all items below:

1. Part 0 Setup + Disclosure section.
2. Chosen problem context and Problem Brief.
3. Part 1 decomposition and human-only solution.
4. Part 1 self-evaluation ratings and time spent.
5. Part 2A prompt + full output.
6. Part 2B prompt + full output.
7. Part 2 comparison table and analysis paragraph.
8. Part 3 prompt/output log for required turns.
10. Part 3 final collaborative solution and ratings.
11. Part 4 reflection responses.