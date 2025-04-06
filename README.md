# Global-Weather-Repository
This project analyzes and forecasts temperature trends using a combination of machine learning and deep learning models. The pipeline includes data preprocessing, exploratory data analysis, and model comparison for time series forecasting.

---

## 📂 Dataset

- The dataset is sourced from [Kaggle - Global Temperature Time Series](https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data).
- It contains long-term historical data of average temperatures across various locations.
  
---

## 🛠️ Project Structure

- `data_analysis.ipynb`: Handles data loading, cleaning, feature engineering, and exploratory visualizations.
- `model_comparison.ipynb`: Implements four models (XGBoost, ARIMA, LSTM, Transformer), evaluates and compares their performances.

---

## 📊 Exploratory Data Analysis Highlights

- Temperature trends were visualized monthly and annually.
- Seasonal patterns and long-term warming trends were identified.
- Outliers and missing data were handled for accurate modeling.

---

## 🤖 Models Implemented

1. **XGBoost Regressor**
2. **ARIMA**
3. **LSTM (Long Short-Term Memory)**
4. **Transformer-based model**

Each model was trained on historical temperature data to predict future temperature values.

---

## 📈 Results & Inference

| Model        | MAE   | RMSE  | Accuracy |
|--------------|-------|-------|----------|
| **XGBoost**      | 4.006 | 6.019 | 78.09%   |
| **ARIMA**        | 9.016 | 12.057| 50.69%   |
| **LSTM**         | 3.431 | 4.434 | **85.10%** |
| **Transformer**  | 3.513 | 4.402 | 84.74%   |

### ✅ Inference

- **LSTM** outperformed all other models, achieving the lowest MAE and RMSE and the highest accuracy of 85.10%, making it the most suitable model for this time series forecasting task.
- **Transformer** model followed closely behind, showing strong potential for capturing temporal patterns with high accuracy.
- **XGBoost** performed well for a non-sequential model, achieving 78.09% accuracy, but it lacks the sequential memory advantage of LSTM/Transformer.
- **ARIMA** had the poorest performance among all models, indicating that classical statistical methods may not be sufficient for capturing complex patterns in the temperature data.

➡️ Conclusion: Deep learning models, especially LSTM, are more effective in forecasting temperature trends compared to traditional statistical and tree-based methods in this case.

---

## 💻 How to Run

1. Clone this repo:
   ```bash
   git clone https://github.com/yourusername/temperature-forecasting.git
   cd temperature-forecasting
   ```
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebooks in order:
   - `data_analysis.ipynb`
   - `model_comparison.ipynb`
