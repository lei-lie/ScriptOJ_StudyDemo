# 概述

利用ScriptOJ学习平台，来强化自己前端编程技能以及培养逻辑思维，开始记录学习的进度；

# 学习资料
[ScriptOJ](https://scriptoj.com/ "ScriptOJ")
[正则表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions"正则表达式")
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
