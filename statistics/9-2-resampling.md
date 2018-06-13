[Think Stats Chapter 9 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2010.html#toc90) (resampling)

>> Write a class `DiffMeanResample` which inherits from `DiffMeanPermutation` and overrides `RunModel`.
>> ```python
>> >>> import thinkstats2
>> >>> import numpy as np
>> >>> class DiffMeansResample(DiffMeansPermute):
>> ...     def RunModel(self):
>> ...         group1 = np.random.choice(self.pool, self.n)
>> ...         group2 = np.random.choice(self.pool, self.m)
>> ...         return group1, group2
>> ```
>> Run dataset on pregnant length.
>> ```python
>> >>> import first
>> >>> live, firsts, others = first.MakeFrames()
>> >>> data1 = firsts.prglngth.dropna(), others.prglngth.dropna()
>> >>> p1 = DiffMeansPermute(data1) 
>> >>> r1 = DiffMeansResample(data1)
>> >>> print('p-value(by permutation): %f. The maximum mean diff: %f.' 
>> ...       % (p1.PValue(10000), p1.MaxTestStat()))
>> >>> print('p-value(by resampling): %f. The maximum mean diff: %f.' 
>> ...       % (r1.PValue(10000), r1.MaxTestStat()))
>> >>> print('The abs mean diff from the dataset is %f.' % r1.actual )
>> ```
>> ```
>> p-value(by permutation): 0.175000. The maximum mean diff: 0.231704.
>> p-value(by resampling): 0.167600. The maximum mean diff: 0.229590.
>> The abs mean diff from the dataset is 0.078037.
>> ```
>> Run dataset on baby weight.
>> ```python
>> >>> data2 = firsts.totalwgt_lb.dropna(), others.totalwgt_lb.dropna()
>> >>> p2 = DiffMeansPermute(data2) 
>> >>> r2 = DiffMeansResample(data2)
>> >>> print('p-value(by permutation): %f. The maximum mean diff: %f.' 
>> ...       % (p2.PValue(10000), p2.MaxTestStat()))
>> >>> print('p-value(by resampling): %f. The maximum mean diff: %f.' 
>> ...       % (r2.PValue(10000), r2.MaxTestStat()))
>> >>> print('The abs mean diff from the dataset is %f.' % r2.actual )
>> ```
>> ```
>> p-value(by permutation): 0.000000. The maximum mean diff: 0.120774.
>> p-value(by resampling): 0.000000. The maximum mean diff: 0.110646.
>> The mean from the dataset is 0.124761.
>> ```
>> The testing result using model from resampling is very close to the model from permutation. There's hardly any effect on the result.  
