[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

import scipy.stats
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
ans1 = dist.cdf(177.8)
ans2 = dist.cdf(185.4)
Answer = ans2-ans1
Answer
