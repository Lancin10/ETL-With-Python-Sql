## ETL Project Description

This project consist to build an ETL from two CSV files that contain air pollution data from 8 cities between the years 2017 and 2020.


<b>Tools: #Jupyter Notebook, #Python, #PostgreSQL, PGAdmin, Pandas.</b>

### Extract 
Loaded 2 csv files from the Resources folder using pd.read_csv.

### Transform
Removed unnecessary columns and renamed Count column on each dataframe, Count_o3 and Count_pm25. I then merged these two df's using a left merge on the Date, Country, and City columns in each, resulting in one df with the counts of o3 and pm25 for each day in each city.

### Load 
Created a schema, using quotes for capitalized column names. Using pg admin, created the database etl_projct2 and within it, the table called merge_counts. I then loaded the data into the database using new_df.to_sql. Finally, I used pd.read_sql_query to confirm that the data was successfully loaded into the database. In addition, I stored a screenshot of the database

The screanshots of the ETL process on Jupyter Notebook are located in this repertory.
