# Avocados Data Overview
The data backing this project and sequential blog post was provided by a gentleman named Justin Kiggins (here)[https://www.kaggle.com/datasets/neuromusic/avocado-prices] on Kaggle. For those who don't know, Kaggle is a website where people can post and retrieve public data sets. This particular data set stores avocado sales data from various areas across the United States from 2015-2018. More details regarding the data set can be found through the provided link although he was not as extensive in his explanation has he maybe should have been. I'll discuss this later.


### Sample
![](images/raw-sample.png)


## Initial Thoughts/Tweaks
If you're wondering what the *4046*, *4225*, and *4770* columns represent, so did I. These numbers represent PLUs or Price Look-Up codes; these are essentially unique identifiers for different avocado types/brands. The only data these columns represent is quantity sold and since we already have a very nice total volume column, I found these three columns to be useless for my purposes and removed them.

Secondly, I noticed that just about every value that represents quantity is a decimal number. How exactly 0.89 of an avocado was sold is a huge question mark. The description provided by Kiggins indicates all of these values as quantities aside from the average price column. Therefore, I would suspect that Kiggins is either identifying his data incorrectly or made a great error in the vast majority of his entries. Either way, I do not want to round all of the values. This would taint the data greatly and force me to recalculate the total volume column with skewed data. I decided to keep that element of the data as is and to use rounding on the end results during analysis. This will yield more accurate calculations.


## Data Cleaning
