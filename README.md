# SpaceX Falcon 9 First Stage Landing Prediction

## Project Overview

This project is a comprehensive analysis of SpaceX Falcon 9 rocket launches with the goal of predicting the landing outcome of the first stage. The ability to reuse the first stage is a major cost-saving factor for SpaceX, and predicting this outcome can be valuable for competing launch providers.

The project is structured as a series of Jupyter notebooks that guide you through the complete data science pipeline:

* **Data Collection:** We begin by collecting raw data from a Wikipedia page using web scraping with `BeautifulSoup` and from the SpaceX REST API using the `requests` library.
* **Data Wrangling:** The raw data, which contains missing values and non-uniform formats, is cleaned and prepared. We convert the data into a structured Pandas DataFrame, handle missing values, and transform categorical variables.
* **Exploratory Data Analysis (EDA):** We perform an in-depth analysis of the data to uncover relationships between various factors (e.g., payload mass, orbit type, launch site) and the landing success rate. This is done using data visualization libraries like `Seaborn` and `Matplotlib`.
* **Geospatial Analysis:** Using the `Folium` library, we visualize the geographical locations of the launch sites and plot the outcomes of each launch on an interactive map. We also analyze the proximity of launch sites to important geographical features.
* **Machine Learning Prediction:** We build and train several classification models to predict the landing outcome (`1` for success, `0` for failure). The models used include Logistic Regression, Support Vector Machines, Decision Trees, and K-Nearest Neighbors. We use `GridSearchCV` to tune the hyperparameters of each model and evaluate their performance on test data.

## Notebooks in this Repository

1.  `jupyter-labs-webscraping.ipynb`: Collects and cleans launch data from Wikipedia.
2.  `jupyter-labs-spacex-data-collection-api.ipynb`: Fetches and processes launch data from the SpaceX API.
3.  `labs-jupyter-spacex-data-wrangling.ipynb`: Merges and cleans the datasets, including handling missing values and creating a binary classification label (`Class`).
4.  `edadataviz.ipynb`: Performs exploratory data analysis (EDA) to visualize relationships between key variables and launch success.
5.  `lab_jupyter_launch_site_location.ipynb`: Conducts interactive geospatial analysis of launch sites using Folium.
6.  `SpaceX_Machine Learning Prediction.ipynb`: Develops and evaluates machine learning models to predict the landing outcome.

## How to Use

To run the notebooks, you need a Python environment with the following libraries installed:
* `pandas`
* `numpy`
* `requests`
* `BeautifulSoup4`
* `seaborn`
* `matplotlib`
* `folium`
* `scikit-learn`

You can install them using pip:
`pip install pandas numpy requests beautifulsoup4 seaborn matplotlib folium scikit-learn`

Then, you can open and run the notebooks in a Jupyter environment. Make sure to run the cells in sequential order.
