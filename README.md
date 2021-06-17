# Movies-ETL

## Project Overview

This project extract different types of movies data from various sources like Wikipedia (JSON) and Kaggle (CSV) , transform the data by analyzing, cleasing and structuring , then load the data as tables in PostgresSQL. ETL process helps in getting organized structured data for analytical purposes.

## Resources
- Data source : Kaggle : movies_metadata.csv, ratings.csv ; Wikipedia : wikipedia.movies
- Software : PostgreSQL, Pandas 

### ETL_function_test.iypnb

Create a function extract_transform_load() which read wiki file, movies file and ratings file, transform file to dataframe and return the dataframe. 

### ETL_clean_wiki_movies.ipynb
 
Create reusable **clean_movie** function which accept movie name and perfrom cleansing data. Expand extract_transform_load() function by cleansing wiki data, applying regex function for each column, parsing numeric fields and dropping repetitive or null daata columns.

### ETL_clean_kaggle_data.ipynb

Refractor the above code by passing kaggle metadata and cleansing it. Comparing wiki and kaggle data to pick valid data between two sources, fill missing data from wiki data and load into new dataframe. Merge Wiki dataframe and movies dataframe by IMDB id / Kaggle Id and dropping nulls. Load ratings data and merge it with Movies dataframe on Kaggle id and cleanse the ratings. Extraction and cleaning is completed for wiki and kaggle data. 

### ETL_create_database.ipynb

Refracting teh same extract_transform_load() function by extracting, transforming wiki , kaggle data and loading the dataframe to PostgresSQL. Movies dataframe is loaded into Movies table and load ratings.csv file into ratings table in movie_data database.

![image](https://user-images.githubusercontent.com/83181834/122449282-8cbaf100-cf5a-11eb-87bb-e0b799f6e701.png)
