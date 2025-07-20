# Train Delay Predictor

A machine learning project that predicts whether a train will be delayed based on a variety of factors including **weather**, **scheduled time**, **station**, **day of the week**, and **holiday status**.

## Dataset

The dataset used for training and evaluation consists of **500 entries**, each representing a scheduled train service with the following features:

- `station`: Name of the station
- `scheduled_time`: Scheduled time of the train (in HHMM format)
- `weather`: Weather condition (e.g., Sunny, Foggy, Cloudy)
- `day_of_week`: Day of the week
- `is_holiday`: Whether the scheduled date is a public holiday (0 or 1)
- `is_delayed`: Target variable, indicating if the train was delayed (0 or 1)

## Objective

The goal is to build a model that predicts the binary outcome `is_delayed` based on input features using different machine learning algorithms.

##  Technologies & Libraries

- Python 3
- Pandas
- Seaborn & Matplotlib (for visualization)
- scikit-learn
  - Random Forest
  - Logistic Regression
  - Train-test split
  - StandardScaler
- TensorFlow / Keras
  - Sequential model
  - Dense layers
- Accuracy metrics

## Models Explored

- **Random Forest Classifier**
- **Logistic Regression**
- **Neural Network** using Keras' `Sequential` model

## Workflow

1. **Load Data**: Read the CSV file containing train data.
2. **Preprocessing**:
   - Encode categorical columns (`station`, `weather`, `day_of_week`) to numeric types.
   - Convert `scheduled_time` to a numeric HHMM format.
3. **Feature Scaling**: Applied `StandardScaler` to standardize feature range.
4. **Model Training**:
   - Split the data into training and test sets (typically 80:20).
   - Train and compare different models.
5. **Evaluation**:
   - Used accuracy score to evaluate the performance of each model.
   - Considered implications of weather and time on delay rate via visualization.
