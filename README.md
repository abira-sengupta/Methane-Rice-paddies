# Methane (CH4) emissions from rice paddies

- The early emission peak is the first one. In this pattern,
CH4 fluxes increase after flooding for rice transplant-
ing, as straw and/or stubble from the previous sea-
son provides the substrate for CH4 production. CH4
emissions peak during tillering and typically decrease
to near-zero levels before harvest. This group covers
about 40% of all observations. This is observed in
Vietnam.
- There are two emission peaks in the second pattern.
After transplanting, CH4 fluxes rise, peak during the
tillering stage, and then fall. At the heading stage,
when anaerobic conditions are created by flooding and
rice roots serve as substrates for the production of
CH4, emissions usually show a second peak. Vietnam
is included in the 27% of total observations that fall
into this category.
- There is only one late emission peak in the third pat-
tern. In this instance, the low temperature causes
low initial CH4 fluxes following transplantation. CH4
fluxes progressively increase root exudates as the
growing season goes on. Due to root exudates, CH4
then peaks at the heading stage. Due to low tempera-
tures and pre-harvest drainage, emissions start to de-
cline after the heading. This category includes about
24% of all observations, including those from India.
- The final pattern is distinguished by emissions that are
almost continuous. After transplanting, CH4 fluxes
rise but stay high due to constant flooding and high
temperatures. They then fall until draining at the end
of the rice season. Approximately 8% of all observa-
tions, including India, follow this pattern.



![Example Image](image/Local-explanations.png)

# Table 1: The atmospheric composition satellite retrievals used as input into
the CAMS reanalysis EGG4 are listed below.

| Parameter      | Satellite         | Period     | Data   |
|----------------|-------------------|------------|--------|
| CH4            | Environmental satellite (Envisat)          | 2003-01-08  - 2012-04-08     | ESACCI (SRON) v7.0|
| CH4            | MetoP-A          | 2007-07-01 - 2015-06-30       | LMD v8.3    | 
| CH4            | MetoP-B          | 2013-02-01 - continue      | LMD v8.1   |
|CH4             | Greenhouse Gases Observing satellite (GoSAT) |2009-06-01 - continue | ESACCI (SRON)|

# HP importances for the six regression models
![Example Image](image/CH4-HP-Regression.png)


# HP importances for the six classification models
![Example Image](image/CH4-HP-Classification.png)


| Model     | Hyperparameter           | Value         | Type         |
|-----------|--------------------------|---------------|--------------|
| RF        | class_weight             | balanced      | classification|
| RF        | max_depth                | 4             | classification|
| RF        | max_samples              | 0.920910      | classification|
| RF        | min_samples_leaf         | 0.1060876     | classification|
| RF        | min_samples_split        | 0.223397      | classification|
| RF        | n_estimators             | 43            | classification|
| RF        | criterion                | poisson       | classification|
| RF        | max_depth                | 2             | classification|
| RF        | max_samples              | 0.651752      | classification|
| RF        | min_samples_leaf         | 0.189317      | classification|
| RF        | min_samples_split        | 0.449878      | classification|
| RF        | n_estimators             | 23            | classification|
| AdaBoost  | learning_rate            | 1.562151      | classification|
| AdaBoost  | n_estimators             | 48            | classification|
| AdaBoost  | learning_rate            | 0.014532      | classification|
| AdaBoost  | n_estimators             | 110           | classification|
| XGBC      | eta                      | 0.320501      | classification|
| XGBC      | eval_metric              | auc           | classification|
| XGBC      | gamma                    | 0.437727      | classification|
| XGBC      | max_depth                | 2             | classification|
| XGBC      | max_leaves               | 2             | classification|
| XGBC      | min_child_weight         | 5             | classification|
| XGBC      | n_estimators             | 27            | classification|
| XGBR      | eta                      | 0.027458      | regression   |
| XGBR      | eval_metric              | rmse          | regression   |
| XGBR      | gamma                    | 0.771812      | regression   |
| XGBR      | max_depth                | 5             | regression   |
| XGBR      | max_leaves               | 5             | regression   |
| XGBR      | min_child_weight         | 1             | regression   |
| XGBR      | n_estimators             | 99            | regression   |
| LGBM      | class_weight             | balanced      | classification|
| LGBM      | feature_fraction         | 0.489883      | classification|
| LGBM      | learning_rate            | 0.614967      | classification|
| LGBM      | max_depth                | 5             | classification|
| LGBM      | min_data_in_leaf         | 82            | classification|
| LGBM      | n_estimators             | 81            | classification|
| LGBM      | num_leaves               | 34            | classification|
| LGBM      | objective                | binary        | classification|
| LGBM      | feature_fraction         | 0.458930      | classification|
| LGBM      | learning_rate            | 0.082612      | classification|
| LGBM      | max_depth                | 1             | classification|
| LGBM      | min_data_in_leaf         | 2             | classification|
| LGBM      | n_estimators             | 18            | classification|
| LGBM      | num_leaves               | 28            | classification|
| LGBM      | objective                | regression    | regression   |
| MLP       | activation               | tanh          | regression   |
| MLP       | alpha                    | 0.000544      | regression   |
| MLP       | hidden_layer_sizes       | 9             | regression   |
| MLP       | learning_rate            | invscaling    | regression   |
| MLP       | learning_rate_init       | 0.007015      | regression   |
| MLP       | max_iter                 | 486           | regression   |
| MLP       | momentum                 | 0.994338      | regression   |
| MLP       | solver                   | lbfgs         | regression   |
| MLP       | activation               | logistic      | classification|
| MLP       | alpha                    | 0.000842      | classification|
| MLP       | hidden_layer_sizes       | 14            | classification|
| MLP       | learning_rate            | adaptive      | classification|
| MLP       | learning_rate_init       | 0.003694      | classification|
| MLP       | max_iter                 | 265           | classification|
| MLP       | momentum                 | 0.071646      | classification|
| MLP       | solver                   | sgd           | classification|
