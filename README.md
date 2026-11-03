# Titanic Survival Prediction Analysis

Exploratory data analysis of the Titanic passenger dataset to find which factors are related to survival,
followed by chi-square tests of independence and a logistic regression model that predicts whether a passenger survived.

The full analysis is in [`Survival Prediction Analysis.ipynb`](Survival%20Prediction%20Analysis.ipynb).

## Contents

1. **Data loading and overview**: structure and summary statistics of the dataset.
2. **Exploratory analysis**: survival by passenger class, sex, age, port of embarkation, siblings/spouses, parents/children and ticket fare.
3. **Chi-square tests**: statistical test of the relationship between each variable and survival.
4. **Logistic regression**: a model trained on these features, evaluated with accuracy, a confusion matrix and a classification report.

## Key findings

- **Sex** and **passenger class** are the strongest predictors: about 74% of women survived compared with 19% of men,
  and 63% of 1st class passengers survived compared with 24% in 3rd class.
- Port of embarkation, ticket fare and family aboard are also significantly related to survival (p < 0.05).
- Age on its own is not significant in the chi-square test (p ≈ 0.10).
- The logistic regression model reaches about **81% accuracy** on the test set.

## Dataset

The data is loaded directly from
[datasciencedojo/datasets](https://github.com/datasciencedojo/datasets/blob/master/titanic.csv) (891 passengers),
so no download is needed. An internet connection is required to run the notebook.

## Running it locally

Requires Python 3.10+.

```bash
git clone https://github.com/alvarogope/titanic-survival-analysis.git
cd titanic-survival-analysis

python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
```

Then open the notebook in Cursor or VS Code and select the `.venv` interpreter as the kernel,
or run `pip install notebook` and `jupyter notebook` to use it in the browser.

## Tech stack

pandas · NumPy · Matplotlib · seaborn · SciPy · scikit-learn
