# Framework Architecture Design

**Research Title:** A Knowledge-Grounded LLM Framework for Level-Aware Educational Content Generation

**Case Study:** Palestinian Grade 8 Science Curriculum – Cell Division

**Selected RAG Framework:** LlamaIndex

**Version:** 1.0

**Status:** Initial Architecture Design — Proposal-Aligned

## 1. Purpose

The proposed framework aims to generate curriculum-grounded educational content adapted to three learner levels: Basic, Intermediate, and Advanced.

The framework integrates Retrieval-Augmented Generation (RAG), Large Language Models (LLMs), pedagogical differentiation, and rule-based learner assessment and adaptive level recommendations.

The framework is designed to support the generation of structured self-learning educational packages grounded in the official Palestinian Grade 8 Science curriculum.

The three instructional levels follow the same selected curriculum content and relevant official learning objectives. Differences between levels concern the pedagogical presentation and cognitive appropriateness of the generated educational materials rather than the scope of curriculum coverage.

## 2. Core Design Principles

### DP1 — Common Curriculum, Differentiated Instruction

The framework maintains consistent coverage of the selected curriculum content and relevant official learning objectives across Basic, Intermediate, and Advanced instructional levels.

Differentiation concerns instructional presentation, explanation depth, language complexity, scaffolding, and cognitive appropriateness rather than removing essential curriculum content.

All three instructional levels are expected to cover the same selected curriculum topics and relevant official learning objectives, regardless of differences in instructional presentation.

### DP2 — Rule-Based Initial Level Determination

The framework determines the learner's initial instructional level (Basic, Intermediate, or Advanced) using predefined assessment indicators.

A pre-assessment may serve as one source of evidence for initial level determination. The specific indicators, scoring criteria, and any applicable weights or classification rules will be defined during implementation, in accordance with the approved methodology.

Initial level determination follows predefined rules and does not require a separately trained learner-classification model.

### DP3 — Curriculum-Grounded Generation

Generated educational content is grounded in relevant information retrieved from the selected official curriculum through RAG.

The same authoritative curriculum source is used to generate educational content across all three instructional levels.

The retrieved curriculum information provides the knowledge context for generating educational materials aligned with the selected topics and relevant official learning objectives.

### DP4 — Rule-Based Adaptive Level Recommendation

Learner performance is evaluated using predefined criteria to recommend reinforcement, continuation at the current level, or progression to a higher instructional level.

The adaptation mechanism is rule-based and remains within the controlled research implementation.

The specific performance indicators and decision rules will be defined during implementation in accordance with the approved research methodology.

### DP5 — Structured Self-Learning Educational Packages

The framework generates structured self-learning educational packages containing explanations, key vocabulary, practice exercises, and self-assessment questions.

These components are differentiated according to the pedagogical requirements of Basic, Intermediate, and Advanced levels while maintaining consistent coverage of the selected curriculum content.

The package structure remains consistent across instructional levels, while the instructional presentation and cognitive complexity are adapted to the assigned learner level.

## 3. Proposed Framework Components

### 3.1 Curriculum Knowledge Base

The Curriculum Knowledge Base prepares and organizes the selected official curriculum material for retrieval.

It includes:

- Preparing machine-readable curriculum content.
- Segmenting curriculum content into concept-aware semantic chunks.
- Generating vector representations using embedding models.
- Storing vector representations in a vector database.

The knowledge base provides the authoritative curriculum content used by the retrieval component.

### 3.2 Knowledge Retrieval Module

The Knowledge Retrieval Module uses LlamaIndex to retrieve relevant curriculum content from the knowledge base.

Retrieved content is selected according to the educational topic and its relevance to the curriculum.

The retrieved information provides the grounding context for subsequent educational content generation.

### 3.3 Learner Assessment Module

The Learner Assessment Module evaluates learner performance using predefined assessment criteria.

It supports:

- Initial learner assessment to provide evidence for instructional level determination.
- Subsequent performance-based assessment within the selected curriculum case study.
- Assessment results used by the rule-based level determination and adaptation component.

The assessment mechanism is limited to predefined performance indicators and does not require advanced learner modeling.

### 3.4 Rule-Based Level Determination and Adaptation Module

This module applies predefined rules to learner assessment results.

It supports:

- Initial assignment to Basic, Intermediate, or Advanced.
- Recommendation of reinforcement when needed.
- Recommendation of continuation at the current instructional level.
- Recommendation of progression to a higher instructional level when predefined criteria are satisfied.

The module uses predefined assessment indicators and decision rules rather than a separately trained predictive learner model.

The specific rules and thresholds will be established during implementation.

### 3.5 Level-Aware Educational Content Generation Module

This module combines:

- Retrieved official curriculum content.
- The assigned instructional level.
- The corresponding pedagogical profile.
- Structured educational content requirements.

The LLM generates curriculum-grounded educational content appropriate to the assigned learner level.

The three instructional levels use the same underlying curriculum source and relevant official learning objectives while differing in instructional presentation, language complexity, scaffolding, and cognitive appropriateness.

Level-aware generation does not remove essential curriculum topics or learning objectives from any instructional level.

### 3.6 Structured Educational Package Module

This module organizes generated educational content into a structured self-learning package.

Each package includes:

- Explanations.
- Key vocabulary.
- Practice exercises.
- Self-assessment questions.

The package structure remains consistent across the three instructional levels, while the presentation and cognitive complexity are adapted to the assigned level.

### 3.7 Curriculum Coverage Verification

The framework verifies that educational packages generated for Basic, Intermediate, and Advanced levels cover the same selected curriculum topics and relevant official learning objectives.

Differences between levels are limited to pedagogical presentation and cognitive appropriateness.

Coverage verification is performed against the selected curriculum content and relevant official learning objectives.

This verification does not require a separate learner-tracking system.

The specific verification criteria and procedures will be defined during implementation.

## 4. Framework Workflow

The proposed framework follows these steps:

1. **Curriculum Preparation:** The selected official curriculum content is prepared and organized in the Curriculum Knowledge Base.

2. **Initial Learner Assessment:** The learner's initial assessment information is collected using predefined assessment indicators.

3. **Initial Level Determination:** The learner is assigned to Basic, Intermediate, or Advanced using predefined rule-based criteria.

4. **Curriculum Topic Identification:** The relevant curriculum topic and associated learning objectives are identified.

5. **Knowledge Retrieval:** The Knowledge Retrieval Module retrieves relevant curriculum content using LlamaIndex.

6. **Level-Aware Content Generation:** The retrieved curriculum content and the assigned pedagogical profile are provided to the LLM.

7. **Structured Educational Package Generation:** The LLM generates a structured, curriculum-grounded educational package appropriate to the assigned instructional level.

8. **Curriculum Coverage Verification:** The generated educational package is checked for coverage of the selected curriculum topics and relevant official learning objectives, ensuring consistency across all three instructional levels.

9. **Learner Performance Assessment:** Learner performance is evaluated using predefined assessment criteria.

10. **Rule-Based Adaptation:** The framework applies predefined adaptation criteria to recommend reinforcement, continuation at the current instructional level, or progression to a higher level.

This workflow represents the proposed framework within the defined research scope.

The framework maintains consistent curriculum coverage across instructional levels while adapting educational content and learning activities to the learner's assessed level.

## 5. Research Implementation Scope

The implementation uses Lesson 3, "Cell Division" (انقسام الخلايا), from the Palestinian Grade 8 Science curriculum as the selected case study.

The research focuses on designing and testing a knowledge-grounded LLM framework capable of:

- Retrieving relevant content from the selected official curriculum.
- Determining initial instructional levels using predefined assessment indicators and rule-based criteria.
- Generating structured educational packages for Basic, Intermediate, and Advanced levels.
- Maintaining curriculum alignment and consistent coverage of selected curriculum topics and relevant official learning objectives across the three instructional levels.
- Applying rule-based learner assessment and adaptive level recommendations.
- Verifying curriculum coverage within the selected case study.

The implementation is limited to the selected curriculum case study and controlled testing of the proposed framework.

The framework is intended to function as an integrated research prototype rather than a collection of independent retrieval or generation experiments.

The research does not aim to deploy a complete learning management system, develop a separately trained learner-classification model, or conduct a large-scale real-world educational intervention.

## 6. Evaluation and Refinement

The proposed framework will be evaluated through controlled testing and expert-based qualitative evaluation, consistent with the approved research methodology.

The evaluation will examine the generated educational materials in relation to:

- Curriculum alignment.
- Educational content quality.
- Appropriateness for the intended instructional level.

Controlled testing will also examine whether the generated educational packages maintain consistent coverage of the selected curriculum topics and relevant official learning objectives across the three instructional levels.

Expert feedback will inform iterative refinement of the framework and its generated educational materials.

The evaluation is a research activity rather than a separate operational module within the framework.

## 7. Design Details to Be Specified During Implementation

The following implementation details will be defined in accordance with the approved methodology and requirements:

- Initial assessment indicators and assessment questions.
- Predefined scoring criteria and any applicable weights.
- Rule-based criteria for initial learner level determination.
- Rule-based criteria for reinforcement, continuation, and progression.
- Retrieval and generation configurations.
- Level-specific pedagogical profiles.
- Structured educational package format.
- Curriculum coverage verification criteria and procedures.
- Interfaces and data exchange between framework components.
- Controlled testing procedures.
- Expert-based qualitative evaluation criteria and instruments.

These details will be documented during the corresponding implementation and evaluation stages without extending the approved research scope.

## 8. Scope Alignment

The proposed architecture follows the approved research objectives and methodology.

It integrates curriculum-grounded retrieval, level-aware educational content generation, structured self-learning packages, and rule-based learner assessment and adaptation.

Initial learner levels are determined using predefined assessment indicators, while subsequent learner performance informs adaptive recommendations.

All three instructional levels maintain coverage of the same selected curriculum content and relevant official learning objectives, with differentiation limited to pedagogical presentation and cognitive appropriateness.

Curriculum coverage verification is incorporated into the framework workflow without introducing a separate learner-tracking system.

The architecture is intended for controlled implementation and expert-based evaluation using the selected Palestinian Grade 8 Science curriculum case study.

No additional research objectives, independent predictive models, large-scale learner tracking systems, or real-world deployment requirements are introduced.
