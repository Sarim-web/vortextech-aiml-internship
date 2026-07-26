# Sentiment Analysis on Amazon Product Reviews

VortexTech AI/ML Internship — Week 4 (Capstone Project)

## Overview
This project builds a sentiment classifier that predicts whether an Amazon
product review is **positive** or **negative**, using TF-IDF feature
extraction and Logistic Regression.

## Dataset
[Amazon Reviews 2023](https://www.kaggle.com/datasets/ravirajbabasomane/amazon-reviews-2023)
(Kaggle). Not included in this repo due to size — download it and place the
CSV in `data/raw/`.

Labels are derived from star ratings: 4–5 stars = positive, 1–2 stars =
negative, 3-star reviews excluded as ambiguous.

## Results
| Model | Accuracy | F1-score |
|---|---|---|
| Logistic Regression | 90.15% | 0.9007 |
| Multinomial Naive Bayes | 88.45% | 0.8835 |

## Project Structure
data/raw/          → raw dataset (not tracked in git)
notebooks/         → main analysis notebook
requirements.txt   → dependencies

## How to Run
1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Download the dataset and place it in `data/raw/`
4. Open and run `notebooks/week4_sentiment_analysis_model.ipynb`

## Key Limitation
TF-IDF represents text as an unordered bag of words, so it cannot capture
word order or clause-level structure. This means contrastive sentences
(e.g. "great but overpriced") are harder to classify reliably. See the
notebook's final section for detailed error analysis.

## Author
Sarim — VortexTech AI/ML Internship