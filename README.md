# NASDAQ Quarterly Performance Analysis

This project analyzes historical NASDAQ data to uncover key economic indicators, seasonal trends, and influential factors affecting NASDAQ’s performance. Using a combination of machine learning, data visualization, and statistical analysis, this project provides stakeholders with actionable insights and predictive assessments for future quarterly trends.

## Project Objectives
The primary objectives of this project are:
1. To identify the economic factors with the largest impact on NASDAQ performance.
2. To understand seasonal quarterly performance patterns.
3. To predict future NASDAQ quarterly performance using machine learning models.
4. To communicate insights in a way that aids strategic decision-making.

## Dataset Description
The project uses `nasdq.csv` as the main dataset, which includes the following columns:
- **Date**: The date of each entry.
- **Open, High, Low, Close**: Daily NASDAQ prices, showing market behavior within each day.
- **Volume**: Number of shares traded on a given day.
- **Interest Rate**: The prevailing interest rate at the time.
- **Exchange Rate**: The exchange rate of USD against other currencies.
- **VIX**: Volatility Index, a measure of market risk and investor sentiment.
- **TED Spread**: Difference between interest rates on interbank loans and U.S. government debt, an indicator of market risk.
- **EFFR**: Effective Federal Funds Rate, which reflects monetary policy.
- **Gold, Oil**: Prices of gold and oil, representing commodities that influence the market.

These attributes provide a comprehensive view of economic indicators and NASDAQ’s performance metrics.

## Methodology

1. **Data Preparation**:  
   Data was loaded from `nasdq.csv`, resampled to quarterly frequency, and aggregated. Missing values were filled, and target variables for machine learning were created based on quarterly Close price changes.

2. **Exploratory Data Analysis (EDA)**:  
   - Histograms of key indicators were generated to visualize data distributions.
   - Seasonal patterns in quarterly performance were analyzed.
   - A feature importance analysis was conducted using a Random Forest model.

3. **Machine Learning**:  
   - A Random Forest Classifier was trained to predict NASDAQ quarterly performance.
   - The model’s feature importance scores provided insights into which factors most influence NASDAQ changes.

4. **Visualizations**:  
   - **Quarterly Trends**: Analyzed seasonal performance over time to identify high-performing quarters.
   - **Feature Importance**: Displayed the influence of each factor on NASDAQ using an exploded pie chart for the top three indicators.
   - **Historical vs. Projected Performance**: Showed historical Close prices and projected trends for the next 10 quarters using linear regression.

## Key Insights
- **Quarterly Performance Patterns**:  
  Certain quarters have consistently shown stronger performance, allowing stakeholders to anticipate seasonal trends.
  
- **Influential Economic Indicators**:  
  The analysis identified **Interest Rate**, **VIX**, and **TED Spread** as the primary drivers of NASDAQ performance, based on feature importance from the Random Forest model.

- **Predictive Projections**:  
  A linear regression model projected steady growth in NASDAQ for the next 10 quarters. This projection highlights the importance of monitoring key indicators to anticipate potential corrections or shifts.

## Usage Instructions

1. **Requirements**:  
   Ensure you have Python 3.x installed, along with the following packages:
   - `pandas`
   - `numpy`
   - `matplotlib`
   - `seaborn`
   - `scikit-learn`

2. **Running the Notebook**:  
   - Open the Jupyter Notebook file (`charlieNasdaq.ipynb`) in Jupyter Notebook or Jupyter Lab.
   - Run each cell sequentially to load data, process it, train models, and generate visualizations.

3. **File Structure**:
   - `nasdq.csv`: The main dataset with historical NASDAQ and economic data.
   - `charlieNasdaq.ipynb`: The main project notebook containing all code, analyses, and visualizations.

4. **Viewing Insights**:  
   - The notebook provides insights in both textual and visual formats. Key findings and recommendations are included to help stakeholders make data-driven decisions based on the analysis.

## Future Improvements

To enhance this analysis further:
- **Explore Time-Series Models**: Consider using models like ARIMA or Prophet to capture more nuanced time-series patterns.
- **Add More Economic Indicators**: Incorporating additional economic indicators could improve prediction accuracy.
- **Experiment with Different Models**: Testing other machine learning algorithms, such as Gradient Boosting or SVM, could provide additional perspectives on the data.

## Conclusion

This NASDAQ analysis project provides stakeholders with a robust framework for understanding and predicting market trends. By leveraging historical data, economic indicators, and machine learning models, this project delivers insights into quarterly performance patterns and key factors influencing NASDAQ. Stakeholders can use these insights to inform investment strategies, anticipate potential risks, and make data-driven decisions for future quarters.
