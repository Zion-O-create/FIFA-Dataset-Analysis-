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

### 💡 Tips for Customization:
1. **Dataset Year:** If you are specifically using FIFA 21, 22, or 23, update the Title (e.g., # FIFA 23 Dataset Analysis).
2. **Screenshots:** I recommend creating a folder named `plots` and adding an image of your best graph to the README using `![Alt Text](plots/graph.png)`. This makes the project much more professional.
3. **Requirements:** If you don't have a `requirements.txt` yet, you can create one by running `pip freeze > requirements.txt` in your terminal.
