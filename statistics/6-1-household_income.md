[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

>> Import hinc and read data
>> ```python
>> >>> import hinc
>> >>> income_df = hinc.ReadData()
>> ```
>> Assume the log upper bound of income is 6 and generate the sample and build the CDF.
>> ```python
>> >>> log_sample = InterpolateSample(income_df, log_upper=6.0)
>> >>> sample = np.power(10, log_sample)
>> >>> cdf = thinkstats2.Cdf(sample)
>> ```
>> Calculate mean, median, skewness and Pearson's median skewness. The Skewness and PearsonMedianSkewness function were defined in this chapter. 
>> ```python
>> >>> median = cdf.Value(0.5)
>> >>> mean = np.mean(sample)
>> >>> g1 = Skewness(sample)
>> >>> gp = PearsonMedianSkewness(sample)
>> >>> mean, median, g1, gp
>> ```
>> ```
>> (74278.7075311872, 51226.45447894046, 4.949920244429583, 0.7361258019141782)
>> ```
>> The mean is 74278.71. The median is 51226.45. The skewness is 4.95 and the Pearson's median skewness is 0.74.
>> ```python
>> >>> p = cdf.Prob(mean)
>> >>> p
>> ```
>> ```
>> 0.660005879566872
>> ```
>> The proportion of the household reoprting a taxable income below the mean is about 0.66. 
>>  
>> To see how the result depends on the upper bound, change to log upper bound to 7, re-generate the data and calculate the mean, median, skewness and Pearson median skewness.
>> ```python
>> >>> log_sample1 = InterpolateSample(income_df, log_upper=7.0)
>> >>> sample1 = np.power(10, log_sample1)
>> >>> cdf1= thinkstats2.Cdf(sample1)
>> >>> median1 = cdf1.Value(0.5)
>> >>> mean1 = np.mean(sample1)
>> >>> g1_1 = Skewness(sample1)
>> >>> gp_1 = PearsonMedianSkewness(sample1)
>> >>> median1, mean1, g1_1, gp_1
>> ```
>> ```
>> (51226.45447894046, 124267.39722164697, 11.603690267537793,0.39156450927742087)
>> ```
>> The mean is 124267.40, which increases with the increase of the upper bound. The median is 51226.45, which doesn't change. The skewness is also affected greatly by the increase of the upper bound. It is now 11.60 and the Pearson's median skewness is 0.39.


