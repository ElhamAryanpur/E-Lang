# E-Lang

`E-Lang is human readable computer programming language`

E-Lang was designed to look exactly as English grammer while holding its computer programming power! Written with Python 3.6.8 and is licenced as MIT. This is the Documentation on how to use this language!

## Requirement

To use E-Lang, you should first make sure you have [Python](https://www.python.org) version 3.x and Pip installer and on `Path`! Then you can compile it two ways:
1. Pyinstaller

  To use this method, install it with pip: `pip install pyinstaller`. Then navigate to the folder that E-Lang.py lives and type: `python -m pyinstaller --onefile E-Lang.py`. This should make two folders and a file. Navigate to "dist" folder and there will be the compiled E-Lang that you can use on your system!

2. Nuitka

  Nuitka is a bit tricky and hard to set up but it is recommended to use nuitka for production or less size purposes. To use nuitka, first install it: `pip install nuitka`. Then set up C++ compiler as mentioned in [Nuitka Docs](http://www.nuitka.net). After that you will be able to compile E-Lang compiler with: `python -m nuitka --standalone --follow-imports --show-progress E-Lang.py`
  
## Getting Started

Before starting to use E-Lang, you should first know some things! E-Lang is a compiler that was built with python! Python is an interpreter which means it is not supposed to be standalone. So you won't be able to compile **your** E-Lang codes as standalone! What you **can** do instead is to write all your code in a file named `c.e` and rename the E-Lang compiled compiler as your program! When someone run E-Lang compiled compiler, it would automatically start executing the `c.e` code! So your program would look like:

- <your_program>.(the system executable architecture)
- c.e

EXAMPLE:

- MyFirstECode.exe
- c.e

Maybe in next few releases the standalone feature be made!

## USAGE

As said, the syntax (grammer) of E-Lang was built to look like English. The E-Lang compiler execute your code line by line thus you can not write two statements in one line! A `Hello World!` Program in E-Lang would look like:

```
  show Hello_World!
```
NOTE! In E-Lang, you do not need to add quotations(" ') to beginning and end of each string! Rather, you add Underscores( _ ) in place of each white space between string words! Upon execution, the unerscores will be replaced with white space to represent your sentence! If you for example have a sentence that need underscore in between, you can replace the underscore with ( - ) to represent same idea! This factor was choosed for efficiency and readability of E-Lang code!

### Data Types of E-Lang:

1. Strings: Which contains alphanumeric stream with underscores ( _ ) in place of spaces! You can have unlimited, or the highest limit on system, characters on your strings!
2. Numbers: Which contains digits without decimal places. You can have unlimited, or the highest limit on system, digits on your numbers!

### Variables

Variables are a place in memory to store temporary data! In E-Lang, you can store both string and number variables! The syntax to store variable:
```
  var <name of variable> = <data of variable>
```
**name of variable** being the name you wish to call your variable! (NOTE: Do not add space or underscores ( _ ) to your variable names!) and **data of variable** being the data you wish to store in your variable!

Example:
```
  var myVar = Hello_World!
```
#### NOTE:
You should always use exact layout as shown in syntax and examples! E-Lang parse the code in parts splitted by *spaces*. So if you mistype spaces or forget to type spaces in specific order, the code will be executed incorrectly which may result in errors or incorrect execution!

### Showing data on screen

To show your data on screen, you can use `show` keyword:
```
  show <data you wish to show>
```
Example:
```
  show Hello_World!
```

### Taking input

To take input from the user, you can use the keyword `take`:
```
  take <variable to save>
```
with **variable to save** being the name of variable you wish to save the collected data! (NOTE: Do not use spaces or underscores ( _ ) on your variable name)

Example:
```
  take my-Input
```

### Doing MATH

You can do _**basic**_ math in E-Lang, for now. The four legendary operations that is groundwork for math world in E-Lang which are `+` as addition `-` as subtraction `*` as multiplication and `/` for division. NOTE: You can only do one operation in each line:
```
  sum <variable to save results> <first number> <operator> <second number>
```
NOTE: You can also use variables in place of numbers! If variable don't exist, then it will show error and stop your program!

Example:
```
  sum my-results 10 + 10
```
Another example:
```
  var first-number = 10
  var second-number = 10
  
  sum my-result first-number + second-number
```

### Conditions

You can have conditions in E-Lang (because why not? they are cool!):
```
  if <first data> <condition> <second data> then <operation to do if it condition is correct>
```
You can do four conditions: 
 - `=` to compare first data to second data! Will be true if both sides have same data!
 - `>` to compare if first data is bigger than second data (numbers)! Will be true if first data is bigger than second data!
 - `>` to compare if second data is bigger than first data (numbers)! Will be true if second data is bigger than first data!
 - `not` to compare if first data is not the same as second data! If first data is truely not exactly the same as second data, then it will return true!

Example:
```
  if 1 = 1 then show 1_is_equal_to_one!
  if 2 > 1 then show 2_is_bigger_than_1!
  if 1 < 2 then show 1_is_smaller_than_2!
  if 1 not 2 then how 1_is_not_equal_to_2!
```

### Emulate command line

If you wish to emulate command line, you can use `run` keyword:
```
  run <commands to run. You can add spaces too!>
```
Example:
```
  run echo Hello World!
```
### Comments
To add a comment in your code, just write normal sentences! E-Lang always look for the first word to do it's execution so if you write your first word of comment anything that is not used by statements, it will be a comment! Comments are not executed and are ignored upon compilation!

### Save to file
at some point, you will need to save data for later use! Good news is that doing this is really really simple in E-Lang:
```
  to write to file use:
  write <data> to <file name>
  
  to append to file:
  append <data> to <file name>
  
  to read file:
  read <file name> and save to <variable name>
```
**Writing** and **Appending** are pretty much same in syntax except append adds the data on side of current data that exist in file! 

_**NOTE**_: All files should be either under or on same directory!

Example:
```
  write Hello to hello.txt
  
  append _World! to hello.txt
  
  read hello.txt and save to reading-variable
```

## EXAMPLE PROJECT
Here is code for a simple calculator in E-Lang:
```
  show Enter_the_first_number:
  take first-number

  show Enter_the_second_number:
  take second-number

  show What_operation_to_do?_(add_sub_mul_div):
  take operator

  if operator = add then sum result first-number + second-number
  if operator = sub then sum result first-number - second-number
  if operator = mul then sum result first-number * second-number
  if operator = div then sum result first-number / second-number

  show
  show Results_are:
  show result
```

## Final Words

Well, you have came to end of E-Lang's current documentation! If you had further questions or suggestions, you can find me on [Facebook](https://www.facebook.com/elham.aryanpur.10) and on [Instagram](https://www.instagram.com/elham_aryanpur)
