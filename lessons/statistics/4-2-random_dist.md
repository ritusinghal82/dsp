[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

numbers = np.random.random_sample(1000)
number_pmf = thinkstats2.Pmf(numbers)
#thinkplot.PrePlot(2)
thinkplot.Pmf(number_pmf)
thinkplot.Config(xlabel='Random Numbers', ylabel='PMF')

rank_cdf = thinkstats2.Cdf(numbers)
thinkplot.Cdf(rank_cdf)
thinkplot.Config(xlabel='Numbers', ylabel='CDF')

CDF plot indicates distribution is uniform
