# SAFE-VA: Statistical Analysis and Forecasting of Crime Events in Virginia

## Overview
SAFE-VA is an innovative predictive analytics tool designed to forecast crime rates across neighborhoods in Virginia. Using advanced statistical models and machine learning algorithms, SAFE-VA processes historical crime data along with socio-economic indicators to predict future crime trends. This project aims to aid policymakers, law enforcement, and community planners by providing actionable insights through a data-driven approach.

---

## Features

- **Crime Rate Prediction**: Accurately forecasts crime rates in various Virginia neighborhoods based on key socio-economic factors such as population density, unemployment rates, and education levels.
- **Streamlit Interface**: An intuitive user interface that allows stakeholders to adjust socio-economic variables dynamically and observe how these changes influence crime rates.
- **Modeling Techniques**: Utilizes robust machine learning algorithms, including `RandomForestRegressor`, `GradientBoostingRegressor`, and **Stacking** models, to ensure high prediction accuracy and interpretability.
- **Exploratory Data Analysis (EDA)**: Thorough analysis of crime trends across counties, revealing patterns and correlations between crime rates and socio-economic conditions.
- **Interactive Visualization**: Real-time graphical representations of the predicted crime rates, enabling stakeholders to explore the impact of changes in various socio-economic indicators.

---

## Research Motivation
1. **Crime Impact Mitigation**: Develop strategies that reduce crime rates effectively by identifying key factors influencing crime dynamics.
2. **Data-Driven Policy Making**: Empower policymakers with predictive insights that support proactive public safety measures and efficient resource allocation.
3. **Community Safety Enhancement**: Equip communities with data that informs safety interventions and fosters collaboration between local authorities and residents.

---

## Dataset

SAFE-VA uses multiple datasets to analyze crime trends:
- **FBI Uniform Crime Reporting (UCR)**: Detailed county-level crime data.
- **US Department of Labor**: Unemployment rates by county.
- **Data.gov**: School enrollment and population statistics.

### Key Data Attributes
- **Crime Categories**: Murder, rape, robbery, aggravated assault, burglary, larceny-theft, motor vehicle theft.
- **Socio-Economic Variables**: Population size, unemployment rate, educational enrollment (Pre-K, K-5, 6-8, 9-12).

---

## Methodology

### Data Preparation
- **Normalization**: Consistent scaling of numerical variables using `StandardScaler`.
- **Categorical Encoding**: Converted categorical variables (e.g., county) using `OneHotEncoder` for effective ML modeling.
- **Outliers**: Treated using Z-scores and the Interquartile Range (IQR) to prevent skewed analysis.

### Modeling Approach
- **RandomForestRegressor**: Combats overfitting and handles non-linear relationships.
- **GradientBoostingRegressor**: Strong predictive power and flexibility in optimization.
- **Stacking Ensemble**: Combines multiple models for improved prediction accuracy by leveraging the strengths of each base learner.

---

## Results

- **Model Accuracy**: Stacking model achieved the best performance with the lowest **MSE** and **MAE** compared to RandomForest and GradientBoosting.
- **Insights from EDA**:
  - Strong correlations between unemployment rates and property crimes.
  - Higher population densities often linked with increased violent crime rates.
  - Disparities in crime patterns across counties tied to local socio-economic conditions.

---

## Application Interface

SAFE-VA’s Streamlit-based interface provides an interactive, user-friendly experience:
- **Interactive Controls**: Sliders and dropdowns to toggle variables like unemployment rate and population density.
- **Real-Time Feedback**: Immediate visualization of crime predictions as users adjust inputs.
- **Graphical Representations**: Bar charts for easy comparison of predicted crime rates.

### How to Use
1. Launch the Streamlit app.
2. Adjust input variables (e.g., population, unemployment rate).
3. View updated crime rate predictions in real-time.

---

## Limitations and Future Work

### Limitations
- **Data Coverage**: Predictions constrained by availability and recency of socio-economic and crime data for certain years and counties.
- **Generalizability**: Reduced reliability in counties with limited or missing data.

### Future Work
- **Data Expansion**: Incorporate real-time feeds and additional socio-economic features.
- **Refined UI**: Add more interactive visualizations and scenario planning.
- **Community Engagement**: Make insights accessible to communities to foster collaboration with local authorities.

---

## Tech Stack
- **Data Scraping**: Python (`BeautifulSoup`, `requests`)
- **Data Analysis**: Python (`pandas`, `numpy`)
- **Modeling**: `scikit-learn`, `TensorFlow`
- **User Interface**: `Streamlit`

---

## How to Run the Project

### Prerequisites
- Python 3.7+
- Streamlit
- scikit-learn
- pandas
- TensorFlow

### Installation
```bash
git clone https://github.com/Spandana-28/SAFE-VA.git
cd SAFE-VA
pip install -r requirements.txt


### Running the Application
To run the Streamlit app:
```bash
streamlit run streamlit_model.py
```

## Author
Spandana Meker Kuberappa — Data Collection, Analysis, Model Building & UI Development

## References
- FBI Uniform Crime Reporting (UCR): https://www.fbi.gov/how-we-can-help-you/more-fbi-services-and-information/ucr
- Data.gov Census Data: https://www.data.gov/
- Streamlit Documentation: https://streamlit.io/
- Pandas Documentation: https://pandas.pydata.org/
- scikit-learn Documentation: https://scikit-learn.org/
- TensorFlow Documentation: https://www.tensorflow.org/
