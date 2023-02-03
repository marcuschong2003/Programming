# Programming
#### Everything I know that you need or don't need to know for PRG1102
---

## Types of programming Language
- #### Machine language
  - ##### Directly executed by CPU
  - ##### Customised for each architecture such as `x86` or `arm` etc.
  - ##### `.bin` file
- #### Assembly language
  - ##### English like abbrieviations
  - ##### Contains syntax for elementary operation and allow maximum control of the computer
  - ##### Pointers and garbage management are crucial
  - ##### `.exe` , `.dll` etc.
- #### High-level language
  - ##### Highly readable as compared with Machine language and Assembly language
  - ##### Includes more syntax for much more complex action and control
  - ##### Automated memory control but allow for manual instructing to minimize security flaws such as memory leaks
  - ##### `R`, `Python`, `C++` etc.
---

## Interpreting vs Compiling
| Interpreting | Compiling |
|:----------------:|:-------------:|
|Translate line by line|Translate whole code and output result|
|Require interpreter|Result can be used standalone|
|Program is much more flexbile|Program is specified and require <br/> require docking if needed to be portable|
|Program is usually slower|Program is usually faster|
|python 3.10|py2exe|

## Code Organisation
- #### Code needs to be organised so maintainance and update can be done
- #### Moduling
  - ##### Module is a piece of code that can be run independently
  - ##### Module can be imported to be used in a program and is reusable
- #### Project
  - ##### A project contains all the file under the same programme
  - ##### When a programme gets large, it is usually better to separate into different files and cross refer to better debug and maintain
  - ##### IDE(`Integrated Development Environment`)s are usually used when working with projects
  - ##### python IDE and VSCode are examples of commonly used IDEs
- #### Package Manager
  - ##### A package manager can be thought of as a store of library of codes that are useful and general.
  - ##### With a package manager, packages and libraries can be imported and managed efficiently.
  - ##### `PIP`(python) and `node.js`(JavaScript) are examples of Package manager.
- #### namespace
  - ###### Namespacing is crucial to avoid name clashes causing the programme to fail
  - ###### In python, namespaces are defined by the indiviual modules.
  - ###### It is also commonnly seen to have a line of `namespace std` at the start of a `C++` programme indicating the default namespace in the programme
    - In `C++` the syntax looks like `std::cout` and `std::cin` and utilising the namespace setting the syntax can be shorten into `cout<< text` and etc.
---
## Data Types
- #### A variable can be defined as `name = value` in python and other dynamically typed language
- #### For a static typed language such as `C++` the types need to be declared initally such as `int a = 1`
- #### There are many data types and some languages might have some that other languages doesn't include
- #### Here are some examples in python:
  - ###### integer (Whole number integer, 32bit, from -2 billion to 2 billion)
  - ###### double (for precise decimal as they allocate the most memory for single variable
  - ###### float (for decimal but the decimal point is floating, hence the name, and part of the memory is used to store the location of the point)
  - ###### boolean (`true` or `false`, as a result of logical comparison)
  - ###### list 
    - syntax: []
    - used to store a number of datas together like a collection
    - index starts at 0
    - The sequence of data matters
  - ###### Dictionaries
    - syntax: `name = {"key":"value"}`
    - The datas are stored in key-value pair
    - Values can be looked up by using the key value
  - ###### tuples
    - syntax: `name=(object1,object2...)'
    - The datas are permanent and ordered
    - Allow duplicate value
  - ###### Sets
    - syntax: `name={object1,object2...}`
    - The datas are changable
    - Doesn't allow duplicate value
  - ###### Note that there are a lot of other data types out there such as pointers that are certainly useful in advanced use case by we will not be learning it for now.
---

## Syntax
- #### Syntax is a set of rules defining how the code should be written
- #### Syntax can be thought of as the grammar of a certain programming language
- #### There are some keyword that are reserved as a part of the syntax
  - ##### some of the examples include: `if`, `elif`, `else`, `while`, `for` and more for python
- #### Numerical operator are also reserved for logical and numerical operation.
- #### Some operator can be used for different purposed depending on the input
- #### For context of some of the operator mentioned below, we will assume `a=true` and `b=false`
|Operator|Description|Example|Output|
|:---:|:---:|:---:|:---:|
|`+`|Addition|1+2|3|
|`-`|Subtraction|1-2|-1|
|`*`|Multiplication|8\*7|56|
|`/`|Division|8/3|2.3333|
|`%`|Modulo/Remainder|8%3|2|
|`**`|Power|2**3|8|
|`==`|Is equal to|2==3|`false`|
|`!=`|Is not equatl to |2!=3|`true`|
|`<`|Less than|2<2|`false`|
|`<=`|Less than or equal to|2<=2|`true`|
|`>`|More than|2>2|`false`|
|`>=`|More than or equal to|2>=2|`true`|
|`&&`|AND|a&&b|`false`|
|`\|\|`|OR|a\|\|b|`true`|
|`!`|NOT| !a|`false`|
- #### Note that `<` and `>` can also be used to manipulate binary datas
---

## Working with Numbers
- #### Numbers can be manipulated with some of the operator as mention in syntax part
- #### When numbers are in counter, it can be incremented and decremented such as when in a loop.
  - ##### `a++`
  - ##### `a--`
- #### When working with arithmetic, the sequence is the same as when inputed into a calculator
---

## Working with String
- #### String Concatenation
  - ##### `"ali"+"abu"` gives `"aliabu"`
- #### Splitting String
  - ##### `"ali".split()` gives a list `["a","l","i"]`
- #### Substring
  - ##### Equivalent to firsting splitting a string then concatenating the selected element
  - ##### `ali.substring(1)` gives `"li"` (note that the sequence of index always start in 0 in python)
- #### Case Conversion
  - ##### `.lower()`
  - ##### `.upper()`
- #### f-String
  - ##### Used when part of the string/ text to be printed is refered to another variable or need additional process
  - ##### `print(f'one plus one is equal to {1+1}')` will gives `one plus one is equal to 2`
  - ##### Variable can be referred in the curly braces {} for the output to refer.
