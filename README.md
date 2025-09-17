# 🌡️ Air Temperature Prediction - Multivariate Time Series Problem

## 📌 Project Overview
This project focuses on a deep learning approach to analyze a multivariate time series dataset. The goal is to perform exploratory data analysis (EDA) and use an **LSTM (Long Short-Term Memory)** model to predict air temperature one hour ahead based on past 5 hours of data.

## 📊 Dataset
The dataset consists of 50,400 rows and 23 columns. It is a **multivariate time series dataset**, with data recorded at uniform hourly intervals. The variables are mostly numerical, with the exception of 'From Date' and 'To Date', which are object data types. The dataset contains null values in the numeric variables, but no duplicated values.

## 🔍 Key Findings
1. The data has a consistent temporal pattern, making it suitable for multivariate time series analysis.
2. The final model achieved a **Mean Absolute Error (MAE)** of approximately **0.31**, a **Mean Squared Error (MSE)** of around **0.25**, and an **R-squared (R^2)** value of about **0.999**.
3. The high R-squared value indicates that the LSTM model was able to explain a very high percentage of the variance in the target variable, making accurate predictions.
4. The low MAE and MSE values confirm the model's high accuracy in predicting the target variable.
5. The use of EarlyStopping and ReduceLROnPlateau callbacks helped prevent overfitting and optimize the learning rate, contributing to the strong performance of the model.

## Steps
1. **Data Cleaning & Preprocessing**: The 'From Date' and 'To Date' columns were converted to datetime objects, and 'From Date' was set as the index. The remaining numerical columns contain null values, which would need to be addressed in the preprocessing step. There were no duplicate values found in the dataset.
2. **Modelling & Evaluation**: An LSTM deep learning model was built using the tensorflow.keras.models.Sequential API. The model includes LSTM, Dense, and Dropout layers. An EarlyStopping callback was used to prevent overfitting, and a ReduceLROnPlateau callback was used to adjust the learning rate during training. Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R2) were used as evaluation metrics for the model.

## 💡 Conclusion
The project successfully developed a deep learning model to predict air temperature (AT) using multivariate time series data. The data's consistent hourly intervals and the correlations between various atmospheric variables proved suitable for this type of analysis.

## 🔮 Possible Future Works
1. Further exploration of different preprocessing techniques for handling missing data, such as imputation or advanced interpolation methods.
2. Experimenting with different deep learning architectures, such as Bidirectional LSTMs or CNN-LSTMs, to potentially improve model performance.
3. Investigating the impact of different hyperparameter tuning strategies on the model's accuracy and efficiency.

## 👨‍💻 Author
**Liliana Djaja Witama** | Undergraduate Data Science Student at BINUS University
