# Amazon Vine Analysis

## <b>Overview of the analysis:</b>

The purpose of the analysis was to review luggage reviews by members of the paid Amazon Vine Program.  Due to the pandemic, travel has been put on hold and people are ready to get some new luggage to finally start traveling again.  I extracted the luggage dataset, transfromed it and connected it to an AWS RDS instance.  After I had created dataframes for customers, products, reviews and the vine data, I was able to upload it into PgAdmin.  The next process was to analyze the data by looking at total counts of reviews from members and non members to see if there is any bias in the reviews based on whether or not the reviewer is a member.  

<b>Deliverable 1</b>

I had extracted reviews on luggage items as a dataframe and transformed it into four DataFrames.  After putting into the four DataFrames, I uploaded each one to pgAdmin as you can see from the images below.

![](/Resources/customers_table.png)

![](/Resources/products_table.png)

![](/Resources/review_id_table.png)

![](/Resources/vine_table.png)


<b>Deliverable 2</b>

Using PySpark, I created two data frames showing the review id's, star rating, helpful votes, total votes, whether or not it was a verified purchases.  It was then filtered by including total votes that were over 20 and then filtered by only including where helpful votes were great than or equal to 50% of the total votes.  The two dataframes were then filtered by those that are part of the Vine program and one was filtered by those that are not part of the Vine program.  

This first image is showing the paid reviews.  

![](/Resources/program.png)

This second image is showing the reviews by those that are not members of the Vine program.  

![](/Resources/non_member.png)

Based on the images above, following are the results of the analysis.
* How many Vine reviews and non-Vine reviews were there?  There were 21 Vine reviews and 6,690 non-Vine reviews.
* How many Vine reviews were 5 stars?  How many non-Vine reviews were 5 stars?  The Vine reviews included 10 5 star reviews and the non-Vine included 6,690 5 star revies.
* What percentage of Vine reviews were 5 stars?  What percentage of non-Vine reviews were 5 stars?  47.62% of the Vine reviews were 5 star and 51.54% of the non-Vine reviews were 5 stars.






