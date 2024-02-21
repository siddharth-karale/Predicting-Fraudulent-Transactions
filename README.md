# Predicting-Fraudulent-Transactions

Develop a model for predicting fraudulent transactions for a financial company.
This case requires trainees to develop a model for predicting fraudulent transactions for a 
financial company and use insights from the model to develop an actionable plan. Data for the 
case is available in CSV format having 6362620 rows and 10 columns.

## Technologies Used:

  * Python
  * Pandas
  * NumPy
  * Seaborn
  * Matpplotlib
  * Scikit-learn
    
## Data: 

* step - maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation).
* type - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.
* amount - amount of the transaction in local currency.
* nameOrig - customer who started the transaction
* oldbalanceOrg - initial balance before the transaction
* newbalanceOrig - new balance after the transaction
* nameDest - customer who is the recipient of the transaction
* oldbalanceDest - initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants).
* newbalanceDest - new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants).
* isFraud - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system.
* isFlaggedFraud - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200.000 in a single transaction.


## Methodology: 

* We have data here that is highly imbalanced our approache should be to deal with the imbalanced data.
* Decision trees perform well in unbalanced data because they naturally split data based on features relevant to both classes. Such algorithms not only allow for constructing a model that can cope with the missing values in our data, but they naturally allow for speedup via parallel-processing.
* Ensemble methods like Random Forests further improve this by combining multiple decision trees.
* XGBoost's tree-based structure inherently focuses on informative features for all classes, making it inherently more robust than algorithms sensitive to majority classes.
* A better approach might be to oversample the minority class, say by the synthetic minority oversampling technique (SMOTE) contained in the 'imblearn' library. Combining resampling techniques like SMOTE with robust algorithms can yield superior results.
* Due to there reason's we have trained our model on XGBoost, Decision Tree and Random Forest algorithms. Further to oversample the data we have used synthetic minority oversampling technique (SMOTE) and trained the model again with oversampled data.


## Project Structure:

The project is organized as follows:

* Data: This directory contains the Gold Price dataset in CSV format.
* Notebooks: This directory contains Jupyter notebooks with the Python code used for data analysis and visualization.
* README.md: This file provides an overview of the project, objectives, and instructions for running the code.
* LICENSE: This project is under the MIT License.

## Contributing: 

Contributions to this project are welcome! If you have ideas for improving the analysis, adding new features, or fixing issues, please open an issue or submit a pull request.

## License: 

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments:

The Fraud dataset used in this project is publicly available and can be found on various sources, including Kaggle.
Thank you for your interest in the Fraudulent Transaction Prediction project! We hope you find the insights and code provided valuable for your data analysis endeavors.
