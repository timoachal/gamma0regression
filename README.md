# Gamma Regression Model

This repository demonstrates the use of a Gamma regression model to analyze insurance claim amounts using Python. The main analysis is performed in a Jupyter notebook, focusing on the Australian "carclaims" dataset.

## Overview

The model fits a Gamma generalized linear model (GLM) with a log link function to insurance claims data, predicting claim amounts (`claimcst0`) greater than zero. The predictors include vehicle value, vehicle age, policyholder gender, geographical area, and age category.

## Features

- **Data Filtering:** Only claims with a positive claim amount are analyzed.
- **Categorical Encoding:** Categorical variables (gender, area, age category) are properly encoded.
- **Model Formula:**  
  ```
  claimcst0 ~ veh_value + veh_age + C(gender) + C(area) + C(agecat)
  ```
- **Model Fitting:** The model is fitted using `statsmodels`' GLM with the Gamma family and log link.
- **Model Interpretation:** Statistical summaries and interpretations of coefficients are provided in the notebook.

## Key Findings

- **Significant Predictors:**
  - **Gender:** Male policyholders are associated with higher claim costs.
  - **Area:** Policyholders in Area F have significantly higher expected claim amounts.
  - **Age Category:** Older age categories (2-6) are associated with lower claim costs compared to the youngest category.
- **Vehicle value and age:** Vehicle value is not a significant predictor; vehicle age has a weak positive association.
- **Model Performance:** The model explains some variability, but much remains unexplained, suggesting the need for further model refinement or additional predictors.

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/timoachal/gamma0regression.git
   cd gamma0regression
   ```

2. Install requirements (make sure you have Python 3.9+ and Jupyter Notebook):
   ```bash
   pip install pandas statsmodels matplotlib seaborn bambi jupyter
   ```

3. Run the Jupyter notebook:
   ```bash
   jupyter notebook gamma_jupyter/gamma\ regression.ipynb
   ```

## Requirements

- pandas
- statsmodels
- matplotlib
- seaborn
- bambi
- jupyter

## Project Structure

```
gamma0regression/
└── gamma_jupyter/
    └── gamma regression.ipynb
```

## License

No license specified.

## Author

[timoachal](https://github.com/timoachal)

---

*This repository provides a foundation for using Gamma regression in actuarial science and insurance analytics. Contributions and suggestions are welcome!*
