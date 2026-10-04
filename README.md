# Heart Disease Prediction API

A machine learning web API that predicts the likelihood of heart disease based on patient health data, built with **FastAPI** and a **Logistic Regression** model.

## Overview

This project trains a classification model on a heart disease dataset and serves predictions through a REST API, allowing users to input patient parameters and receive a risk prediction in real time.

## Model Performance

- **Algorithm:** Logistic Regression
- **Accuracy:** 81%
- **AUC-ROC:** 0.897

## Tech Stack

- **Python**
- **FastAPI** — REST API framework
- **Uvicorn** — ASGI server
- **scikit-learn** — model training and evaluation
- **Pandas / NumPy** — data processing
- **Pydantic** — request/response validation

## Project Structure

```
heart-disease-prediction-fastapi/
├── main.py              # FastAPI app and prediction endpoint
├── model.pkl            # Trained logistic regression model
├── requirements.txt     # Project dependencies
└── README.md
```

## Setup & Installation

1. Clone the repository
   ```
   git clone https://github.com/yourusername/heart-disease-prediction-fastapi.git
   cd heart-disease-prediction-fastapi
   ```

2. Install dependencies
   ```
   python -m pip install -r requirements.txt
   ```

3. Run the app
   ```
   uvicorn main:app --reload
   ```

4. Open your browser at `http://127.0.0.1:8000/docs` to test the API using the interactive Swagger UI.

## API Usage

**Endpoint:** `POST /predict`

**Example Request Body:**
```json
{
  "age": 52,
  "sex": 1,
  "cp": 0,
  "trestbps": 125,
  "chol": 212,
  "fbs": 0,
  "restecg": 1,
  "thalach": 168,
  "exang": 0,
  "oldpeak": 1.0,
  "slope": 2,
  "ca": 2,
  "thal": 3
}
```

**Example Response:**
```json
{
  "prediction": 1,
  "risk": "High"
}
```

## Future Improvements

- Containerize with Docker
- Deploy to Render
- Add a frontend interface for non-technical users

## Author

**Yuvanraj M**
[GitHub](https://github.com/yuvan05-ship-it) · [LinkedIn](https://linkedin.com/in/yuvanraj05)
