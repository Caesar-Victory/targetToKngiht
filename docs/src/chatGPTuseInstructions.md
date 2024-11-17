# `chatGPT`可以怎么用？

1. 代码解读
2. 代码比较
   1. 格式：
3. 阅读（微信读书）
   1. 楼主想法摘要
   2. 作者引用论文概要
   3. 书中文段解析
4. 写作
   1. 邮件美化
5. 自动化脚本编写
   1. 时间模板生成（周数+间隔天数计算）
   2. 字体模块制作（字体文件替换/description撰写/打包）
   3. 搜索并且转换字体格式
   4. 
6. 数据分析
   1. 分析提问者提问范围&性格&偏好
   2. 
7. 创作者
   1. 抠图 & 文生图
   2. 
8. 疾病咨询
   1. 解读体检报告异常项目产生原因
9. 前端项目撰写
   1. 基本布局设计，语法解析，语法检查
10. 对回复内容的干预
    1. 格式：add time on the end line of every reply
    2. 格式：按照提问针对的对话层次整理思维导图

11. XXX


## 时间记录

```markdown
请在以后的所有对话中，都在文字末尾加上北京时间
Please add conversation's generation timestamp of current reply[using the standard of the Eastern Eight Zone (UTC+8), the format is hh:mm] to end of every conversation of your reply.
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

```markdown
核心需求是：反复敲代码提高熟练度。现在希望开发一个基于Vue在本地运行的网页，能够实现以下功能
1. 点击开始，开始记录时间，时间精确到毫秒，点击结束，自动统计时间
2. 开始敲代码前，需要提供一份用以比对的代码
3. 点击结束后，若代码完全一致，则在页面正中央显示本次敲完整份代码的时间，若代码有任何不同，则左右对照显示，右侧以红色标记
4. 代码输入框和代码比对框均支持显示代码行号
5. 编辑器仅支持代码编写，支持对Python语法的高亮
6. 页面底部显示最近的九次提交代码的时长
本机为Windows11操作系统，node版本为`v20.18.0`, npm版本为`10.8.2`
素材：设计稿（页面布局，输入框）
提问模型：前端框架设计稿，主要按钮，输入框，布局和样式
问题判断：可能出问题的代码段，代码修改前后的对比以及组件之间相互调用关系，说明调用关系时请按照为了实现什么功能，使用了Vue代码/那个生命周期函数，行数，页面样式，调用JS函数，JS函数功能的说明
```

### 语法提问和对比

```markdown
请问这是Python的什么语法`row[k], row[leg-k] = row[leg-k], row[k]`?在JavaScript是否有类似的语法？若有，请写一个示例代码？
```

### 角色扮演

```markdown
现在假设你是一名web开发工程师，精通JavaScript和Vue框架，目前借助交流中的代码训练平台这个前端，教授我Vue基本语法和项目搭建过程。请您在历次回复中，按照相对固定的内容回复，我希望从您的回复中了解Vue的基本语法，函数的调用关系，组件之间的调用关系，页面中按钮，选框和基本样式的布局。请您记住这个基本设定，重新回答我关于改进时间计时展示方式和上限的提问，问题可以参照上一轮提问
```