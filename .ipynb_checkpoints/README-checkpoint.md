---

# Bank Customer Churn Prediction

This project aims to predict whether a bank customer will churn (leave the bank) using a dataset with various customer attributes. The goal is to build a robust model that can help the bank identify potential churners and take proactive measures to retain them.

## Table of Contents
- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Data Overview](#data-overview)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction
Churn prediction is crucial for banks to retain their customers and maintain a competitive edge. This project explores customer data to build a predictive model using neural networks, iteratively improving the model to achieve higher accuracy and reliability.

## Project Structure
1. **Data Exploration**
2. **Data Cleaning**
3. **Feature Engineering**
4. **Model Building**
5. **Model Evaluation**
6. **Business Recommendations**

## Data Overview
The dataset contains 10,000 records with 14 features each, including:
- **Customer Information**: e.g., CustomerId, Surname
- **Demographic Information**: e.g., Geography, Gender, Age
- **Account Information**: e.g., Tenure, Balance, NumberOfProducts, HasCrCard, IsActiveMember, EstimatedSalary
- **Target Variable**: Exited (whether the customer has churned)

### Statistical Summary
- The average CreditScore is 650, with a range from 350 to 850.
- Customers' ages range from 18 to 92, with an average of 39.
- Around 70% of the customers have a credit card.
- Approximately 50% of the customers are active members.

## Exploratory Data Analysis (EDA)
EDA is conducted to uncover patterns, detect anomalies, test hypotheses, and verify assumptions using summary statistics and graphical representations.

### Key Findings:
1. **Missing Values**: Features like `RowNumber`, `CustomerId`, and `Surname` are not useful for prediction and are excluded.
2. **Gender Distribution**: ~55% of the customers are male.
3. **Geographical Distribution**: Customers are from France, Germany, and Spain.
4. **Credit Card Ownership**: Over 70% of the customers have a credit card.
5. **Active Membership**: Around 50% of the customers are active members.

## Feature Engineering
Feature engineering involves creating new features based on existing data to enhance model performance.

### Key Features:
1. **isHighBalance**: Indicates if the balance is above the median.
2. **isSeniorCitizen**: Checks if the age is above 60.
3. **averageProducts**: Average number of products owned by customers.

- **Accuracy**: 76% on test data
- **F1-Score**: 84% for class 0 and 57% for class 1

### Improved Model
Using the Dropout technique and additional dense layers, the final model achieves:
- **Accuracy**: 80%
- **F1-Score**: 87% for class 0 and 60% for class 1

## Model Evaluation
The model is evaluated based on accuracy, F1-score, precision, and recall. The final model shows significant improvement in predicting customer churn.

## Installation
### Prerequisites:
- Python 3.8 or higher
- Jupyter Notebook

### Step-by-Step Installation:
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/bank-churn-prediction.git
    cd bank-churn-prediction
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Start the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

2. Open `eda.ipynb` for exploratory data analysis.

3. Open `model_building.ipynb` for building and evaluating the models.

## Contributing
We welcome contributions to improve the project. Please fork the repository, create a new branch, and submit a pull request with your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
