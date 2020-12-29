[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

resp = nsfg.ReadFemResp()
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf
pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')
biased_pmf = BiasPmf(pmf, label='observed')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='No. of children under 18', ylabel='PMF')
print('Actual mean', pmf.Mean())
print('Observed mean', biased_pmf.Mean())  

It can be seen that actual mean is smaller than observed mean, which is in line with the class paradox exaplained in the text.
