# Preliminary Findings

## Scope

The following findings were derived from the researcher-based comparison of two controlled proof-of-concept experiments:

- Experiment 1 – Mitosis
- Experiment 2 – Meiosis

Both experiments used selected content from the Palestinian Grade 8 Science curriculum and followed the same general level-aware generation procedure.

These findings represent preliminary feasibility and design observations. They do not constitute validation of the complete proposed framework, formal expert evaluation, learner-effectiveness evidence, or generalizable conclusions.

---

## Finding 1 – Level Differentiation Was Partial and Uneven

Across both experiments, differences were observed among the final Basic, Intermediate, and Advanced educational packages.

However, the differentiation was not equally clear across all predefined criteria.

The strongest and most consistent differences were observed in:

- Cognitive Demand;
- Exercise Difficulty; and
- Self-Assessment Difficulty.

Weaker differentiation was observed in:

- Vocabulary Complexity;
- Explanation Depth; and
- Scaffolding Level.

The Basic packages were generally more clearly distinguishable from the higher-level packages.

The distinction between Intermediate and Advanced was less consistent, particularly in vocabulary, explanatory structure, and instructional support.

Some Advanced-level differences reflected more academically developed wording, longer formulations, or more demanding task instructions rather than a consistently distinct pedagogical treatment.

Therefore, the two experiments provide preliminary evidence of **partial level differentiation**, rather than uniformly strong differentiation across Basic, Intermediate, and Advanced.

---

## Finding 2 – Control Criteria Remained Stable Across Learner Levels

Within each experiment, the following elements were intentionally held constant:

- curriculum source;
- selected lesson scope;
- five Learning Objectives;
- Fixed Retrieved Curriculum Knowledge; and
- four-component Output Structure.

Three comparison criteria therefore functioned primarily as control criteria:

- Curriculum Grounding;
- Learning Objectives Coverage; and
- Scientific Core Consistency.

These criteria remained largely consistent across the final Basic, Intermediate, and Advanced outputs after required grounding revisions.

This consistency was expected because learner-level differentiation was intended to change how the same scientific knowledge was presented and processed, rather than which scientific knowledge was taught.

---

## Finding 3 – The Pedagogical Profile Influenced Some Dimensions More Strongly Than Others

The Pedagogical Profile was the main experimental variable intentionally changed across the three learner levels.

The two experiments indicate that this variable influenced some output characteristics more clearly than others.

Its strongest observable influence occurred in:

- the cognitive operations required from the learner;
- exercise design; and
- self-assessment design.

Its influence was less distinct in:

- vocabulary complexity;
- explanation depth; and
- scaffolding.

This recurring pattern suggests that the current Pedagogical Profiles require more precise operational definitions if they are intended to produce clearly distinguishable Basic, Intermediate, and Advanced packages across all predefined differentiation criteria.

---

## Finding 4 – Higher Task Demand Could Be Created Without Intentionally Adding New Scientific Knowledge

After grounding-related revisions, the higher-level packages retained more demanding learner activities while remaining within the fixed curriculum knowledge boundary.

Higher task demand was created through operations such as:

- application;
- interpretation;
- comparison;
- relationship analysis;
- justification; and
- integration of fixed concepts.

This provides preliminary design evidence that task difficulty can be increased by changing how learners process the same curriculum knowledge rather than by intentionally introducing higher-grade or external scientific content.

However, this finding applies primarily to the task and assessment dimensions of the generated packages and should not be interpreted as evidence that all pedagogical dimensions were successfully differentiated.

---

## Finding 5 – Grounding-Related Revisions Were Required in Both Experiments

The same broad revision pattern occurred in both controlled experiments:

| Learner Level | Mitosis | Meiosis |
|---|---|---|
| Basic | No grounding revision required | No grounding revision required |
| Intermediate | Grounding-related revision required | Grounding-related revision required |
| Advanced | Grounding-related revision required | Grounding-related revision required |

The specific issues differed between the two experiments.

Examples included:

- ambiguous or expanded scientific explanations;
- hypothetical numerical examples outside the fixed knowledge;
- unsupported causal explanations;
- hypothetical scenarios; and
- analytical extensions beyond the intended curriculum boundary.

These issues were addressed through revision prompts and stronger grounding constraints.

---

## Finding 6 – Grounding and Cognitive Demand Require Joint Control

Across the two experiments, grounding-related issues appeared in the initial Intermediate and Advanced generations, while the Basic generations were accepted without grounding revision.

This recurring pattern suggests that maintaining a strict curriculum boundary may become more challenging when higher cognitive-demand activities are requested.

However, the two experiments are insufficient to establish that higher cognitive demand causes grounding problems.

The observation instead indicates an important design requirement for the proposed framework: level-aware prompting should operate together with explicit curriculum-grounding constraints.

---

## Finding 7 – Prompt Refinement Improved Curriculum-Boundary Adherence

In both experiments, revision prompts were used to remove content that exceeded the Fixed Retrieved Curriculum Knowledge.

The revisions allowed the Intermediate and Advanced packages to retain higher-demand learner activities while improving adherence to the defined curriculum boundary.

This provides preliminary evidence that grounding constraints can be strengthened without necessarily reducing the cognitive demand of the generated activities.

However, the revised outputs still showed uneven differentiation in vocabulary complexity, explanation depth, and scaffolding.

Therefore, successful grounding refinement should not be treated as equivalent to successful level differentiation.

The two requirements should be evaluated separately.

---

## Finding 8 – The WHAT/HOW Distinction Remains Useful but Requires More Precise HOW Controls

The experiments support a conceptual distinction between:

- **WHAT knowledge may be used**, controlled by curriculum grounding; and
- **HOW that knowledge is presented, practiced, and assessed**, intended to be controlled by the Pedagogical Profile.

The curriculum-related controls were successfully maintained in the final accepted outputs.

However, the Pedagogical Profile did not influence every differentiation dimension equally.

The results therefore suggest that the WHAT/HOW distinction remains useful for the proposed framework, but the rules controlling **HOW** content changes across Basic, Intermediate, and Advanced levels require further refinement and more measurable definitions.

---

## Finding 9 – The Two Experiments Tested Only Part of the Proposed Framework

The proof-of-concept experiments primarily examined the curriculum-grounded, level-aware content generation component.

They did not implement or evaluate the complete proposed framework.

In particular, the experiments did not include:

- a complete technical RAG pipeline with explicitly implemented embeddings and vector database retrieval;
- learner-performance testing;
- initial learner-level classification based on actual performance;
- rule-based adaptive level progression based on learner responses;
- learner profile updating;
- formal expert-based qualitative evaluation; or
- a complete expert-driven DBR refinement cycle.

These components therefore remain separate stages of the proposed framework and should not be treated as validated by the current experiments.

---

## Preliminary Overall Finding

Across two selected Grade 8 Science curriculum sections, changing the Pedagogical Profile while maintaining fixed content-related variables produced observable differences in the generated Basic, Intermediate, and Advanced educational packages.

However, the differentiation was **partial and uneven across the predefined criteria**.

The clearest recurring differences were observed in Cognitive Demand, Exercise Difficulty, and Self-Assessment Difficulty.

Vocabulary Complexity, Explanation Depth, and Scaffolding showed weaker differentiation, particularly between the Intermediate and Advanced packages.

The experiments also revealed a recurring grounding challenge in the initial Intermediate and Advanced generations. Revision prompts and stronger grounding constraints improved curriculum-boundary adherence while retaining higher-demand learner activities.

Taken together, the findings indicate that the current level-aware generation approach is promising as a preliminary design direction, but the Pedagogical Profiles and generation prompts require further refinement before stronger claims about clearly separated Basic, Intermediate, and Advanced educational packages can be made.

---

## Design Implication for the Next Iteration

The next refinement should focus on making the differentiation criteria more operational and observable.

In particular, future Pedagogical Profiles should specify more explicit rules for:

- vocabulary and sentence complexity;
- depth of conceptual relationships;
- amount and type of scaffolding;
- learner independence;
- cognitive operations;
- exercise design; and
- self-assessment design.

The purpose of this refinement should be to create more clearly distinguishable levels while preserving:

- the same curriculum knowledge boundary;
- the same scientific learning objectives; and
- the same core scientific content.

Any refined profiles should then be tested in a new documented iteration rather than replacing the original experimental records.

---

## Limitations

The findings should be interpreted within the following boundaries:

- Only two curriculum sections were tested.
- Both sections belong to the same Grade 8 Science lesson.
- Both experiments used Google NotebookLM.
- The comparison was conducted by the researcher.
- No formal expert evaluation was conducted.
- No learner participants were involved.
- Learner outcomes were not measured.
- Adaptive learner progression was not tested.
- A complete technical RAG implementation was not tested.
- Generalizability across subjects, grades, curricula, learners, or LLM environments was not established.
