# 🚀 Winning Space Race with Data Science
## IBM Data Science Professional Certificate — Capstone Project

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![IBM](https://img.shields.io/badge/IBM-Data%20Science%20Capstone-052FAD?logo=ibm&logoColor=white)
![License](https://img.shields.io/badge/License-GPL--3.0-green)

---

## 📋 Project Overview

SpaceX advertises Falcon 9 rocket launches at a cost of **$62 million**, while other providers charge upward of **$165 million**. The significant cost reduction is due to SpaceX's ability to **reuse the first stage of the rocket**. By predicting whether the first stage will land successfully, we can estimate the cost of a launch — giving a competitor the ability to **bid more effectively against SpaceX**.

This project applies the **full Data Science methodology** — from data collection and wrangling through exploratory analysis, visual analytics, and machine learning — to answer:

> **Can we predict whether SpaceX will successfully land Falcon 9's first stage booster?**

---

## 🎯 Objectives

- Collect SpaceX Falcon 9 launch data via REST API and Wikipedia web scraping
- Perform data wrangling and feature engineering
- Conduct Exploratory Data Analysis (EDA) using SQL and Python visualizations
- Build interactive dashboards using Folium and Plotly Dash
- Train and compare multiple ML classification models
- Identify the best model to predict first-stage landing success

---

## 📁 Repository Structure

```
IBM-DataScience-Capstone-SpaceX/
│
├── 📓 Notebooks/
│   ├── jupyter-labs-spacex-data-collection-api.ipynb        # Week 1 – SpaceX API
│   ├── jupyter-labs-webscraping.ipynb                        # Week 1 – Web Scraping
│   ├── labs-jupyter-spacex-Data wrangling.ipynb              # Week 2 – Data Wrangling
│   ├── edadataviz.ipynb                                      # Week 3 – EDA & Visualization
│   ├── jupyter-labs-eda-sql-coursera_sqllite.ipynb           # Week 3 – EDA with SQL
│   ├── lab_jupyter_launch_site_location.ipynb                # Week 4 – Folium Maps
│   ├── SpaceX_Machine Learning Prediction_Part_5.ipynb       # Week 5 – ML Prediction
│
│
├── 📱 Dashboard/
│   └── app.py                      # Plotly Dash interactive app
│
├── 📄 Presentation/
│   ├── SpaceX_Capstone_Presentation.pptx
│   └── SpaceX_Capstone_Presentation.pdf
│
└── README.md
```

---

## 📓 Notebooks — Description

### Week 1: Data Collection

| Notebook | Description |
|----------|-------------|
| [`jupyter-labs-spacex-data-collection-api.ipynb`](jupyter-labs-spacex-data-collection-api.ipynb) | Collects Falcon 9 launch data using the SpaceX REST API. Extracts flight number, payload mass, orbit, launch site, and landing outcome. Outputs `dataset_part_1.csv` |
| [`jupyter-labs-webscraping.ipynb`](jupyter-labs-webscraping.ipynb) | Scrapes Falcon 9 launch records from Wikipedia using BeautifulSoup. Outputs `spacex_web_scraped.csv` |

### Week 2: Data Wrangling

| Notebook | Description |
|----------|-------------|
| [`labs-jupyter-spacex-Data wrangling.ipynb`](labs-jupyter-spacex-Data%20wrangling.ipynb) | Cleans missing values, creates the binary `Class` label (1 = landing success, 0 = failure), applies one-hot encoding to categorical features. Outputs `dataset_part_2.csv` |

### Week 3: Exploratory Data Analysis

| Notebook | Description |
|----------|-------------|
| [`edadataviz.ipynb`](edadataviz.ipynb) | Creates scatter plots, bar charts, and line charts using Matplotlib and Seaborn to explore relationships between payload, orbit, launch site, and landing success |
| [`jupyter-labs-eda-sql-coursera_sqllite.ipynb`](jupyter-labs-eda-sql-coursera_sqllite.ipynb) | Loads the SpaceX dataset into SQLite and performs SQL queries to explore launch sites, payloads, landing outcomes, and booster statistics |

### Week 4: Interactive Visual Analytics

| Notebook | Description |
|----------|-------------|
| [`lab_jupyter_launch_site_location.ipynb`](lab_jupyter_launch_site_location.ipynb) | Creates interactive Folium maps showing all 4 launch sites with success/failure markers, proximity analysis (coast, city, highway, railway), and circle overlays |
| [`app.py`](app.py) | Plotly Dash application with dropdown for launch site selection, pie chart for success count, payload range slider, and scatter plot of payload vs. outcome by booster version |

### Week 5: Predictive Analysis

| Notebook | Description |
|----------|-------------|
| [`SpaceX_Machine Learning Prediction_Part_5.ipynb`](SpaceX_Machine%20Learning%20Prediction_Part_5.ipynb) | Trains Logistic Regression, SVM, Decision Tree, and KNN classifiers. Uses GridSearchCV for hyperparameter tuning. Evaluates with confusion matrices and accuracy scores |

---

## 🔍 Key Findings

### 🏆 Best Model — Decision Tree Classifier
| Model | Test Accuracy | CV Accuracy |
|-------|:---:|:---:|
| Logistic Regression | 83.3% | 84.7% |
| Support Vector Machine | 83.3% | 84.8% |
| **Decision Tree** | **87.5%** | **87.1%** |
| K-Nearest Neighbors | 83.3% | 84.2% |

### 📊 EDA Insights
- **KSC LC-39A** has the highest landing success rate (**77.8%**)
- Landing success rate grew from **0% (2010–2014)** to **90% (2020)**
- **LEO and ISS** orbits show the highest success rates (100%)
- Payloads in the **2,000–5,000 kg range** have the best landing outcomes
- Heavier payloads (>6,000 kg) tend to have more failed landings

### 🗺️ Folium Findings
- All 4 launch sites are on the **coastline** — for safe ocean trajectories
- **VAFB SLC-4E** is ideal for polar orbits (furthest from populated areas)
- **KSC LC-39A** has the best infrastructure access (railways, highways)

### 📊 SQL Findings
- Total payload for NASA (CRS) missions: **~45,596 kg**
- First successful ground pad landing: **December 22, 2015**
- Average payload for Falcon 9 v1.1: **~2,928 kg**

---

## 🛠️ Technologies Used

| Category | Tools |
|----------|-------|
| Language | Python 3.8+ |
| Data Collection | `requests`, `BeautifulSoup4` |
| Data Processing | `pandas`, `numpy` |
| Visualization | `matplotlib`, `seaborn`, `plotly` |
| Interactive Maps | `folium` |
| Interactive Dashboard | `dash`, `plotly` |
| Database/SQL | `sqlite3`, `ibm_db_sa`, `SQLAlchemy` |
| Machine Learning | `scikit-learn` |
| Hyperparameter Tuning | `GridSearchCV` |
| Notebook Environment | Jupyter Notebook / JupyterLab |

---

## ⚙️ How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/IBM-DataScience-Capstone-SpaceX.git
cd IBM-DataScience-Capstone-SpaceX
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn folium dash plotly requests beautifulsoup4 sqlalchemy
```

### 3. Run the Notebooks
Open in JupyterLab and run in order:
1. Data Collection API notebook
2. Web Scraping notebook
3. Data Wrangling notebook
4. EDA Visualization notebook
5. EDA SQL notebook
6. Folium notebook
7. Machine Learning notebook

### 4. Run the Dash App
```bash
python app.py
```
Open browser at `http://127.0.0.1:8050/`

---

## 💡 Business Impact

| Scenario | Bid Price |
|----------|-----------|
| Model predicts **successful** first stage landing | **~$62M** |
| Model predicts **failed** first stage landing | **~$150M** |

With **87.5% accuracy**, the model gives a competitor reliable cost estimates to bid against SpaceX — a significant competitive advantage in the commercial launch market.

---

## 📜 License

This project is licensed under the **GPL-3.0 License** — see the [LICENSE](LICENSE) file for details.

---

## 🎓 Certificate

This project is the **Capstone** of the [IBM Data Science Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-science) on Coursera.

**Author:** Arijit Bose  
**Certificate:** IBM Data Science Professional Certificate  
**Year:** 2025–26

---

*Part of the IBM Data Science Professional Certificate — 10-course series covering Python, SQL, data visualization, machine learning, and applied data science.*
