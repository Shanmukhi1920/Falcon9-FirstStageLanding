# SpaceX Falcon 9 Launch Analysis and Prediction

## Project Overview
This project analyzes SpaceX Falcon 9 rocket launches to predict landing outcomes and estimate costs, aiming to inform competitive bidding strategies in the space industry. It combines diverse data collection methods, comprehensive exploratory data analysis, and machine learning techniques to provide actionable insights. The study culminates in an interactive dashboard for visualizing key metrics, offering a powerful tool for understanding factors influencing launch success and costs in the commercial space sector.

## Datasets

* `Spacex.csv`: Primary dataset containing information about SpaceX launches.
* `spacex_launch_dash.csv`: Dataset prepared for use in the Plotly Dash application.
* `spacex_web_scraped.csv`: Dataset created from web scraping, containing additional launch information.

## Methodology

### Data Collection

Data for this project was collected using two methods:

1. **API Data Collection** (`Data Collection API.ipynb`):
   - Utilized SpaceX API to extract launch information
   - Developed helper functions to process API data
   - Converted extracted data into a pandas DataFrame

2. **Web Scraping** (`Data Collection with Webscrapping.ipynb`):
   - Scraped historical launch records from Wikipedia
   - Used BeautifulSoup to extract table data
   - Processed HTML data and converted it to a DataFrame

The collected data is stored in the `data/` directory.

### Exploratory Data Analysis

EDA was performed using various techniques:

1. **Python EDA** (`EDA.ipynb`):
   - Analyzed null values and data types
   - Calculated launch frequencies by site and orbit type
   - Examined mission outcomes by orbit type

2. **SQL EDA** (`EDA with SQL.ipynb`):
   - Loaded data into IBM Db2 console
   - Executed various SQL queries to explore the dataset

3. **Data Visualization EDA** (`EDA with Data Visualization.ipynb`):
   - Created scatter plots, bar plots, and line charts
   - Performed feature engineering and one-hot encoding

### Data Visualization

Advanced visualizations were created using:

1. **Folium** (`Interactive Visual Analytics with Folium Lab.ipynb`):
   - Mapped launch sites and outcomes
   - Analyzed proximities to launch sites

2. **Plotly Dash** (`scripts/spacex_dash_app.py`):
   - Developed an interactive dashboard
   - Created a pie chart for successful launches by site
   - Produced a scatter plot for payload mass vs. launch class

### Machine Learning Prediction

Machine learning models were developed in `Machine Learning Prediction.ipynb`:

- Preprocessed data: standardization and transformation
- Split data into training and test sets (80/20 split)
- Implemented multiple classifiers: Logistic Regression, SVM, Decision Tree, KNN
- Performed hyperparameter tuning using GridSearchCV
- Evaluated models using accuracy scores and confusion matrices

### Interactive Dashboard

- Developed an interactive dashboard using Plotly Dash to visualize key metrics and allow for user interaction with the data.

## Installation and Usage
```bash
git clone https://github.com/Shanmukhi1920/Predicting_SpaceX_Falcon9_FirstStageLanding
cd Predicting_SpaceX_Falcon9_FirstStageLanding
jupyter notebook
```

Then, open the desired notebook in the `notebooks/` directory.

To run the Dash application:
```bash
python scripts/spacex_dash_app.py
```

## Results and Conclusions

- All implemented models achieved an accuracy of approximately 83.3% on the test data
- For detailed results and insights, please refer to the `DS Presentation.pdf` in the `docs/` directory
