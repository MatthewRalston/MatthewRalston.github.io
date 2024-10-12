---
author: Matt Ralston
header-image: "/images/dna3.gif"
hero-title: GNUish producitvity setup (Part 1.)
hero-subtitle: Ubuntu flavor + Python3, pipenv, emacs, org-mode, org-roam, org-roam-ui, Rstudio, pandoc
category: Coding
tags: python system meta
---


# Ubuntu-based Linux System

Personally, I use pop!_os 24.04 LTS, and I use a variety of programs in my daily productivity stack. To start, let's review our Python coding environment.


# Python

The first step for a Python+R productivity setup using FOSS and GNU centered C toolchains, involves installing Python from source, and using pipenv (and/or pyenv) to mediate Python virtualenv management.

Pyenv is an optional, 3rd-party dependency that pipenv recognizes to install Python locally to user home directory. `https://github.com/pyenv/pyenv` and `https://github.com/pyenv/pyenv-virtualenv` did the trick for me.

## `pipenv`

Pipenv allows the generation of project specfic virtual environments, and creates independent shells with all Pythonpath and other variables set accordingly.

Moreover, pipenv is PyPA/PyPI. 

```bash
pipenv --python 3.12.4
pipenv shell

```
# R/Rstudio

I install RStudio via the `.deb` package from (`https://posit.co/download/rstudio-desktop/`)

Bioconductor for Bioinformatics and data science packages (DESeq2, limma, edgeR, ggplot2, tidyverse, dplyr, plyr, etc.)

# System

System specific configurations are left to the user. Your software development stack might not consistent of just Python for development. YMMV. 

Other system packages should be user-driven, and your installation may require its own documentation/recap.

For now, I'll say I needed to install some prerequisites from the Ubuntu/Pop!_OS ppa package authorities to install Python.

And now I'll say, `rvm` Ruby Version Manager (`https://rvm.io`) is useful for configuring ruby versions, NodeJS configures itself, your choice of development environment and IDEs or other software may require custom installations.



I use `gpg2` and `ssh` with 'RSA' cryptography for effortless insecure connections to other servers my DNS is shitty at verifying.



## Utility

### `git`

I use vanilla git, a simple shell customization, and a branch manager when things get more complex, aside from documentation in plain `.org`-mode.



.gitconfig
```
[color]
        ui     = true
[core]
        editor = emacs
[alias]
	amen = commit --amend --no-edit
[init]
	defaultBranch = main
```

basic configuration aside from signature/gpg2 signatures.



### gitmode and `$PS1` : Conveneience shell feature for use in all bash terminal emulation.

Gitmode is a script from StackOverflow that I've co-opted along the way to provide features, that, when mixed with my `.bash_profile`, allow for quick coloring and ASCII characters to represent changes to the source tree at each new process on a tty with login shell.



### twig : a Ruby Gem for task/branch management with git.

Twig is a Ruby Gem functioning as a branch manager. It allows for arbitrary metadata to be linked to branches, and it's useful at times when keeping track of specifics in `.org` doesn't make sense. So it's a nifty plugin for quick access to metadata, stash descriptions.


### gpg2 public-key/private-key signature validation

Use `gpg2` to sign your source code befor sending to social media source repositories (GitHub, GitLab, etc.)

### ssh + RSA cryptography

Use `ssh` with RSA cryptography to log-in to tarpits.

# Emacs

Emacs is GNU software. Emacs is a highly customizable editor system that has access to graphics stacks, system calls, code IDE, autocompletion, and much more.

I use `org-mode` for much of my note taking and productivity (to-do lists, documentation, master lists, task-management). The fact that org-mode now can be coupled with the zettlekasten software `org-roam` and associated visualization solution `org-roam-ui`, lots of my organizational problems are wrong.


## `org-mode` - for productivity

Not your average to-do list: ASCII, nesting, linking, pandoc compatibility, and more.

Cycle through collapsed regions of the bulleted list tree, easily rearrange and reorganize your lists, breeze through TODO organization and clock-in, capture notes, reply reminders, journal items, todo items, and basically anything you can template in elisp.
## `org-roam` - for zettlekasten 

Essentially, it's just mind-mapping using more-or-less plain `.org`-mode and emacs key-binding shortcuts to quickly move throughout the network to add/edit information to a zettlekasten system. This is compared to more conventional paid/freemium solutions like Obsidian.

I like that it's just plain `.org`-mode because that means you can grep-out your header (`;;` - comment prefixes), concatenate all your zettlekasten notes into a single `.org` file, then use pandoc to convert it to whatever other format you want. PDF? PPT? Markdown? 


## `org-roam-ui` - visualization solution

This is currently my go-to mind-mapping visualizer. It draws from a directory of `.org` files, say `~/Documents/org/roam` . With the available configuration, it can generate a force-diagram in a canvas and bring the diagram up on your Internet Browser, say Firefox or Chrome. 


## `org-agenda` - capture templates for various spontaneous tasks

Use capture templates to run workflow organizational tasks, all without switching to another buffer window or pop-up window, inline note taking, task capture, todo items, and morel.
