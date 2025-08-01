# SuperHero Data Analysis Notebook

## Overview

This project uses the `SuperHero.ipynb` Jupyter Notebook to analyze and visualize superhero data from DC Comics and Marvel Comics. The notebook loads, cleans, merges, and explores several CSV datasets, and stores them in a SQLite database for advanced querying and analysis.

---

Project Summary
This project analyzes comic book superheroes from DC Comics and Marvel Comics using Python, Pandas, Matplotlib, Seaborn, and SQLite. The workflow includes:

Data Import: Multiple CSV files are loaded for DC, Marvel, hero attributes, and powers.
Data Cleaning: Null values are replaced with 'Unknown', and further filtering removes 'Unknown' and nulls for analysis.
Database Integration: Cleaned data is imported into SQLite tables for efficient querying and joining.
Filtering: Only DC and Marvel heroes are included in the powers table.
Analysis Functions:
Gender distribution and deceased hero ratios by publisher.
Pie charts and bar charts visualize gender and creation year trends.
SQL joins display hero stats and powers together.
Visualization: Results are shown using pie charts (with legend showing sex count and percent) and bar charts (by year and gender).
The project provides interactive analysis and clear visualizations to explore the diversity and history of comic book heroes

---

## Getting Started

### 1. **Requirements**

- Python 3.x
- Jupyter Notebook
- Required libraries:
  - pandas
  - matplotlib
  - seaborn
  - numpy
  - sqlite3

You can install the required libraries using:

```bash
pip install pandas matplotlib seaborn numpy
```

---

### 2. **Data Files**

Place the following CSV files in a `data/` folder in your project directory:

- `dc-wikia-data_updated.csv`
- `marvel-wikia-data_update.csv`
- `superheroes_data.csv`
- `superheroes.csv`

---

### 3. **How to Use the Notebook**

1. **Open `SuperHero.ipynb` in Jupyter Notebook or VS Code.**

2. **Run the notebook cells in order:**

   - The notebook will:
     - Import all required libraries.
     - Load the CSV files into pandas DataFrames.
     - Display sample data and column names for exploration.
     - Filter and clean the data as needed.
     - Create and populate SQLite tables for each dataset.
     - Provide functions for interactive analysis and visualization.

3. **Key Functions:**

   - **Drop Table:**  
     Drop any table from the SQLite database if needed and you want to test the table creation and importing process.
   - **hero_gender_distribution():**  
     Prompts for a publisher and displays the gender distribution of heroes in a line chart.
   - **deceased_hero_gender_ratio():**  
     Prompts for a publisher and shows the gender ratio of deceased heroes using a horizontal bar chart.
   - **join_publisher_with_powers_and_display():**  
     Prompts for a publisher and displays a merged table of heroes and their powers. This uses a SQL Join Statement.
   - **hero_gender_exploded_pie_chart():**  
     Prompts for a publisher and displays a pie chart based on the Gender of the heroes. Shows a count of each gender as well as a percentage of the data set. This is an exploded pie chart to make it easier to read the lower values.
   - **hero_year_40yr_bar_chart():**  
     Displays a vertical bar chart based on how many characters were released by publisher every 40 years.
   - **hero_year_40yr_bar_chart_by_sex():**  
     Displays a vertical bar chart based on how many characters were released by publisher every 40 years seperating each section by gender.

4. **Custom Queries:**  
   You can modify or add new SQL queries and pandas operations to explore the data further.

---

## Example Usage

- To see the gender distribution for DC Comics heroes, run the cell with `hero_gender_distribution()` and enter `DC Comics` when prompted.
- To join DC heroes with their powers, run the cell with `join_publisher_with_powers_and_display()` and enter `DC Comics`.

---

## Notes

- Make sure your CSV files are correctly named and located in the `data/` directory.
- The notebook will create a SQLite database file named `Hero.db` in your project directory.
- You can extend the notebook with your own analysis and visualizations.

---

## Troubleshooting

- If you encounter errors about missing columns or tables, check that your CSV files match the expected format.
- If you add new data, re-run the relevant cells to update the database and DataFrames.

---

## License

This project is for educational and non-commercial use.

---

## I obtained the datasets from the following locations.

Superhero Power Analytics: https://www.kaggle.com/datasets/shreyasur965/super-heroes-dataset/data?select=superheroes_data.csv (sourced from superheroapi.com)

Comic Characters: https://www.kaggle.com/datasets/vipulgote4/comic-characters/data?select=marvel-wikia-data_csv.csv (Both DC & Marvel found here)

Superhero Characters and Powers: https://www.kaggle.com/datasets/baraazaid/superherodb?resource=download (plan on using this as a look-up to display the abilities of each hero)

I would like to try and use BeautifulSoup to scrub superheroapi.com into my database to ensure I have the latest data for each character. However when I tried importing it, I successfully installed the package but I consistently ran into an error stating 'No module named 'beautifulsoup4''
