# Starbucks Promotional Offer A/B Testing Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)

## 📊 Project Overview

Analyzed Starbucks promotional offer data to determine whether promotional offers actually drive incremental customer spending, which offer types perform best, and which customer segments are most responsive.

**Key Business Questions:**
1. Do promotional offers increase customer spending?
2. Which offer type (BOGO vs Discount) performs better?
3. Which customer segments should Starbucks target for maximum ROI?

---

## 🔍 Key Findings

### 1. Promotional Offers Increase Spending by 80%
| Group | Avg Spending | Sample Size |
|-------|-------------|-------------|
| Received Offers | $104.64 | 16,928 |
| No Offers | $57.98 | 72 |

- **Difference:** +$46.66 (+80%)
- **Statistical Significance:** p < 0.0001 (Mann-Whitney U Test)
- **Effect Size:** Cohen's d = 0.37 (small-medium)
- **95% Confidence Interval:** [$26.93, $67.02]

### 2. Discount Offers Have Higher Completion Rates
| Offer Type | Completion Rate | Avg Spending |
|------------|-----------------|--------------|
| BOGO | 53.5% | $104.00 |
| Discount | 57.1% | $105.59 |

- **Chi-Square Test:** p = 0.000003 (statistically significant difference)

### 3. Best Customer Segments to Target
| Segment | Completion Rate | Avg Spending |
|---------|-----------------|--------------|
| Female | 70% | $141.21 |
| Senior (60+) | 70% | $140.40 |
| High Income ($100k+) | 73% | $176.12 |

**Recommendation:** Target high-income senior females for maximum ROI.

---

## 🧪 Statistical Methods Used

| Method | Purpose |
|--------|---------|
| **Mann-Whitney U Test** | Compare spending distributions (non-parametric) |
| **Welch's T-Test** | Compare group means with unequal variances |
| **Chi-Square Test** | Compare completion rates between offer types |
| **Bootstrap Confidence Intervals** | Distribution-free uncertainty estimation |
| **Cohen's d** | Measure practical effect size |
| **Power Analysis** | Validate sample size adequacy (achieved 88% power) |

---

## 📁 Data Overview

- **Source:** Starbucks promotional offer dataset (simulated customer data)
- **Time Period:** 30 days (714 hours)
- **Scale:** 
  - 17,000 customers
  - 306,534 events
  - $1.78M total revenue

### Three Datasets:
1. **portfolio.csv** - 10 different offer types (BOGO, Discount, Informational)
2. **profile.csv** - Customer demographics (age, gender, income)
3. **transcript.csv** - Event log (offers received, viewed, completed, transactions)

---

## 📈 Visualizations

The notebook includes:
- Customer demographic distributions
- Offer funnel analysis (received → viewed → completed)
- Treatment vs Control spending comparison (box plots, histograms)
- Bootstrap distribution of spending differences
- BOGO vs Discount performance comparison
- Segmentation heatmaps (Age × Income)

---

## 🛠️ Technologies Used
```
pandas
numpy
matplotlib
seaborn
scipy (stats)
statsmodels
```

---

## 🚀 How to Run

1. Clone this repository:
```bash
git clone https://github.com/RohiniVishwanathan/starbucks-ab-testing.git
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels
```

3. Open the notebook:
```bash
jupyter notebook A_B_testing_starbucks.ipynb
```

Or open directly in [Google Colab](https://colab.research.google.com/).

---

## 📋 Project Structure
```
starbucks-ab-testing/
│
├── A_B_testing_starbucks.ipynb    # Main analysis notebook
├── portfolio.csv                   # Offer information
├── profile.csv                     # Customer demographics
├── transcript.csv                  # Event log data
├── README.md                       # This file
└── starbucks_analysis_dataset.csv  # Cleaned analysis dataset (output)
```

---

## ⚠️ Limitations & Future Work

**Limitations:**
- Small control group (72 customers) limits causal inference
- Potential selection bias - customers receiving offers may differ systematically
- 30-day window may not capture long-term customer lifetime value effects

**Future Improvements:**
- Propensity score matching to create synthetic control group
- Uplift modeling to predict individual treatment effects
- Time series analysis for seasonality and offer fatigue
- A/B test simulation with proper randomization

---

## 👤 Author

**Rohini Vishwanathan**  
M.S. Information Systems & Technology (Data Science) | Claremont Graduate University

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue.svg)](https://linkedin.com/in/rohini-vishwanathan)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black.svg)](https://github.com/RohiniVishwanathan)

---

## 📄 License

This project is for educational and portfolio purposes.


---

## 🤖 AI Acknowledgment

This project was developed with assistance from Claude (Anthropic) for:
- Code structure and best practices
- Statistical test selection and interpretation
- README documentation

All analysis was executed, validated, and interpreted by me. I fully understand the methodology and can explain all aspects of this project.

---
