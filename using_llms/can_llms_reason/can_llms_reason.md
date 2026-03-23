# Can LLMs Reason? It Depends on How You Ask

## Background Info

### Purpose of This Assignment

This assignment investigates a deceptively simple question: when an LLM "solves" a reasoning problem, is it actually reasoning — or is it retrieving a memorized answer and dressing it up in step-by-step language? You will test this by giving LLMs famous reasoning problems they have almost certainly seen in training data, then constructing your own novel variants and observing what happens under different prompting strategies. The core comparison is between performance on canonical (likely memorized) problems versus structurally similar but novel problems, and between naive versus scaffolded versus interactive prompting. By the end, you should have a practical sense of when LLM "reasoning" can be trusted and when it is brittle, shallow, or performative.

### Quick Specs
- **Target time:** ~5–6 hours
- **Model requirements:** At least one LLM chat interface (e.g., ChatGPT, Claude, Gemini). You may use more than one model, but one is sufficient.
- **Grading basis:** Effort, process quality, reproducibility, cross-condition comparison, and reflection
- **Submission format:** Edit and submit this `.md` file

### How to Download This File
1. On the GitHub page for this file, click the **Raw** button (top-right of the file view).
2. Right-click anywhere on the page and choose **Save As**.
3. Make sure the filename ends in `.md` and save it somewhere you can find it.
4. Open it in any text editor (VS Code, PyCharm, Notepad, TextEdit, etc.) to fill it in.
5. Submit the completed `.md` file to Canvas.

### Key Terms

- **Canonical problem:** A well-known version of a reasoning task that has been widely published online, in textbooks, and in puzzle collections. LLMs have almost certainly encountered these exact phrasings during training.
- **Novel variant:** A structurally similar problem you construct yourself, with changed surface features (names, items, relationships) and at least one structural modification (added complexity, altered constraints, changed logical relationships). The goal is to create a problem the LLM is unlikely to have memorized.
- **Naive prompt:** A minimal, unstructured prompt — you present the problem and ask for an answer without giving the model any guidance on how to approach it.
- **Scaffolded prompt:** A structured one-shot prompt that explicitly instructs the model to reason step-by-step, break the problem into subparts, check its work, or follow a particular solution strategy.
- **Interactive session:** A multi-turn conversation where you guide the model through the problem, ask follow-up questions, challenge errors, and probe its reasoning.
- **Reasoning validity:** Whether the intermediate steps in a solution are logically sound — that is, whether each step actually follows from the previous ones, regardless of whether the final answer is correct.
- **Confabulation:** When a model produces a confident, plausible-sounding explanation that does not actually track the logical structure of the problem. The explanation may "sound right" while containing invalid inferences or post-hoc rationalizations.

### Scoring Dimensions

After each LLM condition (canonical, naive, scaffolded, interactive), rate the model's response on the following dimensions using a 1–5 scale:

- **Correctness:** Did the model arrive at the right final answer?
  - 1 = completely wrong
  - 3 = partially correct (e.g., some parts right, some wrong)
  - 5 = fully correct

- **Reasoning validity:** Are the intermediate steps logically sound?
  - 1 = reasoning is mostly invalid, skipped, or circular
  - 3 = some valid steps mixed with unsupported leaps or errors
  - 5 = each step follows logically from the previous one with explicit justification

- **Completeness:** Does the explanation address all necessary parts of the problem?
  - 1 = major steps or cases are missing
  - 3 = most steps are present but some are glossed over
  - 5 = all necessary steps and cases are explicitly addressed

- **Transparency:** When wrong or uncertain, does the model acknowledge it?
  - 1 = confidently wrong with no hedging (confabulation)
  - 3 = some hedging but still presents uncertain conclusions as likely
  - 5 = clearly flags uncertainty, identifies where reasoning is weak, or says "I'm not sure"

### How This Assignment Works

This assignment has two parts, each built around a different family of reasoning problems. Within each part, you follow the same five-step procedure:

**Step 1 — Choose a problem and test the canonical version.** Pick one of three problem options. Present the famous/textbook version to the LLM using a naive prompt. Observe that it (probably) succeeds. Rate the response.

**Step 2 — Ask yourself: is this reasoning or recall?** Before moving on, reflect briefly on whether the model's success tells you anything about its reasoning ability, or whether it might simply be retrieving a memorized solution.

**Step 3 — Construct your own novel variant.** Using the scaffolding provided, build a new version of the problem that preserves the logical structure but changes enough surface and structural features that memorization alone shouldn't help. Solve it yourself first to confirm it has a valid, unique answer. This is your human baseline.

**Step 4 — Run the prompt experiment on your novel variant.** Test the model under three conditions, each in a fresh chat thread:
- **Condition A (Naive):** Present your problem with no guidance. One prompt, one response, no follow-up.
- **Condition B (Scaffolded):** Present your problem with explicit reasoning instructions (step-by-step, check your work, etc.). One prompt, one response, no follow-up.
- **Condition C (Interactive):** Present your problem and then engage in a multi-turn conversation — guide the model, ask it to explain steps, challenge errors, request corrections. Minimum 4 turns total (your prompt + at least 3 follow-ups).

**Step 5 — Analyze and compare.** Rate each condition, fill in the comparison table, and write a short analysis of what changed across conditions and why.

**Important rules for the prompt experiment:**
- Use a **fresh chat thread** for each condition (canonical test, Condition A, Condition B, Condition C). Do not let context from one condition bleed into another.
- In Conditions A and B, do **not** send follow-up messages. One prompt, one response.
- **Save your exact prompts** and representative output excerpts for each condition.
- If you use a model with a "thinking" or "reasoning" mode, note which mode you used and keep it consistent across conditions (or document if you varied it deliberately).


---

## Part 0 — Setup + Disclosure (~15–20 min)

Complete this section before starting the main assignment.

**Models/interfaces used:**
> **[1 POINT]** *YOUR ANSWER HERE — list each model and interface you used (e.g., "Claude Sonnet 3.7, claude.ai web interface").*

**Model version/tier/settings:**
> **[1 POINT]** *YOUR ANSWER HERE — specify free vs. paid, reasoning vs. fast mode, temperature if set, etc.*

**Date/time window:**
> **[1 POINT]** *YOUR ANSWER HERE — approximate date(s) and time range when you did the work.*

**Tools/features used:**
> **[1 POINT]** *YOUR ANSWER HERE — note any special tools or modes (e.g., "thinking mode," "extended thinking," browsing, file upload), or write "none."*

**Disclosure statement:**
> **[1 POINT]** *YOUR ANSWER HERE — 2–4 sentences: what you asked the model to do, what text was copied vs. adapted vs. written yourself.*


---

## Part 1 — Logical Deduction Problems (~120 min)

These problems require you to apply formal logical rules — evaluating whether conclusions follow from premises, identifying which evidence is relevant to testing a rule, or deducing a unique solution from a set of constraints. LLMs tend to perform well on famous versions of these problems, likely because they've seen them many times in training data. But performance often degrades on novel variants — especially when surface content conflicts with logical structure, or when the problem requires careful tracking of multiple interacting constraints.

### Step 1.1 — Choose Your Problem and Test the Canonical Version

Pick **one** of the following three problems. 
Present the canonical version below to your LLM using a simple, minimal prompt (e.g., just paste the problem and ask "What's the answer?" or "Solve this"). 
Do this in a fresh chat thread.

---

**Option A: Syllogism with Believability Conflict**

*What it is:* A syllogism gives you two premises and asks whether a conclusion logically follows. The twist in "believability conflict" syllogisms is that the conclusion is either true in the real world but logically invalid, or false in the real world but logically valid. This creates a tension between what "sounds right" and what the logic actually supports. Humans frequently get these wrong — and so do LLMs.

*Canonical version to present to the LLM:*

> Consider the following syllogism. Is the conclusion logically valid — that is, does it follow necessarily from the premises? Explain your reasoning.
>
> Premise 1: All flowers need water.
> Premise 2: All roses need water.
> Conclusion: Therefore, all roses are flowers.

*Correct answer:* The conclusion is **logically invalid**. This is the fallacy of the undistributed middle. Both flowers and roses need water, but that does not mean roses are a subset of flowers — logically, they could be two separate categories that both happen to need water. The conclusion happens to be true in the real world (roses *are* flowers), but it does not follow from these premises alone. The logical structure is: All A are C; All B are C; therefore All B are A — which is invalid.

---

**Option B: Wason Selection Task**

*What it is:* You are shown four cards, each with information on both sides. You are given a conditional rule ("If P, then Q") and must decide which cards you need to flip over to test whether the rule is being violated. This is one of the most studied reasoning tasks in cognitive psychology — most people (and many LLMs) get it wrong in the abstract version by failing to check the card that could falsify the rule.

*Canonical version to present to the LLM:*

> You see four cards on a table. Each card has a letter on one side and a number on the other side. The visible faces show: **A**, **K**, **4**, **7**.
>
> Here is a rule: "If a card has a vowel on one side, then it has an even number on the other side."
>
> Which card(s) must you flip over to determine whether the rule is being violated? Explain your reasoning.

*Correct answer:* You must flip **A** and **7**. The card showing A could have an odd number on the back (which would violate the rule). The card showing 7 could have a vowel on the back (which would also violate the rule). You do not need to flip K (a consonant tells you nothing about the rule, since the rule only applies to vowels). You do not need to flip 4 (even if it has a consonant on the back, that doesn't violate the rule — the rule doesn't say "only vowels get even numbers"). The common error is choosing A and 4, which reflects confirmation bias (looking for cases that confirm the rule rather than cases that could falsify it).

---

**Option C: Grid Logic Puzzle**

*What it is:* Several people each have a unique combination of attributes (house color, pet, hobby, etc.). A set of clues constrains the possibilities. You must deduce the full assignment from the clues.

*Canonical version to present to the LLM:*

> Three friends — Alice, Bob, and Carol — each live in a different-colored house (red, blue, green) and each own a different pet (cat, dog, fish). Use these clues:
> 1. Alice does not live in the red house.
> 2. The person in the blue house owns a cat.
> 3. Bob does not own a fish.
> 4. Carol lives in the red house.
>
> Who lives in which house and owns which pet?

*Correct answer:* Carol = red house, fish. Alice = blue house, cat. Bob = green house, dog.

---

**Which problem did you choose?**
> **[1 POINT]** *YOUR ANSWER HERE — write A, B, or C.*

**Paste your exact prompt (what you sent to the LLM):**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Paste the model's response (or a representative excerpt):**
> **[1 POINT]** *PASTE THE MODEL'S RESPONSE HERE.*

**Rate the model's response on the canonical version:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

### Step 1.2 — Reasoning or Recall?

Before moving on, reflect briefly (3–5 sentences): Does the model's success on this canonical problem tell you much about whether it can actually reason through this type of problem? What would convince you that this is genuine reasoning rather than pattern-matching against a memorized solution? What features of the problem or the model's response (if any) point in one direction or the other?

> **[3 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences.*

### Step 1.3 — Construct Your Own Novel Variant

Now build your own version of the problem. The goal is to create something more complex than the canonical version and different enough that memorization alone is unlikely to help the LLM. Your variant should be harder than the canonical problem — more steps, more moving parts, more opportunities for the model to go wrong.

You must **solve your own problem by hand first** to confirm it works (has a definite answer for syllogisms and Wason tasks, or exactly one valid solution for grid puzzles). Your hand solution serves as the human baseline for comparison.

Follow the construction guide for the option you chose:

---

**If you chose Option A (Syllogism) — Construction Guide**

The canonical version was a simple two-premise syllogism. Your variant should be a **multi-step argument** with at least 3–4 premises, and it should create a conflict between logical structure and real-world believability.

**Two design choices to make:**

*Choice 1 — Logical structure:* Decide whether your syllogism will be **logically valid** (the conclusion genuinely follows from the premises) or **logically invalid** (the conclusion does not follow, even though it may look like it does). This is the "right answer" the LLM needs to get correct.

*Choice 2 — Content believability:* Decide whether the content will **facilitate** or **inhibit** correct reasoning. Facilitating content means the real-world truth of the conclusion matches its logical status (valid conclusion that sounds true, or invalid conclusion that sounds false). Inhibiting content means the real-world plausibility conflicts with the logical status (valid conclusion that sounds absurd, or invalid conclusion that sounds obviously true). Inhibiting content is harder for both humans and LLMs because it creates a tug-of-war between "does this feel right?" and "does this follow logically?"

This gives you four possible combinations:

| | Facilitating content | Inhibiting content |
|---|---|---|
| **Valid structure** | Valid + conclusion sounds true (easiest) | Valid + conclusion sounds false or absurd (hard) |
| **Invalid structure** | Invalid + conclusion sounds false (moderate) | Invalid + conclusion sounds true (hard — this is what the canonical version does) |

**We recommend choosing an inhibiting-content version** (right column) because these are more likely to reveal whether the LLM is tracking logical form versus just responding to plausibility.

**Symbolic formulas to use as scaffolding:**

Below are templates showing the logical skeleton. Replace each letter with a real-world category to create your content. Use the quantifiers shown, or substitute others (Some, No, Most).

*Chain structure (3–4 premises linked end-to-end):*

```
Premise 1: All A are B.
Premise 2: All B are C.
Premise 3: All C are D.
Conclusion: Therefore, all A are D.    ← VALID
```

To make this invalid, break the chain — for example, swap the conclusion to something that doesn't follow:

```
Premise 1: All A are B.
Premise 2: All B are C.
Premise 3: All C are D.
Conclusion: Therefore, all D are A.    ← INVALID (reverses the direction)
```

*Converging structure (two branches feed into one category):*

```
Premise 1: All A are C.
Premise 2: All B are C.
Conclusion: Therefore, all A are B.    ← INVALID (undistributed middle — same error as the canonical version, but with an extra premise)
```

To make a valid converging version, the branches must connect through a shared link:

```
Premise 1: All A are B.
Premise 2: All C are B.
Premise 3: All B are D.
Conclusion: Therefore, all A are D.    ← VALID (follows from premises 1 and 3; premise 2 is a distractor)
```

*Mixed quantifier structure:*

```
Premise 1: All A are B.
Premise 2: Some B are C.
Conclusion: Therefore, some A are C.    ← INVALID (the "some B" that are C might not overlap with the A's)
```

**How to fill in the letters:**

1. Pick a topic domain (animals, occupations, foods, campus locations — anything you like).
2. Assign each letter a category from that domain.
3. Check whether the real-world relationships between your chosen categories match or conflict with the logical structure. If you want inhibiting content, deliberately choose categories where the real-world truth contradicts the logical status.

*Example of a valid-but-absurd-sounding chain (inhibiting):*

```
Premise 1: All textbooks are flammable objects.
Premise 2: All flammable objects are safety hazards.
Premise 3: All safety hazards require warning labels.
Conclusion: Therefore, all textbooks require warning labels.    ← VALID (but sounds odd)
```

*Example of an invalid-but-true-sounding convergence (inhibiting):*

```
Premise 1: All surgeons have college degrees.
Premise 2: All lawyers have college degrees.
Premise 3: All people with college degrees are literate.
Conclusion: Therefore, all surgeons are lawyers.    ← INVALID (but the shared "college degree" link makes the structure feel connected)
```

That second example is deliberately constructed so the premises create a feeling of connection between surgeons and lawyers, even though the logic doesn't support the conclusion. The third premise is a distractor that makes the argument feel more complete than it is.

---

**If you chose Option B (Wason Selection Task) — Construction Guide**

The canonical version uses an abstract rule with letters and numbers. Your variant should use a **concrete real-world scenario** and should create a conflict between the intuitive "check" and the logically correct one.

**Two design choices to make:**

*Choice 1 — Rule validity:* Decide whether your rule is **logically clean** (a straightforward conditional: "If P then Q") or **complicated** (a biconditional "P if and only if Q," a negated conditional "If not-P then Q," or a rule phrased as "P only if Q"). Complicated phrasings make it harder to identify which cards to flip.

*Choice 2 — Content framing:* Decide whether the scenario will **facilitate** or **inhibit** correct reasoning. Research in psychology has shown that people perform much better on the Wason task when the rule is framed as a social contract or permission rule (e.g., "If you are drinking alcohol, you must be over 21") compared to an arbitrary abstract rule. Facilitating content uses a social-contract framing where violations feel intuitively obvious. Inhibiting content uses an arbitrary or counterintuitive rule where the correct cards to flip are not obvious.

This gives you four possible combinations:

| | Facilitating content (social contract) | Inhibiting content (arbitrary rule) |
|---|---|---|
| **Clean rule (If P then Q)** | Easiest — intuition and logic align | Moderate — abstract content, but simple rule |
| **Complicated rule** | Moderate — intuitive scenario, but tricky phrasing | Hardest — arbitrary content and tricky rule |

**We recommend choosing an inhibiting-content version or a complicated-rule version** (or both) because these are more likely to reveal reasoning failures.

**Symbolic formula and card template:**

The Wason task always has this structure: a **rule** and a set of **cards** where each card has two sides. You need to identify which cards could reveal a violation of the rule.

*Step 1 — Write your rule:*

The basic form is: **"If [P], then [Q]."**

Replace P and Q with observable properties. For example:
- P = "a student is in the library after midnight," Q = "they have a valid late-access pass"
- P = "a product is labeled organic," Q = "it contains no synthetic pesticides"
- P = "an employee works on a holiday," Q = "they receive overtime pay"

For a complicated version, try one of these phrasings (each is subtly different in what counts as a violation):
- **"P only if Q"** — logically equivalent to "If P then Q," but people often misinterpret it
- **"If not-P, then Q"** — flips which cards matter
- **"P if and only if Q"** — now violations can go in both directions

*Step 2 — Construct your cards:*

You need at least 4 cards. Each card should show one visible face. The standard set is:

| Card | Visible face | Hidden face |
|---|---|---|
| Card 1 | Shows P | Could have Q or not-Q on the back |
| Card 2 | Shows not-P | Could have Q or not-Q on the back |
| Card 3 | Shows Q | Could have P or not-P on the back |
| Card 4 | Shows not-Q | Could have P or not-P on the back |

For the basic rule "If P then Q," the correct cards to flip are **Card 1 (P)** and **Card 4 (not-Q)** — because those are the only cards that could reveal a violation. Card 1 could have not-Q on the back (violation). Card 4 could have P on the back (violation). The common error is choosing Card 1 and Card 3, which is confirmation bias.

For your variant, fill in concrete content for each card face. You may also add a 5th or 6th card to increase complexity (e.g., an ambiguous case, or a second P-type card with different content).

*Step 3 — Verify your answer:*

Before giving this to the LLM, work through each card yourself: "If I flip this card and see [X] on the back, does that violate the rule? If I see [Y], does that violate it?" A card needs to be flipped only if there is some possible back-side value that would constitute a violation.

*Example of a complicated-rule, inhibiting-content variant:*

> A university has the following policy: "A student may use the research lab only if they have completed the safety training."
>
> You see four student ID cards. Each card shows the student's lab access status on one side and their training status on the other. The visible faces show:
> - Card 1: "Has lab access"
> - Card 2: "Does not have lab access"
> - Card 3: "Completed safety training"
> - Card 4: "Has not completed safety training"
>
> Which cards must you flip to check whether the policy is being violated?

Answer: Flip Card 1 and Card 4. "P only if Q" means "If P then Q" — if someone has lab access (P), they must have completed training (Q). Card 1 might show "has not completed training" on the back (violation). Card 4 might show "has lab access" on the back (violation).

---

**If you chose Option C (Grid Logic) — Construction Guide**

The canonical version was a 3-person, 2-attribute puzzle with simple direct clues. Your variant should be a **4-person, 2-attribute puzzle** (or 3-person, 3-attribute puzzle) using a mix of direct and indirect clues.

**Construction template:**

*Step 1 — Set up your grid:*

Choose your entities and attributes. For example:

| Person | Attribute 1 (e.g., color) | Attribute 2 (e.g., pet) |
|---|---|---|
| Person A: ___ | Value 1a: ___ | Value 2a: ___ |
| Person B: ___ | Value 1b: ___ | Value 2b: ___ |
| Person C: ___ | Value 1c: ___ | Value 2c: ___ |
| Person D: ___ | Value 1d: ___ | Value 2d: ___ |

Fill in the solution first — this is the answer you are working toward.

*Step 2 — Write clues that lead to exactly one solution:*

Use a mix of clue types (aim for at least 5–6 clues for a 4×2 puzzle):
- **Direct positive:** "Alex lives in the blue house." (Directly assigns a value.)
- **Direct negative:** "Jordan does not own the cat." (Eliminates one option.)
- **Relational:** "The person who owns the dog lives in the green house." (Links two attribute values without naming the person.)
- **Conditional:** "If Sam lives in the red house, then Sam owns the fish." (Only applies under a condition.)
- **Negative relational:** "The person in the yellow house does not own the bird." (Eliminates a cross-attribute pairing.)
- **Compound negative:** "Neither the cat owner nor the person in the blue house is Morgan." (Eliminates two possibilities at once.)

*Step 3 — Verify unique solvability:*

Work through your clues by hand using a standard elimination grid. Confirm that (a) you can reach the solution using only the given clues, and (b) no clue is redundant (removing any single clue should make the puzzle unsolvable or ambiguous). If a clue is redundant, remove it or replace it — the puzzle should be tight.

*Tips for making it harder for LLMs:*
- Use relational and compound-negative clues more than direct ones — LLMs tend to handle "X lives in Y" easily but struggle with "The person who does not own Z does not live next to the person in W."
- Include at least one clue that requires multi-step inference (you can't use it directly; you have to combine it with another clue first).
- Use names and attributes that don't have strong real-world associations (avoid "the farmer owns the chicken" patterns that might activate memorized associations).

---

**Your novel problem (paste the full text of the problem you constructed):**
> **[3 POINTS]** *PASTE YOUR NOVEL PROBLEM HERE.*

**Which design choices did you make?**

If Option A: What is your logical structure (chain, converging, mixed quantifier, or other)? Is it valid or invalid? Is the content facilitating or inhibiting?

If Option B: What is your rule phrasing (If P then Q, P only if Q, biconditional, negated)? Is the content facilitating (social contract) or inhibiting (arbitrary)?

If Option C: How many people/attributes? What clue types did you use?

> **[1 POINT]** *YOUR ANSWER HERE — identify your design choices in 2–4 sentences.*

**Your hand-solved answer (show your work):**
> **[4 POINTS]** *YOUR ANSWER HERE — write out your solution step by step. For syllogisms, show the logical form and explain why the conclusion is valid or invalid. For Wason tasks, explain for each card why it does or does not need to be flipped. For grid puzzles, show your elimination steps. This is your human baseline.*

**What features of your variant do you think will be hardest for the LLM, and why?**
> **[2 POINTS]** *YOUR ANSWER HERE — 2–4 sentences identifying the specific features you expect to challenge the model and your prediction about what will go wrong.*

### Step 1.4 — Prompt Experiment on Your Novel Variant

Now run three conditions on your novel variant, each in a **fresh chat thread**. Follow the procedure described in "How This Assignment Works" above.

#### Condition A: Naive Prompt

Present your novel problem to the LLM with no guidance — just the problem text and a request to solve it.

**Paste your exact prompt:**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Paste the model's response (or representative excerpt):**
> **[1 POINT]** *PASTE THE MODEL'S RESPONSE HERE.*

**Rate the response:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

#### Condition B: Scaffolded Prompt

Present your novel problem with explicit instructions for structured reasoning. Use or adapt the following template:

```text
Solve the following problem step by step.

[Paste your novel problem here]

Instructions:
1. Before solving, identify all the constraints and what type of logic each one requires.
2. Work through the possibilities systematically — do not jump to an answer.
3. For each step, state what you are concluding and which constraint(s) justify it.
4. After reaching an answer, verify it by checking every constraint against your solution.
5. If any constraint is violated, go back and find the error.
```

**Paste your exact prompt:**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Paste the model's response (or representative excerpt):**
> **[1 POINT]** *PASTE THE MODEL'S RESPONSE HERE.*

**Rate the response:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

#### Condition C: Interactive Session

Present your novel problem in a fresh thread, then engage in a multi-turn conversation. Your goals are to:
- Ask the model to explain its reasoning at each step
- Challenge any step that seems wrong or unjustified
- Ask it to verify its own answer against the constraints
- If it got something wrong, point out the error and see if it can recover

You need at least **4 total turns** (your initial prompt + at least 3 follow-ups).

**Paste your initial prompt:**
> **[1 POINT]** *PASTE YOUR INITIAL PROMPT HERE.*

**Paste the key exchanges from your conversation (at least 3 follow-ups and responses, or a representative excerpt if the conversation was long):**
> **[1 POINT]** *PASTE YOUR CONVERSATION EXCERPT HERE.*

**Rate the model's final answer after the interactive session:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

### Step 1.5 — Part 1 Analysis

**Comparison table:**

| Dimension | Canonical (Step 1.1) | Condition A (Naive) | Condition B (Scaffolded) | Condition C (Interactive) |
|---|---|---|---|---|
| Correctness | | | | |
| Reasoning validity | | | | |
| Completeness | | | | |
| Transparency | | | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

**Analysis (write 1–2 paragraphs):** What changed between the canonical version and your novel variant? Did the model's performance drop, and if so, where? What changed between the naive, scaffolded, and interactive conditions on your novel variant — did structure or interaction help, and if so, in what specific ways? Were there any moments of confabulation (confident but invalid reasoning)?

> **[3 POINTS]** *YOUR ANSWER HERE — write 1–2 paragraphs.*


---

## Part 2 — Cognitive Bias Problems (~120 min)

These problems exploit systematic errors in human reasoning — situations where fast intuitive thinking produces a confident but wrong answer, and arriving at the correct answer requires overriding that intuition with careful analysis. These are among the most heavily studied problems in cognitive psychology, and their canonical versions are all over the internet. LLMs almost certainly have them memorized. The question is whether they can handle novel variants that preserve the same logical trap but change the surface content.

### Step 2.1 — Choose Your Problem and Test the Canonical Version

Pick **one** of the following three problems. Present the canonical version below to your LLM using a simple, minimal prompt (e.g., just paste the problem and ask for the answer). Do this in a fresh chat thread.

---

**Option A: Cognitive Reflection Test (CRT) Item**

*What it is:* CRT problems are designed so that an obvious, intuitive answer springs to mind immediately — but that answer is wrong. The correct answer requires suppressing the intuitive response and doing more careful reasoning. The classic example was introduced by Shane Frederick in 2005 and has become one of the most widely replicated findings in cognitive psychology.

*Canonical version to present to the LLM:*

> A bat and a ball cost \$1.10 in total. The bat costs \$1.00 more than the ball. How much does the ball cost?

*Correct answer:* The ball costs **\$0.05** (and the bat costs \$1.05). 
The intuitive but wrong answer is \$0.10 — which feels right because \$1.00 + \$0.10 = \$1.10.
But fails the "costs \$1.00 *more*" constraint.
The difference between \$1.10 and \$0.10 is \$1.00, but the difference between \$1.05 and \$0.05 is also \$1.00,
and only the latter pair sums to $1.10.

*Why LLMs often get the canonical version right:* This exact problem has been discussed in thousands of articles, blog posts, and textbooks. Most current LLMs have almost certainly memorized the answer and the reasoning. Success on this version tells you very little about whether the model can actually do the underlying algebra.

---

**Option B: Conjunction Fallacy (Linda Problem)**

*What it is:* The conjunction fallacy occurs when people judge the conjunction of two events (A and B) as more probable than one of the events alone (A), because the conjunction fits a compelling narrative. Logically, P(A and B) can never exceed P(A) — the conjunction of two events is always less likely than or equal to either event alone. This was demonstrated by Tversky and Kahneman in 1983 and remains one of the most famous findings in judgment and decision-making research.

*Canonical version to present to the LLM:*

> Linda is 31 years old, single, outspoken, and very bright. She majored in philosophy. As a student, she was deeply concerned with issues of discrimination and social justice, and also participated in anti-nuclear demonstrations.
>
> Which is more probable?
> (a) Linda is a bank teller.
> (b) Linda is a bank teller and is active in the feminist movement.

*Correct answer:* **(a) is more probable.** 
No matter how well the description matches a "feminist bank teller," if we are treating this as a statement of formal logic,
the probability that Linda is a bank teller (which includes all bank tellers, including feminist ones) must be greater than or equal to the probability that she is specifically a bank teller *and* a feminist activist. 
Option (b) is a subset of option (a). 
Choosing (b) is the conjunction fallacy — the narrative coherence of the description makes the more specific option feel more representative, overriding the basic probability rule.

*Why LLMs often get the canonical version right:* This problem has been analyzed extensively online. LLMs typically give the correct answer along with an explanation of the conjunction rule. But this may reflect memorization of the "Linda problem" as a pattern rather than genuine probabilistic reasoning.

---

**Option C: Base Rate Neglect (Bayesian Reasoning)**

*What it is:* Base rate neglect occurs when people focus on the specific diagnostic information (like a test result) and ignore the prior probability (how common the condition is in the population). The correct answer requires applying Bayes' theorem, which combines the base rate with the diagnostic information. People — and LLMs — tend to dramatically overestimate the probability when the base rate is low, because the high test accuracy feels like it should dominate the answer.

*Canonical version to present to the LLM:*

> A disease affects 1 in 1000 people in a population. A test for the disease is 95% accurate — meaning it correctly identifies 95% of people who have the disease (sensitivity), and correctly identifies 95% of people who don't have the disease (specificity). A randomly selected person tests positive. What is the probability that this person actually has the disease?

*Correct answer:* Approximately **1.9%** (roughly 1 in 53). Here's the calculation: Out of 100,000 people, 100 have the disease and 99,900 don't. The test correctly identifies 95 of the 100 who have it (true positives). The test incorrectly flags 5% of the 99,900 who don't have it = 4,995 (false positives). Total positives: 95 + 4,995 = 5,090. Probability of actually having the disease given a positive test: 95 / 5,090 ≈ 0.019 or about 1.9%. The intuitive but wrong answer is "about 95%," which ignores the base rate entirely.

*Why LLMs often get the canonical version right:* The "1 in 1000, 95% accurate test" problem is a textbook example found across hundreds of statistics, probability, and cognitive bias resources. LLMs can typically reproduce the Bayesian calculation correctly for this exact setup.

---

**Which problem did you choose?**
> **[1 POINT]** *YOUR ANSWER HERE — write A, B, or C.*

**Paste your exact prompt (what you sent to the LLM):**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Paste the model's response (or a representative excerpt):**
> **[1 POINT]** *PASTE THE MODEL'S RESPONSE HERE.*

**Rate the model's response on the canonical version:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

### Step 2.2 — Reasoning or Recall?

Before moving on, reflect briefly (3–5 sentences): Does the model's success on this canonical problem tell you much about whether it can actually reason through this type of problem? What would convince you that this is genuine reasoning rather than pattern-matching against a memorized solution? What features of the problem or the model's response (if any) point in one direction or the other?

> **[3 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences.*

### Step 2.3 — Construct Your Own Novel Variant

Now build your own version of the problem. As in Part 1, the goal is to create something that preserves the core cognitive trap but changes enough surface and structural features that memorization alone is unlikely to help. Your variant should be at least as complex as the canonical version, and ideally harder.

You must **solve your own problem by hand first** to confirm it has a definite correct answer. Your hand solution serves as the human baseline for comparison.

Follow the construction guide for the option you chose:

---

**If you chose Option A (CRT) — Construction Guide**

The canonical bat-and-ball problem works by embedding a simple algebra problem inside a misleading surface frame. The word "more" creates an intuitive subtraction that gives the wrong answer. Your variant should use the same structural trick — an intuitive mental shortcut that gives a wrong answer — but with different content and numbers.

**The algebraic structure behind CRT problems:**

The bat-and-ball problem has this hidden structure:

```
Given:
  X + Y = Total
  X = Y + Difference

Intuitive (wrong) answer: Y = Total - Difference
Correct answer: Y = (Total - Difference) / 2
```

In the canonical version: Total = \$1.10, Difference = \$1.00, so the correct answer is (\$1.10 - \$1.00) / 2 = \$0.05. The intuitive answer is \$1.10 - \$1.00 = \$0.10.

**How to build your variant:**

*Step 1 — Choose new content and numbers:*

Pick a new cover story (not bats and balls) and new values for Total and Difference. 
The trick works best when the intuitive wrong answer is a round, satisfying number.

Template:
```
A [item1] and a [item2] cost [Total] in total.
The [item1] costs [Difference] more than the [item2].
How much does the [item2] cost?

Intuitive (wrong) answer: Total - Difference = ___
Correct answer: (Total - Difference) / 2 = ___
```

Your attempt to test the LLM against memorization will work even better if you can change cover story in as many ways as possible.
For example:
- change the ordering of the information
- add irrelevant or extraneous details that have no bearing or are even misleading
- change the story so it is not about "cost" differences but some other quantitative difference: size, weight, etc.

Examples of good number choices:
- Total = \$2.50, Difference = \$2.00 → Intuitive: \$0.50, Correct: $0.25
- Total = \$5.30, Difference = \$5.00 → Intuitive: \$0.30, Correct: $0.15
- Total = 110 minutes, Difference = 100 minutes → Intuitive: 10 min, Correct: 5 min

*Step 2 — Make it harder (do at least one of the following):*

1. **Multi-part version:** Add a second relationship that depends on the first answer. For example: "A notebook and a pen cost $3.20 together. The notebook costs $3.00 more than the pen. A folder costs twice as much as the pen. How much do all three items cost together?" (Now the model must get the first part right to answer the second.)
2. **Non-monetary framing:** Use time, weight, distance, or another unit instead of money. For example: "A hike to the summit and back takes 5 hours and 10 minutes total. The hike up takes 5 hours longer than the hike down." This obscures the algebraic structure by removing the familiar "$" cue.
3. **Reversed or nested phrasing:** Instead of "X costs Y more than Z," try "Z costs Y less than X" or "the difference between X and Z is Y, and together they are T."
4. **Add a distractor:** Include extra information that is irrelevant to the calculation but makes the problem feel more complex. For example: "There are 15 items on the shelf. A lamp and a vase cost $6.20 together. The lamp costs $6.00 more than the vase. The other 13 items cost $4.00 each. How much does the vase cost?"

*Step 3 — Verify:*

Solve your problem algebraically. Confirm that (a) the intuitive answer is wrong, (b) the correct answer is unambiguous, and (c) if you added a multi-part extension, the chain of reasoning works.

---

**If you chose Option B (Conjunction Fallacy) — Construction Guide**

The canonical Linda problem works by giving a character description that strongly activates a stereotype, then asking people to compare a general category against a conjunction that matches the stereotype. Your variant should use the same structural trap but with a completely different character and category pairing.

**The logical structure behind conjunction fallacy problems:**

```
Setup: A vivid description of person X that strongly suggests trait T.

Question: Which is more probable?
  (a) X is a member of broad category C.
  (b) X is a member of broad category C AND has trait T.

Correct answer: Always (a), because P(C and T) ≤ P(C).
Fallacy: People choose (b) because the description makes C+T feel more "representative" of X than C alone.
```

**How to build your variant:**

*Step 1 — Choose a character profile and target categories:*

Create a character description (3–5 sentences) that strongly suggests a particular trait or identity without stating it outright. Then choose a broad category (C) that feels unlikely given the description, and a conjunction (C + T) that feels much more fitting.

Template:
```
Character: [Name] is [age], [personality traits], [background details].
[2-3 sentences of behavioral/biographical details that strongly suggest trait T
 without ever stating it directly.]

Which is more probable?
(a) [Name] is a [broad category C].
(b) [Name] is a [broad category C] and [trait T].
```

The key: the description should make option (b) feel intuitively compelling, even though (a) is always the logically correct answer.

*Step 2 — Make it harder (do at least one of the following):*

1. **Multiple conjunctions:** Add options (c) and (d) that combine the broad category with different traits — some matching the description and some not. For example: "(a) Marcus is a high school teacher. (b) Marcus is a high school teacher and coaches the debate team. (c) Marcus is a high school teacher and coaches the football team. (d) Marcus is a high school teacher, coaches the debate team, and volunteers at the public library." Now the student must recognize that (a) is more probable than all of the others, and that (d) is the *least* probable despite matching the description best.
2. **Quantitative framing:** Instead of "which is more probable," ask the person to assign probabilities to each option (e.g., "rate the probability of each on a 0–100 scale"). This makes the violation more measurable — if someone rates (b) higher than (a), the conjunction fallacy is explicit and numerical.
3. **Strengthen the misleading description:** Make the character description very detailed and specific, with lots of concrete behavioral examples that all point toward trait T. The stronger the narrative pull, the harder it is for the LLM to resist the fallacy.
4. **Use an unfamiliar domain:** Instead of well-known social categories (bank teller, feminist), use occupational or hobby categories that the model is less likely to have seen in conjunction-fallacy examples: birdwatcher, food truck owner, competitive chess player, community theater actor.

*Step 3 — Verify:*

Confirm that (a) your broad category genuinely includes the conjunction as a subset (this is what makes the conjunction rule apply), and (b) your description creates a strong intuitive pull toward the conjunction option. Try to articulate why someone (or an LLM) might choose the conjunction — this will help you analyze the model's response later.

---

**If you chose Option C (Base Rate Neglect) — Construction Guide**

The canonical medical-test problem works by combining a low base rate with a reasonably accurate test, producing a counterintuitive result: even after a positive test, the probability of having the disease is still low. Your variant should use the same Bayesian structure but with different numbers, a different domain, and ideally a twist that makes the calculation harder.

**The mathematical structure behind base rate problems:**

```
Given:
  Base rate: P(condition) = B          (e.g., 1/1000 = 0.001)
  Sensitivity: P(positive | condition) = S    (e.g., 0.95)
  Specificity: P(negative | no condition) = Sp  (e.g., 0.95)
  False positive rate: P(positive | no condition) = 1 - Sp

Bayes' theorem:
  P(condition | positive) = (S × B) / [(S × B) + ((1-Sp) × (1-B))]

The intuitive (wrong) answer: People typically say "about S" (e.g., ~95%)
The correct answer is usually much lower when B is small.
```

A useful shortcut for constructing these: imagine a population of N people. Count the true positives, false positives, and compute the ratio. This "natural frequency" approach is easier than working with the formula directly.

**How to build your variant:**

*Step 1 — Choose a domain and set your parameters:*

Pick a scenario other than medical testing. Good alternatives include: quality control in manufacturing (defective parts), airport security (detecting contraband), hiring (screening tests for job performance), fraud detection (flagging suspicious transactions), or academic misconduct (plagiarism detectors).

Template:
```
In a population of [N], the base rate of [condition] is [B].
A detection method has:
  - Sensitivity of [S]% (correctly identifies [S]% of true cases)
  - Specificity of [Sp]% (correctly clears [Sp]% of non-cases)
A randomly selected [entity] tests positive. What is the probability it actually has [condition]?
```

Choose your numbers so that the correct answer is counterintuitive — meaning the base rate is low enough that even with good test accuracy, the posterior probability is surprisingly small. Here are some parameter combinations that work well:

| Base rate (B) | Sensitivity (S) | Specificity (Sp) | Correct posterior | Intuitive wrong answer |
|---|---|---|---|---|
| 1/1000 (0.1%) | 95% | 95% | ~1.9% | "about 95%" |
| 1/500 (0.2%) | 90% | 90% | ~1.8% | "about 90%" |
| 1/100 (1%) | 99% | 95% | ~16.7% | "about 99%" |
| 1/200 (0.5%) | 80% | 90% | ~3.8% | "about 80%" |

*Step 2 — Make it harder (do at least one of the following):*

1. **Two-test scenario:** After the first positive, administer a second independent test (same or different accuracy). Ask for the updated probability. This requires applying Bayes' theorem twice, using the posterior from the first test as the prior for the second. Most LLMs struggle significantly with this step.
2. **Asymmetric error rates:** Make the sensitivity and specificity different from each other (e.g., sensitivity = 99%, specificity = 90%). The canonical version uses the same number for both, which makes it easier to remember/memorize; asymmetric rates force real calculation.
3. **Natural frequency framing vs. probability framing:** Present the problem using raw counts instead of percentages ("Out of 10,000 products, 50 are defective. The scanner catches 48 of the 50 defective ones, but also flags 500 of the 9,950 good ones.") and see if the model handles it differently. Or present it in pure probability notation and see if it can convert.
4. **Embedded comparison:** Ask the model to compare two scenarios with different base rates but the same test accuracy, and explain which scenario makes the test more useful. For example: "The same 95%-accurate test is used in City A (prevalence 5%) and City B (prevalence 0.1%). In which city is a positive result more meaningful, and by how much?"

*Step 3 — Verify:*

Work through the calculation yourself using the natural frequency method:
1. Start with a round population number (e.g., 100,000).
2. Compute: how many have the condition? How many don't?
3. Of those who have it, how many test positive? (true positives = condition count × sensitivity)
4. Of those who don't, how many test positive? (false positives = non-condition count × (1 - specificity))
5. Posterior = true positives / (true positives + false positives)

If you used a two-test extension, repeat steps 3–5 using the posterior from the first test as the new base rate.

---

**Your novel problem (paste the full text of the problem you constructed):**
> **[3 POINTS]** *PASTE YOUR NOVEL PROBLEM HERE.*

**Which design choices did you make?**

If Option A: What are your Total and Difference values? Which complexity extensions did you add (multi-part, non-monetary, reversed phrasing, distractor)?

If Option B: What is your character profile designed to suggest? What categories did you use? Which extensions did you add (multiple conjunctions, quantitative framing, unfamiliar domain)?

If Option C: What are your base rate, sensitivity, and specificity values? What domain did you use? Which extensions did you add (two-test, asymmetric rates, natural frequency, embedded comparison)?

> **[1 POINT]** *YOUR ANSWER HERE — identify your design choices in 2–4 sentences.*

**Your hand-solved answer (show your work):**
> **[4 POINTS]** *YOUR ANSWER HERE — For CRT: show the algebra. For conjunction fallacy: explain why the broad category must be more probable and identify the specific trap in your description. For base rate: show the natural frequency calculation step by step. This is your human baseline.*

**What features of your variant do you think will be hardest for the LLM, and why?**
> **[2 POINTS]** *YOUR ANSWER HERE — 2–4 sentences identifying the specific features you expect to challenge the model and your prediction about what will go wrong.*

### Step 2.4 — Prompt Experiment on Your Novel Variant

Now run three conditions on your novel variant, each in a **fresh chat thread**. Follow the procedure described in "How This Assignment Works" above.

#### Condition A: Naive Prompt

Present your novel problem to the LLM with no guidance — just the problem text and a request to solve it.

**Paste your exact prompt:**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Paste the model's response (or representative excerpt):**
> **[1 POINT]** *PASTE THE MODEL'S RESPONSE HERE.*

**Rate the response:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

#### Condition B: Scaffolded Prompt

Present your novel problem with explicit instructions for structured reasoning. Use or adapt the following template:

```text
Solve the following problem step by step. Be careful — the intuitive answer may be wrong.

[Paste your novel problem here]

Instructions:
1. Before computing anything, identify what the problem is actually asking and what mathematical or logical relationship is involved.
2. Set up the problem formally — define variables, write equations, or draw out the probability space.
3. Solve step by step, showing all work.
4. After reaching an answer, plug it back into the original problem to verify it satisfies all stated conditions.
5. If your answer doesn't check out, find and correct the error.
```

**Paste your exact prompt:**
> **[1 POINT]** *PASTE YOUR EXACT PROMPT HERE.*

**Paste the model's response (or representative excerpt):**
> **[1 POINT]** *PASTE THE MODEL'S RESPONSE HERE.*

**Rate the response:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

#### Condition C: Interactive Session

Present your novel problem in a fresh thread, then engage in a multi-turn conversation. Your goals are to:
- Ask the model to explain its reasoning at each step
- Challenge any step that seems wrong or unjustified
- Ask it to verify its own answer against the original constraints
- If it got something wrong, point out the error and see if it can recover

You need at least **4 total turns** (your initial prompt + at least 3 follow-ups).

**Paste your initial prompt:**
> **[1 POINT]** *PASTE YOUR INITIAL PROMPT HERE.*

**Paste the key exchanges from your conversation (at least 3 follow-ups and responses, or a representative excerpt if the conversation was long):**
> **[1 POINT]** *PASTE YOUR CONVERSATION EXCERPT HERE.*

**Rate the model's final answer after the interactive session:**

| Dimension | Rating (1–5) | Brief justification |
|---|---|---|
| Correctness | | |
| Reasoning validity | | |
| Completeness | | |
| Transparency | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

### Step 2.5 — Part 2 Analysis

**Comparison table:**

| Dimension | Canonical (Step 2.1) | Condition A (Naive) | Condition B (Scaffolded) | Condition C (Interactive) |
|---|---|---|---|---|
| Correctness | | | | |
| Reasoning validity | | | | |
| Completeness | | | | |
| Transparency | | | | |

> **[2 POINTS]** *REPLACE THIS TABLE WITH YOUR COMPLETED RATINGS.*

**Analysis (write 1–2 paragraphs):** What changed between the canonical version and your novel variant? Did the model fall for the cognitive bias trap, or did it avoid it? If it avoided it on the canonical version but fell for it on your variant, what does that tell you? What changed between the naive, scaffolded, and interactive conditions — did explicit reasoning instructions help the model avoid the trap? Were there any moments of confabulation (confident but invalid reasoning)?

> **[3 POINTS]** *YOUR ANSWER HERE — write 1–2 paragraphs.*


---

## Part 3 — Reflection (~35–45 min)

Look across both parts of the assignment and answer the following questions.

**1. The memorization question:** Across your two problem types, how much of the LLM's success on canonical versions do you think reflects genuine reasoning versus memorized solutions? What evidence from your novel variants supports your assessment?

> **[4 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences.*

**2. Prompt sensitivity:** How much did the model's reasoning quality change based on how you asked? Was the effect of scaffolding and interaction consistent across problem types, or did it matter more for some types than others?

> **[4 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences.*

**3. Confabulation patterns:** Did you observe cases where the model was confidently wrong — producing fluent, plausible-sounding reasoning that was actually invalid? What did those cases have in common?

> **[4 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences.*

**4. Canonical vs. novel performance:** For each part, compare the model's performance on the canonical version to its performance on your novel variant. Was the drop-off similar across both problem types, or did the model handle novelty better in one domain than the other? What might explain the difference?

> **[5 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences.*

**5. Your own reasoning versus the model's:** Comparing your hand-solved solutions to the model's attempts, where did the model reason in ways you found genuinely useful or insightful? Where did it fall short of what a careful human would do?

> **[4 POINTS]** *YOUR ANSWER HERE — write 3–5 sentences.*

**6. Practical takeaway:** Based on this experience, when would you trust an LLM to reason through a novel problem, and what safeguards would you put in place? State a concrete rule or heuristic you would follow.

> **[4 POINTS]** *YOUR ANSWER HERE — write 2–4 sentences.*

### Discussion Prep

Prepare a 2-minute summary for in-class group discussion:
- Which problem type showed the biggest gap between canonical and novel performance?
- One example of a confabulation or reasoning breakdown you observed
- Your best practical rule for when to trust (and when to verify) LLM reasoning


---

## What to Turn In

Submit your completed version of this `.md` file to Canvas. Before submitting, confirm:

- [ ] Part 0 Setup + Disclosure is filled in
- [ ] Part 1 has a chosen problem, canonical test, novel variant, and three-condition experiment
- [ ] Part 2 has a chosen problem, canonical test, novel variant, and three-condition experiment
- [ ] All required prompt texts are pasted in
- [ ] All required output excerpts are included
- [ ] All rating tables are completed with justifications
- [ ] All analysis sections are written
- [ ] Part 3 reflection is complete
- [ ] All "YOUR RESPONSE HERE" placeholders have been replaced
