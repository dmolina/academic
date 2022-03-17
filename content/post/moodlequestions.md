+++
title = "My first Julia Package"
author = ["Daniel Molina"]
date = 2020-03-27T23:54:00+01:00
lastmod = 2020-03-27T23:58:01+01:00
tags = ["teaching", "julia"]
categories = ["teaching", "programming"]
draft = false
+++

For online teaching I use Moodle. I have a lot of experience using it (for more
than 10 years). Unfortunately, the software could be improved a lot. My main
complains are:

-   You can import the grades using an Excel file. However, you cannot import the
    comments.  I like to give comment to explain the reason of the qualifications.

-   The Quiz is potent, but the creation of questions is very slow. Also, in my
    University several teachers have historically used another software. However,
    Moodle is unable to import these questions (in a different XML format).

In order to solve the second one, and in conjunction with my interest in Julia,
I have created a package: [MoodleQuestions](https://github.com/dmolina/MoodleQuestions.jl). Not only it is able to export from
the previous software, but it is also able to create the questions in a
MoodleXML from a more intuitive file, in text file:


## Input text file format {#input-text-file-format}

This package is able to read a text file. The format has been designed to be as simple and readable as possible.

```text
 * Category 1

Question 1

- Option 1.1.
- Option 1.2.
+ Option 1.3.

 * Category 2

Question 2

+ Option 2.1.
- Option 2.2.
```

The sentences starting with \* is a new category, with the name.

The sentences without \*, +, or - are the text of the question. It is expected to
be from only one line.

The sentences starting with - or + and the different answers for the previous
question. The - means that the answer is false, and the + means that the
sentence is the right answer.

The answers in the question are shuffle, except when one of the word of A, B,
... is used. In these cases, the order of the options is maintained.

In my opinion, to create a text file with the questions in that format is a lot
easier than using the web interface of Moodle.


## My experience creating a package {#my-experience-creating-a-package}

I have experience creating a PyPI package in Python, and I only can say that
creating a Julia package is a lot easier.

1.  First, there are packages like [PkgTemplates](https://github.com/invenia/PkgTemplates.jl) that create all the structure of
    the code.

2.  Because in Julia you can add a non-official package adding the github url,
    you can use the package working (and share it) without have to register it.

3.  The tests can be tested very easily with [Tracis CI](https://travis-ci.com/dmolina/MoodleQuestions.jl), for different Julia
    version and Operative System (it detected an error only in Windows). However,
    because Julia is not officially supported and the Sandbox implies to install
    all required packages for each time, the time in the test implies a lot of
    time, more than 1m30 in several versions. At least, it gives the tranquility
    of working in different julia versions.

4.  The documentation can be done very easily with [Documenter.jl](https://github.com/JuliaDocs/Documenter.jl), and it publish
    in Github Pages (the only problem was to define the DOCUMENTER\_KEY
    environment variable, but the error was clear).

5.  The Registration is was very simple. Originally, you had to do a Pull Request
    to the <https://github.com/JuliaRegistries/General> repository. However,
    nowadays you should use <https://github.com/JuliaRegistries/Registrator.jl>,
    that with a simple web interface it will do the PR for you (only the URL is
    required).

To summarise, the experience has been very positive. In my opinion, you are a
lot more lost than in Python when you have to create your first setup.py, and it
is easier to follow the good practices of Continous Integration with tests and
Documentation. Also, there is a great presentation at
<https://www.youtube.com/watch?v=QVmU29rCjaA>.
