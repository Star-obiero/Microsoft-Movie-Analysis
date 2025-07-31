

# Microsoft Movie Analysis

## Overview

This project explores the key factors that contribute to a movie's box office success. Microsoft is considering entering the original film production market, and this analysis helps identify patterns in genres, directors, runtime, budget, and audience ratings that influence a film's total gross revenue.

## Business Problem

Microsoft wants to understand what makes a movie financially successful in order to guide future investments in original video content. By analyzing historical movie data, we aim to discover trends and correlations that point to high-grossing films.

## Data

The dataset was formed by merging movie information from IMDb and Box Office Mojo. It includes the following features:

* `start_year`: Release year of the movie
* `runtime_minutes`: Length of the movie
* `genres`: One or more genres per film
* `averagerating`: IMDb average rating
* `numvotes`: Number of votes on IMDb
* `total_gross`: Total revenue generated (target variable)
* `director`, `budget`, and other supporting features

We cleaned the data by:

* Handling multiple genres via `.str.split()` and `.explode()`
* Removing or imputing missing values
* Converting financial and numerical columns to appropriate formats

## Methods

We conducted exploratory data analysis and modeling in the following steps:

### Correlation Analysis

A correlation heatmap was used to examine linear relationships between `total_gross` and other numeric variables. Key takeaways:

* `numvotes` had the strongest positive correlation with `total_gross` (0.67)
* `averagerating` also showed a positive, though weaker, correlation

### Grouped Visualizations

We built bar plots showing how total gross varies by genre and release year. By splitting multi-genre entries, we accurately visualized:

* Average gross per genre per year
* Trends across time that reveal which genres consistently perform well

### Iterative Refinement

We improved our approach by:

* Starting with scatter plots and histograms
* Cleaning and exploding genres for more granular analysis
* Dropping irrelevant columns and formatting currency values
* Imputing missing values with mean or mode where appropriate

These techniques helped us extract meaningful signals from the data and refine our understanding of what drives box office success.

## Evaluation

Our exploratory analysis effectively addressed the business problem, even without predictive modeling.

**Key insights include:**

* Genres like **Action** and **Adventure** dominate in total gross performance.
* Directors like **Christopher Nolan** and **Steven Spielberg** consistently lead high-grossing projects.
* **Summer releases** (especially May to July) outperform other months.
* **Higher budgets** generally correlate with higher gross, though with diminishing returns.
* Films between **100 and 130 minutes** long tend to perform better.

Although we did not build a regression or machine learning model, our visual and statistical evidence strongly supports actionable conclusions.

**Confidence in Generalization:**

* The data reflects a wide range of films from 2010–2018
* The strong performance of genres and patterns over time suggest robust trends
* However, changes in streaming consumption or global events could affect future applicability

## Conclusions

### Summary & Recommendations

From our analysis, Microsoft should:

* Focus on producing **Action** and **Adventure** films
* Aim for **Season releases** to maximize box office potential
* Monitor **IMDb ratings** and **vote counts** as proxies for audience engagement
* Invest in **well-budgeted** projects, while managing cost-effectiveness

### Limitations

* Missing values required imputation or reduced the sample size
* No machine learning models were deployed to predict gross revenue
* Streaming data and modern distribution models were not included

### Next Steps

To enhance this analysis:

* Build a linear regression model to predict `total_gross`
* Add features like marketing spend, star power, and international sales
* Expand the dataset to include post-2019 data and streaming metrics

This project provides a strong foundation for Microsoft's strategic entry into movie production based on real-world data and clear trends.

![blueprint](images/blueprint.png)


