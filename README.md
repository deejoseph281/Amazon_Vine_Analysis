# Amazon_Vine_Analysis

## Overview

The purpose of this project is to analyze Amazon reviews written by members of Amazon Vine program, a service that allows manufacturers and publishers to receive reviews of their products and determine if there are any biases between Vine members and Non-Vine member's reviews. 

In order to determine if there is any bias, we were asked to choose from 50 datasets to extract, transform and load into a dataframe in order to complete our analysis.

Dataset used for this analysis can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Electronics_v1_00.tsv.gz)

## Results

The dataset had +3 million reviews. We filtered the dataset by:

* Count of Total Votes equal or greater than 20. 
* Percent of Helpful Votes to Total Votes equal or greater than 50%. 

The results reduced the total number of reviews from 3M to 50.7K. This allowed us to answer the following questions:

**1. How many Vine reviews and non-Vine reviews were there?**

* **Vine** members made up only 2.1% (1,080) of the reviews whereas the remaining 97.9% were **Non-Vine** members (49,659).

![image](https://user-images.githubusercontent.com/115019829/217983373-03b4fc4a-8313-45c0-bd22-67c2051454d5.png)

**2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?**

* **Vine** members gave 454 out of 1,080 reviews a 5 star rating.
* **Non-Vine** members gave 23,034 out of 49,659 reviews a 5 star rating.

**3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?**

* 42% of the reviews for **Vine** members were rated 5 stars.
* 46.4% of the reviews for **Non-Vine** members were rated 5 stars.

## Summary

Based on the results, **Vine** members did not show bias when rating their products considering that the number of 5-star ratings was about 10% less than **Non-Vine** members (42% vs. 46.4%). With this, we can assume that Vine customers are more critical when submitting their review. However, in order to support this assumption further, we should include all of the data rather than filtering it to a percentage of helpful vs. total votes as we did for this analysis. Reviewing the data as is would give us more information and allow us to further support our assumption as shown below. 

![image](https://user-images.githubusercontent.com/115019829/217983452-1aa24c6f-8f0a-434a-99db-e5e1b2411dff.png)


In addition, running the same analysis using datasets from different product categories can provide us with the whole picture of whether reviews made by **Vine** members are bias.
