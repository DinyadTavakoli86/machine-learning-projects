# Titanic Survival Prediction

This project applies machine learning techniques to predict passenger survival on the Titanic dataset.

The workflow covers data preprocessing, feature engineering, model comparison, hyperparameter tuning, feature importance analysis, and model evaluation.

---

## Project Workflow

1. Data Loading
2. Handling Missing Values
3. Feature Engineering
4. Encoding Categorical Features
5. Model Comparison using Cross Validation
6. Train-Test Split
7. Hyperparameter Tuning with GridSearchCV
8. Feature Importance Analysis
9. Decision Tree Visualization
10. Random Forest Visualization
11. Model Evaluation
12. Conclusion

---

## Feature Engineering

Several new features were created to improve model performance:

- **Title** extracted from passenger names
- **HasCabin** indicating whether cabin information is available
- **FamilySize** representing the total number of family members aboard

---

## Models Evaluated

The following models were compared using 5-Fold Cross Validation:

- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)

After the initial comparison, the two best-performing models were further optimized using GridSearchCV.

---

## Hyperparameter Tuning

GridSearchCV with 5-Fold Cross Validation was used to find the optimal value of:

- `max_depth` for Decision Tree
- `max_depth` for Random Forest

This approach helps reduce overfitting and provides a more reliable estimate of model performance.

---

## Results

### Final Test Accuracy

| Model | Accuracy |
|--------|----------|
| Decision Tree | **80.72%** |
| Random Forest | **82.06%** |

Random Forest achieved the highest accuracy and demonstrated more stable performance compared to a single Decision Tree.

---

## Feature Importance

Feature importance analysis showed that the most influential features include:

- Sex
- Title
- Fare
- Pclass
- Age

These variables played a major role in predicting passenger survival.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Model Export

The best Random Forest model is serialized using Joblib and saved as:

```python
best_random_forest.pkl
```

This file can be loaded later for inference without retraining the model.

Example:

```python
import joblib

model = joblib.load("best_random_forest.pkl")
prediction = model.predict(new_data)
```

## Dataset

Titanic Dataset:

The project uses the Titanic passenger dataset, which contains demographic and travel information used to predict passenger survival.

The dataset includes features such as:

- PassengerId
- Survived
- Pclass
- Name
- Sex
- Age
- SibSp
- Parch
- Ticket
- Fare
- Cabin
- Embarked

---

## Conclusion

Several machine learning models were evaluated and compared using 5-Fold Cross Validation.

The two best-performing models were further optimized using GridSearchCV, and their performance was evaluated on a separate test set.

Random Forest achieved the highest accuracy (**82.06%**) and outperformed a single Decision Tree (**80.72%**).

This project demonstrates a complete machine learning workflow, including data preprocessing, feature engineering, model comparison, hyperparameter tuning, feature importance analysis, and final model evaluation.