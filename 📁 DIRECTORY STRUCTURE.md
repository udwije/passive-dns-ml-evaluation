# Directory Structure
```
dns-threat-detection-bsc/
├── 📄 README.md
├── 📄 PROJECT_OVERVIEW.md
├── 📄 .gitignore
│
├── 📁 data/
│   ├── 📄 SOURCES.md
│   ├── 📁 raw/
│   │   ├── 📁 malicious/
│   │   │   ├── 📄 urlhaus.csv
│   │   │   ├── 📄 phishtank.csv
│   │   │   └── 📄 abuse_ch.csv
│   │   └── 📁 benign/
│   │       ├── 📄 alexa_top_1m.csv
│   │       └── 📄 tranco_list.csv
│   └── 📁 processed/
│       ├── 📄 training_data.csv
│       ├── 📄 validation_data.csv
│       └── 📄 test_data.csv
│
├── 📁 ml/
│   ├── 📄 requirements.txt
│   ├── 📄 config.yaml
│   ├── 📁 feature_engineering/
│   │   ├── 📄 extractor.py
│   │   ├── 📄 features.yaml
│   │   └── 📄 validation.py
│   ├── 📁 models/
│   │   ├── 📄 random_forest/
│   │   │   ├── 📄 model.py
│   │   │   ├── 📄 train.py
│   │   │   └── 📄 hyperparameters.yaml
│   │   └── 📄 logistic_regression/
│   │       ├── 📄 model.py
│   │       └── 📄 train.py
│   ├── 📁 training/
│   │   ├── 📄 pipeline.py
│   │   └── 📄 cross_validation.py
│   ├── 📁 evaluation/
│   │   ├── 📄 metrics.py
│   │   ├── 📄 performance.py
│   │   └── 📄 feature_importance.py
│   └── 📁 saved_models/
│       ├── 📄 random_forest_v1.pkl
│       └── 📄 logistic_regression_v1.pkl
│
├── 📁 src/ (Rust TUI)
│   ├── 📄 Cargo.toml
│   ├── 📁 src/
│   │   ├── 📄 main.rs
│   │   ├── 📁 network/
│   │   │   ├── 📄 capture.rs
│   │   │   ├── 📄 dns_parser.rs
│   │   │   └── 📄 interface.rs
│   │   ├── 📁 ml_integration/
│   │   │   ├── 📄 client.rs
│   │   │   ├── 📄 feature_extraction.rs
│   │   │   └── 📄 analysis_result.rs
│   │   ├── 📁 ui/
│   │   │   ├── 📄 app.rs
│   │   │   ├── 📄 views/
│   │   │   │   ├── 📄 monitor.rs
│   │   │   │   ├── 📄 statistics.rs
│   │   │   │   └── 📄 help.rs
│   │   │   └── 📄 components/
│   │   │       ├── 📄 dns_list.rs
│   │   │       ├── 📄 metrics_display.rs
│   │   │       └── 📄 alerts.rs
│   │   └── 📁 utils/
│   │       ├── 📄 error_handling.rs
│   │       ├── 📄 logging.rs
│   │       └── 📄 time_utils.rs
│   └── 📁 config/
│       ├── 📄 default.yaml
│       ├── 📄 development.yaml
│       └── 📄 monitoring.yaml
│
├── 📁 results/
│   ├── 📁 model_performance/
│   │   ├── 📄 metrics.json
│   │   ├── 📄 confusion_matrix.png
│   │   └── 📄 roc_curve.png
│   ├── 📁 feature_analysis/
│   │   ├── 📄 importance_scores.csv
│   │   └── 📄 ablation_results.json
│   └── 📁 live_monitoring/
│       ├── 📄 performance_metrics.json
│       └── 📄 sample_captures/
│
├── 📁 dissertation/
│   ├── 📁 chapters/
│   │   ├── 📄 01_introduction.md
│   │   ├── 📄 02_literature_review.md
│   │   ├── 📄 03_methodology.md
│   │   ├── 📄 04_implementation.md
│   │   ├── 📄 05_results.md
│   │   └── 📄 06_conclusion.md
│   ├── 📁 references/
│   │   ├── 📄 bibliography.bib
│   │   └── 📄 key_papers.md
│   └── 📁 appendix/
│       ├── 📄 feature_specifications.md
│       └── 📄 dataset_details.md
│
├── 📁 scripts/
│   ├── 📄 setup.sh
│   ├── 📄 download_data.sh
│   ├── 📄 train_model.sh
│   ├── 📄 start_monitor.sh
│   └── 📄 evaluate.sh
│
└── 📁 product/ (Optional - Portable version)
    ├── 📄 Dockerfile
    ├── 📄 install.sh
    └── 📄 demo_script.sh
```