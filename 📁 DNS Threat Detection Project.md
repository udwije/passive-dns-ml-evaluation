# 📁 DNS Threat Detection Project - Complete Directory Structure

```
dns-threat-detection-bsc/
├── 📄 docs/                          # Documentation
├── 🔧 src/                           # Rust source code
├── 🤖 ml/                            # Python ML code
├── 📊 data/                          # Datasets and processed data
├── 🧪 tests/                         # Testing files
├── 📋 scripts/                       # Utility scripts
├── 📦 config/                        # Configuration files
├── 🐳 docker/                        # Containerization
├── 📈 results/                       # Analysis results
└── 📝 dissertation/                  # Dissertation writing
```

## 📄 docs/ - Documentation
```
docs/
├── 📖 project-proposal.md            # Original project proposal
├── 🔬 research-methodology.md        # Detailed methodology
├── 📋 requirements.md                # Functional & non-functional requirements
├── 🛠️ installation-guide.md          # Setup instructions
├── 📖 user-manual.md                 # How to use the system
├── 🔧 api-reference.md               # API documentation (if any)
├── 🐛 troubleshooting.md             # Common issues & solutions
├── 📊 dataset-documentation.md       # Data sources & preprocessing
└── 🎯 evaluation-methodology.md      # How to evaluate the system
```
## 🔧 src/ - Rust Source Code
```
src/
├── 📁 Cargo.toml                     # Rust project configuration
├── 📁 Cargo.lock                     # Dependency lock file
├── 📁 src/                           # Main source code
│   ├── 📄 main.rs                    # Entry point
│   ├── 📄 lib.rs                     # Library root
│   ├── 📁 packet/                    # DNS packet handling
│   │   ├── 📄 mod.rs                 # Module declaration
│   │   ├── 📄 dns_parser.rs          # DNS protocol parser
│   │   ├── 📄 packet_capture.rs      # Network packet capture
│   │   └── 📄 protocol_types.rs      # DNS data structures
│   ├── 📁 ml/                        # Machine learning integration
│   │   ├── 📄 mod.rs
│   │   ├── 📄 feature_extractor.rs   # Domain feature extraction
│   │   ├── 📄 api_client.rs          # Python ML API client
│   │   └── 📄 analysis_result.rs     # Analysis result structures
│   ├── 📁 tui/                       # Terminal user interface
│   │   ├── 📄 mod.rs
│   │   ├── 📄 app.rs                 # Main application state
│   │   ├── 📄 ui.rs                  # UI rendering logic
│   │   ├── 📄 screens/               # Different TUI screens
│   │   │   ├── 📄 mod.rs
│   │   │   ├── 📄 main_screen.rs     # Main dashboard
│   │   │   ├── 📄 monitor_screen.rs  # Real-time monitoring
│   │   │   ├── 📄 analysis_screen.rs # Batch analysis
│   │   │   ├── 📄 stats_screen.rs    # Statistics view
│   │   │   └── 📄 help_screen.rs     # Help information
│   │   └── 📄 components/            # Reusable UI components
│   │       ├── 📄 mod.rs
│   │       ├── 📄 charts.rs          # Text-based charts
│   │       ├── 📄 tables.rs          # Data tables
│   │       └── 📄 gauges.rs          # Progress gauges
│   ├── 📁 config/                    # Configuration management
│   │   ├── 📄 mod.rs
│   │   ├── 📄 settings.rs            # Application settings
│   │   └── 📄 defaults.rs            # Default configurations
│   ├── 📁 logging/                   # Logging utilities
│   │   ├── 📄 mod.rs
│   │   └── 📄 logger.rs              # Custom logger implementation
│   └── 📁 utils/                     # Utility functions
│       ├── 📄 mod.rs
│       ├── 📄 error_handling.rs      # Error types and handling
│       ├── 📄 time_utils.rs          # Time formatting
│       └── 📄 file_utils.rs          # File operations
└── 📁 target/                        # Built artifacts (ignored in git)
```
## 🤖 ml/ - Python Machine Learning
```
ml/
├── 📁 requirements.txt               # Python dependencies
├── 📁 pyproject.toml                 # Python project config (optional)
├── 📁 src/                           # Python source code
│   ├── 📄 __init__.py
│   ├── 📄 main.py                    # ML training entry point
│   ├── 📁 data/                      # Data handling
│   │   ├── 📄 __init__.py
│   │   ├── 📄 dataset_loader.py      # Load and preprocess data
│   │   ├── 📄 feature_engineering.py # Feature extraction logic
│   │   └── 📄 data_validation.py     # Data quality checks
│   ├── 📁 models/                    # ML model implementations
│   │   ├── 📄 __init__.py
│   │   ├── 📄 base_model.py          # Base model class
│   │   ├── 📄 random_forest.py       # Random Forest implementation
│   │   ├── 📄 xgboost_model.py       # XGBoost implementation
│   │   ├── 📄 neural_network.py      # Neural Network implementation
│   │   └── 📄 model_factory.py       # Model creation helper
│   ├── 📁 training/                  # Model training
│   │   ├── 📄 __init__.py
│   │   ├── 📄 trainer.py             # Training pipeline
│   │   ├── 📄 hyperparameter_tuning.py # Model optimization
│   │   └── 📄 cross_validation.py    # Cross-validation logic
│   ├── 📁 evaluation/                # Model evaluation
│   │   ├── 📄 __init__.py
│   │   ├── 📄 evaluator.py           # Evaluation metrics
│   │   ├── 📄 visualization.py       # Results visualization
│   │   └── 📄 comparison.py          # Model comparison
│   ├── 📁 api/                       # ML API server
│   │   ├── 📄 __init__.py
│   │   ├── 📄 app.py                 # Flask/FastAPI application
│   │   ├── 📄 routes.py              # API endpoints
│   │   └── 📄 schemas.py             # API data schemas
│   └── 📁 utils/                     # Utilities
│       ├── 📄 __init__.py
│       ├── 📄 config.py              # Configuration
│       └── 📄 logging_setup.py       # Logging configuration
├── 📁 notebooks/                     # Jupyter notebooks
│   ├── 📄 01_data_exploration.ipynb  # Dataset analysis
│   ├── 📄 02_feature_analysis.ipynb  # Feature importance
│   ├── 📄 03_model_experiments.ipynb # Model testing
│   └── 📄 04_results_analysis.ipynb  # Final evaluation
├── 📁 models/                        # Saved models
│   ├── 📄 random_forest_v1.pkl
│   ├── 📄 xgboost_v1.pkl
│   └── 📄 neural_network_v1.h5
└── 📁 experiments/                   # Experiment tracking
    ├── 📄 experiment_001/            # Individual experiment runs
    │   ├── 📄 config.yaml
    │   ├── 📄 results.json
    │   └── 📄 metrics.csv
    └── 📄 experiment_log.csv         # Experiment history
```

## 📊 data/ - Datasets
```
data/
├── 📁 raw/                           # Original downloaded data
│   ├── 📁 malicious/
│   │   ├── 📄 urlhaus.csv            # URLHaus malware domains
│   │   ├── 📄 phishtank.csv          # PhishTank phishing sites
│   │   ├── 📄 abuse_ch.csv           # Abuse.ch threat intelligence
│   │   └── 📄 dga_archive.csv        # DGA domain lists
│   ├── 📁 benign/
│   │   ├── 📄 alexa_top_1m.csv       # Alexa popular domains
│   │   ├── 📄 cisco_umbrella.csv     # Cisco domain list
│   │   └── 📄 tranco_list.csv        # Tranco research list
│   └── 📁 academic/
│       ├── 📄 cic_dns_2021/          # CIC dataset (if obtained)
│       └── 📄 iscx_dns_2016/         # ISCX dataset
├── 📁 processed/                     # Cleaned and processed data
│   ├── 📄 malicious_domains_clean.csv
│   ├── 📄 benign_domains_clean.csv
│   ├── 📄 training_dataset.csv       # Combined training data
│   ├── 📄 validation_dataset.csv     # Validation split
│   └── 📄 test_dataset.csv           # Test split
├── 📁 features/                      # Extracted features
│   ├── 📄 feature_set_v1.csv         # First feature set
│   ├── 📄 feature_importance.csv     # Feature importance scores
│   └── 📄 feature_correlations.csv   # Correlation matrix
└── 📁 live_capture/                  # Real-time captured data
    ├── 📄 capture_20240115.pcap      # Packet capture files
    ├── 📄 dns_queries_20240115.csv   # Extracted DNS queries
    └── 📄 analysis_results.json      # Analysis results
```
## 🧪 tests/ - Testing
```
tests/
├── 📁 rust/                          # Rust tests
│   ├── 📄 integration_tests.rs       # Integration tests
│   ├── 📁 unit/                      # Unit tests
│   │   ├── 📄 packet_parser_test.rs
│   │   ├── 📄 feature_extractor_test.rs
│   │   └── 📄 tui_components_test.rs
│   └── 📁 integration/               # Integration tests
│       ├── 📄 ml_api_test.rs
│       └── 📄 end_to_end_test.rs
├── 📁 python/                        # Python tests
│   ├── 📄 test_data_processing.py
│   ├── 📄 test_feature_engineering.py
│   ├── 📄 test_models.py
│   ├── 📄 test_api.py
│   └── 📄 conftest.py                # pytest configuration
├── 📁 data/                          # Test data
│   ├── 📄 sample_dns_packets.bin     # Sample DNS packets
│   ├── 📄 test_domains.csv           # Test domain lists
│   └── 📄 mock_responses.json        # Mock API responses
└── 📁 performance/                   # Performance tests
    ├── 📄 load_test.py               # Load testing
    ├── 📄 latency_test.rs            # Latency measurements
    └── 📄 memory_usage_test.rs       # Memory profiling
```
## 📋 scripts/ - Utility Scripts
```
scripts/
├── 📄 setup.sh                       # Project setup script
├── 📄 install_dependencies.sh        # Dependency installation
├── 📄 data_download.sh               # Automated data download
├── 📄 preprocessing_pipeline.sh      # Data preprocessing
├── 📄 train_model.sh                 # Model training script
├── 📄 start_monitoring.sh            # Start DNS monitoring
├── 📄 build_and_deploy.sh            # Build and deployment
├── 📄 backup_data.sh                 # Data backup
└── 📄 cleanup.sh                     # Clean temporary files
```
## 📦 config/ - Configuration Files
```
config/
├── 📄 default.yaml                   # Default configuration
├── 📄 development.yaml               # Development settings
├── 📄 production.yaml                # Production settings
├── 📄 ml_training.yaml               # ML training configuration
├── 📄 feature_extraction.yaml        # Feature extraction settings
└── 📄 tui_settings.yaml              # TUI display settings
```
### xample config/default.yaml:

app:
  name: "DNS Threat Detection"
  version: "1.0.0"
  
monitoring:
  interface: "eth0"
  promiscuous_mode: true
  buffer_size: 65535
  
ml:
  api_url: "http://localhost:8000"
  timeout_seconds: 30
  model_path: "./ml/models/random_forest_v1.pkl"
  
tui:
  refresh_rate_ms: 100
  max_history_entries: 1000
  color_scheme: "default"
  
logging:
  level: "info"
  file: "logs/app.log"
  max_size_mb: 100

## 🐳 docker/ - Containerization
```
docker/
├── 📄 Dockerfile.rust                # Rust application Dockerfile
├── 📄 Dockerfile.ml                  # Python ML Dockerfile
├── 📄 docker-compose.yml             # Full stack composition
├── 📄 docker-compose.dev.yml         # Development composition
└── 📁 entrypoint/                    # Container entry scripts
    ├── 📄 start_rust_app.sh
    └── 📄 start_ml_api.sh
```
## 📈 results/ - Analysis Results
```
results/
├── 📁 model_performance/             # ML model results
│   ├── 📄 random_forest_metrics.json
│   ├── 📄 xgboost_metrics.json
│   ├── 📄 neural_network_metrics.json
│   ├── 📄 model_comparison.csv
│   └── 📄 confusion_matrices/        # Visualization files
│       ├── 📄 rf_confusion.png
│       ├── 📄 xgb_confusion.png
│       └── 📄 nn_confusion.png
├── 📁 feature_analysis/              # Feature analysis results
│   ├── 📄 importance_scores.csv
│   ├── 📄 correlation_matrix.csv
│   └── 📄 ablation_study_results.json
├── 📁 performance/                   # System performance
│   ├── 📄 latency_measurements.csv
│   ├── 📄 throughput_analysis.json
│   └── 📄 resource_usage.log
└── 📁 final_evaluation/              # Final dissertation results
    ├── 📄 overall_performance.json
    ├── 📄 statistical_tests.csv
    └── 📄 limitations_analysis.md
```
## 📝 dissertation/ - Dissertation Materials
```
dissertation/
├── 📁 chapters/                      # Individual chapters
│   ├── 📄 01_introduction.md
│   ├── 📄 02_literature_review.md
│   ├── 📄 03_methodology.md
│   ├── 📄 04_implementation.md
│   ├── 📄 05_evaluation.md
│   ├── 📄 06_conclusion.md
│   └── 📄 abstract.md
├── 📁 references/                    # Reference materials
│   ├── 📄 bibliography.bib
│   ├── 📄 academic_papers/           # PDFs of key papers
│   └── 📄 rfc_documents/             # DNS RFCs
├── 📁 figures/                       # Charts and diagrams
│   ├── 📄 architecture_diagram.png
│   ├── 📄 performance_charts/
│   └── 📄 system_screenshots/
├── 📁 appendices/                    # Supplementary materials
│   ├── 📄 source_code_listing.md
│   ├── 📄 dataset_details.md
│   └── 📄 user_manual.md
└── 📄 dissertation.pdf               # Final compiled PDF
```
## 🗂️ Root Level Files
```
dns-threat-detection-bsc/
├── 📄 .gitignore                     # Git ignore rules
├── 📄 README.md                      # Project overview
├── 📄 LICENSE                        # Project license
├── 📄 .env.example                   # Environment variables template
├── 📄 Makefile                       # Build automation
├── 📄 project-plan.md                # Overall project plan
├── 📄 milestones.md                  # Key milestones
└── 📄 risk-assessment.md             # Risk analysis
```
---
## 🔄 Complete Build & Run Workflow
Setting up the project:
#### Clone and setup
```
git clone <repository>
cd dns-threat-detection-bsc
```
#### Run setup script
```
./scripts/setup.sh
```
#### Install dependencies
```
./scripts/install_dependencies.sh
```
#### Download data
```
./scripts/data_download.sh
```
## Development workflow:
#### Start ML API (Terminal 1)
```
cd ml/
python src/api/app.py
```
#### Build and run Rust app (Terminal 2)
```/
cd src/
cargo build
cargo run
```