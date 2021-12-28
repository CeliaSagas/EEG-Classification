<!-- Add banner here -->
![Banner](https://github.com/CeliaSagas/Data-Coin/blob/e016fd55fecf69dd8a8a5694ae838f494b5f0517/img/datacoinheader.png)

# EEG Classification

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

![Preictal Title](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/salary_hist.png)

![Preictal Wavelet](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/salary_hist.png)

Wavelet transformation involves decomposing a signal into a set of wavelets, or wave-like oscillations. We're basically calculating how much of a certain type of wavelet, or shape, is in that signal.

This decomposition approach generates an array for each level of wave transformation, plus an approximation coefficient, which is basically the low pass, or "coarse", representation of the original signal.


![Preictal Correlation](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/revenue_bar.png)


![Interictal Correlation](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/location_bar.png)

Correlation coefficients for the 1st electrode with each of the other 15 electrodes in the signal, and removed the correlation for the electrode with itself (which is 1.0).


[Click Here](https://github.com/CeliaSagas/Data-Coin) to see the full project

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
  3.	Resampled each signal to 399 MHz to have a consistent signal frequency across all subjects.
  4.	Performed a discrete wavelet transformation to 5 levels of decomposition for each single electrode channel
  5.	Computed the zero crossings, mean crossings, maximum, minimum, mean, standard deviation, and skew for each single channel.
  6.	Computed the correlation coefficients for each channel in the ten-minute recording.

# Models

  **Models**

  Logistic Regression, Naïve Bayes, Random Forest, XGBoost, and Extra Trees classifiers were used before choosing Extra Trees as the model with the strongest performance in cross-validation.


  **Model Evaluation and Selection**

  The training set of 4,067 recordings was split into 80/20 train vs. holdout, all features were generated separately for training and testing respectively, and all scores were reported below were calculated with 5-fold cross validation on the training portion only.

  The metric used for the American Epilepsy Competition was accuracy, however, f1 was also taken into consideration as a more useful means of identifying the strength of the model in identifying a minority class.

  Finally, the training and holdout data were combined to train the model for the Kaggle competition data, consisting of 3,935 recordings, for which a key has now been released. The model was tested on the competition set and the scores are also reported below.

  ![XG Boost ROC AUC](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/revenue_bar.png)


  ![XG Boost Confusion Matrix](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/location_bar.png)


# Usage
[(Back to top)](#table-of-contents)

American Epilepsy Society Seizure Prediction Data:

[American Epilepsy Data](https://www.kaggle.com/c/seizure-prediction/overview)


# License
[(Back to top)](#table-of-contents)

This project is designed for free and open use.

[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)

# Footer
[(Back to top)](#table-of-contents)

I hope this information brings you all the fulfillment and Salary options in your job search!

<!-- Add the footer here -->

![Footer](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/datacoinfooter.png)
