<!-- Add banner here -->
![Banner](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/EEG%20Class.jpg)

# EEG Classification
Identifying Pre-Seizure state in Electrical Brain Wave Activity with Wavelet Decomposition

<!-- Add buttons here -->


![GitHub last commit](https://img.shields.io/github/last-commit/Celiasagas/eeg-classification)
![GitHub issues](https://img.shields.io/github/issues/CeliaSagas/EEG-Classification)
![GitHub pull requests](https://img.shields.io/github/issues-pr/celiasagas/eeg-classification)
![Project Code](https://img.shields.io/github/languages/top/celiasagas/eeg-classification)


<!-- Describe your project in brief -->

So first: how do you predict seizures? If you've ever seen those popular videos on Tiktok of dogs alerting their owners to an oncoming seizure, then you know there must be something that those dogs are picking up on: some change they can detect with their super sensory powers.

The goal of this project is to harness the power of noticing that change: to identify the difference between imminent seizure activity (preictal) and baseline brain activity (interictal) using Electroencephalogram (EEG) signals that measure electrical activity in the brain.

The idea is if it dogs can do it, we should be able to do it too.

The reason for doing so is not just intellectual curiosity or friendly competition with our canine companions: if we can reliably predict when a seizure is imminent, we can create wearable technology that can alert a user living with epilepsy before they lose cognitive or motor control.

This would be a life changing service not only for those living with epilepsy, but for the friends, family, and loved ones of those they share their lives with. The person living with epilepsy could secure a safe space in which to be for an oncoming seizure, while parents of children with epilepsy could better prepare to support their child without getting caught off guard.

This technology isn't a cure, but it is a useful tool that would make living with epilepsy a bit more manageable.


# Demo-Preview
<!-- Add a demo for your project -->

This project uses Python packages: pandas, numpy, request, os, PyWavelets, XGBoost, sklearn, scipy, collections, glob, itertools, seaborn, and matplotlib to model and visualize salary data scraped from Glassdoor.

![Preictal Title](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/preictal_title.png)

![Preictal Wavelet](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/preictal.png)

Wavelet transformation involves decomposing a signal into a set of wavelets, or wave-like oscillations. We're basically calculating how much of a certain type of wavelet, or shape, is in that signal.

This decomposition approach generates an array for each level of wave transformation, plus an approximation coefficient, which is basically the low pass, or "coarse", representation of the original signal.


![Preictal Correlation](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/preictalCorrelation.png)


![Interictal Correlation](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/interictalCorrelation.png)

Correlation coefficients for the 1st electrode with each of the other 15 electrodes in the signal, and removed the correlation for the electrode with itself (which is 1.0).


[Click Here](https://github.com/CeliaSagas/EEG-classification) to see the full project

# Table of contents


- [Project Title](#project-title)
- [Demo-Preview](#demo-preview)
- [Table of contents](#table-of-contents)
- [Feature Engineering](#feature-engineering)
- [Models](#models)
- [Usage](#usage)
- [License](#license)
- [Footer](#footer)

# Feature-Engineering

**Feature Engineering**

The following transformations were performed on the data in order to support further analysis:

  1.	Extracted subject ID, segment type, and recording order for each file.
  2.	Selected the first 15 electrode channels for each subject.
  3.	Resampled each signal to 256 mHz to have a consistent signal frequency across all subjects.
  4.	Performed a discrete wavelet transformation to 6 levels of decomposition for one electrode channel
  5.	Computed energy per wavelet level.
  6.	Calculated the correlation coefficients for each channel in the ten-minute recording.

# Models

  **Models**

  Logistic Regression, Naïve Bayes, Random Forest, XGBoost, and Extra Trees classifiers were used before choosing Extra Trees as the model with the strongest performance in cross-validation.


  **Model Evaluation and Selection**

  The training set of 4,067 recordings was split into 80/20 train vs. holdout, all features were generated separately for training and testing respectively.

  The metric used for the American Epilepsy Competition was ROC AUC, and it was used to evaluate model efficacy.


  ![XG Boost ROC AUC](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/XGBoost_final.png)


  ![XG Boost Confusion Matrix](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/'Confusion_matrix_XGBoost_final.png)

  The training and validation phase revealed that XGBoost Classifier works best with this data set, scoring an .859 ROC score, compared to Logistic Regressions’ .627, and narrowly beating out a Random Forest score of .851.
  The final model can correctly identify the difference between baseline and pre-seizure signals with a final ROC score of .841 across all patients, with no hyper-parameter tuning. Just a simple fit.



# Usage
[(Back to top)](#table-of-contents)

American Epilepsy Society Seizure Prediction Data:[Kaggle](https://www.kaggle.com/c/seizure-prediction/overview)


# License
[(Back to top)](#table-of-contents)

This project is designed for free and open use.

[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)

# Footer
[(Back to top)](#table-of-contents)

I hope this information brings you all the fulfillment and Salary options in your job search!

<!-- Add the footer here -->

![Footer](https://github.com/CeliaSagas/EEG-Classification/blob/5b477abe64c37ab00fd32f7f16a562ca11d0cca9/img/footer.jpg)
