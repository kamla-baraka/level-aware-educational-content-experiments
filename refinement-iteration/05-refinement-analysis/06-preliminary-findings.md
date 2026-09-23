# Preliminary Findings from the Pedagogical Profile Refinement Iteration

## 1. Purpose of the Refinement Iteration

The refinement iteration was conducted after the criterion-based re-analysis of the original Mitosis and Meiosis experiments showed that level differentiation was partial and uneven.

In the original experiments, the clearest differences were observed in cognitive demand, exercise difficulty, and self-assessment difficulty. However, vocabulary complexity, explanation depth, and scaffolding showed weaker differentiation, particularly between the Intermediate and Advanced conditions.

The pedagogical profiles were therefore operationalized to make the intended differences more observable and controllable.

The refinement did not change the curriculum source, scientific scope, or general output structure.

---

## 2. Refined Pedagogical Profiles

The refined profiles operationalized learner-level differences through observable instructional characteristics.

### Basic

The Basic condition emphasized:

- simple and familiar vocabulary;
- short and direct explanations;
- one concept or direct relationship at a time;
- high scaffolding;
- limited conceptual load;
- low learner independence;
- Remember and Understand;
- guided recall and simple understanding tasks.

### Intermediate

The Intermediate condition emphasized:

- standard Grade 8 curriculum terminology;
- explicit connections between related concepts;
- moderate scaffolding;
- moderate learner independence;
- processing of up to two closely related ideas;
- Understand and Apply;
- guided comparison, sequencing, classification, correction, and simple application.

### Advanced

The Advanced condition emphasized:

- full Grade 8 curriculum terminology;
- integration of multiple curriculum concepts;
- lower scaffolding;
- greater learner independence;
- multi-step reasoning;
- Apply and Analyze;
- relationship analysis;
- evaluation and correction;
- evidence-based justification using only the fixed curriculum knowledge.

Importantly, Advanced was defined as deeper processing of the same curriculum knowledge rather than the introduction of additional scientific knowledge.

---

## 3. Controlled Replication

The refined profiles were first applied to the Meiosis lesson.

After completing and analyzing the refined Meiosis experiment, the profiles were kept unchanged and applied to the Mitosis lesson.

This allowed the second experiment to function as a controlled replication of the pedagogical-profile conditions using different lesson content from the same selected Grade 8 science chapter.

The same general experimental principles were maintained:

- official curriculum source;
- fixed learning objectives for each lesson;
- fixed curriculum knowledge;
- strict knowledge boundary;
- Basic, Intermediate, and Advanced conditions;
- the same four output components;
- the same ten evaluation criteria.

---

## 4. Main Cross-Experiment Result

Across the refined Meiosis and Mitosis experiments, a similar pattern of level differentiation was observed.

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
| Overall Differentiation | Clearer and more systematic | Clearer and more systematic |

The strongest and most consistent distinctions across the two refined lesson conditions were observed in:

- explanation depth;
- scaffolding;
- cognitive demand;
- exercise difficulty;
- self-assessment difficulty.

Vocabulary complexity remained more moderately differentiated.

---

## 5. Original vs Refined Pattern

The original experiments showed partial and uneven differentiation.

After operationalizing the pedagogical profiles, the following general pattern was observed across the two lessons:

| Dimension | Original Experiments | Refined Experiments |
|---|---|---|
| Vocabulary Complexity | Limited | Moderate |
| Explanation Depth | Limited–Moderate / Moderate | Clear |
| Scaffolding Level | Moderate / Partial | Clear |
| Cognitive Demand | Clear | Clear |
| Exercise Difficulty | Clear | Clear |
| Self-Assessment Difficulty | Clear | Clear |

The most observable improvements occurred in explanation depth and scaffolding.

Vocabulary differentiation also improved, but remained more moderate because the same Grade 8 curriculum terminology was intentionally preserved across learner levels.

Cognitive demand, exercise difficulty, and self-assessment difficulty were already relatively strong in the original experiments and remained strong after refinement.

---

## 6. Grounding Observation

A repeated observation emerged during the generation process.

As the required level of integration and analytical reasoning increased, particularly in the Advanced condition, the model sometimes introduced information or relationships beyond the predefined curriculum boundary.

Examples included:

- unsupported causal explanations;
- hypothetical scenarios;
- broader biological interpretations;
- unsupported numerical or structural deductions.

Targeted grounding revisions were therefore required to remove these expansions while preserving the intended cognitive level.

This observation suggests that level-aware pedagogical control alone is not sufficient for curriculum-grounded generation.

The framework should maintain a distinction between:

**Pedagogical Profile → controls HOW the knowledge is processed and presented.**

**Grounding / Retrieval Control → controls WHAT knowledge may be used.**

These components should interact during generation.

This is a preliminary design observation from the controlled experiments and should not be interpreted as a general causal finding.

---

## 7. Implication for the Proposed Framework

The refined profiles provide working operational definitions for the Basic, Intermediate, and Advanced learner-level conditions in the next framework-design stage.

The proof-of-concept experiments suggest that learner-level differentiation should not be implemented merely by instructing an LLM to generate "easy," "medium," or "advanced" content.

Instead, each pedagogical profile should specify observable generation constraints such as:

- vocabulary treatment;
- number of concepts processed together;
- explanation depth;
- scaffolding;
- learner independence;
- cognitive operation;
- exercise structure;
- self-assessment demand;
- degree of integration and justification.

These profiles should be combined with curriculum-grounded retrieval and explicit knowledge-boundary control.

---

## 8. Relationship to the Conceptual Framework

The refinement findings support the following conceptual flow:

**Learner Assessment → Learner Level → Pedagogical Profile → Curriculum Retrieval → Level-Aware Generation → Assessment → Profile Update**

Within this flow:

1. **Learner Assessment** provides evidence about learner performance.
2. **Learner Level** represents the current Basic, Intermediate, or Advanced classification/recommendation.
3. **Pedagogical Profile** defines how educational content should be presented for that level.
4. **Curriculum Retrieval** supplies relevant knowledge from the approved curriculum source.
5. **Level-Aware Generation** combines retrieved knowledge with the pedagogical profile.
6. **Assessment** evaluates learner performance on the generated package.
7. **Profile Update** supports a rule-based recommendation to remain at the current level, receive reinforcement, or progress according to predefined indicators.

The current proof-of-concept experiments primarily examined the interaction between curriculum-grounded knowledge and level-aware generation.

They did not implement the complete end-to-end framework.

---

## 9. What Has and Has Not Been Demonstrated

### The Current Experiments Provide Preliminary Evidence That:

- operational pedagogical profiles can produce observable differences across Basic, Intermediate, and Advanced generated packages;
- the same refined profiles produced a similar differentiation pattern across two controlled lesson conditions;
- differentiation can be achieved while maintaining substantially the same scientific core;
- explicit grounding constraints remain necessary when cognitive complexity increases.

### The Current Experiments Do Not Demonstrate:

- educational effectiveness;
- improved learner achievement;
- accurate real-world learner classification;
- effectiveness of adaptive progression;
- expert validation;
- generalizability across subjects, chapters, or grade levels;
- performance of a fully implemented technical RAG pipeline;
- validation of the complete proposed framework.

---

## 10. Limitations

The refinement iteration has several limitations.

First, only two lessons from one selected Grade 8 science chapter were examined.

Second, the analysis was conducted by the researcher and has not yet been replaced by formal expert evaluation.

Third, the experiments evaluated generated educational artifacts rather than actual learner performance.

Fourth, NotebookLM was used as a controlled proof-of-concept environment, rather than implementing an independent technical RAG pipeline with explicitly configured chunking, embeddings, vector storage, retrieval, and similarity search.

Fifth, the learner-assessment and adaptive-progression components of the proposed framework were not implemented in these experiments.

---

## 11. Preliminary Conclusion

The pedagogical profile refinement iteration produced a clearer and more systematic pattern of level differentiation across the two controlled lesson conditions than was observed in the original experiments.

The clearest distinctions were observed in explanation depth, scaffolding, cognitive demand, exercise difficulty, and self-assessment difficulty.

Vocabulary complexity remained more moderately differentiated because the same curriculum terminology was intentionally preserved across levels.

The repeated pattern across Meiosis and Mitosis provides preliminary proof-of-concept evidence supporting the use of operational pedagogical profiles within the proposed level-aware generation component.

At the same time, the grounding revisions required during generation indicate that pedagogical complexity must remain constrained by curriculum-grounding mechanisms.

These findings support proceeding to the next framework-development stage while retaining the refined pedagogical profiles as working design requirements.

They do not constitute validation of the complete framework or evidence of educational effectiveness.

---

## 12. Next Stage

The next stage is to move from the isolated level-aware generation proof-of-concept toward the proposed framework design and controlled implementation.

The next work should therefore focus on translating the conceptual components into explicit technical and procedural modules, including:

- curriculum knowledge-base preparation;
- curriculum chunking and representation;
- embedding and retrieval mechanisms;
- RAG integration;
- refined pedagogical-profile implementation;
- level-aware prompting;
- structured educational-package generation;
- learner assessment logic;
- rule-based level recommendation and progression;
- controlled testing;
- preparation for expert-based qualitative evaluation.
