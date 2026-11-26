# Data Science with Python: course notebooks

These are the notebooks I wrote while following the **Data Science with Python** unit (SQA, SCQF level 8) of my Diploma in Computing and IT, from January to February 2025. They are class work and practice, not finished projects.

My final project for this unit is a separate repo: [customer_segmentation](https://github.com/suwasghale/customer_segmentation) (RFM features and K-means clustering).

## `pandas/`: working with data

| Notebook | What I practised |
|---|---|
| `working-with-csv.ipynb` | Reading CSV files: separators, index and header options, selecting columns, reading from a URL |
| `data_accessing_and_cleaning.ipynb` | Assessing and cleaning messy tables (a clinical-trial example with patients, treatments and adverse reactions): writing a data summary, describing columns, listing quality problems |
| `EDA.ipynb` | Exploratory data analysis: univariate analysis of numerical and categorical columns, distribution shape and spread |
| `multiIndex_Pivot (1).ipynb` | Multi-index Series and DataFrames, stacking and unstacking, long vs wide data, merging, pivot tables |
| `visualization.ipynb` | Line, scatter and bar charts from lists and DataFrames |
| `google_playstore.ipynb`, `google_playstore_clean.ipynb` | Cleaning the Google Play Store apps dataset |
| `ecommerce-purchase.ipynb` | Exploring an e-commerce purchases dataset |

## `ml/`: machine learning with scikit-learn

| Notebook | Task | What I found |
|---|---|---|
| `churn_ml.ipynb` | Predict which bank customers leave (classification) | Logistic regression 81% accuracy, SVM 86%, random forest 86%. But only 20%, 38% and 48% of the customers who actually left were found (recall). Accuracy alone hides this, because most customers stay. |
| `heart.ipynb` | Predict heart disease (classification, 5 models) | On a test set of 61 patients: random forest 84% correct, logistic regression 80%, decision tree 75%, KNN 64%, SVM 59% |
| `insurance.ipynb` | Predict insurance charges (regression) | R²: gradient boosting 0.90, random forest 0.88, linear regression 0.81. SVR scored −0.13: it did not fit this data at all. |
| `pizza.ipynb` | Predict pizza prices (regression) | Cleaning, converting binary columns, encoding, scaling, then comparing linear regression, SVR, decision tree, random forest and gradient boosting; the encoder and model are saved with joblib |
| `feature-scaling.ipynb` | Effect of standardisation (Social Network Ads data) | Logistic regression went from 65% to 86% accuracy after scaling, KNN from 82.5% to 91%, and the decision tree stayed at 84%: trees do not need scaling |
| `mobile.ipynb` | Cleaning a mobile phone price dataset | Checking missing values and removing duplicates |
| `iris.ipynb`, `ML unsupervised.ipynb` | Clustering (unsupervised) | K-means and PCA on the iris dataset |

The files `churn_model`, `rfc_model`, `model_joblib_gbr`, `pizza_encoder` and `pizza_price_modal` are models saved from these notebooks with joblib.

## What I took from this unit

- Cleaning usually takes more time than modelling.
- Choose the metric that fits the problem: for churn, recall on the customers who leave matters more than overall accuracy.
- Scale features for distance-based and margin-based models (KNN, SVM, logistic regression), but not for trees.

## Run it

```bash
pip install pandas numpy scikit-learn matplotlib seaborn openpyxl jupyter
jupyter notebook
```

The datasets are public practice datasets, stored next to the notebooks that use them.