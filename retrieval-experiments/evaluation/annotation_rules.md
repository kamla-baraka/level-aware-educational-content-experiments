# Retrieval Annotation Rules

## 1. Purpose

This document defines the annotation rules used to evaluate the preliminary retrieval experiment.

The rules are aligned with the frozen Preliminary Retrieval Configuration Experiment Protocol and are applied before full retrieval-quality annotation begins.

The evaluation is based on the frozen Expected Curriculum Content defined for Q01–Q12.

Expected chunk IDs are not used as retrieval ground truth.

---

## 2. Unit of Annotation

The basic annotation unit is one retrieved chunk for one query under one experimental condition.

Each retrieved record is evaluated using:

- the query;
- the frozen Expected Curriculum Content;
- the predefined expected-content elements;
- the retrieved curriculum text.

Similarity scores are retained as diagnostic retrieval outputs but are not used to determine relevance or expected-content recovery.

When the same retrieved curriculum text occurs for the same query across multiple experimental conditions, the expected-content recovery judgment may be made once and propagated to identical query-text pairs.

This deduplication is an implementation procedure only and does not change the experimental unit, raw retrieval results, or evaluation criteria.

---

## 3. Expected-Content Recovery

For each query, the predefined Expected Curriculum Content is represented by one or more required expected-content elements.

A required element is counted as recovered when the retrieved curriculum text directly contains the same curriculum meaning.

Exact word-for-word matching is not required.

No information may be inferred from external scientific knowledge.

An element is not counted as recovered when the retrieved text:

- only mentions the general topic;
- asks a question without providing the required curriculum information;
- provides related contextual information without the required curriculum meaning; or
- requires external knowledge or unsupported inference to establish the element.

For each expected-content element, the annotation judgment is:

- `Yes` — the element is directly supported by the retrieved curriculum text.
- `No` — the element is not directly supported by the retrieved curriculum text.

---

## 4. Recovered Element Count

For each retrieved chunk:

`recovered_element_count`

records the number of required expected-content elements directly supported by that retrieved chunk.

The value must range from:

`0`

to:

`expected_element_count`

for the corresponding query.

The recovered-element judgments are the primary basis for determining curriculum relevance.

---

## 5. Curriculum Relevance

Each retrieved chunk is assigned one of three relevance labels based on recovery of the predefined Expected Curriculum Content.

### Relevant

A retrieved chunk is **Relevant** when it contains the complete Expected Curriculum Content required for the query.

Operationally:

`recovered_element_count = expected_element_count`

### Partially Relevant

A retrieved chunk is **Partially Relevant** when it directly recovers one or more required expected-content elements but does not contain the complete Expected Curriculum Content required for the query.

Operationally:

`0 < recovered_element_count < expected_element_count`

This category therefore represents actual partial recovery of required curriculum content rather than general topical relatedness.

### Not Relevant

A retrieved chunk is **Not Relevant** when it recovers none of the required Expected Curriculum Content elements.

Operationally:

`recovered_element_count = 0`

A chunk is therefore not considered partially relevant merely because it discusses the same general topic or provides related contextual information.

---

## 6. Full Hit@1

A query receives a Full Hit@1 when the rank-1 retrieved chunk contains all required Expected Curriculum Content elements for that query.

Formally:

`Full Hit@1 = 1`

when all required elements are recovered from rank 1.

Otherwise:

`Full Hit@1 = 0`

---

## 7. Full Hit@3

A query receives a Full Hit@3 when the required Expected Curriculum Content is completely recovered collectively across the top three retrieved chunks.

The same required element is counted only once when it appears in multiple retrieved chunks.

Formally:

`Full Hit@3 = 1`

when the union of recovered expected-content elements across ranks 1–3 contains all required elements.

Otherwise:

`Full Hit@3 = 0`

---

## 8. Coverage@3

For queries with multiple predefined expected-content elements, Coverage@3 measures the proportion of required Expected Curriculum Content elements recovered collectively across the top three retrieved chunks.

`Coverage@3 = Number of unique required elements recovered across Top-3 / Total number of required elements`

Coverage@3 ranges from:

`0.0` to `1.0`

Duplicate recovery of the same element across multiple chunks does not increase coverage.

Coverage@3 is reported according to the experimental protocol for queries with multiple predefined expected-content elements.

---

## 9. Annotation Notes

The `annotation_notes` field may be used when clarification is required, including:

- ambiguous curriculum wording;
- partial recovery requiring explanation;
- duplicated information across retrieved chunks;
- overlap-related context;
- source-continuity issues; or
- other issues relevant to later review.

Notes are optional when the recovery judgment is clear.

Notes must not introduce external scientific information.

---

## 10. Source Boundary

Annotation is restricted to the selected official Palestinian Grade 8 Science curriculum source used in the experiment.

No external scientific knowledge is used to judge whether missing curriculum information should be assumed.

The annotation evaluates retrieval of the predefined curriculum content, not general scientific correctness beyond the selected curriculum source.

---

## 11. Similarity Scores

Similarity scores are preserved for diagnostic analysis.

Raw similarity magnitudes are not used as direct evidence that one embedding model is better than another, particularly across different embedding architectures.

Model and configuration comparison is based on the predefined retrieval-quality metrics.

---

## 12. Annotation Workflow

The annotation workflow is:

1. Read the query.
2. Read its frozen Expected Curriculum Content elements.
3. Inspect the retrieved curriculum text.
4. Mark each expected-content element as `Yes` or `No`.
5. Calculate `recovered_element_count`.
6. Derive the curriculum relevance label from the recovered-element count.
7. Add an annotation note only where clarification is required.

The relevance label is therefore derived from expected-content recovery rather than independently assigned as a separate subjective judgment.

---

## 13. Annotation Timing and Methodological Correction

The original annotation rules were prepared before full retrieval-quality annotation.

A pilot annotation was then conducted to verify the operational application of the evaluation criteria.

During this pilot-quality-control stage, an inconsistency was identified between the initial operational definition of `Partially Relevant` and the definition specified in the frozen Preliminary Retrieval Configuration Experiment Protocol.

The initial annotation rule allowed a retrieved chunk to be classified as `Partially Relevant` when it provided useful contextual information without directly recovering required Expected Curriculum Content.

The experimental protocol, however, defines partial relevance in terms of recovery of a required part of the Expected Curriculum Content.

The annotation rule was therefore corrected before full annotation to restore consistency with the frozen experimental protocol.

This correction:

- was made before full retrieval-quality annotation;
- does not modify the retrieval queries;
- does not modify the Expected Curriculum Content;
- does not modify the raw retrieval results;
- does not modify the experimental configurations;
- does not modify the retrieved rankings;
- does not modify the predefined retrieval-quality metrics; and
- is not based on comparative model or configuration performance.

Following this correction, the annotation criteria remain fixed throughout full retrieval-quality annotation.

Any subsequent methodological correction must be documented explicitly rather than silently changing the evaluation criteria.
