# Data Scientist


#### Technical Skills: Python, SQL, AWS, Snowflake, DBT

## Education			        		
- B.A., Computer Science and Statistics | Harvard University (_May 2017_)

## Work Experience
**Data Science Manager @ Fivestars by SumUp (_June 2022 - Present_)**
- Uncovered and corrected missing step in production data pipeline which impacted over 70% of active accounts
- Redeveloped loan originations model which resulted in 50% improvement in model performance and saving 1 million dollars in potential losses

**Data Scientist @ Amazon (_December 2020 - Present_)**
- Regional Forecasting Model: Created a time series model which decomposes order units and sales of the US county-level forecast into MSA (a group of counties) level with an error rate of +-3%. Chose the best model with backtesting and optimized hyper-parameters with HyperOpt. The result is published on Tableau every morning, which allows the risk team and fulfillment center to identify anomalies or forecast misses by comparing the forecast data to actual data.
- Anomaly Detection Model: Created an anomaly detection model with STL by taking trends, weekly seasonality, and special events (Prime Day) into account. The model successfully identifies the anomaly data points, which were flagged manually at weekly callouts. It made weekly callouts more scalable at more granularities and way less time-consuming.

**Data Scientist @ TripAdvisor (_December 2020 - Present_)**
- Short-term user value model: Owned User Value Model, which calculates the value of each user action on the TripAdvisor website and is crucial to the entire Search Engine Marketing Team (especially bidding). Replaced old multiple linear regression model with XGBoost model on Kubernetes and MLflow platforms. Intuitively explained the XGBoost model to stakeholders by visualizing feature importance with SHAP values and the expected impact of the new model on error reductions and revenue increase.
- Marketing Attribution Model: Developed new offline models to predict revenue incurred by each hotel booking and to predict hotel booking conversion rate of each click. Collaborated with an engineer to productionize codes and successfully pushed to the live site. Used elastic net regression and cross-validation to select useful features and reduced RMSE of hotel booking revenue prediction by 50%. This model was used across different teams at TripAdvisor. For example, Hotel Sorting Team had an 8% booking revenue increase by using this new model prediction as one of the features. Moreover, this model has been widely used at TripAdvisor to allocate revenue from providers that do not share revenue data with TripAdvisor.

**Data Scientist Intern @ Facebook (_December 2020 - Present_)**
- AB Test: Detected anomaly drop-off points and unnatural flow of users on Facebook Platform and drove a team of about 20 engineers
to conduct A/B tests by changing the description of stages where users tend to drop off. Predicted user completion rate with logistic regression based on variables such as user experience, past revenue, and country


## Projects
### Non-Inferiority Test

- [Link to Repository](https://github.com/takehiromatsuzawa/portfolio/blob/main/Projects/num_samples_non_inferiority_test.ipynb)


Non-inferiority trials test whether a new product is not unacceptably worse than a product already in use.
This python script allows you to compute the number of samples you need for non-inferiority tests. You need to enter mean, variance, significance and power to compute.

For example, we want to run A/B tests with a goal of improving revenue per visitor. 
1. Our null hypothesis would be then that the variant is not performing better than control. Occasionally, we can also accept a variant that is not
performing worse than e.g. -1% (relative) in terms of RPV compared to control. 
2. Hence, the null hypothesis (2) is
that the variant performs -1% or worse than control. Here is a sample data of revenue / visitor.
　

### Bank Fraud Detection

- [Link to Summary Documentation](https://github.com/takehiromatsuzawa/portfolio/blob/main/Projects/Bank%20Anomaly%20Detection/Bank%20Fraud%20Detection.pdf)

- [Link to Code](https://github.com/takehiromatsuzawa/portfolio/blob/main/Projects/Bank%20Anomaly%20Detection/Retail%20bank%20identifying%20scam%20transactions.ipynb)

Problem: Retail bank identifying scam transactions
A large retail bank is aiming to better identify scam transactions. The dataset they provide contains a sample of information about historical transactions, the customers making the transactions and whether the transaction was fraudulent. They currently use a simple rules-based approach using a subset of the features in the dataset to flag transactions, but they are open to more complex solutions that can give better predictive power while remaining explainable.

Fit Logistic Regression to explain the significant variables
1. Time Spent on App: An increase of 1 in Time Spent on App is associated with an increase of 1.5% in the odds of being fraud (assuming that all the variables remains fixed).
2. Years of Education: An increase of 1 in Years of Education  is associated with an decrease of 36% in the odds of being fraud (assuming that all the variables remains fixed).
3. Number of Transactions to Beneficiary:  An increase of 1 in Number of Transactions to Beneficiary  is associated with an decrease of 31% in the odds of being fraud (assuming that all the variables remains fixed).


### SQL Conversion Rate Investigation (Product Analysis)
1. SQL conversion rate dropped overall over the span of 4 weeks (47%, 47%, 34%, 39%).
2. During the 4-week span, the average conversion rate for paid social, direct email, other, and Email are 31%, 38%, 45%, and 83% respectively. 
3. If you break it down by sources, the conversion rates monotonically went up at the source level. Email  (70%-> 72%-> 84%-> 93%). Direct Emaill (18%-> 26%-> 35%-> 41%). Paid Social (18% -> 22% -> 23% -> 33%). 
4. SQL conversion rate dropped overall since the number of paid social and daily mail increased