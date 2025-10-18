# playing-repor

# Credit-Card-Fraud-Detection

---

# Credit-Card-Fraud-Detection
## overview
This repository provides a comprehensive guide to a credit card fraud detection project based on a Kaggle dataset.
The main challenge of this project is the highly imbalanced dataset, where only 492 out of 284,807 transactions are fraudulent, representing just 0.172% of all transactions.

Another major challenge is that most features are anonymized, which makes feature engineering and interpretability more difficult.

To address the class imbalance, I experimented with various modeling techniques and sampling strategies to optimize the F1-score. After extensive testing, the best two models were scikit-learn’s MLPClassifier and Random Forest, both trained on raw, scaled data, achieving an F1-score of approximately 0.83.

Interestingly, sampling techniques did not improve performance in this project. Undersampling significantly reduced model accuracy and generalization, while oversampling provided little to no benefit.

---


## Why Are Imbalanced Datasets a Challenge in Fraud Detection?

Imbalanced datasets are very common in fraud detection problems, where fraud cases make up only a small percentage of all transactions. This creates several challenges:

- **Biased predictions:**
  If we train a model on the imbalanced data as it is, the model may learn to always predict the majority class (e.g., "not fraud"). This can     result in high accuracy but poor fraud detection, because most fraud cases will be missed.
  
- **Mismatch with real-world data:**
   Resampling techniques like oversampling or undersampling change the class distribution in the training set. For example, turning 1% fraud      cases into 35% changes the nature of the data(in real life). This can help the model learn to detect fraud better, but it no longer reflects    the true distribution seen in real-world scenarios.

- **Performance depends on the dataset:**
   While techniques like oversampling can improve results, they don’t always work well on every dataset. Their success depends on the data         characteristics and the models used.

---

## Install Requirements

To install the required dependencies, run:

```bash
pip install -r requirements.txt


---

## Repo structure 



│   .gitattributes
│   credit_fraud_data_utils.py
│   Credit_Fraud_Detection_Report.pdf
│   credit_fraud_val_utils.py
│   Fraud_Credit_Train.py
│   Fraud_detection_EDA.ipynb
│   predict.py
│   README.md
│   requirements.txt
│
├───.all_trained_models
│      
├───.best_models
│       model_scaled_MLPClassifier_default_thresh.pkl
│       model_scaled_RandomForest_default_thresh.pkl
│
├───.classification_reports_for_all_models
│      
├───.confusion_metrics_for_all_models
│       
├───.data
│    data_splits.zip
│        ├───train.csv
│        ├───val.csv
│        ├───test.csv
│        ├───trainval.csv
├───.f1_score_visualization(for_all_models_through_all_experiments)
│       f1_heatmap.png
│       f1_heatmap_best_threshold.png
│       f1_scores_cost_sensitive.png
│       f1_scores_cost_sensitive_scaled.png
│       f1_scores_oversample.png
│       f1_scores_oversample_scaled.png
│       f1_scores_over_and_under.png
│       f1_scores_over_and_under_scaled.png
│       f1_scores_raw.png
│       f1_scores_scaled.png
│       f1_scores_undersample.png
│       f1_scores_undersample_scaled.png


---







  


