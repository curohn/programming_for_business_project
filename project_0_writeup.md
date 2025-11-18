Project 0

Group
Carson Johnston - cjohnston15@student.gsu.edu - Team Leader
Diana Dickson - ldickson2@student.gsu.edu 
John Curran - jcurran6@student.gsu.edu  

“Statement of Academic Honesty:
The following code represents our own work. We have neither received nor given inappropriate assistance. We have not copied or modified code from any source other than the course webpage or the course textbook. We recognize that any unauthorized assistance or plagiarism will be handled in accordance with Georgia State University's Academic Honesty Policy and the policies of this course. We recognize that our work is based on an assignment created by the Institute for Insight at Georgia State University. Any publishing or posting of source code for this project is strictly prohibited unless you have written consent from the Institute for Insight at Georgia State University.”
The Problem

Zillow hosts the most popular real estate platform in the world, allowing users to view, explore, and purchase homes across the United States. Our platform makes buying, selling, and all real estate transactions easy. However, many properties lack accurate price estimates, making it difficult for users to determine fair market value and compare options effectively. We need to create a prediction engine that can automatically estimate home prices based on property features.

	Identifying and solving this issue would allow the organization to provide a new offering to our customers. Whether they are buying, selling, or advising, they would be able to see reasonable price estimates for the real estate and compare it to others nearby, allowing them to make smarter decisions. 

For Zillow itself, this pricing model would add nuance and depth to our analytics internally. Analyses on macro economic trends, micro economic trends, and others would become possible and better informed. This data also could be provided to larger government and Non-governmental groups for large scale research, increasing the transparency in markets and creating fairer transactions for all. 

Goals

Provide a prediction model that can predict a fair and reasonable price.
Provide aggregated statistics for different locations, allowing comparisons between regions. 
Provide a service that  increases user engagement and satisfaction with the platform. 
Allow users to make more informed real estate decisions. As stated early, having knowledge of comparable real estate prices will allow these transactions to be fairer to all. 

Future Solution

Solving the dilemma of accurate pricing information is crucial for user satisfaction and confidence in real estate transactions. For either the buyer or the seller it allows for informed decision making when purchasing real estate allowing for both a fair and competitive price. For Zillow as an organization, improving price prediction strengthens user trust, enhances engagement, and sets it apart from competitors by leveraging advanced analytics and machine learning. On a societal level, the solution promotes transparency, fairness, and efficiency in housing markets, helping individuals make sound financial decisions in one of life’s most significant investments.

Current Solution

Currently Zillow uses a mixture of techniques to help identify current market conditions. Generally price estimates focus on traditional appraisals, comparative market analyses, and public records & tax assessments to help determine the current value of a home. In traditional appraisals a mixture of in person inspections, local sale comps and considering condition/upgrades are used to help account for the houses fair market value. Using comparative market analyses uses recent sales, current listings, and expired listings combined with local knowledge to prepare a home and evaluation. If the other two methods fail to bring a clear valuation, tax assessments on the property and public sale records to find a property value would be used although that data is generally outdated. 

Data Acquisition

We plan to use a public dataset gathered from Kaggle.com. The "USA Real Estate Dataset" provides real world prices of homes across the United States. It is available at: https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset

This dataset contains one record for a single property sale in the United States. It also has numerous features. This is from 900,000+ property records.
  - Key features include:
    - Price (target variable): Sale price of the property
    - Bedrooms: Number of bedrooms
    - Bathrooms: Number of bathrooms  
    - Lot size: Property size in acres
    - Location data: Street address, city, state, and zip code
    - Sale status: Whether the property was sold, for sale, etc.
Future augmentation can include additional information on demographics, property age, square footage and even market trends for the region.

Data Analytics Components 

Our solution will include several key components of the data analytics process to ensure that the predictive model we develop for Zillow is accurate, interpretable, and ready for deployment. The dataset has been obtained externally so we will begin by assessing the variable to determine the influence on housing prices. Like any dataset we will need to clean the data by adjusting for missing data, duplicate and extreme outliers that cause inaccuracies in the pricing model. Once cleaned, we plan to use heatmaps, scatterplots, and boxplots to identify patterns and inform feature selections. These trends can be further dived into by adding  additional variables by calculating the price per a square foot or by adding regional median income to help identify more complex trends.

We will train and test multiple machine learning models, such as Linear Regression, Random Forest, and XGBoost, to predict home prices. Model performance will be evaluated using metrics like Root Mean Squared Error (RMSE) and R² to determine accuracy and generalizability. Once the best model is selected, we will interpret the most influential features driving price predictions. The final model will be designed for integration into Zillow’s platform to provide users with dynamic, real-time price estimates.

Data Processing 

The data will need to be processed in batches as we don't need the immediate values, but rather help identify trends in the market place. Our data will revolve around property characteristics, location features, market data, categorical descriptors, and current market value. We will need to clean the data for any outliers or data with inaccurate, missing values, or outdated valuations.We may also group certain regions that notice pricing correlations to help better track trends over time. 

Predictive Analytics Solution

We propose using regression models to predict home prices based on features like number of bedrooms, bathrooms, lot size, and location. We will start with Linear Regression as our baseline model and then explore more advanced techniques like Random Forest to improve accuracy. Regression is designed for predicting continuous numerical values (like price), which is exactly what we need. Given features like "3 bedrooms, 2 bathrooms, 1500 sq ft" the model will output a predicted price. This model will be based on real patterns, be easy to read and identify patterns in home sales and not to mention it is an industry standard to use a regression-based approach for price estimate tools.
 
Evaluation Strategy 

Our evaluation strategy focuses on assessing both the technical accuracy of the predictive model and its business impact once implemented in Zillow’s platform. The evaluation will occur in two stages: model-level evaluation (quantitative performance metrics) and organizational-level evaluation (impact on key performance indicators).

Model Evaluation Metrics: To measure how well our model predicts housing prices, we will use the following metrics:

Root Mean Squared Error (RMSE): RMSE will assess the average magnitude of prediction errors, penalizing larger errors more heavily. This is critical for price prediction tasks where even small deviations can affect user trust.
Mean Absolute Error (MAE): MAE will complement RMSE by providing a straightforward measure of average error in dollar terms, offering intuitive insight into how far off predictions are from actual prices.
R² (Coefficient of Determination): R² will help evaluate how well the model explains variability in housing prices and determine its overall explanatory power. Using multiple metrics ensures a balanced view of performance, capturing both the precision and reliability of the model.
Model Validation Approach: We will implement train-test splits and cross-validation to prevent overfitting and verify model generalization across different data subsets. Residual plots and error analysis will be performed to detect systematic biases in certain property types or price ranges.
Organizational Impact Evaluation (Post-Integration): Once integrated into Zillow’s platform, the effectiveness of the predictive model will be evaluated based on business KPIs that reflect user engagement, satisfaction, and retention. Key performance indicators include:
Increase in User Engagement: Measured through metrics such as time spent on property pages, the number of repeated visits, and interactions with pricing tools.
User Trust and Accuracy Feedback: Tracking how closely model-generated price estimates align with final sale prices and user-reported satisfaction ratings.
Conversion Rate Improvement: Monitoring whether accurate estimates lead to more users contacting agents, saving listings, or completing purchases.
Brand Credibility: Improvement in user retention and growth in new users driven by enhanced pricing transparency.

Evaluating Improvement: We will compare the model’s performance against Zillow’s previous pricing methods (if available) to quantify improvements in prediction accuracy and user behavior. Reductions in RMSE and MAE will indicate technical success, while upward trends in engagement and conversion KPIs will demonstrate tangible business value.
We here at Zillow host the most popular real estate platform in the world. Our platform allows our users to view, explore, and purchase homes in every market in the United States. We would like to create a prediction engine that attempts to price real estate based on a number of features. This would benefit our users by allowing them to get an estimate on price for each home they view, as well as price shop. This would benefit the organization by making our users happier, and more likely to come back to us here at Zillow.

Utilization

Zillow would use the model as a supplemental tool in their research when evaluating a property. It can be used as a baseline for property evaluation, allowing adjustments for the current market, property conditions and other desired features. This would let Zillow make more accurate and timely pricing decisions for properties. While at the same time bringing a potential competitive advantage compared to their peers. There are no real capacity requirements for this solution outside of collecting the data, entering it, server costs and general model maintenance to maintain model accuracy. 

