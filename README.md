# 🛒 Week 5: A/B Testing Strategy in E-Commerce

## 📌 Project Overview

This project is part of my **Data Science Internship – Week 5 Task**. The objective is to design a comprehensive **A/B Testing strategy for an e-commerce environment**.

A/B testing is a controlled experimental technique used to compare two versions of a website, marketing campaign, product page, or feature. In this project, an e-commerce product-page **Call-to-Action (CTA)** is selected as the experiment subject.

The proposed experiment compares the existing CTA (**Control – A**) with a redesigned CTA (**Treatment – B**) to determine whether the new design can improve customer purchase conversion.

The project focuses on experiment design, hypothesis formulation, sampling, randomization, KPI selection, sample-size planning, statistical analysis, and result interpretation.

---

## 🎯 Objectives

The main objectives of this project are:

* Understand the importance of A/B testing in e-commerce.
* Design a controlled experiment for an e-commerce website.
* Formulate null and alternative hypotheses.
* Define control and treatment groups.
* Develop a suitable sampling and randomization strategy.
* Identify primary, secondary, and guardrail KPIs.
* Plan appropriate sample-size determination.
* Identify potential confounding factors and sources of bias.
* Select suitable statistical tests.
* Define clear decision rules for interpreting experiment results.
* Provide recommendations based on statistical and business significance.

---

## 🧪 Experiment Scenario

### Experiment

The experiment tests whether a **redesigned Product Page CTA** can improve purchase conversion.

### Control Group – A

Users see the existing product-page CTA.

### Treatment Group – B

Users see the redesigned CTA with improved wording and visual prominence.

### Randomization

Eligible users are randomly assigned to either:

* **50% → Control Group (A)**
* **50% → Treatment Group (B)**

The assignment should remain persistent so that the same user does not switch between variants.

---

## 💡 Hypothesis

### Null Hypothesis (H₀)

The redesigned CTA does **not** change the purchase conversion rate compared with the existing CTA.

### Alternative Hypothesis (H₁)

The redesigned CTA **increases the purchase conversion rate** compared with the existing CTA.

### Success Criteria

The treatment will be considered successful when:

* The improvement is statistically significant.
* **p-value < 0.05**
* The confidence interval supports a positive treatment effect.
* The improvement meets the predefined business minimum detectable effect.
* Important guardrail metrics do not deteriorate.

---

## 📊 Key Performance Indicators (KPIs)

### Primary KPI

**Purchase Conversion Rate**

```text
Conversion Rate =
Number of Purchasers / Number of Eligible Users × 100
```

### Secondary KPIs

* Add-to-Cart Rate
* Checkout Completion Rate
* Average Order Value (AOV)
* Revenue per Visitor
* CTA Click/Interaction Rate

### Guardrail Metrics

* Bounce/Exit Rate
* Page Load Time
* Technical Error Rate
* Refund/Cancellation Rate
* Customer Complaints

---

## 🔬 Experimental Design

| Component          | Design                   |
| ------------------ | ------------------------ |
| Experiment Type    | A/B Test                 |
| Control            | Existing CTA             |
| Treatment          | Redesigned CTA           |
| Allocation         | 50% / 50%                |
| Randomization Unit | User/Visitor             |
| Primary KPI        | Purchase Conversion Rate |
| Significance Level | α = 0.05                 |
| Statistical Power  | 80%                      |
| Analysis           | Two-Proportion Test      |
| Confidence Level   | 95%                      |

---

## 👥 Sampling Method

The target population consists of eligible e-commerce visitors who reach the selected product pages during the experiment period.

Users should be randomly assigned to either the control or treatment group.

Users may be excluded when:

* They are internal employees or test accounts.
* Technical problems prevent proper exposure.
* They do not meet experiment eligibility criteria.
* Required tracking events are missing.

Important segments for analysis include:

* New vs Returning Users
* Mobile vs Desktop
* Organic vs Paid Traffic
* Different Geographic Markets
* Different Product Categories

---

## 📏 Sample Size Planning

Sample size should be determined **before launching the experiment**.

Important parameters include:

* Baseline conversion rate
* Minimum Detectable Effect (MDE)
* Significance level (α)
* Statistical power
* Expected treatment effect

A commonly used setup is:

```text
Significance Level = 5%
Statistical Power = 80%
Confidence Level = 95%
```

For example, if the baseline conversion rate is **4.0%**, the business may define an improvement to **4.4%** as the minimum effect worth detecting.

The experiment should not be stopped early simply because an initial result appears positive.

---

## 📥 Data Collection

The experiment should collect event-level data such as:

```text
experiment_id
anonymous_user_id
variant
exposure_timestamp
product_category
device_type
traffic_source
add_to_cart
checkout_started
purchase_completed
order_value
```

The data should be collected consistently for both Control and Treatment groups.

---

## ⚠️ Potential Confounding Factors

Several factors can influence experiment results:

* Seasonal demand
* Marketing campaigns
* Product availability
* Pricing changes
* Traffic source
* Device type
* Website performance
* Promotional offers
* Holidays or special events
* Technical problems

To reduce bias, unrelated website or marketing changes should be avoided during the experiment whenever possible.

---

## 📈 Statistical Analysis

The primary KPI is a binary outcome:

```text
Purchase = Yes / No
```

Therefore, the primary analysis can use a **two-proportion z-test**.

The analysis should report:

1. Control conversion rate
2. Treatment conversion rate
3. Absolute lift
4. Relative lift
5. 95% confidence interval
6. p-value
7. Effect size
8. Business impact

### Absolute Lift

```text
Treatment Conversion − Control Conversion
```

### Relative Lift

```text
(Treatment Conversion − Control Conversion)
------------------------------------------------ × 100
        Control Conversion
```

---

## 📊 Example Interpretation

Suppose:

```text
Control Conversion Rate   = 4.0%
Treatment Conversion Rate = 4.5%
```

Then:

```text
Absolute Lift = 4.5% − 4.0%
              = 0.5 percentage points

Relative Lift = 12.5%
```

If the statistical test produces:

```text
p-value < 0.05
```

and the confidence interval supports a positive effect, the evidence would support the treatment.

However, statistical significance alone is not enough. The improvement should also be large enough to provide meaningful business value.

---

## 🚦 Decision Framework

| Result                                 | Decision                           |
| -------------------------------------- | ---------------------------------- |
| Significant positive result            | Consider rolling out Treatment     |
| Non-significant result                 | Keep Control / redesign and retest |
| Significant but very small improvement | Evaluate ROI before rollout        |
| Negative treatment effect              | Stop or rollback Treatment         |
| Guardrail metrics deteriorate          | Investigate before rollout         |

---

## 🗂️ Project Structure

```text
Week-5-AB-Testing-Ecommerce/
│
├── README.md
│
├── Week_5_AB_Testing_Ecommerce_Internship_Report.docx
│
├── data/
│   └── README.md
│
├── analysis/
│   └── README.md
│
└── references/
    └── README.md
```

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib
* Jupyter Notebook
* Microsoft Word
* GitHub
* Statistical Hypothesis Testing

---

## 🔄 A/B Testing Workflow

```text
Business Problem
       ↓
Experiment Objective
       ↓
Hypothesis Formation
       ↓
Define Control & Treatment
       ↓
Randomization
       ↓
Sample Size Planning
       ↓
Data Collection
       ↓
KPI Measurement
       ↓
Statistical Testing
       ↓
Result Interpretation
       ↓
Business Decision
```

---

## ✅ Quality Assurance Checklist

* [x] Define experiment objective
* [x] Define null hypothesis
* [x] Define alternative hypothesis
* [x] Select primary KPI
* [x] Define secondary KPIs
* [x] Define guardrail metrics
* [x] Design control and treatment groups
* [x] Define randomization strategy
* [x] Plan sample size
* [x] Identify confounding factors
* [x] Define statistical analysis
* [x] Define decision rules
* [x] Document experiment execution process

---

## 📌 Expected Business Impact

A successful A/B testing framework can help an e-commerce company:

* Increase conversion rates
* Improve customer experience
* Reduce cart abandonment
* Increase revenue
* Optimize product pages
* Improve marketing campaigns
* Make data-driven decisions
* Reduce the risk of deploying ineffective changes

---

## 🏁 Conclusion

This project presents a complete framework for designing and implementing an A/B testing strategy in an e-commerce environment.

The proposed experiment compares an existing product-page CTA with a redesigned CTA using randomized user assignment. The strategy includes hypothesis formulation, sampling, randomization, KPI selection, sample-size planning, data collection, statistical testing, and business decision-making.

The key principle is to define the experiment and success criteria **before observing the final results**. Both statistical significance and practical business significance should be considered before making a rollout decision.

This framework can also be extended to test **website layouts, product recommendations, promotional offers, checkout processes, email campaigns, search results, and other e-commerce features**.

---

## 📚 References / Statistical Concepts

* A/B Testing
* Randomized Controlled Experiments
* Hypothesis Testing
* Two-Proportion Z-Test
* Chi-Square Test
* Confidence Intervals
* P-Values
* Statistical Power
* Minimum Detectable Effect (MDE)
* Effect Size
* Bootstrap Methods
* Business Significance vs Statistical Significance

---

## 👨‍💻 Internship Task

**Week:** 5
**Domain:** Data Science / E-Commerce
**Task:** Designing and Implementing A/B Testing Strategies in E-Commerce
**Deliverable:** A/B Testing Strategy Report
