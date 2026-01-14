# credit-risk-assessment-system
Credit risk prediction and explanation system using ML, SHAP, and LLM-based natural language explanations.

# 📌 Project Overview

This project demonstrates an end-to-end AI-driven credit risk assessment system.
The goal is to predict the probability of default for credit card customers
and provide clear, human-readable explanations for the risk assessment.

# The project combines: 

The system follows a structured pipeline from raw data to business-ready explanations:
   - Data Preprocessing: Handling class imbalance, log transformations for skewed financial variables, and standard scaling.
   - ML Modeling: A robust classification pipeline using StandardScaler and LogisticRegression to predict default probability.
   - Explainability (SHAP): Calculating SHAP values to identify which features (e.g., payment delays, credit limit) contributed most to the specific risk score.
   - LLM Explanation Layer: Feeding model predictions and SHAP insights into GPT-4o to generate a context-aware, professional risk assessment text for credit officers.
The system is designed to reflect real-world banking practices, where transparency, interpretability, and responsible AI usage are critical.
     
# Data Transformation Pipeline

The project implements a dedicated preprocess_pipeline using scikit-learn to ensure technical consistency and prevent data leakage:
   - StandardScaler() Integration: To handle features with different scales (e.g., LIMIT_BAL vs PAY_0), a standard scaler is used to transform data to have a mean of 0 and a standard deviation of 1.
   - Leakage Prevention: By encapsulating the scaler within a Pipeline, the transformation parameters are learned only from the training set and then applied to the test set, ensuring a statistically sound evaluation.
   - Feature Compatibility: This step is crucial for the Logistic Regression model, as it ensures all numerical inputs contribute equally to the final risk probability calculation.
     
# 📌 Key Objectives
  - Build a credit risk prediction model
  - Engineer behavior-based risk features 
  - Explain model decisions using SHAP values 
  - Generate natural language risk explanations using Generative AI
  - Ensure explanations are suitable for credit officers and customers
    
# 📌 Technologies Used
  - Python
  - Pandas & NumPy
  - Scikit-learn
  - SHAP
  - OpenAI GPT-4o (for explanation generation)
    
# 📌 Why This Project Matters
In regulated domains such as banking, models must be interpretable and auditable.
This project shows how predictive models and Generative AI can be combined
responsibly to improve transparency without compromising decision integrity.
