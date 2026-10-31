<div align="center">

# QuerySense

### Detecting duplicate questions using Natural Language Processing

A machine learning application that compares two questions and predicts whether they express the same meaning.

<br>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge\&logo=scikitlearn\&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-Text%20Processing-8A2BE2?style=for-the-badge)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge\&logo=streamlit\&logoColor=white)

</div>

---

## Overview

QuerySense tackles the duplicate question detection problem using the Quora Question Pairs dataset.

Given two questions, the application predicts whether they are duplicates based on their textual similarity and extracted linguistic features.

**Example**

| Question 1              | Question 2                            |
| ----------------------- | ------------------------------------- |
| How can I learn Python? | What is the best way to learn Python? |

**Prediction:** Duplicate

---

## Features

* **Text preprocessing** — Cleans and normalizes question text.
* **Bag of Words** — Converts questions into numerical feature vectors.
* **Feature engineering** — Extracts common-word, token, and question-length features.
* **Fuzzy matching** — Uses string similarity measures to compare question pairs.
* **ML classification** — Predicts whether two questions are duplicates.
* **Interactive interface** — Provides predictions through a Streamlit application.

---

## How It Works

```text
       Question 1          Question 2
             │                  │
             └────────┬─────────┘
                      │
                Text Preprocessing
                      │
                Feature Extraction
                      │
          ┌───────────┴───────────┐
          │                       │
       Bag of Words          Engineered Features
          │                       │
          └───────────┬───────────┘
                      │
               ML Classification
                      │
                Prediction
                      │
             Duplicate / Not Duplicate
```

---

## Tech Stack

| Category         | Technologies                 |
| ---------------- | ---------------------------- |
| Language         | Python                       |
| Machine Learning | Scikit-learn                 |
| NLP              | Bag of Words, Fuzzy Matching |
| Data Processing  | NumPy, Pandas                |
| Visualization    | Matplotlib, Seaborn          |
| Web Application  | Streamlit                    |

---

## Project Structure

```text
QuerySense/
│
├── initial_EDA.ipynb
├── only-bow.ipynb
├── bow-with-basic-features.ipynb
├── bow-with-preprocessing-and-advanced-features.ipynb
│
└── streamlit-app/
    ├── app.py
    ├── helper.py
    ├── requirements.txt
    └── Procfile
```

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/ankvsh/QuerySense.git
cd QuerySense
```

### 2. Install dependencies

```bash
pip install -r streamlit-app/requirements.txt
```

### 3. Prepare model files

The Streamlit application loads the trained model and vectorizer using pickle.

Make sure these files are available in the `streamlit-app/` directory:

* `model.pkl`
* `cv.pkl`
* `stopwords.pkl`

These artifacts must be generated or obtained before running the application.

### 4. Run the application

```bash
cd streamlit-app
streamlit run app.py
```

---

## Dataset

The project uses the **Quora Question Pairs** dataset.

Dataset: [Kaggle — Quora Question Pairs](https://www.kaggle.com/c/quora-question-pairs)

---

## Author

**Ankush Gupta**

Data Science Undergraduate | IIT Madras

[GitHub](https://github.com/ankvsh)

---

<div align="center">

**QuerySense — Comparing questions beyond their wording.**

</div>
