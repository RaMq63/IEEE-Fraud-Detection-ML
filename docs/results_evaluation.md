## Results and Evalua+on

This part provides a comprehensive revision of the ML models that had been built for fraud detec1on. the Results showed strong performance and has been visualized in confusion matrices.

----

## Quanitaive Performance Metrics

All models were measured with Accuracy, Precision, Recall, F1-score, and AUC which provided an overview of the models from all perspec1ves.

Model Performance summary:

Model	accuracy	Precision(Fraud)	Recall(Fraud)	F1-Score	AUC
Random Forest	0.8797	0.18	0.71	0.29	0.8795
XGBoost(SMOTE)	0.8724	0.17	0.70	0.28	0.8753
XGBoost(scale_pos)	0.9645	0.49	0.50	0.50	0.8956
LightGBM	0.9026	0.22	0.70	0.34	0.8924
Isola0on Forest	0.8735	0.11	0.38	0.17	0.7293
Key Observa0ons

• The best-performing model was XGBoost(scale_pos) model, producing the highest precision along with high recall. • High recall values for both Random Forest and LightGBM indicated they were able to capture many fraud cases, but they have predicted high rage of False posi1ve according to Precision. • Isola1on Forest showed strong performance even though it's an unsupervised model.

----

## Visual Evaluaion

Using confusion matrices to give us the level of understanding on the correctness of each classifier diﬀeren1a1ng between fraudulent and non-fraudulent transac1ons, we created confusion matrices for all models.

The visual representa1ons allow us to beier see a clear paierns of correct and incorrect classifica1ons and evaluate the performance of the available models in detec1ng fraud, avoiding false alarms, and maintaining balanced performance.
