# Preliminary Chunking Pilot Experiment

## Overview

This experiment provides a preliminary exploration of curriculum chunk granularity for the knowledge-grounded RAG component of the proposed framework.

The experiment uses the Mitosis section from the selected Palestinian Grade 8 Science curriculum case study.

The purpose is to explore how different concept-aware chunking granularities may affect the amount and organization of curriculum context available for answering different types of curriculum-based queries.

This is an exploratory experiment and is not intended to determine the final chunking strategy or evaluate the implemented RAG pipeline.

---

## Source Material

- Curriculum: Palestinian Curriculum
- Grade: Grade 8
- Subject: Science
- Lesson: Cell Division
- Selected Topic: Mitosis
- Source Pages: 26–27
- Language: Arabic

The experiment uses only curriculum content already prepared during the curriculum data preparation stage.

No external scientific knowledge was intentionally added to the experimental source variants.

---

## Experimental Variable

The experiment compares two representations of the same Mitosis curriculum content.

The primary variable is:

**Chunk granularity**

The scientific curriculum content is kept consistent across the two variants, while the organization of that content into conceptual units is changed.

### Variant A — Fine-Grained Concept-Aware Representation

The Mitosis content is divided into smaller conceptual units:

1. Interphase and Purpose
2. Prophase
3. Metaphase
4. Anaphase
5. Telophase and Cytokinesis

### Variant B — Broader Concept-Aware Representation

The same content is organized into broader units:

1. Interphase and Purpose
2. Mitosis Stages

The second unit preserves the four Mitosis stages and cytokinesis together as a broader coherent context.

---

## Test Environment

The two variants were explored separately using Google NotebookLM.

A separate notebook was used for each variant to avoid exposing the system to both representations during the same test.

NotebookLM was used only as a preliminary exploratory environment.

Because its internal chunking and retrieval mechanisms are not controlled by this experiment, the results cannot be interpreted as a controlled evaluation of the final RAG retrieval strategy.

A later evaluation within the implemented RAG pipeline will be required to compare chunking alternatives under controlled retrieval settings.

---

## Controlled Query Set

The same five queries were submitted to both variants in the same order:

1. ما هو الطور البيني وما الذي يحدث فيه؟
2. ماذا يحدث في الدور الانفصالي؟
3. اشرح مراحل الانقسام المتساوي.
4. كيف تنتقل الخلية من ترتيب الكروموسومات إلى تكوين خليتين متماثلتين؟
5. ما نتيجة الانقسام المتساوي وما عدد الكروموسومات في الخلايا الناتجة؟

The query set was designed to include both narrow and broader information needs.

The questions include:

- a specific preparatory-stage query;
- a specific Mitosis-stage query;
- a complete-stage query;
- a relational/sequential query;
- an outcome-focused query.

---

## Common Instruction

The same instruction was used for both variants:

> Answer each query using only the provided source.
> Do not add external scientific information.
> For each answer:
> 1. Provide the answer.
> 2. Identify the source section or chunk used.
> 3. State whether the retrieved source context was sufficient to answer the query completely.

The instruction and query set were kept consistent to support comparison between the two experimental conditions.

---

## Comparison Dimensions

The exploratory results are examined using the following dimensions:

- relevance of the identified source context;
- completeness of the context used for answering;
- amount of additional context associated with narrow queries;
- ability to support multi-concept or sequential questions;
- consistency with the provided curriculum source.

The experiment also distinguishes between observations about source context and observations about the generated answer.

This distinction is important because differences in generated responses may result from LLM generation behavior rather than chunk granularity alone.

---

## Interpretation Boundary

This pilot does not establish that either fine-grained or broader chunking is superior.

NotebookLM may internally process and segment uploaded sources independently of the explicit chunk labels used in the experimental files.

Therefore, references to the experimental chunk labels indicate the source sections identified in the generated responses, but they do not provide direct access to NotebookLM's internal retrieval process.

The experiment is consequently treated as a preliminary exploration that informs later controlled RAG implementation and retrieval testing.

---

## Next Steps

The next steps are to:

1. preserve the exact source representation used for Variant A;
2. preserve the exact source representation used for Variant B;
3. preserve the outputs produced for both variants;
4. compare the observed behavior across the common query set;
5. use these observations to inform the design of controlled chunking experiments in the implemented RAG pipeline.

The final chunking configuration will not be selected solely on the basis of this preliminary NotebookLM experiment.
