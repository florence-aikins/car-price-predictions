# car-price-predictions

## Overview

This project was completed as part of the **Advanced Machine Learning** module for the **MSc Data Science** programme at **Manchester Metropolitan University**.

The aim of this project is to develop machine learning models capable of accurately predicting used car prices based on vehicle characteristics. The project explores the complete machine learning workflow, including data preprocessing, feature engineering, model development, explainable AI, dimensionality reduction, polynomial regression, and clustering techniques.


## Project Objectives

- Perform exploratory data analysis (EDA)
- Clean and preprocess the dataset
- Select the most informative features
- Build and compare regression models
- Interpret model predictions using Explainable AI
- Apply dimensionality reduction techniques
- Improve model performance through feature engineering


## Dataset

The dataset contains information on used vehicles, including:

- Price (Target Variable)
- Mileage
- Year of Registration
- Standard Make
- Fuel Type
- Body Type
- Vehicle Condition
- Transmission
- Engine Size
- Additional vehicle specifications

### Data Cleaning

The following columns were removed because they contained redundant identifiers or provided little predictive value:

- Public Reference
- Standard Model
- Standard Colour
- Registration Code
- Cross Over Car and Van

Categorical variables were one-hot encoded, missing values were handled, and numerical variables were scaled where required.


## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- SHAP


## Machine Learning Pipeline

### 1. Data Preprocessing

- Data cleaning
- Missing value handling
- One-hot encoding
- Feature scaling
- Train, validation and test split


### 2. Feature Selection

- Recursive Feature Elimination (RFE)


### 3. Machine Learning Models

- Linear Regression
- Polynomial Regression
- Random Forest Regressor
- Boosted Trees


### 4. Model Interpretation

- Permutation Importance
- SHAP (SHapley Additive exPlanations)
- Partial Dependence Plots (PDP)


### 5. Dimensionality Reduction

#### Linear

- Principal Component Analysis (PCA)

#### Non-linear

- Isomap


### 6. Feature Engineering

- K-Means Clustering


## Model Evaluation

Models were evaluated using:

- Cross Validation
- Mean Cross Validation Score
- Standard Deviation
- R² Score


## Key Results

- Random Forest produced the strongest predictive performance.
- **Year of registration** was identified as the most influential predictor of vehicle price.
- **Mileage** was the second most important feature.
- SHAP values provided local explanations for individual predictions.
- Partial Dependence Plots demonstrated how mileage and vehicle age influence predicted prices.
- PCA reduced dimensionality while preserving approximately **95% of the dataset variance**.
- Isomap successfully captured non-linear relationships within the dataset.
- Polynomial regression modelled the non-linear relationship between mileage and price more effectively than standard linear regression.
- K-Means clustering generated an additional cluster feature that slightly improved model performance.


## Repository Structure

```text
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── AML_assessment.ipynb
│
├── images/
│   ├── shap_summary.png
│   ├── shap_waterfall.png
│   ├── permutation_importance.png
│   ├── partial_dependence.png
│   ├── pca_results.png
│   ├── isomap_results.png
│   ├── polynomial_regression.png
│   └── kmeans_clusters.png
│
├── README.md
├── requirements.txt
└── LICENSE
```


## How to Run

Clone the repository:

```bash
git clone https://github.com/florence-aikins/car-price-predictions.git
```

Move into the project folder:

```bash
cd car-price-predictions
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook
```

or upload the notebook to **Google Colab**.


## References

- James, G., Witten, D., Hastie, T. & Tibshirani, R. (2021). *An Introduction to Statistical Learning*. 2nd ed.
- Hastie, T., Tibshirani, R. & Friedman, J. (2009). *The Elements of Statistical Learning*. 2nd ed.
- Pedregosa, F. et al. (2011). *Scikit-learn: Machine Learning in Python*. Journal of Machine Learning Research, 12, 2825–2830.


## Author

**Florence Aikins**

MSc Data Science  
Manchester Metropolitan University

- GitHub: https://github.com/florence-aikins
- LinkedIn: https://www.linkedin.com/in/florence-aikins-aa1696387


## Acknowledgements

This project was completed as part of the **Advanced Machine Learning** coursework at **Manchester Metropolitan University** and demonstrates the application of regression modelling, feature engineering, explainable AI, dimensionality reduction, and clustering techniques to a real-world used car pricing problem.
