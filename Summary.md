
Make sure to work in git and have a project using the structure. Project Structure:
		/<competition_name>
		/notebooks
		/data
		/README.md
		/setup.py

Work using git branches, each member uses its own branch and merges to master are made once in a while.

It’s better to keep track of which code version (specific commit) + dataset was used to make a specific prediction. Otherwise, you get tons of predictions (csv files) that you can’t really keep track of its origin.

Evaluate model technics: Rolling / spanding cross validation. This can be used to evaluate model before submitting a prediction.

Models for structural data:
LinearRegression / LogisticRegression
RandomForestRegressor / Classifier 
XGBOOST / LGMB / Catboost
Ensemble

It’s better to start with feature engineering, and only after that start with hyper parameters tuning.

Ensembling: average models. Each team member can train a model, and then you average these predictions. It’s not really used in production, but can be used for kaggle. Y = a0 y01 + … + an yn

To do that, you have to split your data to 3 / 4 parts (google it)

Workflow: explore features, work with categorical values (enums: male/female, etc.),  

Data exploration:
Drop from the dataset features (not samples) that 90% or above are nulls, they’re probability not very meaningful
Draw correlations for floats features, use this: https://seaborn.pydata.org/examples/pair_grid_with_kde.html
If you think it's not linear, check mutual information (it’s a form of correlation, google it)

Glib says - watch this one:
https://vimeo.com/272696002

Feature selection: you can examine if a feature useful or not, by training without it and see if it ok. Do several runs for it to be statistically valid. Confidence internal - google it.

Magic line train_df.notnull().sum(axis=0)
