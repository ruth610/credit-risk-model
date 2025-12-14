# credit-risk-model

## Credit Scoring Business Understanding

### Basel II Accord and Model Interpretability

The Basel II Capital Accord emphasizes risk-sensitive capital requirements and mandates that financial institutions measure, manage, and document credit risk in a transparent and auditable manner. This regulatory framework requires banks to clearly explain how credit decisions are made, how risk is quantified, and how models are validated and monitored over time.

As a result, credit risk models must be interpretable and well-documented. Interpretability allows regulators, auditors, and internal risk teams to understand how input variables influence predictions, while documentation ensures reproducibility and accountability. In this project, where alternative behavioral data replaces traditional credit bureau data, transparency is particularly important to justify the model’s assumptions and outcomes.

---

### Proxy Variable for Credit Risk

The dataset does not include a direct indicator of loan default, which is typically required for supervised credit risk modeling. Therefore, creating a proxy target variable is necessary. We approximate credit risk by identifying disengaged customers using behavioral metrics derived from Recency, Frequency, and Monetary (RFM) analysis.

Customers with low transaction frequency, low monetary value, and long inactivity periods are labeled as high-risk proxies. While this approach enables model training, it introduces potential business risks such as label noise, bias, and misclassification. Disengaged behavior does not always equate to loan default. However, proxy-based modeling is a widely accepted approach in alternative credit scoring, especially in data-scarce environments, provided assumptions are clearly documented and regularly reviewed.

---

### Trade-offs Between Model Interpretability and Performance

There is an inherent trade-off between simple, interpretable models and complex, high-performance models in regulated financial environments.

Interpretable models such as Logistic Regression with Weight of Evidence (WoE) offer transparency, regulatory friendliness, and stability but may struggle to capture nonlinear relationships. In contrast, complex models like Gradient Boosting can achieve higher predictive accuracy by modeling intricate patterns but are harder to explain and govern.

In this project, both approaches are evaluated. The final model selection prioritizes not only predictive performance but also regulatory compliance, explainability, and operational risk considerations.
