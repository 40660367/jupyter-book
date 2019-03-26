---
redirect_from:
  - "/chapter1/1gettingstarted"
interact_link: content/C:\Users\David\jb\jupyter-book\content\chapter1/1Gettingstarted.ipynb
kernel_name: julia-1.0
title: '开始之前'
prev_page:
  url: /chapter1/index
  title: '第一篇：基础入门'
next_page:
  url: /chapter1/2Strings
  title: '字符串'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---

# Getting started

Topics:
1.  How to print
2. How to assign variables
3. How to comment
4. Syntax for basic math

## How to print

In Julia we usually use `println()` to print



{:.input_area}
```julia
println("I'm excited to learn Julia!")
```


## How to assign variables

All we need is a variable name, value, and an equal's sign!<br>
Julia will figure out types for us.



{:.input_area}
```julia
my_answer = 42
typeof(my_answer)
```




{:.input_area}
```julia
my_pi = 3.14159
typeof(my_pi)
```




{:.input_area}
```julia
😺 = "smiley cat!"
typeof(😺)
```


To type a smiley cat, use tab completion to select the emoji name and then tab again



{:.input_area}
```julia
# \:smi + <tab> --> select with down arrow + <enter> ---> <tab> + <enter> to complete
```


After assigning a value to a variable, we can reassign a value of a different type to that variable without any issue.



{:.input_area}
```julia
😺 = 1
```




{:.input_area}
```julia
typeof(😺)
```


Note: Julia allows us to write super generic code, and 😺 is an example of this. 

This allows us to write code like



{:.input_area}
```julia
😀 = 0
😞 = -1
```




{:.input_area}
```julia
😺 + 😞 == 😀
```


## How to comment



{:.input_area}
```julia
# You can leave comments on a single line using the pound/hash key
```




{:.input_area}
```julia
#=

For multi-line comments, 
use the '#= =#' sequence.

=#
```


## Syntax for basic math



{:.input_area}
```julia
sum = 3 + 7
```




{:.input_area}
```julia
difference = 10 - 3
```




{:.input_area}
```julia
product = 20 * 5
```




{:.input_area}
```julia
quotient = 100 / 10
```




{:.input_area}
```julia
power = 10 ^ 2
```




{:.input_area}
```julia
modulus = 101 % 2
```


### Exercises

#### 1.1
Look up docs for the `convert` function.

#### 1.2
Assign `365` to a variable named `days`. Convert `days` to a float and assign it to variable `days_float`



{:.input_area}
```julia
@assert days == 365
@assert days_float == 365.0

```


#### 1.3
See what happens when you execute

```julia
convert(Int64, "1")
```
and

```julia
parse(Int64, "1")
```



{:.input_area}
```julia
Please click on `Validate` on the top, once you are done with the exercises.
```

