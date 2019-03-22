---
redirect_from:
  - "/chapter1/0jupyternotebooks"
interact_link: content/C:\Users\David\jb\jupyter-book\content\chapter1/0JupyterNotebooks.ipynb
kernel_name: julia-1.0
title: 'Jupyter notebooks'
prev_page:
  url: /chapter1/index
  title: '第一篇：基础入门'
next_page:
  url: /chapter1/1Gettingstarted
  title: '开始之前'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---

## Getting started with Jupyter notebooks

### Running a cell
To execute code within a cell, select that cell and either (1) hit `Shift` and `Enter` or (2) hit the run button (the right pointing arrow) above.



{:.input_area}
```julia
1 + 1
2 + 2
```


If you're new to jupyter notebooks, note that only the last line of a cell prints by default when you execute that cell and that you can suppress this output with a semicolon



{:.input_area}
```julia
1 + 1
2 + 2;
```


### How to get docs for Julia functions

To get docs for a function you're not familiar with, precede it with a question mark. (This works at the REPL too!)



{:.input_area}
```julia
?println
```


### How to use shell commands

Type `;` and then you can use shell commands. For example,



{:.input_area}
```julia
;ls
```




{:.input_area}
```julia
;pwd
```


Shell commands also work at the REPL!
