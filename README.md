# Credit_Risk_Analysis

MODULE 17
_______________________

![image](https://user-images.githubusercontent.com/90135381/158720051-8bc1d2b3-3649-4863-bad9-8f56aaf40859.jpeg)




***RESOURCES:***

SOFTWARE: Jupyter Notebook, Pandas, Anaconda, Python, VSC

DATA: credit_risk_resampling_starter_code.ipynb, credit_risk_ensemble_starter_code.ipynb, LoanStats-2019Q1
___________________


***OVERVIEW:***
The purpose of this challenge was to assist Jill assess credit card risk with various algorithms in machine learning, in order to determine which one is the most appropriate. This was completed by preprocessing and preparing the data, performing statistical measures and ML on a dataset obtained by LendingClub and entailed the following steps:

1. load data to Jupyter Notebook
2. train and test data with imbalanced-learn and scikit-learn
3. make predictions regarding the testing
4. evaluate the model with a confusion matrix
5. calculate accuracy 
6. generate a classification report for precision, recall and F1
7. perform oversampling with Naive Random, then SMOTE ML's
8. perform undersampling
9. combo of over/under-sampling with SMOTEENN
10. compare 2 ML models with BalancedRandomForestClassifier and EasyEsembleClassifier
11. lastly, evaluate the performance of each and determine if they should be used to predict credit risk
________________

***RESULTS:***

***DELIVERABLE 1: USE RESAMPLING MODELS TO PREDICT CREDIT RISK***

For this Deliverable, both the imbalanced-learn and scikit-learn libraries were utilized to evaluate three ML models via resampling (RandomOverSampler, SMOTE, ClusterCentroids) to see which is the most appropriate for predicting credit card risk. After resampling, the count of the target classes were then scrutinized, a logistic regression classifier was trained, a balanced accuracy score was calculated, a confusion matrix was generated, as well as an imbalanced classification report for analysis. The statistical measures calculated are listed and defined as follows:

-accuracy-how close result is to the correct value (TP+TN/Total)

-precision-how reliable the positive classification is (TP/TP+FP)

-recall-the capacity of a classifier to find all the positive values (TP/TP+FN)

-F1-harmonic mean between precision and sensitivity (2(precision*sensitivity)/precision+sensitivity))

<img width="1030" alt="Del1-load data" src="https://user-images.githubusercontent.com/90135381/156424382-f51773d6-434b-435f-9c41-0f3707642dd4.png">

                              FIGURE 1: Load Data


<img width="981" alt="Del1-split into train:test" src="https://user-images.githubusercontent.com/90135381/156424398-435be2b2-ddd1-45b5-9bee-430cc9ebb3fd.png">

                         FIGURE 2: Split Into Train/Test

<img width="1440" alt="Del1-corrected naive-sklearn" src="https://user-images.githubusercontent.com/90135381/156642336-7d43ec1a-4722-4ddc-a300-0f235e843847.png">

                        
                                             
                          FIGURE 3: Naive Random OverSampling
                          
                          
<img width="1440" alt="Del1-corrected:smote" src="https://user-images.githubusercontent.com/90135381/156642387-6d314a3b-5c58-4089-a1da-ca860ad07f48.png">




                          FIGURE 4: SMOTE OverSampling
                          
                          
<img width="1440" alt="D1correction-undersampling (r=45:f1=62)" src="https://user-images.githubusercontent.com/90135381/156642419-1d29812c-7fe9-43d1-95f0-49a844966c41.png">




                          FIGURE 5: UnderSampling (ClusterCentroids)

***DELIVERABLE 2: USE THE SMOTEENN ALGORITHM TO PREDICT CREDIT RISK***

With the aforementioned libraries, this Deliverable will address the combinaion of over/under-sampling with SMOTEENN and compare the results with those obtained in Deliverable 1, in order to determine if this algorithm is better at calculating credit card risk.

<img width="1440" alt="D2-corrected(A=51 90)" src="https://user-images.githubusercontent.com/90135381/156642455-c1355678-5097-469f-a81f-2a067f231684.png">




                            FIGURE 6: Combo (Over/Under) Sampling

***DELIVERABLE 3: USE ENSEMBLE CLASSIFIERS TO PREDICT CREDIT RISK***

The last Deliverable will implement imblearn.ensemble library to train/compare the data to that of the prior Deliverables' data with BalancedRandomForestClassifier and EasyEnsembleClassifier.

<img width="958" alt="Del3-load data" src="https://user-images.githubusercontent.com/90135381/156424475-435c8302-f1b1-487a-b6db-1d155f5fac65.png">

                                   FIGURE 7: Load Data


<img width="975" alt="Del3-split into train:test" src="https://user-images.githubusercontent.com/90135381/156424488-73717040-f694-4348-9aba-e100170351fd.png">

                          FIGURE 8: Split into Train/Test


<img width="856" alt="Del3-Bal Random Forest Classifier" src="https://user-images.githubusercontent.com/90135381/156424501-7f3fa6b2-e160-4fd5-ab99-05083239d6aa.png">

                          FIGURE 9: Balanced Random Forest Classifier

<img width="1140" alt="Del3-Easy Ensemble AdaBoost Classifier" src="https://user-images.githubusercontent.com/90135381/156424508-a6a33c6c-8037-473c-ab88-7b44fa2e8a5e.png">

                           FIGURE 10: Easy Ensemble AdaBoost Classifier

***BULLETED RESULTS***

NAIVE RANDOM OVERSAMPLING:

-accuracy: 64.56=64.56%

-precision: 0.99=99%

-recall: 0.68=68%

-F1: 0.81=81%

SMOTE OVERSAMPLING:

-accuracy: 0.6234=62.34%

-precision: 0.99=99%

-recall: 0.64=64%

-F1: 0.77=77%

UNDERSAMPLING:

-accuracy: 0.6234=62.34%

-precision: 0.99=99%

-recall: 0.45=45%

-F1: 0.62=62%

SMOTEENN:

-accuracy: 0.5177=51.90%

-precision: 0.99=99%

-recall: 0.58=58%

-F1: 0.73=73%

BALANCED RANDOM FOREST CLASSIFIER:

-accuracy: 0.7877=78.77%

-precision: 0 99=99%

-recall: 0.91=91%

-F1: 0.95=95%

EASY ENSEMBLE ADABOOST CLASSIFIER:

-accuracy: 0.9254=92.54%

-precision: 0.99=99%

-recall: 0.94=94%

-F1: 0.97=97%
______________

***SUMMARY:***

***RESULTS IN TABULAR FORMAT***

<img width="599" alt="Corrected Table" src="https://user-images.githubusercontent.com/90135381/156644500-98e27238-a7bd-4d20-b3c6-2d96c87fb613.png">


Therefore; when considering the prior figures, lists and table, it can be ascertained that the Easy Ensemble Adaboost Classifier is the most appropriate machine learning model/algorithm for predicting credit card risk, as it out performed in ALL statistical categories. The accuracy score was 92.54% (the proximity of the result is close to the true value); all of the 6 ML models demonstrated 99% precision (high reliability); recall was 94% (high sensitivity); and a high F1 score 97% was observed (balance between precision and sensitivity).

The recommendation of ML model conclusively is the Easy Ensemble Adaboost Classifier.

_____________

***REFERENCES:*** BCS, Google, GitHub, StackOverflow



