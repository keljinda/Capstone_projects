# Insider Cyber Threat Detection using CERT Data

This project focuses on detecting insider cybersecurity threats using data from the Computer Emergency Response Team (CERT). By leveraging Natural Language Processing (NLP) and machine learning techniques, the project identifies behavioural and contextual anomalies to flag potential insider threats. The study incorporates insights from the OCEAN (Big Five personality traits) model to theorize psychological influences on insider risk. The project evaluates two primary approaches:

1.  Contextual Analysis: Focused on analyzing textual data (cleaned_email) using NLP techniques.

2. Feature Selection: Focused on structured numerical and categorical features to analyze behavioral and contextual patterns.

The goal is to develop robust detection models that balance recall (to minimize missed threats) and precision (to reduce false positives) for practical implementation.

## Methodology

1. Data Preprocessing

	• Text Preprocessing (for Contextual Analysis):

	- Emails were tokenized and lemmatized.

	- Stop words were removed, and TF-IDF vectors were generated for cleaned_email.

	•  Structured Data Preprocessing (for Feature Selection):

	- Categorical variables were encoded, and numerical features were scaled.

	- The following structured features were selected:num_recipients, hour, day_of_week, attachments, size, sentiment_score, keyword_threat, and anomaly.

2. OCEAN Model Hypothesis

	The Big Five Personality Traits (OCEAN) were used to theorize psychological influences on insider risks:

	• Conscientiousness [C]:

	- Lower C: Higher accidental risks due to poor security hygiene.

	- Higher C: Predictable behavior patterns, which can be exploited.

	•  Openness [O]:

	- Lower O: Resistance to new security measures.

	- Higher O: More experimentation with unauthorized systems/tools.

	•  Agreeableness [A]:

	- Lower A: Independent, potentially policy-breaking actions.

	- Higher A: Vulnerable to social engineering.

	•  Extraversion [E]:

	- Lower E: Reduced detection due to less interaction.

	- Higher E: Oversharing of information.

	• Neuroticism [N]:

	- Higher N: Susceptible to stress-induced lapses or manipulation.

## Modeling and Evaluation

- Linear Regression

- XGBoost

- Voting System

- Confusion Matrix

- Classification Report

## Results

1. Contextual Analysis

	This model analyzes only cleaned_email using TF-IDF vectors. Optimal threshold for predictions: 0.29794335.

	Ensemble Model:

	•  Accuracy: 88.08%

	•  Precision (True): 89%

	•  Recall (True): 87%

	•  F1-Score (True): 0.88

2. Feature Selection

	This model focuses on structured features

	Ensemble Model:

	•  Accuracy: 56%

	•  Precision (True): 38%

	•  Recall (True): 51%

	•  F1-Score (True): 0.44

	•  Macro Average F1-Score: 0.53

•  Weighted Average F1-Score: 0.57

## Dataset

- [CERT Insider threat](https://www.kaggle.com/datasets/nitishabharathi/cert-insider-threat?resource=download)

- [Source data - Insider Threat Test Dataset](https://kilthub.cmu.edu/articles/dataset/Insider_Threat_Test_Dataset/12841247/1)
