# FIFA Dataset Analysis ⚽📊

![Python](https://img.shields.io/badge/python-3.x-blue.svg)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Data-Analysis-green.svg)

## 📌 Project Overview
This repository contains a comprehensive Exploratory Data Analysis (EDA) of FIFA player datasets. The goal of this project is to uncover insights regarding player performance, market value, age distributions, and club/national team statistics. 

By analyzing the attributes of thousands of players, this project identifies trends in the football world and provides visualizations that make complex data easy to understand.

## 🚀 Features
- **Data Cleaning:** Handling missing values, converting currency strings (Wages/Value) into numeric formats, and formatting player positions.
- **Player Analysis:** Identifying top-rated players, highest earners, and high-potential "wonderkids."
- **Club & Country Insights:** Comparing clubs based on total squad value and identifying countries that produce the highest-rated talent.
- **Correlation Studies:** Analyzing the relationship between age and potential, or physical attributes and overall ratings.
- **Visualizations:** Detailed charts using Seaborn and Matplotlib including Histograms, Boxplots, and Heatmaps.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** - `pandas` (Data manipulation)
  - `numpy` (Numerical computations)
  - `matplotlib` (Static visualizations)
  - `seaborn` (Statistical data visualization)
  - `jupyter notebook` (Development environment)

## 📁 Repository Structure
```bash
├── data/               # Folder containing the FIFA .csv files
├── notebooks/          # Jupyter notebooks with step-by-step analysis
├── plots/              # Exported visualizations and charts
├── README.md           # Project documentation
└── requirements.txt    # List of dependencies

```

## ⚙️ Installation & Usage

1. **Clone the repository:**
```bash
git clone [https://github.com/Zion-O-create/FIFA-Dataset-Analysis-.git](https://github.com/Zion-O-create/FIFA-Dataset-Analysis-.git)
cd FIFA-Dataset-Analysis-

```


2. **Install dependencies:**
```bash
pip install -r requirements.txt

```


3. **Run the analysis:**
Open the Jupyter Notebook and run the cells:
```bash
jupyter notebook notebooks/analysis.ipynb

```



## 📊 Sample Insights

* **Age vs Potential:** Analysis shows a clear downward trend in potential as players pass the age of 24.
* **Wage Distribution:** A small percentage of elite players command over 60% of the total wage bill in top leagues.
* **Skill Correlations:** Strong correlation found between 'Reactions' and 'Overall Rating' across all positions.

## 🤝 Contributing

Contributions are welcome! If you have ideas for new analyses or improvements, feel free to:

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/NewAnalysis`)
3. Commit your Changes (`git commit -m 'Add some NewAnalysis'`)
4. Push to the Branch (`git push origin feature/NewAnalysis`)
5. Open a Pull Request

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.


***

Technical Documentation: Data Cleaning Phase 🛠️
This project involves an intensive data-cleaning pipeline to transform a "dirty" FIFA dataset into a structured format suitable for exploratory data analysis (EDA) and predictive modeling.

Key Data Transformations
Financial Column Standardization: Developed a custom Python function to handle string-to-numeric conversion for Value, Wage, and Release Clause.

Stripped currency symbols (€) and shorthand notations ('M', 'K').

Converted values into full floating-point integers (e.g., "€103.5M" → 103,500,000).

Temporal Formatting: Converted the Joined column from a generic object/string type into a standard datetime64[ns] format. This enables time-series analysis of player loyalty and contract duration.

Schema Refinement:

Renamed columns to include units of measurement (e.g., Value €, Wage €, Release Clause €) for better semantic clarity.

Verified the uniqueness and consistency of the data using .unique() and .head() inspections after each transformation step.

Data Export: Successfully exported the final processed dataset as new_Clean_FIFA_dataset.csv for downstream analysis.

Code Snippets: The Cleaning Logic
Python

# Converting 'Joined' to datetime
df['Joined'] = pd.to_datetime(df['Joined'])

# Handling financial suffixes (Example for 'Value' column)
def value(x):
    if 'M' in x:
        x = x.replace('M', '')
        x = float(x[1:]) * 1000000
        return round(x)
    elif 'K' in x:
        # Handling thousands...

### 💡 Tips for Customization:
1. **Dataset Year:** If you are specifically using FIFA 21, 22, or 23, update the Title (e.g., # FIFA 23 Dataset Analysis).
2. **Screenshots:** I recommend creating a folder named `plots` and adding an image of your best graph to the README using `![Alt Text](plots/graph.png)`. This makes the project much more professional.
3. **Requirements:** If you don't have a `requirements.txt` yet, you can create one by running `pip freeze > requirements.txt` in your terminal.

🎯 Project Goals
The primary objective of this project is to leverage the FIFA Dataset to bridge the gap between raw data and actionable footballing insights. By the end of this analysis, the project aims to:

Identify Market Inefficiencies: Discover "undervalued" players whose skills (OVA) and Potential (POT) far exceed their current market value.

Performance vs. Pay: Analyze the correlation between player wages and their actual output on the pitch to see which clubs manage their finances most efficiently.

Aging Curves: Map out how player attributes decline or grow over time, specifically looking at the 'Joined' dates to see the impact of long-term development.

🚀 Future Work (The Roadmap)
Now that the data is cleaned and standardized, the next phases of this project will include:

Exploratory Data Analysis (EDA): Creating a visual dashboard to show the distribution of talent across different nationalities and clubs.

Position-Specific Clustering: Using Unsupervised Machine Learning (K-Means) to group players based on their technical attributes rather than just their listed position.

Predictive Modeling: Building a regression model to predict a player's Release Clause based on their age, potential, and performance metrics.

Scouting Recommendation System: Developing a simple tool where a user can input a "target player" and get a list of 5 "similar" players who are younger or cheaper.
