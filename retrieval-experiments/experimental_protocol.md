# Preliminary Retrieval Configuration Experiment Protocol

## 1. Purpose

This protocol defines the preliminary experiments used to evaluate retrieval configurations for the curriculum knowledge base of the proposed framework.

The experiments are conducted using the selected Palestinian Grade 8 Science curriculum case study, specifically Lesson 3, "Cell Division" (انقسام الخلايا), pages 23–29.

The purpose of the experiments is to examine how alternative retrieval configurations affect the retrieval of relevant curriculum content before selecting the configuration to be used in the curriculum knowledge base.

In accordance with the proposed methodology, the preliminary experiments examine:

1. Chunk configuration and semantic granularity.
2. Overlap settings.
3. Multilingual embedding model selection.

The experiments focus on semantic retrieval quality and curriculum alignment.

They do not evaluate LLM-generated educational content, learner-level differentiation, learner performance, or educational effectiveness.

No preferred chunk configuration, overlap setting, or embedding model is selected before the experimental results are obtained.

---

## 2. Experimental Source

The experiment uses curriculum content derived exclusively from the official Palestinian Grade 8 Science curriculum.

Selected case study:

- Grade: 8
- Subject: Science
- Lesson: Cell Division (انقسام الخلايا)
- Source pages: 23–29
- Language: Arabic
- Source type: Official Palestinian Science textbook

The machine-readable curriculum dataset serves as the source representation from which the experimental semantic chunk configurations are constructed.

All experimental configurations represent the same underlying curriculum content.

No external scientific knowledge is added to the curriculum chunks during the retrieval experiments.

Differences between experimental configurations therefore result from retrieval configuration choices rather than differences in the underlying curriculum knowledge.

---

## 3. Experimental Variables

Three retrieval configuration factors are examined:

1. Semantic chunk configuration and granularity.
2. Overlap setting.
3. Multilingual embedding model.

Other parameters required to execute the experiment are treated as controlled implementation parameters rather than additional experimental variables.

---

## 3.1 Chunk Configurations

Three concept-aware semantic chunk configurations are evaluated.

All configurations are derived from the same machine-readable curriculum source and preserve:

- curriculum structure;
- topic and concept boundaries;
- semantic coherence;
- source fidelity;
- source traceability; and
- the relevant official unit-level learning objective.

Chunks are not split or merged solely to achieve predetermined text lengths.

### Configuration A — Fine-Grained

The fine-grained configuration separates selected curriculum concepts into smaller semantically coherent units where the internal curriculum structure supports meaningful subdivision.

Initial configuration:

- A01 — Chromosome Numbers in Living Organisms
- A02 — Cell Division Activity and Purpose
- A03 — Chromatin and Preparation for Cell Division
- A04 — Duplicated Chromosome Structure
- A05 — Somatic and Reproductive Cells
- A06 — Interphase
- A07 — Purpose and Occurrence of Mitosis
- A08 — Mitosis Activity Introduction and Prophase
- A09 — Metaphase
- A10 — Anaphase
- A11 — Telophase and Cytokinesis
- A12 — Mitosis Questions
- A13 — Plant and Animal Cell Division
- A14 — Meiosis
- A15 — Down Syndrome Curriculum Context
- A16 — Chromosome Number Change and Down Syndrome
- A17 — Chromosome 21 and Meiosis Error

Total initial chunks: 17.

### Configuration B — Baseline

The baseline configuration corresponds to the initial concept-aware semantic segmentation developed during curriculum preparation.

- B01 — Chromosome Numbers in Living Organisms
- B02 — Cell Division and Preparation
- B03 — Duplicated Chromosome Structure
- B04 — Somatic and Reproductive Cells
- B05 — Interphase and Purpose of Mitosis
- B06 — Mitosis Stages
- B07 — Mitosis Questions
- B08 — Plant and Animal Cell Division
- B09 — Meiosis
- B10 — Down Syndrome Curriculum Context
- B11 — Chromosome Number Change, Down Syndrome and Chromosome 21

Total chunks: 11.

### Configuration C — Broader

The broader configuration combines closely connected curriculum content into larger semantically coherent units while preserving meaningful topic boundaries.

- C01 — Chromosome Numbers in Living Organisms
- C02 — Cell Division and Preparation
- C03 — Duplicated Chromosome Structure
- C04 — Somatic and Reproductive Cells
- C05 — Mitosis: Preparation, Purpose and Stages
- C06 — Mitosis Questions
- C07 — Plant and Animal Cell Division
- C08 — Meiosis
- C09 — Chromosome Number Changes and Down Syndrome

Total initial chunks: 9.

Before retrieval execution, all three configurations will be validated against the machine-readable curriculum source to confirm complete curriculum coverage and source fidelity.

---

## 3.2 Overlap Settings

Overlap is treated as an experimental retrieval configuration parameter.

Two conditions are considered:

### O0 — No Overlap

Chunks contain only the curriculum content assigned to their semantic boundaries.

### O1 — Limited Fixed Overlap

A limited and reproducible overlap condition will be applied for comparison.

The exact overlap value will be fixed after examining the actual chunk-length distribution and before any retrieval results are generated.

Once fixed, the overlap value will remain unchanged throughout the retrieval experiment.

Any experimental overlap must:

- use only content already present in the curriculum source;
- preserve source fidelity;
- avoid generated bridging text;
- avoid external knowledge; and
- follow the same predefined implementation procedure across applicable configurations.

Cross-page continuation that belongs to the original curriculum source is treated as source continuity rather than experimental overlap.

If implementation validation demonstrates that an overlap condition produces no distinct representation for a particular configuration, that condition will be documented as non-distinct rather than treated as an independent experimental result.

---

## 3.3 Candidate Embedding Models

Three multilingual embedding models are selected as candidates for the preliminary retrieval comparison:

- E1 — `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`
- E2 — `intfloat/multilingual-e5-base`
- E3 — `BAAI/bge-m3`

The models are evaluated as candidate retrieval models and are not ordered by expected performance.

Each model will be applied to the same curriculum configurations, evaluation queries, retrieval depth, and evaluation criteria.

Each model will use its documented recommended encoding procedure.

Model-specific query or document formatting required by the model will be treated as part of the model implementation rather than as a separate experimental variable.

The exact model revision, encoding procedure, normalization settings, and relevant implementation parameters will be recorded during implementation.

No embedding model will be designated as preferred before retrieval results are analyzed.

---

## 4. Retrieval Evaluation Set

A predefined retrieval evaluation set is used to evaluate the experimental configurations.

The evaluation set consists of researcher-constructed queries derived exclusively from the selected curriculum content.

Each query is associated with predefined expected curriculum content representing the information that successful retrieval should recover.

The queries and expected content are defined before executing the retrieval experiments and remain unchanged across experimental configurations.

The evaluation set includes:

- direct factual retrieval;
- relational retrieval;
- sequential and multi-part retrieval;
- comparison across curriculum concepts; and
- causal or multi-step retrieval.

The evaluation set is intended only for preliminary retrieval evaluation within the selected case study.

It is not an externally validated retrieval benchmark.

---

### Q01 — DNA Duplication

**Query:**  
ماذا يحدث للمادة الوراثية DNA قبل انقسام الخلية؟

**Expected Curriculum Content:**  
يحدث تضاعف لمادة الوراثة (DNA) قبل البدء بعملية الانقسام.

**Retrieval Type:** Direct / Narrow

---

### Q02 — Duplicated Chromosome Structure

**Query:**  
مم يتكون الكروموسوم المتضاعف وكيف يرتبط مكوناه؟

**Expected Curriculum Content:**  
يتكون الكروموسوم المتضاعف من كروماتيدين، ويرتبطان بنقطة تسمى السنترومير.

**Retrieval Type:** Direct / Narrow

---

### Q03 — Somatic Cells and Mitosis

**Query:**  
ما نوع الانقسام المرتبط بالخلايا الجسمية وما نتيجته؟

**Expected Curriculum Content:**  
تنقسم نواة الخلايا الجسمية بالانقسام المتساوي، وينتج عنه خليتان تحتوي كل منهما على العدد نفسه من الكروموسومات.

**Retrieval Type:** Direct / Relational

---

### Q04 — Interphase

**Query:**  
ماذا يحدث للخلية في الطور البيني؟

**Expected Curriculum Content:**  
تنمو الخلية، ويزداد حجمها، وتتضاعف كمية المادة الوراثية (DNA).

**Retrieval Type:** Direct / Narrow

---

### Q05 — Anaphase

**Query:**  
ماذا يحدث للكروماتيدات الشقيقة في الدور الانفصالي؟

**Expected Curriculum Content:**  
تتباعد الكروماتيدات الشقيقة بفعل انكماش خيوط المغزل، كل إلى قطب.

**Retrieval Type:** Direct / Narrow

---

### Q06 — Mitosis Sequence

**Query:**  
ما مراحل الانقسام المتساوي وما الذي يحدث خلالها حتى تنتج خليتان؟

**Expected Curriculum Content Elements:**

1. الدور التمهيدي.
2. الدور الاستوائي.
3. الدور الانفصالي.
4. الدور النهائي.
5. انقسام السيتوبلازم والنتيجة النهائية.

The expected outcome includes the production of two identical cells, each containing the same number of chromosomes as the mother cell.

**Retrieval Type:** Sequence / Multi-part

---

### Q07 — Plant and Animal Cell Division

**Query:**  
ما أوجه الاختلاف بين انقسام الخلية النباتية والخلية الحيوانية كما يعرضها المنهج؟

**Expected Curriculum Content:**  
The retrieved curriculum context should recover the information used by the curriculum to compare plant and animal cell division, including the middle plate shown for the plant cell and membrane constriction shown for the animal cell.

**Retrieval Type:** Comparison

---

### Q08 — Meiosis Outcome

**Query:**  
ما نتيجة الانقسام المنصف من حيث عدد الخلايا وعدد الكروموسومات؟

**Expected Curriculum Content:**  
ينتج عن الانقسام المنصف أربع خلايا، تحتوي كل منها على نصف العدد الأصلي من كروموسومات الخلية الأم.

**Retrieval Type:** Direct / Narrow

---

### Q09 — Somatic and Reproductive Cells

**Query:**  
ما العلاقة بين الخلايا الجسمية والخلايا التناسلية ونوع الانقسام الذي يحدث في كل منها؟

**Expected Curriculum Content Elements:**

1. الخلايا الجسمية ترتبط بالانقسام المتساوي.
2. الخلايا التناسلية ترتبط بالانقسام المنصف الذي ينتج الغاميتات.

**Retrieval Type:** Relational / Comparison

---

### Q10 — Meiosis Error and Chromosome Number

**Query:**  
كيف يمكن أن يؤدي خلل أثناء الانقسام المنصف إلى وجود 47 كروموسومًا؟

**Expected Curriculum Content Elements:**

1. حدوث خلل أثناء الانقسام المنصف.
2. إنتاج غاميت يحتوي على 24 كروموسومًا.
3. اتحاد هذا الغاميت مع غاميت طبيعي يحتوي على 23 كروموسومًا.
4. الناتج يحتوي على 47 كروموسومًا.

**Retrieval Type:** Causal / Multi-step

---

### Q11 — Mitosis and Meiosis Outcomes

**Query:**  
ما الفرق بين نواتج الانقسام المتساوي والانقسام المنصف من حيث عدد الخلايا وعدد الكروموسومات؟

**Expected Curriculum Content Elements:**

1. Mitosis produces two cells containing the same chromosome number as the mother cell.
2. Meiosis produces four cells, each containing half the original chromosome number.

**Retrieval Type:** Comparison / Multi-concept

This query assesses retrieval of curriculum information required for the conceptual comparison represented in the relevant unit-level learning objective. It does not independently evaluate the complete objective, including its drawing component.

---

### Q12 — Chromosome Number

**Query:**  
ما عدد الكروموسومات في خلايا الإنسان العادي وما العدد الموجود في متلازمة داون؟

**Expected Curriculum Content Elements:**

1. خلايا الإنسان العادي تحتوي على 46 كروموسومًا.
2. خلايا الجسم في متلازمة داون تحتوي على 47 كروموسومًا.

**Retrieval Type:** Direct / Comparison

---

## 5. Expected Content Ground Truth

The retrieval ground truth is defined in terms of expected curriculum content rather than predetermined chunk identifiers.

This is necessary because the same curriculum information may be represented by different chunk identifiers across the fine-grained, baseline, and broader configurations.

For multi-part queries, the required curriculum content elements are predefined before retrieval execution.

The expected content definitions will not be modified based on retrieval results.

---

## 6. Retrieval Procedure

For each valid experimental configuration, the following procedure will be applied:

1. Construct the semantic chunks from the same machine-readable curriculum source according to the predefined chunk configuration.
2. Apply the predefined overlap setting.
3. Encode the curriculum chunks using the selected candidate embedding model.
4. Encode each evaluation query using the same embedding model and its documented encoding procedure.
5. Perform semantic similarity retrieval against the curriculum chunk representations.
6. Retrieve the Top-3 ranked chunks for each query.
7. Store the raw retrieval outputs.
8. Compare the retrieved curriculum content with the predefined expected curriculum content.
9. Apply the predefined retrieval evaluation measures.
10. Summarize results at query and configuration levels.

No LLM-based answer generation will be performed during this experiment.

The experiment evaluates retrieval only.

---

## 6.1 Retrieval Depth

A fixed retrieval depth of:

`Top-k = 3`

will be used throughout the preliminary retrieval experiment.

The same retrieval depth will be applied across all experimental configurations.

Top-k will not be optimized independently during this experiment.

Top-k is treated as a controlled implementation parameter rather than an additional experimental variable.

---

## 7. Retrieval Evaluation Measures

### 7.1 Full Hit@1

Full Hit@1 equals 1 when the first-ranked retrieved chunk contains the complete expected curriculum content required for the query.

Otherwise:

`Full Hit@1 = 0`

For multi-part queries, Rank 1 must contain all predefined required elements to receive a Full Hit@1.

---

### 7.2 Full Hit@3

Full Hit@3 equals 1 when the complete expected curriculum content is collectively recovered within the first three retrieved chunks.

Otherwise:

`Full Hit@3 = 0`

For multi-part queries, required content may be distributed across multiple Top-3 retrieved chunks.

---

### 7.3 Expected Content Coverage@3

For queries with multiple predefined expected content elements:

`Coverage@3 = Recovered Expected Content Elements / Total Expected Content Elements`

Coverage is reported as a proportion or percentage.

The required content elements are defined before retrieval execution and are not modified based on experimental results.

---

### 7.4 Curriculum Relevance

Each retrieved chunk within the Top-3 results is evaluated against the predefined expected curriculum content.

The relevance categories are:

**Relevant**  
The retrieved chunk contains information directly required by the query.

**Partially Relevant**  
The retrieved chunk contains a required part of the expected content but is insufficient for a multi-part query.

**Not Relevant**  
The retrieved chunk does not contain information required by the expected curriculum content.

Relevance assessment is based on the selected curriculum source rather than external scientific knowledge.

---

### 7.5 Similarity Scores

Similarity scores produced by the retrieval system are preserved as diagnostic information.

They may be used to examine ranking behavior within an experimental setup.

Raw similarity score magnitudes from different embedding model architectures are not treated as directly comparable performance measures unless their scoring procedures are demonstrated to be comparable.

---

## 8. Experimental Matrix

The potential experimental design consists of:

- 3 semantic chunk configurations;
- 2 overlap settings; and
- 3 multilingual embedding models.

This produces up to:

`3 × 2 × 3 = 18 experimental configurations`

The configuration identifiers are:

### Fine-Grained

- A_O0_E1
- A_O0_E2
- A_O0_E3
- A_O1_E1
- A_O1_E2
- A_O1_E3

### Baseline

- B_O0_E1
- B_O0_E2
- B_O0_E3
- B_O1_E1
- B_O1_E2
- B_O1_E3

### Broader

- C_O0_E1
- C_O0_E2
- C_O0_E3
- C_O1_E1
- C_O1_E2
- C_O1_E3

Each distinct configuration will be evaluated using the same 12 predefined queries.

If all 18 conditions remain distinct after implementation validation, the experiment will contain:

`18 configurations × 12 queries = 216 query-condition runs`

With Top-k = 3, this produces:

`216 × 3 = 648 ranked retrieval records`

If an overlap condition produces an identical representation to its corresponding no-overlap condition, it will be documented as non-distinct rather than counted as independent experimental evidence.

---

## 9. Experimental Controls

The following are held constant across experimental comparisons:

- official curriculum source;
- machine-readable curriculum content;
- evaluation queries Q01–Q12;
- expected curriculum content;
- expected content elements;
- retrieval depth (Top-k = 3);
- evaluation rules;
- curriculum language;
- absence of external scientific knowledge; and
- absence of LLM answer generation.

The experimental factors are limited to:

1. chunk configuration;
2. overlap setting; and
3. embedding model.

---

## 10. Raw Result Preservation

Raw retrieval outputs will be preserved before researcher interpretation.

For every query and experimental configuration, raw results will include at least:

- run identifier;
- chunk configuration;
- overlap setting;
- embedding model;
- query identifier;
- query text;
- retrieval rank;
- retrieved chunk identifier;
- retrieved curriculum text; and
- similarity score.

Researcher relevance annotations will be stored separately from the original raw retrieval output.

Raw retrieval results will not be overwritten when annotated or summarized results are produced.

---

## 11. Relevance Annotation

After raw retrieval results are preserved, retrieved chunks will be assessed against the predefined expected curriculum content.

Annotation records will include:

- query identifier;
- retrieved chunk identifier;
- retrieval rank;
- relevance label;
- expected content elements recovered, where applicable; and
- brief annotation notes where clarification is required.

The annotation process will not modify the raw retrieval output.

---

## 12. Reproducibility Metadata

Implementation metadata will be recorded for the retrieval experiments, including where applicable:

- model name;
- model revision or version;
- Python version;
- relevant library versions;
- execution device;
- encoding procedure;
- query formatting;
- document formatting;
- normalization setting;
- similarity method;
- Top-k;
- overlap implementation and value;
- chunk configuration version; and
- execution timestamp.

This information is maintained to support reproducibility of the experimental runs.

---

## 13. Pre-Execution Rules

Before retrieval results are generated:

1. The A, B, and C configurations must be constructed from the machine-readable curriculum source.
2. Complete curriculum coverage must be validated.
3. Source fidelity and source-unit traceability must be checked.
4. Actual chunk-length distributions must be measured.
5. The O1 overlap implementation and value must be fixed.
6. Candidate embedding model implementation procedures must be recorded.
7. Q01–Q12 and their expected curriculum content must be frozen.
8. Top-k must remain fixed at 3.

Once retrieval execution begins, these definitions will not be changed in response to retrieval performance.

If a genuine implementation or source-mapping error is discovered, the error and correction will be documented and all affected runs will be repeated consistently.

### Pre-Execution Source-Mapping Validation Note

During pre-execution source-mapping validation, a cross-page source continuation was identified between `p28_u12` and `p29_u01`.

The two source units form a continuous curriculum statement across pages 28–29. Their semantic mapping was therefore adjusted to preserve source continuity and semantic coherence.

This correction was made before embedding generation, retrieval execution, or inspection of retrieval results.

After the correction, all three experimental chunk configurations were programmatically validated:

- Configuration A: 17 chunks, 63/63 source units covered exactly once.
- Configuration B: 11 chunks, 63/63 source units covered exactly once.
- Configuration C: 9 chunks, 63/63 source units covered exactly once.
- Missing source units: 0.
- Duplicate source units: 0.
- Unknown source units: 0.
---

## 14. Configuration-Level Analysis

For each experimental configuration, the following will be summarized:

- Full Hit@1 rate;
- Full Hit@3 rate;
- Mean Expected Content Coverage@3;
- distribution of Relevant, Partially Relevant, and Not Relevant retrieved chunks;
- query-level retrieval behavior; and
- retrieval behavior across different query types.

No arbitrary weighted composite score will be created.

The final retrieval configuration will be selected based on the combined experimental evidence concerning:

- retrieval accuracy;
- expected curriculum content coverage;
- curriculum relevance;
- consistency across query types; and
- Arabic semantic retrieval behavior.

If configurations demonstrate different strengths and weaknesses, the trade-offs will be reported rather than forcing an unsupported overall ranking.

---

## 15. Interpretation Boundaries

The results of this experiment will be interpreted only within the scope of the selected case study.

The experiment does not establish:

- general superiority of an embedding model;
- educational effectiveness;
- learner performance improvement;
- effectiveness of adaptive progression;
- quality of generated educational packages; or
- generalizability across the complete Palestinian curriculum.

The experiment provides preliminary evidence for selecting a retrieval configuration for the proposed framework.

---

## 16. Limitations

The preliminary retrieval experiment is subject to the following limitations:

- it uses one selected Grade 8 Science curriculum case study;
- the evaluation queries are researcher-constructed;
- the evaluation set is not an externally validated benchmark;
- the curriculum corpus is limited in size;
- the evaluation focuses on retrieval rather than generation;
- relevance assessment includes researcher judgment; and
- findings are specific to the tested retrieval configurations and experimental context.

These limitations will be considered when interpreting and reporting the experimental results.

---

## 17. Transition to Knowledge Base Construction

After the preliminary retrieval experiments are completed, the experimental evidence will be used to select the retrieval configuration for the curriculum knowledge base.

The selected configuration will determine:

- semantic chunk representation;
- overlap setting;
- embedding model; and
- final curriculum embeddings.

The resulting embeddings will then be indexed using the vector-storage approach selected for the framework, such as FAISS or ChromaDB, to enable semantic curriculum retrieval.

The resulting retrieval component will subsequently provide grounded curriculum context to the level-aware generation component of the proposed framework.

The retrieval experiment therefore evaluates the knowledge-grounding layer independently before integration with LLM-based educational content generation.
