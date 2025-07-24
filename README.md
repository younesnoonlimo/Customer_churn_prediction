# Customer Churn Prediction

## Overview
In this project, we aim to predict customer churn (whether a customer will leave a service provider) based on various customer attributes. This is a classic machine learning problem involving **customer retention**, and we used a dataset from **IBM Sample Data Sets** hosted on Kaggle.

### Dataset Description
This dataset contains information about customers, including details about their demographics, services they use, and account information. The target variable is **Churn**, which indicates whether the customer has left the service provider.

#### Context
The goal is to analyze relevant customer data and develop a focused customer retention program. The dataset allows us to predict customer behavior and make informed decisions about customer retention strategies.

> **Context from IBM**: "Predict behavior to retain customers. You can analyze all relevant customer data and develop focused customer retention programs." [IBM Sample Data Sets]

### Content
Each row in the dataset represents a customer. The columns contain various customer attributes that describe them. The dataset includes the following features:
- **Churn**: Whether the customer left in the last month (target variable).
- **Services**: Information about services subscribed to by the customer (phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV/movies).
- **Account Information**: Data about the customer’s account, such as tenure, contract type, payment method, paperless billing, monthly charges, and total charges.
- **Demographics**: Customer's gender, age range, and whether they have partners or dependents.

### Project Workflow

1. **Data Exploration**:
   - We began by exploring the dataset to understand its structure and identify useful features for the prediction model.
   - We checked for missing data, distributions of numerical variables, and the relationships between features.

2. **Data Cleaning**:
   - We handled missing values, removed unnecessary columns, and ensured that all data was in the correct format for analysis.
   - Categorical variables were encoded using **One-Hot Encoding** for multilevel categories (e.g., `gender`, `PhoneService`), and **Label Encoding** was used for the binary target variable `Churn`.

3. **Model Building**:
   - **Feature Engineering**: We selected the most relevant features based on data exploration, such as `gender`, `tenure`, `PhoneService`, `Contract`, `MonthlyCharges`, and `Churn`.
   - **Data Splitting**: The data was split into training and testing sets to evaluate the model's performance properly. A typical 80-20 split was used for training and testing.
   - **Model Selection**: A **Decision Tree** model was selected as the base model for classification due to its interpretability and ability to handle both categorical and numerical features.
   - **Model Training**: We trained the Decision Tree model on the training dataset.
   - **Model Evaluation**: The model was evaluated using common metrics such as accuracy, precision, recall, and the confusion matrix.

4. **Results**:
   - After training the model, we assessed its performance on the test set.
   - The Decision Tree model provided a good starting point for the churn prediction task, though further improvements (e.g., hyperparameter tuning or using more complex models) could be made.
   - Key insights and potential customer retention strategies were drawn from the model's results.

### Inspirations
This project was inspired by the challenge of predicting customer behavior and retention, which is a common problem for businesses across industries. We also used resources from the IBM community for reference, which provides a more detailed overview of similar problems.

- **New version from IBM**: [Telco Customer Churn Blog](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113)

---

### Technologies Used
- **Python**: Programming language used for data manipulation and machine learning.
- **Pandas**: Data analysis and manipulation.
- **Scikit-learn**: For building and evaluating machine learning models.
- **Matplotlib / Seaborn**: For data visualization.

---

## How to Run the Project

1. Clone this repository.
2. Install necessary dependencies:
   ```bash
   pip install -r requirements.txt
