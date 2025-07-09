# SQL Basics and CRUD

## Structured Query Language (SQL)

[![Introduction to SQL for Data Scientists](https://img.youtube.com/vi/0x0dW8T-4uo/0.jpg)](https://youtu.be/0x0dW8T-4uo)



## SQL basics
- CRUD (CREATE, READ, UPDATE and DELETE)
- Join,Group by
- Window Functions

## Introduction to Databases
- Why Databases?
    - Alternatives: CSV file, text file, excel file are all flat files
    - Databases make our life simpler, easier, faster, reliable, and secure
    - E.g finding rows where value of a particular column>10 is time consuming in flat files. Databases
        use a technique called indexing with simple and easy to use langauge called SQL
        to achieve the result faster.
    - This is done without much programming background, instead it uses the quering language.
    - Databases backup the data at multiple places to increase reliability

- Example Databases
    - Oracle, MySQL, SQLServer

- Relational and Non-relational Databases
    - Relational Databases (Traditional DBs (from 1970s) like the one listed above): A relational database 
    stores data in structured tables with rows and columns, using a predefined schema to clearly define relationships between data points
    
    - Non-Relational Databases
        - e.g. MongoDB, non-relational database (often called NoSQL) offers more flexibility by storing data in various formats like documents, key-value pairs, or graphs, allowing for less structured  and more dynamic data sets; 

    - Relational databases are ideal for highly structured data with complex queries, while non-relational databases excel in handling large volumes of diverse data with rapid scalability needs.

- Tables
    - In a relational database all of our data is stored across multiple tables. For example,

    - movie_id, movie_name, year, actor_id, actor_name, gender
        1             Spiderman, 2009, aid_1, name_1, Male
        1             Spiderman, 2009, aid_2, name_2, Male

    - Here only some part of data changes other part we are simply copying which is inefficient

    - In relational databases data is stored across muliple tables to avoid data duplication

        - Table 1: movie_id, movie_name, year
        - Table 2: actor_id, actor_name, gender
        - Table 3: movie_id, actor_id
        - Here movie_id and actor_id are unique

    - There is a Primary Key associated with each tables

## Why SQL
- SQL stands for Structured Query Language
    - has its beginings from 1970's from IBM
    - Standard way to query/add/delete/modify data
    - e.g. query: List of all movies that released after 2012
    - SQL is used by data scientist, ML engieers, Software engineers etc.

- SQL is not a general purpose programming langauge, it is domain specific language

- General purpose programming langauge lets you create web/mobile apps, games, DBs, Operating systems etc.

- C/C++, Python, etc are procedural programming langauge, step by step instructin provided

- SQL is declarative programming langauge


- Execution of an SQL statement
    - The execution follows the following actions
    - SQL->Parser, compiler 
         ->parser: tries to understand the query
         ->compiler: query optimizer (optimal way to execute) & generates code
         ->query executer->DB->results

## IMDB dataset
- Website owed by amazon.com: has data on movies
- data about 388,269 movies (since 1888-)
- 817,718 actors
- 86, 880 directors
- Tables
- Schema of a database: All tables and their relationship
    - directors
        - id (primary key)
        - first_name
        - last_name
    - movies
        - id (primary key)
        - name
        - year
        - rank
    - actors
        - id (primary key)
        - first_name
        - last_name
        - gender
    roles
        - actor_id
        - movie_id
        - role
    director-genre
        - director_id
        - genre
        - prob

    movie_directors
        - director_id
        - movie_id

    movie_genre
        - movie_id
        - genre


## Installing MySQL
- www.mysql.com
    - MySQL community edition: MySQL Community server
    - MySQL commandline client

- https://sqlzoo.net/wiki/SQL_Tutorial


## Load IMDB data
mysql -u username -p password
CREATE DATABASE imdb;
USE imdb;
source /path/to/imdb.sql;
SHOW tables;


- USE, DESCRIBE, SHOW Tables
    - mysql -u root -p root
    - CNTRL+L to clear the screen
    - CREATE DATABASE imdb;
    - USE <DB NAME>;
        - USE imdb;
    - SHOW tables;
    - DESCRIBE <table_name>;
        - shows the schema of a particular table
        - DESCRIBE actors;


https://www.sqlzoo.net/


- SELECT
    - Suppose if i want to list all the movies, i can use select clause 

    USE imdb;
    SHOW Tables;
    DESCRIBE movies;
    SELECT * FROM movies;
    - In reality there will be tables with 100's of columns
    - SELECT name, year FROM movies;
        - here we are not explaining how to generate the output
        - the output row order is same as the one in the table

- LIMIT, OFFSET
    -  view information like a page by page fashion
        - e.g. flipkart view gadgets by price/review

    - SELECT name, rankscore FROM movies LIMIT 20;
    - SELECT name, rankscore FROM movies LIMIT 20 OFFSET 40;

- ORDER BY
    - SELECT name, year FROM movies ORDER BY year DESC LIMIT 10;
    - default sorting order in ascending
    - The output row order maynot be same as the one in the table due to
    query optimizer and internal data-structures/indices.

- DISTINCT
    - Can be used to find distinct values with in a columns
    - SELECT DISTINCT genre FROM movie_genres;
    - SELECT DISTINCT first_name. last_name FROM directors ORDER BY first_name;

- WHERE, Comparison operators, NULL
    - SELECT name, year, rankscore FROM movies WHERE rankscore>9;
    - SELECT name, year, rankscore
      FROM movies
      WHERE rankscore>9
      ORDER BY rankscore DESC
      LIMIT 10;
    - Conditions can be TRUE, FALSE, NULL
    - comparison operator =,<> or !=, <,<=,>,>=
    - SELECT * FROM movie_genres WHERE genre='Comedy';
    - SELECT * FROM movie_genres WHERE genre<>'Horror';
    - NULL: does not exist/unknown/missing
    - "=" does not work with NULL, will give you an empty set


    - SELECT name, year, rankscore FROM movies WHERE rankscore=NULL;
    - SELECT name, year, rankscore FROM movies WHERE rankscore IS NULL;
    - SELECT name, year, rankscore FROM movies WHERE rankscore IS NOT NULL;

- LOGICAL OPERATORS
    - AND, OR, NOT, ALL, ANY, BETWEEN, EXIST, IN, LIKE, SOME

    - SELECT name, year, rankscore FROM movies WHERE rankscore>9 AND year>2000;
    - SELECT name, year FROM movies WHERE NOT year<=2000 LIMIT 20;
    - SELECT name, year FROM movies WHERE year BETWEEN 1992 AND 2000;

    - SELECT name, year FROM movies WHERE year BETWEEN 2000 AND 1992;
      will result an empty set

    - SELECT director_id, genre FROM directors_genres WHERE genre IN ('Comedy', 'Horror');
    - SELECT name,year,rankscore FROM movies WHERE name LIKE 'Tis%';
      % is a wildcard character to imply zero of more characters

    - SELECT first_name FROM actors WHERE first_name LIKE 'Agn_s';
      _ implies only atmost one character. 

    If we want to match % or _, we should use backslash as an escape character: \% and \_


- AGGREGATE FUNCTIONS COUNT, MAX, MIN, AVG, SUM
    SELECT MIN(year) FROM movies;
    SELECT MAX(year) FROM movies;
    SELECT COUNT(*) FROM movies;
    SELECT COUNT(*) FROM movies where year>2000;
    SELECT COUNT(year) FROM movies;


- GROUP BY
    - often used with COUNT, MIN, MAX, or SUM
    - if grouping columns contain NULL values, all null values are grouped together

    SELECT year, count(year) FROM movies GROUP BY year; # to know #ofmovies released/year

    SELECT year, count(year) year_count FROM movies GROUP BY year ORDER BY year_count;
    # here year_count is an alias


- HAVING
    - Print years which have>1000 movies in our DB
    - Specifiy a condition on groups using HAVING

    - e.g. SELECT year, COUNT(year) year_count FROM movies GROUP BY year HAVING year_count>1000;

    - Order or execusion
        1. GROUP BY to create groups
        2. apply the aggregate functions
        3. apply having condition

    - HAVING is often used with GROUP BY but not mandatory
    - e.g. SELECT name, year FROM movies HAVING year>2000;
    - HAVING without GROUP BY is same as WHERE
    - WHERE is applied on individual rows while HAVING is applied on groups
    - HAVING is applied after grouping while WHERE is used before grouping
    - e.g. SELECT year, COUNT(year) year_count
           FROM movies
           WHERE rankscore>9
           GROUP BY year
           HAVING year_count>20;


## Order of KEYWORDS
 - https://dev.mysql.com/doc/refman/8.4/en/select.html

 - SELECT * FROM WHERE G-H-O-L
 - *: ALL (even distinct can be used in this place)
 - G : GROUP BY
 - H : HAVING
 - O : ORDER BY (have ASC and DESC)
 - L : LIMIT (has OFFSET)