# SuperHero Data Analysis Notebook

## Objective

I was wondering what the gender spread looks like for comics through time. I also wanted a way to compare information about comic characters between the two major comic companies and if there have been any female characters that are deceased and if so, what's the percent of female to male deaths throughout the years.

## Overview

This project uses the `SuperHero.ipynb` Jupyter Notebook to analyze and visualize superhero data from DC Comics and Marvel Comics. The notebook loads, cleans, merges, and explores several CSV datasets, and stores them in a SQLite database for advanced querying and analysis.

---

### Setting up the Virtual Environment

## Project Setup Instructions:

- Fork the repository and clone to your computer.

- Open the repository folder in a code editor; and create the virtual environment in that folder.

- Create and Activate a Virtual Environment (commands below)

- Install the requirements.txt file

- Run the `SuperHero.ipynb`

- This program will ask for user input at times.

- When you are finished, deactivate the virtual environment and close the repository folder.

## Virtual Environment Commands

| **Command** | **Linux/Mac**                     | **Windows/GitBash**               |
| ----------- | --------------------------------- | --------------------------------- |
| Create      | `python3 -m venv venv`            | `python -m venv venv`             |
| Activate    | `source venv/bin/activate`        | `source venv/Scripts/activate`    |
| Install     | `pip install -r requirements.txt` | `pip install -r requirements.txt` |
| Deactivate  | `deactivate`                      | `deactivate`                      |

---

## **Data Dictionary**

Below are the main columns used in the superhero datasets and their descriptions:

### DC & Marvel Comics Data (`dc-wikia-data_updated.csv`, `marvel-wikia-data_update.csv`)

| Column Name      | Description                                       |
| ---------------- | ------------------------------------------------- |
| id               | Unique identifier for the character               |
| name             | Character's name                                  |
| identity         | Secret or public identity status                  |
| align            | Alignment (good, bad, neutral, etc.)              |
| eye              | Eye color                                         |
| hair             | Hair color                                        |
| sex              | Gender/Sex (Male, Female, etc.)                   |
| alive            | Living status (living, deceased characters, etc.) |
| appearances      | Number of comic appearances                       |
| first_appearance | Issue of first appearance                         |
| year             | Year of first appearance                          |

### Superheroes Data (`superheroes_data.csv`)

| Column Name       | Description                                |
| ----------------- | ------------------------------------------ |
| id                | Unique identifier for the character        |
| name              | Character's name                           |
| intelligence      | Intelligence score                         |
| strength          | Strength score                             |
| speed             | Speed score                                |
| durability        | Durability score                           |
| power             | Power score                                |
| combat            | Combat ability score                       |
| full_name         | Full name of the character                 |
| alter_egos        | Alternate identities                       |
| aliases           | List of aliases                            |
| place_of_birth    | Place of birth                             |
| first_appearance  | Issue of first appearance                  |
| publisher         | Publisher (DC Comics, Marvel Comics, etc.) |
| alignment         | Alignment (good, bad, neutral, etc.)       |
| gender            | Gender/Sex                                 |
| race              | Race/Species                               |
| height            | Height (cm)                                |
| weight            | Weight (kg)                                |
| eye_color         | Eye color                                  |
| hair_color        | Hair color                                 |
| occupation        | Occupation                                 |
| base              | Base of operations                         |
| group_affiliation | Group/team affiliations                    |
| relatives         | Known relatives                            |
| url               | Reference URL                              |

### Superheroes Powers Data (`superheroes_updated.csv`)

| Column Name  | Description                                |
| ------------ | ------------------------------------------ |
| id           | Unique identifier for the character        |
| Creator      | Publisher (DC Comics, Marvel Comics, etc.) |
| Durability   | Durability score                           |
| Equipment    | Equipment used                             |
| Eye_color    | Eye color                                  |
| Gender       | Gender/Sex                                 |
| Hair_color   | Hair color                                 |
| IQ           | IQ score                                   |
| Intelligence | Intelligence score                         |
| Name         | Character's name                           |
| Occupation   | Occupation                                 |
| Power        | Power score                                |
| Relatives    | Known relatives                            |
| Speed        | Speed score                                |
| Strength     | Strength score                             |
| Super_powers | List of super powers                       |
| Weight       | Weight (kg)                                |

---

## Data Summary: Total Rows and Columns per Table

Below is a summary of the main tables/datasets used in this project, including the number of rows (records) and columns (fields) for each.

| Table / CSV File             | Rows (Records) | Columns |
| ---------------------------- | :------------: | :-----: |
| dc-wikia-data_updated.csv    |      6896      |   11    |
| marvel-wikia-data_update.csv |     16376      |   11    |
| superheroes_data.csv         |      734       |   27    |
| superheroes_updated.csv      |      667       |   16    |

---

## Technologies Used:

**Languages & Core Libraries:**\
_Python_ – primary language for data analysis and project development\
_Pandas_ – for data cleaning, transformation, and analysis

**Visualization Tools:**\
_Matplotlib_ – for basic charts and static visualizations\
_Plotly_ – for interactive graphs and visual exploration\
_Tableau_ – for building interactive dashboards and communicating insights visually

**Data Storage & Querying:**\
_SQLite_ – for lightweight, file-based data storage and SQL querying

**Development Environment:**\
_Jupyter Notebook_ – for exploratory data analysis and documenting workflows\
_VS Code_ – for script development and file management

**Version Control & Documentation:**\
_Git & GitHub_ – for version control and project sharing\
_Markdown_ – for notes, documentation, and explanations

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

## Data Sources

Superhero Power Analytics: https://www.kaggle.com/datasets/shreyasur965/super-heroes-dataset/data?select=superheroes_data.csv (sourced from superheroapi.com)

Comic Characters: https://www.kaggle.com/datasets/vipulgote4/comic-characters/data?select=marvel-wikia-data_csv.csv (Both DC & Marvel found here)

Superhero Characters and Powers: https://www.kaggle.com/datasets/baraazaid/superherodb?resource=download (plan on using this as a look-up to display the abilities of each hero)

I would like to try and use BeautifulSoup to scrub superheroapi.com into my database to ensure I have the latest data for each character. However when I tried importing it, I successfully installed the package but I consistently ran into an error stating 'No module named 'beautifulsoup4''

## Project Summary

In my research, I found that there were more genders than just Male and Female like I originally thought. Also that there were a lot more Female deceased characters from both Publishers than I knew about.
