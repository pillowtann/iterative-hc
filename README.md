# iterative-hc
<b>Recursive hierarchical clustering to overcome missing variables</b><br>

The purpose of this script is to do Exploratory analysis of how similar the demand of each country is to one another. Instead of using actual country or product features, I am using the approach of comparing weighted demand of SKU products to represent preference of a country relative to another.
The novel elements of this script is the way I approach missing data via an iterative clustering methodology (see last section).<br>
I wish to believe the problem with the missing data is that the products might not be offered to the countries in the first place. If that is the case, it is unfair to compare no sales for a country that could not have had demand should there be no sellers.
Yet, the dropna() method reduces my dataset drastically, dropping valuable information.<br>
This inspired me to think of a novel method of iteratively doing clustering by a filtered set, tagging the cluster similarity in a correlation matrix, subsequently observing the results.<br>

I am using the public dataset <a href = 'https://archive.ics.uci.edu/ml/datasets/Online%20Retail#'>
Online Retail Data Set</a> for the purpose of this tutorial.
