## 📘 Overview

This project analyzes historical weather data to predict future weather
conditions using supervised machine learning. It walks through a
complete data science workflow --- from preprocessing to model
evaluation.

------------------------------------------------------------------------

## 🧩 Objectives

-   Load and explore the weather dataset\
-   Clean, encode, and scale the data\
-   Select the most relevant features\
-   Train and evaluate classification models\
-   Optimize model parameters and compare results

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   **Python 3.x**\
-   **pandas** -- data manipulation\
-   **scikit-learn** -- preprocessing, model building, and evaluation\
-   **NumPy** -- numerical computation\
-   *(Optional)* **Matplotlib / Seaborn** -- visualization

------------------------------------------------------------------------

## ⚙️ Workflow Summary

1.  **Data Loading**
    -   Load the dataset `Weather Data.csv` using pandas.
2.  **Data Preprocessing**
    -   Handle missing values with `SimpleImputer`
    -   Encode categorical variables with `LabelEncoder` or
        `OneHotEncoder`
    -   Scale numerical features using `StandardScaler` or
        `MinMaxScaler`
3.  **Feature Selection**
    -   Apply `SelectKBest` using the chi-square (`chi2`) method to
        retain top predictors.
4.  **Model Building**
    -   Train and compare:
        -   **Logistic Regression**
        -   **Decision Tree Classifier**
    -   Split data into training and test sets using `train_test_split`.
5.  **Model Evaluation**
    -   Evaluate performance using:
        -   **Accuracy Score**
        -   **Classification Report (Precision, Recall, F1)**
        -   **Confusion Matrix**
        -   **F2 Score**
    -   Tune Decision Tree using varying depths to balance training and
        testing accuracy.

------------------------------------------------------------------------

## 📊 Results

  ------------------------------------------------------------------------------------
  Model        Accuracy       Precision     Recall           F1-score     F2-score
  ------------ -------------- ------------- ---------------- ------------ ------------
  Logistic     \~0.85--0.90   High for      Moderate         \~0.86       \~0.84
  Regression                  majority                                    
                              classes                                     

  Decision     \~0.88         Slightly      Good             \~0.87       \~0.86
  Tree                        higher        generalization                
  (Optimal                    precision                                   
  Depth ≈                                                                 
  5--7)                                                                   
  ------------------------------------------------------------------------------------

-   **Confusion Matrix:**\
    Showed strong diagonal dominance, indicating good predictive
    performance.
-   **F2 Score:**\
    Used to emphasize recall performance; model achieved a balanced
    recall-to-precision trade-off.
-   **Depth Tuning:**\
    Very shallow trees underfit; very deep trees overfit. Optimal
    performance achieved at mid-depth (5--7).

------------------------------------------------------------------------

## 📁 Files

-   `Weather_ver02.ipynb` -- Main analysis notebook\
-   `Weather Data.csv` -- Input dataset

------------------------------------------------------------------------
