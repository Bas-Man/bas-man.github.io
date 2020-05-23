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
  - [Schedule Posts in Jekyll](https://alxmjo.com/2017/05/30/how-to-schedule-posts-with-jekyll/)
  - [Deprecating a Package](https://www.dampfkraft.com/code/how-to-deprecate-a-pypi-package.html) Reference: [Pycoder's Weekly](https://pycoders.com/issues/421)
  - [Untangling Decorators](https://rednafi.github.io/digressions/python/2020/05/13/python-decorators.html)
  - [Google Script](https://medium.com/@jsarafajr/google-apps-script-without-pain-or-success-story-of-atlassian-cloud-for-gmail-6cd99ba40de0)
### Sphinx
    - [Don't be afraid to commit](https://dont-be-afraid-to-commit.readthedocs.io/en/latest/prerequisites.html)
    - [Getting started with Sphinx](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html)
### LaTeX
    - [Writing Japanese with LaTeX Part 1](https://www.preining.info/blog/2014/12/writing-japanese-in-latex-part-1-introduction/)
    - [Writing Japese with LaTex Part 2](https://www.preining.info/blog/2014/12/writing-japanese-in-latex-part-2-characters-and-encodings/)
    - [Writing Japanese with LaTeX Part 3](https://www.preining.info/blog/2014/12/writing-japanese-in-latex-part-3-simple-documents/)

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

  - Mock Python Version for testing.
    {% gist bd3425dd09585398da7e7970f62b67e7 %}

### Modules
This is a list of modules that I am interested in using.
  - [Pendulm](https://pendulum.eustace.io)
    An alternative to the datetime module
  - [pyfakefs](https://pypi.org/project/pyfakefs/)
    Mock your file system calls.
  - [inflect](https://pypi.org/project/inflect/)
    Automatically plurualise words
  - [Deprecated](https://pypi.org/project/Deprecated/)
    Deprecate code in Python.
