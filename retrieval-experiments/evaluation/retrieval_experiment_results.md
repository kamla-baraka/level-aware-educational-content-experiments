# Preliminary Retrieval Experiment Results

## 1. Purpose

This preliminary experiment evaluated alternative retrieval configurations for the selected Grade 8 Science case study, Cell Division, before constructing the final retrieval component of the knowledge-grounded framework.

The experiment focused on three retrieval design factors:

- semantic chunk configuration;
- overlap setting; and
- multilingual embedding model.

The purpose was to identify a suitable retrieval configuration for the selected curriculum case study based on retrieval quality and curriculum-content coverage.

This experiment evaluates retrieval performance only. It does not evaluate LLM generation quality, learner outcomes, or the complete framework.

---

## 2. Experimental Factors

Three semantic chunk configurations were evaluated:

- **A_Fine** — fine-grained semantic segmentation;
- **B_Baseline** — baseline semantic segmentation;
- **C_Broad** — broader semantic segmentation.

Two overlap settings were evaluated:

- **O0** — no source-unit overlap;
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

- direct and narrow retrieval;
- relational retrieval;
- comparison;
- sequence and multi-part retrieval;
- causal and multi-step retrieval; and
- multi-concept retrieval.

Each query was associated with predefined expected curriculum-content elements.

Across Q01–Q12, there were 36 expected elements in total.

The query set was used as a controlled evaluation set for the selected Cell Division case study and is not presented as a validated retrieval benchmark.

---

## 4. Retrieval Procedure

For every experimental condition, each of the 12 queries retrieved the top three curriculum chunks.

This produced:

- 18 experimental conditions;
- 12 queries per condition;
- 216 query-condition runs;
- 3 retrieved records per run; and
- 648 ranked retrieval records.

Retrieval was performed using normalized embeddings and FAISS inner-product search for cosine-based similarity.

Raw similarity scores were retained as diagnostic information. Their absolute magnitudes were not used for direct quality comparison across different embedding models.

---

## 5. Human Annotation

Retrieval evaluation was based on researcher review of the retrieved curriculum text.

For each query, every predefined expected content element was assessed separately as:

- **Yes** — the retrieved text recovered the expected curriculum element; or
- **No** — the expected element was not recovered.

Assessment was based only on the retrieved curriculum text and the predefined expected curriculum content. Semantic equivalence was accepted where the required curriculum meaning was explicitly represented, but external knowledge or unsupported inference was not used.

Identical `(query_id, retrieval_text)` pairs were annotated once and the reviewed element-level judgments were subsequently propagated to repeated identical occurrences in the retrieval results.

The completed annotation dataset contained:

- 220 unique query-text annotation units;
- 674 element-level judgments;
- 211 Yes judgments; and
- 463 No judgments.

All 674 element-level judgments were completed before retrieval metrics were calculated.

---

## 6. Derived Relevance

Record-level curriculum relevance was derived from the completed element-level annotations:

- **Relevant** — all predefined expected elements for the query were recovered by the retrieved text.
- **Partially Relevant** — at least one, but not all, predefined expected elements were recovered.
- **Not Relevant** — none of the predefined expected elements were recovered.

Across the 648 retrieved records:

- 189 were Relevant;
- 122 were Partially Relevant; and
- 337 were Not Relevant.

These relevance categories were derived from the frozen element-level judgments and were not independently assigned.

---

## 7. Retrieval Metrics

Three principal retrieval measures were used.

### Full Hit@1

A query-condition run received `Full Hit@1 = 1` when the first-ranked retrieved chunk contained all predefined expected elements for that query.

### Full Hit@3

A query-condition run received `Full Hit@3 = 1` when the union of the top three retrieved chunks contained all predefined expected elements for that query.

### Expected Content Coverage@3

For queries with multiple predefined expected content elements, `Coverage@3` measured the proportion of expected elements recovered across the union of the top three retrieved chunks:

`Coverage@3 = Recovered Expected Content Elements / Total Expected Content Elements`

Q01 contained one predefined expected element and was therefore excluded from Mean Coverage@3 calculations in accordance with the predefined evaluation protocol.

Coverage@3 summary statistics consequently use the 198 query-condition runs corresponding to Q02–Q12.

No weighted composite score was used to select the retrieval configuration.

---

## 8. Overall Results

Across all 216 query-condition runs:

- **Full Hit@1:** 120/216 (**55.56%**)
- **Full Hit@3:** 175/216 (**81.02%**)

Across the 198 multi-element query-condition runs used for Coverage@3:

- **Mean Coverage@3:** **85.57%**

Complete expected-content retrieval was therefore more frequently achieved when evidence across the Top-3 retrieved chunks was considered than when only the first-ranked chunk was considered.

---

## 9. Factor-Level Observations

### Chunk Configuration

| Configuration | Full Hit@1 | Full Hit@3 | Mean Coverage@3* |
|---|---:|---:|---:|
| A_Fine | 55.56% | 76.39% | 83.59% |
| B_Baseline | 58.33% | 83.33% | 87.12% |
| C_Broad | 52.78% | 83.33% | 86.00% |

\* Mean Coverage@3 is calculated using multi-element queries only.

B_Baseline and C_Broad produced the same aggregate Full Hit@3 rate, while B_Baseline produced a slightly higher Mean Coverage@3 in this experiment.

### Overlap Setting

| Overlap | Full Hit@1 | Full Hit@3 | Mean Coverage@3* |
|---|---:|---:|---:|
| O0 | 61.11% | 81.48% | 85.19% |
| O1 | 50.00% | 80.56% | 85.95% |

\* Mean Coverage@3 is calculated using multi-element queries only.

The overlap setting did not produce a uniform improvement across the evaluated metrics.

### Embedding Model

| Model | Full Hit@1 | Full Hit@3 | Mean Coverage@3* |
|---|---:|---:|---:|
| E1 | 44.44% | 77.78% | 82.58% |
| E2 | 62.50% | 80.56% | 83.15% |
| E3 | 59.72% | 84.72% | 90.98% |

\* Mean Coverage@3 is calculated using multi-element queries only.

E3 produced the highest aggregate Full Hit@3 and Mean Coverage@3 across all tested chunk and overlap configurations. However, configuration selection was based on the combined condition-level evidence rather than embedding-model averages alone.

---

## 10. Query-Level Observations

Retrieval performance varied across the 12 evaluation queries.

Q01, Q02, Q07, and Q09 achieved Full Hit@3 across all 18 experimental conditions.

Incomplete Top-3 retrieval was concentrated mainly in:

- **Q03** — 12 incomplete runs;
- **Q06** — 7 incomplete runs;
- **Q10** — 7 incomplete runs; and
- **Q11** — 8 incomplete runs.

These results indicate that retrieval behavior varied across query structures. The experiment does not establish that query type or expected-element count caused these differences.

Coverage@3 was not used for Q01 because it contained only one predefined expected element.

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
- **Mean Coverage@3 (multi-element queries only):** **100%**
- **Minimum Coverage@3 (multi-element queries only):** **100%**
- **Incomplete Top-3 runs:** **0**

It was the only tested condition that recovered all predefined expected curriculum elements within the Top-3 retrieved chunks for all 12 evaluation queries.

Although other conditions produced higher Full Hit@1 values, the selected condition provided complete Top-3 expected-element recovery across the full controlled query set. For the multi-element queries used in Coverage@3 calculations, it also achieved complete expected-content coverage.

Accordingly, **B_Baseline + O0 + E1** was selected as the retrieval configuration for the next implementation stage of the selected case study.

This selection does not indicate that E1 is generally superior to the other tested embedding models. It reflects the combined retrieval evidence obtained for this controlled case study and evaluation set.

---

## 12. Interpretation Boundary

The selection applies to the controlled Cell Division case study and the fixed Q01–Q12 evaluation set.

The experiment does not establish:

- that E1 is universally superior to the other embedding models;
- that B_Baseline is optimal for other curriculum chapters;
- educational effectiveness;
- learner-performance improvement;
- effectiveness of adaptive progression;
- quality of generated educational packages; or
- generalizability across the complete Palestinian curriculum.

The findings are therefore treated as preliminary configuration evidence for implementation of the selected case study rather than as general benchmarking results.

---

## 13. Next Step

The selected retrieval configuration will be used to construct the curriculum knowledge base and retrieval component for the selected case study.

The next implementation stage will therefore use:

**B_Baseline + O0 + E1 + Top-3 retrieval**

as the experimentally selected retrieval setup.

The B_Baseline semantic chunk representation will be embedded using E1 without experimental source-unit overlap. The resulting curriculum embeddings will then be indexed using the vector-storage approach selected for the framework to support semantic curriculum retrieval in the subsequent knowledge-grounding stage.
