# Retrieval Annotation Rules

## 1. Purpose

This document defines the annotation rules used to evaluate the preliminary retrieval experiment.

The rules are fixed before retrieval-quality annotation begins.

The evaluation is based on the frozen Expected Curriculum Content defined for Q01–Q12.

Expected chunk IDs are not used as retrieval ground truth.

---

## 2. Unit of Annotation

The basic annotation unit is one retrieved chunk for one query under one experimental condition.

Each retrieved record is evaluated using:

- the query;
- the frozen Expected Curriculum Content;
- the retrieved curriculum text.

Similarity scores are retained as diagnostic retrieval outputs but are not used to determine relevance or expected-content recovery.

---

## 3. Curriculum Relevance

Each retrieved chunk is assigned one of three labels:

### Relevant

A retrieved chunk is **Relevant** when it directly contains curriculum information needed to answer the query or directly contributes one or more required expected-content elements.

### Partially Relevant

A retrieved chunk is **Partially Relevant** when it is related to the queried curriculum concept and provides useful contextual information, but does not directly provide the required answer or expected-content element(s).

### Not Relevant

A retrieved chunk is **Not Relevant** when it does not provide information that directly answers or meaningfully supports the query.

---

## 4. Expected-Content Recovery

For each query, the predefined Expected Curriculum Content is divided into required elements.

A required element is counted as recovered when the retrieved curriculum text contains the same curriculum meaning.

Exact word-for-word matching is not required.

No information may be inferred from external scientific knowledge.

An element is not counted as recovered when the retrieved text only mentions the general topic without providing the required curriculum information.

---

## 5. Recovered Element Count

For each retrieved chunk:

`recovered_element_count`

records the number of required expected-content elements directly supported by that retrieved chunk.

The value must range from:

`0`

to:

`expected_element_count`

for the corresponding query.

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

Coverage@3 measures the proportion of required Expected Curriculum Content elements recovered collectively across the top three retrieved chunks.

`Coverage@3 = Number of unique required elements recovered across Top-3 / Total number of required elements`

Coverage@3 ranges from:

`0.0` to `1.0`

Duplicate recovery of the same element across multiple chunks does not increase coverage.

---

## 9. Annotation Notes

The `annotation_notes` field may be used to document:

- ambiguous relevance;
- partial recovery;
- duplicated information across retrieved chunks;
- overlap-related context;
- curriculum wording that requires interpretation;
- other issues relevant to later review.

Notes must not introduce external scientific information.

---

## 10. Source Boundary

Annotation is restricted to the selected official Palestinian Grade 8 Science curriculum source used in the experiment.

No external scientific knowledge is used to judge whether missing curriculum information should be assumed.

---

## 11. Similarity Scores

Similarity scores are preserved for diagnostic analysis.

Raw similarity magnitudes are not used as direct evidence that one embedding model is better than another, particularly across different embedding architectures.

Model and configuration comparison is based on the predefined retrieval-quality metrics.

---

## 12. Annotation Timing

These rules are fixed before retrieval-quality annotation begins.

They must not be modified in response to observed model or configuration performance.

Any later methodological correction must be documented explicitly rather than silently changing the annotation criteria.
