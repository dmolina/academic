+++
title = "Packages in Python for CEC'2019 100 Digit Competition"
author = ["Daniel Molina"]
date = 2018-12-14T12:11:00+01:00
lastmod = 2018-12-14T12:21:28+01:00
tags = ["computer_science", "python"]
categories = ["computer-science"]
draft = false
+++

I usually design my evolutionary algorithms in Python (initially for
prototyping, but I am too lazy for doing later a version in C/C++ or similar).
However, unfortunately, the majority of people in my area work in Matlab :sob:.
Thus, sometimes I have to wrap the source code for the benchmarks in competition
to python :relaxed:.

This is the story of the my new package at PyPi:
<https://pypi.org/project/cec2019comp100digit/>.

This package is for being able to participate in the [CEC'2019 100-Digit Challenge
Competition](http://cec2019.org/programs/competitions.html#cec-06), website here:
<http://www.ntu.edu.sg/home/epnsugan/index%5Ffiles/CEC2019/CEC2019.htm>.
That website was the source code in C/C++ and Matlab (using mex), but it was
missing Python. This package solves it.

As usual, the complete source code is [available at Github](https://github.com/dmolina/cec2019comp100digit).

In the package Pypi page there is [more documentation](https://pypi.org/project/cec2019comp100digit/), but in the following I
briefly describe the API:

The package is very simple to use. There is a package cec2019comp100digit with
three functions:

-   **init(fun\_id, Dim)**
    Init the function for the dimension selected.

-   **eval(sol)**
    Eval the solution, when sol is a numpy (or array) of dimension **Dim**.

-   **end()**
    Free resources.


## Installation {#installation}

It as simple as:

```sh
pip install cec2019comp100digit
```

Requirements:

-   Python3.
-   Numpy.
-   Cython.


## Process {#process}

-   For init the function.

    ```python
    from cec2019comp100digit import cec2019comp100digit
    bench = cec2019comp100digit
    bench.init(3, 10) # Init function 3 with dimension 10
    ```

-   To create one or several solutions to eval

    It can be used both numpy and/or array (but only numpy has been actually
    tested).

    ```python
    import numpy as np
    sol = np.random.rand(10)
    ```

-   Evaluate the solution

    It is as simple as:

    ```python
    fit = bench.eval(sol)
    ```

-   Finally, for free the resources

    ```python
    bench.end()
    ```

You can also use it for participate in the competition.

I would like to take this opportunity to remind you that I too am organising
[another competition](https://dmolina.github.io/en/post/lsgo%5Fcec2019/), you do not any excuse :smile:.
