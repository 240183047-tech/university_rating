# 🎓 Global University Ranking Analysis (Mathematics & Statistics)

## 📌 Project Overview
This project investigates the driving factors behind global university rankings, focusing on the Shanghai Ranking (ARWU) data for Mathematics and Statistics. By combining automated data collection, rigorous statistical testing, and machine learning, we identified the specific institutional metrics that lead to academic excellence.

---

## 👥 Team: On Jeti
* **Zhanar Muratova**: Web Scraping Architecture, [Report](./onjeti_report%20(1).pdf) & [Presentation](./universities_presentation.pdf).
* **Akmeiir Amirseit**: Data Preprocessing, Machine Learning Engineering.
* **Feruza Shamshimetova**: Data Visualization & Spatial Analysis.
* **Fazilat Kholmirzayeva**: Exploratory Data Analysis (EDA) & Hypothesis Testing.

---

## ⚙️ Technical Workflow

### 1. Data Acquisition (The Hybrid Pipeline)
To bypass the limitations of static scraping, we implemented a dual-layer extraction system:
* **Selenium**: Used for the *Primary Ranking Table* (~7,000 records) to handle dynamic pagination and JavaScript-rendered content.
* **BeautifulSoup**: Used for *University Profiles* (~3,000 records) to extract institutional details with high efficiency.
* **Resilience**: The scripts include randomized request delays and a recovery mechanism to handle 6+ hours of continuous scraping.

### 2. Data Engineering
* **Cleaning**: Automated deduplication and standardizing university names across longitudinal data (2021–2025).
* **Imputation**: Logical summation used to fill missing values in composite scoring columns.
* **Outlier Detection**: Applied Z-score filtering to ensure statistical models weren't skewed by extreme institutional anomalies.

### 3. Analysis & Modeling
* **Statistical Validation**: Conducted ANOVA, Tukey’s HSD, and Welch’s T-tests to verify differences in research impact across regions.
* **Machine Learning**: Developed a Random Forest Classifier to distinguish between the academic "signatures" of Mathematics and Statistics departments.
  * **Accuracy**: `>90%`
  * **Top Feature**: Research Impact (Importance Score: `0.33`).

---

## 💡 Key Insights
* **The 2023–2024 Pivot**: Our analysis caught a significant shift in ranking methodologies that favored research-heavy institutions.
* **Academic Signatures**: Mathematics departments tend to follow more "traditional" metric profiles, while Statistics departments show higher variance in Research Impact.

---

## 🛠️ Installation & Setup

To run this project locally, clone the repository and install the required dependencies:

```bash
pip install -r requirements.txt
