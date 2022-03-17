+++
title = "My Julia journey"
author = ["Daniel Molina Cabrera"]
date = 2020-08-21T22:08:00+02:00
lastmod = 2020-08-21T22:14:44+02:00
tags = ["teaching", "julia"]
categories = ["teaching", "programming"]
draft = false
+++

In this post I am going to tell my Julia journey.

I have read about Julia but not actually use it before version 0.7 just before
1.0. I work on Machine Learning and stochastic optimization (with evolutionary
computation). In Machine Learning (and Deep Learning) I work nicely with Python
(Scikit-learn and Keras/PyTorch). However, in optimization I usually did
prototype in Python, and later have to translate to C++ for performance (well,
not while the function evaluation takes too much). Now I starting using Julia
for these algorithms (I prefer it a lot against Numpy). For ML I am actually
testing options with Julia
([MLJ.jl](<https://github.com/alan-turing-institute/MLJ.jl>) and
[Flux](<https://github.com/FluxML/Flux.jl>) mainly).

My main problem is the lack of examples/tutorials in the documentation for
several packages. Also, some missing functionality. I am going to explain it
with an example. I did a small website in Julia to receive a file and transform
it (for learning, I have experience in other technologies like Python/JS, ..)
<http://pradofacil.danimolina.net/>. I did it using Frankling have to create my
own website, it was nice. The server side I have two problems:

-   HTTP.jl is simple but not very complete, I have to create my own function to
    extract the POST parameters.

-   I wanted to have error messages in two different languages (English and
    Spanish), but the Gettext package did required Python, and I do not want to
    install it in the server only for that. So, I create my own package
    [SimpleTranslation.jl](<https://github.com/dmolina/SimpleTranslations.jl>) to
    translate easy messages in a simple way.

Usually I create scripts, but in Julia the time required to load the packages
make them slower than similar to Python. In order to reduce that problem I
recently created [DaemonMode.jl](<https://github.com/dmolina/DaemonMode.jl>)
package, that got a great interest (even it was mentioned in JuliaCon 2020!).

The good and bad:

-   good: How easily is to create packages, and register it. The syntax, and many
    great packages: DataFrames, Plots, ...

-   bad: documentation of several packages. There is the API, but learning to use
    them usually implies several tests.

To summarise, it is a great language. When you use it, sometimes to affort small
problems due to a not too mature ecosystem, but the evolution is clearly to
best. For sure I will use it!
