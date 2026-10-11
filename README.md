# Movie Investment Analysis

## Project Overview

This project explores movie financial performance from an investment perspective.

The main objective is to analyse how production budget and movie genre are related to revenue, profitability and return on investment (ROI), and to evaluate whether historical movie data can support investment decisions.

The project combines:

- exploratory data analysis,
- financial analysis,
- data visualisation,
- basic machine learning,
- business interpretation of the results.

## Business Questions

The analysis focuses on several key questions:

1. Which movie genres generate the highest average profits?
2. Which genres provide the highest return on investment?
3. Does a higher production budget lead to better financial performance?
4. Which genres provide the best balance between absolute profit and capital efficiency?
5. Can a simple machine learning model help estimate movie revenue?

## Dataset

The project uses the TMDB 5000 Movie Dataset, including information such as:

- movie title,
- production budget,
- revenue,
- genres,
- popularity and other movie characteristics.

The main financial metrics used in the analysis are:

*Profit*

Profit = Revenue - Budget

*Return on Investment (ROI)*

ROI = Profit / Budget × 100

## Key Findings

The analysis identified different investment profiles across movie genres.

- *Animation* generated the highest average absolute profit.
- *Family, Science Fiction and Adventure* showed a strong combination of profitability and median ROI.
- *Horror* generated the highest median ROI, suggesting strong capital efficiency despite lower average absolute profit.
- *Action* movies generated relatively high profits but showed lower investment efficiency compared with several other genres.

Genres with very small sample sizes were excluded from selected comparisons to improve the reliability of the analysis.

## Business Interpretation

Based on the analysed historical data:

- Family, Science Fiction and Adventure showed a good balance between average profit and median ROI.
- Horror had the highest median ROI, but lower average profit.
- Animation generated the highest average profit, but also required higher production budgets.

These results show that movie genres can differ significantly in terms of profitability and ROI. However, genre alone is not enough to predict the financial success of a movie.


## Machine Learning

A basic machine learning approach was used to estimate movie revenue.

Two regression models were tested:
- Linear Regression
- Random Forest Regressor

The Random Forest model was further optimized using GridSearchCV.

The best parameters were:
- max_depth: 5
- min_samples_split: 5
- n_estimators: 200

After tuning, the Random Forest model achieved:
- R² ≈ 0.52
- MAE ≈ 83.8 million

The optimized model showed a small improvement compared with the initial Random Forest model. However, it was still unable to reliably identify loss-making movies.

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Visual Studio Code

## Project Structure

```movie_investment_project/
│
├── data/
│   ├── tmdb_5000_movies.csv
│   └── tmdb_5000_credits.csv
│
├── movie_analysis.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

1. Clone or download the repository.
2. Install the required Python packages:

   pip install -r requirements.txt

3. Open movie_analysis.ipynb in Jupyter Notebook or Visual Studio Code.
4. Run the notebook from top to bottom.

## Skills Demonstrated

- Data loading and cleaning with Pandas
- Exploratory data analysis
- Financial metrics calculation
- Data visualisation with Matplotlib
- Basic machine learning with Scikit-learn
- Interpretation of model results
- Business-oriented data analysis