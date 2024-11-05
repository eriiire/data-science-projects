# EasyVisa Project

## Context
The demand for human resources in the United States continues to rise, with businesses frequently seeking both domestic and international talent. Under the Immigration and Nationality Act (INA), the Office of Foreign Labor Certification (OFLC) oversees the certification of foreign workers, ensuring that employment practices protect U.S. wages and working conditions. In recent years, the volume of visa applications has increased, prompting a need for machine learning solutions to streamline visa approval processes and improve decision-making efficiency.

## Objective
EasyVisa, tasked with supporting OFLC, aims to use machine learning to:
- Predict visa approval likelihood for applicants.
- Identify key applicant and employer characteristics influencing visa outcomes, assisting in certification decisions.

## Data Description
The dataset includes several fields related to employees and employers, which contribute to modeling visa approval decisions:

- **case_id**: Unique identifier for each visa application.
- **continent**: Continent of the employee's origin.
- **education_of_employee**: Education level of the employee.
- **has_job_experience**: Indicates if the employee has job experience (Yes/No).
- **requires_job_training**: Indicates if the employee requires job training (Yes/No).
- **no_of_employees**: Total employees in the employer's company.
- **yr_of_estab**: Year when the employer's company was established.
- **region_of_employment**: Region in the U.S. where the foreign worker intends to work.
- **prevailing_wage**: Average wage paid to workers in a specific role and region, used to ensure wage parity.
- **unit_of_wage**: Wage frequency (Hourly, Weekly, Monthly, Yearly).
- **full_time_position**: Indicates if the job position is full-time (Yes/No).
- **case_status**: Status of the visa application (Certified/Denied).

## Technical and Analytical Skills Demonstrated

### Data Handling and Preprocessing
- **Data Cleaning**: Identified and managed missing values, dropped redundant columns, and converted categorical variables into appropriate formats to prepare for analysis.
- **Feature Engineering**: Generated additional features to enhance model performance and improve interpretability.
- **Outlier Detection**: Analyzed and treated outliers to ensure robust model inputs.

### Exploratory Data Analysis (EDA)
- **Univariate and Bivariate Analysis**: Used histograms, box plots, and bar charts to examine data distributions and relationships.
- **Correlation Analysis**: Conducted correlation analyses to uncover relationships among numerical variables and identify key drivers of visa application outcomes.

### Model Development
- **Classification Modeling**: Built a classification model to predict visa status, optimizing feature selection to enhance predictive accuracy.

### Hyperparameter Tuning and Evaluation
- **Hyperparameter Tuning**: Implemented hyperparameter tuning techniques, such as Grid Search and Randomized Search, to optimize model parameters, ensuring improved model performance and reliability.
- **Model Evaluation**: Assessed model performance using metrics such as accuracy, precision, recall, and F1-score, ensuring a robust evaluation of model quality. These metrics provided insights into the model’s capability to accurately classify visa outcomes, leading to well-informed decisions.

### Visualization and Reporting
- **Data Visualization**: Leveraged Seaborn and Matplotlib to create meaningful visuals, enhancing insight communication.
- **Markdown Documentation**: Documented all analysis steps and findings clearly within the Jupyter Notebook, ensuring the project is accessible for review.

### Coding and Data Science Best Practices
- **Code Modularity**: Organized code into well-defined sections for loading, preprocessing, and analysis, following best practices for readability and maintainability.
- **Statistical Analysis**: Integrated statistical analysis to support data-driven decisions, examining variables like education and job experience for their impact on visa outcomes.

## Conclusions and Recommendations
Based on the model's insights, further analysis can be done to:
- **Streamline Visa Processing**: Use predictive models to prioritize applications with high approval probability.
- **Optimize Resource Allocation**: Identify and address trends in regions or roles where visa denial rates are high, potentially addressing root causes with data-driven interventions.

The EasyVisa project demonstrates proficiency in data handling, exploratory analysis, predictive modeling, hyperparameter tuning, and evaluation—all applied to a real-world problem in labor certification.

---

This project showcases data science skills across data preprocessing, EDA, hyperparameter tuning, and effective communication, making it a strong addition to a professional portfolio.
