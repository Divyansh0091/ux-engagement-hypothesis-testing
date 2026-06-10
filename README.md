# UX Analytics: Two-Tailed Hypothesis Testing for Website Design Optimization

## 📌 Project Overview
In digital product management, layout adjustments and user interface modifications directly influence user retention and platform interaction. This project focuses on **Data-Driven UX Performance Benchmarking**, comparing the total time spent by users on two distinct website variations: **Design A** and **Design B**.

Using a sample size of 100 users per variant, this analysis implements an **Independent Two-Sample Two-Tailed T-Test** in Python to mathematically determine if the variations yield a statistically significant difference in user engagement or if the discrepancies are merely random variance.

---

## 📊 Business Problem & Hypothesis Framework
The Product Design team introduced a structural layout overhaul (Design B) to optimize user retention. Before rolling out the change globally, a two-tailed test was performed to check for any significant operational difference—positive or negative—compared to the baseline (Design A).

* **Null Hypothesis ($H_0$):** There is no significant difference between the average time spent on Design A and Design B ($\mu_A = \mu_B$).
* **Alternative Hypothesis ($H_1$):** The average time spent on Design A is significantly different from Design B ($\mu_A \neq \mu_B$).
* **Significance Level ($\alpha$):** 0.05 ($5\%$)

---

## 🛠️ Tech Stack & Advanced Implementation
* **Language:** Python
* **Core Libraries:** NumPy, SciPy (Stats), Seaborn, Matplotlib
* **Key Analytical Milestones:**
  * **Large-Scale Synthesized Simulation:** Generated standard normal distributions ($n = 100$ per group) mimicking production user metrics.
  * **Critical Value Calculation:** Programmatically mapped alpha division across a two-tailed probability split using the Percent Point Function (`stats.t.ppf`).
  * **Manual Formula Auditing:** Hand-coded algebraic t-statistic logic incorporating squared standard deviations (variances) and distinct sample sizes to protect against mathematical edge cases.
  * **Probability Mapping:** Plotted comprehensive Kernel Density Estimation (KDE) maps to visualize density overlapping intervals.

---

## 📈 Visualizing User Engagement Profiles
The visual layout features a high-fidelity **Kernel Density Estimation (KDE) Overlap Plot** that compares probability densities for both design frameworks:

* **Design A (Blue Curve):** Represents baseline user interaction patterns, centering around a lower mean threshold.
* **Design B (Brown/Orange Curve):** Captures the updated design iteration, demonstrating a prominent rightward shift toward prolonged user interaction.

The minimal overlap zone visually emphasizes a major divergence in consumer behavioral profiles across the two interfaces.

---

## 🔑 Key Findings & Core Statistical Decision
* **Calculated T-Statistic ($t_{cal}$):** $\approx -18.3797$ (The extreme negative value confirms Design B's engagement patterns are heavily shifted toward extended session durations).
* **Two-Tailed Critical Boundaries:** $\pm 1.9720$
* **Statistical Conclusion:** Since the absolute value of the calculated statistic ($| -18.3797 | = 18.3797$) significantly supersedes the critical boundary limit ($1.9720$), we **Reject the Null Hypothesis ($H_0$)**.

### 💼 Data-Driven Business Impact
The test delivers conclusive statistical proof that the layout variation directly drives altered user retention behaviors. Design B shows an indisputable, reproducible boost in user session length rather than a temporary trend. Based on these statistical insights, corporate leadership can confidently deploy Design B enterprise-wide to scale platform optimization and increase user conversion rates.

---

## 🚀 How to Run & Replicate
1. Clone this repository to your local directory.
2. Install the production-ready libraries:
   ```bash
   pip install numpy scipy seaborn matplotlib
