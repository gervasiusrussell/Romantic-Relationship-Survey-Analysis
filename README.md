# ❤️ Romantic Relationship Survey Analysis

## 📖 Project Overview

This project analyzes survey data about **BINUS students’ romantic relationships**. The workflow includes **data collecting (Gforms), data cleaning, exploratory data analysis (EDA), measurement quality testing, and predictive modeling**.
The aim is to understand relationship dynamics and predict respondents’ **perception of their last relationship**.

---

## ⚙️ Technologies Used

* **Python 3**
* **Pandas, NumPy** – Data preprocessing
* **Matplotlib, Seaborn** – Visualization
* **Scikit-learn** – Machine Learning (Random Forest)
* **Pingouin** – Reliability & validity testing
* **SciPy** – Statistical analysis

---

## 📊 Workflow

### 1. Data Preprocessing

* Dropped unnecessary column (`Timestamp`)
* Cleaned non-ASCII characters & emojis
* Renamed survey columns to English-friendly names
* Converted categorical variables to numeric (gender, faculty, semester, relationship status, etc.)
* Imputed missing values (mean for numeric, mode/random sampling for categorical)
* Created filtered dataset (`df_pernah`) for respondents who had prior relationships

---

### 2. Measurement Quality

* **Corrected Item-Total Correlation (CITC)**: Validity check for Likert items
* **Cronbach’s Alpha**: Reliability score for 5 core relationship variables

---

### 3. Exploratory Analysis

* **Boxplots**: Distribution of age, number of relationships, average duration, and dates
* **Pie Charts**: Demographics (semester, gender, faculty) and relationship indicators
* **Stacked Likert Bar Charts**: Satisfaction, love, communication, social support, social media influence, conflict frequency, conflict resolution

**Key Insights:**

* Most respondents are aged 19–21 (university students).
* Majority had **1–6 relationships**, median ~3.
* About **60% currently in a relationship**.
* Most met partners via **campus/organizations** or **friends**.
* Communication and conflict resolution rated high (≥ 50% agree/strongly agree).

---

### 4. Predictive Modeling

* **Target variable**: *Perception of Last Relationship* (supportive vs disturbing)
* **Model**: Random Forest Classifier (with preprocessing pipeline for numerical & categorical features)
* **Train/Test Split**: 80/20, stratified
* **Evaluation Metrics**: Accuracy, Classification Report, Confusion Matrix

**Results:**

* Accuracy: ~80% (varies per run)
* Strong predictive performance in distinguishing supportive vs disturbing relationships.

---

## 🚀 How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/<your-username>/relationship-survey-analysis.git
   cd relationship-survey-analysis
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook or Python script:

   ```bash
   jupyter notebook analysis.ipynb
   ```

---

## 📌 Example Output

**Confusion Matrix (Random Forest Classifier):**

```
                  Predicted
                  1   2   3   4   5
True Label   1   12   0   1   0   0
            2    1   15   2   0   0
            3    0    1  18   2   0
            4    0    0   2  20   1
            5    0    0   1   1  25
```

---

✍️ **Author**: Gervasius Russell
🎓 **Major**: Data Science, BINUS University
📌 **Goal**: To analyze and model how relationship factors influence student perceptions of romantic experiences.
