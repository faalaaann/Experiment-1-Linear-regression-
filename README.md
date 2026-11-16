# Experiment 1: Linear Regression

A machine learning experiment that uses multiple linear regression to estimate house prices from property features.

## Project overview

The notebook trains a scikit-learn regression pipeline on housing data using:

- Standardized numerical features with `StandardScaler`
- `LinearRegression` as the prediction model
- An 80/20 train-test split with `random_state=42`
- Evaluation with R², RMSE, and MAE
- An actual-versus-predicted price plot

## Features used

| Feature | Description |
| --- | --- |
| `sq_ft` | Property size in square feet |
| `bedrooms` | Number of bedrooms |
| `bathrooms` | Number of bathrooms |
| `walkability_score` | Walkability score from 20 to 100 |
| `house_age` | Property age in years |
| `price` | Target house price |

## Repository contents

- [`EX1 linear regresson.ipynb`](./EX1%20linear%20regresson.ipynb) — experiment notebook
- [`notebooks_housing_features.csv`](./notebooks_housing_features.csv) — housing dataset

## Requirements

Python 3.8 or newer is recommended. Install the required packages with:

```bash
pip install numpy pandas scikit-learn matplotlib joblib jupyter
```

## Running the experiment

1. Clone the repository:

   ```bash
   git clone https://github.com/faalaaann/Experiment-1-Linear-regression-.git
   cd Experiment-1-Linear-regression-
   ```

2. Start Jupyter:

   ```bash
   jupyter notebook
   ```

3. Open `EX1 linear regresson.ipynb` and run the cells in order.

The notebook expects the dataset at `data/housing_features.csv`. If using the dataset included in this repository, either create a `data` directory and move or copy `notebooks_housing_features.csv` there with the name `housing_features.csv`, or update the notebook’s `pd.read_csv(...)` path to point to the root-level CSV file.

## Results

The recorded experiment produced the following test-set metrics:

| Metric | Result |
| --- | ---: |
| R² score | 0.9133 |
| Root mean squared error | $26,071.05 |
| Mean absolute error | $20,861.84 |

The model explains approximately 91% of the variance in the test-set house prices. Results may vary if the data, random seed, or preprocessing steps are changed.

## Output

When the experiment runs successfully, it also creates an `actual_vs_predicted.png` plot showing predicted prices against actual prices, with a reference line for perfect predictions.

## License

No license has been specified for this repository.