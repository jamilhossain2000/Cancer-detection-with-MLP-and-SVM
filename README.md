
# 🩺 Breast Cancer Prediction using MLP and SVM

A Machine Learning project for predicting breast cancer diagnosis using **Multi-layer Perceptron (MLP)** and **Support Vector Machine (SVM)** classifiers.

This project demonstrates a complete machine learning pipeline including:

- Data Loading
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Feature Scaling
- Model Training
- Performance Evaluation

The goal is to classify breast cancer tumors as:

- **Malignant (M)** → Cancerous
- **Benign (B)** → Non-cancerous

using features extracted from digitized images of Fine Needle Aspirates (FNA) of breast masses.

---

# 📌 Project Overview

Breast cancer remains one of the most critical health challenges worldwide. Early and accurate diagnosis can significantly improve treatment success and survival rates.

This project uses supervised machine learning techniques to analyze medical data and predict whether a tumor is malignant or benign based on several cellular characteristics.

Two machine learning models were implemented and compared:

1. **Multi-layer Perceptron (MLP)**
2. **Support Vector Machine (SVM)**

The notebook provides a complete workflow from raw data processing to final model evaluation.

---

# 📂 Dataset Information

The dataset used in this project is:

```bash
Cancer_Data.csv
```

The dataset contains multiple numerical features computed from digitized images of breast mass cell nuclei.

### Features Included

- Radius
- Texture
- Perimeter
- Area
- Smoothness
- Compactness
- Concavity
- Concave points
- Symmetry
- Fractal dimension

and several related mean, standard error, and worst-case measurements.

### Target Variable

| Diagnosis | Meaning |
|------------|----------|
| M | Malignant |
| B | Benign |

---

# ⚙️ Technologies and Libraries Used

The project was implemented using Python and the following libraries:

- NumPy
- Pandas
- Seaborn
- Matplotlib
- Scikit-learn (sklearn)
- Jupyter Notebook

---

# 📦 Prerequisites

Install the required Python libraries before running the notebook.

```bash
pip install numpy pandas seaborn matplotlib scikit-learn
```

---

# 🚀 Usage

## 1️⃣ Clone the Repository

```bash
git clone <repository_url>
cd Breast_Cancer_Prediction
```

---

## 2️⃣ Place the Dataset

Ensure that the dataset file:

```bash
Cancer_Data.csv
```

is placed in the same directory as the notebook file.

---

## 3️⃣ Run the Jupyter Notebook

Open and execute the notebook using Jupyter Notebook or Jupyter Lab.

```bash
jupyter notebook Breast_Cancer_Prediction.ipynb
```

---

# 📊 Notebook Workflow

The notebook follows the following machine learning workflow:

---

## 🔹 1. Data Loading

The dataset is loaded into a Pandas DataFrame.

### Operations Performed

- Read CSV file
- Display first few rows using `.head()`
- Display dataset information using `.info()`

---

## 🔹 2. Exploratory Data Analysis (EDA)

EDA is performed to better understand the dataset and identify patterns.

### Analysis Includes

- Checking missing values using:

```python
df.isnull().sum()
```

- Diagnosis class distribution
- Histograms for feature distributions
- Correlation matrix visualization
- Count plots for diagnosis labels

### Visualizations Used

- Histograms
- Heatmaps
- Count plots

These visualizations help understand:

- Feature relationships
- Data distribution
- Correlation between variables

---

## 🔹 3. Data Preprocessing

Several preprocessing steps are applied before training the models.

### Steps Performed

### ✔ Remove Irrelevant Columns

The following unnecessary columns are removed:

```python
'id'
'Unnamed: 32'
```

### ✔ Label Encoding

The diagnosis labels are encoded as:

| Original | Encoded |
|----------|----------|
| M | 1 |
| B | 0 |

using:

```python
LabelEncoder()
```

### ✔ Feature and Target Separation

```python
X = Features
y = Target
```

### ✔ Train-Test Split

Dataset is divided into:

- 60% Training Data
- 40% Testing Data

using:

```python
train_test_split(random_state=42)
```

### ✔ Feature Scaling

Standardization is performed using:

```python
StandardScaler()
```

This improves model performance and ensures all features are on the same scale.

---

# 🤖 Machine Learning Models

Two classification models are implemented and evaluated.

---

# 🧠 1. Multi-layer Perceptron (MLP)

The MLP model is a feedforward artificial neural network capable of learning complex patterns.

## Model Configuration

```python
MLPClassifier(hidden_layer_sizes=(80,20), max_iter=1000)
```

### Parameters

| Parameter | Value |
|-----------|------|
| Hidden Layers | (80,20) |
| Maximum Iterations | 1000 |

---

## Training Steps

- Train model on scaled training data
- Predict testing data
- Evaluate performance

---

## Evaluation Metrics

- Classification Report
- Confusion Matrix
- Accuracy Score

---

## ✅ MLP Accuracy

```bash
Accuracy: 0.969
```

---

# 📈 2. Support Vector Machine (SVM)

Support Vector Machine is a powerful supervised learning algorithm widely used for classification problems.

## Model Configuration

```python
SVC()
```

---

## Training Steps

- Train model on scaled training data
- Predict testing data
- Evaluate performance

---

## Evaluation Metrics

- Classification Report
- Confusion Matrix
- Accuracy Score

---

## ✅ SVM Accuracy

```bash
Accuracy: 0.974
```

---

# 📌 Results Summary

| Model | Accuracy |
|------|------|
| Multi-layer Perceptron (MLP) | 96.9% |
| Support Vector Machine (SVM) | 97.4% |

### Observation

The SVM classifier slightly outperformed the MLP classifier in terms of overall accuracy.

Both models achieved excellent classification performance for breast cancer diagnosis.

---

# 📉 Evaluation Metrics Used

The following evaluation metrics were used to measure model performance:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

These metrics provide deeper insight into the classification capabilities of the models.

---


# 🎯 Future Improvements

Possible future enhancements for this project include:

- Hyperparameter tuning
- Cross-validation
- Deep learning implementation
- Feature selection methods
- Model deployment using Flask or Streamlit
- Comparison with additional machine learning algorithms


---

# 📧 Contact

For any questions, suggestions, or collaborations, please open an issue in this repository.

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.

It helps the project reach more learners and developers in the machine learning community.
