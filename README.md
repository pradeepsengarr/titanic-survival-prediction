#  Titanic Survival Prediction using Logistic Regression

This project I Worked on  trained a model to predict which passengers survived the Titanic disaster — inspired by the classic Kaggle Titanic dataset.


##  **Project Overview**
- **Dataset**: Classic Titanic dataset (features like Pclass, Sex, Age, Fare, etc.)
- **Goal**: Predict whether a passenger survived (`0` = did not survive, `1` = survived)
- **Model**: Logistic Regression (simple yet powerful for binary classification)

##  **Steps:**
1. **Data Cleaning**  
   - Fill missing Age values with median (from train data)
   - Encode categorical variables (`Sex`, `Embarked`) into numeric features

2. **Feature Selection**  
   - Selected features: `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked_Q`, `Embarked_S`

3. **Train/Test Split**  
   - Split data into train and validation sets

4. **Model Training**  
   - Trained Logistic Regression with `max_iter=1000`

5. **Evaluation**  
   - Accuracy score, confusion matrix, and classification report

6. **Prediction**  
   - Created sample passengers to test model predictions


##  **Example: Predicting a new passenger**

```python
import pandas as pd

new_passenger = pd.DataFrame([{
    'Pclass': 3,
    'Sex': 1,
    'Age': 25,
    'SibSp': 0,
    'Parch': 0,
    'Fare': 7.25,
    'Embarked_Q': 0,
    'Embarked_S': 1
}])

prediction = model.predict(new_passenger)
print("Predicted class (0=did not survive, 1=survived):", prediction[0])
