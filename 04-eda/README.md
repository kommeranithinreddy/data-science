# Exploratory Data Analysis (EDA)

This section documents my hands-on EDA projects using real-world datasets.

The objective is to understand datasets, assess data quality, investigate patterns and relationships, visualize results, and communicate meaningful insights through data analysis.

## Projects

| Project | Dataset | Status |
|---|---|---|
| Titanic EDA | Titanic passenger dataset | Completed |
| Online Retail EDA | Online Retail transaction dataset | Completed |

---

# 1. Titanic EDA

## Project Overview

The Titanic dataset contains passenger information from the Titanic disaster.

This project investigates passenger characteristics and explores relationships between passenger attributes and survival outcomes.

### Dataset Information

| Attribute | Details |
|---|---|
| Rows | 891 |
| Columns | 12 |
| Unit of observation | One passenger |
| Target variable | `Survived` |

### Analysis Performed

- Inspected dataset structure, column names, and data types.
- Examined descriptive statistics.
- Identified missing values and investigated data quality.
- Analyzed numerical and categorical variables.
- Examined distributions using histograms.
- Investigated distributions and potential outliers using box plots.
- Compared categorical groups using bar charts.
- Explored relationships between numerical variables using scatter plots.
- Compared survival rates across passenger groups.
- Interpreted results and identified limitations.

### Key Findings

**Passenger class and survival**

| Passenger Class | Survival Rate |
|---|---:|
| First Class | 62.96% |
| Second Class | 47.28% |
| Third Class | 24.24% |

Passengers in first class had a higher observed survival rate than passengers in second and third class.

This demonstrates how grouping data and comparing rates can reveal meaningful relationships between variables.

### Data Quality Observations

- `Age` contains 177 missing values.
- `Cabin` contains missing values.
- `Embarked` contains missing values.
- `Survived` is a binary variable representing the survival outcome.

### Skills Practiced

- Dataset inspection
- Missing-value analysis
- Numerical and categorical analysis
- Distribution analysis
- Data visualization
- Grouped statistical comparisons
- Survival-rate calculations
- Interpretation of relationships between variables

---

# 2. Online Retail EDA

## Project Overview

This project analyzes retail transactions to understand revenue patterns, product performance, country-level sales, and customer purchasing behaviour.

The dataset covers transactions from a UK-based online retailer between December 2010 and December 2011.

**Dataset:** [UCI Machine Learning Repository — Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail)

**Notebook:** `online_retail_eda.ipynb`

### Dataset Information

| Attribute | Details |
|---|---|
| Original rows | 541,909 |
| Columns | 8 |
| Duplicate rows removed | 5,268 |
| Rows after duplicate removal | 536,641 |
| Missing customer IDs after duplicate removal | 135,037 |
| Missing product descriptions | 1,454 |

### Business Questions

- Which product descriptions generate the most revenue?
- Which countries contribute the most revenue?
- How does revenue change over time?
- Which customers contribute the most revenue?
- Which customers place orders most frequently?
- What patterns exist in customer purchasing behaviour?
- What data quality issues affect the analysis?

### Analysis Performed

#### Data Quality Assessment
- Identified and removed exact duplicate rows.
- Examined missing values.
- Investigated negative quantities.
- Identified zero and negative unit prices.
- Investigated unusual transactions.
- Made analysis-specific data preparation decisions.

#### Product Revenue Analysis
- Calculated revenue using quantity multiplied by unit price.
- Aggregated revenue by product description.
- Ranked product descriptions by total revenue.
- Interpreted rankings in a business context.

#### Country Analysis
- Aggregated revenue by country.
- Counted unique invoices by country.
- Compared revenue contributions and invoice volumes.

#### Time-Based Analysis
- Extracted year and month from transaction dates.
- Aggregated revenue by month.
- Visualized monthly revenue trends.
- Identified the peak revenue month.
- Considered incomplete reporting periods.

#### Customer Analysis
- Calculated total revenue by customer.
- Counted unique orders per customer.
- Calculated total quantities purchased.
- Identified high-revenue customers.
- Compared mean and median values to understand customer purchasing behaviour.

### Key Findings

**Country revenue**

The United Kingdom generated approximately 9.00 million in revenue, substantially more than any other country in the analysis.

**Product revenue**

DOTCOM POSTAGE ranked first by product description, followed by REGENCY CAKESTAND 3 TIER.

The rankings also included entries such as POSTAGE and Manual, highlighting the importance of interpreting product descriptions carefully.

**Monthly revenue**

November was the highest-revenue month in the observed period. September, October, and November were also among the strongest months.

December 2011 was incomplete because the dataset ends on 9 December 2011.

**Customer behaviour**

| Metric | Highest observed customer | Result |
|---|---|---:|
| Total revenue | Customer 14646 | 280,206.02 |
| Number of unique orders | Customer 14911 | 201 |
| Total quantity purchased | Customer 14646 | 196,915 |

The mean exceeded the median for customer revenue, order count, and quantity purchased. This suggests right-skewed distributions in which a smaller number of high-value customers influence the averages.

### Data Quality and Analytical Considerations

- Negative quantities may represent returns, cancellations, or other adjustments.
- Missing customer IDs limit customer-level analysis.
- The sales analysis included only records with positive quantities and positive unit prices.
- Revenue represents quantity multiplied by unit price, not profit.
- The calculated revenue totals do not account for returns and should not be interpreted as net revenue.
- Observed relationships do not establish causation.

---

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## EDA Workflow

The projects follow this general workflow:

1. Define the objective and questions.
2. Load and inspect the dataset.
3. Assess data quality.
4. Prepare the data for analysis.
5. Analyze distributions and relationships.
6. Visualize important patterns.
7. Interpret results.
8. Communicate findings and limitations.

## Learning Progress

| Area | Status |
|---|---|
| Dataset inspection | Completed |
| Missing-value and duplicate analysis | Practiced |
| Numerical and categorical analysis | Practiced |
| Distribution analysis | Practiced |
| Data visualization | Practiced |
| Grouped analysis and comparisons | Practiced |
| Time-based analysis | Completed in Online Retail EDA |
| Customer and business analysis | Completed in Online Retail EDA |
| Interpretation of findings | Practiced |

## Future Improvements

- Explore additional datasets and business problems.
- Practice more advanced statistical analysis.
- Improve visualizations and analytical storytelling.
- Apply EDA techniques during Machine Learning projects.