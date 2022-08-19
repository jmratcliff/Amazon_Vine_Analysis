# Amazon Vine Shoe Review Analysis
*Big Data - ETL and analysis utilizing AWS, RDS and PySpark*
 
 
 
## Overview

Analysis of Amazon reviews for shoes sold to help the client make an informed decision around utilizing Amazon's Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

Analysis designed to determine if there is any bias toward favorable reviews from Vine members.

## Process

#### Dataset used:
US shoe sale review data from Amazon - **4,366,916 reviews were analyzed**

PySpark was used to perform the ETL (Extract, Transform, Load) process which was connected to an AWS RDS instance and then loaded to pgAdmin. PySpark used to analyze the 4.3 million reviews.

## Results

The 4.3M reviews were first narrowed down to the reviews where there were at least 20 votes:

![20votes](/images/votes_over20.png)

Those votes were then narrowed further to where at least half of the votes were labeled as Helpful:

![helpful_votes](/images/helpful_votes.png)

The resulting votes were then broken down into reviews from Vine members (paid) and *regular* buyers (unpaid):

![paid_unpaid](/images/paid_unpaid.png)

Statistics for total number of votes, 5 star votes, and percentage of 5 star votes for both groups were calculated:

![bias](/images/vine_analysis_bias.png)

## Summary

### Bias Stats

##### Paid Reviews/Vine members
* 20 total reviews
* 12 Five Star reviews
* 60.0% Five Star reviews

#### Unpaid Reviews
* 25,104 reviews
* 13,479 Five Star reviews
* 53.7% Five Star reviews

### Conclusion

