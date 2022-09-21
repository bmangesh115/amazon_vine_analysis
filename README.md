# amazon_vine_analysis

# Overview
The purpose is to analyze data set from the Amazon Vine program to determine if there is any bias toward favorable reviews from Vine members in the dataset .  
1. Perform cloud ETL process on dataset using PySpark and extract dataset into DataFrames.
2. Create AWS RDS database with tables in pgAdmin and run queries in pgAdmin to confrim that the data has been uploaded.
3. Linear regression analysis to identify key variables to predict mpg of prototypes.
2. Summary statistics on pounds per square inch (PSI) of suspension coils from manufacturing lots.
3. t-tests to determine if the manufacturing lots are statistically different from the mean population .
4. Design a statistical study to compare vehicle performance against different manufacturers.

## Resources
- Data Source: [Amazon Reviews Health and Personam Care]("https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Health_Personal_Care_v1_00.tsv.gz")
- Software: PySpark, Jupyter Notebook 4, Python 3.7.13, PostgreSQL12.11, pgAdmin4Visual Studio Code 1.68.1

## Results

The link to the PySpark Script for the cloud ETL.<br>
[PySpark Script for the cloud ETL](/amazon_reviews_etl.ipynb)<br>

The link to the Python Script for the data analysis.<br>
[Python Script for the data analysis](/vine_review_analysis.ipynb)<br>

### DataFrames loaded into the tables in pgAdmnin

1. Four DataFrames were created after extracting health and personal care dataset from the Amazon reviews.
2. DataFrames were loaded into respective tables in pgAdmin through AWS RDS database.
3. Data tables pgAdminin,
    - customers table
    - products table
    - review id table
    - vine table

<figure>
    <figcaption>Customers table</figcaption>
    <img src="/customers_table.png" width=821 height=auto
         alt="Customers table">
</figure> <br>

<figure>
    <figcaption>Products table</figcaption>
    <img src="/products_table.png" width=1710 height=auto
         alt="Products table">
</figure> <br>

<figure>
    <figcaption>Review ID table</figcaption>
    <img src="/reveiw_id_table.png" width=2608 height=auto
         alt="Review ID table">
</figure> <br>

<figure>
    <figcaption>Vine table</figcaption>
    <img src="/vine_table.png" width=2814 height=auto
         alt="Vine table">
</figure> <br>

### Data analysis on vine and non-vine reviews

1. Total number of Vine reviews = 497
2. Total number of non-Vine reviews = 120863
3. Number of Vine reviews with 5-star rating = 220
4. Number of on-Vine reviews with 5-star rating = 74470
5. Percentage of Vine Reviews with 5-Star Rating = 44.3%
6. Percentage of non-Vine Reviews with 5-Star Rating = 61.6%

<figure>
    <figcaption>Data summary Vine reviews</figcaption>
    <img src="/summary_vine_reviews.png" width=681 height=auto
         alt="Data summary Vine reviews">
</figure> <br>

<figure>
    <figcaption>Data summary non-Vine reviews</figcaption>
    <img src="/summary_non_vine_reviews.png" width=710 height=auto
         alt="Data summary non-Vine reviews">
</figure> <br>

## Summary

1. Preliminary analysis shows there is no positive bias as percentage of reviews with 5-Star rating for non-Vine and vine program are 61.6% and 44.3% respectively.
2. Additionl statistical t-test study can be performed between star rating for vine and non-vine reviews. It will show if there is bias of higher star rating for vine reviews over non-vine reviews.