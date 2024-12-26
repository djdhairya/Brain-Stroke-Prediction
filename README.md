
# Brain Stroke Prediction

## Introduction
The **Brain Stroke Prediction** application predicts whether a person is at risk of having a stroke based on input parameters like age, medical history, and lifestyle factors. This project uses machine learning techniques for the prediction.

---

## Project Description
The prediction model leverages multiple features such as gender, age, hypertension, heart disease, and more. It uses a combination of data preprocessing, feature engineering, and a machine learning ensemble classifier for robust predictions. Users can input their details via a web interface, and the system will display the likelihood of a stroke.

---

## Installation

### Prerequisites
- Required Python libraries:
  ```bash
  pip install flask pandas numpy matplotlib seaborn plotly scikit-learn joblib
  ```

### Steps
1. Clone or download the project repository.
2. Ensure the `model.joblib` file is available at the specified path:
3. Run the Flask application:
   ```bash
   python app.py
   ```
4. Open the application in your browser at `http://127.0.0.1:5000`.

---

## Usage
1. Open the application in a web browser.
2. Enter the required details in the input form.
3. Submit the form to receive the prediction result.

---

## Input Fields
| **Field**              | **Description**                                            | **Example**            |
|-------------------------|------------------------------------------------------------|------------------------|
| `gender`               | Gender of the individual                                   | `male`, `female`       |
| `age`                  | Age in years                                              | `45`                  |
| `hypertension`         | 1 if the individual has hypertension, 0 otherwise         | `1`                   |
| `heart_disease`        | 1 if the individual has a heart disease, 0 otherwise      | `0`                   |
| `ever_married`         | `yes` if ever married, `no` otherwise                     | `yes`                 |
| `work_type`            | Type of work: `Private`, `Govt_job`, `children`, etc.     | `Private`             |
| `Residence_type`       | Type of residence: `Urban` or `Rural`                     | `Urban`               |
| `avg_glucose_level`    | Average glucose level in the blood (mg/dL)                | `105.5`               |
| `bmi`                  | Body Mass Index                                           | `22.4`                |
| `smoking_status`       | Smoking habit: `smokes`, `never smoked`, or `formerly smoked` | `never smoked`      |

---

## Output
The application predicts whether the person is:
- **Likely** to have a stroke.
- **Not Likely** to have a stroke.

---

## Training Details

### Libraries Used
The following libraries were used for data processing, visualization, and model training:
- **Data Handling and Visualization**:
  - `pandas`, `numpy`: Data manipulation and analysis.
  - `matplotlib`, `seaborn`: Static data visualization.
  - `plotly`: Interactive data visualization.

- **Machine Learning**:
  - `sklearn.preprocessing`:
    - `OneHotEncoder`: For encoding categorical features.
    - `OrdinalEncoder`: For ordinal data encoding.
  - `sklearn.pipeline`:
    - `Pipeline`: For chaining preprocessing and model steps.
  - `sklearn.compose`:
    - `ColumnTransformer`: For applying different preprocessing to column subsets.
  - `sklearn.ensemble`:
    - `VotingClassifier`: For combining multiple classifiers for robust predictions.
  - `sklearn.metrics`:
    - `roc_auc_score`, `roc_curve`, `auc`: For performance evaluation.
    - `PredictionErrorDisplay`: For visualizing prediction errors.

### Model Workflow
1. **Data Preprocessing**:
   - Handled missing values.
   - Encoded categorical features using `OneHotEncoder` and `OrdinalEncoder`.
   - Normalized numeric features.

2. **Model Training**:
   - Used an ensemble `VotingClassifier` to combine multiple models.
   - Optimized hyperparameters for best performance.
   - Evaluated the model using metrics such as AUC-ROC.

3. **Final Model**:
   - Saved using `joblib` for deployment.

---

## File Structure
```
Brain Stroke Prediction/
├── app.py                
├── model/
│   └── model.joblib      
├── templates/
│   ├── index.html        
│   └── result.html       
├── README.md             
├── data/
│   └── datasets.csv      
└── brain_stroke_prediction.ipynb  
```
![Screenshot 2024-12-26 104643](https://github.com/user-attachments/assets/31b09b10-3771-413d-a234-05412a37aec3)
![Screenshot 2024-12-26 104703](https://github.com/user-attachments/assets/e5359e0f-e43f-43d2-83a9-76a9e0062a90)


---

