Credit Card Fraud Detection
Overview
This project focuses on detecting fraudulent credit card transactions using machine learning techniques. Fraud detection is a critical area in finance, where timely and accurate detection can help prevent significant financial losses. The dataset used for this analysis contains anonymized transaction information, including both fraudulent and legitimate transactions.

Dataset
The dataset consists of transactions made by European credit cardholders in September 2013.

It contains 284,807 transactions, of which 492 are frauds (approx. 0.172%).

Due to this severe class imbalance, special care is taken during model training and evaluation.

Data Preprocessing
Features were already anonymized using PCA (Principal Component Analysis), except for Time and Amount.

The Time feature was dropped as it didn’t contribute meaningfully to the model.

Amount was scaled using StandardScaler to normalize its values.

The dataset was then split into training and testing sets in a 70:30 ratio.

Class imbalance was handled using Random Oversampling and SMOTE.

Model Used: KNN, Logistic,Regression, SVC, Random Forest, and Gradient Boosting were used. Best performance was achieved by the Random Forest Classifier.

The Random Forest Classifier was selected for its robustness and ability to handle imbalanced datasets well. Various hyperparameters were tested, and class weighting was applied to manage the imbalance.

Results
Performance on Test Data:
Accuracy: ~99.96%

Precision: ~89.74%

Recall: ~85.37%

F1-Score: ~87.50%

AUC-ROC Score: ~0.97

Observations:
The model achieves very high accuracy, which is common in imbalanced datasets, but more importantly:

It maintains a high recall, meaning most fraud cases are successfully identified.

The high precision shows that most flagged transactions are actually frauds.

The ROC Curve also shows strong model performance with a large area under the curve.

Conclusion
The Random Forest model was effective in detecting fraudulent transactions with a high degree of accuracy, precision, and recall. Although some false positives and false negatives remain, the model provides a solid baseline for real-world fraud detection systems.

Future Work
Explore other ensemble methods or anomaly detection techniques.

Experiment with deep learning models like Autoencoders or LSTMs.

