# Module 8 worked examples

These wine classification and used-car price regression examples were adapted
from Daniel Bauer's [Predictive Modeling and Machine Learning materials](https://github.com/danielbauer1979/MSDIA_PredictiveModelingAndMachineLearning).

For GB656 in 2026, submit your report PDF and reproducible code through Canvas.
The final-project assignment lists the approved project choices and deliverables.

## Wine quality classification

[Open the wine notebook in Colab](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/module8/GB656_08_WineExample.ipynb)
or view the [notebook](GB656_08_WineExample.ipynb) and [data](GB656_08_winequality.csv).

The notebook removes exact duplicate rows and reserves 25% of the remaining
wines for final evaluation. It compares unpenalized logistic regression with
L1-penalized logistic regression. Five-fold cross-validation on the development
data tunes the L1 penalty, with scaling fitted inside each fold. Both finalized
models use the same held-out wines for the ROC curves, AUC, and confusion
matrices. Both confusion matrices use a 0.50 cutoff.

The red-wine data originate from the [UCI Wine Quality dataset](https://archive.ics.uci.edu/dataset/186/wine%2Bquality).
The supplied target is 1 for an original quality score of at least 7 and 0
otherwise. Original reference: Cortez, Cerdeira, Almeida, Matos, and Reis
(2009), *Modeling wine preferences by data mining from physicochemical
properties*, [Decision Support Systems](https://doi.org/10.1016/j.dss.2009.05.016).

## Used-car price regression

[Open the car notebook in Colab](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/module8/GB656_08_CarExample.ipynb)
or view the [notebook](GB656_08_CarExample.ipynb) and labeled data in
[part 1](GB656_08_train_1.csv) and [part 2](GB656_08_train_2.csv).

The notebook combines the two labeled files and reserves 25% of the listings
for final evaluation. It fits preprocessing on the development rows and uses
the same transformations for the held-out rows. It compares ordinary least
squares fitted on all development rows with a second fit that excludes
development prices above the 99.9th percentile. Both models are evaluated with
root mean squared error on the same complete held-out set.

The data originate from Kaggle's [Regression of Used Car Prices competition](https://www.kaggle.com/competitions/playground-series-s4e9).
The [unlabeled inference file](GB656_08_test.csv) and
[sample submission file](GB656_08_sample_submission.csv) are retained as
historical competition assets. The notebook uses only the two labeled files.
