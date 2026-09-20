# Preliminary Findings

## Scope

The following findings were derived from the researcher-based comparison of two controlled proof-of-concept experiments:

- Experiment 1 – Mitosis
- Experiment 2 – Meiosis

Both experiments used selected content from the Palestinian Grade 8 Science curriculum and followed the same general level-aware generation procedure.

These findings represent preliminary feasibility observations. They do not constitute validation of the complete proposed framework, formal expert evaluation, learner-effectiveness evidence, or generalizable conclusions.

---

## Finding 1 – Level-Aware Differentiation Was Observed

Across both experiments, the final generated educational packages showed distinguishable Basic, Intermediate, and Advanced characteristics.

The general progression observed was:

**Basic → High Scaffolding → Remember / Understand**

**Intermediate → Moderate Scaffolding → Understand / Apply**

**Advanced → Low Scaffolding → Apply / Analyze**

The differences were reflected in:

- vocabulary complexity;
- explanation depth;
- scaffolding;
- learner independence;
- cognitive demand;
- exercise difficulty;
- and self-assessment difficulty.

This provides preliminary evidence that level differentiation can be produced without intentionally assigning different scientific knowledge to each learner level.

---

## Finding 2 – The Scientific Core Could Remain Fixed While the Pedagogical Treatment Changed

Within each experiment, the curriculum source, selected lesson scope, Learning Objectives, Fixed Retrieved Curriculum Knowledge, and Output Structure were held constant across the three learner levels.

The main intentionally varied element was the Pedagogical Profile.

The final outputs therefore demonstrated a distinction between:

- **WHAT knowledge is available for generation**, controlled by curriculum grounding; and
- **HOW that knowledge is presented and processed**, controlled by the Pedagogical Profile.

This distinction was observed in both Mitosis and Meiosis.

---

## Finding 3 – Higher Difficulty Did Not Require Additional Scientific Knowledge

The final Advanced packages remained more cognitively demanding than the Basic and Intermediate packages after unsupported scientific extensions were removed.

Advanced-level difficulty was maintained through:

- interpretation;
- comparison;
- relationship analysis;
- justification;
- integration;
- and synthesis of the fixed curriculum knowledge.

This suggests that greater pedagogical difficulty can be designed through cognitive operations applied to the same knowledge rather than through the addition of higher-grade or external scientific content.

---

## Finding 4 – Grounding-Related Revisions Were Required in Both Experiments

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
- hypothetical scenarios;
- and analytical extensions beyond the intended curriculum boundary.

These issues were addressed through prompt refinement and stronger grounding constraints.

---

## Finding 5 – Grounding and Cognitive Demand Require Joint Control

Across the two experiments, grounding-related issues appeared in the initial Intermediate and Advanced generations, while the Basic generations were accepted without grounding revision.

This recurring pattern suggests that maintaining a strict curriculum boundary may become more challenging when higher cognitive-demand activities are requested.

However, the two experiments are insufficient to establish that higher cognitive demand causes grounding problems.

The observation instead indicates a design requirement for the proposed framework: level-aware prompting should operate together with explicit curriculum-grounding constraints.

---

## Finding 6 – Prompt Refinement Improved Boundary Adherence Without Removing Level Differentiation

In both experiments, revision prompts were used to remove content that exceeded the Fixed Retrieved Curriculum Knowledge.

The revisions did not simply reduce the difficulty of the generated packages.

Instead, the revised outputs retained their intended Pedagogical Profiles while constraining the scientific content to the defined curriculum boundary.

This provides preliminary design evidence that grounding refinement and pedagogical differentiation can operate together rather than functioning as competing requirements.

---

## Finding 7 – The Two Experiments Tested Only Part of the Proposed Framework

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

Across two selected Grade 8 Science curriculum sections, the controlled proof-of-concept experiments provided preliminary evidence that the same curriculum-grounded knowledge could be transformed into meaningfully differentiated Basic, Intermediate, and Advanced educational packages by varying the Pedagogical Profile while maintaining fixed curriculum knowledge, Learning Objectives, and Output Structure within each experiment.

The experiments also revealed a recurring grounding challenge in the initial higher-demand generations. Prompt refinement and stronger grounding constraints reduced these curriculum-boundary issues while preserving the intended level differentiation.

These findings support continued development and testing of the proposed framework, but they remain preliminary and limited to the current controlled proof-of-concept setting.

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
