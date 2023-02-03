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

## Syntax
- #### Syntax is a set of rules defining how the code should be written
- #### Syntax can be thought of as the grammar of a certain programming language
- #### There are some keyword that are reserved as a part of the syntax
  - ##### some of the examples include: `if`, `elif`, `else`, `while`, `for` and more for python
- #### Numerical operator are also reserved for logical and numerical operation.
- #### Some operator can be used for different purposed depending on the input
