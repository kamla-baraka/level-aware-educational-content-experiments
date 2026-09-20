# Experiment Parameters and Variables

## Experiment

Experiment 2 – Meiosis

## Experimental Purpose

This controlled proof-of-concept experiment examined whether the same curriculum-grounded Meiosis knowledge could be presented as Basic, Intermediate, and Advanced educational packages by varying the Pedagogical Profile while keeping the main content-related variables fixed.

## Experimental Parameters

| Parameter / Variable | Setting | Role in the Experiment |
|---|---|---|
| Curriculum | Palestinian Grade 8 Science Curriculum | Controlled |
| Source Lesson | Cell Division (انقسام الخلايا) | Controlled |
| Selected Experimental Lesson | Meiosis (الانقسام المنصف) | Controlled |
| Source Format | 7-page PDF | Controlled |
| Generation Environment | Google NotebookLM | Controlled |
| Number of Learning Objectives | 5 | Controlled |
| Learning Objectives | Same five objectives across all levels | Controlled |
| Retrieved Curriculum Knowledge | Fixed before level-aware generation | Controlled |
| Knowledge Boundary | Curriculum-grounded Meiosis knowledge only; no intended external or higher-grade scientific content | Controlled |
| Learner Levels | Basic, Intermediate, Advanced | Experimental conditions |
| Pedagogical Profile | Different fixed profile for each learner level | Intentionally varied |
| Basic Cognitive Demand | Remember and Understand | Level-specific setting |
| Intermediate Cognitive Demand | Understand and Apply | Level-specific setting |
| Advanced Cognitive Demand | Apply and Analyze | Level-specific setting |
| Output Structure | Explanations, Key Vocabulary, Exercises, Self-Assessment Questions | Controlled |
| Number of Output Components | 4 | Controlled |
| Initial Generation | Generated separately for each learner level | Experimental procedure |
| Revision | Applied when grounding or content-boundary issues were identified | Refinement step |
| Comparison | Researcher-based comparison across the three generated levels | Analysis |
| Expert Evaluation | Not conducted in this proof-of-concept experiment | Outside current experiment |
| Learner Testing | Not conducted | Outside current experiment |
| Full Technical RAG Implementation | Not implemented | Outside current experiment |

## Variable Intentionally Changed

The main variable intentionally changed across the three generation conditions was the **Pedagogical Profile**.

The Pedagogical Profile controlled:

- Vocabulary complexity
- Explanation depth
- Scaffolding level
- Concept load
- Example style
- Cognitive demand
- Learner independence
- Assessment focus and difficulty

## Variables Held Fixed

The following variables were held constant across Basic, Intermediate, and Advanced generation:

- Curriculum source
- Selected Meiosis lesson
- Experimental scope
- Five Learning Objectives
- Fixed Retrieved Curriculum Knowledge
- Knowledge boundary
- Generation environment
- Four-component Output Structure

## Observed Output Characteristics

The final generated outputs were compared using the following characteristics:

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

## Revision Conditions

The Basic package was accepted without a grounding revision.

The initial Intermediate package required revision after researcher review identified grounding-related issues, including:

- Hypothetical chromosome counts not contained in the fixed knowledge
- Additional causal explanation concerning chromosome stability
- Terminology not fully aligned with the fixed quantitative progression

The initial Advanced package also required revision after researcher review identified:

- A hypothetical chromosome-reduction failure scenario
- Combined chromosome calculations across the four gametes
- Additional causal interpretations beyond the fixed knowledge

The revised Intermediate and Advanced packages were retained as the final versions for comparative analysis.

## Experimental Boundary

This experiment represents a controlled proof-of-concept of the curriculum-grounded, level-aware content generation component.

It does not represent:

- Validation of the complete proposed framework
- Learner-effectiveness testing
- Formal expert evaluation
- Implementation or validation of a complete technical RAG pipeline
- Evidence of generalizability across other lessons, subjects, curricula, or LLM environments
