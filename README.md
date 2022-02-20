# Rakamin-Academy-Homework
Classification machine learning model to predict late delivery. 
Steps yang dilakukan : 
1. Data overview
2. EDA
3. Data PreProcessing
4. Feature Selection
5. Machine learning model
6. Hyperparameter Tuning
7. Feature importance

Hasil:
1. Data overview

2. EDA
  - Terdapat 10999 observasi
  - Semua tipe data sudah benar
  - Tidak ada null values
  - Tidak ada duplicated values

3. Data PreProcessing
  - Tidak ada missing, duplicate, redundant, ataupun invalid data
  - Pengecekan outlier menggunakan Z-score dan membuang Z-score yang lebih dari 3

4. Feature Selection
  - Chi Squared test: melihat predictive power dari categorical features.          product_importance_high yang memiliki score tinggi
  - Feature importances menggunakan RandomForestClassiﬁer
  - Feature Rankings menggunakan  Boruta dari hasil feature importances RandomForestClassiﬁer, dan diambil ﬁtur  ranking 1 dan 2 saja
  - Multicollinearity: Pearson correlation matrix untuk melihat ﬁtur yang  redundant, dibuang yang secara feature importance lebih rendah

Melalui tahapan-tahapan feature selection, berikut adalah list ﬁtur yang  terseleksi untuk digunakan pada machine learning model:
  1. cost_of_the_product
  2. discount_offered
  3. trf_weight_in_gms (np.sqrt)
  4. product_importance_high (satu-satunya categorical feature yang  memiliki chi-squared statistic tinggi

5. Machine learning model
  - XGBoostRF merupakan model yang paling unggul (dan paling viable untuk  hyperparameter tuning)

6. Hyperparameter Tuning
  - XGBRF
  - Stacking
  - Bagging

7. Feature importance
  - Feature Importance menggunakan RandomForestClassifier, dan
  - Feature Ranking menggunakan Boruta
 

