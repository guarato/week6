~~~ headers
input:          theme.tex
usetheme:       CambridgeUS
usecolortheme:  orchid

title:          [Git - Reminder]
author:         [BA] Benjamin Audren
institute:      [EPFL] \'Ecole Polytechnique F\'ed\'erale de Lausanne
date:           \today
~~~


====================
Git version control 
====================

# Title #

None
-------

``This must be Thursday. I never could get the hang of Thursdays''
{\Grey\it (Arthur Dent, a few minutes before the Earth gets
destroyed)}


# Version Control with Git

## Motivation

Motivation
-----------

    ~~~ block | What is Version Control ?; 80%
    * System that keeps tracks of different {\bf\Green versions} of a
      code (several file), tracking its entire {\bf\Red
      history} of creation.
    * Accessible from a {\bf\Blue central repository}, that stores all
      the versions, and allow communication between developers.
    * Can revert to a previous version to {\bf\Red reproduce} exactly
      the behaviour at a certain time (bug hunting)
    ~~~


Softwares
-----------

    ~~~ block | Version Control Softwares; 60%
    * CVS (Concurrent Versions System)
    * Apache Subversion (SVN)
    * {\only<2>{\Red\bf} Git}
    ~~~

    \vspace{0.5cm}
    \only<2>{ {\it Linus Torvalds}: ``Subversion used to say CVS done
    right: with that slogan there is nowhere you can go. There is no way
    to do cvs right.''}
  

Differences between svn and git
--------------------------------

    ~~~ block | {\Red\bf git} vs {\Green\bf svn}; 70%
    *- remote repositories {\Blue\bf both}
    *- merging capabilities {\Blue\bf both}
    *- ok, good merging capabilities {\Red\bf git}
    *- local repository is an entire copy {\Red\bf git}
    *- offline work ! {\Red\bf git}
    *- pull-request system (user subtmitted patch) {\Red\bf git}
    ~~~


Worflow
-----------
{\bf Basic}, master branch only

    ~~~ block | Into an existing or newly created directory; 60%
    *- \verb?git init?
    *- \verb?$EDITOR file.py?
    *- \verb?git status?
    *- \verb?git add file.py?
    *- \verb?git commit -m 'file added'?
    ~~~


Reminder: Staging Area
-----------------------

    ~~~ block | After modifying; 70%
    *- Local version is affected: {\bf Working Tree}
    *- {\Red\bf add} files to the index (staging area)
    *- {\Green\bf commit them} to the repository
    ~~~

    ~~~ alertblock | Beware; 60%, <4->
    *- You can easily {\Red\bf un-add} files from the staging area
    *- You can easily {\Green\bf un-commit} files once commited ({\bf
    amend, rebase})...
    *- But you should probably {\Blue\bf avoid} doing it...
    *- Except {\Red\bf locally only}
    ~~~



Important other things
-----------------------
Configuration

    ~~~ block | Important files to be present; 70%
    * a \verb?.gitignore?
    * a \verb?README.md? or any other markup language
    ~~~

    \vspace{1cm}

    The \verb?git.config? file should contain at minima:
~~~ verbatim
[user]
  name = First Last
  email = first.last@somewhere.com
~~~

Important other things
-----------------------
More basic commands

    ~~~ block | See the history; 50%, <1->
    with \verb?git log?
    ~~~

    ~~~ alertblock | Recover previous version of a file; 50%, <2->
    with \verb?git checkout file.py?
    ~~~

    ~~~ exampleblock | Unstage a file for commit; 50%, <3>
    with \verb?git reset HEAD file.py?
    ~~~

Hands-on
---------
go ahead !

    ~~~ block | Exercise; 60%
    Go to last week directory where you created a {\bf very simple
    module}, and turn it into a git repository.
    ~~~

    ~~~ alertblock | Do some work; 60%, <2>
    Make some changes, commit, try to see the history
    ~~~

