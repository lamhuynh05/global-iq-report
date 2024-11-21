# Global IQ Report

# Client Bio 
The United Nations (UN) is an international organisation that is committed to maintaining international peace and security, promoting social progress, and human rights (United Nations, 2017). The organisation actively promotes educational and economic development as key elements of its sustainable development goals. https://www.un.org/en

# Recommendation
- Statistical analysis reveals a robust correlation between educational attainment and economic prosperity, evidenced by higher Gross National Income (GNI) per capita with increased schooling years. 

- This report recommends that the United Nations intensifies efforts to extend mean years of schooling globally, particularly in underperforming regions. Such a strategy not only aligns with the UN’s Sustainable Development Goal 4 and 8 (THE 17 GOALS | Sustainable Development, 2015) but also promises significant economic uplift.

- Implementing this recommendation will advance global economic stability and reduce inequalities, reinforcing the UN's commitment to sustainable development.

# Evidence 

## Initial Data Analysis (IDA)
### Source:
The dataset used is titled “Average global IQ per country with other stats”. It was collected and formatted by Matheus Felipe on Kaggle (https://www.kaggle.com/datasets/mlippo/average-global-iq-per-country-with-other-stats?resource=download)

### Limitation:
There are many rows with missing data in mean years of schooling and GNI which may lead to inaccurate and non-inclusive results. 

### Structure:
The dataset consists of 193 rows, each row represents a country or small territory. There are 10 columns of different variables:

- Rank

- Country

- Average IQ

- Continent

- Literacy Rate

- Nobel Prizes

- HDI

- Mean years of schooling: Mean years of education that a country’s citizens receive.

- GNI: Gross National Income of that country. 

- Population

### Data Cleaning:
Command read_csv classifies the columns when the dataset was imported. The column labels were changed from question format to short and precise names for convenience and reusability.

## Linear Regression Models
According to Marquez-Ramos, education is important as it affects the country’s economic growth (Marquez-Ramos). From the IQ dataset, education is quantified as mean years of schooling and economic growth is measured by Gross National Income (GNI). 

To clarify how mean years of schooling impacts economic outcomes in varied contexts, countries are divided into lower and higher GNI groups based on median GNI, reducing variability within groups and enabling more precise comparisons.

In order to ensure that a relationship between education and economic growth exists and visualise such a relationship, scatter plots are used for both lower GNI and higher GNI groups.

<img width="711" alt="Screenshot 2024-11-22 at 1 19 11 am" src="https://github.com/user-attachments/assets/a3fe36b8-b6b8-47cd-97e3-a19d46b3e70e">

<img width="829" alt="Screenshot 2024-11-22 at 1 20 02 am" src="https://github.com/user-attachments/assets/76299364-1724-4bee-8680-4fc84884e615">

The two scatter plots demonstrate that as the countries' mean years of school increases, their GNI also increases, therefore, there is a positive relationship between the two variables. This is consistent with current research showing that as individuals receive more education, their income tends to increase (Clarke, 2022), which in turn aligns with the recommendation that higher education levels can lead to a greater country’s GNI. 

After a visible relationship between mean years of school and GNI has formed, a linear model is used to quantitatively measure this relationship, providing precise estimates and enabling statistical testing for significance.

<img width="719" alt="Screenshot 2024-11-22 at 1 20 30 am" src="https://github.com/user-attachments/assets/681c9c81-67bd-41a2-bdf2-0180dd0b08fc">

<img width="830" alt="Screenshot 2024-11-22 at 1 20 50 am" src="https://github.com/user-attachments/assets/a71de162-5395-441a-aa65-9e4bcfc880db">

Both p-values from the linear regression models of the lower and higher GNI groups are below 0.05, indicating a statistically significant relationship between mean years of schooling and GNI in both economic tiers, confirming that education positively impacts economic performance across different levels of national income.

## Bar Plot
Creating a bar plot to compare mean of mean school years by GNI levels provides a clear, visual method for highlighting educational disparities between lower and higher GNI countries. 

<img width="682" alt="Screenshot 2024-11-22 at 1 22 35 am" src="https://github.com/user-attachments/assets/c3632351-b851-46f4-a163-1531c977fb21">

The bar plot shows that higher GNI countries tend to have more years of schooling. According to Vegas, wealthier nations invest more in education which suggests that increasing educational opportunities in lower GNI countries could be a key strategy for economic development (Vegas, 2020).

## Hypothesis Testing
H0 = There is no difference in the mean years of schooling between the lower GNI group and the higher GNI group.

H1 = There is a difference in the mean years of schooling between the lower GNI group and the higher GNI group.

A Welch Two Sample t-test is performed on the mean school years of lower GNI group and higher GNI group. As the p-value is smaller than 0.05, there is sufficient evidence to reject the null hypothesis. Therefore, there is a difference in mean years of schooling between the two groups of GNI. 

<img width="832" alt="Screenshot 2024-11-22 at 1 27 55 am" src="https://github.com/user-attachments/assets/c97cdd79-3d27-4b25-a610-c35733b16cc1">

# Appendix 

## Client Choice
United Nations is chosen as the client for this project's recommendation because of its global influence and commitment to promoting quality education. 

## Statisitcal Analyses
Independence: The samples are all independent as each country is only used once. 

### Hypothesis
This is done in section 3.4

### Assumptions
#### Linear Regression Models

- Scatter plots: Linearity of scatter plots can be found in section 2.2. 

- Residual plots: The points on both residual plots appear to randomly scatter around the horizontal axis which demonstrates homoscedastic. 

Thus, the two assumptions are met for the linear regression models that are done in section 2.2.

<img width="714" alt="Screenshot 2024-11-22 at 1 29 01 am" src="https://github.com/user-attachments/assets/d011fb3c-617b-4118-8d41-d64e7cd38e5e">

<img width="701" alt="Screenshot 2024-11-22 at 1 29 33 am" src="https://github.com/user-attachments/assets/cc5580f7-3036-4b4d-9367-028adda2ba88">

#### Hypothesis Testing
Normality:

- Box plot: The comparative box plots display symmetrical distribution and absence of significant skewness or outliers. This suggests that the data conforms well to a normal distribution.

- QQ plots: The QQ plots show a straight line, confirming that the data points closely adhere to a normal distribution. 

- Normality Check: As both sample size are both larger than 30, the Central Limit Theorem ensures the sample means are approximately normal.

<img width="679" alt="Screenshot 2024-11-22 at 1 31 34 am" src="https://github.com/user-attachments/assets/3ea7fd25-c46d-44c9-b42a-e1a6352ee27d">

<img width="677" alt="Screenshot 2024-11-22 at 1 31 53 am" src="https://github.com/user-attachments/assets/b0bc9913-8629-48a3-a60a-ebc8c63413cb">

<img width="663" alt="Screenshot 2024-11-22 at 1 32 20 am" src="https://github.com/user-attachments/assets/da258c97-7cf3-45e2-a789-e2e4682cdd88">

<img width="672" alt="Screenshot 2024-11-22 at 1 32 39 am" src="https://github.com/user-attachments/assets/fbcfd1e9-ae23-4a5a-9466-547d69b5f92e">

Equal Spread: 

- Variance Test: As p-value is smaller than 0.05, the null hypothesis is rejected, the variances of the groups are not equal. Thus, instead of 2 Sample T-test, Welch Two Sample t-test is used in section 2.3.

  H0: The variances of the groups are equal
    
  H1: The variances of the groups are not equal

<img width="832" alt="Screenshot 2024-11-22 at 1 33 18 am" src="https://github.com/user-attachments/assets/10783e85-4299-4f74-afcb-56ad8768fd7a">

### Test Statistic and P-value
With a t-value of -14.106 and a p-value < 2.2e-16, there is a statistically significant difference between mean school years of lower GNI and higher GNI groups.

### Conclusion
Statistical conclusion: As p-value < 0.05, the null hypothesis is rejected. There is a difference in the mean years of schooling between the lower GNI group and the higher GNI group

Scientific conclusion: The data suggests that a country’s mean years of school does have an effect on its GNI. 

## Limitations
- Temporal relevance: Variables like HDI, GNI, and Mean years of schooling were collected in 2021, which may not reflect recent changes, potentially limiting the applicability of this project's findings.
