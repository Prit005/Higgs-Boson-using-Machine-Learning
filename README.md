# Higgs-Boson-using-Machine-Learning

Description: The ATLAS experiment and the CMS experiment recently claimed the discovery of the Higgs boson. The discovery was acknowledged by the 2013 Nobel prize in physics given to Francois Englert and Peter Higgs. This particle was theorized almost 50 years ago to have the role of giving mass to other elementary particles. It is the final ingredient of the Standard Model of particle physics, ruling subatomic particles and forces. The experiments are running at the Large Hadron Collider (LHC) at CERN (the European Organization for Nuclear Research), Geneva, which began operating in 2009 after about 20 years of design and construction, and which will continue operating for at least the next 10 years.

The Higgs boson has many different processes through which it can decay. When it decays, it produces other particles. In physics, a decay into specific particles is called a channel. The Higgs boson has been seen first in three distinct decay channels which are all boson pairs. One of the next important topics is to seek evidence on the decay into fermion pairs, namely tau-leptons or b-quarks, and to precisely measure their characteristics. The first evidence of the H to tau tau channel was recently reported by the ATLAS experiment, which, in the rest of this paper, will be referred to as ”the reference document”. The subject of the Challenge is to try and improve on this analysis.

**Type of Machine Learning Problem => Two Class Classification Problem. We have to predict Labels Background and Signal as per features given in datasets.** 

**Performance Metric:-** F1-Score, AUC.

## Dataset:- Download from [**here**](https://www.kaggle.com/c/higgs-boson/data).
## Dataset Details: 
training.csv - Training set of 250000 events, with an ID column, 30 feature columns, a weight column and a label column.

Some details to get started:

* all variables are floating point, except PRI_jet_num which is integer
* variables prefixed with PRI (for PRImitives) are “raw” quantities about the bunch collision as measured by the detector.
* variables prefixed with DER (for DERived) are quantities computed from the primitive features, which were selected by  the physicists of ATLAS
* it can happen that for some entries some variables are meaningless or cannot be computed; in this case, their value is −999.0, which is outside the normal range of all variables

# TASK!!
## 1. EDA and Data Pre-processing
## 2. AutoML EDA Libraries => DABL(Data Analysis Baseline Library) AutoEDA Library
## 3. Feature Engineering

## 4. Machine Learning Algorithms:-
###    * Baseline Model
           1) LogisticRegression
           2) SGDClassifier

###    * Ensemble Model with HyperParameterTuning
           1) DecisionTreeClassifier
           2) GradientBoostingClassifier
           3) LGBMClassifier

From this Baseline Model and Ensemble Models, we choose **SGDClassifier** as a **Best** Model for **Baseline Model** and **LGBMClassifier** as a **Best** Model for **Ensemble Model**.

## HyperparameterTuning Best Parameters are:
![image](https://user-images.githubusercontent.com/69208280/135707071-4c22f7a5-4fb5-4054-bb39-59b7aea5e63d.png)

## SGDClassifier results:
![image](https://user-images.githubusercontent.com/69208280/135707116-b4c2247d-cbaf-440f-851e-e487abca53fd.png)

## HyperparameterTuning Best Parameters are:
![LGBMClassifier_param](https://user-images.githubusercontent.com/69208280/135707589-86fc8938-ecb0-4d0b-b748-eae838e44126.png)

## LGBMClassifier results:
![LGBMClassifier_results](https://user-images.githubusercontent.com/69208280/135707577-c01ba5b3-e2c4-4e32-936d-a6dfd024075b.png)

## 5. ExplainableAI(SHAP Library) feature importance:
![image](https://user-images.githubusercontent.com/69208280/135707552-011cba12-1a5c-480e-9dba-b393b6630402.png)

## Actual vs Predicted Results are:
![image](https://user-images.githubusercontent.com/69208280/135707611-cbbed8fb-a2ac-4fa4-8130-2bcb65017afc.png)



