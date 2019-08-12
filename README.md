# Hypothesis Tests for Northwind Food Distributior

# Files:
**index.ipynb**: A Jupyter Notebook with my code and analysis.
**images**: Diagrams to illustrate how I created 'invoices.'
**nontechnical_slideshow.pdf**: A deck to present and findings and recommendations to Northwind's nontechnical management.
**Northwind_small.sqlite**: The database used in the analysis.

# The Data

Northwind is a fake company; its data was generated  by Microsoft. This project uses a smaller version of the data in a SQLite database of several tables. Exploratory data analysis revealed that the company had 9 salespeople selling 77 different products to 91 customers in North America and Europe.

# Methods

I used the read_sql function in Pandas to query the database and return tabular data in DataFrames. With these queries I isolated segments of the data as populations to compare in hypothesis tests.

I used SciPy to run two-sample t tests on the populations and in one case used bootstrapping to generate more normal-shaped distributions of data for testing.

With the general goal of making recommendations to Northwind to boost its sales I needed to see invoices. Invoices would reveal transactions: who was selling what to whom in what quantity. This would be more useful than just pulling out gross sales by category, person, or time period. The data did not contain an 'invoices' table. In my queries I rearranged the data to create invoices so that I could measure totals sold by certain salespeople and subtotals of different categories of products sold.

# Hypotheses: questions and answers

## Test 1:

**Part 1: Do discounts have a statistically significant effect on the number of products customers order?**

No.

**Part 2: If so, what level of discount?**

Yes: while this results seems to belie the result found at the all-discount level, some thought will lead one to realize that this is an intuitive result: it would be more odd if customers were ordering the same number of products at each level of discount as they were without. (It would be strangely precise and machine-like.)

## Test 2:

**Do the employees in the PNW offices get higher invoice totals on average than employees in the London office?**

No.

## Test 3:

**Did average sales decline in 2014 compared to 2013?**

No.

## Test 4:

**Do orders containing beverages bring in more revenue on average than orders without beverages?**

Yes.

# Recommendations:

The Jupyter Notebook and slide deck discuss specific recommendations for the (fake) comnpany to boost its sales: do not focus on discounts; investigate why the London sales reps gross less revenue each than the PNW sales reps; look for missing invoices from 2014; and sell more booze.
