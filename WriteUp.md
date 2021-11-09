![Header](https://github.com/CeliaSagas/EEG-Classification/blob/0637ec5a882a1b6dd030057aa6e9726643d43a90/img/EEG%20Class.jpg)




# EEG - Classification
Predicting Seizures from Electrical Brain Wave Activity

**Abstract**

The goal of this project is to classify preictal (pre-seizure) EEG signals and interictal (between seizure, or baseline) EEG signals from 10-minute EEG recordings collected from seven patients living with epilepsy, including 5 dogs and 2 humans. The accurate classification of preictal EEG signals is vital to the creation of wearable technology that can warn those living with epilepsy of an impending seizure, and by doing so, help them avoid personal harm due to uncontrollable actions.

**Design**

This project originated from the American Epilepsy Society Seizure Prediction Challenge. The data is provided by the National Institutes of Health (NINDS), the Epilepsy Foundation, and the American Epilepsy Society. The challenge is a two-class classification of EEG signals into either preictal (pre-seizure) or interictal (baseline) categories, with the purpose being the creation of technology that can alert those living with epilepsy of impending seizures.


**Data**

This project originated from the American Epilepsy Society Seizure Prediction Challenge. The data is provided by the National Institutes of Health (NINDS), the Epilepsy Foundation, and the American Epilepsy Society. The challenge is a two-class classification of EEG signals into either preictal (pre-seizure) or interictal (baseline) categories, with the purpose being the creation of technology that can alert those living with epilepsy of impending seizures.


**Algorithms**

**Feature Engineering**

The following transformations were performed on the data in order to support further analysis:

    1.	Extracted subject ID, segment type, and recording order for each file.
    2.	Selected the first 15 electrode channels for each subject.
    3.	Resampled each signal to 399 MHz to have a consistent signal frequency across all subjects.
    4.	Performed a discrete wavelet transformation to 5 levels of decomposition for each single electrode channel
    5.	Computed the zero crossings, mean crossings, maximum, minimum, mean, standard deviation, and skew for each single channel.
    6.	Computed the correlation coefficients for each channel in the ten-minute recording.



**Models**

Logistic Regression, Naïve Bayes, Random Forest, XGBoost, and Extra Trees classifiers were used before choosing Extra Trees as the model with the strongest performance in cross-validation.

**Model Evaluation and Selection**

The training set of 4,067 recordings was split into 80/20 train vs. holdout, all features were generated separately for training and testing respectively, and all scores were reported below were calculated with 5-fold cross validation on the training portion only.

The metric used for the American Epilepsy Competition was accuracy, however, f1 was also taken into consideration as a more useful means of identifying the strength of the model in identifying a minority class.

Finally, the training and holdout data were combined to train the model for the Kaggle competition data, consisting of 3,935 recordings, for which a key has now been released. The model was tested on the competition set and the scores are also reported below.

**Final Extra Trees 5-fold CV Scores: 928 Features**

    -	Accuracy: 94.65%
    -	Precision: 94.0%
    -	Recall: 30.7%
    -	F1: 45.9%

**Holdout**

    -	Accuracy: 94.84%
    -	Precision: 93.75%
    -	Recall: 26.8%
    -	F1: 41.6%

**Competition Test Data**

    -	Accuracy: 89.6%
    -	Precision: 10.9%
    -	Recall: 8.7%
    -	F1: 9.7%


**Tools**

  -	Pandas, Numpy, Scipy, Sklearn, and Glob for data analysis
  -	Matplotlib Seaborn for data visualization


**Communication**

Data Visualization and write-up will be shared on Medium, Celiasagastume.com, and in class through PowerPoint presentation.
