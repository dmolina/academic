+++
title = "Learning new languages?"
date = 2012-07-04
lastmod = 2017-10-10T17:57:39+02:00
categories = ["programming"]
draft = false
+++

I love to learn new programming languages, specially whose that has new features that could be used to change your personal
programming way. Also, it is very useful to get used to accept new ideas and avoid get in in the famous _language wars_.
In this post, I'm going to give my personal idea of these languages, starting from a C/C++ and Java
programmer. Over all, this is my personal opinion, after hours of working in these languages, not only using a
joy program.


## Perl {#perl}

It was my first _scripting language_, and I've been working in Perl in a proyect for a private company for two years
eight hours per day (my first job without extra hours without been paid). In that case, it was a good language decision,
and I learnt many tricks to write readable programs in **Perl**.

-   <span class="underline">community</span>:
    A community that likes to create an ecosystem to reuse, that create the [CPAN](http://www.cpan.org). At the same time, a
    community that enforces freedom, allowing each one to use the library and guidelines that considers good.

-   <span class="underline">The good:</span>
    The [CPAN](http://www.cpan.org), and the conciseness and flexbility of the language, with packages like [Moose](http://search.cpan.org/search?q%3DMoose) and several test packages
    (and very strange packages in _ACME_ domain :-) ). At the same time, there is always simpler version of packages if
    you want them.

-   <span class="underline">The bad:</span>
    The original Object-Oriented, the complexity in creating your own modules (in comparisons to the simpler
    packages model like python). Also, if you don't want to use object-oriented, sometimes you need to create complex
    combinations of _hashes_ and _arrays_ with references, and it is not very readable.

-   <span class="underline">Developer tools</span>: I usually edit with [Vim](http://www.vim.org), I don't need any particular framework, but I strongly recommend strict
    mode, and essential packages like [autodie](http://search.cpan.org/search?q%3Dautodie), [Moose](http://search.cpan.org/search?q%3DMoose), [<:IO>](http://search.cpan.org/search?q%3DFile::IO), test packages like [Test::More](http://search.cpan.org/search?q%3DTest::More). Always check [CPAN](http://www.cpan.org) before a new
    proyect.

I resume, although many people say that Perl is dead, it is still alive, and if you learn it, you don't regret it, it is
a very useful tool. I still makes many small programs almost everyday using Perl because it's a very useful language,
mainly for text processing (probably the best one).

To learn more I recommend the free book [Higher-Order Perl](http://hop.perl.plover.com/), it is a opening book. Also, the freely book [Modern Perl](http://www.modernperlbooks.com) is a
useful book to see new modern programming ways and wonderful packages.


## Python {#python}

My first love, a very simple but more readable, and very useful tools for any field. The most beautiful syntax in my
opinion. I have been deeply working in Python, for prototyping and several complex project.  Also, very good in web
developer (my favourite is [Django](http://www.djangoproject.com) but there are many good ones).

-   <span class="underline">The good:</span> Its syntax, packages and object models. Also, its libraries have tendency to have simple APIs (by a
    community very worried about that). The great interactive shell [ipython](http://ipython.org). Also, it have many interesting tools for
    scientific researchers: [numpy](http://numpy.scipy.org/), [matplotlib](http://matplotlib.sourceforge.net/), several parallel libraries, [scipy](http://www.scipy.org/).

-   <span class="underline">The bad:</span> nothing really serious, the inherent problems with duck typing, like excessive trivial testing. However,
    tools like [pyflakes](http://pypi.python.org/pypi/pyflakes/) or [pylint](http://pypi.python.org/pypi/pylint/) allow developers reduce trivial errors.

-   <span class="underline">Developer tools:</span> Sometimes I edit with [Vim](http://www.vim.org), but nowadays I uses [spyder 2](http://code.google.com/p/spyderlib/) by its integration with  [pyflakes](http://pypi.python.org/pypi/pyflakes/) and
    [ipython](http://ipython.org). There are also very good IDEs like [eric4](http://eric-ide.python-projects.org/). For performance aspects, there are many tools, in a future
    post, I am going to put a real example of improvement.

I resume, it is a very good language that any developer should now, because it is very simple and useful. Specially for
scientific works, not only by the mathematical tool [Sage](http://www.sagemath.org/) but also by many libraries.


## Scala {#scala}

The most recent adquisition to this list is the [Scala language](http://www.scala-lang.org/). This **JVM language** is similar to [Groovy](http://groovy.codehaus.org/) but in my
opinion, superior.  However, it is a very good language but I think that it is not very popular in pragmatic programmer
by the scientific origin of its author, clearly seen in its documentation. Also, sometimes the _converse_ developers
likes to show how flexible and powerful is the language with complex examples (not in length, but in its syntax) have
given the idea of a complex language.

-   <span class="underline">The good:</span> Its syntax is very orthogonal and simple (reducing the verbosity of Java). It is a strong typing system
    (different with **groovy**) with a auto-detection of types (like auto keywords in other languages). It enforces to uses
    immutable classes and method, allowing you a functional programming.

-   <span class="underline">The bad:</span> Differences in generical contenedors with Java. There are very powerful but you have to converse from one
    to another.

-   <span class="underline">Developer tools:</span> like in Java, I recommed [Eclipse](http://www.eclipse.org) with [scala plugins](http://scala-ide.org/). For compiling proyects in both
    languages you can use [maven](http://maven.apache.org/) but you need several plugins (only if you combine them). Another compiling tools like
    [sbt](https://github.com/harrah/xsbt/wiki/) or [grandle](http://gradle.org/) could be useful.

In resume, a very interesting language that java developer should give a look, but it still have a promising future.

In my opinion, its community should 'break' the idea of complexity or it going to be a very niching language while groovy would
be stronger and widely used.


## In resume {#in-resume}

I always recommend to learn new languages. You can learn many possibilites: clojure, immutability, libraries, ... that are not
so visible in your current main language.

PS: I have let out other languages that I've been playing in: R, Ruby, Haskell, groovy, F# because I want to write only about languages
in which I have a strong knowledge, and used it in real-word projects (and not only joy projects).
