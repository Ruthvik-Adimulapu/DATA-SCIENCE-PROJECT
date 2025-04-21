#  Olympic Medal Prediction using Machine Learning

This project utilizes over a century of Olympic data to predict the medal-winning potential of countries using machine learning models such as Logistic Regression, Random Forest, and Gradient Boosting. It also features a Streamlit-based web app for interactive exploration.

## Project Structure

├── data/ │ ├── athlete_events.csv │ └── noc_regions.csv ├── preprocessing.ipynb │ └── modeling.ipynb ├── app/ │ └── streamlit_app.py 
---

##  Dataset Description

- **athlete_events.csv**: Contains individual athlete data from the Summer Olympics (1896–2016).
- **noc_regions.csv**: Maps National Olympic Committee codes to countries/regions.

---

## Preprocessing & Feature Engineering
- Removed missing data (imputation for age/weight/height).
- managed to get the visualisations for the required web application
- Developed various grafs and imported to the pycharm fir the web application
- Aggregated medal counts at country-level per Olympic year.
- Engineered features like:
  - 5-year rolling averages
  - Medal ratios
  - Host nation advantage
  - Event-specific performance trends

---

## Models Used

| Model               | Accuracy | F1 Score | CV F1 Mean | CV Std Dev |
|---------------------|----------|----------|-------------|-------------|
| Logistic Regression | 100%     | 1.000     | 0.999       | 0.002       |
| Random Forest       | 95.4%    | 0.954     | 0.925       | 0.025       |
| Gradient Boosting   | 95.0%    | 0.949     | 0.952       | 0.026       |

> **Note**: SMOTE was used to handle class imbalance.

---

##  Web Application Features

Built with **Streamlit**, the app allows users to:

- Select a country and year
- Input previous medal counts
- Get medal forecasts & historical comparisons
- View probability scores from different models
- Analyze key feature contributions

Run it locally with:

```bash
streamlit run app/streamlit_app.py
eg: Sample Prediction Output

Country: Russia
Year: 2016
Predicted Total Medals: 82
Actual: 115
Probability of Medaling:
Logistic Regression: 99.8%
Random Forest: 97.7%
Gradient Boosting: 86.4%

##References
Chawla et al. (2002) - SMOTE for Imbalanced Data
Pappalardo et al. (2019) - Sports Analytics Using ML
Andreff (2021) - Economic Determinants of Olympic Success
Applications of Expert Systems (IF: 8.5) - Ensemble Methods in Olympic Prediction

Future Improvements

Include Winter Olympics data
Integrate deeper economic/sociopolitical factors
Scale the model for larger datasets
Deploy web app on cloud

In this webapp.py, helper.py, pre-processor.py are used for pycharm and the python jupyter code is stored in DATA SCIENCE PROJECT.pynb
