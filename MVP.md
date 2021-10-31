![Header](https://github.com/CeliaSagas/EEG-Classification/blob/079217439009b1b819e28221496e2287f7911dd7/img/EEG%20Class.jpg)




# EEG-Classification
Identifying Pre-Seizure EEG Signals in Epileptic Patients

Extra Trees is the most effective classification model for this data, outperforming all other models (Bayes, Logistic Regression, XGBoost, and Random Forest) on statistics derived from single channel 10 minute recordings per electrode:


![Accuracy Score per Electrode](https://github.com/CeliaSagas/Data-Coin/blob/22583032ecc7f28e60e0e58b921188df5765866f/PredvsActual.png)

**Model performance improves if single channel recording statistics are aggregated per 10 Minute recording session**

![Accuracy Score per Recording](https://github.com/CeliaSagas/Data-Coin/blob/22583032ecc7f28e60e0e58b921188df5765866f/Residual.png)
