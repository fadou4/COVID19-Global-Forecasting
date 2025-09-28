# COVID19-Global-Forecasting
# 🦠 COVID19-Global-Forecasting

A project for **statistical analysis and machine learning forecasting** of COVID-19 cases and fatalities worldwide.
Built as part of a Master’s project, it applies data preprocessing, regression modeling, and evaluation to predict pandemic evolution.

---

## 🎯 Objectives

* Explore and analyze COVID-19 global datasets
* Clean and preprocess raw data to ensure consistency
* Apply machine learning regression models for forecasting
* Evaluate accuracy with R², MSE, and MAE metrics
* Visualize predictions vs real data to validate the models

---

## 📂 Repository Contents

| File / Folder                             | Description                                                          |
| ----------------------------------------- | -------------------------------------------------------------------- |
| `covid19-global-forecasting-week-4.ipynb` | Main Jupyter Notebook with preprocessing, training, and forecasting. |
| `covide_19.ipynb`                         | Initial data exploration and experiments.                            |
| `SadRapport.pdf`                          | Project report detailing methodology, results, and references.       |
| `.DS_Store`                               | Mac OS system file *(can be ignored)*.                               |

---

## 🛠 Technologies & Tools

* **Python**
* **Jupyter Notebook**
* Libraries:

  * [NumPy](https://numpy.org/doc/)
  * [Pandas](https://pandas.pydata.org/docs/)
  * [Matplotlib](https://matplotlib.org/stable/)
  * [Scikit-learn](https://scikit-learn.org/stable/)

Dataset: COVID-19 global data (Confirmed Cases, Fatalities, Country/Region, Date).

---

## 🔍 Data Exploration

* Dataset shape: **35,995 rows × 6 columns**
* Variables:

  * `ProvinceState`, `CountryRegion`, `Date` (categorical)
  * `ConfirmedCases`, `Fatalities` (numerical)
  * `Id` (removed as irrelevant)
* Insights:

  * `ConfirmedCases` and `Fatalities` distributions are approximately normal
  * Strong correlation between confirmed cases and fatalities
  * US, Italy, Spain, UK, and France showed the highest cases and deaths

---

## 🧹 Preprocessing

* Removed duplicates → dataset remains 35,995 rows × 6 columns
* Dropped `ProvinceState` (57% missing values)
* Aggregated fatalities per `CountryRegion` and `Date` to resolve inconsistencies
* Final cleaned dataset: **21,160 rows × 3 columns**
* Encoding:

  * `CountryRegion` → Label encoding (0 to 183)
  * `Date` → Converted to datetime, then encoded

---

## 🤖 Modeling

* Model: **Random Forest Regressor**
* Parameters: `n_estimators = 300` (number of decision trees)
* Training: split into `X_train, Y_train` and `X_test, Y_test`
* Evaluation results:

  * **R² Score**: 0.9993
  * **Mean Squared Error (MSE)**: 0.1640
  * **Mean Absolute Error (MAE)**: 0.0239
* Visualization showed predicted vs actual values were **very close**, confirming high accuracy.

---

## 📊 Results & Conclusion

* The supervised learning approach achieved **high precision** in forecasting COVID-19 cases.
* Predictions closely matched real data across multiple countries.
* This demonstrates the effectiveness of machine learning for large-scale health data forecasting.

---

## 🚀 Installation & Usage

1. Clone the repo:

   ```bash
   git clone https://github.com/fadou4/COVID19-Global-Forecasting.git
   cd COVID19-Global-Forecasting
   ```

2. Create a virtual environment (recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Open and run notebooks in Jupyter or VS Code.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a new branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m "Add feature"`)
4. Push (`git push origin feature/YourFeature`)
5. Open a Pull Request

---


## 👩‍💻 Authors

* **Fadoua Ounissi** ([fadou4](https://github.com/fadou4))
* Alioua Chaima
* Bouzellifa Nora


---

## 🙏 Acknowledgements

* [NumPy Documentation](https://numpy.org/doc/)
* [Pandas Documentation](https://pandas.pydata.org/docs/)
* [Matplotlib Documentation](https://matplotlib.org/stable/)
* [Scikit-learn Documentation](https://scikit-learn.org/stable/)
* Educational resources & tutorial videos on data analysis and forecasting
