# Level-Aware Educational Content Generation Experiments

## Overview

This repository documents a series of controlled proof-of-concept experiments conducted as part of a Master's research project on curriculum-grounded, level-aware educational content generation using Large Language Models (LLMs).

The experiments investigate whether the same official curriculum knowledge can be transformed into educational packages for three intended learner levels:

- Basic
- Intermediate
- Advanced

The experiments focus on how pedagogical treatment can vary across learner levels while maintaining the same curriculum knowledge boundary.

The work also examines the interaction between:

- Curriculum grounding
- Pedagogical profiles
- Explanation depth
- Scaffolding
- Cognitive demand
- Exercise difficulty
- Self-assessment difficulty

The experiments represent an exploratory and iterative stage of the proposed framework and should not be interpreted as validation of the complete framework or evidence of educational effectiveness.

---

## Research Context

The broader research proposes a knowledge-grounded LLM framework for generating curriculum-aligned, level-aware self-learning educational packages.

The intended conceptual flow is:

**Learner Assessment → Learner Level → Pedagogical Profile → Curriculum Retrieval → Level-Aware Generation → Assessment → Profile Update**

The current repository primarily investigates the interaction between:

**Curriculum-Grounded Knowledge + Pedagogical Profile → Level-Aware Educational Content**

The complete learner-assessment, adaptive-progression, and technical RAG components are outside the scope of the current proof-of-concept experiments.

---

## Case Study

The controlled experiments use a selected chapter from the official Palestinian Grade 8 Science curriculum.

Two lessons from the same chapter were examined:

1. **Mitosis**
2. **Meiosis**

For each lesson, educational packages were generated for:

- Basic learners
- Intermediate learners
- Advanced learners

The scientific content boundary was controlled so that higher learner levels were not intentionally given additional scientific knowledge.

Instead, differentiation was expected to occur through the pedagogical treatment of the same curriculum knowledge.

---

## Educational Package Structure

Each generated package contains exactly four components:

1. Explanations
2. Key Vocabulary
3. Exercises
4. Self-Assessment Questions

This structure was maintained across learner levels and experiments.

---

## Evaluation Criteria

The generated outputs were compared using ten predefined criteria:

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

The criteria were conceptually divided into two groups.

### Control Criteria

The following criteria were expected to remain stable across learner levels:

- Curriculum Grounding
- Learning Objectives Coverage
- Scientific Core Consistency

### Differentiation Criteria

The following criteria were expected to vary according to the pedagogical profile:

- Vocabulary Complexity
- Explanation Depth
- Scaffolding Level
- Cognitive Demand
- Exercise Difficulty
- Self-Assessment Difficulty

Text length alone was not considered sufficient evidence of successful level differentiation.

---

# Experimental Development

## Stage 1: Original Experiments

The first proof-of-concept experiments were conducted on:

- Mitosis
- Meiosis

The same general Basic, Intermediate, and Advanced learner-level definitions were applied.

The generated outputs were then reviewed using the predefined criteria.

### Original Findings

The original experiments showed **partial and uneven level differentiation**.

The clearest differences were observed in:

- Cognitive demand
- Exercise difficulty
- Self-assessment difficulty

Weaker differentiation was observed in:

- Vocabulary complexity
- Explanation depth
- Scaffolding

The distinction between Basic and the higher levels was generally more visible than the distinction between Intermediate and Advanced.

Some differences between Intermediate and Advanced appeared to reflect increased linguistic elaboration rather than consistently distinct pedagogical treatment.

---

## Stage 2: Pedagogical Profile Refinement

Based on the criterion-based analysis of the original experiments, the pedagogical profiles were operationalized.

The refinement focused particularly on dimensions that showed weaker differentiation:

- Vocabulary treatment
- Explanation depth
- Scaffolding
- Learner independence
- Number of concepts processed together
- Relationship integration

The refined profiles also defined more explicit cognitive and task requirements.

### Basic Profile

The refined Basic condition emphasizes:

- Simple and familiar vocabulary
- Short and direct explanations
- One concept or direct relationship at a time
- High scaffolding
- Limited conceptual load
- Low learner independence
- Remember and Understand
- Highly guided tasks

### Intermediate Profile

The refined Intermediate condition emphasizes:

- Standard Grade 8 curriculum terminology
- Explicit relationships between related concepts
- Moderate scaffolding
- Moderate learner independence
- Processing of closely related concepts
- Understand and Apply
- Guided comparison, sequencing, classification, correction, and simple application

### Advanced Profile

The refined Advanced condition emphasizes:

- Full Grade 8 curriculum terminology
- Integration of multiple curriculum concepts
- Lower scaffolding
- Greater learner independence
- Multi-step reasoning
- Apply and Analyze
- Relationship analysis
- Evaluation and correction
- Evidence-based justification

Advanced-level generation is defined as deeper processing of the **same curriculum knowledge**, rather than the introduction of additional scientific content.

---

## Stage 3: Refined Meiosis Experiment

The refined pedagogical profiles were first applied to the Meiosis lesson.

The same official curriculum source, fixed learning objectives, fixed curriculum knowledge, output structure, and strict knowledge boundary were maintained.

Where the generated content extended beyond the predefined curriculum boundary, targeted grounding revisions were applied.

After these revisions, the final outputs showed the following pattern:

| Criterion | Refined Meiosis |
|---|---|
| Curriculum Grounding | Control maintained |
| Learning Objectives Coverage | Control maintained |
| Vocabulary Complexity | Moderate differentiation |
| Explanation Depth | Clear differentiation |
| Scaffolding Level | Clear differentiation |
| Cognitive Demand | Clear differentiation |
| Exercise Difficulty | Clear differentiation |
| Self-Assessment Difficulty | Clear differentiation |
| Scientific Core Consistency | Control maintained |
| Overall Level Differentiation | Clearer and more systematic |

The strongest distinctions were observed in explanation depth, scaffolding, cognitive demand, exercise difficulty, and self-assessment difficulty.

Vocabulary complexity showed a more moderate distinction because the same Grade 8 curriculum terminology was intentionally maintained across the three learner levels.

---

## Stage 4: Refined Mitosis Replication

After completing the refined Meiosis experiment, the refined pedagogical profiles were kept unchanged and applied to the Mitosis lesson.

This allowed the Mitosis experiment to function as a controlled replication of the refined pedagogical-profile conditions using different lesson content from the same curriculum chapter.

The same general experimental controls were maintained:

- Official curriculum source
- Fixed Mitosis learning objectives
- Fixed curriculum knowledge
- Strict knowledge boundary
- Same refined pedagogical profiles
- Same four output components
- Same ten evaluation criteria

After targeted grounding revisions, the refined Mitosis experiment showed the following pattern:

| Criterion | Refined Mitosis |
|---|---|
| Curriculum Grounding | Control maintained |
| Learning Objectives Coverage | Control maintained |
| Vocabulary Complexity | Moderate differentiation |
| Explanation Depth | Clear differentiation |
| Scaffolding Level | Clear differentiation |
| Cognitive Demand | Clear differentiation |
| Exercise Difficulty | Clear differentiation |
| Self-Assessment Difficulty | Clear differentiation |
| Scientific Core Consistency | Control maintained |
| Overall Level Differentiation | Clearer and more systematic |

The refined Mitosis condition therefore showed a pattern similar to that observed in the refined Meiosis experiment.

---

# Cross-Experiment Findings

Across the refined Meiosis and Mitosis experiments, a similar differentiation pattern was observed.

| Criterion | Refined Meiosis | Refined Mitosis |
|---|---|---|
| Curriculum Grounding | Control maintained | Control maintained |
| Learning Objectives Coverage | Control maintained | Control maintained |
| Vocabulary Complexity | Moderate | Moderate |
| Explanation Depth | Clear | Clear |
| Scaffolding Level | Clear | Clear |
| Cognitive Demand | Clear | Clear |
| Exercise Difficulty | Clear | Clear |
| Self-Assessment Difficulty | Clear | Clear |
| Scientific Core Consistency | Control maintained | Control maintained |
| Overall Level Differentiation | Clearer and more systematic | Clearer and more systematic |

The strongest and most consistent distinctions across the two refined lesson conditions were observed in:

- Explanation depth
- Scaffolding
- Cognitive demand
- Exercise difficulty
- Self-assessment difficulty

Vocabulary complexity showed a more moderate distinction because the same Grade 8 curriculum terminology was intentionally maintained across learner levels.

The control criteria remained substantially stable across the experiments.

The refined experiments therefore provide preliminary proof-of-concept evidence that operational pedagogical profiles can produce observable learner-level differences while maintaining the same scientific core.

These observations do not constitute validation of the complete framework or evidence of educational effectiveness.

---

# Original vs Refined Pattern

The original experiments showed partial and uneven differentiation.

After operationalizing the pedagogical profiles, a clearer and more systematic pattern was observed across both refined lesson conditions.

| Dimension | Original Experiments | Refined Experiments |
|---|---|---|
| Vocabulary Complexity | Limited | Moderate |
| Explanation Depth | Limited–Moderate / Moderate | Clear |
| Scaffolding Level | Moderate / Partial | Clear |
| Cognitive Demand | Clear | Clear |
| Exercise Difficulty | Clear | Clear |
| Self-Assessment Difficulty | Clear | Clear |

The most observable changes occurred in:

- Explanation depth
- Scaffolding

Vocabulary differentiation also became more visible but remained moderate.

Cognitive demand, exercise difficulty, and self-assessment difficulty were already relatively strong in the original experiments and remained strong after refinement.

---

# Grounding Observation

An important observation emerged repeatedly during the experiments.

As the Advanced condition required greater integration and analytical reasoning, the model sometimes introduced relationships, causal interpretations, hypothetical situations, or deductions beyond the predefined curriculum boundary.

Examples included:

- Unsupported causal explanations
- Hypothetical scenarios
- Broader biological interpretations
- Unsupported numerical or structural deductions

Targeted grounding revisions were required to remove these expansions while preserving the intended Advanced cognitive structure.

This provides preliminary design evidence for treating pedagogical control and knowledge grounding as distinct but interacting functions:

**Pedagogical Profile → controls HOW the retrieved knowledge is processed and presented.**

**Grounding / Retrieval → controls WHAT knowledge may be used.**

The pedagogical profile therefore should not independently determine the scientific content available to the model.

Instead, the curriculum-grounding mechanism should provide and constrain the approved knowledge, while the pedagogical profile determines how that knowledge is transformed for the learner level.

This observation is preliminary and should not be interpreted as establishing a general causal relationship between cognitive complexity and grounding errors.

---

# Refined Pedagogical Profile Interpretation

The refinement experiments suggest that learner-level differentiation should not rely only on broad instructions such as:

- "Generate easy content"
- "Generate intermediate content"
- "Generate advanced content"

Instead, the learner-level profiles should define observable generation requirements.

These include:

- Vocabulary treatment
- Number of concepts processed together
- Explanation depth
- Relationship integration
- Scaffolding
- Learner independence
- Cognitive operation
- Exercise structure
- Self-assessment demand
- Degree of required justification

This operationalization allows the learner-level condition to influence the pedagogical treatment of curriculum knowledge without intentionally changing the scientific knowledge itself.

---

# Relationship to the Proposed Framework

The experimental findings support the following conceptual flow:

**Learner Assessment → Learner Level → Pedagogical Profile → Curriculum Retrieval → Level-Aware Generation → Assessment → Profile Update**

Within this flow:

1. **Learner Assessment** provides evidence about learner performance.
2. **Learner Level** represents the current Basic, Intermediate, or Advanced classification or recommendation.
3. **Pedagogical Profile** specifies how educational content should be presented for that learner level.
4. **Curriculum Retrieval** provides relevant knowledge from the approved curriculum source.
5. **Level-Aware Generation** combines retrieved curriculum knowledge with the selected pedagogical profile.
6. **Assessment** evaluates learner performance on the generated educational package.
7. **Profile Update** supports a rule-based recommendation to remain at the current level, receive reinforcement, or progress according to predefined performance indicators.

The current experiments primarily examine the relationship between curriculum-grounded knowledge and level-aware generation.

They do not implement the complete end-to-end framework.

---

# Repository Structure

```text
level-aware-educational-content-experiments/
│
├── README.md
│
├── experiment-01-mitosis/
│   ├── 01-source-input/
│   ├── 02-experiment-setup/
│   ├── 03-prompts/
│   ├── 04-outputs/
│   └── 05-analysis/
│
├── experiment-02-meiosis/
│   ├── 01-source-input/
│   ├── 02-experiment-setup/
│   ├── 03-prompts/
│   ├── 04-outputs/
│   └── 05-analysis/
│
├── cross-experiment-analysis/
│   ├── comparison.md
│   └── preliminary-findings.md
│
└── refinement-iteration/
    ├── 01-refinement-rationale.md
    ├── 02-refined-pedagogical-profiles.md
    │
    ├── 03-refined-prompts/
    │   ├── 00-common-prompt-template.md
    │   ├── 01-basic-refined-prompt.md
    │   ├── 02-intermediate-refined-prompt.md
    │   ├── 03-advanced-refined-prompt.md
    │   └── 04-experimental-control-check.md
    │
    ├── 04-refined-outputs/
    │   ├── 01-basic-initial-output.md
    │   ├── 02-basic-final-output.md
    │   ├── 03-intermediate-initial-output.md
    │   ├── 04-intermediate-final-output.md
    │   ├── 05-advanced-initial-output.md
    │   └── 06-advanced-final-output.md
    │
    └── 05-refinement-analysis/
        ├── 01-refined-meiosis-comparison.md
        ├── 02-original-vs-refined-meiosis.md
        ├── 03-refined-mitosis-comparison.md
        ├── 04-original-vs-refined-mitosis.md
        ├── 05-refined-cross-experiment-comparison.md
        └── 06-preliminary-findings.md
```

> **Note:** The repository structure may continue to expand as the framework implementation stage progresses.

---

# Methodological Traceability

The original experimental records are retained as historical records of the initial proof-of-concept experiments.

The refinement iteration is documented separately rather than replacing the original prompts, outputs, or analyses.

This provides traceability across the experimental development process:

**Initial Generation → Criterion-Based Analysis → Pedagogical Profile Refinement → Controlled Re-Generation → Original-vs-Refined Comparison → Cross-Experiment Analysis**

Where grounding issues occurred, both initial and revised outputs were retained when relevant.

This allows the repository to document not only the accepted final outputs but also the refinement decisions that occurred during the experimental process.

---

# What the Current Experiments Provide

The current experiments provide preliminary evidence that:

- Operational pedagogical profiles can produce observable differences across Basic, Intermediate, and Advanced generated educational packages.
- The same refined pedagogical profiles produced a similar differentiation pattern across two controlled lesson conditions.
- Level differentiation can be achieved while maintaining substantially the same scientific core.
- Explicit grounding constraints remain important as cognitive and analytical complexity increases.
- Explanation depth and scaffolding became more clearly differentiated after profile operationalization.
- Cognitive demand, exercise difficulty, and self-assessment difficulty remained strong differentiation dimensions across the experiments.

---

# What the Current Experiments Do Not Establish

The current experiments do not establish:

- Educational effectiveness
- Improved learner achievement
- Accurate real-world learner classification
- Effectiveness of adaptive learner progression
- Expert validation
- Generalizability across subjects, chapters, or grade levels
- Performance of a fully implemented technical RAG pipeline
- Validation of the complete proposed framework

These questions require subsequent framework implementation and evaluation stages.

---

# Limitations

The current experimental work has several limitations.

First, only two lessons from one selected Grade 8 Science chapter were examined.

Second, the comparative analysis was conducted by the researcher and has not yet been replaced by formal expert evaluation.

Third, the experiments evaluate generated educational artifacts rather than actual learner performance.

Fourth, NotebookLM was used as a controlled proof-of-concept environment rather than implementing an independent technical RAG pipeline with explicitly configured:

- Chunking
- Embeddings
- Vector storage
- Similarity search
- Retrieval

Therefore, the current NotebookLM experiments should not be interpreted as a complete technical implementation of the proposed RAG architecture.

Fifth, the learner-assessment and adaptive-progression components of the proposed framework were not implemented in these experiments.

---

# Preliminary Conclusion

The pedagogical-profile refinement iteration produced a clearer and more systematic pattern of learner-level differentiation across the two controlled lesson conditions than was observed in the original experiments.

The clearest distinctions were observed in:

- Explanation depth
- Scaffolding
- Cognitive demand
- Exercise difficulty
- Self-assessment difficulty

Vocabulary complexity remained more moderately differentiated because the same curriculum terminology was intentionally preserved across learner levels.

The repeated pattern across Meiosis and Mitosis provides preliminary proof-of-concept evidence supporting the use of operational pedagogical profiles within the proposed level-aware generation component.

At the same time, the grounding revisions required during generation indicate that pedagogical complexity should remain constrained by curriculum-grounding mechanisms.

These findings support proceeding to the next framework-development stage while retaining the refined pedagogical profiles as working design requirements.

They do not constitute validation of the complete framework or evidence of educational effectiveness.

---

# Next Stage

The next research stage moves from isolated level-aware generation experiments toward the controlled design and implementation of the proposed framework.

The next stage will focus on:

- Curriculum knowledge-base preparation
- Curriculum chunking and representation
- Embedding generation
- Vector storage
- Semantic retrieval
- RAG integration
- Implementation of the refined pedagogical profiles
- Level-aware prompting
- Structured educational-package generation
- Learner-assessment logic
- Rule-based learner-level recommendation and progression
- Controlled framework testing
- Preparation for expert-based qualitative evaluation

---

## Research Status

**Current Stage:** Pedagogical-profile refinement and controlled proof-of-concept experiments completed.

**Next Stage:** Framework design and controlled technical implementation.

The repository will continue to document experimental and implementation artifacts as the research progresses.
