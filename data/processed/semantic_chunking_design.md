# Semantic Chunking Design

## 1. Purpose

This document defines the initial semantic segmentation design for the selected Grade 8 Science curriculum material, Lesson 3: Cell Division (انقسام الخلايا).

The segmentation operationalizes the proposed methodology, which specifies a concept-aware semantic chunking strategy guided by:

- curriculum structure;
- learning objectives;
- topic boundaries;

with the aim of preserving contextual coherence.

This stage defines the initial semantic organization of the curriculum content. It does not determine the final chunk size, overlap settings, or embedding model. These will be examined later through preliminary retrieval experiments during implementation of the RAG pipeline.

---

## 2. Curriculum Source

- Curriculum: Palestinian Curriculum
- Grade: Grade 8
- Subject: Science
- Lesson: Lesson 3 – Cell Division (انقسام الخلايا)
- Selected Source Pages: 23–29
- Language: Arabic
- Source Type: Official Science Textbook

The cleaned and structured curriculum text is used as the source for the semantic segmentation.

No external scientific information is introduced during this stage.

---

## 3. Curriculum Structure

The selected curriculum material is organized around the following content structure:

1. **Chromosome Number in Living Organisms**
   - Activity 1: كائنات حية متنوعة
   - chromosome-number examples;
   - related questions.

2. **Cell Division Background and Preparation**
   - Activity 2: الخلايا تضاعف أعدادها;
   - need for new cells;
   - chromatin before cell division;
   - DNA and organelle duplication;
   - chromosome duplication.

3. **Chromosome Structure**
   - duplicated chromosome;
   - chromatids;
   - centromere;
   - Activity 3: تمثيل الكروموسوم.

4. **Types of Cells and Corresponding Division**
   - somatic cells and Mitosis;
   - reproductive cells and Meiosis.

5. **Mitosis**
   - interphase;
   - purpose and occurrence of Mitosis;
   - prophase;
   - metaphase;
   - anaphase;
   - telophase;
   - cytokinesis;
   - Activity 4 questions.

6. **Plant and Animal Cell Division**
   - Activity 5;
   - plant cell division;
   - animal cell division.

7. **Meiosis**
   - Activity 6;
   - Meiosis outcome;
   - number of resulting cells;
   - chromosome number;
   - gametes;
   - numerical representation of chromosome number.

8. **Chromosome Number Changes and Down Syndrome**
   - chromosome-number change;
   - Palestinian success story presented in the curriculum;
   - Down syndrome;
   - characteristics presented in the curriculum;
   - Activity 7;
   - chromosome 21 explanation.

---

## 4. Relevant Curriculum Learning Objective

The curriculum unit containing the selected lesson provides unit-level learning objectives.

The learning objective directly relevant to the selected Cell Division content is:

> المقارنة بين نواتج الانقسام المتساوي والانقسام المنصف بالرسم.

This objective is treated as a **relevant unit-level learning objective**, rather than as a lesson-specific objective, because it is presented at the unit level in the official curriculum.

The remaining unit-level objectives relate to other content within the unit and are not used as direct guides for segmentation of the selected Cell Division material.

No additional lesson-specific learning objectives are inferred or introduced during this stage.

---

## 5. Topic Boundaries

Based on the curriculum structure and the selected content, the following topic boundaries were identified:

### T1 — Chromosome Number in Living Organisms

**Source page:** 23

Covers chromosome-number examples for different organisms and the associated curriculum questions.

### T2 — Cell Division and Preparation for Division

**Source page:** 24

Covers the need for new cells, cell division, chromatin before division, and duplication of DNA and organelles.

### T3 — Duplicated Chromosome Structure

**Source page:** 25

Covers chromatids, the centromere, and the chromosome representation activity.

### T4 — Somatic and Reproductive Cells

**Source pages:** 25–26

Covers the distinction between somatic and reproductive cells and their association with Mitosis and Meiosis.

### T5 — Mitosis

**Source pages:** 26–27

Covers interphase, the purpose and occurrence of Mitosis, the stages of Mitosis, cytokinesis, and the associated questions.

### T6 — Plant and Animal Cell Division

**Source page:** 27

Covers the curriculum comparison between plant and animal cell division.

### T7 — Meiosis

**Source page:** 28

Covers the curriculum explanation of Meiosis, its resulting cells, chromosome number, gametes, and the numerical example.

### T8 — Chromosome Number Changes and Down Syndrome

**Source pages:** 28–29

Covers chromosome-number change, the curriculum context related to Down syndrome, and the chromosome 21 explanation.

---

## 6. Initial Semantic Segmentation

Based on the curriculum structure, relevant unit-level learning objective, and topic boundaries, the selected curriculum content is initially segmented into the following semantic units.

### C01 — Chromosome Numbers in Living Organisms

**Source page:** 23

Includes:

- Activity 1;
- chromosome-number examples;
- associated questions.

### C02 — Cell Division and Preparation

**Source page:** 24

Includes:

- Activity 2;
- associated questions;
- need for new cells;
- chromatin before cell division;
- DNA and organelle duplication;
- chromosome-duplication figure information.

### C03 — Duplicated Chromosome Structure

**Source page:** 25

Includes:

- duplicated chromosome structure;
- chromatids;
- centromere;
- Activity 3;
- associated questions.

### C04 — Somatic and Reproductive Cells

**Source pages:** 25–26

Includes:

- somatic cells;
- their association with Mitosis;
- reproductive cells;
- their association with Meiosis.

This semantic unit crosses a page boundary because the two cell types form a connected curriculum concept.

### C05 — Interphase and Purpose of Mitosis

**Source page:** 26

Includes:

- interphase;
- cell growth;
- DNA duplication during interphase;
- occurrence and purpose of Mitosis.

### C06 — Mitosis Stages

**Source page:** 26

Includes:

- prophase;
- metaphase;
- anaphase;
- telophase;
- cytokinesis.

The stages are initially retained as one connected sequence. This does not establish that this granularity is the final retrieval configuration.

### C07 — Mitosis Questions

**Source page:** 27

Includes the questions associated with Activity 4 and the Mitosis content presented on the preceding page.

### C08 — Plant and Animal Cell Division

**Source page:** 27

Includes:

- Activity 5;
- plant cell division figure information;
- animal cell division figure information.

### C09 — Meiosis

**Source page:** 28

Includes:

- Activity 6;
- associated questions;
- explanatory content about Meiosis;
- resulting cells and chromosome number;
- gametes;
- numerical model:
  - one cell with 46 chromosomes;
  - two cells with 23 chromosomes each;
  - four cells with 23 chromosomes each.

### C10 — Chromosome Number Change and Curriculum Context

**Source page:** 28

Includes:

- the Palestinian success story presented in the curriculum;
- stability of chromosome number;
- change in chromosome number;
- the curriculum statement relating chromosome-number change to mutation.

### C11 — Down Syndrome and Chromosome 21

**Source page:** 29

Includes:

- the curriculum explanation of Down syndrome;
- chromosome number 47;
- characteristics listed in the curriculum;
- associated questions;
- Activity 7;
- chromosome 21 explanation;
- numerical relationship:
  - 24 + 23 → 47.

---

## 7. Segmentation Considerations

The initial segmentation follows conceptual and curriculum boundaries rather than treating each textbook page as an independent semantic unit.

Some concepts cross page boundaries when their curriculum meaning continues across adjacent pages. For example, the discussion of somatic and reproductive cells extends across pages 25 and 26 and is therefore retained as a connected semantic unit.

Likewise, the stages of Mitosis are initially retained as a connected sequence rather than automatically separating every stage into an independent chunk.

This decision does not establish a final preferred chunk granularity.

The previous preliminary chunking exploration indicated a potential trade-off between fine-grained and broader concept-aware representations. Therefore, alternative chunk configurations remain subject to later controlled retrieval testing.

---

## 8. Current Scope and Limitations

This stage establishes an initial concept-aware semantic segmentation of the selected curriculum material.

At this stage:

- no final chunk size is selected;
- no fixed overlap setting is selected;
- no embedding model is selected through this segmentation process;
- no superiority is assigned to fine-grained or broader chunking;
- no controlled RAG retrieval performance is claimed.

The final retrieval configuration will be informed by the preliminary experiments specified in the proposed methodology, including evaluation of chunk size, overlap settings, and embedding model selection.

---

## 9. Current Segmentation Map

The resulting initial semantic segmentation is:

1. **C01 — Chromosome Numbers in Living Organisms**
2. **C02 — Cell Division and Preparation**
3. **C03 — Duplicated Chromosome Structure**
4. **C04 — Somatic and Reproductive Cells**
5. **C05 — Interphase and Purpose of Mitosis**
6. **C06 — Mitosis Stages**
7. **C07 — Mitosis Questions**
8. **C08 — Plant and Animal Cell Division**
9. **C09 — Meiosis**
10. **C10 — Chromosome Number Change and Curriculum Context**
11. **C11 — Down Syndrome and Chromosome 21**

This initial segmentation prepares the selected curriculum content for the subsequent Knowledge Base Construction (RAG Setup) phase and the preliminary retrieval experiments specified in the proposed methodology.
