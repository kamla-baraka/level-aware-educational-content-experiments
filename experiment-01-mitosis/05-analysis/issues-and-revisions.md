# Issues and Revisions

## Experiment

Experiment 1 – Mitosis

## Purpose

This document records the grounding and content-boundary issues observed during the generation of the Basic, Intermediate, and Advanced Mitosis packages, together with the revisions applied during the proof-of-concept experiment.
## Revision Summary

| Learner Level | Initial Generation Status | Revision Required | Main Reason |
|---|---|---|---|
| Basic | Accepted | No | The generated package remained sufficiently aligned with the fixed curriculum knowledge and intended Basic pedagogical profile. |
| Intermediate | Revision required | Yes | Some content introduced ambiguity or explanatory assumptions beyond the fixed retrieved curriculum knowledge. |
| Advanced | Revision required | Yes | Several explanations, mechanisms, and hypothetical scenarios extended beyond the fixed retrieved curriculum knowledge boundary. |

## Basic Level

### Initial Review

The Basic package was accepted without a grounding revision.

The generated content maintained the intended characteristics of the Basic Pedagogical Profile, including:

- Simple and familiar language
- Short and clear explanations
- High scaffolding
- Limited concept load
- Cognitive demand focused mainly on Remember and Understand
- Direct exercises and self-assessment questions

The package addressed the five fixed learning objectives and remained sufficiently aligned with the fixed retrieved curriculum knowledge.

### Revision Decision

**No revision was required.**

The Basic output was therefore retained as the final Basic package.

---

## Intermediate Level

### Issues Observed in the Initial Generation

The initial Intermediate package showed the intended increase in cognitive demand, but several grounding-related issues were identified during researcher review.

The main issues included:

1. **Ambiguity between DNA duplication and chromosome number**

   An exercise introduced a hypothetical cell containing 24 chromosomes and asked about chromosome numbers after DNA duplication and about the number of separated sister chromatids.

   This created unnecessary ambiguity between:

   - DNA duplication
   - Chromosome duplication
   - Sister chromatids
   - Chromosome number

2. **Additional causal or mechanistic explanations**

   Some explanations went beyond the fixed retrieved curriculum knowledge by adding causal interpretations to curriculum facts.

   Examples included explanations concerning:

   - Why chromosomes align individually during metaphase
   - Why cytokinesis differs between animal and plant cells
   - The relationship between specific structural events and successful genetic distribution

3. **Knowledge-boundary expansion**

   The Intermediate package occasionally attempted to achieve a higher cognitive level by introducing additional scientific explanation rather than relying only on relationships, sequencing, comparison, and simple application of the fixed knowledge.

### Revision Applied

A grounding-focused revision prompt was used.

The revision instructed the model to:

- Preserve the Intermediate Pedagogical Profile.
- Preserve the five fixed learning objectives.
- Preserve the four fixed output components.
- Use only the previously fixed retrieved curriculum knowledge.
- Remove unsupported scientific properties, mechanisms, or assumptions.
- Revise the ambiguous exercise involving DNA duplication and chromosome number.
- Maintain Understand and Apply cognitive demand through sequencing, relationships, comparison, and simple application rather than through additional scientific knowledge.

### Result After Revision

The revised Intermediate package showed improved adherence to the fixed curriculum knowledge while maintaining meaningful differentiation from the Basic package.

The revised exercises emphasized:

- Sequencing
- Comparison
- Relationships between stages and structures
- Simple application of curriculum knowledge

The revised Intermediate output was accepted as the final Intermediate package.

---

## Advanced Level

### Issues Observed in the Initial Generation

The initial Advanced package demonstrated increased analytical demand, but it also showed the clearest expansion beyond the fixed curriculum knowledge boundary.

The main issues included:

1. **Unsupported biological mechanisms and structures**

   The generated package introduced information that was not part of the fixed retrieved knowledge.

   Examples included:

   - Additional explanation for why plant and animal cytokinesis differ
   - Reference to protein aggregates and absence of centrioles in the plant-cell comparison
   - Additional mechanistic explanations concerning chromosome movement and nuclear-envelope disappearance

2. **Unsupported causal explanations**

   Some curriculum events were connected through causal explanations that were not explicitly available in the fixed retrieved knowledge.

3. **Hypothetical scenarios requiring knowledge beyond the fixed boundary**

   Some Advanced exercises required the learner to reason about situations such as preventing spindle-fiber contraction.

   Although these questions increased cognitive demand, answering them could require assumptions or scientific knowledge beyond the fixed retrieved curriculum content.

4. **Internally inconsistent example**

   One self-assessment item referred to a liver cell in the context of a skin wound, creating an internal inconsistency in the application scenario.

### Revision Applied

A stricter grounding revision was applied while preserving the Advanced Pedagogical Profile.

The revision instructed the model to:

- Maintain Apply and Analyze cognitive demand.
- Use comparison, interpretation, prediction, justification, and relationships only when supported by the fixed retrieved knowledge.
- Remove unsupported biological mechanisms and structures.
- Remove unsupported explanations for differences between plant and animal cytokinesis.
- Avoid unsupported causal explanations.
- Use hypothetical scenarios only when their answers could be reasoned directly from the fixed knowledge.
- Correct internally inconsistent examples.
- Preserve the same curriculum source, lesson scope, learning objectives, retrieved knowledge, pedagogical profile, and four output components.

### Result After Revision

The revised Advanced package showed improved adherence to the fixed curriculum boundary while retaining higher cognitive demand than the Basic and Intermediate packages.

The Advanced level continued to emphasize:

- Integration of multiple curriculum concepts
- Comparison
- Interpretation
- Justification
- Drawing conclusions from the available curriculum knowledge
- Apply and Analyze cognitive demand

The revised Advanced output was accepted as the final Advanced package.

---

## Cross-Level Observation

Across the three generation conditions, the Basic package was accepted without grounding revision, while the initial Intermediate and Advanced packages required revision.

In this controlled experiment, grounding-related issues became more evident when the generated activities requested greater cognitive depth and more complex relationships.

This observation suggests that maintaining a strict curriculum boundary may become more challenging when higher cognitive-demand educational content is requested. However, this single experiment is insufficient to establish a causal relationship between learner level, cognitive demand, and grounding errors.

The revision process showed that stronger grounding instructions could reduce knowledge-boundary expansion while preserving the intended pedagogical differentiation.

## Interpretation Boundary

These observations represent researcher-based findings from a controlled proof-of-concept experiment.

They should not be interpreted as:

- Validation of the complete proposed framework
- Evidence of learner effectiveness
- Formal expert evaluation
- Evidence that higher cognitive demand necessarily causes grounding errors
- Evidence that the observed pattern will generalize to other lessons, subjects, curricula, or LLM environments
