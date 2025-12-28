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
The models were evaluated using the following metrics:
- **Accuracy Score**
- **Precision Score**
- **Recall Score**
- **F1 Score**
- **Training and Testing Accuracy**

From the notebook analysis, the models achieved high accuracy. For specific metric values and detailed performance on the test set, please refer to the notebook's output cells.
*(Note: You can add specific numbers here if you run the notebook or extract them from the outputs).*

## Files
- `Penguin_Model.ipynb`: Jupyter notebook containing the code for data analysis, preprocessing, model training, and evaluation.
- `penguins_size.csv`: The dataset file.
- `README.md`: Project documentation.
