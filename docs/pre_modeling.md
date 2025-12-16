Pre-modeling

In this stage, the goal is to prepare the dataset to be fed into the models, star1ng by split the data, standardiza0on, Handling imbalance and PCA.

1. spliVng the dataset

AQer merging and cleaning the data, the data was split into: 80% —> training data 20% —-> tes1ng data Using train_test _split method.

2. Standardiza0on

Before applying PCA and SMOTE numeric feature were normalized using standardScaler. This step to ensure that the PCA captures meaningful variance and SMOTE generate balance samples properly.

3. Handling Class Imbalance with SMOTE

The classes distribu1on before SMOTE were:

Not Fraud: 455,902

Fraud: 16,530

aQer SMOTE:

Not Fraud: 455,902

Fraud: 455,902

SMOTE generated 439,372 (synthe1c fraud samples), crea1ng a perfectly balanced dataset of 911,804 training rows. This will improves recall for supervised classifiers.

4. Dimensionality reduc0on (PCA)

In this sec1on, PCA was applied over the balanced data(aQer SMOTE), and for data before applying SMOTE, to evaluate our models in both outcomes.

For imbalance data: Before PCA: number of features = 414 Using cumula1ve explained variance:

PCA need to keep 78 components to capture 95% of the total variance.

aQer transforma1on:

X_train_pca → (911,804, 78)

X_test_pca → (118,108, 78)

For balanced data: Before PCA: number of features = 414 Using cumula1ve explained variance:

PCA need to keep 77 components to capture 95% of the total variance.

aQer transforma1on:

X_train_pca → (911,804, 77)

X_test_pca → (118,108, 77)

This mean that PCA successfully lowered number of feature while s1ll keeping the important paiern that help detect the frauds. When PCA was applied on balance data, the plot showed even distribu1on, and when it was applied on the original data, it was dominated by the non-fraud class, fraud point appeared in very small area.
