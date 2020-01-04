[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.
In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

Convert heights from feet/inches to centimeters. Calculate the difference between the probabilities.

```
difference_in_probabilities = dist.cdf(185.42) - dist.cdf(177.8)
print(difference_in_probabilities)
```
Printed answer is 0.3427468376314737 or 34.27%. 
