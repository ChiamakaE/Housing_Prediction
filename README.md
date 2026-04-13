<h1>NULL HYPOTHESIS</h1>
<li> There is no statistically significant relationship between the bedrooms and the price of the houses.</li>
<li>There is no statistically significant relationship between the bathrooms and the price of the houses.</li>
<li>There is no statistically significant relationship between the sqft_living ( The square footage of the interior housing space that is above ground level) and the price of the houses.</li>
<li>There is no statistically significant relationship between the sqft_lot (THe square footage of the interior housing space that is below ground level) and the price of the houses.</li>
<li>There is no statistically significant relationship between the floors and the price of the houses.</li>
<li>There is no statistically significant relationship between the waterfront and the price of the houses.</li>
<li>There is no statistically significant relationship between the view and the price of the houses.</li>
<li>There is no statistically significant relationship between the condition and the price of the houses.</li>
<li>There is no statistically significant relationship between the grade and the price of the houses.</li>
<li>There is no statistically significant relationship between the sqft_above and the price of the houses.</li>
<li>There is no statistically significant relationship between the sqft_basement and the price of the houses.</li>
<li>There is no statistically significant relationship between the yr_built and the price of the houses.</li>
<li>There is no statistically significant relationship between the yr_renovated and the price of the houses.</li>
<li>There is no statistically significant relationship between the zipcode and the price of the houses.</li>
<li>There is no statistically significant relationship between the lat and the price of the houses.</li>
<li>There is no statistically significant relationship between the long and the price of the houses.</li>
<li>There is no statistically significant relationship between the sqft_living15(The square footage of interior housing living space for the nearest 15 neighbors) and the price of the houses.</li>
<li>There is no statistically significant relationship between the sqft_lot15(The square footage of the land lots of the nearest 15 neighbors) and the price of the houses.</li>


<h1>Research Question</h1>
<li>What is the relationship between the number of bedrooms and the price of a house?</li>
<li>Does the size of the living area (sqft_living) impact the price of a house?</li>
<li>Are there any significant correlations between variables like condition, grade, and the price of houses?</li>
<li>How do other variables like waterfront, view, and location (zipcode) affect house prices?</li>


<h1>Tests of Normality</h1>
<li>The p-value (Sig.) is less than your chosen alpha level -0.05,p-values for all variables (all .000), it appears that the data significantly deviates from a normal distribution for each variable.</li>

<li>All the variables in your table have very low p-values, suggesting that they do not follow a normal distribution. </li>
<img width="584" height="1015" alt="image" src="https://github.com/user-attachments/assets/a4c40b51-0b1a-4ab1-a1de-ef8283cd2a5c" />


<h1>Descriptive Statistics for numerical Variables</h1>
<li>Price has a very high positive kurtosis of 34.522, indicating heavy-tailed data with many extreme values.</li>
<li>Other variables like sqft_living, sqft_lot, sqft_above, etc., also have positive kurtosis values, suggesting heavy-tailed distributions.</li>
<img width="1353" height="706" alt="image" src="https://github.com/user-attachments/assets/e0593616-aaf4-4de2-86f5-30e13f36867f" />


<li>
Significance levels (Sig. or p-values) indicate whether the correlation is statistically significant. In the table, there are two levels of significance: 0.01 (very significant) and 0.05 (significant).
A smaller p-value (e.g., 0.000) indicates a more significant correlation, while a larger p-value (e.g., 0.05) suggests a less significant or non-significant relationship.</li>
<img width="1593" height="1113" alt="image" src="https://github.com/user-attachments/assets/27ebaae2-be92-4253-aed2-4206d88eebb0" />


<li>For example</li>
The Pearson correlation coefficient between the number of bedrooms and house prices was 0.308. Additionally, the two-tailed significance (Sig.) value associated with this correlation was 0.000, which is statistically significant.
The positive correlation coefficient of 0.308 suggests a moderate positive relationship between the number of bedrooms in a house and its price. In other words, as the number of bedrooms in a house increases, the house price tends to increase as well. This finding indicates that larger houses with more bedrooms tend to command higher prices in the housing market.
<img width="8797" height="543" alt="image" src="https://github.com/user-attachments/assets/5effe619-7198-4288-b7ce-0167a88f9fc3" />

<li>Multiple linear regression analysis is done with the dependent variable "price" and multiple independent variables. To determine whether to accept or reject the null hypothesis for each independent variable, focus on the "Sig." (Significance) column in the Coefficients table.</li>

<h3>For example</h3>
<li>Bathrooms:</li>The coefficient for "bathrooms" is 41276.711 with a very low p-value of .000. This indicates that the number of bathrooms has a statistically significant and positive effect on the price. In other words, as the number of bathrooms increases, the price tends to increase. Therefore, you should reject the null hypothesis for "bathrooms."
 
<li> sqft_lot:</li> The coefficient for "sqft_lot" is 0.125 with a p-value of .009. This indicates that the square footage of the lot has a statistically significant but relatively weak positive effect on the price. Therefore, you should reject the null hypothesis for "sqft_lot." 
<img width="5280" height="261" alt="image" src="https://github.com/user-attachments/assets/a254efd6-1c06-4479-aafb-dc2aff233716" />





<img width="1802" height="981" alt="image" src="https://github.com/user-attachments/assets/2afa0283-cee9-4aac-aca0-3d6afe8a70b1" />

- R: The correlation coefficient (R) measures the strength and direction of the linear relationship between the dependent variable (price) and the independent variables collectively. In this model, R is 0.837, which suggests a strong positive linear relationship between the independent variables and the dependent variable.

- R Square: R Square, or the coefficient of determination, represents the proportion of the variance in the dependent variable (price) that is explained by the independent variables in the model. In this case, R Square is 0.701, which means that approximately 70.1% of the variance in the price can be explained by the independent variables in the model.

- Adjusted R Square: Adjusted R Square is similar to R Square but adjusted for the number of predictors in the model. It provides a more conservative estimate of the variance explained. In this model, it's also 0.701, which suggests that the inclusion of these independent variables explains a substantial amount of the variation in price.

- Std. Error of the Estimate: This value (200880.07723) is a measure of the variability of the actual values of the dependent variable (price) around the predicted values. Lower values indicate better model fit.

- Change Statistics: This section reports the change in R Square, F-statistic, and other statistics when the model is tested. The F Change statistic tests whether the addition of independent variables significantly improves the model. In this case, the F Change statistic is 2815.816, and the associated p-value is very close to zero, indicating that adding the independent variables to the model significantly improved its fit.

- Durbin-Watson: The Durbin-Watson statistic (1.266) is used to test for the presence of autocorrelation in the residuals (errors) of the model. It ranges from 0 to 4, with values around 2 indicating no autocorrelation. In this case, the value is below 2, suggesting a potential issue with autocorrelation.


- R: The correlation coefficient (R) measures the strength and direction of the linear relationship between the dependent variable (price) and the independent variables collectively. In this model, R is 0.837, which suggests a strong positive linear relationship between the independent variables and the dependent variable.

- R Square: R Square, or the coefficient of determination, represents the proportion of the variance in the dependent variable (price) that is explained by the independent variables in the model. In this case, R Square is 0.701, which means that approximately 70.1% of the variance in the price can be explained by the independent variables in the model.

- Adjusted R Square: Adjusted R Square is similar to R Square but adjusted for the number of predictors in the model. It provides a more conservative estimate of the variance explained. In this model, it's also 0.701, which suggests that the inclusion of these independent variables explains a substantial amount of the variation in price.

- Std. Error of the Estimate: This value (200880.07723) is a measure of the variability of the actual values of the dependent variable (price) around the predicted values. Lower values indicate better model fit.

- Change Statistics: This section reports the change in R Square, F-statistic, and other statistics when the model is tested. The F Change statistic tests whether the addition of independent variables significantly improves the model. In this case, the F Change statistic is 2815.816, and the associated p-value is very close to zero, indicating that adding the independent variables to the model significantly improved its fit.

- Durbin-Watson: The Durbin-Watson statistic (1.266) is used to test for the presence of autocorrelation in the residuals (errors) of the model. It ranges from 0 to 4, with values around 2 indicating no autocorrelation. In this case, the value is below 2, suggesting a potential issue with autocorrelation.

Overall, this Model Summary table provides essential information about the quality of your regression model. An R Square of 0.701 indicates that the model explains a substantial portion of the variance in the dependent variable. The low p-value associated with the F Change statistic indicates that the model is statistically significant. However, you should also consider the issue of autocorrelation indicated by the Durbin-Watson statistic, as this can impact the validity of the model's assumptions.
<img width="13506" height="1100" alt="image" src="https://github.com/user-attachments/assets/069e0ff0-21c8-4acc-af26-dee5e94d61f8" />

Overall, this Model Summary table provides essential information about the quality of your regression model. An R Square of 0.701 indicates that the model explains a substantial portion of the variance in the dependent variable. The low p-value associated with the F Change statistic indicates that the model is statistically significant. However, you should also consider the issue of autocorrelation indicated by the Durbin-Watson statistic, as this can impact the validity of the model's assumptions.


