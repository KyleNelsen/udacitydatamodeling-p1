This is my second project for the data wrangling part of the Udacity Data Analytics Nanodegree. It involves creating a Postgres database and building an ETL pipeline using python for a fictional startup called Sparkify who wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. 

The ETL process involves taking json files from the data folder provided by Udacity, transforming the data such as taking a timestamp in milliseconds and converting it into a datetime object where can it be split up into multiple columns for a more understandable timestamp. Finally the data can be loaded into tables through sql queries and be inside the database.

As you can see from ERD.png, the database is a star schema.


data - folder that contains log_data and song_data. log_data is data on the user, song_data is data on the song.

create_tables.py - creates database, drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.

ERD.png - image of the Entity-Relationship Diagram of the database

etl.ipynb - reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.

etl.py - reads and processes files from song_data and log_data and loads them into your tables. You can fill this out based on your work in the ETL notebook.

fix_db.sql - code to recreate database in case you get error

sql_queries.py - contains all your sql queries, and is imported into the last three files above.

test.ipynb - displays the first few rows of each table to let you check your database.


In order to run the code:
1. Run create_tables.py to create database and tables
2. Run etl.py to process data
3. Run test.ipynb to see if it all worked


Problems with original template
================================
-couldn't launch database, I ran fix_df.py to recreate database and user

-to run %load_ext sql - conda install ipython-sql or pip install ipython-sql

-if you get this error - MetaData.__init__() got an unexpected keyword argument 'bind'
Connection info needed in SQLAlchemy format, example:
               postgresql://username:password@hostname/dbname
               or an existing connection: dict_keys([])

run this to fix:
conda install jupysql -c conda-forge or pip install jupysql -c conda-forge"# udacitydatawrangling-p2" 

<img src="ERD.png"/>
