# Credit Card Fraud Detection

This project aims to detect fraudulent credit card transactions using machine learning techniques. It addresses the challenge of highly imbalanced data, where legitimate transactions significantly outnumber fraudulent ones.

## Dataset

[Link to the Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
### Dataset Overview

The dataset used in this project contains credit card transactions from September 2013, made by European cardholders. Key characteristics include:

- **Time span**: 2 days
- **Total transactions**: 284,807
- **Fraudulent transactions**: 492 (0.172% of total)

#### Data Imbalance

The dataset is highly skewed, with fraudulent transactions (positive class) accounting for only 0.172% of all transactions.

#### Features

The dataset consists of numerical input variables, most of which are the result of PCA (Principal Component Analysis) transformation:

1. **PCA-transformed features**: V1, V2, ..., V28
2. **Non-transformed features**:
   - **Time**: Seconds elapsed between each transaction and the first transaction
   - **Amount**: Transaction amount (can be used for example-dependent cost-sensitive learning)
3. **Target variable**:
   - **Class**: 1 for fraudulent transactions, 0 for legitimate ones

#### Confidentiality

Due to privacy concerns, the original features and additional background information are not available. The PCA transformation was applied to maintain confidentiality of the cardholders.

## Requirements

To run this project, you need the following libraries:

- numpy
- pandas
- scikit-learn
- imblearn
- xgboost
- matplotlib

Install these libraries using pip:
pip install numpy pandas scikit-learn imblearn xgboost matplotlib

## Usage

1. Clone this repository: 
```bash
 git clone https://github.com/priyanshuanandd/AspireNex.git
```
3. Navigate to the project directory:
```bash
cd AspireNex
```
5. Run the Jupyter Notebook:
```bash
jupyter notebook Credit_Card_Fraud_Detection.ipynb
```

## Methodology

The project follows these key steps:

1. **Data Preprocessing:** 
- Handle missing values
- Normalize transaction amounts

2. **Addressing Class Imbalance:**
- Undersampling: Randomly select a subset of legitimate transactions
- Oversampling (SMOTE): Generate synthetic samples for fraudulent transactions

3. **Model Training and Evaluation:**
- Train and evaluate various classifiers:
  - Logistic Regression
  - XGBoost
  - Random Forest
- Use both undersampled and oversampled datasets

4. **Comparison and Visualization:**
- Compare model performance
- Visualize results using bar graphs

## Results

This project demonstrates the effectiveness of different models and sampling techniques in detecting credit card fraud. The results can guide the selection of appropriate models and strategies for real-world fraud detection systems.
![download (1)](https://github.com/priyanshuanandd/AspireNex/assets/112546168/3c175360-c8ae-4408-b368-6c3acdadeaa9)



## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvement, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

