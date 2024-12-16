
# Insider Cyber Threat Detection using CERT Data



Overview

This project focuses on detecting insider cybersecurity threats using data from the Computer Emergency Response Team (CERT). By leveraging Natural Language Processing (NLP) and machine learning techniques, the project identifies behavioral and contextual anomalies to flag potential insider threats. The study incorporates insights from the OCEAN (Big Five personality traits) model to theorize psychological influences on insider risk.
The project evaluates two primary approaches:
1.	Contextual Analysis: Focused on analyzing textual data (cleaned_email) using NLP techniques.
2.	Feature Selection: Focused on structured numerical and categorical features to analyze behavioral and contextual patterns.
The goal is to develop robust detection models that balance recall (to minimize missed threats) and precision (to reduce false positives) for practical implementation.

## Methodology

1. Data Preprocessing
•	Text Preprocessing (for Contextual Analysis):

    •	Emails were tokenized and lemmatized.
    •	Stop words were removed, and TF-IDF vectors were generated for cleaned_email.
•	Structured Data Preprocessing (for Feature Selection)
    
    •	Categorical variables were encoded, and numerical features were scaled.
    •	The following structured features were selected:
        •	num_recipients, hour, day_of_week, attachments, size, sentiment_score, keyword_threat, and anomaly.


2. OCEAN Model Hypothesis
•	The Big Five Personality Traits (OCEAN) were used to theorize psychological influences on insider risks:
•	Conscientiousness (C):
    o	Lower C: Higher accidental risks due to poor security hygiene.
    o	Higher C: Predictable behavior patterns, which can be exploited.
•	Openness (O):
    o	Higher O: More experimentation with unauthorized systems/tools.
    o	Lower O: Resistance to new security measures.
•	Agreeableness (A):
    o	Lower A: Independent, potentially policy-breaking actions.
    o	Higher A: Vulnerable to social engineering.
•	Extraversion (E):
    o	Higher E: Oversharing of information.
    o	Lower E: Reduced detection due to less interaction.
•	Neuroticism (N):
    o	High N: Susceptible to stress-induced lapses or manipulation.


## Modeling and Evaluation

- Linear Regression
- XGBoost
- Voting System
- Confusion Matrix
- Classification Report


## Dataset

- [CERT Insider threat](https://www.kaggle.com/datasets/nitishabharathi/cert-insider-threat?resource=download)
- [Source data - Insider Threat Test Dataset](https://kilthub.cmu.edu/articles/dataset/Insider_Threat_Test_Dataset/12841247/1)


