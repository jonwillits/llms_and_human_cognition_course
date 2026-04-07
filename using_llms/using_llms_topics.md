# Using LLMs Topics

## 1. LLMs as Writing Partners: Help or Harm?

### Description

Explore how LLMs function as collaborators in writing tasks—drafting, revising, summarizing, or stylistically transforming text—and whether this support improves clarity and argumentation or instead encourages surface-level polish, loss of voice, and cognitive offloading.

### Assignment Activities

- Baseline comparison: You will write a short paragraph or argument unaided, then revise it with an LLM, and compare what changed in structure, clarity, and substance.
- Role manipulation: You will prompt the model as an editor, a co-author, and a critic, then compare how each role changes your final text and your own effort.
- Voice and ownership probe: You will mark parts of the final text that feel "yours" versus "the model's," and note whether the LLM pulls you toward a generic style.
- Failure case exploration: You will intentionally give the model a vague or flawed draft and evaluate whether it improves the underlying reasoning or mainly smooths the writing.

## 2. Can LLMs Reason? It Depends on How You Ask...

### Description

Explore how much of an LLM's "reasoning" is a stable capability versus an interaction effect created by the prompt or set of prompts. You'll test the same problems under different forms of guidance (constraints, decomposition, examples, and step-by-step formats) and look for telling patterns: sudden collapses, confident nonsense, shallow pattern-matching, or surprisingly robust multi-step solutions. The goal is to develop a practical sense of when an LLM can be treated like a reasoning partner and when it behaves more like a persuasive generator.

### Assignment Activities

- Prompt variation test: You will pose the same reasoning problem using different prompt styles (direct answer, step-by-step reasoning, decomposition into subproblems) and compare accuracy and consistency.
- Fragility probe: You will slightly modify a successful prompt (e.g., remove structure or add ambiguity) and observe when and how reasoning breaks down.
- Self-explanation check: You will ask the model to explain its own answers and evaluate whether the explanations track the solution or merely rationalize the output.
- Comparison to human reasoning: You will solve the same problem yourself, then reflect on which steps were genuinely assisted by the LLM and which were obscured or distorted.

## 3. Creative Generation and Idea Fixation

### Description

Explore how LLMs change the space of ideas you generate—sometimes expanding it with novel combinations, but sometimes narrowing it by anchoring you on common tropes, "safe" continuations, or the model's default aesthetic. You'll use LLMs for brainstorming and creative production, then analyze whether they increase originality and diversity or instead produce convergence, cliche, and fixation. The goal is to learn when LLMs are genuinely generative versus when they quietly standardize what counts as a "good idea."

### Assignment Activities

- Baseline creativity comparison: You will generate ideas (e.g., research hypotheses, story premises, product concepts, or experiment variants) first without an LLM and then with one, and compare novelty, diversity, and usefulness.
- Fixation test: You will start from an LLM's first set of ideas and attempt a second round that explicitly avoids overlap, then measure how hard it is to escape the initial cluster.
- Prompt framing manipulation: You will vary prompts to encourage safe vs risky ideation (e.g., "best practices" vs "weird alternatives") and compare how the output distribution changes.
- Human recombination step: You will take multiple LLM-generated ideas and deliberately recombine or mutate them, then evaluate whether your best outcomes come from the model's suggestions or your transformations.

## 4. Human–AI Collaboration in Problem Solving

### Description

Explore how problem-solving changes when humans and LLMs work together, focusing on how tasks are divided, when collaboration helps or hurts, and how coordination failures arise. You'll examine whether LLMs function best as advisors, collaborators, or tools, and how overreliance, underuse, or misalignment between human goals and model behavior affects outcomes. The aim is to understand collaboration not as "human vs. AI," but as a joint cognitive system with its own strengths and weaknesses.

### Assignment Activities

- Task decomposition comparison: You will solve a multi-step problem alone, then with an LLM, and compare solution quality, time, and error patterns.
- Role assignment experiment: You will assign the LLM different roles (planner, checker, explainer, executor) and evaluate which roles lead to the most effective collaboration.
- Overreliance probe: You will intentionally accept or reject LLM suggestions and track when trust improves outcomes versus when it leads to errors.
- Reflection on division of labor: You will document which cognitive steps you outsourced, which you retained, and whether that division felt stable or fragile.

## 5. Bias, Perspective, and Representation in Practice

### Description

Explore how social, cultural, and normative biases surface in everyday LLM use—not only through overt stereotypes, but through omissions, framing choices, and defaults about what counts as normal, important, or relevant. Rather than treating bias as an abstract property of models, you'll investigate how it emerges in specific tasks and how prompt choices, constraints, and context can amplify or mitigate these effects.

### Assignment Activities

- Prompt sensitivity exploration: You will pose the same question with different framing, identities, or assumptions and observe how the model's perspective and emphasis shift.
- Omission analysis: You will analyze what perspectives, groups, or alternatives are consistently left out of model responses to open-ended prompts.
- Mitigation attempt: You will experiment with prompts intended to reduce bias (e.g., explicit diversity constraints) and evaluate their effectiveness and limitations.
- Comparison to human judgment: You will compare model outputs to your own intuitions or to human-authored texts, noting where biases align, diverge, or become harder to detect.

## 6. LLMs and the Feeling of Knowing

### Description

Explore the boundary between using LLMs as tools for understanding and using them as shortcuts that bypass learning. You'll test whether different kinds of assistance—explanations, worked examples, answers, or feedback—lead to deeper comprehension, superficial performance, or misplaced confidence. The goal is to distinguish uses that support learning from those that merely improve outputs without improving understanding.

### Assignment Activities

- Assistance type comparison: You will learn a new concept using different forms of LLM help (explanation, example, direct answer) and compare retention and understanding afterward.
- Delayed performance test: You will complete a follow-up task without LLM access to see which forms of assistance transfer to independent performance.
- Confidence calibration check: You will rate your confidence before and after using the LLM and compare it to actual performance.
- Boundary reflection: You will articulate criteria for when LLM use feels like learning support versus cheating, and note where the boundary is unclear.
- Comparison to human reasoning: You will solve the same problem yourself, then reflect on which steps were genuinely assisted by the LLM and which were obscured or distorted.

## 7. Comparing Models and Interfaces

### Description

Explore how differences between models (e.g., size, training style, alignment) and interfaces (chat UI, system prompts, APIs) shape behavior, reliability, and user trust. You'll investigate how much of what people attribute to "the model" is actually a consequence of interface design, defaults, or interaction constraints, and how these choices influence cognition and decision-making.

### Assignment Activities

- Cross-model comparison: You will run the same prompts on different models (or model settings) and compare output quality, consistency, and failure modes.
- Interface contrast: You will perform the same task using a chat-based interface and a more structured or programmatic interaction (where available), noting differences in control and transparency.
- Default behavior probe: You will remove or alter system instructions or safety constraints (when possible) and observe how outputs change.
- Attribution reflection: You will reflect on which differences feel like "model intelligence" versus interface effects, and how that distinction affects your trust in the system.

## 8. Vibe Coding vs. Structured Code Querying

### Description

Explore two contrasting ways of using LLMs for programming and data analysis: informal, conversational "vibe coding" versus more explicit, structured querying with clear specifications and constraints. You'll examine how these interaction styles affect correctness, reproducibility, debugging, and your own understanding of the code. The goal is to see when natural-language fluency accelerates progress and when it masks errors or weakens conceptual grasp.

### Assignment Activities

- Style comparison task: You will attempt the same coding or data-analysis task using free-form conversational prompts and then using a carefully specified, step-by-step query, and compare the resulting code.
- Debugging challenge: You will intentionally introduce an error and observe how easily it can be detected and fixed under each interaction style.
- Reproducibility check: You will assess whether the generated code can be rerun, modified, or explained without further LLM assistance.
- Understanding reflection: You will reflect on how well you understand the final code in each condition and where fluency substituted for comprehension.

## 9. LLMs for Data Analysis and Interpretation

### Description

Explore how LLMs can assist with data analysis workflows—from generating analysis code to interpreting statistical outputs—and where their strengths and weaknesses lie. You'll examine whether LLMs improve insight, merely speed up routine steps, or introduce subtle errors and overconfident interpretations that are hard to detect without domain knowledge.

### Assignment Activities

- Code generation test: You will ask an LLM to generate analysis code for a dataset and evaluate its correctness, assumptions, and robustness.
- Interpretation comparison: You will compare the model's interpretation of results (tables, plots, statistics) with your own or with a reference explanation.
- Error discovery exercise: You will identify at least one mistake, omission, or questionable assumption in the LLM's analysis or interpretation.
- Workflow reflection: You will reflect on which parts of the analysis pipeline benefited most from LLM assistance and which required careful human oversight.

## 10. Literature Review: Synthesis or Hallucination?

### Description

Explore how well LLMs can support background research by summarizing literatures, identifying themes, and connecting ideas—and where they fail by fabricating citations, blurring distinctions between theories, or smoothing over genuine disagreements. You'll assess whether LLMs function as useful tools for orientation and synthesis or whether they create a false sense of understanding in domains you only partially know.

### Assignment Activities

- Grounded review test: You will ask an LLM to summarize a research area you are already somewhat familiar with and compare its account to the actual papers.
- Citation audit: You will check whether cited studies exist, are described accurately, and support the claims attributed to them.
- Boundary probing: You will push the model to distinguish between closely related theories or findings and observe where it collapses distinctions.
- Usefulness reflection: You will evaluate which stages of literature review (orientation, synthesis, critique) the LLM helped with and where it was actively misleading.

## 11. Brainstorming Research Questions

### Description

Explore how LLMs can be used to generate research questions, hypotheses, and directions, and whether this process genuinely expands the space of inquiry or mainly recombines familiar ideas and paradigms. You'll examine how prompt framing, constraints, and background context shape the kinds of questions the model proposes, and whether those questions are theoretically meaningful, novel, and empirically tractable.

### Assignment Activities

- Idea generation comparison: You will generate a set of research questions on a topic without an LLM and then with LLM assistance, and compare novelty, clarity, and scope.
- Constraint manipulation: You will ask the model for questions under different constraints (e.g., "high risk," "incremental," "theory-driven," "data-driven") and observe how the output changes.
- Feasibility check: You will select a few LLM-generated questions and assess whether they could realistically be studied with available methods and data.
- Meta-reflection: You will reflect on whether the model pushed you toward questions you would not have considered, or toward safer, more conventional ideas.

## 12. Designing Experiments

### Description

Explore how LLMs can assist in translating research questions into experimental designs, including choices about variables, controls, tasks, and measurements. You'll investigate whether LLMs help clarify design logic and anticipate confounds, or whether they produce superficially plausible but methodologically weak or incoherent experiments.

### Assignment Activities

- Design generation task: You will ask an LLM to propose an experiment for a given research question and examine its structure, assumptions, and completeness.
- Confound detection: You will identify potential confounds or design flaws in the LLM's proposal that are not explicitly acknowledged.
- Iterative refinement: You will iteratively prompt the model to improve the design and assess whether revisions meaningfully strengthen the experiment or merely add complexity.
- Human–model comparison: You will compare the LLM-generated design to one created by you or discussed in class, noting where the model's reasoning aligns with or diverges from standard experimental logic.

## 13. Operationalizing Constructs and Writing Methods Sections

### Description

Explore how LLMs handle the difficult step of translating abstract theoretical constructs into concrete, measurable variables and procedures. You'll test whether models can generate sensible operational definitions and methods descriptions, or whether they gloss over key assumptions, validity concerns, and tradeoffs that are central to good experimental design.

### Assignment Activities

- Construct operationalization task: You will ask an LLM to operationalize an abstract construct (e.g., attention, cognitive load, anxiety) and evaluate the validity and clarity of the proposed measures.
- Methods drafting exercise: You will have the model draft a methods section based on a study description and analyze what details are missing, vague, or unjustified.
- Validity critique: You will assess the operationalizations in terms of construct validity, reliability, and potential confounds.
- Revision comparison: You will revise the LLM-generated methods yourself and reflect on which improvements required domain knowledge the model did not supply.

## 14. Interpreting Statistical Results and Writing Results Sections

### Description

Explore how LLMs interpret statistical outputs and communicate empirical findings, and whether they respect inferential logic or merely produce rhetorically polished summaries. You'll examine how models handle uncertainty, effect sizes, significance, and causal language, and where they tend to overstate, misattribute, or obscure results.

### Assignment Activities

- Results interpretation test: You will give an LLM statistical outputs (e.g., regression tables, p-values, confidence intervals, plots) and compare its interpretation to a correct or instructor-provided explanation.
- Language audit: You will analyze whether the model uses appropriate hedging, avoids causal claims when unwarranted, and accurately reflects uncertainty.
- Error identification: You will identify at least one subtle misinterpretation, omission, or misleading phrasing in the LLM's results write-up.
- Human rewrite comparison: You will rewrite the results section yourself and reflect on where your interpretation diverges from the model's and why.

## 15. Implications of AI for Replication and Reproducibility

### Description

Explore how LLMs interact with issues of scientific reliability, including whether they help clarify analytic pipelines or instead introduce hidden assumptions, undocumented choices, and specification gaming. You'll examine how easily LLM-generated analyses can be reproduced and how small prompt changes can lead to materially different "results."

### Assignment Activities

- Reproduction attempt: You will attempt to reproduce an analysis or result generated with LLM assistance and document which steps are underspecified or irreproducible.
- Specification sensitivity test: You will slightly vary prompts or assumptions and observe how much the resulting analysis or conclusions change.
- Pipeline audit: You will reconstruct the full analytic pipeline implied by the LLM's output and identify missing decisions or defaults.
- Reliability reflection: You will reflect on whether LLM use made the analysis more transparent and robust or more opaque and fragile.

## 16. Theoretical Argumentation and Counterargument Generation

### Description

Explore how LLMs construct theoretical arguments and generate counterarguments, and whether they engage with underlying assumptions, evidence, and logical structure or mainly reproduce rhetorically balanced positions. You'll examine whether LLMs help clarify debates and reveal hidden premises, or instead create the illusion of depth by presenting symmetrical but shallow viewpoints.

### Assignment Activities

- Argument generation task: You will ask an LLM to generate an argument for a theoretical position relevant to cognitive science and evaluate its coherence and evidential grounding.
- Counterargument probe: You will have the model generate counterarguments and assess whether they meaningfully challenge the original position or merely restate common objections.
- Assumption analysis: You will identify unstated assumptions in both the argument and counterargument produced by the LLM.
- Human–model comparison: You will write your own argument or counterargument and compare its structure and depth to the model's output.

## 17. Constructing and Critiquing Survey Instruments

### Description

Explore how LLMs generate survey questions and scales, and whether they capture psychological constructs accurately or fall prey to leading wording, ambiguity, and poor measurement practices. You'll test whether LLMs can support early-stage instrument design while recognizing the limits of their understanding of psychometrics and respondent behavior.

### Assignment Activities

- Item generation task: You will ask an LLM to generate survey items for a specific construct and evaluate clarity, bias, and redundancy.
- Wording sensitivity check: You will modify item phrasing and observe how small changes alter the construct being measured.
- Validity critique: You will assess the generated items for face validity, construct validity, and potential response biases.
- Revision exercise: You will revise the LLM-generated survey and reflect on which improvements required domain knowledge or methodological judgment.

## 18. Ethical Review and IRB-Style Reasoning

### Description

Explore how LLMs reason about research ethics, risk, and human subjects protections, and whether they capture the spirit of ethical review or merely reproduce surface-level norms and checklists. You'll examine how well models anticipate real-world harms, contextual nuance, and power dynamics, and where their ethical reasoning breaks down.

### Assignment Activities

- Ethical assessment task: You will present an experimental proposal to an LLM and ask it to identify ethical risks and mitigation strategies.
- Context sensitivity probe: You will modify key details of the study (population, setting, stakes) and observe whether the model's ethical assessment adapts appropriately.
- Comparison to formal standards: You will compare the model's reasoning to IRB guidelines or case studies and identify omissions or misprioritizations.
- Judgment reflection: You will reflect on which ethical concerns the model raised that you found insightful and which important issues it failed to recognize.

## 19. Using Open-Source Models, Tools, and APIs

### Description

Explore how working directly with open-source LLMs and programmatic interfaces changes what you can do, what you can see, and what responsibility you bear as a user. You'll compare chat-based, closed systems with open models and APIs to understand tradeoffs in transparency, control, reproducibility, and ethical risk.

### Assignment Activities

- Interface comparison task: You will complete a simple task using a closed chat-based LLM and an open-source model or API (where feasible), and compare control, visibility, and limitations.
- Parameter exploration: You will adjust settings such as temperature, context length, or system prompts and observe how these affect outputs and stability.
- Pipeline construction: You will design a minimal workflow (e.g., prompt → output → verification step) and reflect on how tooling shapes reliability.
- Responsibility reflection: You will reflect on how greater control and access also increase responsibility for misuse, bias, or error.

## 20. Text Analysis and Annotation

### Description

Explore how LLMs can be used for text analysis tasks such as coding, labeling, summarization, and annotation, and how their performance compares to human judgment and traditional computational methods. You'll investigate when LLMs function as efficient assistants for qualitative analysis and when they introduce bias, inconsistency, or overconfident categorization.

### Assignment Activities

- Annotation comparison task: You will use an LLM to annotate or code a small corpus of text and compare its labels to your own or to a reference scheme.
- Consistency check: You will rerun the same annotation task with slight prompt variations and assess how stable the model's categorizations are.
- Bias and framing probe: You will examine whether certain categories are overused, underused, or implicitly reframed by the model.
- Human–model reconciliation: You will reconcile disagreements between your annotations and the model's and reflect on which judgments you trust and why.

## 21. Using LLMs for Meta-Reasoning and Self-Reflection

### Description

Explore whether LLMs can support reflection on your own thinking—such as identifying blind spots, questioning assumptions, or suggesting alternative strategies—or whether they mainly mirror and reinforce existing beliefs. You'll test the extent to which models can function as productive "thinking mirrors" versus sources of confirmation bias and overconfidence.

### Assignment Activities

- Reflection prompting task: You will ask an LLM to critique your reasoning process on a task and suggest alternative approaches or perspectives.
- Blind-spot probe: You will prompt the model to identify assumptions or weaknesses in your argument and evaluate whether these insights are substantive or generic.
- Confirmation bias test: You will vary prompts to encourage agreement versus critique and observe how readily the model adapts its stance.
- Metacognitive reflection: You will reflect on whether the model genuinely helped you think differently or mainly provided reassuring feedback.
