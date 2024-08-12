EADME: Analysis of Garment Worker Productivity Data

Project Overview
This project analyzes a dataset related to garment worker productivity, focusing on various factors such as incentives, overtime, SMV (Standard Minute Value), WIP (Work In Progress), and the number of workers. The goal is to explore the relationships between these variables and worker productivity, using different machine learning models for classification and regression tasks.

Dataset Description
The dataset includes the following key columns:
- **date**: Date of the record.
- **quarter**: The quarter of the year.
- **department**: Department within the factory.
- **day**: Day of the week.
- **team**: The team working on the garment.
- **targeted_productivity**: The target productivity for the day.
- **smv**: Standard Minute Value.
- **wip**: Work In Progress.
- **over_time**: Overtime in minutes.
- **incentive**: Incentive amount.
- **idle_time**: Idle time in minutes.
- **idle_men**: Number of idle workers.
- **no_of_style_change**: Number of style changes.
- **no_of_workers**: Number of workers.
- **actual_productivity**: Actual productivity achieved.

Analysis and Findings

**1. Correlation Analysis**
- **SMV and No. of Workers**: There is a strong positive correlation (0.91), indicating that as SMV increases, the number of workers also tends to increase significantly.
- **Productivity Class and Actual Productivity**: A strong correlation (0.79), expected since productivity classes were derived from actual productivity.
- **Overtime and No. of Workers**: A positive correlation (0.73), suggesting more workers are associated with higher overtime.
- **Team, SMV, WIP, and No. of Workers**: The strongest correlation in this subset is between SMV and No. of Workers, while other relationships are weak.

**2. Machine Learning Models**
- **k-Nearest Neighbors (kNN)**: This model showed moderate accuracy in predicting productivity classes based on overtime, with an accuracy of 69.17%.
- **Decision Tree**: Performed the best among the models, with an accuracy of 84.58%.
- **Logistic Regression**: Showed a bias towards higher productivity classes, with a lower accuracy of 65.42%.
- **Support Vector Machine (SVM)**: The least effective model in this case, with an accuracy of 58.75%.

**3. Visualizations**
- **Heatmap of Correlations**: Provided a visual overview of relationships between numeric variables, highlighting the strongest correlations in the dataset.
- **Scatter Plots and Histograms**: Used to visualize relationships between incentives, overtime, and actual productivity.

Conclusion
This analysis highlights the relationships between key factors like SMV, the number of workers, overtime, and productivity in garment manufacturing. The Decision Tree model proved to be the most effective in predicting productivity, while the correlation analysis underscored the significant role of SMV in workforce dynamics.

Recommendations
- **Further Exploration**: Consider hyperparameter tuning for models like kNN and Logistic Regression to improve accuracy.
- **Feature Engineering**: Additional features derived from existing data could potentially enhance model performance.

How to Use This Repository
- **Data Preparation**: The dataset requires preprocessing, including handling missing values and converting categorical variables to numeric form.
- **Model Training**: Python scripts are included for training and evaluating kNN, Decision Tree, Logistic Regression, and SVM models.
- **Visualization**: Various plots and heatmaps are provided to visualize data relationships and model results.


