# iterative-hc
<b>Recursive hierarchical clustering to overcome missing variables</b><br>

The purpose of this script is to do Exploratory analysis of how similar the demand of each country is to one another. Instead of using actual country or product features, I am using the approach of comparing weighted demand of SKU products to represent preference of a country relative to another.<br><br>

I wish to believe the problem with the missing data is that the products might not be offered to the countries in the first place. If that is the case, it is unfair to compare no sales for a country that could not have had demand should there be no sellers.
Yet, the dropna() method reduces my dataset drastically, dropping valuable information.<br>

This inspired me to think of a novel method of iteratively doing clustering by a filtered set, tagging the cluster similarity in a correlation matrix, subsequently observing the results.<br><br>

The logic runs as follows:<br>
1. Randomly select 7 countries<br>
2. Keep common products offered as features<br>
3. Weight sold quantity values down<br>
4. Perform clustering technique (KMeans in my case)<br>
5. Tag if same (+1) or different (-1) if two countries are in the same or different cluster<br>
6. Loop Steps 1-5 for 100 times (specified by user)<br>
6. Calculate average correlation matrix table<br>
7. Plot correlation matrix using a gradient chart<br><br>

I am using the public dataset <a href = 'https://archive.ics.uci.edu/ml/datasets/Online%20Retail#'>
Online Retail Data Set</a> for the purpose of this tutorial.
