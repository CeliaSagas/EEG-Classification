![Header](https://github.com/CeliaSagas/EEG-Classification/blob/079217439009b1b819e28221496e2287f7911dd7/img/EEG%20Class.jpg)




# EEG-Classification
Identifying Pre-Seizure EEG Signals in Epileptic Patients

Extra Trees is the most effective classification model for this data, outperforming all other models (Bayes, Logistic Regression, XGBoost, and Random Forest) on statistics derived from single channel 10 minute recordings per electrode:


![Accuracy Score per Electrode](https://github.com/CeliaSagas/EEG-Classification/blob/74ee58bf889ff060d0e053e69163246f713d3998/img/Accuracy_score_cv.png)



![F Score per Recording](https://github.com/CeliaSagas/EEG-Classification/blob/691c4e93ac2909a53e1485a442bf4eb784d7ac05/img/F_score_cv.png)

I also aggregated single channel recording statistics per file, and model performance improves by 3%


![Accuracy Score Aggregate](https://github.com/CeliaSagas/EEG-Classification/blob/74ee58bf889ff060d0e053e69163246f713d3998/img/Accuracy_score_cv_long.png)
