# Heart Disease Prediction App

A machine learning application that predicts the likelihood of heart disease using patient health metrics. Built with Streamlit and trained using a Random Forest classifier.

## Features

- **Interactive User Interface**: Easy-to-use web interface built with Streamlit
- **Real-time Predictions**: Get instant predictions based on patient data
- **Risk Scoring**: Displays risk percentage alongside prediction
- **Multiple Input Parameters**: Analyzes 11 different health metrics
- **Pre-trained Model**: Uses a Random Forest model trained on comprehensive heart disease datasets

## Input Parameters

The app analyzes the following health metrics:

- **Age**: Patient's age (18-100 years)
- **Sex**: Patient's gender (M/F)
- **Chest Pain Type**: Type of chest pain experienced (ATA, NAP, TA, ASY)
- **Resting Blood Pressure**: Blood pressure at rest (80-200 mm Hg)
- **Cholesterol**: Cholesterol level (100-600 mg/dL)
- **Fasting Blood Sugar**: Whether fasting blood sugar > 120 mg/dL (Yes/No)
- **Resting ECG**: Resting electrocardiogram results (Normal, ST, LVH)
- **Max Heart Rate**: Maximum heart rate achieved (60-220 bpm)
- **Exercise-Induced Angina**: Whether chest pain occurs during exercise (Y/N)
- **Oldpeak**: ST depression induced by exercise relative to rest
- **ST Slope**: Slope of the ST segment (Up, Flat, Down)

## Requirements

- Python 3.7 or higher
- Streamlit
- Pandas
- Scikit-learn
- Joblib

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/heart_disease_prediction.git
cd heart_stroke
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the Streamlit app:
```bash
streamlit run app.py
```

The app will open in your default web browser at `http://localhost:8501`.

### How to Use:

1. Enter or select your health metrics using the input widgets
2. Click the **"Predict"** button
3. View the prediction result and risk score
4. Green checkmark (✅) indicates low risk; Red warning (⚠️) indicates high risk

## Project Structure

```
heart_stroke/
├── app.py                          # Main Streamlit application
├── Heart_Stroke_prediction.ipynb  # Jupyter notebook with model training
├── Random_Forest_heart.pkl        # Pre-trained Random Forest model
├── scaler.pkl                     # Feature scaler for data normalization
├── columns.pkl                    # Expected feature columns
├── requirements.txt               # Project dependencies
└── README.md                      # This file
```

## Model Details

- **Algorithm**: Random Forest Classifier
- **Features**: 11 health-related attributes with one-hot encoding for categorical variables
- **Preprocessing**: StandardScaler normalization for numerical features
- **Output**: Binary classification (0: Low Risk, 1: High Risk) with probability scores

## Notes

- The model is pre-trained and ready to use
- Input data is automatically scaled before prediction
- Missing categorical features are automatically filled with 0s
- The app expects specific feature columns as defined in `columns.pkl`

## Disclaimer

This application is for educational purposes only and should not be used as a substitute for professional medical diagnosis. Always consult with a healthcare professional for medical advice.

## Contributing

Feel free to fork this repository and submit pull requests with improvements.

## Author

Created as a machine learning project for heart disease prediction.

## License

This project is open source and available under the MIT License.
