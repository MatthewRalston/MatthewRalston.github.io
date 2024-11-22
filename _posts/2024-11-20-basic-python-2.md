---
author: Matt Ralston
header-image: "/images/dna1.gif"
hero-title: Python basics for the curious
hero-subtitle: Python code fundamentals in a guide that slaps.
category: python
tags: python prose meta
toc: true
---


> Skip the description, let's get to the code!

## Hello world

![Generic_compsci_meme.jpg](/images/computer_science_what_i_actually_do.jpg)

Many programmers know how to code in Python because it has fairly modern syntax, a full object-oriented programming and inheritance stack, web servers, and other modern tooling.

If you want to read more, check out https://python.org or the Wikipedia page on the language to learn more about its history and use cases.


We're going to skip ahead a bit and get to building modern scripts and describe features that python CLI tools should have for you to get ahead of the competition in modern AI and data science related roles.



## Prerequisites

This tutorial assumes you have some basic knowledge of programming and the Linux or MacOS/OSX POSIX shell environments. These skills are fundamental for invoking the Python interpreter on your scripts, CLI tools, server applications, and more. Such skills include invoking programs from bash/fish/zsh/csh shells and terminal evironments, conventions of standard-input/output and piping outputs to sequential commands, decompressing files, redirection of standard output or standard error streams to different files, and a feeling or familiarity concerning easy-to-use tools and how they handle flags, parameters, logging, arguments, etc.

Second, this tutorial assumes some familiarity with the Python build chain, which revolves around PyPI and PEP standards and includes knowledge of the `pip` command-line tool. Specific additional files in your codebase may be required for installation via `conda` (not covered here) and `pip`. Examples of necessary files are `setup.py`, `pyproject.toml`, `requirements.txt`, `Pipfile`, `.python-version`, and `setup.cfg` (usually optional). You may also require conventional plain-text files such as `README.md`, `LICENSE.txt`, and `.gitignore`.

Additionally, many new users might be overwhelmed with the variety of file formats available on Linux, and how using the wrong file as input may result in parsing errors and program crashing. Most files (such as `.fasta` or `.sam` files in bioinformatics) are simple plain-text without compression or encryption. However, due to the file structure, many plain-text categorized files are incompatible with tools that accept plain-text as input. Play around with different formats in your area with inspection via your IDE or editor, or the `cat` and `head` commands to see what the format specification looks like (how the file looks in terms of sequential lines, columns, separators etc.).

Okay! Let's get to the code!




## How do I design a good Python package?

![Tail recursion](/images/cat_tail_recursion.jpg)


First things first, you should plan out your desired command line tool most likely from the top down. For example, you might want to write a tool that has multiple scripts that can be run from a unified environment. e.g.: `mypackage subcommand --input input.txt`

> By planning the interface first, rather than the functions and modules/classes required, it allows the developer to create elegant and easy to use scripts and packages that require less guesswork for the user to use and/or contribute to development.

## Standard input/output conventions

Many tools in MacOS/Linux environments revolve around the conventions of plain-text standard input and output. You may, for ease-of-use and intuitive invocation reasons, decide to accept either a 'named argument' (e.g. `mypackage subcommand --input input.txt`) or a 'positional argument' (e.g. `mypackage subcommand input.txt`) for the primary input, typically data stored in a file, often simple plain-text. 

As it follows, standard output is often preferable for the primary output of text, formats, and information that can be captured with shell stdin/stdout stream redirection. For this reason, it is *helpful* to separate information for the user into stderr stream, and actual program output and file data exclusively to the stdout stream. 

> Because programming is not my area of first knowledge, it took me some time to get the intuition about how to separate logging, program output and statistics, and data output into stdout and stderr streams, such that a valid or parseable table (`.tsv`, `.csv`) is produced separately from necessary information for the user, such as statistics, run-time, and other metadata.


## `--verbose`, `-v`, `-vv` and logging

Another area that requires some design effort is the system of logging what the program is trying to do, at various levels of verbosity. Conventions for logging often include the date/time, the log-level, and the area of code emitting the log statement.

Without good logging, many poorly designed programs may crash or choke on bogus user input without warning or solution, and result in wasted time for the user, poor opinions about the program for the user, and make you seem clueless as a developer.

There isn't a one-size-fits-all solution for log formatting and log inheritance patterns, especially when logging from other modules conflicts with global verbosity settings.


> In other words, develop robust logging habits and sensibility concerning log-level, debug flags, and other stderr oriented habits for developing, debugging, and compartmentalizing your log statements from user-interface text, which may/should also be on the standard error stream, to differentiate it from output data, which may need to be piped from one command to the next.


## Error handling

Another great way for beginners to make their Python packages more robust is to include assertions and type-checking throughout their codebase. If you have a function, the first thing to do is validate the types of the arguments you're passing through. If the developer has the chance to pass through invalid data from the argument or elsewhere in the codebase, your type checking will let you know at least that the functions you care about will not accept invalid inputs.

Strong error messages may look like the following:


```python

def myfunction(a: int, b: str, named:str=None):

    if type(a) is not int:
        raise TypeError("module.myfunction expects an int as its first positional argument")
    elif type(b) is not str:
        raise TypeError("module.myfunction expects a str as its second positional argument")
    elif named is None or type(named) is not str:
        raise TypeError("module.myfunction expects the 'named' keyword argument to be a str")


    # ...

    print("Done")


myfunction(1, 'hello world', named="foo")
```


The first line defines a function named 'main' with the reserved keyword `def`. This `def` keyword is a special Python syntax for defining Python functions. The name of the Python function follows the `def` keyword, followed by parentheses which enclose arguments to the function, their type-hints, and in the case of the keyword argument 'named' assigns a default value of `None`.

In the example, a Python version 3+ syntax called the 'type-hint' is included, but that's beyond the scope of this blog post. In short, the first argument 'a' follows the opening parenthesis, with a colon followed by another keyword 'int'. Note the syntax highlighting differences between `def`, `myfunction`, 'a', and `int`. The function name preceeds the parenthesis in the function definition line. 'a' represents a variable that will be available in the function body, provided by the user in the last line of the example.

The `int` keyword does not do anything. Isn't that weird? It's merely a notation at this point to remind developers what type is expected for the positional argument 'a'. I refer to arguments as positional as their sequential order in the function definition. 'a' should be an integer, a whole number (0,1,2,... etc.). 

'b' on the other hand is a string argument, ASCII or UTF-8 characters enclosed by single `-> '` or double `-> "` quotation marks. 

The last argument is not positional, and is refered to as a keyword argument. Keyword in this context refers to passing the argument by `named="something"` with an equals sign, not to be confused with my earlier reference to reserved keywords in the Python language such as `def`, `int`, and `str`.

> Now that we've seen an example of Python code and we have described the use-case of defining and calling a function, let's move on to a self-contained example that the reader may copy and paste into a file, make the file executable with 'chmod +x myprogram.py', and call the program with 'python3 myprogram.py'.

## How do I write a Python program?


Let's start with some simple code. Consider the following Python script.


```python
#!/bin/env python3


import argparse

def main(args):
    """
    This is *your* main function, and does exactly two things.
    The rest of the code in this example is boilerplate or related to parsing arguments.


    First, the arguments parsed by the built-in argparse module, which ships with all versions of Python,
    are printed to the console by default.

    Second, the string 'hello world' will be printed to the console.

    That's it! Now you're starting to write Python programs!
    """
    print(args)
    print("hello world")



"""
The following routine has some confusing boilerplate, like 'if __name__ == "__main__":'

But don't worry, in a little bit, most of this stuff will make sense.
"""


if __name__ == "__main__":

    parser = argparse.ArgumentParser()

    parser.add_argument("--required", type=str, help="This argument is required and takes a string as input", required=True)

    parser.add_argument("--flag", action="store_true", help="This is a flag argument, which stores a 'True' bool when added")

    args = parser.parse_args()

    # Main routine
    main(args)


```


In the example above, we have two primary parts. The first is the function main, a simple pair of print statements. In this case, we only have one argument: args. This will be an argparse object, again something beyond the scope of this blog post.

When you run the program, you'll see some notation that packages all of the arguments to the script in a unified object for convenience.

The second part is this awkward `if __name__ == "__main__":` thing. Basically, the Python interpreter looks for this notation by default to describe what must be run first, in order to call additional functions and class methods etc. to produce program behaviors. Inside this block of code we have a few statements that allow the argparse module, that is built-in to the Python interpreter's standard library, to define arguments that can be captured by the program and the interpreter to pass arguments through to the user's main function, with its print statements.


## What is a variable?

Variables and constants can be defined in Python to capture `return` values from functions that can be manipulated and passed to other functions, printed, or used otherwise. Check out this simple example:


```python
CONSTANT = "Dont use globals and constants unless you need to. Variables do just fine, most of the time."

myvariable = 8 # int
myvariable = "now its a string" # str
othervariable = 0.4 # float
nothing = None
convert_a_float_to_a_str = str(othervariable)
```

Variables can be any valid Python type, such as `int`, `float`, `str`, `None`, and more.

## What about conditional statements, or the 'if' operator?

At times, you may want to check your variables to decide what to do next. Enter the 'if' statement. You can use 'if' statements to produce branches of code that do different things. If you have the time, continue reading to learn about the use case for `if`, `else`, `elif`, and `match` statements. 


```python

if myvariable == 8:
    print("This should be True, if your 'myvariable' is indeed 4+4.")
elif type(othervariable) is float:
    print("""This should also be True, because there is a decimal in this variable's
    definition, making the number a floating-point number.""")
else:
    print("Something may have gone wrong.")
    raise RuntimeError("Either myvariable's defintion has changed, or othervariable has changed")

match myvariable:
    case 8:
        print("The variable is still 8. Try changing the variable's definition to something else...")
    case 0.8:
        print("Now we have a real valued 'myvariable', not just the original integer")
    case _:
        print("Underscore '_' represents a generic catch-all value, much like the 'else' statement")
        

```


## Use Python's loop functions to do awesome things on lists!


There are two primary functions to do things in sequence or over items of a list. Allow me to briefly introduce one of Python's most interesting built in data types, the `list`.

```python

mylist = ["C. temminckii", "P. marmorata ", "P. marmorata", "L. wiedii", "L. colocola", "L. pardinus", "O. manul", "P. planiceps", "P. rubiginosus ", "P. rubiginosus", "N. diardi", "P. onca", "P. leo", "P. uncia"] # um cats

# No lesson here. This is a list of cats. Be nice to cats.
```


> Not everything has to be a lesson. Sometimes it's just a matter of exploring your interests.

> Python is probably an end goal for some people. For others its the gateway programming language into a world of systems, tools, and funfunfunctions!


```python


for kittycat in mylist:

    kittycat.replace(" ", "+")
    
    learn_about_exotic_and_vulnerable_cats = "https://www.google.com/search?q=" + kittycat

    # What is your favorite kittycat?

    # Are you a cat or dog person?

    # Do you want to hear a bad cat joke?

```

> Just kitten...


In the example above, we can create URLs from the genus and species of some cool cats (Felids) by replacing the space in the strings with a '+' sign to make the URI friendly to Google. By using the `for` keyword and iterating over the list of some Felids, we can learn about cats one at a time for the sake of near threatened or otherwise rare cats that we are kind of blessed to walk the earth with, or some s#it like that.


>Cats would make better congressional leaders than the ones we have right now. I'm pawsitive.



