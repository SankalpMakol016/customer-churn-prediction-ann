# Customer Churn Prediction using ANN

A deep learning web application that predicts whether a bank customer is likely to churn based on customer profile and account information.

The project uses an **Artificial Neural Network (ANN)** built with TensorFlow/Keras, preprocessing with scikit-learn, and an interactive Streamlit interface for real-time predictions.

## Live Demo

🚀 **Live App:** https://customer-churn-ann2.streamlit.app

## Features

- Interactive customer data input through a Streamlit web app
- Real-time churn probability prediction
- Binary churn classification using a trained ANN
- Gender encoding using `LabelEncoder`
- Geography encoding using `OneHotEncoder`
- Feature scaling using `StandardScaler`
- Early stopping to reduce overfitting
- TensorBoard logging for training visualization
- Saved preprocessing objects for consistent inference

## Tech Stack

- Python
- TensorFlow / Keras
- scikit-learn
- pandas
- NumPy
- Streamlit
- TensorBoard
- Matplotlib

## Project Structure

```text
.
├── app.py
├── experiments.ipynb
├── prediction.ipynb
├── Churn_Modelling.csv
├── model.h5
├── label_encoder_gender.pkl
├── onehot_encode_geography.pkl
├── Scaler.pkl
├── requirements.txt
├── .gitignore
└── README.md
```

## Model Workflow

```text
Customer Input
      ↓
Gender Label Encoding
      ↓
Geography One-Hot Encoding
      ↓
Feature Alignment
      ↓
Standard Scaling
      ↓
Artificial Neural Network
      ↓
Churn Probability
      ↓
Churn / No Churn Prediction
```

## Input Features

The application uses the following customer attributes:

- Geography
- Gender
- Age
- Balance
- Credit Score
- Estimated Salary
- Tenure
- Number of Products
- Credit Card Ownership
- Active Membership Status

## Running Locally

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd customer-churn-prediction-ann
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the environment

For macOS/Linux:

```bash
source .venv/bin/activate
```

For Windows:

```bash
.venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the Streamlit application

```bash
streamlit run app.py
```

## Prediction Logic

The model outputs a churn probability between `0` and `1`.

- Probability greater than `0.5` → Customer is likely to churn
- Probability less than or equal to `0.5` → Customer is not likely to churn

## Model Training

The Artificial Neural Network is trained for binary classification using:

- Binary Cross-Entropy loss
- Adam optimizer
- Accuracy as a training metric
- Early stopping based on validation loss
- TensorBoard callbacks for experiment tracking

The best model weights are restored when validation performance stops improving.

## Deployment

The application is deployed using Streamlit Community Cloud.

🚀 **Live Application:** https://customer-churn-ann2.streamlit.app

## Future Improvements

- Add precision, recall, F1-score, and ROC-AUC evaluation
- Add confusion matrix and ROC curve visualizations
- Improve the Streamlit UI
- Add prediction explanations
- Add batch prediction through CSV upload
- Compare ANN performance with traditional ML models
- Add experiment tracking and model versioning

## Author

Built as an end-to-end ANN classification project covering:

- Data preprocessing
- Feature encoding
- Feature scaling
- Neural network training
- Model evaluation
- Model persistence
- Prediction pipeline
- Streamlit deployment