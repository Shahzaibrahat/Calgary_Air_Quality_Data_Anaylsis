# Calgary Air Quality Index Analysis

This repository contains the analysis and models for predicting the **Air Quality Index (AQI)** for Calgary. The project includes data gathering, exploratory analysis, and the development of statistical models to reverse engineer the AQI formula. The goal was to understand the factors that contribute to air quality levels in Calgary and predict future air quality.

## Repository Files

This repository contains the following files:

1. **Project Report Calgary Air Quality Analysis.pdf**  
   This report discusses the data sources used for Calgary's air quality index, the methodology employed during the analysis, the hypothesis considered, and the results obtained from the analysis.

2. **Best_Multi_Regression_Model_AirQualityIndex.pdf**  
   This PDF is generated from an R Markdown (`.Rmd`) file and provides a comprehensive overview of the statistical tests and models used in the analysis. It includes steps such as:
   - Finding the best additive regression model.
   - Developing interaction models and higher-order interaction models, which were selected as the final model.
   - Conducting tests like Multicollinearity, Breusch-Pagan Test, Shapiro Test, and Cooks Distance (for outlier detection).
   
   These tests were performed to ensure the validity and robustness of the additive linear regression model used to predict AQI.

3. **Project_Presentation.pdf**  
   This is the presentation document summarizing the project. It includes key findings such as:
   - The best and worst months for air quality.
   - Community-level air quality variations and the factors contributing to poor air quality.
   - The effectiveness of the model in predicting future air quality.
   - The model's performance and confusion matrix, which is displayed in the last couple of slides.

4. **MD_file_Project_Air_Quality.Rmd**  
   This R Markdown file contains the complete workflow of the analysis, including data preprocessing, model development, and hypothesis testing. It generates the PDF containing the regression steps and model summaries used in the final analysis.

## Key Findings

- **Best and Worst Months for Air Quality**:  
  Our analysis showed seasonal variations but **Seasonality did not appear significant** in predicting air quality. The season was excluded from the best additive model.

- **Communities with Best and Worst Air Quality**:  
  It is challenging to generalize which communities have the best and worst air quality due to the complexity of the model. However, **Northwest Calgary** had lower coefficients for AQI, while **Northeast Calgary** had higher AQI values.

- **Factors Contributing to Poor Air Quality**:  
  The following factors were identified as major contributors to poor air quality in Calgary:
  - Carbon Monoxide, Methane, Nitric Oxide, Nitrogen Dioxide, Ozone, Non-methane Hydrocarbons, and PM2.5 Mass.

- **Model Performance in Predicting Air Quality**:  
  The final robust model, with an **Adjusted R-squared ~94%**, provides a strong prediction for AQI. It is especially effective if outliers or irregularities are present in future data. We also generated a **confusion matrix** to evaluate model performance and prediction accuracy.

## Statistical Tests

The following statistical tests were performed on the additive linear regression model:

- **Multicollinearity**: Checked using Variance Inflation Factor (VIF) to ensure that the model does not suffer from multicollinearity issues.
- **Breusch-Pagan Test**: To test for heteroscedasticity in the residuals.
- **Shapiro Test**: To assess the normality of the residuals.
- **Cook's Distance**: To detect influential data points or outliers.

These tests ensured the assumptions of the linear regression model were met and helped refine the final model.

## Conclusion

The project successfully reverse-engineered the AQI formula for Calgary. The final model provides strong predictive power and can be used for forecasting air quality. By analyzing the factors contributing to AQI, this model can help in identifying pollution hotspots and take preventive measures for improving air quality in Calgary.
