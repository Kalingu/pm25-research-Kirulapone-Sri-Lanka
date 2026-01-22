PM2.5 Air Quality Forecasting for Kirulapone (Colombo)
Predicting hourly PM2.5 pollution levels using time‑series deep learning models (LSTM and N‑BEATS) with key evaluation metrics. This project was completed as the final research project for the Higher National Diploma in Data Science (HNDDS) at NIBM.

## Dataset

- **Source:** Local air quality monitoring station, Kirulapone, Colombo  
- **Time period:** Hourly readings from **9th January 2022 to 5th December 2025**  
- **Number of records:** 24,864  
- **Features:** 
  - **Target variable:** `pm2_5` (fine particulate matter)  
  - **Other environmental variables:** `pm10`, `carbon_monoxide`, `carbon_dioxide`, `nitrogen_dioxide`, `sulphur_dioxide`, `ozone`, `aerosol_optical_depth`, `dust`, `uv_index`, `uv_index_clear_sky`, `ammonia`, `methane`  
- **Data quality:** No missing values in the `pm2_5` column
- 

## Project Structure

This project compares two forecasting approaches:
- **LSTM (TensorFlow):** Long Short‑Term Memory network for sequential forecasting.
- **N‑BEATS (PyTorch):** Neural basis expansion analysis for interpretable time‑series forecasting.

## Features

- Data Preprocessing: clipping, log transformation, scaling  
- Sequence Creation: prepare time-series data for model input  
- Deep Learning Models: LSTM and N-BEATS  
- Evaluation Metrics: RMSE, MAE, R², MAPE  
- Academic research project: part of **HNDDS final research at NIBM**

## Model Results - PM2.5 Forecasting

The models were evaluated on standard metrics to predict hourly PM2.5 levels in Kirulapone.

| Metric | LSTM | N-BEATS |
|--------|------|---------|
| MSE    | 4.5972 | 2.7522 |
| RMSE   | 2.1441 | 1.6590 |
| MAE    | 1.5150 | 1.1541 |
| R²     | 0.9056 | 0.9435 |
| MAPE (%) | 10.6882 | 8.4915 |

**🏆 Winner:** N-BEATS (best overall performance on all metrics)

## Visualizations - LSTM Model/N-BEATS Model Training vs Validation Curve

<img width="642" height="377" alt="image" src="https://github.com/user-attachments/assets/eff9b3ba-b9ae-465c-a43e-36584bd887dd" />
<img width="640" height="377" alt="image" src="https://github.com/user-attachments/assets/30c63374-91ae-4346-b22e-ee611c3b40cd" />


## Usage

## How to Run
1. Clone the repository  
   `git clone https://github.com/Kalingu/pm25-forecast-kirulapone.git`
2. Install dependencies  
   `pip install -r requirements.txt`
3. Open and run the notebook  
   `jupyter notebook notebooks/pm25_lstm_nbeats.ipynb`
4. View results and plots

## License
This project is licensed under the MIT License — see LICENSE file for details.

