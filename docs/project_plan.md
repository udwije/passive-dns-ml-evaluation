# Project Planning Document  
## Passive DNS Machine Learning Evaluation  
**BSc Cybersecurity Dissertation**

---

## 0. Project Contract (Frozen)

These elements are **fixed** once the proposal is approved.

- **Problem Domain:** DNS security
- **Approach:** Passive monitoring only
- **Detection Method:** Lexical machine learning
- **Purpose:** Evaluation and feasibility study
- **Outcome:** Dissertation + reproducible prototype

Any change to the above requires supervisor re-approval.

---

## 1. Research Definition Phase (Week 1)

### Purpose
Establish a clear, defensible research contract and prevent scope drift.

### Key Decisions
- Finalise research questions (RQ1–RQ3)
- Confirm evaluation-first framing
- Confirm passive-only constraint

### Deliverables
- Approved proposal
- Ethics application submitted
- Supervisor approval email archived

### Exit Criteria
- Supervisor confirms topic and scope
- No objections to methodology or ethics framing

---

## 2. Background & Literature Review Phase (Week 1–2)

### Objectives
- Establish cybersecurity relevance
- Identify research gap
- Support methodology choices

### Focus Areas
- DNS abuse techniques (phishing, malware, C2)
- Malicious domain generation (DGA concepts)
- Lexical analysis of domain names
- ML-based DNS threat detection
- Limitations of static blocklists
- Real-time vs offline detection trade-offs

### Deliverables
- Literature review outline
- Annotated reference list (15–25 papers)
- Clear gap statement:
  > Most existing work evaluates offline accuracy rather than real-time feasibility.

### Constraints
- Do not summarise papers unnecessarily
- Cite only papers you actually reference in argumentation

---

## 3. Dataset Preparation Phase (Week 2–3)

### Objective
Prepare clean, labelled datasets suitable for supervised learning.

### Data Sources
- Public benign domain datasets
- Public malicious domain datasets (phishing, malware)

### Tasks
- Normalise domain names (lowercase, remove protocol)
- Deduplicate domains
- Label domains clearly (benign / malicious)
- Handle class imbalance (document, do not overcorrect)
- Split dataset:
  - Training set
  - Validation set
  - Test set

### Deliverables
- Dataset summary table
- Dataset assumptions and limitations
- Reproducible preprocessing scripts

### Exit Criteria
- Dataset frozen before feature engineering

---

## 4. Feature Engineering Phase (Week 3–4)

### Objective
Extract features that are:
- Lexical only
- Efficient to compute
- Suitable for real-time inference

### Feature Categories

#### Basic Lexical Features
- Domain length
- Subdomain count
- Digit ratio
- Hyphen count
- Vowel-to-consonant ratio

#### Statistical Features
- Shannon entropy
- Character frequency distribution
- Character transition probabilities

#### N-gram Features
- Character n-grams (e.g. 2-gram, 3-gram)
- Normalised frequency vectors

### Constraints
- No DNS payload inspection
- No IP, WHOIS, or reputation data
- No content-based features

### Deliverables
- Final feature list
- Feature extraction scripts
- Feature rationale for dissertation

### Exit Criteria
- Feature set locked and documented

---

## 5. Machine Learning Phase (Week 4–6)

### Objective
Evaluate supervised ML models for malicious domain classification.

---

### 5.1 Problem Formulation

- **Task:** Binary classification (benign vs malicious)
- **Input:** Feature vectors derived from domain names
- **Output:** Class label + confidence score

---

### 5.2 Model Selection

#### Primary Model
- Random Forest classifier

Rationale:
- Handles non-linear feature interactions
- Robust to noise
- Interpretable feature importance

#### Secondary Model (Optional)
- Logistic Regression or Gradient Boosting

Used for comparison only.

---

### 5.3 Training Phase

#### Steps
- Train models on training dataset
- Use validation dataset for limited tuning
- Avoid excessive hyperparameter optimisation

#### Constraints
- No data leakage
- No test data used during training
- Document all parameters used

---

### 5.4 Evaluation Phase (Offline)

#### Metrics
- Precision
- Recall
- F1-score
- ROC-AUC
- False positive rate

#### Outputs
- Confusion matrix
- Performance comparison table
- Baseline comparison with static blocklists

---

### 5.5 Model Selection for Deployment

Criteria:
- Balanced precision and recall
- Acceptable false positive rate
- Low inference latency

### Exit Criteria
- One model selected for real-time inference
- Results reproducible from scripts

---

## 6. Real-Time Integration Phase (Week 6–8)

### Objective
Demonstrate feasibility of real-time DNS inference.

### High-Level Architecture

[ DNS Capture ]
|
[ Domain Extraction ]
|
[ Feature Extraction ]
|
[ ML Inference ]
|
[ Logging / Visualisation ]


### Tasks
- Passive DNS capture using packet capture libraries
- Extract queried domain names only
- Perform per-query feature extraction
- Perform stateless ML inference
- Log results for later analysis

### Constraints
- No traffic blocking
- No response modification
- No PII storage
- Graceful failure handling

### Deliverables
- Working passive pipeline
- Latency measurement per query
- Stability observations

---

## 7. Evaluation Phase (Week 8–9)

### Experiments

1. Offline ML performance evaluation  
2. Comparison against static blocklists  
3. Real-time inference latency measurement  
4. False positive behaviour under live or replayed traffic  

### Metrics
- Detection accuracy
- Processing latency (mean, max)
- False positive rate
- System stability over time

### Deliverables
- Results tables
- Graphs (accuracy vs latency)
- Experimental observations

---

## 8. Results & Analysis Phase (Week 9–10)

### Analysis Focus
- Interpretation of results
- Trade-offs between accuracy and latency
- Comparison with baseline approaches
- Practical feasibility

### Rules
- Do not overclaim
- Negative or weak results are valid
- Tie every conclusion to data

### Deliverables
- Results section
- Analysis section
- Limitations section

---

## 9. Dissertation Writing Phase (Parallel)

### Structure
1. Introduction
2. Background & Literature Review
3. Methodology
4. System Design & Implementation
5. Experimental Evaluation
6. Results & Analysis
7. Limitations
8. Conclusion & Future Work

### Writing Rules
- Past tense for experiments
- Neutral academic language
- Cite all non-obvious claims

---

## 10. Final Review Phase

### Checklist
- Research questions answered
- Methodology matches implementation
- Ethics constraints respected
- Figures and tables referenced
- Repository matches dissertation claims

### Deliverables
- Final dissertation
- Clean Git repository
- Supervisor sign-off (if required)

---

## Risk Register

| Risk | Mitigation |
|----|----|
| Poor ML performance | Discuss limitations |
| High false positives | Emphasise trade-offs |
| Capture issues | Use traffic replay |
| Scope creep | Follow this plan |
| Ethics concerns | Maintain passive framing |

---

## Success Criteria

- Passive DNS analysis demonstrated
- Quantitative ML evaluation completed
- Reproducible methodology
- Honest discussion of limitations
- Clear cybersecurity contribution

---
