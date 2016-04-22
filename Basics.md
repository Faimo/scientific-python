What is Markdown?
=================

My lecture notes will be formated in markdown. Markdown is a minimal, plain text document syntax. Markdown formatted documents are structured using plain text and can be used as such, but it is possible to convert them to other formats. If you need a pdf or html page, you can use [pandoc](http://pandoc.org/). Find the syntax specified here:

    https://daringfireball.net/projects/markdown/

How to install things...
========================
 - Not covered here. You should know this already.

How to open a Terminal
======================

We will be using the terminal a lot. The terminal is an "expert interface" to your computer.

 - Mac
    - COMMAND + SPACE (opens Spolight)
    - "Terminal"
    - Done

 - Windows
    - Win + R
    - "cmd"
    - Done

 - Linux
    - You already have one open, don't you?

Get familiar with your terminal. Basic commands include changing directories, and interacting with files. When I refer to the terminal in my script, I indicate a block of code, starting with a dollar sign. This is just a convention, meaning: do this non your terminal. In Windows, the prompt looks different:

    [johannes@perth ~]$ cat file.txt

Would be

    C:\Users\Johannes\> type file.txt

I will abbreviate both with the Dollar.

    $ command

Tutorial: [http://cli.learncodethehardway.org/book/](http://cli.learncodethehardway.org/book/)

As soon as you have opened your terminal, you can run Python:

    $ python

This will output something like this:

    Python 3.5.1 (default, Mar  3 2016, 09:29:07)
    [GCC 5.3.0] on linux
    Type "help", "copyright", "credits" or "license" for more information.
    >>>

Make sure you are running Python 3.5. The ```>>> ``` indicates that python is now waiting for your input. Your are in the so called "REPL" - this is the READ - EXECUTE - PRINT - Loop. It reads in commands and outputs (prints) their results immediately. This is great for trying out python syntax.

If typing ```$ python``` didn't do anything, you may need to setup your terminal to find the python command, you need to follow these instructions:

https://docs.python.org/3.5/using/windows.html#configuring-python

You can also ask me, I will help you to get started.


What's on the keyboard
======================

The keyboard is your main interface to your computer. I find it surprising that many people don't know where some symbols are, even if they spend significant amounts of their lifetime in front of a keyboard. Here are some special synonyms. Make yourself familiar with where they are on your keyboard.

    - Bindestrich, Dash, Hyphen
    _ Underscore, Unterstrich
    : Doppelpunkt, Colon,
    . Punkt, Dot, Stop, Point
    , Komma
    ()Klammer, Braces, Parentheses
    []Eckige Klammer, Brackets
    {}Schweifklammer, Curly Braces
    <>Winkelklammer, Angle Bracket, Kleiner Als, Größer als
    / Forward Slash
    \ Backward Slash
    | Pipe
    ~ Tilde
    ^ Caret, Accent Circonflexe
    % Percent
    $ Dollar
    @ At, Klammeraffe
    # Hash, Pound, Number, Doppelkreuz
    ! Ausrufezeichen, Bang
    = Istgleich, Equals
    ' Quote
    " Douple Quote
    & Ampersand, Kaufmannsund

    CTRL        Control, Steuerung, STRG
    ALT         Alternative
    SHIFT       Großmachtaste, Pfeil nach oben
    CAPS        Über dem Pfeil nach oben
    Command     ⌘, Apple Only
    Windows     Most underrated Key

Additionally, there are some invisible characters. You know SPACE " ", but in Python you should be aware of "\t". Printing this sequence (backslash t) means the TABULATOR key, which is located left of the Q key. In modern text editors, it is used to indent your code. The Enter key is often abbreviated with "\n", which is short for 'New Line'.

I recommend that you>

 - Get familiar with OS shortcuts. Using the mouse is really slow. Leaving the keyboard slows you down.
 - When typing, make use of the "Jumping" Commands.
 - CTRL + Left / Right allows to jump whole words
 - On a normal computer you have HOME, END and PAGE UP / PAGE DOWN keys.

Mac Keyboards
-------------

On Macs you can use:
    - FN + CTRL + LEFT    = Home (Beginning of Row)
    - FN + CTRL + RIGHT   = End (...of Row)
    - FN + Up Arrow       = PAGE UP
    - FN + Down Arrow     = PAGE DOWN

 - Curly:    { }  = ALT + ( / )
 - Brackets: [ ]  = ALT + SHIFT + ( / )

Pro Tip: Learn the shortcut to switch language layouts (Alt Shift / Windows Space under Windows). The special characters needed for programming are much easier to access on the English keyboard, as they have no use for Umlauts.


Choosing an Editor
==================

The choice of editor doesn't matter. Pick one you like. One will feel "right". I encourage you to try out others. If you have been using Notepad++, try Atom for this lecture. Maybe you will like it, or it may teach you why you where right to begin with.

 - [Notepad++](https://notepad-plus-plus.org/)
 - [Sublime Text 3](https://www.sublimetext.com/3)
 - [Atom](https://atom.io/)
 - [PyCharm](https://www.jetbrains.com/pycharm/) - Not recommended, yet
 - [Vim](http://www.vim.org/), see [http://vimcasts.org/](http://vimcasts.org/) - Powerful, useful to know, but very, VERY step learning curve. Not recommended, especially if there are characters on the keyboard that you don't know.
 - Jupyter Notebook - Something different, we'll see later.

 - Please do not use:
    - notepad
    - wordpad
    - Word
 - Please do use:
    - Monospaced Fonts
    - An Editor with Syntax Highlighting
    - An Editor with Auto Completion

 - Please setup your editor to indent using spaces.

Git
===

Make yourself familiar with git. Git is a practical tool that every software developer should know. Git can be really complicated but is really worth learning about, since you can use it to share and distribute code and other files, track changes and get organized. You can use it even if you lose interest in python, as you can easily track LaTeX Document and other files with it.

To use git, you need a couple of commands. You enter directory and then start a "Repository".

    $ git init

This creates a little data on the side. Git remembers, what state your data is in. This state gets assigned a number. If you break something, for example you fuck up your code or accidentally delete some file, you can ask git to recreate it.

Let's try it out. Go to a directory and do the above ```git init```. Then, create a file:

    $ echo 'Hello' > file.txt

Then, ask git something:

    $ git status

Git status will mention, that it doesn't know the file. This change - the fact that you created a new file - has to be announced to git. Use this:

    $ git add -A .

Doing status again will show you that git understood that you would like to consider this change, when you save the state of your work.

    $ git commit -m "I added a file"

Doing a commit means that you want to store this chunk of work. You also provide a message. Here you should state why did what you did.



I recommend using git from the commandline, but there are visual tools available.

 - [Git Guis](https://git-scm.com/download/gui/linux)
 - [SourceTree][https://www.sourcetreeapp.com/] is really good.

I will distribute my lecture notes with git. To get started, you can call:

    $ git clone https://github.com/cessor/scientific-python.git

If something changes, use this:

    $ git pull origin master

This will pull the latest copy of the lecture notes from the server.

Python
======
Now for some python...


Picking the right version
-------------------------

Python is a programming language, but there is more to the story and some terms might be confusing.

Python itself is a language. There are two main versions, 2.7 and 3.5. They differ in many ways. I recommend that you use python 3.5.

When you download python, you get an interpreter. This interpreter is a program that executes your code in a certain way. There are many interpreters, and they differ in the way they execute the code. Some are faster, some are slower, and there are other reasons why different interpreters exist. For our purposes, the normal, default interpreter, called CPython is fine.


Python comes with pip
---------------------

Python itself is just a language. It can't do much, unless you tell it to. With just the language you can't zip files or download stuff. Therefore the default install comes packed with a basic library, which already contains tons of stuff. Take a look at [The Python Standard Library](https://docs.python.org/3.5/library/index.html). Like this, python follows a "Batteries included" approach.

There are, however, many things you want to do, that you can't do with a python off the shelf. If you would like to convert a markdown file with python, you need a translation tool. This tool can be installed with pip. Pip is short for "Pip installs packages", see [recursive acronym](https://en.wikipedia.org/wiki/Recursive_acronym).

There are cases where pip can't install your packages. Either you install build tools to remove the problem, or you try to find prepackaged binaries. Under Windows, you can download .wheel distributed packages and install them with pip:

    http://www.lfd.uci.edu/~gohlke/pythonlibs/

If you have trouble with this approach, you can use the anaconda distribution. I never used it myself, but I hear it is quite simple to use.

    https://www.continuum.io/downloads

Basic Python
------------

    >>> 1 + 1

    >>> def function():
    ...     print('hello')

In the first session we saw some very basic stuff. We discussed how there is syntax and semantics. Synax means, for example, that I have to close every opening brace.

Semantics are about what the language understands that I want.

    'Hello' + ', World'

Are meaningful. Adding two strings results in a new, concatenated string.

    'Hello' - 'Hello'

on the other hand has no intuitive meaning and will result in a semantic error. Semantics are the exciting part of a programming language. Syntax is usually quite easy, but we'll have to discuss it first.

Syntax
------

How is syntax defined? A language's syntax is described by the rules that the interpreter uses to make sense of the code you wrote. In Python, these rules are defined in an explicit grammar file:

    https://docs.python.org/2/reference/grammar.html

In this file, you find statemens like the following:

    funcdef:        'def' NAME parameters ':' suite
    parameters:     '(' [typedargslist] ')'
    typedargslist:  tfpdef (',' tfpdef)*
    tfpdef:         NAME
    suite:          simple_stmt | NEWLINE INDENT stmt+ DEDENT
    simple_stmt:    small_stmt (';' small_stmt)* [';'] NEWLINE
    NAME:           identifier
    identifier:     (letter|"_")(letter | digit | "_")*
    letter:         lowercase | uppercase
    lowercase:      "a"..."z"
    uppercase:      "A"..."Z"
    digit:          "0"..."9"

This grammar file defines the rules how to build a function-definition. The NAME part is the most interesting one. In Python, as defined by this rule, function names are identifiers, and those can start with an underscore or a letter. You can then type digits, but the function's name can't start with it.

This shows that ```def``` and the colon at the end are quite mandatory, but most other parts can be defined freely. You will have to think up a name.

In the following sessions, we will see why these things (functions) are relevant and what you can do with them.

Keywords
--------

    >>> import keyword
    >>> keyword.kwlist

Next Step: Builtins
https://docs.python.org/3.5/library/functions.html