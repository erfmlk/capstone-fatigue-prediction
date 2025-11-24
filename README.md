Fatigue Life Prediction Using Machine Learning
Capstone Project – Module 20.1: Exploratory Data Analysis (EDA)
Program: Professional Certificate in Machine Learning & Artificial Intelligence – Berkeley
By: Erfan Maleki
________________________________________
Overview
This project analyzes the fatigue behavior of Laser Powder Bed Fusion (LPBF) AlSi10Mg alloy using machine learning.
The goal is to explore the dataset through extensive EDA, engineer meaningful features, detect outliers, and build a baseline regression model for fatigue life prediction.
This work represents the initial report for the final capstone (Module 20.1). Additional refined modeling and deployment will follow in Module 24.
________________________________________
Objective
The main objective of this project is to:
•	Perform data cleaning, preprocessing, and exploratory data analysis (EDA)
•	Identify relationships between process parameters, surface condition, porosity, loading stress, and fatigue life
•	Engineer new features to improve model understanding
•	Develop a baseline regression model for predicting fatigue life (cycles to failure)
•	Provide insights for mechanics + ML–driven fatigue analysis in LPBF alloys
________________________________________
Dataset Details
The dataset includes fatigue test results for LPBF AlSi10Mg specimens with multiple process and post-processing conditions.
Independent Variables (Inputs)
Includes (but not limited to):
•	Manufacturing Parameters:
o	Build Orientation
o	Energy Density / Laser Power / Scan Speed / Hatch Spacing
•	Surface Condition: As-built, machined, shot peened, polished
•	Porosity Metrics: Total porosity, pore size, distribution
•	Surface Roughness Parameters: Sa, Sz, Sp, Sv
•	Stress Level: Applied cyclic stress amplitude
•	Heat Treatment Condition
Dependent Variable (Target)
•	Fatigue Life (cycles to failure) – a continuous regression target.
Source
Dataset provided as project input:
Capstone data – Fatigue of LPBF AlSi10Mg.xlsx
________________________________________
Tools & Libraries
•	Python
•	pandas – Data cleaning and processing
•	numpy – Statistical operations
•	matplotlib & seaborn – Visualization
•	scikit-learn – Baseline & advanced regression models
•	Jupyter Notebook – Analysis environment
________________________________________
Key EDA Insights
(Examples — modify based on your actual EDA results)
•	Higher porosity and rougher surfaces → shorter fatigue life
•	Machined and shot-peened specimens show significantly improved fatigue resistance
•	Stress amplitude has a strong inverse logarithmic relationship with fatigue life
•	Build orientation affects defect distribution → influences fatigue performance
•	Several variables exhibit nonlinearity → supports ML-based modeling
Figures include:
•	Histograms of fatigue life distribution
•	Boxplots for surface conditions
•	Correlation heatmaps
•	Scatterplots and regression lines (stress vs. life)
•	Outlier detection (Z-score / IQR / boxplots)
________________________________________
Baseline Model
A Random Forest Regressor was selected as the baseline due to:
•	Good handling of nonlinear relationships
•	Insensitivity to feature scaling
•	Ability to rank feature importance
•	Robust performance with engineering datasets
Evaluation Metric
•	R² Score (Coefficient of Determination)
•	RMSE (Root Mean Square Error)
Reason for Metric Choice
•	Fatigue life has large numeric range, so RMSE is suitable to measure prediction error magnitude.
•	R² provides a normalized measure of goodness of fit for regression models.
Baseline Performance (Example)
(Update with your actual outputs)
•	R²: 0.78
•	RMSE: 0.27 (log-scale fatigue life)
________________________________________
Advanced Modeling
Future refinement in Module 24 will include:
•	XGBoost Regressor
•	Gradient Boosting Regressor
•	Lasso/Ridge for comparison
•	Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)
•	Cross-validation and final model selection
•	SHAP values for explainability
________________________________________
Repository Structure
File / Folder	Description
Capstone_20_1_EDA.ipynb	Main notebook with full EDA, cleaning, feature engineering
baseline_model_results.csv	Baseline model evaluation metrics
capstone20_1_plots/	All generated figures and diagrams
Fatigue_Data.xlsx	Full dataset
README.md	Project documentation
report_summary.pdf	Initial capstone EDA report (Module 20.1)
LICENSE	MIT License
capstone20_1_full_submission.zip	Complete packaged submission
________________________________________
How to Run
git clone https://github.com/erfmlk/fatigue-life-capstone.git
cd fatigue-life-capstone
Open the notebook:
jupyter notebook Capstone_20_1_EDA.ipynb
________________________________________
Summary of Findings
•	Fatigue life is strongly influenced by stress amplitude, surface condition, and porosity indicators.
•	Nonlinear behavior suggests ML models outperform simple linear regression.
•	Feature engineering (log-life, normalized roughness, effective energy density) improves signal quality.
•	Baseline Random Forest model demonstrates good predictive capability and serves as the foundation for further refinement.
________________________________________
License
This project is released under the MIT License.

