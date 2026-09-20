# Level-Aware Educational Content Generation Experiments

## Overview

This repository documents controlled proof-of-concept experiments conducted as part of a Master's research project on curriculum-grounded, level-aware educational content generation using Large Language Models (LLMs).

The experiments investigate whether the same curriculum-grounded knowledge can be transformed into educational packages for three intended learner levels:

- Basic
- Intermediate
- Advanced

while maintaining control over the curriculum source, learning objectives, retrieved knowledge, and output structure.

The experiments use selected content from the Palestinian Grade 8 Science curriculum and Google NotebookLM as the generation environment.

---

## Research Context

The experiments support the development of a proposed knowledge-grounded LLM framework that integrates:

- Official curriculum knowledge
- Retrieval-Augmented Generation (RAG)
- Level-aware pedagogical profiles
- Structured educational content generation
- Learner assessment
- Rule-based adaptive level progression
- Expert-based qualitative evaluation

The experiments currently documented in this repository focus primarily on the **curriculum-grounded, level-aware content generation component** of the proposed framework.

They should not be interpreted as implementation or validation of the complete framework.

---

## Current Experiments

### Experiment 1 – Mitosis

The first experiment investigates level-aware generation using the **Mitosis** section of the Palestinian Grade 8 Science curriculum.

The same fixed curriculum knowledge and learning objectives were used to generate:

- Basic educational package
- Intermediate educational package
- Advanced educational package

Initial and revised outputs are retained where grounding-related revisions were required.

### Experiment 2 – Meiosis

The second experiment replicates the same general experimental procedure using the **Meiosis** section from the same curriculum source.

The same Basic, Intermediate, and Advanced Pedagogical Profiles used in Experiment 1 were retained.

This replication allows comparison of level differentiation and grounding behavior across two selected curriculum sections.

---

## Experimental Principle

The experiments are based on a distinction between:

> **Curriculum Grounding controls WHAT knowledge may be used.**

and:

> **The Pedagogical Profile is intended to control HOW that knowledge is explained, structured, practiced, and assessed.**

The intended level progression defined before generation was:

**Basic → High Scaffolding → Remember / Understand**

**Intermediate → Moderate Scaffolding → Understand / Apply**

**Advanced → Low Scaffolding → Apply / Analyze**

These profiles represent the intended experimental conditions. Whether the generated outputs actually reflected these distinctions was evaluated separately using the predefined comparison criteria.

---

## Repository Structure

The repository is organized to preserve the experimental procedure, inputs, prompts, generated outputs, revisions, and analysis in a transparent and reproducible structure.

```text
level-aware-educational-content-experiments/
│
├── README.md
│
├── experiment-01-mitosis/
│   ├── 01-source-input/
│   │   ├── source-information.md
│   │   └── انقسام الخلايا.pdf
│   │
│   ├── 02-experiment-setup/
│   │   ├── learning-objectives.md
│   │   ├── pedagogical-profiles.md
│   │   ├── fixed-retrieved-knowledge.md
│   │   ├── output-structure.md
│   │   └── experiment-parameters.md
│   │
│   ├── 03-prompts/
│   │   ├── basic-prompt.md
│   │   ├── intermediate-prompt.md
│   │   ├── intermediate-revision-prompt.md
│   │   ├── advanced-prompt.md
│   │   └── advanced-revision-prompt.md
│   │
│   ├── 04-outputs/
│   │   ├── basic-final.md
│   │   ├── intermediate-initial.md
│   │   ├── intermediate-final.md
│   │   ├── advanced-initial.md
│   │   └── advanced-final.md
│   │
│   └── 05-analysis/
│       ├── issues-and-revisions.md
│       └── comparative-analysis.md
│
├── experiment-02-meiosis/
│   ├── 01-source-input/
│   ├── 02-experiment-setup/
│   ├── 03-prompts/
│   ├── 04-outputs/
│   └── 05-analysis/
│
└── cross-experiment-analysis/
    ├── comparison.md
    └── preliminary-findings.md
```

---

## Experimental Variables

The experiments were designed as controlled proof-of-concept trials.

### Variables Held Fixed Within Each Experiment

The following elements were kept constant across the Basic, Intermediate, and Advanced generation conditions:

- Curriculum source
- Selected lesson scope
- Five Learning Objectives
- Fixed Retrieved Curriculum Knowledge
- Knowledge boundary
- Generation environment
- Four-component Output Structure

### Variable Intentionally Changed

The main variable intentionally changed across the three generation conditions was the **Pedagogical Profile**.

The Pedagogical Profile was intended to control:

- Vocabulary complexity
- Explanation depth
- Scaffolding level
- Concept load
- Example style
- Cognitive demand
- Learner independence
- Exercise design
- Self-assessment difficulty

The final outputs were then compared to determine the extent to which these intended differences were actually reflected in the generated packages.

### Fixed Output Structure

Each generated educational package contained exactly four components:

1. Explanations
2. Key Vocabulary
3. Exercises
4. Self-Assessment Questions

---

## Comparison Criteria

The final outputs were evaluated using ten predefined criteria:

1. Curriculum Grounding
2. Learning Objectives Coverage
3. Vocabulary Complexity
4. Explanation Depth
5. Scaffolding Level
6. Cognitive Demand
7. Exercise Difficulty
8. Self-Assessment Difficulty
9. Scientific Core Consistency
10. Overall Level Differentiation

For interpretation, three criteria functioned primarily as **control criteria**:

- Curriculum Grounding
- Learning Objectives Coverage
- Scientific Core Consistency

These were expected to remain stable across learner levels.

The main **differentiation criteria** were:

- Vocabulary Complexity
- Explanation Depth
- Scaffolding Level
- Cognitive Demand
- Exercise Difficulty
- Self-Assessment Difficulty

This distinction prevents expected consistency in the scientific content from being incorrectly interpreted as a failure of level differentiation.

---

## Grounding and Revision Procedure

Generated outputs were reviewed against the Fixed Retrieved Curriculum Knowledge.

When an initial generation introduced content that exceeded the defined curriculum boundary, a revision prompt was applied while attempting to preserve the intended learner-level Pedagogical Profile.

For transparency, both the initial and revised outputs are retained in the repository when a grounding-related revision was required.

In the two current experiments:

- Basic outputs were accepted without grounding revision.
- Intermediate outputs required grounding-related revision.
- Advanced outputs required grounding-related revision.

This is an observed pattern within the two controlled experiments and should not be interpreted as evidence that higher cognitive demand causes grounding problems.

---

## Preliminary Results

The criterion-based analysis showed that level differentiation across the two experiments was **partial and uneven rather than uniformly strong**.

The clearest and most consistent differentiation was observed in:

- **Cognitive Demand**
- **Exercise Difficulty**
- **Self-Assessment Difficulty**

Weaker differentiation was observed in:

- **Vocabulary Complexity**
- **Explanation Depth**
- **Scaffolding Level**

The Basic packages were generally more clearly distinguishable from the higher-level packages.

The distinction between Intermediate and Advanced was less consistent, particularly in vocabulary, explanatory structure, and instructional support.

Some Advanced-level differences reflected more academically developed wording, longer formulations, or more demanding task instructions rather than a consistently distinct pedagogical treatment.

At the same time, the control criteria—Curriculum Grounding, Learning Objectives Coverage, and Scientific Core Consistency—remained stable across the final outputs, as intended by the experimental design.

The experiments therefore provide preliminary evidence that the Pedagogical Profile can influence some characteristics of generated educational content, particularly task-related cognitive demand, but the current profiles do not yet produce consistently distinct Basic, Intermediate, and Advanced packages across all predefined differentiation criteria.

---

## Grounding Observation

In both experiments, the Basic output was accepted without grounding revision, while the initial Intermediate and Advanced outputs required grounding-related revisions.

After revision, the higher-level packages retained more demanding learner activities while improving adherence to the fixed curriculum knowledge boundary.

This recurring pattern suggests that curriculum grounding and pedagogical differentiation should be treated as related but distinct generation requirements.

The current experiments do not establish that increasing cognitive demand causes grounding problems.

---

## Cross-Experiment Analysis

The repository includes a separate cross-experiment analysis comparing the Mitosis and Meiosis experiments.

The analysis examines:

- consistency of the experimental procedure;
- control and differentiation criteria;
- level differentiation across the two curriculum sections;
- grounding-related revision patterns;
- preservation of the scientific core;
- recurring strengths and weaknesses; and
- preliminary design implications.

See:

- `cross-experiment-analysis/comparison.md`
- `cross-experiment-analysis/preliminary-findings.md`

---

## How to Navigate the Repository

For each experiment, the recommended reading order is:

1. **01-source-input**  
   Review the curriculum source and the selected experimental scope.

2. **02-experiment-setup**  
   Review the Learning Objectives, Pedagogical Profiles, Fixed Retrieved Curriculum Knowledge, Output Structure, and experimental parameters.

3. **03-prompts**  
   Review the prompts used for Basic, Intermediate, and Advanced generation, including revision prompts where applicable.

4. **04-outputs**  
   Review the generated educational packages. Initial and final versions are retained where grounding-related revisions were required.

5. **05-analysis**  
   Review the identified issues, revisions, and researcher-based comparison of the final learner-level outputs.

After reviewing both experiments, the `cross-experiment-analysis` folder provides the comparison and preliminary findings across Mitosis and Meiosis.

---

## Current Scope and Limitations

The experiments documented in this repository represent controlled proof-of-concept work.

At the current stage:

- A complete technical RAG pipeline with explicitly implemented embeddings and vector database retrieval has not been implemented in these experiments.
- Actual learner performance has not been tested.
- Initial learner-level classification based on learner performance has not been tested.
- Rule-based adaptive level progression has not yet been tested in these experiments.
- Learner profile updating has not been tested.
- Formal expert-based qualitative evaluation has not yet been conducted.
- A complete expert-driven DBR refinement cycle has not yet been conducted.
- Generalizability across other subjects, grades, curricula, learners, or LLM environments has not been established.

Therefore, the current experiments should be interpreted as preliminary testing of the **curriculum-grounded, level-aware content generation component** of the proposed framework.

---

## Design Implication

The repeated pattern across Mitosis and Meiosis indicates that the Pedagogical Profiles require further refinement.

In particular, the next iteration should define more observable and operational differences in:

- vocabulary and sentence complexity;
- depth of conceptual relationships;
- amount and type of scaffolding;
- learner independence;
- cognitive operations;
- exercise design; and
- self-assessment design.

The objective of this refinement is to improve differentiation across the three intended learner levels while maintaining the same curriculum knowledge boundary and scientific learning objectives.

The original experiments, prompts, and outputs will remain unchanged as historical experimental records. Any refined profiles and regenerated outputs should be documented as a new experimental iteration.

---

## Next Development Stage

The next experimental stage will extend the proof-of-concept toward the broader adaptive flow proposed in the research:

**Learner Assessment → Learner Level → Pedagogical Profile → Curriculum Retrieval → Level-Aware Generation → Assessment → Performance Analysis → Adaptive Recommendation → Profile Update**

Before making stronger claims about level-aware generation, the Pedagogical Profiles and generation prompts should be refined based on the findings from the current two experiments.

The next stage should distinguish clearly between components that are technically implemented and components that are functionally simulated within controlled testing.

Formal expert-based evaluation will remain a separate evaluation stage.

---

## Research Status

**Status:** Ongoing Master's Research – Controlled Proof-of-Concept and Refinement Stage
