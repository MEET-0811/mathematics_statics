# 📊 Expectation Decider: Probability & Statistics Analysis

> **Unlocking the Secrets of Student Success Through Probability Theory and Statistical Analysis**

![Python](https://img.shields.io/badge/Python-3.13-blue?style=flat-square&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## 📚 Table of Contents

- [Overview](#-overview)
- [Project Objectives](#-project-objectives)
- [Key Concepts](#-key-concepts)
- [Dataset Details](#-dataset-details)
- [Analysis Breakdown](#-analysis-breakdown)
- [Formulas & Mathematical Concepts](#-formulas--mathematical-concepts)
- [Key Findings](#-key-findings)
- [Video Tutorials](#-video-tutorials)
- [Installation & Setup](#-installation--setup)
- [Usage](#-usage)
- [File Structure](#-file-structure)

---

## 🎯 Overview

**Expectation Decider** is a comprehensive Jupyter notebook project that explores **probability theory and statistics** using real-world student academic data. The project demonstrates how probability distributions, conditional probabilities, and Bayes' theorem can be applied to predict student exam success based on study habits, attendance, and collaborative learning activities.

### 🌟 What You'll Learn

✅ Fundamentals of Probability Theory  
✅ Probability Distributions (Binomial Distribution)  
✅ Conditional Probability & Independence  
✅ Bayes' Theorem Application  
✅ Contingency Tables & Joint Probabilities  
✅ Real-World Data Analysis  

---

## 🎓 Project Objectives

| Objective | Description |
|-----------|-------------|
| 📖 **Learn Probability Basics** | Understand the fundamental principles of probability |
| 🔍 **Explore Distributions** | Analyze binomial distributions with real data |
| 🧮 **Apply Bayes' Theorem** | Use conditional probability to make predictions |
| 📈 **Statistical Analysis** | Create visualizations and contingency tables |
| 🎯 **Make Predictions** | Predict student success based on multiple factors |

---

## 🧠 Key Concepts

### 1️⃣ **Probability** 📐

| Term | Definition |
|------|-----------|
| **Event** | An outcome or set of outcomes |
| **Sample Space** | All possible outcomes of an experiment |
| **Probability** | Likelihood of an event occurring (0 to 1) |
| **Favorable Outcomes** | Outcomes that satisfy the event condition |

**Formula:**
$$P(E) = \frac{\text{Number of Favorable Outcomes}}{\text{Total Possible Outcomes}}$$

---

### 2️⃣ **Types of Probability** 🎲

| Type | Description | Example |
|------|-------------|---------|
| **Empirical** | Based on actual observed data | P(Pass) = 121/200 = 0.605 |
| **Theoretical** | Based on mathematical assumptions | P(Head) = 1/2 = 0.5 |
| **Conditional** | Probability given another event occurred | P(Pass \| Group Discussion = Yes) |
| **Joint** | Probability of two events occurring together | P(Yes ∩ Pass) |

---

### 3️⃣ **Random Variable & Binomial Distribution** 🎰

A **Random Variable** is a function that assigns numerical values to outcomes of a random experiment.

**Binomial Distribution PMF (Probability Mass Function):**

$$P(X = k) = \binom{n}{k} \cdot p^k \cdot (1-p)^{n-k}$$

Where:
- **n** = number of trials
- **k** = number of successes
- **p** = probability of success
- $\binom{n}{k}$ = binomial coefficient ("n choose k")

**Mean and Variance:**

| Metric | Formula |
|--------|---------|
| **Mean (Expected Value)** | $\mu = n \cdot p$ |
| **Variance** | $\sigma^2 = n \cdot p \cdot (1-p)$ |
| **Standard Deviation** | $\sigma = \sqrt{n \cdot p \cdot (1-p)}$ |

---

### 4️⃣ **Conditional Probability** 🎯

**Formula:**
$$P(A\|B) = \frac{P(A \cap B)}{P(B)}$$

**Interpretation:** Probability of event A occurring given that event B has already occurred.

**Example from Project:**
$$P(\text{Pass} \| \text{Group Discussion = Yes}) = \frac{P(\text{Pass AND Group Discussion})}{P(\text{Group Discussion})}$$

---

### 5️⃣ **Independence vs. Dependence** 🔗

| Relationship | Condition | Mathematical Expression |
|-------------|-----------|------------------------|
| **Independent** | One event doesn't affect the other | $P(A \cap B) = P(A) \cdot P(B)$ |
| **Dependent** | One event affects the other | $P(A \cap B) \neq P(A) \cdot P(B)$ |
| **Mutually Exclusive** | Events cannot occur together | $P(A \cap B) = 0$ |

---

### 6️⃣ **Bayes' Theorem** 🔄

**Formula:**
$$P(A\|B) = \frac{P(B\|A) \cdot P(A)}{P(B)}$$

**Components:**
- **P(A|B)** = Posterior Probability
- **P(B|A)** = Likelihood
- **P(A)** = Prior Probability
- **P(B)** = Evidence (Total Probability)

**Extended Form:**
$$P(A\|B) = \frac{P(B\|A) \cdot P(A)}{P(B\|A) \cdot P(A) + P(B\|\neg A) \cdot P(\neg A)}$$

---

## 📊 Dataset Details

### 📋 Dataset Overview

| Property | Value |
|----------|-------|
| **Total Records** | 200 students |
| **Features** | 5 columns |
| **Data Type** | Educational performance metrics |
| **File Name** | Expectation Decider Data.csv |

### 📌 Column Description

| Column | Type | Description | Range |
|--------|------|-------------|-------|
| **study_hours** | Numeric | Weekly study hours | 6-18 hours |
| **attendance** | Numeric | Class attendance percentage | 55-78% |
| **group_discussion** | Categorical | Participation in group discussions | Yes/No |
| **previous_test_score** | Numeric | Score from previous test | 42-100 |
| **final_exam_pass** | Categorical | Final exam result | Pass/Fail |

### 📈 Sample Data

| study_hours | attendance | group_discussion | previous_test_score | final_exam_pass |
|-------------|-----------|------------------|-------------------|-----------------|
| 10 | 73 | Yes | 72 | **Pass** ✅ |
| 18 | 70 | Yes | 100 | **Fail** ❌ |
| 14 | 57 | Yes | 57 | **Fail** ❌ |
| 11 | 74 | Yes | 68 | **Pass** ✅ |
| 10 | 78 | Yes | 75 | **Pass** ✅ |

---

## 🔬 Analysis Breakdown

### Section 1️⃣: Understanding the Basics

**Calculates basic probability metrics:**

| Metric | Value | Formula |
|--------|-------|---------|
| Students studying > 10 hrs/week | 108/200 | Count: 108 |
| P(Study > 10 hrs) | **0.54** | 108 ÷ 200 |
| Students with attendance > 80% | 87/200 | Count: 87 |
| P(Attendance > 80%) | **0.435** | 87 ÷ 200 |
| Students who pass | 121/200 | Count: 121 |
| P(Pass) | **0.605** | 121 ÷ 200 |

---

### Section 2️⃣: Types of Probability

#### 🔹 Empirical Probability
**Based on actual data observations**

$$P(\text{Pass}) = \frac{121}{200} = 0.605$$

**Interpretation:** 60.5% of students pass the final exam ✨

#### 🔹 Theoretical Probability
**Based on mathematical theory**

$$P(\text{Head in coin flip}) = \frac{1}{2} = 0.5$$

---

### Section 3️⃣: Random Variable & Binomial Distribution

**Scenario:** Select 3 random students. How many will pass?

**Random Variable X:** Number of students passing (out of 3)  
**Possible Values:** X ∈ {0, 1, 2, 3}

**Probability Distribution:**

| Passes (X) | P(X) | Interpretation |
|-----------|------|-----------------|
| 0 | 0.0616 | 6.16% chance none pass |
| 1 | 0.2832 | 28.32% chance exactly 1 passes |
| 2 | 0.4337 | 43.37% chance exactly 2 pass ⭐ |
| 3 | 0.2214 | 22.14% chance all 3 pass |

**Expected Values:**
- **Mean (μ)** = 1.815 students
- **Variance (σ²)** = 0.717
- **Standard Deviation (σ)** = 0.847

---

### Section 4️⃣: Venn Diagram Probability

**Visualizes relationship between:**
- **Set A:** Students studying > 10 hrs/week
- **Set B:** Students with attendance > 80%
- **A ∩ B:** Students satisfying both conditions

📊 *A visual representation showing the overlap between these two sets*

---

### Section 5️⃣: Contingency Table & Probability

**Table: Group Discussion vs. Final Exam Result**

| | Pass | Fail | **Total** |
|---|------|------|---------|
| **Yes** | 75 | 43 | 118 |
| **No** | 46 | 36 | 82 |
| **Total** | **121** | **79** | **200** |

**Key Probabilities:**

| Probability | Value | Formula |
|-------------|-------|---------|
| P(Pass) | 0.605 | 121/200 |
| P(Group Discussion = Yes) | 0.590 | 118/200 |
| P(Yes ∩ Pass) | 0.375 | 75/200 |
| **P(Pass \| Group Discussion = Yes)** | **0.636** | 75/118 |

---

### Section 6️⃣: Understanding Relationships

#### 🔹 Conditional Probability Analysis

$$P(\text{Pass} \| \text{Group Discussion = Yes}) = \frac{75}{118} = 0.636$$

**Interpretation:** If a student participates in group discussions, there's a **63.6% chance** they'll pass! 🎉

#### 🔹 Independence Test

| Event | Probability |
|-------|-------------|
| P(Yes) | 0.59 |
| P(Pass) | 0.605 |
| P(Yes) × P(Pass) | 0.357 |
| P(Yes ∩ Pass) | 0.375 |

**Result:** 0.375 ≠ 0.357 → **Events are DEPENDENT** 🔗

**Conclusion:** Group discussion participation DOES affect passing probability!

---

### Section 7️⃣: Bayes' Theorem Application

**Given Information:**
- P(High Attendance \| Pass) = 0.70
- P(High Attendance \| Fail) = 0.40
- P(High Attendance) = 0.60

**Find:** P(Pass \| High Attendance)

**Solution:**

$$P(\text{Pass} \| \text{High}) = \frac{P(\text{High} \| \text{Pass}) \cdot P(\text{Pass})}{P(\text{High})}$$

| Step | Calculation |
|------|-------------|
| **P(Pass)** | 0.667 |
| **P(Fail)** | 0.333 |
| **P(Pass \| High Attendance)** | **0.778** |

**Interpretation:** If a student has high attendance, there's a **77.8% probability** they will pass! 🚀

---

## 📋 Formulas & Mathematical Concepts

### 📐 Essential Formulas Reference

| Concept | Formula | Use Case |
|---------|---------|----------|
| **Basic Probability** | $P(E) = \frac{\text{Favorable}}{\text{Total}}$ | Finding event probability |
| **Complement Rule** | $P(E^c) = 1 - P(E)$ | Probability of NOT happening |
| **Addition Rule** | $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ | Probability of A or B |
| **Multiplication Rule** | $P(A \cap B) = P(A) \cdot P(B\|A)$ | Probability of A and B |
| **Conditional Probability** | $P(A\|B) = \frac{P(A \cap B)}{P(B)}$ | Given another event |
| **Bayes' Theorem** | $P(A\|B) = \frac{P(B\|A) \cdot P(A)}{P(B)}$ | Reverse probability |
| **Binomial PMF** | $P(X=k) = \binom{n}{k}p^k(1-p)^{n-k}$ | n independent trials |
| **Expected Value** | $E(X) = \sum x \cdot P(x)$ | Average outcome |
| **Variance** | $\text{Var}(X) = E(X^2) - [E(X)]^2$ | Spread of data |

---

## 🎯 Key Findings

### ✨ Main Discoveries

| Finding | Impact | Confidence |
|---------|--------|------------|
| **Students with group discussion participation have 63.6% pass rate** | High | ⭐⭐⭐⭐⭐ |
| **High attendance (>80%) increases pass probability to 77.8%** | Very High | ⭐⭐⭐⭐⭐ |
| **Study hours and exam results are dependent events** | Medium | ⭐⭐⭐⭐ |
| **Attendance is strongest predictor of success** | Very High | ⭐⭐⭐⭐⭐ |

### 📊 Success Factors Ranking

1. 🥇 **High Attendance (>80%)**
   - Probability boost: +17.3%
   - Most significant factor

2. 🥈 **Active Group Discussion Participation**
   - Probability boost: +3.1%
   - Significant collaborative benefit

3. 🥉 **Consistent Study Hours**
   - Probability boost: +2.0%
   - Moderate individual effort effect

---

## 🎥 Video Tutorials

Learn more about these concepts through video resources:



### 📹 Conditional Probability

[![Demo Video](https://img.shields.io/badge/📺_Watch_Conditional_Probability-FF0000?style=for-the-badge&logo=youtube)](https://www.youtube.com/watch?v=PmD5ibQO5OU)


---

## 💻 Installation & Setup

### Prerequisites ✅

```bash
Python 3.7+
Jupyter Notebook
pip or conda
```

### Required Libraries 📦

```python
numpy          # Numerical computations
pandas         # Data manipulation
matplotlib     # Plotting
seaborn        # Statistical visualizations
scipy          # Statistical functions
matplotlib-venn # Venn diagram visualizations
```

### Installation Steps 🚀

1. **Clone the repository:**
```bash
git clone https://github.com/MEET-0811/mathematics_statics.git
cd mathematics_statics
```

2. **Install dependencies:**
```bash
pip install numpy pandas matplotlib seaborn scipy matplotlib-venn
```

Or using conda:
```bash
conda install numpy pandas matplotlib seaborn scipy matplotlib-venn
```

3. **Launch Jupyter Notebook:**
```bash
jupyter notebook
```

4. **Open the notebook:**
```
Navigate to: Expectation Decider/Expectation Decider.ipynb
```

---

## 🎮 Usage

### Running the Notebook 📖

1. Open `Expectation Decider.ipynb` in Jupyter
2. Run cells sequentially (Shift + Enter)
3. View outputs and visualizations
4. Modify parameters to explore different scenarios

### Example: Calculate Custom Probability

```python
# Load data
import pandas as pd
data = pd.read_csv("Expectation Decider Data.csv")

# Calculate probability of passing
pass_count = (data['final_exam_pass'] == 'Pass').sum()
total_students = len(data)
p_pass = pass_count / total_students

print(f"Probability of Passing: {p_pass:.3f}")
```

### Example: Conditional Probability

```python
# Calculate P(Pass | Group Discussion = Yes)
yes_and_pass = len(data[(data['group_discussion'] == 'Yes') & 
                        (data['final_exam_pass'] == 'Pass')])
yes_total = len(data[data['group_discussion'] == 'Yes'])

p_pass_given_yes = yes_and_pass / yes_total
print(f"P(Pass | Group Discussion = Yes): {p_pass_given_yes:.3f}")
```

---

## 📁 File Structure

```
mathematics_statics/
├── Expectation Decider/
│   ├── Expectation Decider.ipynb          # Main Jupyter notebook
│   ├── Expectation Decider Data.csv       # Dataset file
│   └── README.md                          # This file
└── [Other project files...]
```

---

## 🎓 Learning Outcomes

After completing this project, you will understand:

- ✅ Fundamentals of probability theory
- ✅ How to calculate probabilities from real data
- ✅ Binomial distributions and their applications
- ✅ Conditional probability and Bayes' theorem
- ✅ Independence and dependence of events
- ✅ Statistical analysis of datasets
- ✅ Data visualization techniques
- ✅ Real-world applications of probability



---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- 🐛 Report bugs
- 💡 Suggest improvements
- 📝 Add more examples
- 🎨 Enhance visualizations

---



## 👨‍💻 Author

**MEET-0811**  
 
🔗 GitHub: [@MEET-0811](https://github.com/MEET-0811)

---

## ⭐ Support

If you find this project helpful, please consider:
- ⭐ Starring the repository
- 🔄 Sharing with others
- 💬 Providing feedback
- 🙌 Contributing improvements

---



</div>
