# 🚀 A/B Testing Analysis for Landing Page Optimization

## 📌 Overview
This project implements an end-to-end A/B testing workflow to evaluate whether a new landing page (treatment) improves conversion rates compared to the existing landing page (control).

The goal was to apply statistical methods in a real-world scenario and make data-driven product decisions.

---

## 🎯 Objective

To determine whether the new landing page leads to a statistically significant improvement in conversion rate.

### Hypotheses

- **Null Hypothesis (H₀):**  
  There is no significant difference in conversion rate between the control and treatment groups.

- **Alternative Hypothesis (H₁):**  
  There is a significant difference in conversion rate between the control and treatment groups.

---

## 📊 Dataset

- Source: Kaggle A/B Testing Dataset  
- Includes:
  - `user_id`
  - `group` (control / treatment)
  - `landing_page`
  - `converted` (0 or 1)

---

## ⚙️ Methodology

### 1. Data Cleaning & Validation
- Removed **group–page mismatches**
- Eliminated **duplicate users**
- Ensured valid experimental setup before analysis

---

### 2. Conversion Analysis

| Metric | Control | Treatment |
|--------|--------|-----------|
| Conversion Rate | 12.04% | 11.88% |
| Uplift | -1.31% | |

- The treatment group showed a slightly lower conversion rate compared to control.

---

### 3. Statistical Testing

#### ✅ Two-Proportion Z-Test
- **Z-statistic:** 1.3109  
- **P-value:** 0.1899  

#### ✅ Chi-Square Test
- **Chi-Square Statistic:** 1.7036  
- **P-value:** 0.1918  
- **Degrees of Freedom:** 1  

#### ✅ Confidence Intervals (95%)

- **Control:** (0.1187, 0.1221)  
- **Treatment:** (0.1171, 0.1205)

---

## 📈 Key Insights

- The treatment group performed slightly worse than the control group
- Both statistical tests returned **p-values > 0.05**
- Confidence intervals **overlap significantly**
- No strong evidence of improvement from the new landing page

---

## 💡 Business Recommendation

The observed uplift is **not statistically significant**.

➡️ Recommendation:
- Do **not roll out** the new landing page yet  
- Collect more data or iterate on design improvements  
- Re-run the experiment after making changes  

---

## 🔥 Key Learnings

- Statistical significance ≠ practical significance  
- A higher/lower conversion rate alone is not enough  
- Data validation is critical before analysis  
- A/B testing is about **decision-making, not just metrics**  

---

## 🛠️ Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Statsmodels  
- SciPy  

---

## 📁 Project Structure
