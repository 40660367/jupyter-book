---
redirect_from:
  - "/chapter2/2arithmeticassignmentandstrings"
interact_link: content/C:\Users\David\julia\jupyter-book\jupyter-book\content\chapter2/2ArithmeticAssignmentandStrings.ipynb
kernel_name: julia-1.0
title: 'ArithmeticAssignmentandStrings'
prev_page:
  url: /chapter2/1VariationsOnSum
  title: 'VariationsOnSum'
next_page:
  url: 
  title: ''
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---

# Basics: Arithmetic, Assignment, and Strings

Topics:
1. Infix arithmetic operators
2. Numeric literals
3. Comparisons
4. Assignments
5. Strings

## Arithmetic should largely be familiar



{:.input_area}
```julia
3 + 7 # addition
```




{:.input_area}
```julia
10 - 3 # subtraction
```




{:.input_area}
```julia
20 * 5 # multiplication
```




{:.input_area}
```julia
100 / 10 # division
```




{:.input_area}
```julia
10 ^ 2 # exponentiation
```




{:.input_area}
```julia
101 % 2 # remainder (modulus)
```




{:.input_area}
```julia
sqrt(2) # square root
```




{:.input_area}
```julia
√2 # Unicode to the rescue: \sqrt + TAB
```


Note that dividing two integers yields a floating point number. There are two additional operators that may be helpful here:



{:.input_area}
```julia
10 / 6
```




{:.input_area}
```julia
10 ÷ 6 # \div TAB or the `div` function
```




{:.input_area}
```julia
div(10, 6)
```




{:.input_area}
```julia
10 // 6
```


### Numbers: Many different ways to write the number forty-two



{:.input_area}
```julia
fortytwos = (42, 42.0, 4.20e1, 4.20f1, 84//2, 0x2a)
```




{:.input_area}
```julia
for x in fortytwos
    show(x)
    println("\tisa $(typeof(x))")
end
```


### Bitwise arithmetic



{:.input_area}
```julia
0x2a & 0x70 # AND
```




{:.input_area}
```julia
0x2a | 0x70 # OR
```




{:.input_area}
```julia
42 & 112
```




{:.input_area}
```julia
0b0010 << 2 # == 0b1000
```


### Logical operators



{:.input_area}
```julia
false && true # AND
```




{:.input_area}
```julia
false || true # OR
```


Note that they "short-circuit!"



{:.input_area}
```julia
x = -42
x > 0 || error("x must be positive")
```


### Comparisons



{:.input_area}
```julia
1 == 1.0 # Equality
```




{:.input_area}
```julia
1 === 1.0 # Programmatically identical
```




{:.input_area}
```julia
3 < π
```




{:.input_area}
```julia
1 <= 1
```




{:.input_area}
```julia
.1 + .2
```




{:.input_area}
```julia
.1 + .2 ≈ .3 # \approx + TAB
```


Comparisons "chain"

Try inserting parentheses around one of these comparisons



{:.input_area}
```julia
2 == 2.0 == 0x02
```




{:.input_area}
```julia
x = 42
0 < x < 100 || error("x must be between 0 and 100")
```


# Assignment

Assignment in Julia is done with the single `=`. All it does is associates a name (on the left) to a value (on the right).



{:.input_area}
```julia
x = 1 # Use the name `x` for the value `1`
```




{:.input_area}
```julia
y = x # Use the name `y` for the value that `x` refers to
```




{:.input_area}
```julia
x = "hello!" # Decide you have a better use for the name `x`
```




{:.input_area}
```julia
y # Is still the value 1
```




{:.input_area}
```julia
ϵ = eps(1.0) # You can make your own unicode names
```




{:.input_area}
```julia
5ϵ # Juxtaposition is multiplication
```


## Updating operators

All the infix arithmetic operators above can be used as "updating" operators in conjunction with an assignment:



{:.input_area}
```julia
y += 1
```




{:.input_area}
```julia
# This is exactly the same as:
y = y + 1
```


Note that it's just re-purposing the _same name_ for a new value. This means that the type might even change:



{:.input_area}
```julia
y /= 2
```


# Strings



{:.input_area}
```julia
s1 = "I am a string."
```




{:.input_area}
```julia
s2 = """I am also a string. """
```




{:.input_area}
```julia
"Here, we get an "error" because it's ambiguous where this string ends "
```




{:.input_area}
```julia
"""Look, Mom, no "errors"!!! """
```




{:.input_area}
```julia
    println("""The other nice thing about triple-quoted
               string literals is that they ignore leading
               indentation, which is nice for long strings
               in real code. Try changing these quotes!""")
```


Strings are not written with single `'`s — that's used for a single character:



{:.input_area}
```julia
first(s1)
```




{:.input_area}
```julia
'⊂'
```




{:.input_area}
```julia
'If you try writing a string in single-quotes, you will get an error'
```


## String interpolation

You can use the dollar sign inside a string to evaluate a Julia expression inside a string — either a single variable or a more complicated expression:



{:.input_area}
```julia
name = "Jane"
num_fingers = 10
num_toes = 10
println("Hello, my name is $name.")
println("I have $num_fingers fingers and $num_toes toes.")
```




{:.input_area}
```julia
 println("That is $(num_fingers + num_toes) digits in all!!")
```




{:.input_area}
```julia
@assert days == 365
@assert days_float == 365.0

```

