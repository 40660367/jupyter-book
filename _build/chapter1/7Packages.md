---
redirect_from:
  - "/chapter1/7packages"
interact_link: content/C:\Users\David\julia\jupyter-book\jupyter-book\content\chapter1/7Packages.ipynb
kernel_name: julia-1.0
title: '包'
prev_page:
  url: /chapter1/6Functions
  title: '函数'
next_page:
  url: /chapter1/8Plotting
  title: '绘图'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---

# Packages

Julia has over 2000 registered packages, making packages a huge part of the Julia ecosystem.

Even so, the package ecosystem still has some growing to do. Notably, we have first class function calls  to other languages, providing excellent foreign function interfaces. We can easily call into python or R, for example, with `PyCall` or `Rcall`.

This means that you don't have to wait until the Julia ecosystem is fully mature, and that moving to Julia doesn't mean you have to give up your favorite package/library from another language! 

To see all available packages, check out

https://pkg.julialang.org/
or
https://juliaobserver.com/

For now, let's learn how to use a package.

The first time you use a package on a given Julia installation, you need to use the package manager to explicitly add it:



{:.input_area}
```julia
using Pkg
Pkg.add("Example")
```


Every time you use Julia (start a new session at the REPL, or open a notebook for the first time, for example), you load the package with the `using` keyword



{:.input_area}
```julia
using Example
```


In the source code of `Example.jl` at
https://github.com/JuliaLang/Example.jl/blob/master/src/Example.jl
we see the following function declared

```
hello(who::String) = "Hello, $who"
```

Having loaded `Example`, we should now be able to call `hello`



{:.input_area}
```julia
hello("it's me. I was wondering if after all these years you'd like to meet.")
```


Now let's play with the Colors package



{:.input_area}
```julia
Pkg.add("Colors")
```




{:.input_area}
```julia
using Colors
```


Let's create a palette of 100 different colors



{:.input_area}
```julia
palette = distinguishable_colors(100)
```


and then we can create a randomly checkered matrix using the `rand` command



{:.input_area}
```julia
rand(palette, 3, 3)
```


In the next notebook, we'll use a new package to plot datasets.

### Exercises

#### 7.1
Load the Primes package (source code at https://github.com/JuliaMath/Primes.jl ).



{:.input_area}
```julia
@assert @isdefined Primes
```


#### 7.2
Verify that you can now use the function `primes` to grab all prime numbers under 1,000,000 and store it in variable `primes_list`



{:.input_area}
```julia
@assert primes_list == primes(1000000)
```


Please click on `Validate` on the top, once you are done with the exercises.
