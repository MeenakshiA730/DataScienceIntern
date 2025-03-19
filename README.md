# DataScienceIntern
Movie Rating Prediction
Project Overview
This project builds a predictive model to estimate movie ratings based on various attributes such as genre, director, duration, votes, and historical success metrics. The model is trained using machine learning techniques with preprocessing, feature engineering, and hyperparameter tuning to enhance performance.
Dataset
The dataset used for this project is IMDb Movies India.csv, containing information about Indian movies, including:
- Year of release
- Genre
- Director
- Duration (minutes)
- Votes
- IMDb Rating
Features and Preprocessing
Data Cleaning:
- Extracted numeric values from Year, Duration, and Votes.
- Replaced missing numerical values using SimpleImputer (median strategy).
- Categorical variables (Genre and Director) were grouped into common categories.
Feature Engineering:
- Director_Success_Rate: Average rating of movies by the same director.
- Genre_Avg_Rating: Average rating of movies in the same genre.
- Log transformation of votes to normalize the distribution.
Preprocessing Pipeline:
- Numerical features: Scaled using RobustScaler to handle outliers.
- Categorical features: One-hot encoded with OneHotEncoder.
- Feature Selection: Used SelectKBest to choose the most relevant features.
Model Implementation
- Algorithm: RandomForestRegressor with 300 estimators, depth of 12, and min_samples_split of 5.
- Train-Test Split: 80% training, 20% testing.
- Cross-validation: Performed 5-fold cross-validation to validate model stability.
Model Evaluation
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R-squared Score (R2 Score)
- Cross-Validation R2 Score
Usage
1. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn
   ```
2. Run the script:
   ```bash
   python movie_rating_prediction.py
   ```
3. View model evaluation metrics in the console.
Future Enhancements
- Try other regression models like Gradient Boosting or XGBoost.
- Incorporate text-based features such as movie summaries or reviews.
- Use deep learning models for improved performance.
Author
Developed by Meenakshi A🚀
