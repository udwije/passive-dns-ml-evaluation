# Machine Learning-Based DNS Threat Detection - BSc Dissertation

## Core Research Question
Can lexical features of domain names alone effectively detect malicious domains using machine learning?

## Methodology
- **Passive DNS monitoring** (no traffic modification)
- **Lexical feature analysis** (domain structure only)
- **Random Forest classifier** as primary model
- **Real-time demonstration** with Rust TUI

## Data Sources
### Malicious Domains:
- **URLHaus** (malware distribution): https://urlhaus.abuse.de/
- **PhishTank** (phishing sites): https://phishtank.org/  
- **Abuse.ch** (threat intelligence): https://abuse.ch/

### Benign Domains:
- **Alexa Top 1M** (legitimate sites): http://s3.amazonaws.com/alexa-static/top-1m.csv.zip
- **Tranco List** (research-ranked): https://tranco-list.eu/

### Target Dataset Size:
- Malicious: 10,000+ domains
- Benign: 50,000+ domains  
- Total: 60,000+ domains for training/testing

## Feature Engineering (15-20 Lexical Features)
1. Domain length
2. Character entropy
3. Digit ratio
4. Hyphen count
5. Vowel/consonant ratio
6. Special character patterns
7. Subdomain count
8. TLD analysis
9. Character n-grams
10. Sequential patterns

## Technical Stack
- **Python 3.8+**: ML training & evaluation
- **Rust**: Real-time monitoring TUI
- **libpcap**: Packet capture
- **Docker** (optional): Portable deployment

## Success Metrics
- Accuracy > 90%
- False positive rate < 5%
- Real-time processing < 100ms per query
