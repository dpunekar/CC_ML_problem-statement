This repository contains a complete end-to-end machine learning project which focused on predicting Crowd Energy for live music shows and using those predictions to optimize ticket pricing for maximum profit.
The project combines data cleaning, exploratory data analysis (EDA), feature engineering, model training with cross-validation, and a business-oriented revenue optimization analysis.

The goal of this project is to:
1. Predict Crowd Energy for music shows using historical data
2. Test the singer’s hypotheses using EDA and visualizations
3. Train and tune a regression model with cross-validation
4. Optimize ticket price to maximize profit for a specific venue (V_Gamma – The Snob Pit)

Data Preprocessing (documented in analysis_notebook.ipynb)
Key preprocessing steps include:
1. Cleaning inconsistent date and ticket price formats, handling invalid and missing values.
2. Converting mixed-currency ticket prices into a common scale
3. Feature engineering (e.g., is_weekend)
4. One-hot encoding of categorical features (Venue_ID, Band_Outfit)
5. Ensuring identical preprocessing for train and test datasets

Exploratory Data Analysis (EDA) (charts for analysis in analysis_notebook.ipynb and conclusions in findings_report.pdf)
EDA was used to test several hypotheses proposed by the lead singer, including:
1. The Tuesday Curse
2. Full Moon = Magic
3. Rain Sucks
4. The Sweet Spot (ticket price vs energy)
5. The Crowd Feeds Itself
6. Post-show sales vs crowd energy

Model Training & Evaluation (available in analysis_notebook.ipynb)
Model used: RandomForestRegressor
Chosen for:
1. Non-linear relationship handling
2. Robustness to noise and outliers
3. Compatibility with one-hot encoded features

Hyperparameter tuning is performed using 5-fold cross-validation.

Finally the trained model was used to predict Crowd_Energy for a different test dataset and is exported to prediction.csv

Revenue Optimization
A business-focused optimization was performed for V_Gamma (The Snob Pit).

Business Context:
Capacity: ~800 seats
Fixed cost: $5,000 per show
Variable cost: $8 per attendee

Using the trained model and EDA the optimal price for this purpose was calculated. The completed procedure is documented in revenue_optimisation.pdf

Note: The problem statement document is also uploaded (MachineLearning_CodingWeek.pdf)
