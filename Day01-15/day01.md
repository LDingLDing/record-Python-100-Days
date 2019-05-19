[Day01](https://github.com/jackfrued/Python-100-Days/blob/master/Day01-15/Day01/%E5%88%9D%E8%AF%86Python.md)

# 学习笔记

## 历史

- 生日同年发布的 1.0 版本
- 08 年发布的 3.0 版本， 很多新特性后来也被移植到了 v2.6/2.7 版本中
- 目前常用的 v3.7 版本是 18 年发布的

## 优缺点

Python的优点很多，简单的可以总结为以下几点。
1. 简单和明确，做一件事只有一种方法。
2. 学习曲线低，跟其他很多语言相比，Python更容易上手。
3. 开放源代码，拥有强大的社区和生态圈。
4. 解释型语言，天生具有平台可移植性。
5. 支持两种主流的编程范式（面向对象编程和函数式编程）都提供了支持。
6. 可扩展性和可嵌入性，可以调用C/C++代码，也可以在C/C++中调用Python。
7. 代码规范程度高，可读性强，适合有代码洁癖和强迫症的人群。


Python的缺点主要集中在以下几点。
1. 执行效率稍低，因此计算密集型任务可以由C/C++编写。
2. 代码无法加密，但是现在的公司很多都不是卖软件而是卖服务，这个问题会被淡化。
3. 在开发时可以选择的框架太多（如Web框架就有100多个），有选择的地方就有错误。

## 应用领域


目前Python在云基础设施、DevOps、网络爬虫开发、数据分析挖掘、机器学习等领域都有着广泛的应用，因此也产生了Web后端开发、数据接口开发、自动化运维、自动化测试、科学计算和可视化、数据分析、量化交易、机器人开发、图像识别和处理等一系列的职位。

## 语法1：print

打印输出的函数， 调用示例如下

```python
print('hello', 'world', sep=', ', end='!\n')
```

**完整参数**

| 参数      | 默认     | 含义                   |
| --------- | -------- | ---------------------- |
| \*objects |          | 输出的对象，可以是多个 |
| sep       | 一个空格 | 用来间隔对象           |
| end       | \n       | 以什么结尾             |
| file      |          | 写入的文件对象         |

没试 file 

## 语法2：注释


1. 单行注释 - 以#和空格开头的部分
2. 多行注释 - 三个引号开头，三个引号结尾

## 模块1： sys

[文档](https://docs.python.org/zh-cn/3/library/sys.html?highlight=sys)

- `sys.argv` - 程序外部向程序传递的参数
- `sys.exit([arg])`  - 程序退出
- `sys.platform` - 获取当前系统平台

## 模块2：Turtle库 (绘图)

> Turtle库是Python语言中一个很流行的绘制图像的函数库，想象一个小乌龟，在一个横轴为x、纵轴为y的坐标系原点，(0,0)位置开始，它根据一组函数指令的控制，在这个平面坐标系中移动，从而在它爬行的路径上绘制了图形。

[文档](https://docs.python.org/zh-cn/3/library/turtle.html)


## 工具1：pip

> pip 是 Python 包管理工具，该工具提供了对Python 包的查找、下载、安装、卸载的功能。

### 有问题直接help看

```
pip --help
```

### 安装
```
pip install SomePackage              # 最新版本
pip install SomePackage==1.0.4       # 指定版本
pip install 'SomePackage>=1.0.4'     # 最小版本
```

## 工具2：IPython

> ipython是一个python的交互式shell，比默认的python shell好用得多，支持变量自动补全，自动缩进，支持bash shell命令，内置了许多很有用的功能和函数。学习ipython将会让我们以一种更高的效率来使用python。同时它也是利用Python进行科学计算和交互可视化的一个最佳的平台。

- tab 补全
- 在变量的前面或者后面加上一个问号?，就可以将有关该对象的一些通用信息显示出来，这就叫做对象的内省。
- 如果使用两个问号??，那么还可以显示出该方法的源代码
- 使用 `run` 命令运行脚本 

其他功能还未深入使用

## 工具3：Jupyter Notebook

启动命令
```
jupyter notebook
```

> 一个非常强大的工具，支持运行 40 多种编程语言，可以创建漂亮的交互式文档，制作教学材料，等等

## 工具4：anaconda

没看


# 练习

## 1.在Python交互环境中查看下面的代码结果，并将内容翻译成中文。

```

import this

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

- 优美更好
- 表意清晰更好
- 简单更好
- 复用更好
- 结构简单更好
- 代码有间隔比紧凑在一起更好
- 可读性很重要
- 尽管实用比简约更重用，但特殊情况也不要打破规则（想办法局部重构呗）
- 不要忽略错误，除非明确可忽略
- 有歧义时，不要理所当然猜测
- 最好只有一种明确的方式处理一件事，多考虑下也许不是那么显而易见，除非你是 Dutch ？（ Dutch —— python之父）
- 做比不做好，但立刻就做不如不做（要做，并且要有思考）
- 如果实现很难解释，这肯定不是个好方案
- 如果实现可以清晰地被解释，这大概是个好方案
- 作用域是个好主意，多使用作用域


## 2. 学习使用turtle在屏幕上绘制图形。

![](.\assets\01-01.png)