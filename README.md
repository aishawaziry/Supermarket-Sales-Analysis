# Supermarket Sales Analysis 
<p align="center">
    <img src="https://github.com/user-attachments/assets/cde22788-0e49-454a-ac61-a1ce0a021225"> 

## Project Description
#### The project involves data wrangling and analysis of a supermarket dataset with 14 variables to uncover insights into customer behavior, sales, and product performance. It also includes predictive modeling and an interactive dashboard to support stakeholder decision-making.

## Dataset Overview
#### The dataset consists of historical sales data from a supermarket company, recorded across three different branches over a period of three months. It contains 1006 rows and the following columns:

* Invoice id: Computer generated sales slip invoice identification number
* Branch: Branch of supercenter (3 branches are available identified by A, B and C).
* City: Location of supercenters
* Customer type: Type of customers, recorded by Members for customers using member card and Normal for without member card.
* Gender: Gender type of customer
* Product line: General item categorization groups - Electronic accessories, Fashion accessories, Food and beverages, Health and beauty, Home and lifestyle, Sports and travel
* Unit price: Price of each product in $
* Quantity: Number of products purchased by customer
* Tax: 5% tax fee for customer buying
* Total: Total price including tax
*Date: Date of purchase (Record available from January 2019 to March 2019)
* Time: Purchase time (10am to 9pm)
* Payment: Payment used by customer for purchase (3 methods are available – Cash, Credit card and Ewallet)
* Rating: Customer stratification rating on their overall shopping experience (On a scale of 1 to 10)

## Workflow of the project
#### Steps taken through the whole project to get the insight and results:
* Data Wrangling
* Visualization Using Python
* Prediction
* Dashboard
* Busniess Report 

## Data Wrangling 
#### Data wrangling, also called data cleaning, data remediation, or data munging, is the process of transforming raw data into a more usable format. This involves cleaning, structuring, and enriching the data so that it’s ready for analysis.

#### Data Wrangling has two types:

1. **Data Quality Issues** : These refer to problems or shortcomings in the qualitative or quantitative state of information, such as duplicate data, inaccurate and missing data, inconsistent data, irrelevant data, etc.

2. **Data Tidiness Issues**: These are related to the structure of the data, such as when a column header is a value, multiple variables are stored in one column, multiple columns represent one variable, variables are stored as rows, or observations are spread across multiple tables.

## Issues Found after data discovery
1. **Duplicated Rows**: The dataset contains 6 duplicated rows.
2. **Missing Values**: Missing values are present in the 'Tax' and 'Total' columns.
3. **Irregular Missing Value Representation**: The 'Customer Type' column contains missing values represented as '-'.
4. **Inconsistent Time Format**: The 'Time' column contains a value with the 'pm' word.
5. **Non-standard Time Format**: The 'Time' column includes a value formatted as '8-30' instead of the standard time format.
6. **Incorrect Unit Price Formatting**: Some values in the 'Unit Price' column include the 'USD' word.
7. **Negative Quantity Values**: The 'Quantity' column contains negative values.
8. **Typographical Errors**: Some entries in the 'Customer Type' column are represented as 'Memberr' instead of 'Member'.
9. **Excessive Decimals in Tax**: The 'Tax 5%' column contains values with more than 2 decimal places.
10. **Excessive Decimals in Total**: The 'Total' column contains values with more than 2 decimal places.
11. **Outliers in Quantity**: The 'Quantity' column contains some outliers.
12. **Outliers in Tax 5%**: The 'Tax 5%' column contains some outliers.
13. **Outliers in Total**: The 'Total' column contains some outliers.
14. **Outliers in Rating**: The 'Rating' column contains some outliers.
15. **Non-standard Date Format**: Dates are not in a standard format.
16. **Column misspelling**: Correct 'Naypyitaw' to the correct name.
17. **Multiple columns for one variable**: 'Yangon', 'Naypyidaw' and 'Mandalay'
18. **Columns name headers**: Capitalization in columns name


## Visualization Using Python 

### This section provides visualizations to support predictive modeling and enhance decision-making.

- - - -

* Word Cloud of product line
<p align="center">
  <img src="https://github.com/user-attachments/assets/e1352497-ef89-45cf-be69-10f90c9413ec" alt="products" width="45%">
</p>

* Distribution of rating
<p align="center">
  <img src="https://github.com/user-attachments/assets/a61ebbec-1cf2-4a17-a4cb-0c12b4f070f2" alt="output" width="45%">
</p>

* Day with high average sales

<p align="center">
  <img src="https://github.com/user-attachments/assets/1e6f3f10-51dd-4979-aca7-f9c2e8c5c425e" alt="Days" width="45%">
</p>

* Correlation between features
<p align="center">
  <img src="https://github.com/user-attachments/assets/d43878d9-502f-49fa-8d89-41cb3f0bc850" alt="corr1" width="45%">
  <img src="https://github.com/user-attachments/assets/162a5872-1b72-43f6-aa1e-9d2889bcf19d" alt="corr2" width="45%">
</p>

## Prediction

### Machine Learning Models for Total Sales Forecasting

Utilize machine learning models to accurately forecast **total sales** , enabling data-driven insights and strategic planning.

#### Models Employed
- **Linear Regression**
- **Decision Tree Regression**
- **K-Nearest Neighbors (KNN) Regression**

#### Feature Engineering

* Feature Engineering: Several preprocessing steps were conducted to convert categorical data into numerical form:
    * Time of purchase was categorized into Morning, Afternoon, Evening, and Night based on the hour.
    * Date was simplified to the month level (January, February, etc.).
    * Categorical columns like Product line, Payment method, and City were one-hot encoded for machine learning purposes.

#### Evaluation Metrics
To assess the performance of each model, the following metrics were used:
1. **Mean Absolute Error (MAE)** – Measures the average magnitude of errors in predictions, without considering their direction.
2. **Mean Squared Error (MSE)** – Evaluates the average of the squared differences between predicted and actual values, penalizing larger errors.
3. **R-Squared (R²)** – Represents the proportion of the variance for the dependent variable that's explained by the model.

#### Model Performance Summary

![Model Performance](https://github.com/user-attachments/assets/89514b3f-e5d8-4480-b2ae-552ce364e899)

From the image above, the results indicate that the **Linear Regression** model performed the best, achieving:
- The **lowest MAE**, indicating more accurate predictions with smaller errors.
- The **highest R² score**, showing a stronger explanatory power.

#### Stakeholder Benefits
* **Sales Managers**: Predicting future sales helps in managing supply chains and inventory, avoiding stockouts or overstocking.
* **Marketing Teams**: Understanding sales trends supports better budgeting for campaigns and promotions.
* **Business Strategists**: Data-driven forecasting aids in long-term planning and identifying new growth opportunities.
By implementing these models, stakeholders gain actionable insights that drive profitability, optimize operations, and enable strategic decision-making.

## Dashboards
![Screenshot 2024-09-12 160827](https://github.com/user-attachments/assets/9fbfa7ef-4e63-4987-8838-34789ea1d81b)
![Screenshot 2024-09-12 160849](https://github.com/user-attachments/assets/76de44fe-f7a2-4321-b2f4-46f95a23a6c9)
![Screenshot 2024-09-12 160915](https://github.com/user-attachments/assets/fc612740-bacd-4c57-9b7e-a0deeacf059f)
![Screenshot 2024-09-12 154844](https://github.com/user-attachments/assets/12d16e7f-21cd-4357-b725-21b560a82de5)

## Conclusion 
The data cleaning and preprocessing of the `Supermarket Sales` dataset were essential steps to ensure the quality, consistency, and reliability of the data for further analysis. By addressing various issues, including missing values, inconsistent formatting, typographical errors, and outliers, the dataset was transformed into a clean and well-structured form.
This process not only improved the dataset's overall integrity but also enhanced its usability for analytical purposes, such as customer behavior analysis, sales trend identification, and performance evaluation. The cleaned dataset provides accurate insights that can drive decision-making processes.
Using Python and powerful data manipulation libraries like Pandas, the challenges were effectively managed, demonstrating the importance of thorough data preparation in any analytical workflow. This project highlights the critical role of data cleaning in ensuring the validity of subsequent analyses and the value it adds in drawing meaningful and actionable insights.

<table>
    <tbody>
    <tr>
        <td colspan="6" style="text-align: center;"><b> Team Members </b></td>
    </tr>
    <tr>
        <td align="center" valign="top" width="20%">
            <a href="https://github.com/aishawaziry">
                <img alt="Aisha Amr" src="https://avatars.githubusercontent.com/aishawaziry" width="100px;">
                <br/>
                <sub><b>Aisha Amr</b></sub>
            </a>
            <br/>
        </td>
        <td align="center" valign="top" width="20%">
            <a href="https://github.com/esraa12724">
                <img alt="esraa12724" src="https://avatars.githubusercontent.com/esraa12724" width="100px;">
                <br/>
                <sub><b>esraa12724</b></sub>
            </a>
            <br/>
        </td>
        <td align="center" valign="top" width="20%">
            <a href="https://github.com/abdelazizMsakr">
                <img alt="abdelazizMsakr" src="https://avatars.githubusercontent.com/abdelazizMsakr" width="100px;">
                <br/>
                <sub><b>abdelazizMsakr</b></sub>
            </a>
            <br/>
        </td>
        <td align="center" valign="top" width="20%">
            <a href="https://github.com/AsmaaAdel336">
                <img alt="AsmaaAdel336" src="https://avatars.githubusercontent.com/AsmaaAdel336" width="100px;">
                <br/>
                <sub><b>AsmaaAdel336</b></sub>
            </a>
            <br/>
        </td>
    </tr>
    </table>
