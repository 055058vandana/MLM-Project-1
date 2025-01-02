# MLM-Project-1
## Project Report: Imports-Exports Dataset Analysis - Overall Conclusion

**Project Title:** Application of Machine Learning for Imports-Exports Dataset Analysis

**Date:** 2 January 2025

**Prepared by:** Vandana Jain

**1. Executive Summary**

This report summarizes the findings of a comprehensive data analysis project focused on an imports-exports dataset. The project's core objectives were to preprocess and explore the data, identify inherent patterns and groupings, and develop predictive models to understand key aspects of the import-export process. Through a systematic approach encompassing descriptive statistics, data transformation, clustering, and supervised machine learning techniques, the project successfully uncovered actionable insights and built models that provide predictive capabilities for critical business decisions. Notably, the project also delved into the relationships between categorical variables, assessed the normality of numerical variables, and carefully handled data outliers, adding depth to the overall analysis.

**2. Project Goals and Objectives**

The project was initiated to address the following key objectives:

*   Prepare the dataset for advanced analytics and machine learning.
*   Effectively manage and impute missing data.
*   Transform categorical data into a usable numerical format.
*   Standardize and normalize numerical data, including rigorous testing for normality.
*   Identify natural groupings within the transactional data.
*   Assess the relationships between categorical variables using a test of homogeneity.
*   Develop predictive models to understand and forecast shipping methods.
*   Evaluate and compare the performance of different machine learning models.
*   Generate business insights from the analysis, applicable to strategy and operations.

**3. Methodology**

The project followed a multi-phased methodology:

*   **Data Acquisition and Preparation:** The dataset was acquired, loaded, and subjected to rigorous data cleaning and preprocessing, including missing data handling (imputation), categorical data encoding (Ordinal Encoding), and numerical data scaling (MinMaxScaler). Outliers were considered during this stage and managed via row and column removal.
*   **Exploratory Data Analysis (EDA):** Descriptive statistics and visualizations were utilized to understand data characteristics, including central tendency, dispersion, variable relationships, and categorical distributions.
* **Normality Testing:** Rigorous testing was applied to the numerical variables. Tests applied were shapiro-Wilk, Kolmogorov-Smirnov, Anderson-Darling, and Jarque-Bera tests.
* **Test of Homogeneity:** A chi-squared test of homogeneity was implemented to test the independence of all categorical variables.
*   **Cluster Analysis:** K-Means clustering was employed to segment transactional data based on key numerical variables (Quantity, Value, Weight). The optimal number of clusters was evaluated using silhouette and Davies-Bouldin scores.
*   **Supervised Learning:** Supervised machine learning models, including Decision Tree, Logistic Regression, Random Forest and XGBoost, were trained to predict the 'Shipping\_Method' using 'Quantity' and 'Weight' as predictors.
*   **Model Evaluation and Comparison:** The models were rigorously evaluated using relevant metrics such as accuracy, classification reports, and confusion matrices. A comparative analysis of model performance was conducted.
*   **Insight Generation:** Insights derived from EDA, cluster analysis, and model results were translated into actionable business recommendations.

**4. Key Findings**

*   **Data Characteristics:** The dataset consisted of a mix of numerical and categorical variables. Initial exploration revealed that numerical variables varied in scale and distribution, necessitating transformation and scaling. Normality tests confirmed that certain variables deviated significantly from a normal distribution.
*   **Data Quality:** The initial dataset contained missing values which were addressed through a combination of row/column deletion and mean/mode imputation.
* **Categorical Variable Relationships:** The test of homogeneity showed whether each pair of categorical variables were independent of each other.
*   **Cluster Analysis:** K-Means clustering effectively segmented the data into four distinct clusters, revealing inherent groupings based on transactional attributes. ANOVA and Tukey's HSD tests confirmed statistically significant differences between these clusters, which was also supported by chi squared tests performed on the categorical variables.
*   **Predictive Modeling:**
    *   Supervised learning models (Decision Tree, Logistic Regression, Random Forest, and XGBoost) successfully predicted the 'Shipping\_Method' with good accuracy.
    *   The Logistic Regression model achieved the highest accuracy (approximately 76.1%), closely followed by the XGBoost model (75.3%) and Decision Tree model (75.2%).
    * Random Forest had the third highest level of accuracy.
    *   Decision Tree provided valuable insights into feature importance and decision rules.
*   **Variable Relationships:** EDA highlighted the relationships between key variables, such as 'Quantity', 'Value', and 'Weight', which can inform business decisions related to logistics and pricing. The correlation analysis provided a detailed view of these relationships.

**5. Business Implications**

This project's findings have several significant implications for business strategy and operations:

*   **Market Segmentation:** The four identified clusters provide a framework for market segmentation, enabling targeted marketing and customized service offerings based on different transaction profiles.
*   **Operational Optimization:** The predictive models can enhance logistical planning by enabling the anticipation of 'Shipping\_Method', helping optimize delivery routes, and managing resource allocation.
*   **Data-Driven Decision Making:** The comprehensive analysis provides a solid foundation for data-driven decision-making, ensuring strategies are informed by robust statistical analysis and predictive insights.
*   **Risk Management:** Understanding the relationships between variables and the characteristics of different clusters can help mitigate risks associated with fluctuating shipping costs and operational inefficiencies.
* **Customer Tailoring:** Categorical analysis provides insight into customer preferances for different shipping methods, payment terms and more. These characteristics could be used to better serve the different categories of customers.
* **Outlier awareness**: The business is now aware that outliers exist in the data and that they have been handled appropriately.
* **Normality**: The business is now aware that the data is not normally distributed and that the `MinMaxScaler` was used to handle this.

**6. Recommendations**

Based on the project outcomes, the following recommendations are made:

*   **Implement Predictive Modeling:** Integrate the trained predictive models into operational systems to support logistics planning and resource allocation.
*   **Refine Clustering Strategy:** Continuously monitor and update the clustering strategy to reflect changes in transactional patterns and market conditions.
*   **Data Quality Management:** Establish a data quality management program to prevent missing data, validate input data, and ensure ongoing data integrity.
*   **Advanced Analytics:** Explore more advanced analytical techniques such as time-series analysis (if temporal data is available) and integrate external datasets to enrich the analysis.
*   **Continuous Model Improvement:** Regularly evaluate and retrain the models to maintain and improve their predictive accuracy.
* **Explore other classifiers:** There are other classification models which may provide an even higher level of accuracy.
* **Consider Alternate Data Transformations:** Given that some variables did not conform to a normal distribution, explore alternative data transformations beyond MinMax scaling, such as logarithmic or Box-Cox transformations, to potentially enhance model performance.
* **Investigate Outliers Further:** Conduct a deeper investigation into the outliers that were identified. Determine if these outliers represent genuine anomalies or if they are valid, but rare, occurrences. This could lead to the discovery of new business insights.

**7. Conclusion**

This project has successfully analyzed the imports-exports dataset, extracting valuable insights through a combination of exploratory data analysis, normality and homogeneity testing, clustering, and supervised learning. The project met its objectives, providing data-driven insights that can directly influence business strategy and improve operational efficiency. The development of predictive models for shipping methods, alongside the identification of distinct transaction clusters, provides a robust framework for decision-making. The inclusion of data quality assessments and normality testing strengthens the analysis, ensuring that insights are derived from reliable and appropriately treated data. The identified recommendations outline a path for continuous improvement and further leveraging of advanced analytics within the business context.

**8. Future Work**
* A/B testing to explore the effects of targeted customer approaches.
* Use different categorical variables as the target variable in the classifiers.
* Explore the effect of using the cluster labels as an input variable for the classifiers.
* **Investigate Advanced Outlier Detection:** Employ more sophisticated outlier detection techniques, such as isolation forests or local outlier factor analysis, to identify outliers that were not detected by the initial methods.
* **Apply dimensionality reduction:** Explore applying PCA or t-SNE to reduce the dimensions of the dataset.
