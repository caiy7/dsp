[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> After the data was imported, cleaned up and split into DataFrames `firsts` for first babies and `others` for other babies. To get the mean weight of the two groups:  
>> ```python
>> >>> print('The mean weight of first born is %.4f lbs' %firsts.totalwgt_lb.mean())
>> >>> print('The mean weigth of others is %.4f lbs' %others.totalwgt_lb.mean())
>> ```
>> ```
>> The mean weight of first born is 7.2011 lbs
>> The mean weigth of others is 7.3259 lbs
>> ```
>> To compute Cohen's effect size:
>> ```python
>> >>> CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
>> ```
>> ```
>> -0.088672927072602
>> ```
>> The first babies are lighter than the others on average. However the effect size is small. 
