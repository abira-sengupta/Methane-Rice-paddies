# Methane (CH4) emissions from rice paddies

- The early emission peak is the first one. In this pattern,
CH4 fluxes increase after flooding for rice transplanting, as straw and/or stubble from the previous season provides the substrate for CH4 production.
CH4 emissions peak during tillering and typically decrease to near-zero levels before harvest. This group covers about 40% of all observations. This is observed in
Vietnam.
- There are two emission peaks in the second pattern. After transplanting, CH4 fluxes rise, peak during the tillering stage, and then fall. At the heading stage,
when anaerobic conditions are created by flooding and rice roots serve as substrates for the production of CH4, emissions usually show a second peak. Vietnam
is included in the 27% of total observations that fall into this category.
- There is only one late emission peak in the third pattern. In this instance, the low temperature causes low initial CH4 fluxes following transplantation. CH4
fluxes progressively increase root exudates as the growing season goes on. Due to root exudates, CH4 then peaks at the heading stage. Due to low temperatures
and pre-harvest drainage, emissions start to decline after the heading. This category includes about 24% of all observations, including those from India.
- The final pattern is distinguished by emissions that are almost continuous. After transplanting, CH4 fluxes rise but stay high due to constant flooding and high
temperatures. They then fall until draining at the end of the rice season. Approximately 8% of all observations, including India, follow this pattern.



![Example Image](image/Local-explanations.png)

# Table 1: The atmospheric composition satellite retrievals used as input into
the CAMS reanalysis EGG4 are listed below.

| Parameter      | Satellite         | Period     | Data   |
|----------------|-------------------|------------|--------|
| CH4            | Environmental satellite (Envisat)          | 2003-01-08  - 2012-04-08     | ESACCI (SRON) v7.0|
| CH4            | MetoP-A          | 2007-07-01 - 2015-06-30       | LMD v8.3    | 
| CH4            | MetoP-B          | 2013-02-01 - continue      | LMD v8.1   |
| CH4             | Greenhouse Gases Observing satellite (GoSAT) |2009-06-01 - continue | ESACCI (SRON)|

# HP importances for the six regression models
![Example Image](image/CH4-HP-Regression.png)


# HP importances for the six classification models
![Example Image](image/CH4-HP-Classification.png)

# Correlation
![Example Image](image/Correlation.png)

# Boxplot-Bangladesh
![Example Image](image/Box-plots-Bangladesh.png)

# Boxplot-India
![Example Image](image/Box-plots-India.jpg)


# SHAP-India
![Example Image](image/CH4-SHAP-I.jpg)

# SHAP-Bangladesh
![Example Image](image/CH4-SHAP-B.jpg)

# SHAP-Vietnam
![Example Image](image/CH4-SHAP-V.jpg)

# Table 2: Models and HPs for regression and classification.

| Model       | Hyperparameters (Regression)                            |  Model    | Hyperparameters (Classification)           |             
|-------------|----------------------------------------------------------|-----------|--------------------------------------------------|
| **RFR**      | criterion=‘poisson’, max_depth=2, max_samples=0.651752, min_samples_leaf=0.189317, min_samples_split=0.449878, n_estimators=23 | **RFC** | class_weight=‘balanced’, max_depth=4, max_samples=0.920910, min_samples_leaf= 0.1060876, min_samples_split=0.223397, n_estimators=43 |
| **AdaBoostR**| earning_rate=0.014532, n_estimators=110  |  **AdaBoostC** | learning_rate= 1.562151, n_estimators=48|  
| **XGBR**    | eta=0.027458, eval_metric=‘rmse’, gamma=0.771812, max_depth=5, max_leaves=5, min_child_weight=1, n_estimators=99 | **XGBC**    | eta=0.320501, eval_metric=‘auc’, gamma=0.437727, max_depth=2, max_leaves=2, min_child_weight=5, n_estimators=27 |                                                                                            |
| **LGBMR**    | feature_fraction=0.458930, learning_rate=0.082612, max_depth=1, min_data_in_leaf=2, n_estimators=18, num_leaves=28, objective=‘regression’ | **LGBMC** | class_weight=‘balanced’, feature_fraction=0.489883, learning_rate=0.614967, max_depth=5, min_data_in_leaf=82, n_estimators=81, num_leaves=34, objective=‘binary’ |
| **MLPC**  | activation=‘logistic’, alpha=0.000842, hidden_layer_sizes=14, learning_rate=‘adaptive’, learning_rate_init=0.003694, max_iter=265, momentum=0.071646, solver=‘sgd’ | **MLPR** | activation =‘tanh’,alpha=0.000544, hidden_layer_sizes=9, learning_rate=‘invscaling’, learning_rate_init=0.007015, max_iter=486, momentum=0.994338, solver=‘lbfgs’ |
| **DTR** | criterion=‘squared_error’, max_depth=4, min_samples_leaf=2, min_samples_split=12 | **DTC** | criterion=‘entropy’, max_depth=3, min_samples_leaf=9, min_samples_split=13|

# Methane emission-India, Bangladesh, Vietnam (2018, Jan)
![Example Image](image/web-1.png)





