# Tips for better Python performance

1. Benchmark current performance metrics

```
(time, timeit, Python Profiler)
import cProfile
cProfile.run("test_func()")
```

2. Use the latest version of Python
3. Use application performance monitoring tools
4. Import modules lazily whenever possible

```
More details on lazy imports can be found here: https://www.geeksforgeeks.org/lazy-import-in-python/
```

5. Use built-in functions

```
- Whenever possible avoid encapsulating built-in functions into methods.
- Example: call directly pd.read_csv() function instead of creating a generalist functions whose only goal is... to read csv files. 
```

6. Avoid global variables
7. Prefer Numpy arrays over traditional lists
8. Use list comprehension

```
Especially when you want to manually iterate over values, try to use a list comprehension instead of a for loop.
```

9. Avoid checking if a variable is True

```
Example: writing *if str:* is better than *if str != None:*
```

10. Put loop inside functions, rather than otherwise

```
- Sometimes, you might need to define a function and call it multiple times in a sequence. 
An obvious, easy way would be to create a loop and call this function inside the loop multiple times.
However, this can be risky because each function call associates itself with a new stack in the memory for the call.
- Define a function in such a way that it only needs to be called once and it runs a loop
internally to complete the job in only function is preferable. 
```

11. Prefer enumerate for value and index

```
Example: *for i, number in enumerate(arr)* is preferable to *for i in range(len(arr))*
```

12. Use ```in``` over iteration to check whether a certain element is present in a list or not
13. Count unique values using ```Counter()``` method from *Collections*
14. Concatenate strings with ```join()```
15. Try an alternative way (and measure it!)

<br>

### Most common Python performance issues:

- Python is an interpreted language (interpreted languages tend to perform worst than compiled languages) and requires to be interpreted every time before it is run by the processor;
- JIT does not make the execution of byte code any faster (however, the biggest benefit that JIT brings is that enables optimizations in the compilation process);
- Python is dynamically typed (you don't have to define types every time you declare a variable, but this takes a really heavy toll on performance);
- Python can cause inefficient memory utilization;
- Python doesn't support concurrency.

<br>

### More tips:

- Interning strings for efficiency;
- Peephole optimization;
- Use generators & keys for sorting;
- Optimizing loops;
- Use set operations and unions;
- Use external libraries/packages;
- Limit method lookup in a loop;
- Optimizing with strings;
- Optimizing with if statement;
- Consider to write your own generator;
- Use ```xrange()``` instead of ```range()```;
- Remember to use multiple assignment;
- Exit early (i.e., use exceptions correctly);
- Learn itertools;
- Try decorator caching;
- Don't construct a set for a conditional (e.g., don't do ```if animal in set(animals):```);
- Use linked lists.

<br>

**Sources:**

- <https://wiki.python.org/moin/PythonSpeed/PerformanceTips>
- <https://scoutapm.com/blog/python-performance-tips>
- <https://aglowiditsolutions.com/blog/python-optimization/>
- <https://stackify.com/20-simple-python-performance-tuning-tips/>
