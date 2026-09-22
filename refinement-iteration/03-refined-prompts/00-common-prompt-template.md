# Common Prompt Template

## Purpose

This template defines the common generation instructions that remain fixed across the Basic, Intermediate, and Advanced conditions in the refinement iteration.

The only learner-level variable is the Pedagogical Profile and its corresponding operational rules.

---

## Fixed Generation Inputs

The following inputs must remain identical across the three learner-level conditions:

### Selected Lesson

[Insert the selected lesson title]

### Learning Objectives

[Insert the same fixed Learning Objectives used across all three levels]

### Fixed Retrieved Curriculum Knowledge

[Insert the same Fixed Retrieved Curriculum Knowledge used across all three levels]

### Fixed Output Structure

Generate exactly four components:

1. Explanations
2. Key Vocabulary
3. Exercises
4. Self-Assessment Questions

---

## Common Generation Instructions

Generate an educational package for a Grade 8 learner using only the Fixed Retrieved Curriculum Knowledge provided in this prompt.

The generated package must address all stated Learning Objectives.

Follow the learner-level Pedagogical Profile provided in the level-specific section of the prompt.

The learner level must be created by changing the pedagogical treatment of the fixed curriculum knowledge, not by changing or expanding the scientific knowledge.

---

## Curriculum-Grounding Constraints

You must:

- Use only information contained in the Fixed Retrieved Curriculum Knowledge.
- Maintain the scientific meaning of the curriculum content.
- Address the same Learning Objectives across all learner levels.
- Keep the scientific core consistent across learner levels.
- Use only relationships that can be directly supported by the Fixed Retrieved Curriculum Knowledge.

You must not:

- introduce scientific facts outside the Fixed Retrieved Curriculum Knowledge;
- introduce higher-grade scientific content;
- add unsupported scientific mechanisms or causal explanations;
- create new scientific examples that require information outside the fixed knowledge;
- create hypothetical scientific scenarios that require external knowledge;
- add new numerical examples that are not supported by the fixed knowledge; or
- make the package more advanced by adding additional scientific content.

---

## Level-Differentiation Constraints

Level differentiation must be produced through the Pedagogical Profile.

Depending on the assigned learner level, differentiation may involve controlled changes in:

- vocabulary use;
- sentence complexity;
- explanation depth;
- concept load;
- concept relationships;
- scaffolding;
- learner independence;
- cognitive demand;
- exercise structure; and
- self-assessment design.

Increased text length alone does not constitute level differentiation.

Do not make a higher-level package more difficult merely by making sentences longer or using unnecessarily difficult wording.

---

## Output Requirements

Produce exactly the following four sections and no additional educational-content sections:

### 1. Explanations

Explain the lesson according to the assigned Pedagogical Profile while remaining within the Fixed Retrieved Curriculum Knowledge.

### 2. Key Vocabulary

Present the essential scientific vocabulary contained in the fixed curriculum knowledge according to the assigned learner-level rules.

Do not introduce new scientific terminology solely to increase difficulty.

### 3. Exercises

Generate exercises according to the cognitive demand, scaffolding, learner independence, and exercise-design rules of the assigned Pedagogical Profile.

All exercises must be answerable using only the Fixed Retrieved Curriculum Knowledge.

### 4. Self-Assessment Questions

Generate self-assessment questions according to the assigned Pedagogical Profile.

All questions must be answerable using only the Fixed Retrieved Curriculum Knowledge.

---

## Final Grounding Check

Before producing the final response, internally check that:

1. All Learning Objectives are addressed.
2. No scientific knowledge outside the Fixed Retrieved Curriculum Knowledge has been introduced.
3. The four required output components are present.
4. The assigned Pedagogical Profile has been followed.
5. Difficulty has been created through pedagogical treatment rather than additional scientific knowledge.
6. No unsupported mechanism, cause, example, hypothetical scientific scenario, or numerical case has been added.

If any generated content violates these constraints, revise it before providing the final output.

