# Programming
#### 一切我知道的，你需要以及不需要知道的，关于PRG1102的知识 <br/> Everything I know that you need or don't need to know for PRG1102
#### 临时抱佛脚请参考 https://www.youtube.com/watch?v=kqtD5dpn9C8 <br/> For last minute study, please refer to https://www.youtube.com/watch?v=kqtD5dpn9C8
---

## 编译语言种类 <br/> Types of programming Language
- #### 机器语言 <br/> Machine language
  - ##### 由中央处理器直接运行 <br/> Directly executed by CPU
  - ##### 为各个处理器架构（如`x86`,`arm`等）特别编译 <br/> Customised for each architecture such as `x86` or `arm` etc.
  - ##### `.bin` 文件 <br/> `.bin` file
- #### 汇编语言 <br/> Assembly language
  - ##### 存在如同英语词汇般的简写 <br/> English like abbrieviations
  - ##### 包含基础操作的句法，允许用户对电脑的最大化控制 <br/> Contains syntax for elementary operation and allow maximum control of the computer
  - ##### 指针以及（记忆）垃圾处理是关键的 <br/> Pointers and garbage management are crucial
  - ##### `.exe`,`.dll`等文件格式以及`C++`等语言 <br/> `.exe` , `.dll` file and `C++` language etc.
- #### 高阶语言 <br/> High-level language
  - ##### 相较于前两种语言更容易阅读 <br/> Highly readable as compared with Machine language and Assembly language
  - ##### 包含更多更复杂的操作语句以及控制 <br/> Includes more syntax for much more complex action and control
  - ##### 自动化繁琐的记忆规划但也允许自行编译以减少溢出攻击等安全漏洞 <br/> Automated memory control but allow for manual instructing to minimize security flaws such as memory leaks
  - ##### `R`, `Python`, `C++` 等语言 <br/> `R`, `Python` etc.
---

## Interpreting vs Compiling
| Interpreting (可理解为口译) | Compiling 编译 |
|:----------------:|:-------------:|
|逐句翻译 <br/> Translate line by line|整体翻译并汇总输出 <br/> Translate whole code and output result|
|需要编译器才能运行 <br/> Require interpreter|程序能独立运行 <br/> Result can be used standalone|
|程序更容易使用 <br/> Programme is much more flexbile|程序属于高客制化，需要根据环境对程序做出相应变化 <br/> Programme is specified and require <br/> require porting if needed to be portable|
|程序运行更快 <br/> Programme is usually slower|程序运行相对缓慢 <br/> Programme is usually faster|
|python 3.10|py2exe|

## Code Organisation 编码组织
- #### 代码必须有序以方便后续的维修以及更新工作 <br/> Code needs to be organised so maintainance and update can be done
- #### 模块 <br/> Module
  - ##### 模块可视为一组可单独运行的代码 <br/> Module is a piece of code that can be run independently
  - ##### 程序中可以引入模块，模块是可以重复使用的 <br/> Module can be imported to be used in a program and is reusable
- #### 工程 <br/> Project 
  - ##### 一个工程中包含了同一个程序中所需的所有文件以及代码 <br/> A project contains all the file under the same programme
  - ##### 当程序逐渐复杂化，将代码分组互相引入将有助与维修以及排错 <br/> When a programme gets large, it is usually better to separate into different files and cross refer to better debug and maintain
  - ##### 在开发大规模工程时经常会使用各种集成开发环境(IDE) <br/> IDE(`Integrated Development Environment`)s are usually used when working with projects
  - ##### 常见的 IDE 有python IDE 以及 VSCode <br/> python IDE and VSCode are examples of commonly used IDEs
- #### 包管理器 <br/> Package Manager 
  - ##### 一个包管理器就如同一个有着许多好用的代码的商店 <br/> A package manager can be thought of as a store of library of codes that are useful and general.
  - ##### 有了包装管理器，我们可以有效的引用以及管理程序中的包等现有代码 <br/> With a package manager, packages and libraries can be imported and managed efficiently.
  - ##### 常见的包管理器有 `PIP`(python) 以及 `node.js`(JavaScript) <br/> `PIP`(python) and `node.js`(JavaScript) are examples of Package manager.
- #### 命名空间 <br/> namespace 
  - ##### 命名格式化在避免撞名引起的程序溃败里至关重要 <br/> Namespacing is crucial to avoid name clashes causing the programme to fail
  - ##### 在 `Python` 中，命名空间由各个组成空间各自定义 <br/> In python, namespaces are defined by the indiviual modules.
  - ##### 在`C++`语言中常见一条 `namespace std::`，这有助与节省代码，把 `std::cout` 以及 `std::cin` 等价代换成 `cout` 以及 `cin` <br/> It is also commonnly seen to have a line of `namespace std::` at the start of a `C++` programme indicating the default namespace in the programme. In `C++` the syntax looks like `std::cout` and `std::cin` and utilising the namespace setting the syntax can be shorten into `cout<< text` and etc.
---
## Data Types 数据类型
- #### 一个动态语言里的自变量可以用`名字=数值`的方式来定义 <br/> A variable can be defined as `name = value` in python and other dynamically typed language
- #### 静态语言（C++等）里的自变量需要先被定义，比如 `int 名字 = 1`, int 代表`整数类` <br/> For a static typed language such as `C++` the types need to be declared initally such as `int a = 1`
- #### 每个编译语言中含有的数据类型各不相同 <br/> There are many data types and some languages might have some that other languages doesn't include
- #### Python中有的数据类型如下：<br/>Here are some examples in python:
  - ##### 整数类（允许从负二十亿到正二十亿的数值）<br/> integer (Whole number integer, 32bit, from -2 billion to 2 billion)
  - ##### 浮点类（允许小数点，但小数点的具体位置作为一个自变量暂居其中的一小部分储存空间，因其小数点能“漂浮”故称浮点）<br/> float (for decimal but the decimal point is floating, hence the name, and part of the memory is used to store the location of the point)
  - ##### 布尔值（只有`真`以及`假`两种数据，通常作为逻辑运算的结果）<br/> boolean (`true` or `false`, as a result of logical comparison)
  - ##### 字符串（在早期的变成语言中字符只能单独储存，字句只能以一连串的字符并排储存，故称字符串）</br> String (In early stages of programming, `char` only can hold 1 character and thus words and sentences are assigned as a string of `char` thus the name `string`)
    - ###### 通常用户输入会先被储存成一个字符串，在进行后续处理 </br> A user input is usually saved as a string and will be further processed for further usage
    - 语句 <br/> syntax:
``` python
input = input("Please type any integer number:")
```
  - ###### `input(提示句)`表示让程序输出`提示句`，读取用户输入，并储存在相应的自变量中 </br> `input(hints)` indicates the programme to print the `hints` sentences then read the input from user and save it to the predetermined variable
  - ###### `\n` 表示新一行 </br> `\n` indicates a new line to be started
  - ##### 列表 <br/> list 
    - 语句 <br/> syntax: []
    - 用于储存多个数据在一个合集中 <br/> used to store a number of datas together like a collection
    - 编号由0开始<br/> index starts at 0
    - 次序有别 <br/> The sequence of data matters 
``` python
lista = ["a","b","c"]
lista[0] #"a"
lista[1] #"b"
listq = lista + ["x","y","z"]
listq[4] #"y"
```

```python
listq[5]= "q"
listq #["a","b","c","x","y","q"]
listq.pop()
listq #["a","b","c","x","y"]
listq.pop(2)
listq #["a","b","x","y"]
```
  - ##### 词典 <br/> Dictionaries
    - 语句 <br/> syntax: `name = {"key":"value"}`
    - 数据以键值对的形式储存 <br/> The datas are stored in key-value pair
    - 数据的内容可以透过对应的键值检索得到 <br/> Values can be looked up by using the key value
  - ##### 元组 <br/> tuples 
    - 语句 <br/> syntax: `name=(object1,object2...)`
    - 数据永久也有序，不能被更改 <br/> The datas are permanent and ordered
    - 允许重复的内容 <br/> Allow duplicate value
  - ##### 合集 <br/> Sets
    - 语句 <br/> syntax: `name={object1,object2...}`
    - 数据可更动 <br/> The datas are changable
    - 不允许重复的内容 <br/> Doesn't allow duplicate value
  - ##### 注意有许多数据类型时这里没有提及的，比如指针。这些在更复杂的情况下必然有用，比如双指针哈希表等等，但是在这里我们不需要也不会学到。<br/> Note that there are a lot of other data types out there such as pointers that are certainly useful in advanced use case by we will not be learning it for now.
---

## 语法 <br/> Syntax
- #### 语法规定一个编码语言里的代码该如何编写 <br/> Syntax can be thought of as the grammar of a certain programming language
- #### 有一些关键字被预留作为语法里的一部分 <br/> There are some keyword that are reserved as a part of the syntax
  - ##### Python 预留关键字包括：`if`, `elif`, `else`, `while`, `for` <br/> some of the examples include: `if`, `elif`, `else`, `while`, `for` and more for python
- #### 数学运算符号也被预留作为逻辑运算以及数学运算的符号 <br/> Numerical operator are also reserved for logical and numerical operation.
- #### 根据输入的内容种类，有些符号具有多个用途 <br/> Some operator can be used for different purposed depending on the input
- #### 为了下表理解，假设`a=真` and `b=假` <br/> For context of some of the operator mentioned below, we will assume `a=true` and `b=false`
|符号 <br/> Operator|描述<br/> Description|举例<br/>Example|输出<br/>Output|
|:---:|:---:|:---:|:---:|
|`+`|加法</br>Addition|1+2|3|
|`-`|减法</br>Subtraction|1-2|-1|
|`*`|乘法</br>Multiplication|8\*7|56|
|`/`|除法</br>Division|8/3|2.3333|
|`%`|取余</br>Modulo/Remainder|8%3|2|
|`**`|次方</br>Power|2**3|8|
|`==`|等同</br>Is equal to|2==3|`false`|
|`!=`|不同</br>Is not equal to |2!=3|`true`|
|`<`|少于</br>Less than|2<2|`false`|
|`<=`|少于或等于</br>Less than or equal to|2<=2|`true`|
|`>`|大于</br>More than|2>2|`false`|
|`>=`|大于或等于</br>More than or equal to|2>=2|`true`|
|`&&`|与门</br>AND|a&&b|`false`|
|`\|\|`|或门</br>OR|a\|\|b|`true`|
|`!`|非门</br>NOT| !a|`false`|
- #### 注意`<`以及`>`也可被用于改变二进制数据 </br>Note that `<` and `>` can also be used to manipulate binary datas
---

## 数字的运作</br> Working with Numbers
- #### 如同上诉表明，数学符号可以用于改变数字的值</br>Numbers can be manipulated with some of the operator as mention in syntax part
- #### 当一个数字作为计数使用时（如在循环里），增量以及减量可以如下实施 <br/> When numbers are in counter, it can be incremented and decremented such as when in a loop.
  - ##### `a++`
  - ##### `a--`
- #### 当输入四则运算时，把算式如同输入计算机般输入程序，代换符号即可 <br/> When working with arithmetic, the sequence is the same as when inputed into a calculator
---

## 字符串的运作 </br> Working with String
- #### 字符串的结合 </br> String Concatenation
  - ##### `"ali"+"abu"` 生成 `"aliabu"`</br>`"ali"+"abu"` gives `"aliabu"`
- #### 分裂字符串 </br> Splitting String
  - ##### `"ali".split()`生成列表`["a","l","i"]`</br>`"ali".split()` gives a list `["a","l","i"]`
- #### 字字符串 </br> Substring
  - ##### 等同于先分裂，后将所需的字符结合成新的字符串 </br> Equivalent to firsting splitting a string then concatenating the selected element
  - ##### `aliabu.substring(1,2)`生成`"li"`(注意python中的元素编号永远从0开始，即第一个"a"为0)</br>`aliabu.substring(1,2)` gives `"li"` (note that the sequence of index always start in 0 in python)
- #### 大小写转换 </br> Case Conversion
  - ##### `.lower()`
  - ##### `.upper()`
- #### 格式化字符串 </br> f-String
  - ##### 可以在需要输出的字符串中需要引用其他自变量值或额外处理时使用 </br>Used when part of the string/ text to be printed is refered to another variable or need additional process
  - ##### `print(f'one plus one is equal to {1+1}')`将输出`one plus one is equal to 2`</br> `print(f'one plus one is equal to {1+1}')` will gives `one plus one is equal to 2`
  - ##### 自变量的数值可以在{}中被提及一遍输出检索 </br> Variable can be referred in the curly braces {} for the output to refer.
- #### 字符串的长度 </br> Length of string
  - ##### `len("aliabu")` 生成 `6` </br> `len("aliabu")` gives `6`
---

## 程序架构/控制架构 </br> Control Structure
- #### 次序化架构 </br> Sequential Flow
  - ##### 如同食谱中一步一步教学的结构的代码 </br> The code is structured as such of a cookbook
```python
a = 1
b = 2
print(a+b)
```
- #### 输出 </br> Output:
```
3
```
- #### 条件化架构 </br> Conditional Flow
  - ##### 根据条件产出的布尔值决定下一步运行的代码 </br> The code to run will be decided by the condition met
  - ##### `elif` 为 `else if` 的缩写，两者之间可互相交换 </br> `elif` is the short form of `else if`, both are interchangable with each other
```python
a = "coconut"
b = "apple"
if len(a) == len(b):
    print("a 以及 b 长度相同")
elif len(a) < len(b):
    print("a 比 b 短")
else: 
    print("b 比 a 短")
```
- #### 输出 </br> Output:
```
b 比 a 短
```

- #### 重复性架构 </br> Iteration Flow
  - ##### 在给定条件下不断重复一段代码直至达成截断条件，或是重复给定次数 </br> The code to run will be decided by the condition met
```python
for x in range(4):
    print(x)
```
- #### 输出 </br> Output:
```
0
1
2
3
```
  - ##### 截断条件形重复性架构 </br> Breaking conditional iterational structure
```python
x = 3
while x<10:
    print(x)
    x++
```
- #### 输出 </br> Output:
```
3
4
5
6
7
8
9
```

- #### `range()` 是一个在循环中以及各种条件检测中常见的代码，对它的了解有助于更好的控制循环以及次数</br> `range()` is a especially common function in terms of looping and condition checking, understanding it would help in controlling the flow and iteration and such drastically.
- #### `range()` 的输入参数有`start`,`end`,`step`, 句式为`range(start,end,step)`</br>`range()` has parameters of `start`,`end`,`step`
  - ##### `start` 标记起始数字</br> `start` indicates the starting number
  - ##### `end` 标记结束数字或顶值（函数将输出一切小于`end`的`start` + n* `step`，其中n为整数的的数字并包装成列表）</br> `end` indicates the ending number or the ceiling value (Such that the funciton would output all the numbers that fulfill the form of `start` + n*`step` while whole number n that is smaller than `end` into a list)
  - ##### `step` 标记数字间的间隔 </br>`step` indicates the step between all the iterated numbers.
- 代码：</br> code: 
```python
for x in range(1,14,3):
    print(x)
```
- 输出</br>output:
```
1
4
7
10
13
```

- 代码：</br> code: 
```python
for x in range(1,5):
    print(x)
```
- 输出</br>output:
```
1
2
3
4
```


- 代码：</br> code: 
```python
for x in range(7):
    print(x)
```
- 输出</br>output:
```
1
2
3
4
5
6
```
---

## 函数 </br> Function
- #### 函数是一组代码，可以提出输入参数或不提取，然后执行其内涵的代码 </br> Function is a block of code, taking or not taking in any arguments, then running the code as defined
- #### 基础句式：</br> Basic Syntax:
```python
def 函数名称name():
    #运行代码 Code to run
    print("hi")
    return ("a")
    #里面可以是 `for` 循环，条件判别，等等更复杂的代码，需要在同一个程序里多次运行，则会编为独立函数, Within the function, it could be a `for` loop, conditional testing, or much more complex code. If a sequence of code need to be ran several times throughout the programme, then it would be separated into a individual function.
    #`return`用以表诉函数输出的值，可以用于储存在另外的自变量，用于接下来的代码
```
- #### 定式函数，即当输入参数为固定数量及种类时 </br> Fixed Function, functions that has a fixed number and types of argument as defined

- #### 句式：</br> Syntax:
```python
def hello(name)
    print("Hello! " + name)
```
- #### 这里 `hello()` 函数强制要求一个参数 </br> Here, `hello()` functions necessitates one input
- #### 当运行 `hello("Bob")` 则会输出 `Hello! Bob` </br> When `hello("Bob") is ran, `Hello! Bob` is outputed
- #### 若运行 `hello()` 或者 `hello("Bob","Ali")` 则将出现报错 </br> If `hello()` or `hello("Bob","Ali")` is ran instead, an error will be raised.
- #### 未知函数数量 </br> Unknown argument counts
  - ##### 当无法确定参数数量时，则能在函数定义里加入 `*args` 以星号表示未能确定参数数量，输入的参数将以列表形式进入函数进行处理 </br> When the number of arguments are unable to be confirmed, `*args` could be added into the definition to indicate the inability to confirm the number of arguments, as such those argument would be treated as a list in the function

  - ##### 句式：</br> Syntax:
```python
def hello(*args)
    for x in args:
        print("Hello! "+ x)
```
  - ##### 若运行 `hello("Bob","Ali")` 将输出： </br> If `hello("Bob","Ali")` is ran, the output would be:
`Hello! Bob`

`Hello! Ali`
- #### 键值对参数函数 </br> Function with key-value pair as input
  - ##### 某些函数需要输入键值对作为运算参数，这也能在定义中提及参数的名称 </br> Let's say for certain function, multiple key-value pair is needed, the key could be mentioned in the definition and the code
  - ##### 句式：</br> Syntax:
```python
def payment(principal,time,frequency,interest):
    payment = principal/((1-(1+interest)**(-1*time*frequency))/interest)
    return payment
```
  - ##### 则可以运行 `payment(10000,10,3,0.05)` 或 `payment(principal=10000,time=10,frequence=3,interest=0.05)` 以作出相应算式</br> Then `payment(10000,10,3,0.05)` or `payment(principal=10000,time=10,frequence=3,interest=0.05)` could be ran to do the calculation
- #### 未知参数键值对数量函数 Function with unknown number of key-value pair as inputs
  - ##### 同上，若运行 `payment(10000)` 或 `payment(principal=10000)` 则将报错</br> Similarly, if `payment(10000)` 或 `payment(principal=10000)` is ran, an error will be raised
  - #### 若想著名未知参数键值对数量，可用`**kwargs`，用双星号表示未知数量的键值对，这里不做示范，详细参考`*args`。 </br> If the number of keyword-value pair of input is undecided, `**kwargs` could be used to indicate. The syntax is similar as such of unknown number argument.

- #### 递归函数 Recursion
  - ##### 当函数自身在自身的定义中被提及，则称递归函数</br> When a function is ran or mentioned within the function definition itself, then it is a recursion.
  - ##### 句式: </br> Syntax:
```python
def factorial(n):
    if n==1:
        return 1
    elif n>1:
        return n*factorial(n-1)
```
  - ##### 在使用递归函数时如不谨慎可导致无限循环，堆栈溢出等等问题，需格外注意。</br> When using recursion, the user should be careful, and have a stopping statement, for otherwise unending looping or stack overflow etc. could be caused.
  
- #### 朗达函数 Lambda Function
  - ##### 朗达函数为一些简单的，不被命名的函数。只需要一行即可</br> A Lambda function is a function that is simple enough and unnamed. It would only takes one line.
  - ##### 句式: </br> Syntax:
```python
cube_x = lambda x:x**3
cube_x(3) #output 27
```
---

## 档案处理 </br> File Processing
- #### 在许多真实用到的程序中，运行中所需的资讯需要长时间被储存，而非在程序关闭时即删除，例如登录户口，近期文件等等。而这些资料可以透过多种方式储存，例如放上伺服器，或是更简单的就是放在一个文档里，下次打开再载入。</br> In real world application, some of the information in runtime need to be saved for a long time, instead of being deleted right after the programme is terminanted, such as user-auth, recent files etc. These information could be saved with many ways, such as uploading to a server, or simply writing to a text file.
- #### 本质上，这与一个程序运行时定义的自变量等同，不过于此需要延长时效性，或是记录长时间的变化，让程序不会每次都格式化。 </br> This is technically similar to the variable defined and allocated at the runtime, but as the data need to be hold for longer time, to record the change etc. so that the programme would not be formatted if needed.
- #### 文件系统/层级系统 </br> File System 
  - ##### 文件系统为电脑文件的分级规划系统，等同于不断包裹的文件夹。若要寻找到某个文件对其进行阅读或编写工作，则需要知道其与程序的位置。 </br> File system is the system of organising file in the computer, as if there's many folders holding folders etc. If we would like to read or write to a file, the specific location of the target file is needed.
  - ##### 母文件通常的地址为 `/` 或是 Windows 的 `C:/` 等，于此可以透过不断穿梭子文件直到找到文件所在。 </br> The root directory is usually located as `/` or as those in Windows `C:/` , the location of the file can then be located through the subfolders.
  - ##### 一个有效的的（绝对）文件地址如：`C:\Program Files\Adobe\Adobe InDesign 2021.exe` </br> An effective (absolute) file diretory looks like `C:\Program Files\Adobe\Adobe InDesign 2021`
  - ##### 在程序中通常不需要用到绝对文件地址，除非是跨文件夹更动，这里只需要相对文件夹地址。 </br> In a programme, an absolute file directory is usually overpowered, and relative file directory would usually be sufficient.
  - ##### 在相对文件地址中，一切以程序母档案的地址为起始点，若是比程序更深一层（如在和程序同层中的`A`文件夹中的`text.txt`），则可以写 `A/text.txt`，若是在上一层（若觉得饶可以参考上诉地址，并想象在`Adobe`里要去到`Program Files`的文件夹，则写作`../`,以双点作为返回一层的表示）</br> In relative file directory, everything starts at the source file of the programme, if the file to locate is deeper into the folders, e.g. a `text.txt` located within folder `A` at the same level, then the directory is as `A/text.txt`. If the target file is a one layer before the source file of the programme, such as locating `Program Files` from `Adobe` with the direction mentioned above, then the directory write as `../`, meaning to locate the parent directory.
- #### 在知道了文件的地址后，我们就能够在程序中对其做出阅读以及编写的工作。 </br> After knowing the directory of a file, we can now read and write to the file.
- #### Python 内建函数 `open()` 让我们能够打开文件并修改过阅读文件内的内容。 </br> The built-in function `open()` allows us to open the file then read or write to the file.
- #### `open()` 函数需要两个参数，一为文件的相对地址，二位打开模式。 </br> `open()` functioon requires 2 parameters, first is the directory, and second is the mode of access.
- ####  `open()` 的打开模式被默认为 `rt`，其中 `r` 表示阅读（不含编写），`t` 表示文本。其他的参数可以参考如下： </br> `open()` has a default paramter of `rt`, with `r` indicating reading mode, `t` indicating text mode. Other paramter are as listed.
|标记/参数 </br> flag/parameter| 意义 </br> meaning|
|:---:|:---:|
|`r`|阅读</br> Reading|
|`w`|编写</br> Writing|
|`a`|增加</br> Appending|
|`r+`|同时阅读与编写</br> Reading and Writing|
|`t`|文本模式</br> Text mode|
|`b`|二进制模式 </br> Binary mode|

- #### 其中`r`，`w`，`a`，`r+`之间四选一，`t`和`b`之间二选一，共八种组合。</br> In that, one from  `r`,`w`,`a`,`r+` would be chosen, with one from `b` and `t` being chosen, totalling at eight total combination
- #### 假设`text.txt`内容如下：</br> Assume that the content of `text.txt` is as below:
```
Thou shall never leave my mind

For I loved you

Then, and since then
```
```python
infile = open(text.txt,`rt`)
```

- #### 此时，我们可以对`text.txt`进行查阅 </br> Now, we can read `text.txt`
```python
infile.read(1)
```
输出：</br> Output:
```
T
```
- #### 然后执行：</br> Then we run:
```python
infile.read(5)
```
输出：</br> Output:
```
hou s
```
- #### 以此类推，括号里的数字是多少，便会输出多少个之前未读到的字符 </br> And so on, with the number in the brackets as the number of unread character from the string being outputed.
- #### 若括号内没有注明数字则阅读至本行结束，即：</br> If there's no number in the brackets, then the remaining char from the whole line would be outputed.
```python
infile.read()
```
输出：</br> Output:
```
hall never leave my mind\n
```

- #### 此时执行:</br> Now, we run:
```python
infile.readline()
```

输出：</br> Output:
```
\nFor I loved you\n
```

- #### 顾名思义`readline()`将读取一整行文字，直到`\n`因其表示新一行的开始</br> As the name implies, `readline()` will read the whole line and output it, until it reaches `\n` indicating the start of a new line.

- #### 设`test.txt`为一个空的文件 </br> Assume that `test.txt` is an empty text file
- #### 此时执行:</br> Now, we run:
```python
outfile = open(test.txt,`wt`)
```

- #### 则: </br> Then:
```python
outfile.write("HI")
```
输出：</br> Output:
```
2
```
- #### 每当我们执行一次 `write()` 都会输出文件中当前文本的长度</br> Everytime we run `write()`, the updated length of text within the file is outputed.
- #### 无论是读还是写写，在执行完成后，都需要关闭文件：</br> Regardless of reading or writing is done, after the execution, the file should be closed:
```python
infile.close()
outfile.close()
```
