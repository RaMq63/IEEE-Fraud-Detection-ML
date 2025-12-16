4.7 Supervised Learning Models

Three supervised learning models were implemented: • Random Forest • XGBoost • LightGBM (best-performing)

All models were trained using the PCA-transformed balanced dataset.

1. Random Forest

The hyperparameters: • n_es1mators=600, use to improve stability and reduce variance. • max_depth=12, help to generalize beier, and not grow too complex. • min_samples_split=5, prevents the model split on very small. • min_samples_leaf=2, for reduces noise. • random_state=42, to ensure the results repeatability. • n_jobs= -1, speed up training when use many trees.

2. XGBoost Models
1. XGBoost Classifier (with SMOTE)

The hyperparameters:

n_es1mators=300, good number of trees to catch complex paierns.

learning_rate=0.05, this small to improve generaliza1on and reduce overfikng.

max_depth=6, to prevent overfikng and allows for nonlinear rela1onships.

subsample=0.8, to reduce variance and improve generaliza1on.

colsample_bytree=0.8, To prevent over-reliance on any single feature.

random_state=42, to ensures reproducibility.

eval_metric='logloss', evaluates model probability predic1ons, and good for binary classifica1on.

2. XGBoost Classifier (without SMOTE, using scale_pos_weight)

The hyperparameters:

n_es1mators=300, to catch complex paierns without requiring too much training 1me.

learning_rate=0.05, this small to ensures smooth learning and reduces overfikng.

max_depth=6, Reduces tree complexity and balances bias and variance

subsample=0.8 and colsample_bytree=0.8, Random samples are taken from 80% of the rows and features for tree to reduce overfikng.

random_state=42, to ensures reproducibility.

eval_metric='logloss', evaluates model probability predic1ons, and good for binary classifica1on.

scale_pos_weight=scale_pos_weight, use to improved minority class recogni1on without crea1ng synthe1c data. (The threshold tuning allows control over the balance between accuracy and recall to improve the F1 score for the minority class. This approach preserves the original data distribu1on while eﬀec1vely addressing the imbalance.)

3. LightGBM

The hyperparameters:

n_es1mators=1000, allow the model to learn paierns over many boos1ng rounds.

learning_rate=0.05, ensures that updates are incremental and help prevent overfikng.

num_leaves=31, to reduce the complexity of the tree and ensure good generaliza1on.

class_weight='balanced', used to increase automa1cally the sample weight of the minority class during training.

random_state=42, to ensures reproducibility.

n_jobs=-1, allow model to use the full power of the CPU for faster training.

4.8 Unsupervised Learning
1. Isola0on Forest

Isola1on Forest was used to detect fraud without using labels. The hyperparameters: • n_es1mators=300, provide enough isola1on trees to create stable degrees of skew. • contamina1on='auto', allow the model expected rate of data outliers to be es1mated. • max_samples='auto', the algorithm is allowed to select op1mal number of samples. • random_state=42, to ensures consistent and reproducible result. • n_jobs=-1, use all available CPU to speed up training.
