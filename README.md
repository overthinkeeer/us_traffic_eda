# Traffic Accident Severity – Reliability Analysis via Exploratory Data Analysis (EDA)

This project investigates the **validity of severity levels** in the [US Accidents dataset](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents). According to the dataset documentation, the `Severity` feature represents the **level of impact on traffic** — from minor (1) to severe (4).

Through extensive EDA, I demonstrate that:
- Severity values, especially level 3, do **not consistently correlate** with real-world impact.
- Many records contain **extreme anomalies**, such as accidents lasting over 2 years, or with 120-mile visibility.
- The current 4-class severity labeling may be **misleading** and benefit from **reclustering via NLP and Unsupervised Learning**.

---

## 🎯 Research Objective

> Evaluate whether the dataset’s `Severity` classification matches real traffic consequences  
> and assess whether current labels hold **statistical and practical meaning**.

This is a full-scale **research-style EDA** project — not model-focused — aimed at identifying **data inconsistencies** and proposing improvements.

---

## 📊 Dataset Overview

- **Source**: Kaggle – US Accidents (2016–2023, 7M+ records)
- **Sample used**: 500,000 entries (due to resource constraints)
- **License**: Non-commercial, academic use only

---

## 🔍 Key Findings

- `Severity` has a correlation of **−0.037 with incident duration**, contradicting the dataset documentation.
- **Severity level 3** behaves inconsistently — closer to level 1 than 2 or 4.
- Outlier examples include:
  - Accidents lasting **over 4 years** with **traffic delays of just a few miles**
  - **Invalid weather data**: visibility >100 miles, temperature −50 to +200 °F
- Visual analysis supports the hypothesis that `Severity=3` is an ill-defined class.

---

## 🛠️ Methodology

- Data parsing and cleaning: `pandas`, `numpy`
- Outlier detection and replacement
- Time-based feature engineering: calculating `Duration` of accidents
- Correlation heatmaps and distribution plots (`seaborn`, `matplotlib`)
- Geographic analysis (optional) with `plotly`
- Proposal for future NLP-based reclustering of accident descriptions

---

## 📈 Next Steps

- Use **NLP** (TF-IDF or embeddings) to vectorize `Description` field
- Apply **Unsupervised Learning** (e.g., K-Means, DBSCAN) to cluster similar descriptions
- Define **new, statistically justified severity classes**

---

## 🧑‍💻 Author & Academic Interest

**Arsen Kenzhakaev**  
Prospective Computer Science/Data Science student  
📍 Applying to KAIST & GKS Undergraduate Scholarship, 2026 intake  
🎓 Passionate about real-world problem solving through AI, data validation, and research-oriented machine learning

---

## 📄 License

MIT License for all code and notebooks.  
Dataset used under non-commercial academic terms from Kaggle.
