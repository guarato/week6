~~~ headers
input:          theme.tex
usetheme:       CambridgeUS
usecolortheme:  orchid

title:          [Sphinx - First look]
author:         [BA] Benjamin Audren
institute:      [EPFL] \'Ecole Polytechnique F\'ed\'erale de Lausanne
date:           \today
~~~


===============================
A brief introduction to Sphinx
===============================

# Title #


Why writing doc is important
-----------------------------
again...

    ~~~ block | Some reasons; 82%
    *- A code is {\Red\bf read more than it is written}
    *- Time-saver when {\Green\bf expanding} your code (need good IDE)
    *- {\Blue\bf Essential} when sharing with others
    ~~~
    
    \vspace{1cm}
    \only<4>{See uses with the ipython notebook} 


Docstring convention
---------------------
Reminder

    ~~~ block | How to write docstrings; 80%
    *- Text within {\Red\bf triple back-quotes}:
    \pythoninline{"""something"""}
    *- Write {\Green\bf below} statements
    *- {\Blue\bf First line} must contain {\Blue\bf short summary}, followed by blanck line
    *- Then, paragraph of text, and description of arguments, with
    possibly type, etc...
    *- Enjoy using \verb?pydoc -g?
    *- more on PEP 257 \url{http://www.python.org/dev/peps/pep-0257/}
    *- even more on {\Red\bf Google style-guide}
    ~~~


How can it become awesomer ?
----------------------------

    ~~~ block | Sphinx !; 62%
    An {\Red\bf automated documentation generator} !\\ It reads your
    code, build a website/pdf/what you want !\\
    \url{http://sphinx-doc.org/}
    ~~~


Sphinx by example
------------------
likelihood class.py I

    \pythonstyle
    \lstset{basicstyle=\ttfamily\scriptsize}
    \lstinputlisting[linerange={1-14}]{code/likelihood_class.py}
    ...
    

Sphinx by example
------------------
likelihood class.py II

    \pythonstyle
    \lstset{basicstyle=\ttfamily\tiny}
    \lstinputlisting[linerange={21-40}]{code/likelihood_class.py}
    ...


Sphinx by example
------------------
mcmc I

    \pythonstyle
    \lstset{basicstyle=\ttfamily\tiny}
    \lstinputlisting[linerange={1-26}]{code/mcmc.py}
    ...


How does this render ?
----------------------

    go to
    \url{http://baudren.web.cern.ch/baudren/build/likelihood_class.html}
    and 
    \url{http://baudren.web.cern.ch/baudren/build/mcmc.html}


What is this new devilry ?
---------------------------
Source code for the html files
\scriptsize

    \begin{columns}
    \column{0.45\textwidth}

mcmc.rst:

    ~~~ verbatim
    Mcmc module
    ===========

    .. automodule:: mcmc
        :members:
        :undoc-members:
        :show-inheritance:
    ~~~

    \column{0.45\textwidth}

analyze.rst:

    ~~~ verbatim
    Likelihood class module
    =======================

    .. automodule:: likelihood_class
        :members:
        :undoc-members:
        :show-inheritance:
    ~~~

    \end{columns}
