# Comparing Models and Interfaces Lab

## Background Info
### Purpose of This Assignment
This assignment is designed to dive deeper into how different models perform, using a summarization task as our benchmark. 
In particular, we want to help you separate **model effects** from **interface effects** while working on the same real task. 
You will compare how different systems handle the same source reading and evaluate differences in quality, control, transparency, and trust. The main outcomes are (1) learning hidden options/settings in major LLM platforms, and (2) testing one structured two-condition comparison path.

### Quick Specs
- Target time: ~5-6 hours
- Model requirements: No paid account required. Everyone should be able to complete this assignment with free tools.
- Required platforms in Part 1: ChatGPT, Claude, Gemini (web interfaces)
- Required comparison in Part 2: Choose one path (A, B, or C)
- Grading basis: Effort, process quality, condition control, reproducibility, and reflection
- Submission format: One document (`.pdf`, `.docx`, or `.md`) with required tables, prompt logs, and reflection

### Key Terms
- **Model effect**: A difference caused mainly by the underlying model.
- **Interface effect**: A difference caused mainly by product/interface design, defaults, tooling, or workflow constraints.
- **Condition**: One specific setup you compare (for example, chat interface vs API workflow).
- **One-shot run**: One prompt and one response, with no follow-up before scoring.
- **Revision run**: One fixed follow-up prompt applied after the one-shot run in the same thread.
- **Source-faithfulness**: How well output reflects the source text without adding unsupported claims.
- **Calibration**: How well confidence/uncertainty language matches what is actually supported by the source.

### Scoring Dimensions (Use in Parts 1-3)
Rate each scored output on a 1-5 scale:

1. **Source-faithfulness**
   - 1 = many unsupported or distorted claims
   - 3 = mostly grounded, with some drift
   - 5 = strongly grounded in source with clear uncertainty where needed
2. **Constraint adherence**
   - 1 = misses multiple required constraints
   - 3 = meets most constraints with minor misses
   - 5 = meets all required constraints exactly
3. **Audience fit**
   - 1 = mismatched level/tone
   - 3 = partially appropriate for audience
   - 5 = consistently clear and audience-appropriate
4. **Calibration and transparency**
   - 1 = overconfident, little uncertainty signaling
   - 3 = mixed confidence quality
   - 5 = clear uncertainty handling and transparent reasoning limits
5. **Usability**
   - 1 = hard to use for discussion or study
   - 3 = usable with edits
   - 5 = directly usable with minimal edits

### Source Description
You must use an article/chapter that you have already read before and know reasonably well.
Ideally, it is something you have written yourself, and know *that* well.
The goal here is to evaluate how different LLMs, and their different options, settings, and versions, vary in how they perform.

Choose one:
1. **Assigned course reading (recommended):** `/course_content/how_llms_work/LLMs_CH2.docx`
2. **Your own source text:** any article/chapter you have already read and understand or written yourself.

If you choose your own source, it must satisfy all:
- You have read it before this assignment week.
- It is long enough to support synthesis (recommended: 1500+ words).
- It is non-sensitive and appropriate for class discussion.

### If You Get Stuck
Use this sequence before changing tasks:
1. Narrow your source excerpt to 6-12 paragraphs.
2. Re-read and write 5 bullet notes in your own words (no model).
3. Continue with the required prompts exactly as written.
4. If a platform feature is unavailable, mark it `Unavailable` and continue.

## Part 0 - Setup + Disclosure (20-25 min)
Put this at the top of your submission.

1. Models/interfaces used
2. Model versions/settings (free/paid, fast/thinking, etc.)
3. Date/time window (approximate is fine)
4. Tools/features used (browsing, file upload, projects, memory, API console, etc.)
5. Disclosure statement (3-6 sentences):
   - what you asked the model(s) to do
   - what text was copied directly vs adapted vs fully original
   - whether you used any extra tools/scripts

## Part 1 - Platform Options + Settings Exposure (90-105 min)
Goal: learn what each platform exposes or hides, and test small setting changes under controlled prompts.

### Step 1: Prepare the source excerpt (15 min)
Create one source excerpt you will reuse throughout the assignment.
- Use one excerpt only (same excerpt for all runs).
- Length target: ~600-1,200 words.
- Add paragraph numbers `[P1]`, `[P2]`, etc., so you can reference evidence location.

### Step 2: Human-only baseline (15-20 min)
Without LLM help, produce:
1. A 120-180 word summary of the excerpt.
2. Three key claims, points, or events from the excerpt.
3. One likely misconception or misunderstanding a reader might have.

### Step 3: Feature discovery checklist (30-40 min)
Inspect ChatGPT, Claude, and Gemini web interfaces and complete this table.

| Platform | Model picker visible? | Access to Reasoning/thinking mode? | Access to File upload? | Access to Web/browse tool? | Memory/custom instructions? | Advanced controls visible? | Notes on defaults/constraints |
|---|---|------------------------------------|------------------------|----------------------------|---|---|---|
| ChatGPT |  |                                    |                        |                            |  |  |  |
| Claude |  |                                    |                        |                            |  |  |  |
| Gemini |  |                                    |                        |                            |  |  |  |

### Step 4: Controlled settings probe (30-35 min)
You will do **6 one-shot runs total** using the same mini prompt below.

Run counts:
- **S1-S3:** one baseline run each on ChatGPT, Claude, Gemini (default settings)
- **S4-S6:** for all three platforms, rerun after changing exactly one visible setting (if available)

Rules:
1. Start a fresh thread for each run.
2. One prompt, one response (no follow-up before scoring).
3. Keep the source excerpt and prompt text identical except for the one setting change in S4-S5.

Mini prompt for Part 1 runs:

```text
Use only the source excerpt below.

[PASTE THE SAME SOURCE EXCERPT WITH PARAGRAPH TAGS]

Output exactly three sections about the source above:
1) Summary (120-150 words)
2) Three key claims with paragraph references
3) One likely misconception and a correction
```

Part 1 run log template:

| Run ID | Platform | Setting state | Fresh thread? | Output quality notes (3-5 bullets) | Source-faithfulness (1-5) | Constraint adherence (1-5) | Audience fit (1-5) | Calibration and transparency (1-5) | Usability (1-5) |
|--------|---|---|---|---|---|---|---|---|---|
| S1     |  |  |  |  |  |  |  |  |  |
| S2     |  |  |  |  |  |  |  |  |  |
| S3     |  |  |  |  |  |  |  |  |  |
| S4     |  |  |  |  |  |  |  |  |  |
| S5     |  |  |  |  |  |  |  |  |  |
| S6     |  |  |  |  |  |  |  |  |  |

## Part 2 - Main Comparison Path (Choose One) (140-160 min)
Goal: run one controlled two-condition comparison and produce a common deliverable set.

### Step 1: Choose a comparison path (10 min)
Pick one option only.

1. **Option A: Paid vs Free**  
Use the same company/model family where possible.  
Condition 1 = free tier, Condition 2 = paid tier.

Starter scaffolding:
- Keep interface as similar as possible between tiers.
- If a feature exists only in paid, note it as a condition difference.

2. **Option B: Chat Interface vs Companion Tool**  
Example companions: coding assistant, studio/workbench, project tool, notebook-like workspace.  
Condition 1 = standard chat interface, Condition 2 = companion tool.

Starter scaffolding:
- Use the same source and prompts.
- Focus on control, visibility, and workflow differences.

3. **Option C: API vs Web Chat (Gemini default free path)**  
Condition 1 = web chat interface, Condition 2 = API route.

Starter scaffolding:
- No-code route: use an API playground/console.
- Code-capable route: use minimal `curl` or a short script.
- If you use OpenAI/Anthropic API instead of Gemini, disclose paid status/settings.

### Step 2: Run the common task in both conditions (90-110 min)
For each condition, run exactly:
- **M1:** one-shot core prompt
- **M2:** fixed revision prompt in same thread

Total required runs in Part 2: **4 runs** (2 conditions x 2 runs)

Rules:
1. M1 must be one-shot (no pre-scoring follow-up).
2. M2 must use the exact revision prompt below.
3. Use the same source excerpt across both conditions.
4. Record exact settings and tools per run.

Core prompt (M1):

```text
You are helping me create a summary of a written text.
Use only the source excerpt below. If a claim is uncertain or weakly supported by the excerpt, mark it clearly.

[PASTE THE SAME SOURCE EXCERPT WITH PARAGRAPH TAGS]

Output exactly three sections:
1) Main Summary (250-350 words): central thesis + 3 major supporting points + 1 limitation/counterpoint.
2) Claims Table (exactly 6 rows): columns = Claim | Evidence from excerpt (with paragraph tags) | Uncertainty (Low/Med/High) | Why uncertain.
3) Audience Rewrite (150-200 words): explain for a first-year psychology student with no prior AI background.
```

Fixed revision prompt (M2):

```text
Revise all three sections for a skeptical audience.

Requirements:
- Reduce unsupported certainty.
- Keep the Claims Table at exactly 6 rows.
- Keep total length under 650 words.
- Add a final section titled "What Would Change My Mind" with exactly 3 bullet points.
```

Example Claims Table row (format example only):

| Claim | Evidence from excerpt | Uncertainty | Why uncertain |
|---|---|---|---|
| Transformer models reduced recurrence in sequence modeling. | [P8] describes attention replacing recurrence for long-range dependencies. | Low | Mechanism is directly explained in text; implementation details still omitted. |

### Step 3: Compare conditions with scoring + notes (40 min)
Complete one comparison table for M1 and M2 outputs.

| Condition | Interface/tool | M1 scores (5 dimensions) | M2 scores (5 dimensions) | Time spent | Biggest strength | Biggest failure mode |
|---|---|---|---|---|---|---|
| Condition 1 |  |  |  |  |  |  |
| Condition 2 |  |  |  |  |  |  |

Then write 2 short paragraphs:
1. What changed from M1 to M2 in each condition?
2. Which differences seem likely due to model capability vs interface/workflow?

## Part 3 - Attribution Analysis + Discussion Prep (45-60 min)
Goal: make explicit, evidence-based judgments about model vs interface effects.

### Step 1: Attribution matrix (30-40 min)
List at least **6 observed differences** from your runs and classify each as:
- likely model effect
- likely interface effect
- mixed/uncertain

Use this template:

| Observation | Evidence from run logs | Classification (model / interface / mixed) | Why |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Example attribution statement:
- "Condition 2 preserved table constraints more reliably across revisions, which likely reflects interface/tool structure rather than deeper model knowledge."

### Step 2: Discussion-ready summary card (15-20 min)
Prepare a 2-minute class summary:
1. Source text used
2. Comparison path chosen
3. One strong finding
4. One failure mode
5. One practical recommendation for classmates

## Part 4: Final Reflection (25-30 min)
Answer all prompts:

1. What did you learn about hidden defaults and settings across ChatGPT, Claude, and Gemini?
2. In your Part 2 path, what was the most important difference between the two conditions?
3. Where did you trust output too quickly, and what signal should have slowed you down?
4. What is one rule you will use in future model/interface comparisons?
5. If you repeated this assignment, what would you change first?

## What to Turn In
Submit one document containing all of the following:

1. Part 0 Setup + Disclosure section.
2. Source selection note (assigned reading or chosen source) and your excerpt with paragraph tags.
3. Part 1 human-only baseline.
4. Part 1 feature discovery checklist table.
5. Part 1 run logs for S1-S5.
6. Part 2 path selection and condition definitions.
7. Exact M1 and M2 prompts used for both conditions (4 runs total), with key output excerpts.
8. Part 2 comparison table and two analysis paragraphs.
9. Part 3 attribution matrix (6 observations minimum).
10. Final reflection responses.
