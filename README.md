# 🌟 NayePankh Foundation — Fundraising Amount Predictor
### Machine Learning Internship | Option 2 — ML Project

---

## 📌 Project Overview

This project builds a **Machine Learning model to predict the fundraising amount** a campaign can raise, based on campaign features like platform, duration, donor history, social reach, and seasonal patterns.

Built as part of the **NayePankh Foundation ML Internship**, this project demonstrates real-world ML skills including data generation, exploratory analysis, model training, comparison, and deployment-ready prediction.

---

## 🗂️ File Structure

```
NayePankh_Fundraising_Predictor/
│
├── NayePankh_Fundraising_Predictor.ipynb   # Main Jupyter Notebook
└── README.md                                # This file
```

---

## 🧠 Problem Statement

NGOs like NayePankh Foundation run multiple fundraising campaigns across different platforms and causes. The goal is to **predict how much money a campaign will raise** before it launches, so the team can:

- Set realistic fundraising targets
- Allocate volunteer and marketing resources efficiently
- Identify the best time and platform to run campaigns
- Maximize donor engagement

---

## 📊 Dataset

A **synthetic but realistic dataset** of 500 NGO fundraising campaigns was generated, modeled after real NGO patterns.

| Feature | Description |
|---|---|
| `campaign_type` | Education, Health, Women Empowerment, Environment, Child Welfare |
| `platform` | Instagram, Facebook, WhatsApp, Email, Website |
| `month` | Month the campaign ran (Jan–Dec) |
| `duration_days` | How long the campaign ran |
| `num_posts` | Number of social media posts published |
| `avg_post_reach` | Average reach per post |
| `num_volunteers` | Volunteers involved |
| `past_donors_count` | Number of past donors reached |
| `avg_past_donation_inr` | Average past donation amount (₹) |
| `matching_donation` | Whether a matching donation was offered (0/1) |
| `celebrity_endorsement` | Whether a celebrity endorsed the campaign (0/1) |
| `email_subscribers` | Size of the email list |
| `social_shares` | Number of shares the campaign received |
| `funds_raised_inr` | **Target variable — total funds raised (₹)** |

---

## 🤖 Models Used

| Model | Type | Notes |
|---|---|---|
| Linear Regression | Baseline | Simple, interpretable |
| Ridge Regression | Regularized Linear | Handles multicollinearity |
| Random Forest | Ensemble (Trees) | Robust, handles non-linearity |
| **Gradient Boosting** | **Ensemble (Boosting)** | **Best performer 🏆** |

---

## 📈 Results

| Model | R² Score | MAE |
|---|---|---|
| Linear Regression | ~0.80 | Higher |
| Ridge Regression | ~0.81 | Similar |
| Random Forest | ~0.94 | Low |
| **Gradient Boosting** | **~0.96** | **Lowest** |

> **Gradient Boosting** achieved the highest accuracy with ~96% R² score and the lowest Mean Absolute Error.

---

## 🔑 Key Insights

1. **Festive months (Oct–Jan)** drive the highest donations — plan major campaigns here
2. **Matching donations** boost fundraising by ~40% — seek corporate partners
3. **Email list size & past donor count** are the strongest predictors of success
4. **Education & Child Welfare** campaigns raise the most funds
5. **Email and Instagram** outperform other platforms for fundraising reach

---

## 🔮 Predictor Tool

The notebook includes a ready-to-use `predict_fundraising()` function:

```python
predicted = predict_fundraising(
    campaign_type='Education',
    platform='Instagram',
    month='Oct',
    duration_days=30,
    num_posts=25,
    avg_post_reach=6000,
    num_volunteers=40,
    past_donors_count=250,
    avg_past_donation_inr=600,
    matching_donation=1,
    celebrity_endorsement=0,
    email_subscribers=1500,
    social_shares=500
)
# Output: ₹ estimated fundraising amount
```

---

## 🛠️ How to Run

### Option 1 — Google Colab (Recommended, no setup)
1. Upload `NayePankh_Fundraising_Predictor.ipynb` to [colab.research.google.com](https://colab.research.google.com)
2. Click **Runtime → Run All**

### Option 2 — Local Jupyter
```bash
# Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn jupyter

# Launch notebook
jupyter notebook NayePankh_Fundraising_Predictor.ipynb
```

---

## 📦 Dependencies

```
numpy
pandas
matplotlib
seaborn
scikit-learn
colab
```

---

## 👤 Author

**NayePankh Foundation ML Internship**
Submitted as: Option 2 — Create a Simple Machine Learning Project

---

## 📜 License

This project is submitted for internship evaluation purposes only.
