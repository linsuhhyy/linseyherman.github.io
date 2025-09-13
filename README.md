# linseyherman.github.io
1. Project Title: TikTok Claims Classification Project
   
2. Overview: 
This project develops machine learning models to classify TikTok video transcripts as claims or opinions. The purpose is to help moderators prioritize user reports more efficiently by automating claim detection.

3. Approach
- Data: User-submitted text labeled as claim/opinion, with features including text length, verified status, and author ban status. N-gram features were engineered from text using CountVectorizer.
- Models:
  - Logistic Regression (baseline)
  - Random Forest (tuned with GridSearchCV)
  - XGBoost (tuned with GridSearchCV)
- Hyperparameter Tuning: Both Random Forest and XGBoost were optimized using GridSearchCV with 5-fold cross-validation.
- Evaluation Metrics: Accuracy, Precision, Recall, F1-score. Recall was prioritized to minimize false negatives (i.e., missed claims).

4. Results
- Random Forest (tuned) → Recall = 0.82, F1 = 0.80
- XGBoost (tuned) → Recall = 0.86, F1 = 0.83
- Champion Model: XGBoost was selected for its stronger recall, reducing the risk of missed claims.

5. Next Steps
- Explore advanced NLP techniques (e.g., BERT for contextual embeddings).
- Expand model to handle multilingual content.
- Test the champion model in a human-in-the-loop moderation workflow.
