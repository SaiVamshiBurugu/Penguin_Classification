# Penguin Classification Model

## Project Overview
This project involves building and evaluating several machine learning models to classify penguin species based on their physical characteristics. The analysis is performed using the `Palmer Archipelago (Antarctica) penguin data`.

## Dataset
The specific dataset used is `penguins_size.csv`, focusing on predicting the species of penguins.

### Data Columns:
- `species`: Penguin species (Target Variable) - Adelie, Chinstrap, Gentoo
- `island`: Island name (Dream, Torgersen, Biscoe)
- `culmen_length_mm`: Length of the culmen (bill) in mm
- `culmen_depth_mm`: Depth of the culmen (bill) in mm
- `flipper_length_mm`: Length of the flipper in mm
- `body_mass_g`: Body mass in grams
- `sex`: Sex of the penguin

### Key Preprocessing Steps:
- **Missing Value Handling:**
    - `culmen_length_mm`, `culmen_depth_mm`, `flipper_length_mm`, `body_mass_g`: Missing values filled with the mean of the column.
    - `sex`: Missing values filled with the mode.
    - `.` in the `sex` column was replaced with `NaN` before filling.
- **Categorical Encoding:**
    - `sex` and `island` were one-hot encoded using `pd.get_dummies` (drop_first=True).
    - `species` (Target) was Label Encoded.
- **Feature Scaling:**
    - `StandardScaler` was used to scale the features.

## Models Implemented
The following classification models were trained and evaluated:
1.  **Logistic Regression**
2.  **Decision Tree Classifier**
3.  **Random Forest Classifier**
4.  **K-Nearest Neighbors (KNN)**

## Model Evaluation & Results
The models were evaluated based on their accuracy scores. Below is a summary of the performance for each model:

| Model | Training Accuracy | Testing Accuracy |
| :--- | :--- | :--- |
| **Logistic Regression** | 99.22% | 98.84% |
| **K-Nearest Neighbors (KNN)** | 99.61% | 98.84% |
| **Decision Tree** | 100.0% | 97.67% |
| **Random Forest** | 100.0% | 98.84% |
| **AdaBoost** | 97.29% | 98.84% |
| **Gradient Boosting** | 100.0% | 97.67% |

### Key Insights:
- **High Performance:** All models performed exceptionally well, with testing accuracies ranging from 97.67% to 98.84%.
- **Best Performers:** **Logistic Regression, KNN, Random Forest, and AdaBoost** achieved the highest testing accuracy of **98.84%**.
- **Overfitting:** The Decision Tree, Random Forest, and Gradient Boosting models achieved 100% training accuracy, indicating potential overfitting, although they still generalized very well to the test set.
- **Consistency:** Random Forest and KNN showed strong consistency between training and testing performance.

## Conclusion
The project successfully demonstrates the ability to classify penguin species with high precision using standard machine learning algorithms. Based on the results, **Random Forest** or **Logistic Regression** would be excellent choices for deployment due to their high accurracy and robustness.

## Files
- `Penguin_Model.ipynb`: Jupyter notebook containing the code for data analysis, preprocessing, model training, and evaluation.
- `penguins_size.csv`: The dataset file.
- `README.md`: Project documentation.
