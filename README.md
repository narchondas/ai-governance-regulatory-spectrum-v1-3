# ai-governance-regulatory-spectrum-v1-3

A reproducible NLP-based artefact for mapping EU and US AI governance documents on a regulatory spectrum.

<img width="1448" height="1086" alt="image" src="https://github.com/user-attachments/assets/11a304c6-2eff-477a-8b31-9c4bc5606f23" />

# AI Governance Regulatory Spectrum Artefact v1.3

## Overview

This repository contains a reproducible NLP-based artefact developed for a comparative analysis of artificial intelligence governance in the European Union and the United States.

The artefact processes EU and US AI governance documents and positions them on a two-dimensional regulatory spectrum:

- **X-axis:** rights- and citizen-oriented safeguards ↔ innovation
  
- **Y-axis:** voluntary/soft-law ↔ mandatory/control

The project uses PDF text extraction, tokenisation, lemmatisation, predefined analytical vocabularies, relative frequency calculations and document-level legal-force multipliers.

## Purpose

The objective of this repository is twofold:

1. to allow reproduction of the thesis artefact using the same 24-document corpus;
2. to provide a reusable notebook that other researchers may adapt to test additional AI governance documents.

<img width="1448" height="1086" alt="image" src="https://github.com/user-attachments/assets/82b3a8df-4a1e-4b99-8114-ade6eaad375c" />

## Final model version

The final model used in the thesis is **v1.3**.

The key modelling decisions are:

- no word-level weights are applied;
- all vocabulary terms and phrases count as one occurrence;
- the only weighting mechanism is the document-level legal-force multiplier applied to the mandatory/control count;
- broad legal-context terms such as `law`, `regulation`, `rule`, `rules`, `authority` and `authorities` are excluded from the mandatory/control vocabulary;
- implementation and control terms such as `monitoring`, `supervision`, `market surveillance`, `ensure` and `liability` are retained.

## Repository structure

```text
ai-governance-regulatory-spectrum-v1-3/
│
├── README.md
├── requirements.txt
│
├── notebooks/
│   ├── AI_Governance_Regulatory_Spectrum_Artefact_v1_3_Replication.ipynb
│   └── AI_Governance_Regulatory_Spectrum_Artefact_v1_3_Custom_Test.ipynb
│
├── data/
│   ├── corpus_metadata_v1_3.csv
│   └── vocabulary_codebook_v1_3.xlsx
│
├── documents/
│   └── 24 public EU and US AI governance PDF documents
│
├── outputs/
│   └── exported Excel and HTML outputs
│
└── docs/
    └── methodological annex and supporting documentation
