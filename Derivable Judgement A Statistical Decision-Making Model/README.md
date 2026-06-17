# 📊 Derivable Judgement: A Statistical Decision-Making Model

> **Comprehensive Guide to Inferential Statistics & Hypothesis Testing**

---

## 📋 Table of Contents

1. [Overview](#-overview)
2. [Project Structure](#-project-structure)
3. [Core Concepts](#-core-concepts)
4. [Statistical Tests & Formulas](#-statistical-tests--formulas)
5. [Key Findings](#-key-findings)
6. [Dataset Information](#-dataset-information)
7. [How to Use](#-how-to-use)
8. [Videos & Resources](#-videos--resources)

---

## 🎯 Overview

This project is a complete guide to **Inferential Statistics** and **Statistical Decision-Making**. It demonstrates practical applications of statistical hypothesis testing, confidence intervals, and correlation analysis using real health data.

### 🔑 Key Objectives

| Objective | Description |
|-----------|-------------|
| 📚 Understand Inferential Statistics | Learn how to generalize from samples to populations |
| 🔬 Hypothesis Testing | Formulate and test statistical hypotheses |
| 📈 Confidence Intervals | Estimate population parameters with precision |
| 🎯 Statistical Significance | Determine p-values and make evidence-based decisions |
| 📊 Data Visualization | Interpret statistical results through charts |

---

## 📁 Project Structure

```
Derivable Judgement A Statistical Decision-Making Model/
│
├── README.md                                          # This file
├── Part A – Theoretical Foundation.ipynb             # Theory & explanations
├── Part B – Data Analysis & Testing Tasks.ipynb      # Practical implementation
└── health_dataset_200.csv                            # Health data (200 records)
```

---

## 🧠 Core Concepts

### 1️⃣ Inferential Statistics

Inferential statistics uses sample data to make conclusions about an entire population.

**Formula for Sample Mean:**
$$\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i$$

| Term | Meaning |
|------|---------|
| $\bar{x}$ | Sample mean |
| $x_i$ | Individual data point |
| $n$ | Sample size |

**Example:** A researcher surveys 500 adults to estimate the average BMI of all adults in a city.

---

### 2️⃣ Population vs. Sample

| Aspect | Population | Sample |
|--------|-----------|--------|
| 📍 Definition | Entire group of interest | Subset of population |
| 📊 Size | Very large (often unknown) | Manageable size (n) |
| 💰 Cost | Expensive to study | Cost-effective |
| ⏱️ Time | Time-consuming | Quick analysis |
| 🎯 Use Case | Ultimate goal of study | Practical approach |

---

## 📐 Statistical Tests & Formulas

### Test 1: Z-Test (One Sample) ✅

**Purpose:** Test if sample mean differs from population mean

**Formula:**
$$Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}$$

| Component | Definition |
|-----------|-----------|
| $Z$ | Z-statistic |
| $\bar{x}$ | Sample mean |
| $\mu$ | Population mean (hypothesized) |
| $\sigma$ | Standard deviation |
| $n$ | Sample size |

**Decision Rule:**
- If p-value < 0.05 → **Reject H₀** ✓
- If p-value ≥ 0.05 → **Fail to reject H₀** ✗

**Result from our data:**
- Z Statistic: **5.53**
- P-Value: **3.2 × 10⁻⁸**
- **Decision:** Reject H₀ (Weight is significantly different from 70 kg)

---

### Test 2: Chi-Square Test 🔄

**Purpose:** Test association between two categorical variables

**Formula:**
$$\chi^2 = \sum \frac{(O_i - E_i)^2}{E_i}$$

| Component | Definition |
|-----------|-----------|
| $O_i$ | Observed frequency |
| $E_i$ | Expected frequency |
| $\chi^2$ | Chi-square statistic |

**Hypothesis:**
- H₀: Smoking has NO effect on Diabetes
- H₁: Smoking DOES affect Diabetes

**Result from our data:**
- Chi-Square Statistic: **0.31**
- P-Value: **0.857**
- **Decision:** Fail to reject H₀ (No significant relationship found)

---

### Test 3: ANOVA (Analysis of Variance) 📊

**Purpose:** Compare means across multiple groups

**Formula:**
$$F = \frac{\text{Between-Group Variance}}{\text{Within-Group Variance}} = \frac{MS_{\text{between}}}{MS_{\text{within}}}$$

| Component | Definition |
|-----------|-----------|
| $MS_{\text{between}}$ | Mean square between groups |
| $MS_{\text{within}}$ | Mean square within groups |
| $F$ | F-statistic |

**Hypothesis:**
- H₀: Age groups have equal average BMI
- H₁: Age groups have different average BMI

**Result from our data:**
- F Statistic: **1.91**
- P-Value: **0.130**
- **Decision:** Fail to reject H₀ (No significant difference in BMI by age group)

---

### Test 4: Confidence Interval (CI) 🎯

**Purpose:** Estimate range containing true population parameter

**Formula:**
$$CI = \bar{x} \pm Z^* \cdot \frac{\sigma}{\sqrt{n}}$$

| Component | Definition |
|-----------|-----------|
| $\bar{x}$ | Sample mean |
| $Z^*$ | Critical value (1.96 for 95% CI) |
| $\sigma$ | Standard deviation |
| $n$ | Sample size |

**95% Confidence Interval for Weight:**
- **Range: (74.83 kg, 80.12 kg)**
- Interpretation: We are 95% confident the true average weight lies in this range

---

### Test 5: Covariance & Correlation 📈

**Covariance Formula:**
$$\text{Cov}(X,Y) = \frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})$$

**Correlation Formula (Pearson r):**
$$r = \frac{\text{Cov}(X,Y)}{s_X \cdot s_Y}$$

| Metric | Value | Interpretation |
|--------|-------|-----------------|
| 📊 Covariance (Age, BMI) | **-9.26** | Negative relationship |
| 📈 Correlation (Age, BMI) | **-0.136** | Weak negative correlation |

**Interpretation:** As age increases, BMI tends to slightly decrease, but the relationship is weak.

---

## 📊 Critical Values & Decision Thresholds

| Confidence Level | One-Tailed Z* | Two-Tailed Z* |
|------------------|--------------|--------------|
| 90% | 1.28 | 1.645 |
| **95%** | **1.645** | **1.96** |
| 99% | 2.326 | 2.576 |

---

## 🔍 Key Findings

### Finding 1: Weight Analysis ⚖️
- **Sample Mean Weight:** 77.47 kg
- **95% CI:** (74.83 kg, 80.12 kg)
- **Conclusion:** Average weight is significantly different from 70 kg

### Finding 2: Smoking & Diabetes 🚬
- **Chi-Square p-value:** 0.857
- **Conclusion:** No statistically significant relationship between smoking status and diabetes in this sample
- **Note:** May need larger sample size for detection

### Finding 3: BMI by Age Groups 📍
- **ANOVA p-value:** 0.130
- **Conclusion:** No significant difference in BMI across age groups
- **Groups analyzed:** 18-25, 26-35, 36-45, 46-60

### Finding 4: Age-BMI Relationship 📉
- **Correlation:** r = -0.136
- **Conclusion:** Very weak negative relationship
- **Practical meaning:** Age is a poor predictor of BMI in this dataset

---

## 📋 Dataset Information

### 📊 Dataset: `health_dataset_200.csv`

| Feature | Type | Count | Range |
|---------|------|-------|-------|
| **Record ID** | String | 200 | Unique IDs |
| **Age Group** | Categorical | 5 | 18-25, 26-35, 36-45, 46-60, 60+ |
| **Age** | Numeric | 200 | 18-69 years |
| **Weight** | Numeric | 200 | 45-109 kg |
| **Gender** | Categorical | 2 | Male, Female |
| **BMI** | Numeric | 200 | 18.21-34.96 |
| **Blood Pressure** | Numeric | 200 | 90.02-159.95 mmHg |
| **Diabetes** | Boolean | 200 | True/False |
| **Hypertension** | Boolean | 200 | True/False |
| **Cholesterol Level** | Numeric | 200 | 121.63-298.80 mg/dL |
| **Glucose Level** | Numeric | 200 | 70.04-199.41 mg/dL |
| **Smoking Status** | Categorical | 3 | Smoker, Former Smoker, Non-Smoker |
| **Exercise Frequency** | Categorical | 4 | Never, Rarely, Weekly, Daily |
| **Visit Date** | Date | 200 | 2024 dates |

### Sample Data (First 5 Records)

| record_id | age | weight | bmi | diabetes | smoking_status |
|-----------|-----|--------|-----|----------|-----------------|
| b5029371 | 56 | 71 | 28.61 | True | Former Smoker |
| 0793b358 | 69 | 53 | 27.18 | False | Smoker |
| 7798beee | 46 | 106 | 25.46 | False | Former Smoker |
| 3dce3b2a | 32 | 81 | 27.82 | False | Smoker |
| 34f3b6e1 | 60 | 95 | 24.04 | False | Non-Smoker |

---

## 🚀 How to Use

### ✅ Step 1: Open Part A (Theory)
Open `Part A – Theoretical Foundation (Short Notes & Explanation).ipynb` to understand:
- What is Inferential Statistics?
- Key concepts and definitions
- Real-world examples with visualizations

### ✅ Step 2: Open Part B (Practice)
Open `Part B – Data Analysis & Testing Tasks.ipynb` to perform:
1. **Hypothesis Formulation** - Define H₀ and H₁
2. **Confidence Intervals** - Calculate CI for weight
3. **Z-Test** - One-sample hypothesis test
4. **Chi-Square Test** - Test smoking-diabetes relationship
5. **ANOVA** - Compare BMI across age groups
6. **Covariance & Correlation** - Analyze age-BMI relationship
7. **Visualizations** - View distribution charts and scatter plots

### ✅ Step 3: Run Jupyter Notebooks
```bash
# Install required packages
pip install pandas numpy matplotlib scipy statsmodels

# Run the notebook
jupyter notebook "Part B – Data Analysis & Testing Tasks.ipynb"
```

### ✅ Step 4: Interpret Results
Compare your results with the findings section above.

---

## 📹 Videos & Resources

### 📺 Educational Videos

| Topic | Video | Duration |
|-------|-------|----------|
| 📚 Inferential Statistics Basics | [![YouTube](https://img.shields.io/badge/YouTube-View_Video-red?logo=youtube)](https://youtu.be/) | 12 min |
| 🔬 Hypothesis Testing Explained | [![YouTube](https://img.shields.io/badge/YouTube-View_Video-red?logo=youtube)](https://youtu.be/) | 15 min |
| 📊 Z-Test Tutorial | [![YouTube](https://img.shields.io/badge/YouTube-View_Video-red?logo=youtube)](https://youtu.be/) | 10 min |
| 🎯 Chi-Square Test | [![YouTube](https://img.shields.io/badge/YouTube-View_Video-red?logo=youtube)](https://youtu.be/) | 14 min |
| 📈 ANOVA Explained | [![YouTube](https://img.shields.io/badge/YouTube-View_Video-red?logo=youtube)](https://youtu.be/) | 16 min |
| 🔗 Correlation & Covariance | [![YouTube](https://img.shields.io/badge/YouTube-View_Video-red?logo=youtube)](https://youtu.be/) | 11 min |

### 📚 Learning Resources

| Resource | Link | Type |
|----------|------|------|
| 📖 StatQuest Videos | [YouTube Channel](https://www.youtube.com/c/joshstarmer) | Video Series |
| 📕 Khan Academy Statistics | [Khan Academy](https://www.khanacademy.org/math/statistics-probability) | Course |
| 📔 SciPy Documentation | [scipy.stats](https://docs.scipy.org/doc/scipy/reference/stats.html) | Docs |
| 📙 Pandas Tutorials | [pandas.pydata.org](https://pandas.pydata.org/docs/) | Docs |

---

## 🎨 Visualizations in the Project

### 📊 Chart 1: Gender Distribution
Bar chart showing male/female distribution in the dataset

### 📊 Chart 2: Smoking Status
Bar chart showing smoker, non-smoker, and former smoker distribution

### 📊 Chart 3: BMI Distribution
Histogram showing BMI frequency distribution

### 📊 Chart 4: Age vs BMI Scatter Plot
Scatter plot showing relationship between age and BMI

---

## 🔧 Technologies Used

| Technology | Purpose |
|-----------|---------|
| 🐍 **Python 3.13** | Programming language |
| 📓 **Jupyter Notebook** | Interactive coding environment |
| 🐼 **Pandas** | Data manipulation & analysis |
| 🔢 **NumPy** | Numerical computing |
| 📊 **Matplotlib** | Data visualization |
| 🔬 **SciPy** | Statistical functions |
| 📈 **Statsmodels** | Statistical modeling |

---

## 📐 Summary of Formulas

### Quick Reference Table

| Formula | Use Case | Expression |
|---------|----------|-----------|
| **Sample Mean** | Central tendency | $\bar{x} = \frac{\sum x_i}{n}$ |
| **Standard Deviation** | Spread/Dispersion | $s = \sqrt{\frac{\sum(x_i-\bar{x})^2}{n-1}}$ |
| **Z-Statistic** | Hypothesis testing | $Z = \frac{\bar{x}-\mu}{\sigma/\sqrt{n}}$ |
| **95% CI** | Confidence interval | $\bar{x} \pm 1.96 \cdot \frac{\sigma}{\sqrt{n}}$ |
| **Correlation** | Relationship strength | $r = \frac{\text{Cov}(X,Y)}{s_X \cdot s_Y}$ |
| **Chi-Square** | Categorical test | $\chi^2 = \sum \frac{(O-E)^2}{E}$ |
| **F-Statistic** | ANOVA | $F = \frac{MS_{between}}{MS_{within}}$ |

---

## ✨ Key Takeaways

- ✅ **Inferential Statistics** helps us make decisions about populations using sample data
- ✅ **Hypothesis testing** requires p-values < 0.05 for statistical significance (typically)
- ✅ **Confidence intervals** provide a range of plausible values for population parameters
- ✅ **Different tests** are needed for different types of data (continuous vs. categorical)
- ✅ **Visualization** helps communicate statistical findings effectively
- ✅ **Correlation ≠ Causation** - always interpret relationships carefully

---

## 🤝 Contributing

Have suggestions for improvement? Feel free to:
1. 🔀 Fork this repository
2. 📝 Make your changes
3. 📤 Submit a pull request

---

## 📞 Questions or Issues?

If you have questions about this project:
- 📧 Review the notebook comments
- 📚 Check the resources section
- 🎯 Re-read the theoretical foundation

---

## 📜 License

This project is educational material and is open for learning purposes.

---

## 🙏 Acknowledgments

- Dataset created for educational purposes
- Built with industry-standard statistical libraries
- Designed to teach practical statistical decision-making

---

**Last Updated:** 2026-06-17  
**Project Status:** ✅ Complete  
**Version:** 1.0

---

### 🎯 Ready to Learn Statistics? Start with Part A! 📚
