Run cross-validation (to make sure good results)
k-fold/rolling window cross-validation

Structured data approach:
- Linear Regression/ Logistic Regression
- Random Forest Regression/Classifier
- XGBoost/LGBM/CatBoost
- Ensembling
- hyperparameter optimization (cross-validate each)

how to start?
- check amount of non-null values: train_df.notnull().mean(axis=0).plot(kind='hist')
- remove all the data under 0.2

then plot:
- paired density in seaborn (of every 2 features) -floats
- count categorical values - int/object

reduce dimentinality:
- pca
- selection based - switch one feature off and check if the model is better (linear:correlation(x,y)-->0/low p-value) and check accuracy RMSE


we try to avoid highly correlated features in linear regression since they might bias the regression
0.98 is high correlation
0.85 is ok


sklearn.metrics.mutual_info_score

https://vimeo.com/272696002
TRAIN AI 2018 - Building the Software 2.0 Stack
