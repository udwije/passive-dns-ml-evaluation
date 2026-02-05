# 14-Week Project Timeline

## Phase 1: Foundation & Data (Weeks 1-4)

### Week 1: Project Setup & DNS Protocol
- [ ] Finalize project scope and research questions
- [ ] Set up development environment
- [ ] Study DNS protocol (RFC 1035)
- [ ] Create project directory structure
- **Deliverable:** Working environment + DNS understanding

### Week 2: Data Collection
- [ ] Download malicious domains (URLHaus, PhishTank)
- [ ] Download benign domains (Alexa Top 1M)
- [ ] Initial data cleaning and validation
- [ ] Document data sources and ethics
- **Deliverable:** 60,000+ domain dataset

### Week 3: Feature Engineering
- [ ] Implement 15+ lexical feature extractors
- [ ] Validate feature extraction on sample data
- [ ] Document feature definitions and rationale
- [ ] Create feature configuration file
- **Deliverable:** Feature extraction pipeline

### Week 4: ML Model Foundation
- [ ] Set up ML training environment
- [ ] Implement Random Forest classifier
- [ ] Baseline: Logistic Regression
- [ ] Initial training on small dataset
- **Deliverable:** Working ML training pipeline

## Phase 2: Core Development (Weeks 5-8)

### Week 5: Model Training & Optimization
- [ ] Train on full dataset (50,000+ samples)
- [ ] Hyperparameter tuning
- [ ] Cross-validation evaluation
- [ ] Model performance baseline
- **Deliverable:** Optimized Random Forest model

### Week 6: Rust TUI Foundation
- [ ] Learn Rust basics and TUI frameworks
- [ ] Set up Rust project structure
- [ ] Implement basic TUI layout
- [ ] Create DNS packet capture skeleton
- **Deliverable:** Basic Rust TUI framework

### Week 7: DNS Packet Processing
- [ ] Implement DNS packet parser
- [ ] Extract domain names from DNS queries
- [ ] Test with sample packet captures
- [ ] Integrate with TUI display
- **Deliverable:** Working DNS packet analyzer

### Week 8: ML Integration
- [ ] Connect Rust TUI to Python ML model
- [ ] Real-time feature extraction in Rust
- [ ] Display analysis results in TUI
- [ ] End-to-end testing
- **Deliverable:** Integrated monitoring system

## Phase 3: Evaluation & Refinement (Weeks 9-11)

### Week 9: Performance Evaluation
- [ ] Quantitative performance metrics
- [ ] Precision, recall, F1-score measurements
- [ ] False positive/negative analysis
- [ ] Real-time performance benchmarking
- **Deliverable:** Performance evaluation report

### Week 10: Feature Analysis
- [ ] Feature importance analysis
- [ ] Ablation studies (remove features)
- [ ] Error case analysis
- [ ] Statistical significance testing
- **Deliverable:** Feature effectiveness report

### Week 11: System Polish
- [ ] Bug fixes and optimization
- [ ] Improved TUI interface
- [ ] Better error handling
- [ ] Documentation updates
- **Deliverable:** Polished final artifact

## Phase 4: Dissertation & Final (Weeks 12-14)

### Week 12: Dissertation Writing (Part 1)
- [ ] Introduction chapter
- [ ] Literature review
- [ ] Methodology description
- [ ] Initial results section
- **Deliverable:** Chapters 1-4 draft

### Week 13: Dissertation Writing (Part 2)
- [ ] Results analysis
- [ ] Discussion of findings
- [ ] Limitations section
- [ ] Conclusion chapter
- **Deliverable:** Complete dissertation draft

### Week 14: Final Preparation
- [ ] Proofreading and formatting
- [ ] Presentation preparation
- [ ] Code finalization
- [ ] Submission package
- **Deliverable:** Final dissertation submission

## Risk Management
- **Buffer weeks:** Weeks 11 and 14 have buffer time
- **Fallback options:** Simpler TUI if networking complex
- **Minimum viable:** Focus on ML research if time short

## Weekly Time Commitment
- **Weeks 1-8:** 20-25 hours/week
- **Weeks 9-11:** 15-20 hours/week  
- **Weeks 12-14:** 25-30 hours/week
- **Total:** ~300 hours over 14 weeks

---

## 🚀 Getting Started Files

### 1. scripts/setup.sh

```bash
#!/bin/bash
echo "Setting up DNS Threat Detection Project..."

# Create directory structure
mkdir -p {data/{raw/{malicious,benign},processed},ml/{feature_engineering,models/{random_forest,logistic_regression},training,evaluation,saved_models},src/{src/{network,ml_integration,ui/{views,components},utils},config},results/{model_performance,feature_analysis,live_monitoring},dissertation/{chapters,references,appendix},scripts,product}

echo "Directory structure created!"
echo "Next steps:"
echo "1. Run download_data.sh to get datasets"
echo "2. Install Python dependencies: pip install -r ml/requirements.txt"
echo "3. Build Rust project: cd src && cargo build"


```

### 2. scripts/download_data.sh

```bash
#!/bin/bash
echo "Downloading datasets..."

# Malicious domains
wget -O data/raw/malicious/urlhaus.csv "https://urlhaus.abuse.de/downloads/csv_online/"
wget -O data/raw/malicious/phishtank.csv "http://data.phishtank.org/data/online-valid.csv"

# Benign domains  
wget -O data/raw/benign/alexa_top_1m.zip "http://s3.amazonaws.com/alexa-static/top-1m.csv.zip"
unzip -j data/raw/benign/alexa_top_1m.zip -d data/raw/benign/

echo "Data download complete!"
```
