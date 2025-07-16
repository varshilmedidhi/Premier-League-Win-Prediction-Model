# ⚽ EPL Match Outcome Predictor

A machine learning pipeline to predict the outcome (win/loss) of English Premier League (EPL) matches using historical match statistics and engineered features.

---

## 📌 Project Overview

This project leverages historical match data from two EPL seasons to predict whether a team will win a match. It includes full data preprocessing, feature engineering, model training, and evaluation using a Random Forest Classifier.

- **Goal:** Predict win/loss outcomes for football teams.
- **Data:** 1,300+ EPL matches from the 2020–2022 seasons.
- **Model:** Random Forest Classifier from scikit-learn.
- **Target:** Binary win outcome (`1` = Win, `0` = Draw/Loss).

---

## 🧰 Tech Stack

- **Language:** Python
- **Libraries:** pandas, NumPy, scikit-learn
- **Environment:** Jupyter Notebook / VS Code

---

## 🧠 Features & Engineering

- Converted categorical features (venue, opponent, date) into numeric codes.
- Engineered temporal features: match hour, day of week.
- Created rolling averages for key stats like:
  - Goals for/against
  - Shots, shots on target
  - Distance, free kicks, penalties
- Mapped team names to simplify home/away comparisons.

---

## 🔍 Model Training

- Used `RandomForestClassifier` with `n_estimators=100`, `min_samples_split=10`.
- Split data into training (pre-2022) and testing (post-2022) sets.
- Evaluation metrics:
  - **Accuracy:** ~60.8%
  - **Precision (win prediction):** ~60.7% (after feature engineering)

---

## 📈 Results

- Improved win prediction precision from **~46.7%** to **~60.7%** using rolling averages.
- Final model effectively captured team momentum and contextual features.

---

## 📂 File Structure

```
EPL-Predictor/
├── data/
│   └── matches.csv
├── notebooks/
│   └── epl_predictor.ipynb
├── README.md
└── requirements.txt
```

---

## 🚀 How to Run

1. Clone this repo:
```bash
git clone https://github.com/your-username/epl-predictor.git
cd epl-predictor
```
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run the notebook:
```bash
jupyter notebook notebooks/epl_predictor.ipynb
```

---

## 📌 Future Improvements

- Add visualization of feature importance and match outcomes.
- Incorporate player-level stats.
- Experiment with gradient boosting and deep learning models.

---

## 📬 Contact
Feel free to reach out if you’re interested in collaborating or discussing football analytics!

**Varshil**  
Email : varshil.py@gmail.com
