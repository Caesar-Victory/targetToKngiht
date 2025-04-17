# Update the direction to update doc of AI

- 2/5/2025 record usage experience of AI in daily life

# the Limitation of AI

such as Apple Intelligence, we need a integrated AI. We need to spend much time coding special API for personal demand, such as calculation of calorie.

## 时间记录
note: the state of this prompt is **deprecated**, because AI can't add accurate timestamp at the end of reply.
```markdown
Please add conversation's generation timestamp of current reply[using the standard of the Eastern Eight Zone (UTC+8), the format is hh:mm] to end of every conversation of your consequent reply.zzzzzzzzz
```

## Programming Language Conversation

```markdown
Please convert this Python code `` into JavaScript,What's more, you need to keep using same grammer and data structure in possible.
```


## 提问模板



### 字体模板创建

```markdown
请生成一个Python脚本，当前工作目录为：`C:\Users\41999\Documents\wdtest\replace`，工作目录下下有一个名为`module`的文件夹，
1. 请在工作目录下检索后缀为`.ttf`的字体文件，将其重命名为`SysFont-Regular.ttf
SysSans-En-Regular.ttf
SysSans-Hans-Regular.ttf
SysSans-Hant-Regular.ttf`并且替换这个目录：`C:\Users\41999\Documents\wdtest\replace\module\system\fonts`下的同名文件，
2. 获取并且用变量保存用户输入的字体名称，将`module`拷贝并且重命名为用户输入的字体名称
3. 修改`C:\Users\41999\Documents\wdtest\replace\module`下的`module.prop`文件内容
	3.1 给`id`赋值为`1000000`以内的七位随机数，并且随机数不得重复
	3.2 给`name`赋值为用户输入的字体名称
	3.3 给`version`赋值为当前的时间，格式为`YYYYMMDD`
	3.4 给`versionCode`赋值为`1000000`以内的七位正整数，每修改一次自增加1
	3.5 给`description`赋值为随机的长度为20的英文大小写字符串
	3.6 给`author`赋值为`Yifan`
4. 生成以上的模板，并且替换`module.prop`文件
5. 将以用户输入的字体名称命名的文件夹打包为zip文件，电脑CPU为14核20线程，请使用Python中多线程技术加速拷贝和打包过程
6. 清理当前工作目录下的`.ttf`结尾的文件
7. 统计执行时间
```

### 前端项目创建


### 语法提问和对比

```markdown
请问这是Python的什么语法`row[k], row[leg-k] = row[leg-k], row[k]`?在JavaScript是否有类似的语法？若有，请写一个示例代码？
```

### 角色扮演


### Generate code in other Program language by one language
```markdown
Please generate code in JavaScript and C++ by this Python code ``, and the generated code need to keep similar grammar in possible.
```





## 时间记录的数据处理

```markdown
以上为每个任务，任务的开始时间和结束时间。
1. 计算每个任务耗时；
2. 保留耗时和任务名称，以这两者为表格的列标题，其中任务在前，耗时在后；
3. 按照耗时，逆序排列任务; 
4. 相同任务的耗时直接累加，保持任务的唯一性；
5. 请提供CSV格式的表格，给我下载；
6. 请以MM为时间单位。
```

## 软考相关

- 请识别图中题目和选项
- 分析在软件中级系统分析师知识点中
- 分析题目和选项。并就其中的关键概念做出延伸讲解。
- 在自私的基因中第一章【为什么会有人呢？】中提及``


## 请根据根据抖音，小红书和哔哩哔哩平台以及用户群画像，生成视频 & 教程简介


## 将文案转写为小红书风格，并且为我推荐关键词

## 这是我视频的大纲，现在视频即将在抖音和哔哩哔哩以及小红书发布，请综合考虑这三个平台的特性，为我生成适用于哔哩哔哩和抖音的视频简介，适用于小红书的文案，生成时请考虑到各个平台的用户画像，视频文案特点。

## 请识别题目并且分析正确答案

## 假设你是Oracle认证的MySQL 8.0 Database Administrator，而我是一名大学三年级计算机科学与技术学生