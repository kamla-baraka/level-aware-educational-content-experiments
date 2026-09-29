# Preliminary Comparison of Chunking Variants

## 1. Purpose

This document compares the observations obtained from the two chunking representations used in the preliminary NotebookLM experiment:

- **Variant A:** Fine-grained concept-aware representation.
- **Variant B:** Broader concept-aware representation.

The purpose of the comparison is to examine how chunk granularity may influence the organization and amount of curriculum context associated with different types of queries.

This comparison is exploratory. It does not determine the final chunking strategy and does not constitute a controlled evaluation of the proposed RAG pipeline.

---

## 2. Experimental Conditions

Both variants used the same Mitosis curriculum content and were tested using:

- the same five queries;
- the same query order;
- the same instruction;
- separate NotebookLM notebooks;
- the same curriculum scope.

The main experimental difference was the granularity of the explicitly represented curriculum units.

### Variant A

The curriculum content was divided into five conceptual units:

1. Interphase and Purpose
2. Prophase
3. Metaphase
4. Anaphase
5. Telophase and Cytokinesis

### Variant B

The same curriculum content was organized into two broader units:

1. Interphase and Purpose
2. Mitosis Stages

---

## 3. Query-Level Comparison

| Query | Information Need | Variant A: Identified Source Sections | Variant B: Identified Source Sections | Preliminary Observation |
|---|---|---|---|---|
| Q1 | Specific preparatory-stage information | A1 | B1 | Both variants associated the answer with the specific Interphase and Purpose unit. |
| Q2 | Specific Mitosis-stage information | A4 | B2 | Variant A identified a more targeted conceptual unit, while Variant B associated the answer with the broader Mitosis Stages unit. |
| Q3 | Complete Mitosis-stage explanation | A2–A5 | B2 | Variant A required multiple explicitly represented units, while Variant B contained the complete stage sequence within one broader unit. |
| Q4 | Sequential/relational explanation across stages | A3–A5 | B2 | Variant A drew on multiple stage-specific units, while Variant B preserved the required sequence within one broader unit. |
| Q5 | Mitosis outcome and chromosome number | A1 and A5 | B2 | Both variants supported the answer, but the identified source organization differed. |

---

## 4. Variant A Observations

Variant A provided finer conceptual separation of the Mitosis content.

For narrow queries, this representation allowed the generated response to identify a highly specific source unit.

For example, the Anaphase query was associated specifically with:

`Chunk A4 — Anaphase`

This suggests a potential advantage of fine-grained segmentation for queries targeting a single curriculum concept.

However, broader questions required multiple explicitly represented units.

The complete Mitosis-stage question used:

`Chunk A2` through `Chunk A5`

and the sequential question used:

`Chunk A3`, `Chunk A4`, and `Chunk A5`.

This indicates a potential trade-off: finer segmentation can increase conceptual specificity while increasing dependence on the retrieval of multiple relevant units for questions requiring connected information.

---

## 5. Variant B Observations

Variant B preserved the Mitosis stages within one broader conceptual unit.

For the narrow Anaphase query, the identified source was:

`Chunk B2 — Mitosis Stages`

This unit contained more information than was strictly required for the narrow question.

However, the broader and sequential questions were also supported by the same unit.

For Q3 and Q4, the complete relevant stage sequence was available within `Chunk B2`.

This suggests a potential advantage of broader concept-aware segmentation for maintaining contextual continuity across closely related curriculum concepts.

The corresponding trade-off is that a narrow query may be associated with a source unit containing additional information that is not directly required.

---

## 6. Observed Granularity Trade-Off

The exploratory comparison indicates the following potential trade-off:

### Fine-Grained Representation

**Potential advantage:**
- more targeted conceptual units for narrow information needs.

**Potential limitation:**
- broader or relational questions may depend on multiple units being identified and combined.

### Broader Representation

**Potential advantage:**
- preserves connected curriculum context for multi-stage and relational questions.

**Potential limitation:**
- may provide additional context for narrowly focused questions.

Therefore, the preliminary experiment does not indicate that smaller or larger chunks are universally preferable.

Instead, appropriate granularity may depend on the type of information need and the structure of the curriculum concept.

---

## 7. Context Sufficiency

NotebookLM reported sufficient source context for all five queries under both variants.

Therefore, no clear failure condition was observed in this small exploratory test.

This means that the current experiment does not provide sufficient evidence to select Variant A or Variant B as the final chunking strategy.

The absence of failure in either condition also highlights the need for later controlled retrieval testing using a wider query set and an implemented retrieval pipeline.

---

## 8. Retrieval and Generation Should Be Evaluated Separately

An important observation from the experiment is the need to distinguish retrieval behavior from generation behavior.

For example, the Variant A response to Q5 included information about the purpose of Mitosis in addition to the requested outcome and chromosome number.

This additional information was available in the supplied source but was not necessary to answer the question directly.

Such differences in generated answers cannot automatically be attributed to chunk granularity because they may result from the language model's generation behavior.

Therefore, the implemented RAG evaluation should distinguish between:

1. **Retrieval evaluation**
   - Which chunks were retrieved?
   - Were the relevant chunks retrieved?
   - Was necessary context missing?
   - How much irrelevant or unnecessary context was retrieved?

2. **Generation evaluation**
   - Was the generated answer supported by the retrieved context?
   - Did the answer remain within the curriculum knowledge boundary?
   - Did the model introduce unnecessary or unsupported information?

---

## 9. Important Methodological Limitation

NotebookLM controls its own internal source processing, chunking, indexing, and retrieval mechanisms.

The explicit labels such as `Chunk A4` and `Chunk B2` identify the source sections represented in the experimental files and reported in the generated responses.

They should not be interpreted as direct evidence that NotebookLM internally retrieved these units as independent vector-store chunks.

Therefore, this experiment should be treated as a:

**Preliminary Chunking Exploration**

rather than a controlled:

**RAG Chunking Evaluation**

A controlled comparison requires implementation of the retrieval pipeline where chunk boundaries, embeddings, vector storage, similarity search, and retrieval parameters can be directly controlled and inspected.

---

## 10. Preliminary Design Implication

The experiment supports retaining **concept-aware semantic segmentation** as the initial design direction.

However, it does not support fixing a single universal chunk granularity at this stage.

A reasonable next step is to preserve semantic boundaries while allowing chunk granularity to be evaluated experimentally during RAG implementation.

The controlled evaluation should compare alternative chunk configurations using the same curriculum content and query set while directly inspecting retrieved chunks.

Possible variables for later testing include:

- chunk granularity;
- chunk size;
- overlap strategy;
- embedding model;
- retrieval `top-k`.

---

## 11. Current Decision

Based on this preliminary experiment:

1. Concept-aware semantic boundaries remain the primary basis for curriculum segmentation.
2. Page boundaries will not automatically define chunk boundaries.
3. Fine-grained and broader concept-aware alternatives remain candidates for controlled testing.
4. No fixed overlap is selected at this stage.
5. No final chunk size is selected at this stage.
6. The final chunking configuration will be determined during controlled RAG retrieval experiments rather than from the NotebookLM pilot alone.

---

## 12. Conclusion

The preliminary NotebookLM experiment demonstrated that both fine-grained and broader concept-aware representations were sufficient to support grounded responses to the selected Mitosis queries.

Fine-grained representation provided more targeted source units for narrow questions, whereas broader representation preserved related stage information within a single context for broader and sequential questions.

These observations reveal a granularity trade-off but do not establish the superiority of either representation.

The findings therefore inform the design of the subsequent controlled RAG experiments, where retrieval behavior can be directly measured and the final chunking configuration can be selected using controlled evidence.
