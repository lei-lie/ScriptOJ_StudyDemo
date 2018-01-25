# 概述

利用ScriptOJ学习平台，来强化自己前端编程技能以及培养逻辑思维，开始记录学习的进度；

# 学习资料
[ScriptOJ](https://scriptoj.com/ "ScriptOJ")
# 笔记

## 笔记1
### 描述

ScriptOJ前端学习笔记00--获取文件扩展名
### 功能描述

定义一个函数，获取一个文件名的扩展名，例如获取文件名为study.doc扩展名，即	是.doc;

### 实现方法

**方法1：**

通过提取字符擦黄字符的方式实现，找到"."开始的位置，提取从这点开始到文件名字符串最后一个字符的位置，得到的结果即为最终的文件扩展名；
即是假设改文件名使用变量filename存放，使用字符串对象的`indexOf('.')`方法获取“.”首次开始的位置，然后使用`sustring(start,end)`方法截取从`indexOf('.')`开始的位置到str的结尾位置(`filename.length`)；

## 笔记2 
ScriptOJ前端学习笔记01--则表达式删除两端多余空白字符
### 功能描述
定义一个正则表达式，用来删除字符串两端的空白字符；
### 实现思路
首先定义一个正则表达式的匹配规则，用于查找字符串两端的空格字符（以空格开头或者以空格结束），
然后调用String对象的replace方法清除匹配到的空格字符，即是使用空字符替换空格字符；
## 笔记3
+1s程序
### 功能描述
>  完成一个生成计数器的函数 plusFor，调用它会返回一个计数器。计数器本身也是一个函数，每次调用会返回一个字符串。

### 实现思路
 - 定义一个计数函数plusFor，将要+1s输出的字符作为参数传入；
 - 定义一个计数变量，用做增量；
 - 在闭包中返回使用ES6语法拼接得到的新字符串；
# 笔记4
# 题目
李雷向韩梅梅求婚，韩梅梅说过一段时间（20~50ms）再回复他；
# 功能描述

> 完成 proposeToMissHan 函数，会传入一个布尔值参数 isOK，用来预先设定是否答应李雷的求婚。这个函数会返回一个 Promise，一段时间（20～50ms）以后，根据 isOK 参数，韩梅梅可能会说字符串 ok 答应李雷，也可能说字符串 no 来拒绝（reject）李雷。


# 实现思路

 - 创建一个`Promise`对象；
 - 使用定时器实现，韩梅梅考虑的时间（20~50ms）；
 - 根据`isOK`的状态判断，李梅梅是答应还是拒绝，若`isOk`为`false`，则是拒绝，则调用`reject()`, 反之则调用`resolve()`；
# 总结
这道题考察ES6的[Promise][2]对象；


## 笔记5
# 功能描述
> [完成分页函数 getPages，接收两个参数：
> 
* getPages(total, itemsPerPage)
* total： 表示总共有多少条数据
* itemsPerPage：表示每页有多少条数据
* getPages(total, itemsPerPage) 会返回一个数字告诉我们需要有多少页数据。例如，总共 101 条数据，每页有 10 条，就需要 11 页，那么就返回 11。][2]

# 实现思路
* 计算页数：页数 = 总数 / 每页显示的条数；
* 排除页数结果不是整数的情况，结果向上取整；