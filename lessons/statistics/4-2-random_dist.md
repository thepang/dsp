[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> _Question: Exercise 2   The numbers generated by random.random are supposed to be uniform between 0 and 1; that is, every value in the range should have the same probability.
Generate 1000 numbers from random.random and plot their PMF and CDF. Is the distribution uniform?_

Generating 1000 numbers:
```
random_nos = np.random.random_sample((1000,))
```

Attempting to plot PMF:
```
random_pmf = thinkstats2.Pmf(random_nos)
thinkplot.Hist(random_pmf)
```

Graph is empty.

Attempting to plot CDF:
```
random_cdf = thinkstats2.Cdf(random_nos)
thinkplot.Cdf(random_cdf)
```

The CDF is approximately a straight line, which means that the distribution is uniform.
