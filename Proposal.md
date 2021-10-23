![Banner](https://github.com/CeliaSagas/EEG-Classification/blob/ea04509c7d718a20ba113980dbb6475299d47efe/img/EEG%20Class.jpg)



# EEG-Classification
Classification of Baseline and Pre-Seizure EEG Signals for Epileptic Patients




**Question/Need:**

1. What is the question behind your analysis? What is the purpose of the model/system you plan to build?

      - Epileptic seizures are defined as a sudden change in behavior due to a temporary change in the electrical functioning of the brain ([AANS.org](https://www.aans.org/en/Patients/Neurosurgical-Conditions-and-Treatments/Epilepsy#:~:text=Epilepsy%20is%20a%20disorder%20of,impulses%20in%20an%20orderly%20pattern.)). These temporary changes in electrical functioning of the brain can be recorded and classified using EEG signals, data that is collected using non-invasive electrode placement on the scalp of an epileptic patient that records electrical functioning within the brain. Identifying preictal (pre-seizure) EEG patterns from baseline (interictal) signals is critical in order to create wearable technology that can detect the warning signs of an impending seizure and alert users to the likelihood of an oncoming seizure.




2. Who benefits from exploring this question or building this model/system?

    - Alerting epileptic patients and/or their families or guardians (depending on patient age and guardianship status) to the likelihood of oncoming seizures is critical to protecting the health and wellbeing of those who live with epilepsy. Seizures can cause temporary disturbances to motor control and  cognition, causing individuals to lose consciousness and/or physical control and possible harm to themselves or others. A warning system can help those with Epilepsy prepare for a seizure by situating themselves in a safe environment and warning others who may be able to support them.



**Data Description:**

1. What dataset(s) do you plan to use, and how will you obtain the data?

    - The dataset I will be using comes from the [American Epilepsy Society Seizure Prediction Challenge](https://www.kaggle.com/c/seizure-prediction/overview) and includes 10 minute EEG recordings labeled 'preictal' or 'interictal' for 5 canines and 2 humans with epilepsy.

2. What is an individual sample/unit of analysis in this project?

    - A single unit of analysis is a 30 second clip of EEG signals, transformed with [Discrete Multilevel Wavelet Decomposition](https://pywavelets.readthedocs.io/en/latest/ref/dwt-discrete-wavelet-transform.html), using the Daubechies 3 wavelet for 5 levels of decomposition.




3. What characteristics/features do you expect to work with?

    - From the coefficient arrays derived from the wavelet transformation, the entropy, maximum, minimum, mean, standard deviation, zero crossings, and mean crossings are derived and used as features for the classification model.


4. If modeling, what will you predict as your target?

    - The target is preictal EEG recordings.



**Tools:**

1. How do you intend to meet the tools requirement of the project?

    - I plan to use pandas, seaborn, matplotlib, scipy, defaultdict, os, time, numpy, pywavelets, and sklearn for this project.

2. Are you planning in advance to need or use additional tools beyond those required?

  - I will be using the Extra Trees Classifier from SKLearn which has been proven as a strong classification model for this data in the literature, and is not taught as part of the classification module for Metis.



**MVP Goal:**

1. What would a minimum viable product (MVP) look like for this project?

    - My MVP will be a visualization of the EEG signals at n levels using different wavelet transformations in order to show why I chose Daubechies 3 with 5 levels of decomposition.
