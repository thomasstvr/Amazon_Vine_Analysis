# Amazon Vine Analysis
The purpose of this project is to analyze Amazon product reviews made by the paid Amazon Vine program. This program is a service offered by Amazon for sellers to acquire reviews for their products. The sellers pay a fee, then supply the product to Vine members who then write a review of the product.

Our purpose is to determine whether the Vine program creates bias in the product reviews since, after all, they are paid reviews. This analysis covers only the Automotive section of reviews, though the same process could easily be applied to other sections. 

# Results
The data (found here: [Amazon Review datasets]( https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)) was first imported into a Google Colab Notebook [Vine_Review_Analysis.ipynb]( https://github.com/thomasstvr/Amazon_Vine_Analysis/blob/main/Vine_Review_Analysis.ipynb) as a DataFrame then condensed to get rid of unnecessary columns.

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

The following two images show the results in 
