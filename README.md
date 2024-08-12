Copyright (c) 2024 Brad Stafford

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


README: Analysis of Garment Worker Productivity Data

Project Overview
This project analyzes a dataset related to garment worker productivity, focusing on various factors such as incentives, overtime, SMV (Standard Minute Value), WIP (Work In Progress), and the number of workers. The goal is to explore the relationships between these variables and worker productivity, using different machine learning models for classification and regression tasks.


"The Garment Industry is one of the key examples of the industrial globalization of this modern era. It is a highly labour-intensive industry with lots of manual processes. Satisfying the huge global demand for garment products is mostly dependent on the production and delivery performance of the employees in the garment manufacturing companies. So, it is highly desirable among the decision makers in the garments industry to track, analyse and predict the productivity performance of the working teams in their factories. This dataset can be used for regression purpose by predicting the productivity range (0-1) or for classification purpose by transforming the productivity range (0-1) into different classes."

>Reference<
Productivity Prediction of Garment Employees. (2020). UCI Machine Learning Repository. https://doi.org/10.24432/C51S6D.



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


