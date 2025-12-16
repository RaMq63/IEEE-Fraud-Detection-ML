## Discussion and Conclusion

The result of the project produced eﬀec1ve insights out of tree-based machine learning models to prevent online fraudulent, The IEEE-CIS dataset presented a real-word challenges including high dimensionality, high imbalance classes, lot of missing value, and complex non-linear rela1onships, these components made fraud detec1on a diﬃcult task which required strong flexible model.

Boos1ng based models specially XGBoost, preduced the best performance along the other models when imbalance is handled well and threshold op1miza1on is applied, Random Forrest and LightGBM achieved high ROC-AUC values and strong Recall, their F1 score is low because of the precision, this indicate that while these models can detect many fraudulent transac1ons, they tend to classify a lot of ac1vi1es as fraud.

The op1mized XGBoost model, which has been used for handling imbalance class weight(scale_pos_ weight) and decision threshold tuning, achieved the best overall performance with a good F1 score and ROC-AUC close to 0.90, the F1 is an important evalua1on score in fraud detec1on domain, where minimizing missed fraud cases while s1ll controlling false alarms is cri1cal for eﬃcient decision-making in banking and e-commerce systems, from this it was cleared that evalua1on matrixes such as F1_score and ROC_AUC are more informa1ve than accuracy with high imbalances problems.

LightGBM worked eﬃciently and scaled well for large and high dimensional data, however its performance was likely lower than XGBoost in terms of imbalanced fraud detec1on.

Isola1on Forest used as unsupervised anomaly detec1on method, it’s result showed limited performance compared to supervised models, as it should, while s1ll retaining high score even when it is an unsupervised model, this clears that the preprocessing steps were eﬃcient and helped increasing the performance of the whole models.

From a par1cle view, these results show that Boos1ng models with a good imbalance handing are the best and most reasonable op1on for real-word fraud detec1on systems, the models have reached to making the correct decision by focus on high-risk transac1on.

Future work, the project can be improved by exploring hybrid ensemble methods, combining supervised and unsupervised models, use advanced feature selec1on techniques, and deep learning models could be applied such as neural network for beier data representa1on.

In conclusion this project showed that well designed machine learning pipelines especially using XGBoost with handling imbalance very eﬀec1ve can detect fraud transac1on in large and complex dataset, along with the importance of choosing the correct models, proper evalua1on method and op1mize threshold to build real fraud detec1on system.
