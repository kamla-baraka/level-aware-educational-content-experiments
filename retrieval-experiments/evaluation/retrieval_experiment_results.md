# Preliminary Retrieval Experiment Results

## 1. Purpose

This preliminary experiment evaluated alternative retrieval configurations for the selected Grade 8 Science case study, *Cell Division*, before constructing the final retrieval component of the knowledge-grounded framework.

The experiment focused on three retrieval design factors:

1. semantic chunk configuration,
2. overlap setting, and
3. multilingual embedding model.

The purpose was to identify a suitable retrieval configuration for the selected curriculum case study based on retrieval quality and curriculum-content coverage.

This experiment evaluates retrieval performance only. It does not evaluate LLM generation quality, learner outcomes, or the complete framework.

---

## 2. Experimental Factors

Three semantic chunk configurations were evaluated:

- **A_Fine** — fine-grained semantic segmentation,
- **B_Baseline** — baseline semantic segmentation,
- **C_Broad** — broader semantic segmentation.

Two overlap settings were evaluated:

- **O0** — no source-unit overlap,
- **O1** — one-source-unit overlap.

Three multilingual embedding models were evaluated:

- **E1** — `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`
- **E2** — `intfloat/multilingual-e5-base`
- **E3** — `BAAI/bge-m3`

The complete experiment therefore contained:

**3 chunk configurations × 2 overlap settings × 3 embedding models = 18 experimental conditions.**

---

## 3. Evaluation Queries

A fixed set of 12 researcher-constructed queries (Q01–Q12) was used.

The queries represented different retrieval requirements, including:

- direct and narrow retrieval,
- relational retrieval,
- comparison,
- sequence and multi-part retrieval,
- causal and multi-step retrieval, and
- multi-concept retrieval.

Each query was associated with predefined expected curriculum-content elements.

Across Q01–Q12, there were 36 expected elements in total.

The query set was used as a controlled evaluation set for the selected Cell Division case study and is not presented as a validated retrieval benchmark.

---

## 4. Retrieval Procedure

For every experimental condition, each of the 12 queries retrieved the top three curriculum chunks.

This produced:

- **18 experimental conditions**
- **12 queries per condition**
- **216 query-condition runs**
- **3 retrieved records per run**
- **648 ranked retrieval records**

Retrieval was performed using normalized embeddings and FAISS inner-product search for cosine-based similarity.

Raw similarity scores were retained as diagnostic information. Their absolute magnitudes were not used for direct quality comparison across different embedding models.

---

## 5. Human Annotation

Retrieval evaluation was based on researcher review of the retrieved curriculum text.

For each query, every expected element was assessed as:

- **Yes** — the retrieved text recovered the expected curriculum element, or
- **No** — the expected element was not recovered.

Assessment was based only on the retrieved curriculum text. Semantic equivalence was accepted, but external knowledge or unsupported inference was not used.

Identical `(query_id, retrieval_text)` pairs were annotated once and the reviewed annotation was subsequently propagated to repeated occurrences in the retrieval results.

The completed annotation dataset contained:

- **220 unique query-text annotation units**
- **674 element-level judgments**
- **211 Yes judgments**
- **463 No judgments**

All 674 element judgments were completed before retrieval metrics were calculated.

---

## 6. Derived Relevance

Record-level relevance was derived from the completed element annotations:

- **Relevant** — all expected elements for the query were recovered by the retrieved text.
- **Partially Relevant** — at least one, but not all, expected elements were recovered.
- **Not Relevant** — none of the expected elements were recovered.

Across the 648 retrieved records:

- **189** were Relevant,
- **122** were Partially Relevant,
- **337** were Not Relevant.

These relevance labels were derived from the frozen element-level judgments and were not independently assigned.

---

## 7. Retrieval Metrics

Three principal metrics were used.

### Full Hit@1

A query-condition run received Full Hit@1 = 1 when the first-ranked retrieved chunk contained all expected elements for that query.

### Full Hit@3

A query-condition run received Full Hit@3 = 1 when the union of the top three retrieved chunks contained all expected elements for that query.

### Coverage@3

Coverage@3 measured the proportion of expected elements recovered across the union of the top three retrieved chunks.

No weighted composite score was used to select the retrieval configuration.

---

## 8. Overall Results

Across all 216 query-condition runs:

- **Full Hit@1:** 120/216 (**55.56%**)
- **Full Hit@3:** 175/216 (**81.02%**)
- **Mean Coverage@3:** **86.77%**

The results show that complete retrieval was more frequently achieved when evidence across the top three retrieved chunks was considered than when only the first-ranked chunk was considered.

---

## 9. Factor-Level Observations

### Chunk Configuration

| Configuration | Full Hit@1 | Full Hit@3 | Mean Coverage@3 |
|---|---:|---:|---:|
| A_Fine | 55.56% | 76.39% | 84.95% |
| B_Baseline | 58.33% | 83.33% | 88.19% |
| C_Broad | 52.78% | 83.33% | 87.17% |

B_Baseline and C_Broad produced the same aggregate Full Hit@3 rate, while B_Baseline produced slightly higher mean Coverage@3 in this experiment.

### Overlap Setting

| Overlap | Full Hit@1 | Full Hit@3 | Mean Coverage@3 |
|---|---:|---:|---:|
| O0 | 61.11% | 81.48% | 86.42% |
| O1 | 50.00% | 80.56% | 87.13% |

The overlap setting did not produce a uniform improvement across the evaluated metrics.

### Embedding Model

| Model | Full Hit@1 | Full Hit@3 | Mean Coverage@3 |
|---|---:|---:|---:|
| E1 | 44.44% | 77.78% | 84.03% |
| E2 | 62.50% | 80.56% | 84.56% |
| E3 | 59.72% | 84.72% | 91.73% |

E3 produced the highest aggregate Full Hit@3 and mean Coverage@3 across all tested chunk and overlap configurations. However, configuration selection was based on the combined condition-level evidence rather than embedding-model averages alone.

---

## 10. Query-Level Observations

Retrieval performance varied across the 12 evaluation queries.

Q01, Q02, Q07, and Q09 achieved Full Hit@3 across all 18 experimental conditions.

Incomplete Top-3 retrieval was concentrated mainly in:

- Q03 — 12 incomplete runs,
- Q06 — 7 incomplete runs,
- Q10 — 7 incomplete runs,
- Q11 — 8 incomplete runs.

These results indicate that retrieval behavior varied across query structures. The experiment does not establish that query type or expected-element count caused these differences.

---

## 11. Selected Retrieval Configuration

The selected configuration for the next stage is:

- **Chunk configuration:** B_Baseline
- **Overlap:** O0
- **Embedding model:** E1 (`sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`)
- **Retrieval depth:** Top-3

For this condition:

- **Full Hit@1:** 7/12 (**58.33%**)
- **Full Hit@3:** 12/12 (**100%**)
- **Mean Coverage@3:** **100%**
- **Minimum Coverage@3:** **100%**
- **Incomplete Top-3 runs:** **0**

It was the only tested condition that recovered all expected curriculum elements within the top three retrieved chunks for all 12 evaluation queries.

Although other conditions produced higher Full Hit@1 values, the selected condition provided complete Top-3 expected-element coverage across the full controlled query set.

Accordingly, B_Baseline + O0 + E1 was selected as the retrieval configuration for the next implementation stage of the selected case study.

---

## 12. Interpretation Boundary

The selection applies to the controlled *Cell Division* case study and the fixed Q01–Q12 evaluation set.

The experiment does not establish that E1 is universally superior to the other embedding models, that B_Baseline is optimal for other curriculum chapters, or that the selected configuration guarantees retrieval or generation quality in broader educational settings.

The findings are therefore treated as preliminary configuration evidence for the implementation of the selected case study rather than as general benchmarking results.

---

## 13. Next Step

The selected retrieval configuration will be used to construct the curriculum knowledge base and retrieval component for the selected case study.

The next implementation stage will therefore use:

**B_Baseline + O0 + E1 + Top-3 retrieval**

as the experimentally selected retrieval setup.
