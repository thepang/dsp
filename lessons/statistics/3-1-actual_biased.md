[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

To print histogram of number of children as found in the provided data set.
```
resp = nsfg.ReadFemResp()
hist = thinkstats2.Hist(resp.numkdhh, label='numkdhh')
thinkplot.Hist(hist)
thinkplot.Config(xlabel='kids had', ylabel='Count')
```

Simulate biased data set to show data as if we were only able to obtain data from children who reported on the number of children in their family, including themselves.
```
kids_w_sibs = resp[resp.numkdhh >= 1]
hist_live = thinkstats2.Hist(kids_w_sibs.numkdhh, label='numkdhh')
thinkplot.Hist(hist_live)
thinkplot.Config(xlabel='kids with siblings', ylabel='Count')
```

Calculate each mean:
```
print('Actual mean', pmf_kids.Mean())
print('Observed mean', pmf_kids_biased.Mean())
```

Actual mean 1.024205155043831


Observed mean 1.9186274509803922



As seen above, the mean is much higher since each data set is guaranteed to include the person responding to the survey.
