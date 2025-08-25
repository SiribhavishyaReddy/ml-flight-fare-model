✈️ Flight Fare Prediction using Machine Learning
📌 Problem Statement

Airline ticket prices are dynamic and vary depending on factors such as the airline, source, destination, duration, stops, and journey date. The goal of this project is to build a machine learning model that predicts flight ticket prices based on these features.

🎯 Objectives

Perform Exploratory Data Analysis (EDA) to understand patterns in ticket pricing.

Apply feature engineering on date, time, and categorical data.

Train machine learning models to predict ticket prices.

Compare model performances (Extra Trees vs Random Forest).

Visualize actual vs predicted fares.

📂 Dataset

Source: Data_Train.xlsx

Contains details like:

Airline

Date of Journey

Source & Destination

Route & Duration

Total Stops

Price (Target Variable)

🛠️ Steps Performed
🔹 Data Preprocessing & Feature Engineering

Handled missing values.

Extracted:

Journey Day & Month from Date_of_Journey

Departure & Arrival hours and minutes

Duration hours and minutes

Encoded categorical variables (Airline, Source, Destination) using OneHotEncoding.

Converted “Total Stops” into numeric values (non-stop → 0, 2 stops → 2, etc.).

🔹 Exploratory Data Analysis (EDA)

Count plots and boxen plots to study Airline vs Price, Source vs Price, and Destination vs Price.

Observations:

Jet Airways (Business) has the highest fares.

Most airlines have similar median price ranges.

🔹 Modeling & Prediction

📌 Step 1: Split Features & Target

X = all features

y = target (Price)

📌 Step 2: Train/Test Split

80% Training, 20% Testing

📌 Step 3: Models Used

Extra Trees Regressor → Accuracy: 80.6%

Random Forest Regressor → Accuracy: 79.7%

📌 Step 4: Comparison
Created a dataframe showing Actual vs Predicted Prices for both models.

📊 Results

Extra Trees performed slightly better than Random Forest.

Both models predict ticket prices with ~80% accuracy.

Example Output:

Features	Actual Price	Extra Trees Prediction	Random Forest Prediction
Row 1	12,000	11,800	11,900
Row 2	5,500	5,300	5,400
🚀 Technologies Used

Python

Pandas, NumPy

Seaborn, Matplotlib (EDA & Visualization)

Scikit-learn (ML models: ExtraTrees, RandomForest)

📌 Future Improvements

Try XGBoost / LightGBM for higher accuracy.

Deploy model using Streamlit / Flask for real-time predictions.

Add more flight features (booking date, seasonal data, holidays).
