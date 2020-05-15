---
layout: default
title: About
permalink: /cheatsheets/
---

## A list of links and references that I find interesting or useful.
This is just my personal reference for things that I might use or find interesting
for the future.

## Jekyll
  - [Jekyll Categories](https://blog.webjeda.com/jekyll-categories/)

## JavaScript / Clasp
  - [Clasp - youtube](https://www.youtube.com/watch?v=V_7kvwcZf_c)

## Python

### Guides:
  - [Excel Spreadsheet](https://www.marsja.se/your-guide-to-reading-excel-xlsx-files-in-python/?amp)

### Code Snipets:
  - Padding Numbers
    ```py
    >>> n = 4
    >>> print(f'{n:03}') # Preferred method, python >= 3.6
    004
    >>> print('%03d' % n)
    004
    >>> print(format(n, '03')) # python >= 2.6
    004
    >>> print('{0:03d}'.format(n))  # python >= 2.6 + python 3
    004
    >>> print('{foo:03d}'.format(foo=n))  # python >= 2.6 + python 3
    004
    >>> print('{:03d}'.format(n))  # python >= 2.7 + python3
    004
    ```
      Reference: [Stack Overflow](https://stackoverflow.com/questions/339007/how-to-pad-zeroes-to-a-string)
### Modules
  - [Pendulm](https://pendulum.eustace.io)
    An alternative to the datetime module
  - [pyfakefs](https://pypi.org/project/pyfakefs/)
    Mock your file system calls.
  - [inflect](https://pypi.org/project/inflect/)
    automatically plurual words
