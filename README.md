# Description
Adaptation of the [DataCamp](https://www.datacamp.com) [Analyzing Industry Carbon Emissions](https://app.datacamp.com/learn/projects/analyzing_industry_carbon_emissions) project using [DuckDB](https://duckdb.org/). 

In the related Jupyter Notebook the original project description is provided along with setting up the DuckDB environment and tables. 


## Project Description
Product emissions make up more than 75% of global emissions. But which industries are the worst offenders?

Use this dataset alongside your Intermediate SQL skills to find out!


### Notes
Originally I had exported the data as a CSV file but the CSV data had some triple quotes on some of the fields due to the values containing a quotation in the data. The read_csv, read_csv_auto and COPY would eventually fail. Attempting to override the quote parameter with triple quotes resulted in an error as the parameter could only contain 1 byte. As the workspace can store the results of a SQL query into a dataframe I was able to use pandas to then export the data to a parquet file. Importing the parquet file data worked without issue. 