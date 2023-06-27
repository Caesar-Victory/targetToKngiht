# Chapter2 Meaningful Names



## 2.4 Make meaningful distinction



The definite article `the` , the indefinite article `a` and `an`, those can be used as prefix of variable. The formal parameters usually be as section of function, however, the global or local variable is not associated with function formally.

So we can use `the` as prefix of formal parameters, and the indefinite article as prefix of global and local variables.




```python
# Using prefix conventions in variable and argument naming

another_variable = 20

# Prefix "the" for function arguments
def my_function(the_argument):
    # Prefix "a" for local variables
    a_variable = 10
    print("This is a local variable: ", a_variable)
    print("The argument:", the_argument)

# Calling the function
my_function(a_variable)
```



### 2.4.5 Use Searchable Names

The length of variable is associated with using scope of variable. The variable complexity is the price of searchability.

```python
REAL_DAY_PEER_IDEA_DAY = 4
WORK_DAY_PEER_WEEK = 5
task_estimate = [5, 55, 72, 77, 7, 33, 40, 31, 72, 20, 10, 40, 7, 95, 74, 78, 45, 20, 25, 86]
print(task_estimate)
day_tasks = len(task_estimate)
tasks_sum = 0
i = 0
while i < day_tasks:
    real_tasks = task_estimate[i] * REAL_DAY_PEER_IDEA_DAY
    tasks_sum += real_tasks // WORK_DAY_PEER_WEEK
    i += 1
print(tasks_sum)
```
