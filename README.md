🩺 Diabetes Risk Factor EDA
Exploratory Data Analysis on the Pima Indians Diabetes Dataset to identify key risk factors for diabetes using Python.

📌 Overview
This project performs a thorough EDA on a dataset of 768 patient records to understand which health indicators are most strongly associated with diabetes. The analysis covers data cleaning, univariate and bivariate exploration, correlation analysis, and feature-specific deep dives into Glucose, BMI, and Age.

📂 Dataset
Source: Pima Indians Diabetes Database – UCI ML Repository (via Kaggle)
FeatureDescriptionPregnanciesNumber of pregnanciesGlucosePlasma glucose concentration (2-hour OGTT)BloodPressureDiastolic blood pressure (mm Hg)SkinThicknessTriceps skin fold thickness (mm)Insulin2-hour serum insulin (mu U/ml)BMIBody mass index (weight in kg/(height in m)²)DiabetesPedigreeFunctionDiabetes likelihood based on family historyAgeAge in yearsOutcomeTarget variable — 1: Diabetic, 0: Non-Diabetic

🧹 Data Cleaning
Several features (Glucose, BloodPressure, SkinThickness, Insulin, BMI) contained biologically impossible zero values. These were treated as missing and replaced with the column median to preserve data integrity without distorting distributions.

📊 Analysis Performed

Class distribution — count plot and pie chart of diabetic vs non-diabetic cases
Feature distributions — histograms with KDE curves for all 8 features
Boxplots by outcome — comparing feature ranges across diabetic vs non-diabetic groups
Correlation heatmap — identifying which features correlate most strongly with the outcome
Glucose deep dive — KDE distribution and diabetes rate above/below the 140 threshold
BMI analysis — diabetes rate by WHO BMI category (Underweight / Normal / Overweight / Obese)
Age group analysis — diabetes rate across four age bands (21–30, 31–40, 41–50, 50+)
Pairplot — scatter relationships among top features (Glucose, BMI, Age, Insulin) by outcome


🔑 Key Findings

The dataset has a 34.9% diabetic prevalence (268 out of 768 records)
Glucose is the strongest predictor — patients with glucose > 140 are significantly more likely to be diabetic (~3x higher rate)
Obese patients show a considerably higher diabetes rate compared to those with normal BMI
Age > 40 is associated with a higher diabetes rate than age ≤ 30
Top 3 features correlated with the outcome: Glucose → BMI → Age


🛠️ Tech Stack
ToolPurposePython 3Core languagepandasData manipulation and cleaningNumPyNumerical operationsMatplotlibBase plottingSeabornStatistical visualizations

🚀 How to Run

Clone the repository:

bash   git clone https://github.com/sungits23/diabetes-risk-factor-eda.git
   cd diabetes-risk-factor-eda

Install dependencies:

bash   pip install pandas numpy matplotlib seaborn

Open the notebook:

bash   jupyter notebook diabetes-risk-factor-eda.ipynb

Note: If running on Kaggle, the dataset path is pre-configured. For local use, download the dataset from the link above and update the pd.read_csv() path accordingly.


👩‍💻 Author
Sania Roy
B.Sc. (Hons) Data Science | Techno India University
GitHub
