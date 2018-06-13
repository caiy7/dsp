[Think Stats Chapter 8 Exercise 3](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77)

---

>> Define a function `SimulateGame1` to simulate the game:
>> ``` python
>> >>> import random
>> >>> def SimulateGame1(lam):
>> ...     '''
>> ...     Simulate the game with a given lam: scoring rate.
>> ...     Return scoring goals. 
>> ...     '''
>> ...     total = 0 
>> ...     goal = 0
>> ...     while total < 1:
>> ...         t = random.expovariate(lam)
>> ...         total += t
>> ...         goal += 1
>> ...     return goal - 1 
>> ```
>> Write a function `SimulateExp` to iterate the game with `lam` = 2 and times of iteration m:
>> ```python
>> >>> def SimulateExp(m = 1000):
>> ...     '''
>> ...     Simulate the game with lam =2 m times. 
>> ...     Print RMSE and mean error of L. 
>> ...     '''
>> ...     Ls = []
>> ...     for i in range(m):
>> ...         Ls.append(SimulateGame1(2))
>> ...     print('RMSE of L is', RMSE(Ls, 2))
>> ...     print('Mean error of L is', MeanError(Ls, 2))
>> ```
>> Try different number of iterations:
>> ```python
>> >>> for i in [1000, 10000, 100000, 1000000]:
>> ...     print(i)
>> ...     SimulateExp(i)
>> ```
>> ```
>> 1000
>> RMSE of L is 1.4017845768876187
>> Mean error of L is 0.017
>> 10000
>> RMSE of L is 1.4067338056647392
>> Mean error of L is -0.0399
>> 100000
>> RMSE of L is 1.4207216476143383
>> Mean error of L is 0.00201
>> 1000000
>> RMSE of L is 1.4156306015341715
>> Mean error of L is 0.00115
>> ```
>> The RMSE of the estimator L is around 1.4. The mean error is close to 0 and decreases as the iteration number increases. It is probably unbiased estimator. 
---