# Module 8 worked examples

These files are migration copies of the wine classification and used-car price
regression examples from Daniel Bauer's
[Predictive Modeling and Machine Learning materials](https://github.com/danielbauer1979/MSDIA_PredictiveModelingAndMachineLearning).
The original filenames began with `GB886_VIII_4_` and `GB886_VIII_5_`.

For GB656 in 2026, students submit their analysis, report PDF, and code through
Canvas. **No prediction submission to Kaggle is required.** The wine and car
examples demonstrate modeling workflows; the final-project assignment in Canvas
specifies the approved project choices and deliverables.

## Migration status

This initial migration changes the notebook/Colab links and input data locations
to this repository. CSV contents, modeling code, explanations, and saved notebook
outputs are otherwise preserved. Substantive notebook revision is pending, so
the inherited competition and submission wording does not state the 2026 course
requirements.

Known issues awaiting revision include the wine example's false-positive and
false-negative rate formulas, threshold selection using test results, and
preprocessing before cross-validation folds. The car example needs a labeled
held-out evaluation, training-only preprocessing, correction of a stray undefined
variable, and removal of a prediction column inadvertently reused as a feature.
Saved outputs should be regenerated after those corrections.

## Files

- [Wine notebook](GB656_08_WineExample.ipynb) and
  [wine data](GB656_08_winequality.csv).
- [Car notebook](GB656_08_CarExample.ipynb) and labeled car data in
  [part 1](GB656_08_train_1.csv) and [part 2](GB656_08_train_2.csv).
- The [unlabeled car inference data](GB656_08_test.csv) and
  [sample competition submission](GB656_08_sample_submission.csv) are retained
  because the inherited car notebook reads them. They are not Canvas submission
  requirements. Unlabeled inference data cannot supply final test metrics.

The wine data originate from the
[UCI Wine Quality dataset](https://archive.ics.uci.edu/dataset/186/wine%2Bquality).
The supplied red-wine target was recoded to 1 for quality scores of at least 7 and
0 otherwise. Original reference: Cortez, Cerdeira, Almeida, Matos, and Reis (2009),
*Modeling wine preferences by data mining from physicochemical properties*,
[Decision Support Systems](https://doi.org/10.1016/j.dss.2009.05.016).

The car data originate from Kaggle's
[Regression of Used Car Prices competition](https://www.kaggle.com/competitions/playground-series-s4e9).
The two labeled CSV parts are concatenated by the notebook.
