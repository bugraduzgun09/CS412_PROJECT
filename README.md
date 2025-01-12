# CS412_PROJECT


## Project Overview
This project involves building a machine learning pipeline for text analysis using Python. It includes two primary tasks: text classification and regression. The classification task focuses on categorizing users into predefined groups, while the regression task predicts like counts for user posts. The project processes Turkish text data and uses various libraries to handle data cleaning, transformation, and modeling.


## Features and Functionalities

1. **Data Loading**:
   - Loads training and test datasets from CSV and compressed JSONL files.
   - Separates user profiles and posts for further processing.

2. **Text Preprocessing**:
   - Removes unnecessary characters (e.g., zero-width spaces).
   - Replaces emojis with placeholders.
   - Collapses repeated punctuation for consistency.

3. **Feature Engineering**:
   - Transforms text data into numerical features using TF-IDF (Term Frequency-Inverse Document Frequency). TF-IDF was selected to extract meaningful patterns from text data by emphasizing unique words and reducing the weight of common ones.

4. **Model Training and Evaluation**:
   - **Tasks and Models**:
     - **Classification Task**: 
       - **Logistic Regression (LogReg)**: Used for baseline classification evaluations.
     - **Regression Task**:
       - Multiple models were regressed to predict like counts for user posts, including:
         - **Linear Regression (LinReg)**
         - **Support Vector Regression (SVR)**
         - **Gradient Boosting Regression (GBR)**
       - After evaluations, **Random Forest Regression (RF)** was selected as the final model due to its superior performance in handling complex patterns and achieving higher accuracy.
   - Splits data into training and test sets for validation.
   - Evaluates classification performance using metrics like accuracy, precision, and recall.
   - Evaluates regression performance using metrics like Mean Squared Error (MSE) and R-squared.

5. **Results Output**:
   - Saves predictions from classification and regression models to separate CSV files for further analysis.
