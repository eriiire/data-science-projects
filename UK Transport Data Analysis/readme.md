# UK Department for Transport Dataset Analysis

## Project Overview
This project involves an in-depth analysis of the UK Department for Transport dataset to identify high-risk zones for vehicular accidents in Liverpool. Using data from 2013 to 2020, the analysis aims to help city authorities implement preventative measures to reduce accidents, injuries, and fatalities.

### Business Objective
The consultancy service behind this project focuses on analyzing historical accident and casualty data to identify danger zones in Liverpool with a high frequency of vehicular accidents. By identifying these zones, preventative strategies can be recommended to mitigate the risk of future incidents, ultimately contributing to public safety and reducing property damage.

---

## Table of Contents
1. Importing Libraries and Preparing Environment
2. Business Objective
3. Data Preparation
4. Feature Dataset Construction
5. Data Splitting
6. Descriptive Statistics
7. Data Cleaning
8. Statistical Analysis
9. Conclusion
10. Data Exporting

---

## 1. Importing Libraries and Preparing Environment
Necessary libraries, including `pandas`, `numpy`, `matplotlib`, and `seaborn`, are imported for data manipulation and visualization. Additional statistical and machine learning libraries such as `scipy.stats` and `statsmodels` are used for hypothesis testing and further analysis.

## 2. Business Objective
As a consultancy, our goal is to help city authorities identify and address accident-prone areas in Liverpool, focusing on reducing accident frequency and severity through targeted interventions.

## 3. Data Preparation
Two datasets from 1979–2021 and 2022 are loaded. Each dataset provides accident-related statistics, including accident details, vehicle information, and location data. For our analysis, data from 2013–2020 was filtered and limited to Liverpool.

## 4. Feature Dataset Construction
- Columns irrelevant to the analysis, such as `police_force` and `local_authority_highway`, are dropped based on domain knowledge and initial exploration.
- New columns, such as `numeric_fraction` (converting accident time to a numeric format), and a `Month` column from the accident date, are created to enable more detailed analysis.

## 5. Data Splitting
The dataset is split into training and test sets, with a 70:30 ratio. This split will later facilitate predictive modeling in a subsequent notebook.

## 6. Descriptive Statistics
The dataset is analyzed across multiple features:
- **Accident Severity**: Slight, Serious, and Fatal injuries are categorized, with slight injuries accounting for the majority (82.7%).
- **Number of Vehicles and Casualties**: Most accidents involve 2 vehicles, and typically result in 1 casualty.
- **Day of the Week and Time**: Accident frequency peaks on Fridays and between 4:30 PM to 5:30 PM.
- **Month**: November, December, July, and October show higher accident frequencies.
- **Road Characteristics**: Accidents are more common on Single Carriageway roads with a speed limit of 30 mph.

Visualizations, including histograms and bar charts, illustrate accident patterns across various dimensions.

## 7. Data Cleaning
The dataset is cleaned by:
- Removing rows with missing or placeholder values (-1, 9, or 99) where necessary.
- Dropping columns with high levels of missing information or limited analytical value (e.g., `first_road_class`, `junction_control`).
- Filling missing values in columns, such as `age_of_driver` and `age_of_vehicle`, with mean or median values.

## 8. Statistical Analysis
### Hypothesis Testing
1. **Day of the Week and Accident Frequency**: Using a chi-square test, we found that accident frequency significantly depends on the day of the week (p < 0.05).
2. **Month and Accident Frequency**: Similar analysis shows that accident frequency is significantly dependent on the month.

These insights indicate that accident occurrences are not random but vary significantly with specific time periods, such as days and months.

## 9. Conclusion
The analysis successfully constructed a dataset highlighting key insights into vehicular accident patterns in Liverpool. The findings will support the creation of a predictive model in a separate notebook, designed to identify danger zones and recommend preventative measures.

## 10. Data Exporting
The cleaned and transformed datasets (`x_train`, `y_train`, `x_test`, `y_test`) are exported as CSV files. These files will serve as input for the predictive modeling notebook.

---

## Additional Notes
- The project’s next phase will focus on model building, using the preprocessed data to create a model capable of identifying high-risk accident zones in Liverpool.

**Note**: The dataset files are large; external links are provided for downloading them.

--- 

## Repository Structure

The repository includes:
- `Data Analysis`: The current notebook with EDA and statistical analysis.
- `Predictive Modeling`: A separate notebook for building and evaluating accident prediction models (provided separately).

---

## Running the Analysis
1. **Data Analysis**: Start by running this EDA notebook to perform initial data preparation and statistical analysis.
2. **Predictive Modeling**: Use the exported datasets from this notebook as input to build predictive models.

This analysis enables an actionable understanding of accident-prone zones in Liverpool, assisting city authorities in deploying targeted safety interventions.

