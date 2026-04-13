



Table of Contents
1 Statistical Data Analysis	1
1.2 Domain Understanding	1
1.3 Research questions	2
1.4 Descriptive analysis	2
1.4.1 Descriptive Analysis for Price	2
1.4.2 Descriptive Analysis for the categorical variables	2
1.5 Data Set and Data Preparation	7
1.5.1 Automatic Recode	7
1.5.2 Finding Missing Values	8
1.5.2 Handling Missing Values	9
1.5.3 Identifying Duplicate Values	9
1.5.4 Detecting Outliers	10
1.5.5 Handing Outliers	10
1.5.6 Removing Outliers	11
1.6 Test for Normality	13
1.6.1 Hypothesis for Normality	14
1.6.2 Interpretation of the Kolmogorov-Smirnov	14
1.6.3 Interpretation of the P-P Plot	15
1.7 Data Analytical Methods	15
1.7.1 Hypothesis for Research Question A	16
1.7.2 Hypothesis for Research Question (B)	16
1.7.3 Reason for Using the Selected Test	20
1.8 Evaluation and Conclusion	20
1.8.1 Research Question A	20
1.8.2 Analysis for the research question A	20
1.8.3 Research Question B	22
1.8.4 Automatic Linear Modelling	23
1.8.5 Interpretation of Figure 12	24
SECTION 2: Data Modelling	26
2.1 Interpretation of the Entity-Relationship Diagram	27
2.2 Entity Relationship	27
2.3 Creating and Populating the Table/Entities using SQL	30
3. Business Scenarios	39
3. 1 Business Scenario 1:	39
3.2 Business Scenario 2:	40
3.3 Business Scenario 3:	41
References	42



Table of Figures
Figure 1:Bar Chart for Property Type	3
Figure 2: Bar Chart for New Build	4
Figure 3: Automatic Recode of the Variables	8
Figure 4: Boxplot for price paid	10
Figure 5: Histogram showing Price Paid Distribution before handling outliers	11
Figure 6:Creating Z-Score from Price Paid	12
Figure 7: Histogram displaying Price Paid Distribution After removing the Outliers	12
Figure 8:Price Paid shown on a Box Plot After removing outlier	13
Figure 9:P-P plot of Regression Standardized Residual	15
Figure 10: Mean for Price Paid	21
Figure 11: Automatic Linear Modelling	23
Figure 12: Features that determine Price Paid based on their Importance.	24
Figure 13: Entity relationship (ER) diagrams of the Amazon Database	26
Figure 14: Cardinal Relationship between Customer and Order	27
Figure 15: Cardinal Relationship between Product and Order Item	28
Figure 16: Cardinal Relationship between Review and product	28
Figure 17: Cardinal Relationship between Product and Vendor	29
Figure 18: Cardinal Relationship between Order and Order Item	29
Figure 19: Cardinal Relationship between Customer and Review	30
Figure 20: Screenshot of the Customer Table Schema	31
Figure 21: SQL Query for Customer	31
Figure 22: Record Value from the Customer Table	31
Figure 23: Screenshot of the Product Table Schema	32
Figure 24: SQL Query to insert into the Product Table	32
Figure 25: Record Value from the Product Table	33
Figure 26: Screenshot of the Order Table Schema	34
Figure 27: SQL Query to Insert Values to Orders Table	34
Figure 28: Result Output for the Orders Table	34
Figure 29: Screenshot of the Vendor Table Schema	35
Figure 30: SQL Query to Insert Values in Vendor Table	35
Figure 31: Record Value from for the Vendor Table	36
Figure 32: SQL Query Order Item Table Schema	36
Figure 33:SQL Query for Order Item Table	37
Figure 34: Record Value from the Order Item Table	37
Figure 35:Screenshot of the Review Table Schema	38
Figure 36: SQL Query to Insert values to Review Table	38
Figure 37: Record Value from the Review Table	39
Figure 38:SQLCommand for Business Scenario 1	39
Figure 39: Result for Business Scenario 1	39
Figure 40: SQL for Business Scenario 2	40
Figure 41: Result for Business Scenario 2	40
Figure 42: SQL Command for Business Scenario 3	41
Figure 43: Result for Business Scenario 3	41


Tables of Tables
Table 1: Descriptive Analysis for Price	2
Table 2:Descriptive Analysis for Property Type	3
Table 3:Descriptive Frequency for new build	4
Table 4:Descriptive Frequency for Estate Type	5
Table 5: Descriptive Frequency for District	6
Table 6: Descriptive Frequency for County	7
Table 7:Descriptive Frequency for Town	7
Table 8: Missing Value Analysis	9
Table 9:Duplicate data	10
Table 10:Normality Test	14
Table 11: Kruskal-Wallis Test	16
Table 12: Mann-Whitney U Test for Analysing Price and New Build	16
Table 13: Kruskal Wallis Test for Analysing Price and Estate Type	17
Table 14: Kruskal-Wallis Test Analysing Price and Property Type	17
Table 15: Spearman Correlation analysing price paid and District	18
Table 16: Spearman Correlation analysing price paid and deed date	19
Table 17: Spearman Correlation for analysing price paid and postcode	19
Table 18: Descriptive Frequency Statistics for Price Paid Mean	21

 
 
1 Statistical Data Analysis
1.2 Domain Understanding
May et al (2011) conduct determinants of residential property values in South London using a hedonic multiple regression model. Results show that proximity to High Voltage Overhead Transmission Lines (HVOTL) and being part of a terrace negatively impact property values, while detached houses have higher values. Interactions among determinants lead to ambiguous effects, with public parks positively influencing distant houses but not those near pylons. Elasticities and distance analysis highlight relationships between determinants and property values, emphasizing significant connections between both.

Ebru and Eban (2011) investigate the factors influencing house prices in Istanbul through a quantile regression approach. Utilizing quantile regression methods, the researchers explore the connection between housing prices and diverse housing characteristics in the city. The results indicate that several factors, including the age of the property, the presence of cable TV, security features, heating systems, the existence of a garage, the size of the kitchen area, and an augmentation in the number of rooms and bathrooms, have a positive impact on house prices.

(Sivitanides Petros Stavrou, 2018) conducts a study by uses error-correction and partial-adjustment models to evaluate the effects of major macroeconomic forces on London property prices from 1983 to 2016. The results show a strong long-term correlation between key macroeconomic factors, such as the UK GDP, the population of London, the number of completed housing units, and London property prices. The study refutes the claim that user demand has become less of a factor in the inflation of home prices and offers insightful information about the workings of the housing market. The methodology that was used is in line with accepted practices in the literature, which broadens our understanding of the variables affecting the affordability of property in London and clarifies the ongoing discussion in the area.

The research conducted by Sibel Selim(2008) focuses on real estate valuation and housing conduct research focuses on real estate valuation and housing market analysis, utilizing a hedonic model grounded in microeconomic theory to assess house prices and rental values. The study, based on the 2004 Household Budget Survey Data in Turkey, identifies critical variables influencing house prices, including type of house, building type, number of rooms, size, and structural features like water systems, pools, and natural gas.



1.3 Research questions

A.	Which London District offers properties with the highest, middle, and lowest prices?
B.	What are the most important features that determine the price of the property in this data? 


1.4 Descriptive analysis
1.4.1 Descriptive Analysis for Price
Based on dataset, the total number of data is 17547, the minimum price paid for houses in London is $100 and maximum price is $140,000,000. The dataset is positively skewed, this indicates that the tail on the right side of the probability density function is longer than the left side and the bulk of the values lie to the left of the mean(Naik and Abraham, 2013).
According to Groeneveld and Meeden (1984), kurtosis measures “tailedness” of the distribution and higher values indicates heavier tails. The kurtosis has a relative high value of 1521, which indicates heavier tails. The descriptive analysis for price is displayed in Table 1


Table 1: Descriptive Analysis for Price
 

1.4.2 Descriptive Analysis for the categorical variables
1.	Property Type
The Descriptive Analysis for property type is displayed in Table 2. Majority of the houses fall under the category Flat/Maisonette accounting for 58.7% of the total. with the least property type in the data set as Detached comprising only of   2.2%.





Table 2:Descriptive Analysis for Property Type
 


 
Figure 1:Bar Chart for Property Type


2.	New Build
The distribution of the "new_build" variable is shown in Table 3, showing 1% of the houses are new buildings and 99% are not.

Table 3:Descriptive Frequency for new build
 


 
Figure 2: Bar Chart for New Build

3.	Estate Type
Table 3 shows the distribution of the "estate_type" variable among the properties. It shows that 38.1% of the properties are classified as "FREEHOLD," while 61.9% are classified as "LEASEHOLD" estate types.







Table 4:Descriptive Frequency for Estate Type

 


4.	District
The district with the highest percentage of properties is Wandsworth, accounting for 9.0% of the total.
Other districts with significant percentages include Lambeth (6.5%), the City of Westminster (5.7%), Greenwich, and Waltham Forest (5.5%).
Districts like Kingston upon Thames, Bexley, and City of London have relatively low percentages





















Table 5: Descriptive Frequency for District
 




5.	County
The County column summarized in Table 6 has one value which is Greater London
 
Table 6: Descriptive Frequency for County

 

6.	Town
The Town column which is summarized Table 7 has one value which is London 

Table 7:Descriptive Frequency for Town
 

1.5 Data Set and Data Preparation
1.5.1 Automatic Recode 
To find the missing values, the string values was recoded to numeric values as SPSS does not recognize blank cells in non-numeric columns as missing values (IBM, 2023). The Automatic Recode is applied in this case as shown in Figure 3.

 
Figure 3: Automatic Recode of the Variables
1.5.2 Finding Missing Values
The Missing Value analysis was used to find the missing value in the dataset and is displayed Table 8. Locality and postcode are the only variable with missing data












Table 8: Missing Value Analysis

 

1.5.2 Handling Missing Values
There are several ways of handling missing data in a dataset including data deletion, weighting, and imputation (Haukoos and Newgard, 2007). In all three, the dataset is altered through the addition, deletion, or modification of parameter values. 

Based on the statistics above in Table the Locality and Postcode column contains missing values. The Locality column will not be used in the analysis as 93.7% of the data are missing. While the missing values in the postcode code was replaced with the value “Nil” in the report.
1.5.3 Identifying Duplicate Values
 Based on the information in Table 9, there are no duplicate data.

Table 9:Duplicate data
 


1.5.4 Detecting Outliers
In SPSS, outliers can be detected in the data through a scatterplot, box-plot, or by looking at quantile-to-quantile (QQ) plot (Mat Roni and Djajadikerta, 2021). For this report the box plot was used to detect the outliers. There are several outliers in the “price paid” variable as shown in Figure 2. 

 

Figure 4: Boxplot for price paid
1.5.5 Handing Outliers
According to Kwak and Kim (2017) Trimming, Winsorization and Robust estimation method are ways of handling outliers.  Z-score is also commonly used to handle outliers in a dataset (Benallal et al., 2022). For this report, Z score is applied to trim the extreme values Figure 5 shows a price paid variable in a histogram which barely shows values

However, the Z-score is applied to remove the extreme values to improve the shape of the price paid displayed on the histogram

 
Figure 5: Histogram showing Price Paid Distribution before handling outliers
1.5.6 Removing Outliers
The standard value utilized for identifying outliers is an absolute value of ±3.29 (Mowbray, Fox-Wasylyshyn and El-Masri, 2019). In other words, any z-score above +3.29 or below −3.29 is considered as an outlier. The price variable is converted to Z-score and arranged in both ascending and descending manner to determine if any of the cases are outliers


 

Figure 6:Creating Z-Score from Price Paid


After Removing the outliers from Price Paid the histogram and box plot are shown below
 
Figure 7: Histogram displaying Price Paid Distribution After removing the Outliers

 

Figure 8:Price Paid shown on a Box Plot After removing outlier
From Figure 8, it is clear that the outliers still exist in Price Paid but taking out those percentage of outliers shown in the outliers will distort the analysis. However, we can see from Figure 7 that there was an improvement in the shape of the Price Paid histogram. 

1.6 Test for Normality
Given that parametric testing relies on the assumption of normal data, evaluating the normality of the data is a prerequisite for many statistical tests (Hatem et al., 2022).
In multiple regression, the assumption requiring a normal distribution applies only to the residuals (Statistics Solutions, 2013). 
The Kolmogorov-Smirnov (K-S) test and the Shapiro-Wilk test are the primary tests used to evaluate normality (Derya et al 2006). 
According to Mishra et al. (2019), the Kolmogorov-Smirnov (K-S) test is generally used for large sample sizes, while the Shapiro-Wilk test is more suitable for smaller sample sizes


1.6.1 Hypothesis for Normality
The hypothesis for normality is 
•	Null Hypothesis (H0): The data follows a normal distribution.
•	Alternative Hypothesis (H1): The data does not follow a normal distribution.

Table 10:Normality Test

 



1.6.2 Interpretation of the Kolmogorov-Smirnov
The p-value is compared to the significance level, to determine if the null hypothesis in the normality test will be rejected or accepted. The common threshold values for statistical significance include 0.01,0.05 and 0.001(Rebecca Bevans, 2020). A significant level of 0.05 is used in this analysis. From the result of the normality test in Table 10, the distribution is not normally distributed, as shown by the rejection of the null hypothesis and the p-value of the standardized and unstandardized residuals being less than 0.05.  

 
Figure 9:P-P plot of Regression Standardized Residual
1.6.3 Interpretation of the P-P Plot
A Normal P-P plot is a graphical method that is used to check for normality. In order to be considered normally distributed, the dots should follow the line as closely possible (Ghasemi and Zahediasl, 2012). Further evidence that the data are not normally distributed is provided by the diagram in Figure 9.

Non-parametric methods are recommended for the analysis for data does that are not normally distributed.(Shengping Yang and G. Berdine, 2004). Since the data significantly deviates from normality, non-parametric tests is used for the analysis

1.7 Data Analytical Methods
The following Research Question are answered at the end of this analysis
A.	Which London District offers properties with the highest, middle, and lowest prices?
B.	What are the most important features that determine the price of the property in this data? 

1.7.1 Hypothesis for Research Question A
•	Null Hypothesis (H0): There is no significant difference in property prices among different London districts.
•	Alternative Hypothesis (H1): There is a significant difference in property prices among different London districts.

Table 11: Kruskal-Wallis Test
  
Significance Level:
A significant level of 0.05 is used in this analysis. It is statistically significant as the p-value is less than 0.05

Decision
The null hypothesis is rejected based on the Kruskal-Wallis test result in Table 11, where the p-value is less than 0.05.

Interpretation:
This indicates that the distribution of price_paid significantly varies across different categories of district 

1.7.2 Hypothesis for Research Question (B)	
Table 12: Mann-Whitney U Test for Analysing Price and New Build
 

Price and New Build Status:
(H₀): There is no significant relationship between new build status and the price paid for residential properties.
 (H₁): There is a significant relationship between new build status and the price paid for residential properties.

According to the Mann–Whitney U test result in Table 12, p-value < 0.05, the decision is to reject the null hypothesis. It indicates that there is significant relationship between the price paid and new Build.


Table 13: Kruskal Wallis Test for Analysing Price and Estate Type
 

Price and Estate Type:
(H₀): There is no significant relationship between estate type and the price paid for residential properties.
 (H₁): There is a significant relationship between estate type and the price paid for residential properties

From the Kruskal Wallis test result in Table 13, the p-value < 0.05. The decision is to reject the null hypothesis. This indicates that there is significant relationship between price paid and estate type.
Table 14: Kruskal-Wallis Test Analysing Price and Property Type
 


Price and Property Type:
(H₀): There is no significant relationship between property type and the price paid for residential properties.
 (H₁): There is a significant relationship between property type and the price paid for residential properties.
From the result in Table 14 the p-value is less than 0.05, the decision is to reject the null hypothesis. This suggests that there is significant relationship between price paid and property type


Table 15: Spearman Correlation analysing price paid and District
 

Price and District:
(H₀): There is no significant relationship between district and the price paid for residential properties.
(H₁): There is a significant relationship between district and the price paid for residential properties.

From the results in Table 15, p-value <0.01, therefore the null hypothesis is rejected. This therefore suggests that there is a statistically significant relationship between district and price paid.
 





Table 16: Spearman Correlation analysing price paid and deed date
 

Price and Deed Date
(H₀): There is no significant relationship between deed date and the price paid for residential properties.
(H₁): There is a significant relationship between deed date and the price paid for residential properties.
In Table 16, the Spearman Correlation analysis has a p-values < 0.01, therefore the null hypothesis is rejected. This indicates a significant relationship between deed_date and price_paid. 

Table 17: Spearman Correlation for analysing price paid and postcode
 

Price and Post Code
(H₀): There is no significant relationship between postcode and the price paid for residential properties.
 (H₁): There is a significant relationship between postcode and the price paid for residential properties.

The Spearman Correlation analysis in Table 17 has a p-values < 0.01, therefore the null hypothesis is rejected. This indicates a significant relationship between Post_code and price_paid. 
1.7.3 Reason for Using the Selected Test 
1. Spearman's rank correlation: 
The Spearman's rank correlation coefficient test was selected because it is a non-parametric measure of statistical dependence between two variables(Jan W. Gooch, 2006). The ranked correlation between two variables is measured using Spearman's Rank correlation. It computes the degree and direction of correlation between two ranking variables. (Vidanage et al., 2020).

The correlation between the two variables is significant if it is less than or equal to the alpha value that is selected for the study (Saul Mcleod, 2023).

2. Kruskal-Wallis Test:
It is a nonparametric statistical test that evaluates the variations in one non-normally distributed continuous variable between three or more independently sampled groups (McKight and Najab, 2010).

1.8 Evaluation and Conclusion
1.8.1 Research Question A
Which London District offers properties with the highest, middle, and lowest prices?

Before answering the research question for A one hypothesis was formulated and the Kruskal-Wallis Test was used for the analyses in Section 1.71. 
1.8.2 Analysis for the research question A
The Aggregate Data function is used and the mean value is calculated for the price paid and the break Variable is District
 
Figure 10: Mean for Price Paid
A Descriptive Frequency Statistics is done on the Price Paid Mean Value to determine the Highest lowest and median Value. This is displayed in Table 18

Table 18: Descriptive Frequency Statistics for Price Paid Mean
	District	Value
Lowest 	Croydon	412380.85
Middle	Ealing	730800.5978
Highest	Kensington And Chelsea	1761086.97


From the result, the district with the lowest price is CROYDON, Highest price is Kensington and Chelsea and Middle value is Ealing 


1.8.3 Research Question B
What are the most important features that determine the price of the property in this data? 
Before answering this research question six different hypothesis were formulated and corresponding analyses were done. This helps to provides a specific, testable prediction that guides the research (Lagodiienko, Ivanchenkova and Ivanchenkov, 2022)

 From the result in Section 1.7.2, the selected features are statistically significant therefore they would be used in the analysis

Automatic linear modelling will be used to determine the most important features that determine the price of the property in this data. The model selection method used is the Forward Stepwise. 

Forward stepwise is a systematic approach to feature selection that begins with a blank set of features and iteratively adds the most important characteristics to the model. This aids in determining the key elements for dimensionality reduction(Fong and Xu, 2021).

The following features were excluded from the hypothesis and would also be excluded for the linear modelling based on the following reason: 
•	Street –It has a lot of unique variables. Including it in the study may compromise the analysis's validity and impact how the findings are interpreted
•	Town- It has only one variable
•	County – It has only one variable
•	Unique ID: This variable has a lot of unique values and is likely an identifier for each property. While it is important for tracking and referencing individual properties, it may not directly contribute to understanding the factors that determine property prices.
•	Locality: This feature has a 93.7% missing data


1.8.4 Automatic Linear Modelling
In Figure 11, variables not used are in the fields column, the independent variables are in the predictors input, and the dependent variable is in the Target column
 

Figure 11: Automatic Linear Modelling






 
Figure 12: Features that determine Price Paid based on their Importance.
1.8.5 Interpretation of Figure 12
The results indicate that, among the listed features, "district " is considered the most important in predicting the target variable, followed by "property_type," "estate_type," and "new_build."

1.	New_Build:
•	Importance: 0.0101
•	This variable has a relatively low importance (0.0101) in predicting the target variable price paid.

2.	Estate_Type:
•	Importance: 0.0424
•	This variable has a higher importance (0.0424) compared to "new_build" but is still relatively moderate.
3.	Property_Type:
•	Importance: 0.1057
•	The "property_type" variable has a higher importance (0.1057), suggesting to have a greater influence on the target variable's prediction.
4.	District:
•	Importance: 0.8419
•	The "district" variable has a significantly high importance (0.8419), indicating that it is a significant indicator of the target variable(price paid). The high value suggests that variations in this variable strongly influence the model's predictions.
























SECTION 2: Data Modelling


 

Figure 13: Entity relationship (ER) diagrams of the Amazon Database





2.1 Interpretation of the Entity-Relationship Diagram
The Figure 13 shows Entity-Relationship Diagram designed for Amazon database using the Crow foot notation. The following are the component of the diagram:
1.	Entities: There are five main entities shown at the top of each a rectangle, each with a list of attributes within them:
2.	Attributes: Each entity has various attributes within by rectangles with their data type listed. They marked with a white diamond
3.	Primary Keys: Attributes with a key symbol are primary keys, which uniquely identify a record within an entity. 
4.	Relationships: The symbols at the ends of the lines (the crow's foot notation) indicate the cardinality of the relationship this will explained in details in the section 2.2
5.	Foreign Keys: Some attributes are marked with a foreign key symbol (a coloured diamond), indicating that they reference a primary key in another entity. 


2.2 Entity Relationship

1.	Customer to Order
 
Figure 14: Cardinal Relationship between Customer and Order
•	One-to-Many (1:N) relationship
•	One Customer can have multiple orders but each order is associated with exactly one customer





2.	Product to Order Item
 
Figure 15: Cardinal Relationship between Product and Order Item
•	One-to-Many (1: N) relationship
•	A single product can appear in one or more items, however each order item is associated with only one product

3.	Review to Product

 
Figure 16: Cardinal Relationship between Review and product
•	One-to-Many (1: N) relationship
•	Each review is link to a specific product but many reviews can be associated with one product.



4.	Product to Vendor
 
Figure 17: Cardinal Relationship between Product and Vendor
•	Many-to-One relationship
•	One product must be associated with one vendor but a single vendor can supply multiple products
5.	Order to Order item
 
Figure 18: Cardinal Relationship between Order and Order Item
•	One to many relationship
•	A single order can have multiple items on the order item table but each order is associated with only one order.








6.	Customer to Review
 
Figure 19: Cardinal Relationship between Customer and Review
•	One to Many relationship
•	One customer can have multiple reviews but each review is associated with only one customer

2.3	 Creating and Populating the Table/Entities using SQL
1.	Customer Table
The customer table was created using the CREATE TABLE SQL command in the Amazon Database. The structure of this table is to keep track of customers' basic information which can be seen in Figure 13 and Figure 20. The PRIMARY KEY constraint ensures that every customer has a unique identifier Customer ID. The NULL clause is a “logical constraint”, used to ensure that a column never gets a null value assigned to it (Phil Factor, 2020). The NOT NULL constraint ensures that the variable with this constraint has crucial information recorded for every customer. 

 
Figure 20: Screenshot of the Customer Table Schema
After creating the table, ten values were inserted into the table using the SQL INSERT query as shown in Figure 21 below 


 
Figure 21: SQL Query for Customer

The output is displayed in Figure 22 using the SQL SELECT (*) ALL Command
 
Figure 22: Record Value from the Customer Table


2.	Product Table 

This product table is created using the CREATE TABLE. The variable, type and number of characters are shown in Figure 13 and Figure 23. 

The "VendorID" column in the "Product" table and the "VendorID" column in the "Vendor" table are linked by a foreign key relationship established. The ON UPDATE CASCADE clause indicated that if the referenced "VendorID" in the "Vendor" table is updated the changes will automatically reflect on the Vendor ID on the PRODUCT TABLE.

The ON DELETE RESTRICT clause restricts records from being deleted from the "Vendor" table if there are associated products in the "Product" table.


 
Figure 23: Screenshot of the Product Table Schema
After creating the table, ten values were inserted into the table using the SQL INSERT query as shown in Figure 24 
 
Figure 24: SQL Query to insert into the Product Table


The output is displayed in Figure 25 using the SQL SELECT (*) ALL Command  
Figure 25: Record Value from the Product Table

3.	Order Table
This Orders table This product table is created using the CREATE TABLE. The variable, type and number of characters are shown in Figure 13 and Figure 26. 

The table has a Default value for two columns – Credit Card as the default value for the Column “Payment Method” and Processing as the default value for the Column “Order Status”. The "customerID" column in the "orders" table and the "customerID" column in the "customer" table are linked by a foreign key connection created on this table. The ON UPDATE CASCADE clause indicated that if the referenced " CustomerID" in the " Customer" table is updated the changes will automatically reflect on the Customer ID on the Orders TABLE.

 The ON DELETE RESTRICT clause restricts records from being deleted from the "Customer" table if there are associated products in the "Orders" table. 

 
Figure 26: Screenshot of the Order Table Schema

After creating the table, ten values were inserted into the Orders Table using the SQL INSERT query as shown in Figure 27 
 
Figure 27: SQL Query to Insert Values to Orders Table

The output for the is displayed in Figure 28 using the SQL SELECT (*) ALL Command
 
Figure 28: Result Output for the Orders Table

4.	Vendor Table
This Vendor table is created using the CREATE TABLE. The variable, type and number of characters are shown in Figure 13 and Figure 29
The NOT NULL constraints ensure that information must be entered for each Vendor ID, and the PRIMARY KEY constraint ensures that each product has a unique Order ID. 

 
Figure 29: Screenshot of the Vendor Table Schema

After creating the table, ten values were inserted into the Vendor Table using the SQL INSERT query as shown in Figure 30

 
Figure 30: SQL Query to Insert Values in Vendor Table

All the values inserted in the Vendor Table can be viewed using the SQL SELECT (*) ALL Command, the value is displayed in Figure 31 below.
 
Figure 31: Record Value from for the Vendor Table

5.	Order Item
This table is created using the CREATE TABLE. The variable, type and number of characters are shown in Figure 32.  The NOT NULL constraint prevents a column from accepting NULL values and the PRIMARY KEY constraint ensures that each product has a unique Order ID. “Order item ID” is set as the primary key this is used to uniquely identify each record on the table.

There is a link between the Order Item table and the Orders table, this is done by referencing the Orders Table using the Order ID column. The “Foreign key” and “Referencing” SQL commands are used. The “Update Cascade” SQL constraint is used to ensure that if the referenced OrderID in the Orders table is updated, the corresponding values in the Order ID column of the Order Item table will be updated. The 

The ON DELETE RESTRICT restricts a deletion attempt on the Orders table if it has matching records in the Order Item table. 

 
Figure 32: SQL Query Order Item Table Schema


After creating the Order Item table, the INSERT command is used to put the unique values based on the data type into the table as shown in Figure 33
 
Figure 33:SQL Query for Order Item Table
The values were successfully added to the Order Item’s Table and the SELECT (*) All syntax is used to view the records. This is shown in Figure 34
 
Figure 34: Record Value from the Order Item Table

6.	Review
The Review table is created using the CREATE TABLE. The columns, variable type and number of characters are shown in Figure 13 and Figure 35.

The actions to be performed when the referenced Customer table is changed or deleted are specified by the ON UPDATE CASCADE and ON DELETE RESTRICT commands. In this instance, it indicates that the values in the CustomerID column of the Review table should be updated (CASCADE) if the referenced CustomerID in the Customer table is altered. A deletion will be restricted (RESTRICT) if an attempt is made to remove a record from the Customer table that contains comparable records in the Review table.

FOREIGN KEY (ProductID) REFERENCES Product (ProductID) ON UPDATE CASCADE ON DELETE RESTRICT: Similar to the previous foreign key, this establishes a relationship between the ProductID column in the Review table and the ProductID column in the Product table, with specified actions on update and delete.

 
Figure 35:Screenshot of the Review Table Schema

Ten unique values are inserted into the Review table after creating the Review table as shown in Figure 36 based on the table datatype

 

Figure 36: SQL Query to Insert values to Review Table

The values were added successfully to the Review’s Table, and the records can be viewed using the SELECT (All) syntax, as illustrated in Figure 37.
 
Figure 37: Record Value from the Review Table

3. Business Scenarios
3. 1 Business Scenario 1:
Who are the high-value, middle-value and low- value customers in terms of total amount spent and loyalty points?

 
Figure 38:SQLCommand for Business Scenario 1

 
Figure 39: Result for Business Scenario 1
 This evaluates consumer spending patterns and divides them into various groups according to the overall amount spent and loyalty points. The results segment these customers into high Value, Medium Value and Low Value customers. As a result of this segmentation, Amazon is able to customize its marketing and customer care tactics to meet the unique requirements and preferences of each group of customers.

3.2 Business Scenario 2: 
Which Vendor has the lowest rating
 
Figure 40: SQL for Business Scenario 2
 
Figure 41: Result for Business Scenario 2
The result shows the details of the vendor with the lowest rating. Through consistent assessment and management of vendors' performance, Amazon can uphold high-quality standards, improve client contentment, and enhance its standing as a reliable and customer-focused virtual marketplace.






3.3 Business Scenario 3: 
Which of the product has the lowest price and the highest review rate?
 
Figure 42: SQL Command for Business Scenario 3
 
Figure 43: Result for Business Scenario 3

The Bluetooth speaker is the product with the lowest price but has the highest review rate of 5. The information gotten from this query helps improve price, inventory, and product promotion methods, making the market more competitive and raising customer satisfaction levels all around.








