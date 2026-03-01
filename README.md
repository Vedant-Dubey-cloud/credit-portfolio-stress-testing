# Credit Portfolio Stress Testing using Monte Carlo Simulation

## 📌 Overview

This project develops a Monte Carlo-based credit risk stress testing framework to evaluate capital adequacy under normal and adverse economic conditions.

The model simulates portfolio loss distributions, measures tail risk exposure, and evaluates the strategic impact of tightening credit policy on solvency resilience.

---

## 🎯 Objective

To assess whether the existing capital buffer sufficiently protects against extreme portfolio losses and to analyze how stress scenarios and underwriting adjustments influence capital stability.

---

## ⚙️ Methodology

- 5,000 Monte Carlo simulations  
- Loan-level Probability of Default (PD) estimated via risk segmentation  
- Loss Given Default (LGD) = 60%  
- Defaults simulated using a Bernoulli process  
- Portfolio loss calculated as:

  Loss = Default × Loan Amount × LGD  

- Capital calibrated at the **99th percentile (VaR)** of the normal loss distribution  

### Capital Buffer (99% VaR – Normal Scenario):
₹39.84 million

---

## 📊 Scenario Analysis

### 1️⃣ Normal Scenario
- Expected Loss: ₹38.94M  
- 99% VaR: ₹39.84M  
- Capital Breach Probability: 1%  

Under stable economic conditions, the portfolio remains adequately capitalized with limited tail exposure.

---

### 2️⃣ Stress Scenario
- Expected Loss: ₹40.37M  
- 99% VaR: ₹41.31M  
- Capital Breach Probability: 58.54%  

Adverse deterioration among high-risk borrowers materially shifts the loss distribution.  
Approximately 58% of simulated outcomes exceed the available capital buffer, indicating significant vulnerability during downturns.

---

### 3️⃣ Policy Tightening Scenario
- Expected Loss: ₹24.05M  
- 95% VaR: ₹24.78M  
- Capital Breach Probability: 0%  
- Loan Approval Reduction: 33%  

Selective restriction of high-risk borrower approvals substantially reduces expected and tail losses, fully eliminating capital breach risk. However, this comes at the cost of reduced portfolio growth.

---

## 📈 Key Insights

- Capital adequacy is highly sensitive to concentration in high-PD segments.
- Tail risk expands disproportionately during stress events.
- Stability under normal conditions may mask structural downside exposure.
- Risk-based underwriting materially strengthens solvency resilience.
- A measurable trade-off exists between portfolio growth and capital protection.

---

## 🛠 Technologies Used

- Python  
- NumPy  
- Pandas  
- Seaborn  
- Matplotlib  

---

## ▶️ How to Run

1. Install dependencies:
   pip install numpy pandas matplotlib seaborn

2. Run:
   credit_portfolio_stress_testing.ipynb

---

## 📂 Repository Structure

- credit_portfolio_stress_testing.ipynb — Simulation model  
- Credit_Portfolio_Stress_Testing_Report.pdf — Executive summary  
- requirements.txt — Dependencies  

---

## 📌 Conclusion

This project demonstrates how Monte Carlo simulation provides a probabilistic, distribution-based assessment of credit risk and capital adequacy. The analysis highlights the sensitivity of solvency outcomes to stress conditions and strategic credit policy decisions.
