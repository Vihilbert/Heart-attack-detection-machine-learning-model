# Heart Attack Prediction using SVM Classifiers

This project involves predicting heart attacks based on patient data using Support Vector Machine (SVM) classifiers. The dataset used for this task contains features like age, sex, chest pain type (cp), resting blood pressure (trtbps), cholesterol levels (chol), and more. The target variable (`output`) indicates whether a patient has a high risk (1) or low risk (0) of heart attack.

## Dataset

The dataset includes the following columns:
- **age**: Age of the patient
- **sex**: Gender (1 = male, 0 = female)
- **cp**: Chest pain type (categorical)
- **trtbps**: Resting blood pressure
- **chol**: Cholesterol level
- **fbs**: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
- **restecg**: Resting electrocardiographic results (categorical)
- **thalachh**: Maximum heart rate achieved
- **exng**: Exercise-induced angina (1 = yes, 0 = no)
- **oldpeak**: ST depression induced by exercise relative to rest
- **slp**: Slope of the peak exercise ST segment
- **caa**: Number of major vessels (0-3) colored by fluoroscopy
- **thall**: Thalassemia (categorical)
- **output**: Target variable (1 = high risk of heart attack, 0 = low risk)

## Code Description

The provided code performs the following steps:
1. **Data Loading**: The data is loaded into a pandas DataFrame.
2. **Visualization**: Two scatter plots are generated to visualize the relationship between age and cholesterol, colored by the `output` variable.
3. **Data Preprocessing**: The features are selected and converted into numpy arrays. The data is split into training (80%) and testing (20%) sets.
4. **Model Training**: Several SVM classifiers are tested with different kernel functions (`linear`, `poly`, `rbf`, `sigmoid`), and the performance is evaluated using the F1 score. The `linear` kernel performed the best, with an F1 score of 0.917.
5. **Prediction and Evaluation**: The model is trained using the linear SVM classifier, and predictions are made on the test set. Performance metrics such as the confusion matrix, classification report, and F1 score are calculated. The Jaccard index is also computed.

## Model Performance

- **Accuracy**: 92%
- **F1 Score**: 0.9178 (weighted average)
- **Jaccard Score**: 0.8148 (for low-risk class)

The confusion matrix shows:
- **True Positive (1)**: 34 instances correctly classified as high risk
- **True Negative (0)**: 22 instances correctly classified as low risk
- **False Positive (1)**: 3 instances incorrectly classified as high risk
- **False Negative (0)**: 2 instances incorrectly classified as low risk

## Requirements

The following Python libraries are used in the project:
- pandas
- numpy
- scipy
- scikit-learn
- matplotlib

To install the necessary dependencies, run:
```bash
pip install pandas numpy scipy scikit-learn matplotlib
```

## Usage

To run the code, ensure that the dataset is named `heart_attack.csv` and placed in the same directory as the code file. Execute the Python script to train the SVM model and evaluate its performance.

```bash
python heart_attack_prediction.py
```

---
