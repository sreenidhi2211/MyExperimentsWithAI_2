# Exploratory Data Analysis (EDA) 
This project includes comprehensive Exploratory Data Analysis (EDA) conducted using Gemini (Google’s AI tool) within Google Colab to efficiently analyze and visualize the dataset.
<br>
🔍 Key Highlights:
Leveraged Gemini in Google Colab to generate automated insights, visualizations, and statistical summaries.
Explored data distributions, correlations, missing values, and outliers.
Helped in identifying significant features and patterns for further modeling or decision-making.
<br>
🚀 Deployment
All EDA notebooks and generated outputs are available in this GitHub repository.
<br>
💡 AI-assisted EDA helped streamline the process and provided faster, deeper insights into the dataset.
Note:The report is also generated with the assistance of AI
# 1. Introduction

This document details the Exploratory Data Analysis (EDA) conducted on the "mental_health_analysis.csv" dataset. The primary goal of this EDA is to gain a comprehensive understanding of the dataset's structure, characteristics, and relationships between variables, which will inform further analysis and modeling efforts.

# Know More about DataSet from:
https://www.kaggle.com/datasets/aniruddhawankhede/mental-heath-analysis-among-teenagers

# 2. Data Loading and Initial Exploration

The dataset was loaded into a pandas DataFrame named df.
Basic information about the DataFrame, including the first few rows, shape (number of rows and columns), and data types of each column, was examined using df.head(), df.shape, and df.info(), respectively.

# 3. Data Cleaning and Preprocessing

1.Missing Values: The number and percentage of missing values in each column were calculated and displayed. Missing values were handled by imputation:
2.Numerical features: Missing values were imputed with the mean of the respective column.
3.Categorical features: Missing values were imputed with the mode (most frequent value) of the respective column.
4.Outlier Detection: Potential outliers in numerical features were identified using the Interquartile Range (IQR) method. Box plots were used to visualize the distribution of data and highlight outliers. Outlier treatment strategies, such as capping or removal, were considered based on domain knowledge and the specific analysis goals.
5.Data Transformation (if needed): If any numerical features exhibited significant skewness, transformations (e.g., log transformation, Box-Cox transformation) were applied to improve the distribution and potentially enhance model performance in subsequent analysis. However, the data did not suggest that need.

# 4. Feature Engineering
1Combined Stress Score: A new feature called "Combined_Stress_Score" was created by averaging the values of "Survey_Stress_Score" and "Wearable_Stress_Score". This combined score provides a holistic indicator for assessing stress levels in young people.
2.Screen_Sleep_Ratio: An additional feature, "Screen_Sleep_Ratio", was engineered by calculating the ratio of "Screen_Time_Hours" to "Sleep_Hours". This feature aims to capture the relationship between screen time and sleep patterns.

# 5. Univariate Analysis
1.Numerical Features: Histograms and box plots were generated for each numerical feature to visualize their distributions, identify potential outliers, and understand central .endencies (mean, median) and dispersion (standard deviation, IQR). Summary statistics (mean, standard deviation, min, max, quartiles) were also computed using df.describe().
2.Categorical Features: Bar charts were created for each categorical feature to visualize their frequency distributions and understand the relative proportions of different categories. The value_counts() function was used to obtain the frequency counts for each category.

# 6. Bivariate Analysis
1.Correlation Analysis: The correlation matrix between numerical features was calculated using df.corr(). This helped identify potential linear relationships between variables. Scatter plots were used to visualize these relationships and assess the strength and direction of the correlations.
2.Group Comparisons: Group comparisons were performed to analyze the differences in stress levels across various categorical variables:
3.Gender: An independent samples t-test was conducted to compare the average stress levels between males and females.
4.Support Systems: A one-way ANOVA was used to determine if average stress levels differed significantly across different support systems.
5.Age Groups: Stress scores were analyzed for each age to identify which age group has higher stress on average.
6.Relationship Exploration: The relationship between screen time and stress levels was explored using a scatter plot. Additionally, correlation was calculated between those two variables to find the degree of relationship between them.
7.Distribution Analysis: A histogram was created to visualize the distribution of exercise hours among the participants.

# 7. Key Findings and Insights
1.Gender and Stress: Females, on average, reported higher stress levels compared to males.
2.Support Systems: Strong support systems, particularly family support, are associated with lower stress levels. Individuals with no support systems reported notably higher stress.
3.Sleep and Stress: There is a significant negative correlation between sleep hours and stress levels, suggesting that insufficient sleep can contribute to increased stress.
4.Age and Stress: Certain age groups, particularly the age of 17, experience higher stress levels on average.
5.Screen Time and Stress: There is a moderate positive correlation between screen time and stress levels, implying that higher screen time may be associated with increased stress.
5.Exercise and Stress: Exercise hours tend to peak around 2-4 hours per week for most participants.

6.Combined Stress Score: The combined stress score provides a comprehensive measure of stress, integrating data from surveys and wearable devices.

# 8. Conclusion
This EDA provides valuable insights into the factors influencing stress and well-being in young people. The findings highlight the importance of support systems, adequate sleep, and healthy technology habits in managing stress. This information can be used to inform counseling practices, develop targeted interventions, and support young individuals in improving their overall mental health.
