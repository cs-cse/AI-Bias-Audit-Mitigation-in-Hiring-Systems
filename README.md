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
- Analyze conflicts between different fairness definitions  

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
   - Demographic Parity (selection rate)
   - Equal Opportunity (True Positive Rate)  
   - Disparate Impact  
5. Apply mitigation using fairness-constrained optimization (Fairlearn)  
6. Re-evaluate fairness and performance  

<br>

## 📉 Results

### 🔴 Before Mitigation
- **Selection Rate**
  - Female: **7.3%**
  - Male: **25.4%**
- **Disparate Impact:** **0.29** (severely biased)

- **Equal Opportunity (TPR)**
  - Female: **0.54**
  - Male: **0.62**

- **Accuracy:** **85.73%**

<br>

### 🟢 After Mitigation
- **Selection Rate**
  - Female: **15.6%**
  - Male: **17.7%**
- **Disparate Impact:** **0.87** (within acceptable threshold)

- **Equal Opportunity (TPR)**
  - Female: **0.80**
  - Male: **0.47**

- **Accuracy:** **84.06%**

<br>

## ⚖️ Trade-off Analysis

- Bias significantly reduced (**Disparate Impact: 0.29 → 0.87**)  
- Accuracy decreased slightly (**85.73% → 84.06%**, ~1.7% drop)  

### Multi-Metric Insight
- Selection fairness improved significantly  
- However, Equal Opportunity (TPR) disparity increased  

👉 This demonstrates that:
> Improving one fairness metric can introduce bias in another, highlighting the inherent trade-offs in responsible AI systems.

<br>

## 🧠 Key Insights

- Machine learning models can inherit bias from historical data  
- Fairness constraints can effectively reduce selection bias  
- Different fairness metrics (Demographic Parity vs Equal Opportunity) can conflict  
- Responsible AI requires balancing fairness, accuracy, and context-specific priorities  
- Bias mitigation is not a one-time fix and requires continuous evaluation  

<br>

## 📊 Visualization

The project includes a bar chart comparing selection rates before and after mitigation, illustrating improved parity across groups.

<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/b4398f61-84c9-4ed8-8a50-9338be459d28" />


<br>

## 🛠️ Tech Stack

- Python  
- Pandas  
- Scikit-learn  
- Fairlearn  
- Matplotlib  
- Google Colab  

<br>

## 🚀 Future Improvements

- Optimize for multiple fairness constraints simultaneously  
- Add additional fairness metrics (False Positive Rate parity)  
- Extend to NLP-based resume screening systems  
- Build real-time fairness monitoring dashboard  
- Deploy model via API for production simulation  

<br>

## 📌 Conclusion

This project demonstrates how bias in AI systems can be:
- Detected  
- Quantified  
- Mitigated  

It highlights the practical challenges of balancing fairness and performance, and emphasizes that fairness is a multi-dimensional problem requiring context-aware decision-making.

<br>

## 📎 Author

[Chaitanya Shrivastava](https://www.linkedin.com/in/chaitanya-shrivastava)
