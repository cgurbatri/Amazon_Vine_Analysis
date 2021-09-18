# Amazon Vine Analysis

## Project Description
The goal of this analysis is to analyze Amazon reviews written by members of the paid Amazon Vine program. Amazon Vine is a service that allows manufacturers and publishers to receive reviews for their projects. More specifically third-parties like Sellby pay a fee to Amazon to provide products to members of the Amazon Vine program in exchange for a review. 

**Goal**: To determine if there is any bias toward favorable reviews from Vine members in the Amazon books dataset. 

**Method**: PySpark was used to perform the ETL process, connect to an AWS instance, and load the transformed data into pgAdmin for further querying. 

## Resources
Data source: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_01.tsv.gz

Software: Google Colab Notebook, AWS, pgAdmin 4, PostgreSQL 11.13

## Results
* Total number of reviews (non-vine and vine): 337,176 reviews total
* Total number of 5 star reviews (non-vine and vine): 170,404 reviews total

This can be further stratefied into Vine and non-Vine reviews shown below: 

* Total Vine reviews (paid): 4,781
* Total 5-star Vine reviews: 1,604
* Percentage of 5-star Vine reviews: ~33%
<img width="576" alt="Screen Shot 2021-09-18 at 5 21 45 PM" src="https://user-images.githubusercontent.com/45336910/133908839-585f4e5c-77f6-4f88-9660-55c90a269de1.png">

* Total non-Vine (unpaid): 332,395
* Total 5-star non-Vine: 168,800
* Percentage of 5-star non-Vine reviews: ~50.78%
<img width="611" alt="Screen Shot 2021-09-18 at 5 23 04 PM" src="https://user-images.githubusercontent.com/45336910/133908869-a1dc13e0-da39-4c05-b963-113402486687.png">

## Summary and Analysis
* ~ 50% of total reviews (unpaid and paid) were 5 star reviews. 
* ~ 33% of vine (paid) reviews were 5 stars
* ~ 50% of non-vine reviews (unpaid) were 5 stars

Those who were paid to review the books actually had a lower percentage of 5% reviews. This supports that there is no positivity bias for reviews in the Vine program. Looking at the distribution of review scores (mean, median, mode) could provide further insight into the potential of bias. Perhaps, those who are paid are more likely to rate books in a binary manner, either really well (5 stars) or really poorly (1 star) possibly because they feel pressured to have a strong opinion on the book. Further analysis into the distribution of review scores could provide more insight into this hypothesis.
