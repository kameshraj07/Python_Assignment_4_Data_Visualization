🚕 Taxi Data Analysis & Visualization

📌 Project Overview

This project focuses on Exploratory Data Analysis (EDA), data cleaning, and data visualization using Python.

The Taxis dataset available through the Seaborn library is used to analyze taxi trips and understand patterns in fares, trip distances, tips, payment methods, pickup locations, and other numerical and categorical variables.

This project demonstrates practical applications of Pandas, NumPy, Matplotlib, and Seaborn for data manipulation, data cleaning, statistical analysis, and meaningful visualizations.

🎯 Project Objectives

The main objectives of this project are:

Load and explore the Seaborn Taxis dataset.

Identify and handle missing values.

Identify numerical and categorical columns.

Analyze taxi fares and trip distances.

Understand the distribution of trips across pickup boroughs.

Analyze different payment methods.

Study relationships between distance, fare, tip, and total amount.

Visualize correlations between numerical variables.

Compare fare distributions across payment methods.

Perform Exploratory Data Analysis using Matplotlib and Seaborn.

🗂️ Dataset Description

This project uses the built-in Taxis dataset provided by Seaborn.

Loading the Dataset

import seaborn as sns

# Load the Taxis dataset
taxis = sns.load_dataset("taxis")

Dataset Features

The dataset contains the following variables:

Column

Description

pickup

Pickup date and time

dropoff

Drop-off date and time

passengers

Number of passengers

distance

Trip distance

fare

Taxi fare amount

tip

Tip amount

tolls

Toll amount

total

Total trip amount

payment

Payment method

pickup_borough

Pickup borough

pickup_zone

Pickup zone

dropoff_borough

Drop-off borough

dropoff_zone

Drop-off zone

🧹 Data Cleaning and Preprocessing

Data cleaning is an important step in Exploratory Data Analysis.

1. Checking Missing Values

# Check missing values
taxis.isnull().sum()

2. Handling Missing Values Using Imputation

Numerical columns: Missing values are replaced using the median.

for column in numeric_columns:
    taxis[column] = taxis[column].fillna(taxis[column].median())

Categorical columns: Missing values are replaced using the mode.

for col in categorical_columns:
    if taxis[col].isnull().any() and not taxis[col].mode().empty:
        taxis[col] = taxis[col].fillna(taxis[col].mode()[0])

3. Removing Missing Values

Rows containing missing values in critical columns can be removed.

taxis = taxis.dropna(subset=critical_columns)

4. Verifying Cleaned Data

# Check missing values after cleaning
taxis.isnull().sum()

# Dataset information
taxis.info()

📊 Data Visualization and Analysis

This project includes 10 visualizations using Matplotlib, Pandas, and Seaborn.

Matplotlib / Pandas Visualizations

1. Line Chart – Fare Over Time

X-axis: Pickup Time

Y-axis: Fare

Purpose: Analyze changes in taxi fares over time.

2. Bar Chart – Total Fare by Pickup Borough

X-axis: Pickup Borough

Y-axis: Total Fare

Purpose: Compare total fare amounts across different boroughs.

3. Pie Chart – Trips by Payment Method

Purpose: Visualize the proportion of trips made using different payment methods.

4. Histogram – Distribution of Trip Distance

X-axis: Distance

Y-axis: Number of Trips

Purpose: Understand the distribution of taxi trip distances.

5. Box Plot – Tip Amount by Pickup Borough

X-axis: Pickup Borough

Y-axis: Tip Amount

Purpose: Compare tip distributions across pickup boroughs and identify outliers.

Seaborn Visualizations

6. Count Plot – Number of Trips by Pickup Borough

Purpose: Count the number of taxi trips originating from each borough.

7. Scatter Plot – Distance vs Fare

X-axis: Distance

Y-axis: Fare

Hue: Pickup Borough

Purpose: Understand the relationship between trip distance and fare.

8. Correlation Heatmap

The correlation matrix is calculated using the following numerical variables:

numerical_columns = [
    "distance",
    "fare",
    "tip",
    "tolls",
    "total"
]

correlation_matrix = taxis[numerical_columns].corr()

Purpose: Identify relationships and correlations between numerical variables.

9. Pair Plot – Numerical Variables

Variables:

Distance

Fare

Tip

Total

Hue: Pickup Zone

Purpose: Visualize pairwise relationships between multiple numerical variables.

10. Violin Plot – Fare by Payment Method

X-axis: Payment Method

Y-axis: Fare

Purpose: Compare fare distributions, spread, and density across payment methods.

🛠️ Technologies Used

Technology

Purpose

Python

Programming language

Pandas

Data manipulation and analysis

NumPy

Numerical operations

Matplotlib

Data visualization

Seaborn

Statistical data visualization

Jupyter Notebook

Development environment

Git & GitHub

Version control and project hosting

📁 Project Structure

Taxi-Data-Visualization/
│
├── Assignment4_2_Data_Visualization.ipynb
│
├── README.md
│
└── requirements.txt

⚙️ Installation and Setup

1. Clone the Repository

git clone YOUR_GITHUB_REPOSITORY_URL

2. Navigate to the Project Directory

cd Taxi-Data-Visualization

3. Install Required Libraries

pip install pandas numpy matplotlib seaborn jupyter

4. Launch Jupyter Notebook

jupyter notebook

5. Open the Notebook

Open the following file:

Assignment4_2_Data_Visualization.ipynb

Run the notebook cells sequentially to explore the dataset, perform data cleaning, and generate visualizations.

📌 Key Analysis Areas

This project provides hands-on experience in:

Data loading and inspection

Data type identification

Missing-value detection

Missing-value imputation

Data preprocessing

Group-by operations and aggregation

Correlation analysis

Univariate visualization

Bivariate visualization

Multivariate visualization

Categorical data analysis

Exploratory Data Analysis (EDA)

📈 Skills Demonstrated

Through this project, the following Data Science skills are demonstrated:

Python Programming

Pandas Data Analysis

NumPy

Data Cleaning and Preprocessing

Exploratory Data Analysis (EDA)

Matplotlib Visualization

Seaborn Visualization

Statistical Data Visualization

Correlation Analysis

Data Interpretation

👤 Author

A Kameshraj

Aspiring Data Scientist | Python | Pandas | Data Visualization | Machine Learning

⭐ If you find this project useful, feel free to explore the repository and provide feedback.

Thank you for visiting my project! 🚀
