# 🤖 AI Risk Analysis in News Media

> A computational analysis of how artificial intelligence risks are framed in The New York Times using NLP, LLM classification, and network analysis.

[![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)](https://www.r-project.org/)
[![tidyverse](https://img.shields.io/badge/tidyverse-1A162D?style=for-the-badge&logo=tidyverse&logoColor=white)](https://www.tidyverse.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

## 📊 Project Overview

This project analyzes the evolution of AI risk narratives in mainstream media using The New York Times as a case study. By combining advanced Natural Language Processing, Large Language Model classification, and temporal analysis, I mapped how AI risks are discussed, framed, and prioritized over time.

**Research Question:** How has media coverage of AI risks evolved from 2012-2024, and what patterns emerge in the framing of different risk categories?

## ✨ Key Findings

- 📈 **450% increase** in AI risk coverage since 2020
- 🎭 **Major narrative shift** in 2022 from sci-fi scenarios to practical governance concerns
- 🔍 **20 distinct risk categories** identified and classified
- 🌐 Strong co-occurrence between privacy, discrimination, and governance issues
- 💭 Average sentiment score of **-0.15**, indicating cautious/concerned framing

## 🛠️ Technology Stack

- **Language:** R 4.3+
- **Core Libraries:** 
  - `tidyverse` - Data manipulation and visualization
  - `textstem` - Text lemmatization
  - `httr2` - API requests to Ollama
  - `jsonlite` - JSON parsing
  - `lubridate` - Date/time handling
  - `ggraph` & `igraph` - Network visualization
  - `zoo` - Time series analysis

- **AI/ML:**
  - Ollama (local LLM for classification)
  - Custom prompt engineering for risk categorization
  - Pattern-based AI content detection

## 📁 Project Structure

```
ai-risk-analysis/
│
├── data/
│   ├── raw/                    # Original NYT articles dataset
│   ├── processed/              # Cleaned and filtered data
│   └── classified/             # LLM-classified articles
│
├── scripts/
│   ├── 01_data_preprocessing.R # Text cleaning & AI filtering
│   ├── 02_llm_classification.R # Ollama integration & classification
│   ├── 03_temporal_analysis.R  # Time series & velocity analysis
│   ├── 04_sentiment_analysis.R # Sentiment scoring & volatility
│   ├── 05_network_analysis.R   # Co-occurrence & clustering
│   └── 06_visualization.R      # Chart generation
│
├── output/
│   ├── figures/                # Generated plots & charts
│   ├── tables/                 # Summary statistics
│   └── reports/                # Analysis reports
│
├── utils/
│   └── helper_functions.R      # Reusable utility functions
│
├── README.md
├── requirements.R              # Package dependencies
└── LICENSE
```

## 🚀 Getting Started

### Prerequisites

1. **Install R** (4.3 or higher)
2. **Install Ollama** for local LLM inference:
   ```bash
   # macOS/Linux
   curl -fsSL https://ollama.com/install.sh | sh
   
   # Windows - Download from ollama.com
   ```

3. **Pull the required model:**
   ```bash
   ollama pull llama3
   ```

### Installation

```r
# Clone the repository
git clone https://github.com/yourusername/ai-risk-analysis.git
cd ai-risk-analysis

# Install required R packages
source("requirements.R")
```

### Usage

```r
# Run the complete pipeline
source("scripts/01_data_preprocessing.R")
source("scripts/02_llm_classification.R")
source("scripts/03_temporal_analysis.R")
source("scripts/04_sentiment_analysis.R")
source("scripts/05_network_analysis.R")
source("scripts/06_visualization.R")

# Or run individual scripts for specific analyses
```

## 📋 Risk Classification System

The project classifies articles into 20 distinct risk categories, grouped into 6 meta-domains:

### 1. Societal & Economic Risks
- Job displacement
- Economic inequality
- Social disruption

### 2. Governance & Regulatory Risks
- Policy gaps
- Accountability frameworks
- Liability concerns

### 3. Discrimination, Fairness & Social Harms
- Algorithmic bias
- Privacy violations
- Vulnerable populations

### 4. Safety, Reliability & Technical Failure
- System errors
- Dataset quality
- Healthcare risks

### 5. Malicious Use & Security Threats
- Cybersecurity
- Copyright infringement
- Financial fraud

### 6. Long-term / Transformative Risks
- Existential concerns
- AGI scenarios
- Environmental impact

## 🔬 Methodology

### 1. Data Collection & Preprocessing
- Pattern-based AI content detection using comprehensive keyword matching
- Text normalization (lowercasing, punctuation removal, whitespace cleaning)
- Lemmatization for consistent token representation

### 2. LLM Classification
- Custom prompt engineering for accurate risk categorization
- Local Ollama inference for privacy and reproducibility
- Multi-label classification supporting complex articles

### 3. Multi-Dimensional Analysis
- **Frequency Analysis:** Most discussed risk categories
- **Sentiment Analysis:** Emotional tone and controversy levels
- **Temporal Analysis:** Risk velocity and narrative acceleration
- **Network Analysis:** Co-occurrence patterns between categories
- **Domain Clustering:** Meta-level risk grouping

## 📊 Key Visualizations

1. **Risk Velocity Chart** - Month-over-month changes in risk mentions
2. **Sentiment-Controversy Map** - 2D scatter of emotional tone vs. debate intensity
3. **Network Constellation** - Co-occurrence relationships between risks
4. **Narrative Battle Chart** - Sci-fi vs. reality framing over time
5. **Domain Evolution** - Temporal trends by risk domain

## 🎯 Results & Insights

### Major Findings:

1. **Societal & Economic Risks** dominate (40% of coverage)
2. **Governance concerns** show fastest growth post-ChatGPT
3. **Existential risk narratives** decreased post-2023
4. **Privacy-discrimination-governance** forms a strong thematic cluster
5. **Safety category** shows highest sentiment volatility

### Notable Patterns:

- Coverage acceleration coincides with major AI releases (GPT-3, ChatGPT, GPT-4)
- Shift from speculative long-term risks to immediate practical concerns
- Increased focus on regulatory frameworks and accountability
- Growing attention to copyright and intellectual property issues

## 🔮 Future Directions

- [ ] Cross-publication comparative analysis
- [ ] Predictive modeling for emerging risk narratives
- [ ] Topic modeling (LDA/BERTopic) for unsupervised discovery
- [ ] Interactive Shiny dashboard deployment
- [ ] Named entity recognition and stakeholder network analysis
- [ ] Multilingual analysis expansion

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Raghda Bassam**
- Data Scientist | NLP Researcher | AI Risk Analysis

## 🙏 Acknowledgments

- The New York Times for making article data accessible
- Ollama team for local LLM infrastructure
- R community and tidyverse developers
- AI safety research community for theoretical frameworks

## 📊 Project Stats

![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/ai-risk-analysis?style=flat-square)
![GitHub repo size](https://img.shields.io/github/repo-size/yourusername/ai-risk-analysis?style=flat-square)
![GitHub language count](https://img.shields.io/github/languages/count/yourusername/ai-risk-analysis?style=flat-square)

---

⭐ **Star this repository** if you find it helpful!

💬 **Questions or suggestions?** Open an issue or reach out directly.
