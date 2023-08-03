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



## Using Solution / Problem  domain names

For former, the programmers should use terms in CS, math, software engineering, algorithm, design pattern and so on. For example, if we want to display comment by different levels, the data can be described as `comment_tree_all_levels` if we use Problems domain names. If we use Solution domain names, we can describe the data as `bfs_comment_tree`. The conception  of `use problems domain names` emphasize the process of solving problems and encourage using intermediate variables. Following is a example for latter:

```python
def get_user_available_list(user_id):
    reflection_in_num_coupon_type = {0: 'generic type', 1: 'specific direction', 2: 'specific category', 3: 'specific courses'}
    redis = get_redis_connection('cart')
    coupon_all = get_user_coupon_list(user_id)
    encode_course_id_number = redis.hgetall(f"cart_{user_id}")
    course_id_selected = {int(key.decode()) for key, value in encode_course_id_number.items() if value == b'1'}
    course_selected = Course.objects.filter(pk__in=course_id_selected, isDelete=False, isShow=True).all()
```



# Add Meaningful Context





### Other Principles

Pun: The word has different meanings but sound the same—>We should eradicate ambiguity.

Hungarian Notation: use datatype as prefix of variable.
