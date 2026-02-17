# behavioralanalysis



The dataset used in this study integrates quantitative data on student learning behaviors, engagement patterns, demographics, and academic performance. It was compiled by merging two publicly available Kaggle datasets, resulting in a combined file (“merged_dataset.csv”) containing 14,003 student records with 16 attributes. All records are anonymized and contain no personally identifiable information.

The dataset covers the following categories of variables:

    Study behaviors and engagement: StudyHours, Attendance, Extracurricular, AssignmentCompletion, OnlineCourses, Discussions
    Resource access and learning environment: Resources, Internet, EduTech
    Motivation and psychological factors: Motivation, StressLevel
    Demographic information: Gender, Age (ranging from 18 to 30 years)
    Learning preference classification: LearningStyle
    Academic performance indicators: ExamScore, FinalGrade

In this study, “ExamScore” and “FinalGrade” served as the primary performance indicators. The remaining variables were used to derive behavioral and contextual profiles, which were clustered using unsupervised machine learning techniques.

 

The analysis and modeling were implemented in Python through a structured Jupyter Notebook (“Project.ipynb”), which included the following main steps:

    Environment Setup – Import of essential libraries (NumPy, pandas, Matplotlib, Seaborn, SciPy, StatsModels, scikit-learn, imbalanced-learn) and visualization configuration.
    Data Import and Integration – Loading the two source CSV files, harmonizing columns, removing irrelevant attributes, aligning formats, handling missing values, and merging them into a unified dataset (merged_dataset.csv).
Data Preprocessing:

        Encoding categorical variables using LabelEncoder.
        Scaling features using both z-score standardization (for statistical tests and PCA) and Min–Max normalization (for clustering).
        Detecting and removing duplicates.

Clustering Analysis:

        Applying K-Means clustering to segment learners into distinct profiles.
        Determining the optimal number of clusters using the Elbow Method and Silhouette Score.
        Evaluating cluster quality with internal metrics (Silhouette Score, Davies–Bouldin Index).
Dimensionality Reduction & Visualization – Using PCA for 2D/3D cluster visualization and feature importance exploration.

    Mapping Clusters to Learning Styles – Associating each identified cluster with the most relevant learning style model based on feature patterns and alignment scores.
    Statistical Analysis – Conducting ANOVA and regression to test for significant differences in performance between clusters.
    Interpretation & Practical Recommendations – Analyzing cluster-specific characteristics and providing implications for adaptive and mobile learning integration.
