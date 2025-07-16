# Resturant-rating-predictor
 Predicting restaurant ratings using Decision Tree Regression in Python
 This project aims to predict restaurant ratings based on features such as location, cuisine type, pricing, and more. The prediction is made using a Decision Tree Regression model, trained on real-world data.
 🧠 Model Overview
Algorithm Used: Decision Tree Regressor

R² Score (Cross-validated): ~0.91

Top Features:

Votes

Longitude

Currency

Latitude

📊 Features Used
Longitude, Latitude – Geographical location of the restaurant

Cuisines – Encoded cuisine category

Average Cost for two

Currency – Encoded currency type

Has Table booking

Price range

Votes

📦 Installation
pip install -r requirements.txt

🧪 How to Run
To test the model with custom input:
import joblib
import pandas as pd

model = joblib.load('decision_tree_model.pkl')
sample_input = pd.DataFrame([{
    'Longitude': 121.027535,
    'Latitude': 14.565443,
    'Cuisines': 39,
    'Average Cost for two': 12100.0,
    'Currency': 1,
    'Has Table booking': 0,
    'Price range': 3,
    'Votes': 314.0
}])

print("Predicted Rating:", model.predict(sample_input)[0])

✅ Results
The model achieved 92% R² on the training data.

Cross-validated performance (5-fold CV): Mean R² = 0.912

Main features:
Votes and location-based features are highly influential in predicting aggregate restaurant ratings. This model can be a useful tool for food delivery platforms, restaurant reviews, or recommendation systems.






