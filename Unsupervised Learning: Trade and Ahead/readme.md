### Objectives

The project's main objective is to support Trade&Ahead, a financial consultancy firm, in creating personalized investment strategies by analyzing data from stocks listed on the New York Stock Exchange. This analysis involves clustering stocks to identify groups with similar characteristics and minimal correlation, enabling the creation of a diversified portfolio for investors to maximize returns and minimize risk.

### Data Description

The dataset provided by Trade&Ahead contains stock price and financial indicators for companies, with each row representing a unique stock observation. The data includes variables like:

- **Stock price**: The price of each stock.
- **Sector information**: The economic sector to which each stock belongs.
- **Financial metrics**: Various financial indicators that can influence investment decisions.

The analysis aims to use these attributes to classify stocks based on performance metrics, helping investors select stable stocks for investment.

### Technical and Analytical Skills Demonstrated

1. **Data Importation and Handling**:
   - **Libraries Used**: The analysis utilizes **Pandas** for data loading and manipulation.
   - **Data Preprocessing**: The data includes sanity checks, observations, and handling of missing or erroneous data values.

2. **Exploratory Data Analysis (EDA)**:
   - **Statistical Summary**: Examination of stock price distributions, average cash ratios, and Price-to-Earnings (P/E) ratios by sector.
   - **Visual Analysis**: Use of **Matplotlib** and **Seaborn** to generate histograms and correlation heatmaps, facilitating insights into price volatility and sector performance.

3. **Unsupervised Learning**:
   - **Cluster Analysis**:
     - Evaluating clustering algorithms such as K-means and Hierarchical Clustering, comparing their effectiveness in grouping similar stocks.
     - Calculation of silhouette scores to assess cluster compactness and cohesion.

4. **Business Analysis and Insight Generation**:
   - **Cluster Insights**: Identified clusters that signify stock performance:
     - Cluster 0: Stocks with high price stability and positive price changes.
     - Cluster 1: Moderately stable stocks.
     - Cluster 2: Highly volatile stocks with negative price changes, posing higher investment risks.
   - **Investment Recommendations**: Suggestions on clusters suitable for investment versus those to avoid due to high risk.

5. **Feature Engineering and Transformation**:
   - Creation of derived features such as volatility and price change percentages to assist in evaluating stock stability.

6. **Business Insights and Recommendations**:
   - Recommendations on preferred stock clusters for low-risk investments.
   - Clusters of volatile stocks identified as riskier, advising investors to approach with caution.

7. **Conclusion and Recommendations**:
   - Summarized insights on stock clusters, with actionable recommendations tailored to different investor risk profiles, enhancing Trade&Ahead’s ability to guide clients effectively.
  
---

This project highlights skills in data analysis, business analytics, data visualization, and unsupervised machine learning techniques. 

