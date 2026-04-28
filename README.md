# AI Bias Audit & Mitigation in Hiring Systems



## 📌 Overview
Automated hiring systems can unintentionally introduce bias against protected groups.  
This project audits a machine learning model for gender bias and applies mitigation techniques to improve fairness while maintaining performance.

<br>

## 🎯 Objective
- Detect bias in a hiring prediction model  
- Quantify bias using standard fairness metrics  
- Apply mitigation techniques  
- Evaluate fairness vs accuracy trade-offs  

<br>

## 📊 Dataset
- UCI Adult Income Dataset  
- Used as a proxy for hiring decisions (predicting income >50K as selection)

<br>

## ⚙️ Methodology

1. Data preprocessing (cleaning, encoding, scaling)  
2. Train baseline Logistic Regression model  
3. Evaluate performance (accuracy)  
4. Measure fairness using:
   - Demographic Parity  
   - Disparate Impact  
5. Apply mitigation using fairness-constrained optimization (Fairlearn)  
6. Re-evaluate fairness and performance  

<br>

## 📉 Results

### 🔴 Before Mitigation
- Female selection rate: **7.3%**
- Male selection rate: **25.4%**
- Disparate Impact: **0.29** (severely biased)
- Accuracy: **85.73%**

<br>

### 🟢 After Mitigation
- Female selection rate: **15.5%**
- Male selection rate: **17.7%**
- Disparate Impact: **0.87** (within acceptable threshold)
- Accuracy: **84.06%**

<br>

## ⚖️ Trade-off Analysis

- Bias significantly reduced (**0.29 → 0.87**)  
- Accuracy decreased slightly (**85.73% → 84.06%**, ~1.7% drop)

**Insight:**  
A small reduction in accuracy resulted in a substantial improvement in fairness, demonstrating a practical fairness-performance trade-off.

<br>

## 🧠 Key Insights

- Machine learning models can inherit bias from historical data  
- Fairness constraints can effectively reduce bias  
- Trade-offs between fairness and accuracy are inevitable  
- Responsible AI requires continuous monitoring, not one-time fixes  

<br>

## 🛠️ Tech Stack

- Python  
- Pandas  
- Scikit-learn  
- Fairlearn  
- Jupyter Notebook / Google Colab  

<br>

## 🚀 Future Improvements

- Add additional fairness metrics (TPR/FPR parity)  
- Extend to resume screening (NLP-based models)  
- Build real-time bias monitoring dashboard  
- Deploy model with API for production simulation  

<br>

## 📌 Conclusion

This project demonstrates how bias in AI systems can be detected, quantified, and mitigated effectively.  
It highlights the importance of balancing fairness and performance in real-world machine learning applications.

<br>

## 📎 Author

  
[Chaitanya Shrivastava](https://www.linkedin.com/in/chaitanya-shrivastava)
