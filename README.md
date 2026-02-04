# Passive DNS Machine Learning Evaluation

## Overview

This repository contains a research prototype and experimental framework developed as part of a **BSc Cybersecurity dissertation**.  
The project evaluates the feasibility and effectiveness of **lexical machine-learning-based detection of malicious domains** in a **passive DNS monitoring context**.

The primary focus of this work is **measurement and evaluation**, not deployment or enforcement.  
All components are designed to support reproducible experimentation under controlled conditions.

---

## Research Scope

### In Scope
- Passive DNS query observation
- Lexical and statistical feature extraction from domain names
- Supervised machine learning classification
- Offline model training
- Real-time (online) inference for evaluation purposes
- Quantitative performance analysis

### Out of Scope
- Traffic blocking or enforcement
- DNS response manipulation
- Deep packet inspection beyond DNS headers
- User, host, or endpoint attribution
- Content-based threat detection

---

## Methodology Summary

At a high level, the project follows the pipeline below:
```
[ DNS Traffic ]
|
[ Passive Capture ]
|
[ Domain Extraction ]
|
[ Feature Engineering ]
|
[ ML Classification ]
|
[ Evaluation & Metrics ]
```
- Models are trained offline using publicly available datasets.
- Inference is performed in a passive, real-time monitoring context.
- Results are logged and visualised to support analysis.
- The system remains stateless on a per-query basis.

---

## Repository Structure
```
├── data/ # Dataset references and preprocessing scripts
├── features/ # Feature extraction and engineering logic
├── models/ # Trained models and evaluation scripts
├── capture/ # Passive DNS capture components
├── inference/ # Real-time classification pipeline
├── tui/ # Terminal-based visualisation components
├── evaluation/ # Metrics, analysis, and result aggregation
├── docs/ # Project documentation and diagrams
└── README.md
```

Directory names may evolve as the project progresses, but the separation between **data**, **models**, **capture**, and **evaluation** is maintained.

---

## Data Sources

The project uses **publicly available datasets** for training and evaluation, including:
- Benign domain datasets
- Malicious domain datasets related to phishing and malware activity

No proprietary or private datasets are used.

---

## Evaluation Metrics

Performance is assessed using standard security and operational metrics, including:

- Precision
- Recall
- F1-score
- False positive rate
- Per-query processing latency

Where applicable, results are compared against **static DNS blocklists** as a baseline.

---

## Ethical Considerations

This project has been designed to minimise ethical and legal risk.

- DNS traffic is observed **passively**
- No traffic is modified or blocked
- No payload content is stored
- No personally identifiable information (PII) is collected
- Analysis is limited to domain name strings only

The system operates solely for **research and evaluation purposes**.

---

## Reproducibility

The repository is structured to support reproducible experimentation:

- Feature extraction and model training scripts are version-controlled
- Evaluation metrics are computed using deterministic methods
- Experimental assumptions and limitations are documented

Exact reproduction may depend on dataset availability and environment configuration.

---
