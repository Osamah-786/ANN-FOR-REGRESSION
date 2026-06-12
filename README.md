# ANN for Regression using PyTorch

## Overview

This project demonstrates how to build and train an Artificial Neural Network (ANN) for a regression problem using PyTorch. The model is trained to predict power plant energy output based on environmental factors such as temperature, vacuum, pressure, and humidity.

The project covers the complete machine learning workflow, including data preprocessing, feature scaling, neural network design, model training, evaluation, and prediction.

---

## Dataset Features

The dataset contains the following input features:

* **AT** – Ambient Temperature
* **V** – Exhaust Vacuum
* **AP** – Ambient Pressure
* **RH** – Relative Humidity

### Target Variable

* **PE** – Electrical Energy Output

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* PyTorch
* Matplotlib

---

## Project Workflow

### 1. Data Preprocessing

* Load the dataset
* Check for missing values
* Separate features and target variable
* Split data into training and testing sets

### 2. Feature Scaling

* Standardize input features using `StandardScaler`

### 3. Neural Network Architecture

The ANN consists of:

Input Layer → 6 Neurons → ReLU

Hidden Layer → 6 Neurons → ReLU

Output Layer → 1 Neuron

### 4. Model Training

* Loss Function: Mean Squared Error (MSE)
* Optimizer: Adam
* Learning Rate: 0.001
* Epochs: 100

### 5. Model Evaluation

* Training Loss
* Validation Loss
* R² Score
* Predicted vs Actual comparison

---

## Model Architecture

```python
nn.Sequential(
    nn.Linear(input_size, 6),
    nn.ReLU(),

    nn.Linear(6, 6),
    nn.ReLU(),

    nn.Linear(6, 1)
)
```

---

## Results

The trained model is evaluated using:

* Mean Squared Error (MSE)
* R² Score

The best-performing model is automatically saved as:

```text
best_model.pt
```

---

## Files Included

```text
ANN_FOR_REGRESSION.ipynb    # Complete notebook
best_model.pt               # Saved trained model
requirements.txt            # Project dependencies
README.md                   # Project documentation
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Osamah-786/ANN-FOR-REGRESSION.git
```

Move into the project directory:

```bash
cd ANN-FOR-REGRESSION
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Jupyter Notebook:

```bash
jupyter notebook
```

---

## Future Improvements

* Hyperparameter tuning
* Early stopping
* Dropout regularization
* Cross-validation
* Model deployment using Flask or FastAPI
* Interactive prediction dashboard

---

## Author

**Osamah Shaikh**

Aspiring AI/ML Engineer passionate about Machine Learning, Deep Learning, Data Science, and AI-powered applications.
