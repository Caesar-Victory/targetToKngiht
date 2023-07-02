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



## Using Solution/Problem domain names 

比如现有以下场景，作为后端开发，我将给前端返回一个带有多个课程的 `response`，在整理数据结构过程中，我需要一个变量存储实例化后的多个课程，但这个变量将会作为实例化后通过ORM语法批量插入数据库的一个数据源，如果以解决方案，也就是最终数据来说，我直接写一个courses`即可，表示存在多个课程，这一个变量对于用户来说是透明的；

而如果采用问题主导的命令方式，那么我应该按照直接用实例化后的课程集，即`courses_groups_after_instance.`



还会存在一种情况，由于该数据代表的意义比较复杂，我们无法直接用一个单词描述，但是多个单词组合时，面临一个语序问题。比如对于实际支付的价格，我们可以这样写`facutal_price_paid`，我们也可以对象主导，即`price_factual_paid`。这二者都没错，但显然第一种完全符合中文语序，后者则是对象 + 修饰的描述方式，更加适合英语环境，适合语言的变量会读取更快。



### Other Principle

Pun: The word has different meanings but sound the same—>We should eradicate ambiguity.

Hungarian Notation: use datatype as prefix of variable.
