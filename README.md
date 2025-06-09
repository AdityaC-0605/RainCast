# RainCast

RainCast is a machine learning project for rainfall and weather prediction using NASA/POWER daily meteorological data for Kannur, India. The project leverages feature engineering and a Random Forest Regressor to predict surface shortwave diffuse irradiance as a proxy for rainfall.

## Project Structure

- `Kannur.csv` — NASA/POWER daily weather data for Kannur (1990–2024)
- `train.ipynb` — Main Jupyter notebook for data processing, feature engineering, model training, evaluation, and visualization

## Workflow

1. **Data Loading**  
   Reads and preprocesses the raw CSV data, handling missing values and cleaning the dataset.

2. **Feature Engineering**  
   Adds time-based, cyclical, and weather interaction features to improve model performance.

3. **Model Training**  
   - Splits data into training and testing sets
   - Scales features
   - Trains a Random Forest Regressor with hyperparameter tuning via randomized search

4. **Evaluation & Visualization**  
   - Evaluates model performance (R², RMSE, MAE)
   - Visualizes predictions, residuals, feature importance, and error distribution

## Requirements

- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy
- Jupyter Notebook

Install dependencies with:
```sh
pip install pandas numpy matplotlib seaborn scikit-learn scipy notebook
```

## Usage

1. Place `Kannur.csv` in the project directory.
2. Open `train.ipynb` in Jupyter Notebook or VS Code.
3. Run all cells to preprocess data, train the model, and view results.

## Output

- Model performance summary (R², RMSE, MAE for train/test sets)
- Visualizations: actual vs predicted, residuals, feature importance, error distribution

## Notes

- The target variable is `ALLSKY_SFC_SW_DIFF` (surface shortwave diffuse irradiance), used as a rainfall proxy.
- The notebook is modular and can be adapted for other locations or target variables with similar data.

---

Data Source: NASA/POWER  
Location: Kannur, India (Lat: 11.8757, Lon: 75.3768)

---

Feel free to contribute or adapt RainCast for your own weather prediction needs!