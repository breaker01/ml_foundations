
# 🚀 SONAR Rock vs Mine Prediction

This is an end-to-end machine learning project using Python to classify objects as **Rock (R)** or **Mine (M)** based on sonar signal data. The model predicts whether an object detected by sonar is a **rock** or a **metal mine under the sea**, based on frequency signal readings.

---

## 📂 Dataset Description

- The dataset contains **208 samples**, each with **60 features**.
- Each feature represents the strength of the sonar signal at a specific frequency.
- The target label is:
  - **'R'** → Rock
  - **'M'** → Mine

Dataset Source:  
[🔗 UCI Machine Learning Repository - SONAR Dataset](https://archive.ics.uci.edu/ml/datasets/connectionist+bench+(sonar,+mines+vs.+rocks))

---

## 🧠 Project Workflow

1. **Load the Dataset**  
   → Load the CSV dataset into a Pandas DataFrame.

2. **Data Exploration**  
   → View the data structure and count of rock vs mine samples.

3. **Data Preparation**  
   → Separate features (`X`) and labels (`Y`).

4. **Train-Test Split**  
   → Split the dataset into:
   - **90% Training data**
   - **10% Testing data**

5. **Model Creation**  
   → Use the Logistic Regression algorithm.

6. **Model Training**  
   → Train the model using the training set.

7. **Model Evaluation**  
   → Evaluate accuracy on both training and testing sets.

8. **Making Predictions**  
   → Predict whether a new sonar signal indicates a **Rock** or a **Mine**.

---

## 📦 Libraries Used

- Python 🐍
- Pandas
- NumPy
- Scikit-learn

---
## 🔍 Example Usage

```python
# Example input data (60 sonar signal values)
input_data = (0.0307, 0.0523, 0.0653, ..., 0.0055)

# Convert input data to numpy array
input_data_as_numpy_array = np.asarray(input_data)

# Reshape input for a single instance prediction
input_data_reshaped = input_data_as_numpy_array.reshape(1, -1)

# Make prediction
prediction = model.predict(input_data_reshaped)

if prediction[0] == 'R':
    print("The object is a Rock")
else:
    print("The object is a Mine")
```

---

## 📊 Model Performance

| Dataset | Accuracy (%) |
|---------|---------------|
| Training | ✅ (High)     |
| Testing  | ✅ (Good)     |

✔️ The model performs well with balanced accuracy on both training and testing datasets.

---

## ✨ Project Status

✅ Complete basic machine learning pipeline from data loading to prediction.  
🚀 Open for further improvements like:
- Testing with other ML algorithms (SVM, Random Forest, etc.)
- Hyperparameter tuning
- Building a web app interface (Streamlit/Flask)
- Model deployment
