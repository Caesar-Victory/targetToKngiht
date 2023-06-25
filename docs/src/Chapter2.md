# Chapter2 Meaningful Names



## 2.4 Make meaningful distinction



In the given sentence, the author is discussing the use of prefix conventions, specifically the prefixes "a" and "the," to make meaningful distinctions in naming variables and function arguments in Python. The sentence suggests that using these prefixes can be acceptable as long as they serve a purpose.




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



We use the prefix "a" for local variables (`a_variable`, `another_variable`), indicating that these variables are distinct and local to the specific scope they are defined in. The use of "a" as a prefix helps differentiate them from other variables.

We also use the prefix "the" for the function argument (`the_argument`). This naming convention suggests that the argument is unique and refers specifically to the value passed when calling the function. Using "the" as a prefix helps indicate that the argument has a specific and significant role within the function.

It's important to note that the sentence is not describing any Python language features or syntax. Instead, it is discussing a recommended naming convention that can be followed to provide meaningful distinctions in variable and argument names.

Noise words: Words that have no real meaning in the language or are not helpful in understanding the context.

### 2.4.5 Use Searchable Names



In Python, the built-in function doesn't include constant conception. But we conventionally use all upper letter of variable to represent constant.



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
