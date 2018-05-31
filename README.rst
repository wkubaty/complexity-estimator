# Complexity Estimator

This program is estimating complexity of a given function, comparing executing times for vary sizes of problem. It is assumed that the greater size is, the more time it takes. Additionally program estimates execution time for given size of a problem and in reverse - what's the estimating size of problem, it can be solved in a specified time.

## How to use
Required python 3
1. Open your console and type:
```bash
    $ pip3 install git+https://github.com/wkubaty/complexity-estimator.git
```
or install from PyPI:
```bash
    $ pip3 install complexity_estimator
```
2. Run python 3
3. Type: 
```python
    >>> from complexity_estimator import main
```
### Run example
4. Type: 
```python
    >>> main.run_example() to get example estimating
```
### Estimate complexity your own module
4. Type: main.run([module], [size1], [size2], [sizeToCheckTime], [timeToCheckSize], [timeout=30])


* module - name of module you want to test out. It needs to have a special structure containing 3 functions:
  * setup - a function initializing and preparing structures, connections etc. Time of setup is not taken under account.
  * measure - a general function of which the time is measured
  * teardown - a function tearing down like ie. closing connections with databases, deleting some files etc.

* size1 - the size of smaller problem you want to check out. 
* size2 - the size of bigger problem, should be greater than size1 (ie. 10 times)
* sizeToCheckTime - the size of problem you want to estimate time
* timeToCheckSize - the time within the specified problem can be resolved
* timeout - optional function when you can set the maximum time of calculating. Default it is set to 30 seconds. It is not recommended to setting up a lower timeout.
The best complexity estimating result is when it takes at least a few seconds to calculate.
For the small sizes, time execution differences can be unnoticeable, which results inaccurate complexity measurements. If so, try to increase the size of the problems.

