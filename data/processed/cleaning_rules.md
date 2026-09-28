# Curriculum Text Cleaning and Structuring Rules

## Purpose

This document defines the rules used to transform the source-faithful machine-readable curriculum text into a cleaned and structured representation suitable for subsequent semantic processing and chunking.

The cleaning stage focuses on structural normalization and does not modify the intended scientific meaning of the curriculum content.

---

## Cleaning Rules

### CR1 — Preserve Curriculum Content

Preserve the curriculum content and intended scientific meaning.

Do not summarize, simplify, expand, or reinterpret the scientific content during cleaning.

### CR2 — Normalize Headings

Use consistent Markdown headings to represent:

- pages;
- lessons;
- activities;
- explanatory content;
- questions;
- procedures;
- figure information.

### CR3 — Separate Content Types

Separate structurally different curriculum elements where identifiable, including:

- Activity Text
- Activity Instructions
- Explanatory Content
- Questions
- Materials and Tools
- Procedures
- Figure Information

### CR4 — Normalize Lists

Represent questions, procedures, properties, and other list-like information using consistent Markdown numbered or bullet lists.

Structural conversion of continuous source text into lists is allowed when it does not change the source meaning.

### CR5 — Preserve Curriculum Terminology

Retain the terminology used in the curriculum.

Do not replace curriculum terminology with external or higher-level scientific terminology during cleaning.

### CR6 — Remove Extraction and Formatting Artifacts

Remove artifacts caused by PDF extraction or document formatting where they do not represent curriculum content.

Examples include:

- broken character ordering;
- unnecessary line breaks;
- duplicated formatting marks;
- extraction noise.

### CR7 — Preserve Numerical Information

Preserve curriculum numerical values and quantitative examples.

Do not introduce new numerical examples during cleaning.

### CR8 — Preserve Relevant Figure Information

Scientifically or educationally relevant information presented in figures may be represented in text when necessary to preserve the source information in machine-readable form.

Such information should be identified as Figure Information.

### CR9 — No External Knowledge

Do not add scientific explanations, examples, definitions, or interpretations from external sources.

The cleaned dataset must remain grounded in the selected curriculum material.

### CR10 — No Semantic Chunking

Do not divide the curriculum into retrieval chunks during the cleaning stage.

Semantic or concept-aware chunking is performed as a separate subsequent processing stage.

### CR11 — Preserve Activities and Questions

Retain curriculum activities and questions during cleaning.

Decisions about whether different content types should be included in retrieval will be addressed during later knowledge-base and chunking design.

### CR12 — Maintain Source Traceability

Maintain page-level traceability to the original curriculum source.

Page boundaries should remain explicitly represented in the cleaned dataset.

---

## Allowed Transformations

The following transformations are allowed during this stage:

- correcting extraction artifacts;
- normalizing Markdown structure;
- organizing headings;
- converting appropriate continuous text into structured lists;
- separating identifiable content types;
- representing relevant figure information in text;
- standardizing formatting.

---

## Prohibited Transformations

The following transformations are not allowed during this stage:

- adding external scientific knowledge;
- changing the scientific meaning;
- summarizing curriculum content;
- adapting content to Basic, Intermediate, or Advanced learner levels;
- adding new examples;
- generating new learning objectives;
- generating assessment questions;
- performing semantic chunking;
- generating embeddings;
- modifying content based on model knowledge.

---

## Output of the Cleaning Stage

The output of this stage is:

`cell_division_cleaned_ar.md`

This cleaned and structured curriculum representation will serve as the input to the subsequent semantic or concept-aware chunking stage.
