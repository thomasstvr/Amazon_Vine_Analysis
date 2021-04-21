# Amazon Vine Analysis
The purpose of this project is to analyze Amazon product reviews made by the paid Amazon Vine program. This program is a service offered by Amazon for sellers to acquire reviews for their products. The sellers pay a fee, then supply the product to Vine members who then write a review of the product.

Our purpose is to determine whether the Vine program creates bias in the product reviews since, after all, they are paid reviews. This analysis covers only the Automotive section of reviews, though the same process could easily be applied to other sections. 

## Results
The data (found here: [Amazon Review datasets]( https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)) was first imported into a Google Colab Notebook ([Vine_Review_Analysis.ipynb]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Vine_Review_Analysis.ipynb)) as a DataFrame then condensed to get rid of unnecessary columns.

![]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Resources/vine_df.png)

Once the data could be easily viewed it was then sorted to only include reviews which had more than 20 votes and had a helpful vote to total vote ratio of at least 50%.

![]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Resources/helpful_reviews_df.png) 

From here, the data was split into two groups: Vine reviews and Non-Vine reviews.

![]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Resources/vine_reviews_df.png)
Vine reviews.

![]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Resources/nonvine_reviews_df.png)
Non-Vine reviews.

With these new dataframes we can now begin our analysis. 

* 76 reviews were made by Vine participants while 23,015 reviews were made by normal consumers (Non-Vine)
* Of these reviews Vine participants made a total of 30 5-star reviews while normal consumers made 11,914 5-star reviews
* This equates to 5-star reviews making up 39.5% of all Vine reviews and 51.8% of all normal consumer reviews

The results can also be seen in the following two images:

![]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Resources/Vine_totals.png)

![]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Resources/nonvine_totals.png) 

## Summary 
As you can see from the results, the Vine program does not introduce any bias towards positive reviews (at least within the Automotive section that is). With 5-star ratings making up 39.5% of Vine reviews versus 51.8% of normal consumer reviews, it is clear that Vine participants are not bias.

This is not to say that the only good reviews carry a 5-star rating. 4-star ratings are still a positive review and were not considered in this analysis. If the analysis were ran to compare the percentage of 4 and 5-star reviews combined then it would be much more intuitive and may backup or reject the findings from above. 
