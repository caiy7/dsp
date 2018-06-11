[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> Convert the height to cm using the function below
>> ```python
>> >>> def convert_to_cm(feet, inch):
>> ...    return 30.48*feet + 2.54*inch
>> 
>> >>> low = convert_to_cm(5,10)
>> >>> high = convert_to_cm(6,1)
>> >>> print(low, high)
>> ```
>> ```
>> 177.8 185.42
>> ```
>> Use `scipy.stats.norm` to represent a normal distribution with $\mu$ = 178 and $\sigma$ = 7.7. Then get the CDF at `low` (5'10) and `high`(6'1)
>> ```python
>> >>> import scipy.stats
>> >>> dist = scipy.stats.norm(loc=178, scale=7.7)
>> >>> (dist.cdf(high) - dist.cdf(low))*100
>> ```
>> ```
>> 34.274683763147365
>> ```
>> About 34% of us men population is in the range. 

