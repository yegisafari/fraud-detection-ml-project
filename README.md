# Fraud Detection on PaySim Dataset

This project explores fraud detection using the PaySim dataset, which simulates real-world mobile money transactions.

The main challenge in this problem is that fraud cases are extremely rare, making it difficult for machine learning models to detect them effectively.

---

## My Approach

I didn’t just train a model, I tried to understand how the model behaves under imbalance.

Steps I followed:

* Explored the dataset to identify patterns in fraudulent transactions
* Converted categorical transaction types into numerical features
* Built a baseline model (Random Forest)
* Observed that it failed to detect fraud properly
* Applied SMOTE to handle class imbalance
* Switched to XGBoost for better learning on tabular data
* Tuned the decision threshold instead of using the default 0.5

---

## Final Model Performance

* Recall (fraud detection): ~0.72
* Precision: ~0.03
* ROC-AUC: ~0.96

---

## What I learned

This project changed how I think about machine learning models.

At first, I expected to improve all metrics, but I realized that:

* Increasing fraud detection (recall) leads to more false positives
* Reducing false positives causes more fraud to be missed
* There is no perfect model in imbalanced problems

Instead of chasing perfect accuracy, the goal is to **find the right trade-off depending on the application**.

---

## Key Insight

In fraud detection systems, missing a fraud case can be more costly than a false alarm.

Because of this, the model is intentionally tuned to be more sensitive, even if it produces more false positives.

---

## Tools & Libraries

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Imbalanced-learn (SMOTE)
* Matplotlib

---

## Final Thought

This project is less about building a perfect model and more about understanding model behavior, limitations, and decision-making under real-world constraints.

---

## Author

Yeganeh Safari
