# Automotive Loan Default Prediction: local machine hyperparameters tuning attempt

In this part of my university project, I added histograms for all features and discovered that not only was the target variable (binary) unbalanced, but almost every selected feature was as well. Therefore, applying SMOTE to the sample was the correct decision.

Additionally, I attempted to fine-tune the Logistic Regression and XGBoost algorithms. I started with Grid Search, then moved on to Random Search, and when both of these methods exceeded my machine's capacities, I tried Optuna. However, despite multiple attempts to adapt the code, the evaluation metrics for both Logistic Regression and XGBoost were not better than the default hyperparameters, and in fact, they were worse. I am unsure of the reason for this. It could be that the initial hyperparameters were already optimal, or I may need to learn more about the amazing tool Optuna and manually adjust the settings.

In the next session, I plan to focus on cloud computing for the project. I will use Azure ML to run all three algorithms and employ GridSearch and Optuna for hyperparameter optimization and compare the results.
