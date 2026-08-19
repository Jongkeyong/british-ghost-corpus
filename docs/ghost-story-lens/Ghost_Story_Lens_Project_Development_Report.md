---
title: "Ghost Story Lens: Project Genealogy and Development Report"
author: "Prepared for Jong-Keyong (Jake) Kim"
date: "2026-07-19"
status: "Project record prior to Replit implementation"
---

# Ghost Story Lens: Project Genealogy and Development Report

## Executive Summary

**Ghost Story Lens** began not as a conventional software idea but as a practical literary-critical problem arising from the construction and adjudication of a dissertation corpus of British ghost stories. The initiating question was deceptively simple: **When should a narrative count as a ghost story?** In this conversation, that problem first became concrete through the examination of boundary cases such as Thomas De Quincey’s “The Avenger” and the occult narrative discussed as “The Incantation.” These cases demonstrated that supernatural atmosphere, apparitional language, or unexplained terror does not by itself establish the presence of a ghost, and that a narrative may remain close to the ghost-story tradition while centering human revenge, demonic entities, elemental agencies, hallucination, fraud, or metaphorical spectrality instead.

From those corpus-level classification decisions, the project developed into a proposal for an explainable digital-humanities web application. The application would allow a user to upload a literary text or paste it into an interface, evaluate that text against a transparent and revisable rubric, locate it on a 1–10 **Ghost-Story Fit Spectrum**, and show the passages that support and complicate the result. The project’s most distinctive innovation became the **Relational Manifestation Map**, an interactive network showing how a ghost or apparent spectral entity becomes perceptible through objects, spaces, sounds, bodies, documents, atmospheres, technologies, and other mediators before being encountered by one or more ghost-seers.

The project evolved through several stages: literary boundary adjudication; product naming and positioning; development of a provisional eight-criterion rubric; separation of genre fit, entity ontology, and analytical confidence; design of a corpus-comparison and rubric-revision workflow; creation of the interactive network specification; development of a restrained, non-stereotypically Gothic visual language; definition of multilingual and accessibility requirements; specification of JPG and PDF exports; and conversion of the accumulated design into a formal **Product Requirements Document (PRD)** for implementation in Replit.

The principal completed deliverable is **Ghost_Story_Lens_PRD_v1.0.docx**, accompanied by an architecture diagram, a network mockup, and a concise Replit kickoff prompt. A functioning production web application has **not yet** been built. The work completed in this conversation constitutes an implementation-ready conceptual, methodological, visual, and technical specification.

---

## 1. Origin of the Project

### 1.1 The immediate problem: corpus adjudication

The project originated in the recurring need to decide whether difficult literary works belonged in the dissertation’s ghost-story corpus. The early exchanges did not begin with a request to build software. They began with the question, **“Can this story be considered a ghost story?”**

The analysis of “The Avenger” established an important negative case. Although the narrative produces an atmosphere of invisible pursuit, recurrent terror, and the return of a violent past, its apparent supernatural menace is ultimately attributed to human actors and ordinary means. The story therefore resembles a haunting at the level of structure and affect without presenting an actual dead human agent. It was provisionally classified as a **borderline Gothic or spectral-adjacent narrative**, rather than as a core ghost story.

The subsequent analysis of “The Incantation” refined the boundary further. That work contains extraordinary apparitions and sustained occult phenomena, yet the entities are represented primarily as demonic, elemental, or nonhuman spiritual agencies rather than as returning human dead. The distinction showed that the occurrence of words such as *specter*, *spirit*, or *apparition* cannot, by itself, determine genre membership.

These cases revealed a methodological difficulty already present in the dissertation corpus: classification depended on tacit judgment, but those judgments needed to become explicit, contestable, and reproducible.

### 1.2 The larger dissertation context

The application concept emerged from Chapter 4’s broader investment in distributed haunting. The dissertation framework treats spectral agency as relational rather than self-contained. Ghosts become efficacious through architecture, objects, atmosphere, bodily sensation, documents, legal and economic instruments, technologies of inscription and transmission, and the interpretive activity of witnesses.

This context supplied the foundational triad later formalized in the application:

> **spectral source → mediator → attuned perceiver or ghost-seer**

The web application was therefore conceived not merely as a genre classifier, but as a way to operationalize and display the dissertation’s relational account of haunting.

---

## 2. Initial Research Problem and Purpose

The application addresses a problem at the intersection of literary genre studies, corpus construction, computational literary studies, and explainable AI.

Conventional classifications often rely on anthology precedent, keyword matching, an unarticulated sense of “ghostliness,” or a narrow requirement that a visibly embodied dead person appear. Such approaches can obscure important distinctions among human ghosts, revenants, demons, elemental spirits, vampires, doubles, fairies, psychic projections, hallucinations, fraudulent apparitions, technological traces, and metaphorical specters.

At the same time, a rigid yes-or-no definition would contradict the project’s literary premise. Ghost-story status is often gradual, historically contingent, and open to revision. A story may contain a confirmed dead human agent but place that figure at the margin of the plot. Another may never confirm the apparition’s ontology while organizing its entire narrative around postmortem return. A third may feature powerful manifestations that belong to a different supernatural category.

The project was therefore designed to accomplish four related purposes:

1. make the grounds of ghost-story classification explicit;
2. replace binary judgment with a graded and interpretable spectrum;
3. show how haunting is relationally mediated and perceived; and
4. allow difficult texts to challenge and revise the criteria used to classify them.

The governing methodological premise became:

> **Genre classification is an interpretive argument supported by textual evidence, not the discovery of an objectively fixed property.**

---

## 3. Governing Research Questions

The project’s research questions emerged iteratively rather than appearing all at once. In their mature form, they are as follows.

### 3.1 Primary research question

**How can a corpus-grounded and explainable AI system evaluate where a literary text falls on a ghost-story spectrum while preserving the interpretive, historical, and revisable character of genre classification?**

### 3.2 Supporting research questions

1. **What textual relations distinguish a ghost story from adjacent Gothic and supernatural forms?**

2. **How can the system distinguish a dead human ghost or revenant from a demon, elemental spirit, vampire, double, fairy, hallucination, fraud, dream figure, technological trace, or metaphorical specter?**

3. **How does a ghost become perceptible through material, spatial, sensory, documentary, technological, atmospheric, bodily, or interpersonal mediation?**

4. **Who functions as a ghost-seer, witness, interpreter, investigator, recipient of testimony, or bodily sensor of the haunting?**

5. **What passages support the classification, and what passages contradict, complicate, or rationalize it?**

6. **How can the application distinguish Ghost-Story Fit from analytical confidence and supernatural-entity type?**

7. **When does a submitted text expose a limitation in the current rubric, and how can the system propose a revision without silently changing the official criteria?**

8. **How can the application remain accessible to undergraduates while retaining enough methodological specificity for graduate students, instructors, and scholars?**

9. **How can multilingual analysis preserve the original language of evidence while producing explanations in the user’s selected language?**

10. **How can AI-assisted literary interpretation remain inspectable, versioned, reproducible, and subject to human correction?**

---

## 4. Intellectual Provenance of the Classification Criteria

A later exchange in this conversation clarified who contributed what to the present rubric.

### 4.1 Elements supplied by Jong-Keyong (Jake) Kim

The researcher supplied the historical corpus, dissertation framework, and substantive literary commitments from which the application grew. These included:

- the British ghost-story corpus and its chronological frame of 1764–1913;
- the need to distinguish ghost stories from broader Gothic and supernatural fiction;
- repeated inclusion and exclusion decisions concerning ambiguous apparitions, hoaxes, demons, vampires, doubles, fairies, werewolves, and related forms;
- the principle that spectral vocabulary alone cannot determine genre;
- the importance of plot, causation, perception, evidence, material mediation, and historical return;
- the ghost–mediator–seer model;
- the view that ghostly agency may be distributed through objects, architecture, atmosphere, documents, economic instruments, and technologies;
- the preference for a spectrum rather than a binary classifier; and
- the requirement that anomalous texts should be capable of exposing limitations in the computational ontology.

### 4.2 Elements formalized by ChatGPT

ChatGPT translated those premises into a product-level analytical instrument. This work included:

- the provisional eight-criterion rubric;
- numerical criterion weights;
- the 1–10 score bands;
- classification labels such as **Spectral-Adjacent Narrative** and **Paradigmatic Ghost Story**;
- the separation of Ghost-Story Fit, entity ontology, and analytical confidence;
- the multi-pass analysis workflow;
- the structured network data model;
- the rubric-gap and revision procedure;
- the visual and interaction specifications; and
- the formal PRD.

The most accurate statement of authorship is therefore:

> **The Ghost Story Lens rubric is an AI-assisted operationalization of Jong-Keyong Kim’s dissertation framework, corpus decisions, and iterative genre adjudications.**

The rubric has not yet been frozen as an authoritative scholarly standard. Its criteria, weights, and thresholds remain provisional pending expert review and benchmark validation.

---

## 5. Development of the Product Concept

### 5.1 Naming and public positioning

The project required a name intelligible to people unfamiliar with the dissertation. **Ghost Story Lens** was selected because *lens* conveys an interpretive instrument rather than an infallible detector.

The associated public-facing question became:

> **How ghostly is this story—and why?**

The basic description was refined into the following product claim:

> Ghost Story Lens is an explainable, corpus-grounded literary analysis platform that places texts on a revisable ghost-story spectrum, identifies the evidence behind its classification, distinguishes ghosts from adjacent supernatural forms, maps how manifestations are mediated and perceived, and allows users to challenge both the analysis and its underlying criteria through dialogue with AI.

### 5.2 From binary classification to a spectrum

A central design decision was to reject language such as “82% likely to be a ghost story.” Such phrasing would misrepresent the score as a probability and suggest that genre is an objectively measurable natural property.

The application instead reports a **Ghost-Story Fit score** from 1.0 to 10.0. The score measures correspondence with the current rubric and comparison corpus. It is accompanied by a category, a separate confidence rating, the rubric version, and the corpus calibration statement.

The provisional bands are:

| Score | Category | General interpretation |
|---|---|---|
| 1.0–2.4 | Not a Ghost Story | Little or no narratively consequential postmortem presence |
| 2.5–4.4 | Spectral-Adjacent Narrative | Ghostly language, atmosphere, or apparitions without a central human ghost |
| 4.5–6.4 | Borderline or Ambiguous Ghost Story | Substantial spectral evidence complicated by uncertainty, rationalization, or another supernatural category |
| 6.5–8.4 | Strong Ghost Story | A deceased human presence substantially shapes plot, setting, or interpretation |
| 8.5–10.0 | Paradigmatic Ghost Story | A central and causally effective ghost organizes conflict, return, and resolution |

### 5.3 The provisional eight-criterion rubric

The rubric developed through the conversation contains the following dimensions:

| Criterion | Initial weight | Central question |
|---|---:|---|
| Postmortem Identity | 20% | Is the entity a once-living human being who has died? |
| Manifestation | 15% | How does the entity become perceptible? |
| Causal Agency | 15% | Does the ghost alter events, knowledge, bodies, property, or resolution? |
| Narrative Centrality | 15% | Is the apparent haunting indispensable to the story’s principal structure? |
| Structure of Return | 10% | Does the narrative bring an unresolved past into the present? |
| Ontological Status | 10% | Is the manifestation confirmed, ambiguous, rationalized, psychological, fraudulent, or otherwise explained? |
| Mediation and Perception | 10% | Through whom or what does the ghost become perceptible? |
| Generic Function | 5% | What does spectrality accomplish within the narrative? |

The application is designed so that the AI returns structured evidence and criterion judgments, while deterministic code calculates the final weighted score and category.

### 5.4 Entity classification as a separate analytical layer

The project next separated genre fit from entity type. The application may classify an apparent entity as one or more of the following:

- human ghost or revenant;
- ancestral ghost;
- ambiguous apparition;
- nonhuman spirit;
- demon or infernal entity;
- elemental or occult agency;
- vampire;
- werewolf;
- fairy;
- double or doppelgänger;
- psychic projection;
- dream or hallucination;
- fraudulent supernatural appearance;
- technological trace;
- metaphorical specter; or
- unexplained phenomenon.

This layer prevents a text from being classified as a ghost story merely because it contains supernatural vocabulary or dramatic apparitions.

### 5.5 Confidence as distinct from fit

Analytical confidence was introduced as a separate result. A text can receive a low Ghost-Story Fit score with high confidence if the evidence clearly identifies a demon rather than a ghost. Conversely, a text can receive a moderately high fit score with low confidence when its apparition remains ontologically unstable or the source text is incomplete.

This distinction prevents uncertainty from being hidden inside the genre score.

---

## 6. The Relational Manifestation Map

The network visualization became the project’s signature feature.

### 6.1 Conceptual purpose

The map is not a generic character network and is not based merely on co-occurrence. It is designed to show **how the haunting works** by modeling relational pathways among a spectral source, mediating elements, and ghost-seers.

Examples include:

> Ghost → Portrait → Narrator

> Ghost → Locked Room → Footsteps → Housekeeper

> Ghost → Direct Visual Appearance → Clara

### 6.2 Node system

The final specification distinguishes three primary node types.

**Ghost or apparent entity node**

- placed centrally by default;
- rendered in pearl or mist gray with a deep-navy outline;
- labeled by name or by a qualified descriptive identity;
- marked visibly when its ontology is uncertain.

**Mediator nodes**

- rendered in deep navy;
- presented as single-ring nodes;
- divided into exactly three sizes: primary, significant, and supporting;
- sized according to narrative importance rather than frequency alone.

Narrative importance considers causal centrality, distribution across scenes, climactic relevance, interpretive emphasis, and necessity to the manifestation pathway.

**Ghost-seer nodes**

- rendered in emerald;
- displayed with two concentric rings;
- labeled by proper name or a stable narratological role;
- distinguished among visual, auditory, tactile, dream, technologically mediated, and indirect forms of perception.

### 6.3 Edge system and interaction

Edges encode relations such as *manifests through*, *appears in*, *speaks through*, *recorded by*, *perceived by*, *heard by*, *felt by*, *interpreted by*, and *reported to*.

Solid edges represent explicit textual relations, while dashed edges represent inferred, contested, or ambiguous relations. Edge thickness indicates narrative strength or recurrence.

The interactive map allows users to hover, select nodes and edges, inspect evidence, filter relation types, focus on an individual seer’s pathway, drag nodes, zoom, pan, reset the layout, dispute interpretations, add missing mediators, change importance levels, and preserve user revisions alongside the original model output.

### 6.4 Static exports

The map remains interactive in the web application, but users may also download:

- the analysis summary as a JPG;
- the relational map as a JPG; and
- a combined analysis-and-network report as a PDF.

The combined PDF is specified as a multipage research report containing the classification summary, evidence and criterion overview, full network visualization, legend, interpretive statement, rubric version, model version, output language, analysis date, creator attribution, and contact information.

---

## 7. Analysis Workflow and Technical Logic

The project moved away from a single unrestricted prompt toward a staged analysis pipeline.

### 7.1 Submission

Users may paste text or upload TXT, DOCX, or text-based PDF files. Optional metadata include title, author, publication date, source, and language. Image-only or severely degraded PDFs are deferred because unreliable OCR could materially distort literary analysis.

### 7.2 Analytical modes

The application defines three modes:

- **Corpus-Calibrated Mode**, initially calibrated on British ghost fiction from 1764 to 1913;
- **Comparative Mode**, which applies the rubric experimentally to other periods and traditions; and
- **Custom Rubric Mode**, which allows authorized users to modify criteria, weights, and category boundaries without overwriting the default rubric.

### 7.3 Multi-pass AI workflow

The proposed pipeline includes:

1. text cleaning and passage indexing;
2. entity and event extraction;
3. criterion evaluation;
4. adversarial counterevidence search;
5. relational network extraction;
6. corpus comparison;
7. rubric-gap analysis; and
8. multilingual report generation.

The model is responsible for evidence extraction, structured interpretation, entity classification, network proposals, rubric-gap detection, and research dialogue. Deterministic application code is responsible for arithmetic, score bands, node-size tiers, schema validation, evidence-reference checks, versioning, storage, and exports.

### 7.4 Rubric-gap analysis

One of the project’s most original features is the ability to ask what narratively significant evidence is not represented by any existing criterion.

A text might, for example, present postmortem agency only through a photograph, recording, ledger, architectural vibration, or unstable atmosphere. The system may propose clarifying an existing criterion, splitting one criterion into subcategories, adding a new criterion, or modifying a weight. It must also preview possible effects and unintended consequences.

No proposal can silently alter the official rubric. A user with appropriate authority must approve the change, supply a rationale, and create a new version while preserving the previous one.

---

## 8. Audience, Accessibility, and Multilingual Design

### 8.1 Intended users

The application is designed for:

- undergraduates learning genre analysis and evidence-based interpretation;
- graduate students moving between close reading and formal analysis;
- instructors demonstrating the contingency of literary categories; and
- scholars documenting corpus membership and revising analytical ontologies.

Two presentation levels were defined:

- **Reader View**, emphasizing plain-language explanation and concise evidence; and
- **Research View**, exposing criterion weights, network data, passage annotations, version metadata, counterevidence, and exportable structures.

### 8.2 Multilingual requirements

The initial plan includes interfaces and reports in:

- English;
- Korean;
- Simplified Chinese;
- Traditional Chinese;
- Japanese;
- German;
- French;
- Spanish; and
- Hindi.

The project explicitly distinguishes source-text language, interface language, and output language. Original-language evidence remains visible, with optional translations beneath it. Texts outside the British English calibration are labeled as cross-linguistic exploratory analyses rather than treated as culturally neutral classifications.

### 8.3 Accessibility

Accessibility requirements include keyboard-operable network nodes, screen-reader descriptions, sufficient contrast, scalable text, reduced-motion support, visible focus states, and distinctions conveyed through shape and border as well as color.

---

## 9. Visual and Brand Development

The product’s visual identity was deliberately separated from stereotypical Gothic entertainment.

The interface avoids blackletter fonts, predominantly black backgrounds, blood-red accents, candles, ravens, skulls, gravestones, distressed paper, cartoon ghosts, and jump-scare imagery. Its governing metaphor is the **lens**, not the haunted house.

The palette is restrained:

| Function | Color |
|---|---|
| Primary interface and mediator nodes | Deep Navy |
| Ghost-seers and active states | Emerald |
| Main background | Warm Paper |
| Secondary surfaces and ghost node | Mist Gray |
| Main text | Graphite |

The 1–10 spectrum uses a mist-to-navy progression with an emerald position marker rather than a rainbow.

The body typeface is specified as **Aptos Body at 13 pt**, supported by a fallback system stack. Explanatory copy in the About section begins each sentence on a new visual line to improve readability.

The site structure includes Home, Analyze, Results, Sample Analysis, and About.

---

## 10. The About Section and Scholarly Disclosure

The About section was developed as a substantive methodological statement rather than a decorative modal. It explains, in an intentionally reordered sequence:

1. why the application was created;
2. whom it serves;
3. how to use it;
4. what results it produces;
5. what can be exported;
6. what its limitations are; and
7. what responsibilities remain with the user.

A second paragraph describes the technical design. The PRD records that the concept and product documentation were developed in ChatGPT with GPT-5.6 Thinking, that the production application is planned for Replit, and that GPT-5.6 Sol is intended to support structured analysis through the OpenAI API. Because model identifiers and capabilities can change, these implementation details will need to be verified at build time.

The creator attribution is:

> **Created by Jong-Keyong (Jake) Kim**

The contact for questions, corrections, and revision suggestions is:

> **tsbym00@gmail.com**

---

## 11. Completed Deliverables

### 11.1 Conceptual and methodological outputs

The conversation produced:

- a public-facing product name and tagline;
- a concise product description;
- a statement of methodological principles;
- a provisional genre spectrum;
- an eight-criterion scoring rubric;
- a separate entity ontology;
- a confidence model distinct from genre fit;
- a staged AI analysis pipeline;
- a rubric-gap and revision workflow;
- multilingual and accessibility specifications;
- privacy and scholarly-control principles; and
- an evaluation and validation plan.

### 11.2 Visual and interaction outputs

The project also produced:

- a non-stereotypically Gothic visual direction;
- a restricted color system;
- typography and layout specifications;
- an About-page content plan;
- the interactive Relational Manifestation Map specification;
- node, edge, filtering, evidence, and correction behaviors;
- JPG export requirements for the summary and map; and
- a combined PDF-report specification.

### 11.3 Formal implementation outputs

The principal formal artifacts are:

1. **Ghost_Story_Lens_PRD_v1.0.docx** — the complete Product Requirements Document;
2. **architecture.png** — a supporting architecture diagram;
3. **network_mockup.png** — a supporting network-visualization mockup; and
4. a concise **Replit kickoff prompt** instructing the development environment to use the PRD as the source of truth, preserve the signature features, implement structured outputs and deterministic scoring, document deviations, add tests, and provide deployment instructions.

The project has therefore reached the transition point from research and product specification to software implementation.

---

## 12. What Has Not Yet Been Completed

The following items remain pending:

- implementation of the functioning web application in Replit;
- formal review and freezing of the rubric’s criteria, weights, and thresholds;
- construction of a human-annotated benchmark;
- inter-annotator agreement and adjudication procedures;
- validation of entity classification and network relations;
- creation of a deliberate contrast corpus containing non-ghost supernatural and Gothic cases;
- multilingual source-language testing;
- prompt-sensitivity and model-version testing;
- final decisions about input length, storage, authentication, and custom rubrics;
- verification of current API model names and capabilities;
- production-level privacy, copyright, and deletion policies; and
- usability and accessibility testing with the intended audiences.

The present PRD treats these matters as development or validation requirements rather than as completed achievements.

---

## 13. Current Methodological Significance

Ghost Story Lens has developed beyond a tool that asks whether a text contains a ghost. Its current design embodies a more consequential humanities argument.

First, genre is treated as historically situated and relational rather than as an intrinsic property discoverable by keyword matching. Second, the application makes its interpretation visible through passages, criteria, confidence, entity types, and corpus comparisons. Third, it models haunting as an arrangement among spectral sources, mediators, and perceivers. Fourth, it treats classification failure as potentially meaningful: a model-resistant story may disclose a weakness in the rubric or a form of spectral agency that exceeds discrete computational categories.

The project thus joins corpus construction, close reading, ontology design, visualization, and human–AI dialogue. Its intended contribution is not to automate literary judgment away, but to make the grounds, uncertainties, and revisions of that judgment available for inspection.

---

## 14. Recommended Next Step

Before full implementation, the most important scholarly task is to review and freeze **British Ghost Story Criteria v1.0**. That process should examine each criterion, its definition, its weight, the score bands, and representative positive, negative, and borderline texts.

Once the rubric is provisionally frozen, the Replit build can proceed against a stable methodological target. The first testing cycle should use a small benchmark containing unequivocal ghost stories, rationalized hauntings, demonic narratives, Gothic crime stories, ambiguous apparitions, nonhuman spirits, and model-resistant texts. The resulting disagreements should be documented as part of the application’s scholarly development rather than treated merely as software defects.

---

## Conclusion

Ghost Story Lens began with the practical difficulty of deciding whether individual works belonged in a dissertation corpus. Through sustained dialogue, that difficulty became a broader research project about how genre boundaries are made, explained, visualized, challenged, and revised. The project progressed from close readings of boundary cases to a corpus-informed spectrum, from a score to an evidence system, from an isolated ghost to a relational manifestation network, and from a conceptual sketch to a formal PRD prepared for Replit development.

Its most important achievement to date is not a finished classifier, but an articulated methodological architecture. That architecture preserves the researcher’s literary judgment, makes AI-supported claims inspectable, and allows the texts themselves to contest the categories designed to contain them.
