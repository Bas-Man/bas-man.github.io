---
layout: default
title: Code Snipets
permalink: /codesnipets/
---

These are some of my favourite code snipets. 

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
