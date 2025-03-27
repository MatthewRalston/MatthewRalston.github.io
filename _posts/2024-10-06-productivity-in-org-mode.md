---
author: Matt Ralston
title: Don't copy loosers.
description: No really. WHy copypasta dummies... But.. *sigh* What is your task management and organizational workflow?
date: 2023-05-06 19:25:00 +0400
category: [Opinion]
tags: [linux, software, prose, meta]
hidden: false
pin: true
---

## Goals

1. Introduce org-mode briefly for those unfamiliar with it.
2. Explain some key benefits of using org-mode for personal productivity.
3. Share experience and workflow using org-mode.
4. Include one short org-agenda cheatsheet
5. Discuss how org-mode integrates with other tooling
6. Offer tips for getting started with org-mode for productivity.
7. Mention any challenges I've found


## Introduction

`org-mode` is installed with each new installations of GNU Emacs (v27+) and above. It is primarily a plain-text bulleted list and tree editing mode.

# Key Benefits

Coupling `org-mode` with other forms of literate programming via `pandoc` makes interconversion of `org-mode` documents with LaTeX support inline, a pleasure to edit in Emacs.

I feel at my best when I can use capture templates to stash and reorganize simple [TODO] items, capture notes, express deadlines, and manipulate information easily using emacs key bindings and `org-mode`s positional rearrangement hotkeys for list editing and managing my notes.

To add functionality, check out the `org-mode` compatible libraries on MELPA and consider `org-roam` for Obsidian-like graphical note experiences.

# Personal Experience and Workflow

My workflow involves vanilla `org-mode`, `org-agenda` for capture mode and template-driven note taking. I try to use timestamping but it's arguably a weaker point when I'm doing serious debugging.

Capture mode allows you to capture notes effectively inline, and places you right back where your cursor was before your idea/note/journal/reply took you away for a moment.

I find this incredibly convenient.

# Small example

Copy and paste the following into a fresh `.org` file. It's a rough guide for basic org-mode functionality.


```
* Emacs basics
** C-h v - describe a variable
** C-x f - open a file
** M-x command-name - run a command
** M-x treemacs-mode - start a directory structure
* Org-mode pomodoro
** C-c C-x ; - start pomodoro timer
** M-x org-timer-pause-or-continue
* Org-mode essentials
:PROPERTIES:
:TYPE:     Meta
:END:

** M-{Left,Right,Up,Down}        - Change indentation, position of bullet
** M-RET        - New bullet at current level
:PROPERTIES:
:TYPE: Create
:END:
*** M-S-RET New TODO item at current level
:PROPERTIES:
:TYPE: Create
:END:
*** S-{Left,Right} Change state of TODO item
*** C-c C-x TAB        - CLOCK IN on a task!
*** C-c C-x C-o        - CLOCK OUT on a task!
*** S-Right        - Cycle to DONE to complete AND log the completion time!
*** C-c C-s        - Schedule time for a task
*** C-c C-d        - Schedule a deadline (7d)
** Tasks / checkboxes [1/2]
    - [X]        - Step 1: Use list syntax: '-'
    - [ ]        - Step 2: Use checkbox with / to reference task completeness in parent task
      - [ ]        - Step 2.a: Use indentation rules (M-RET + M-{Left,Right,Up,Down}) to add subtasks
      - [ ]        - Step 2.b: As subtasks are checked, they will eventually check the parent task (Step 2)
*** C-C C-c        - Toggle checkbox
** Formatting (org-mode plain-text formatting)
*** *Bold*
*** /italic/
*** _underline_
*** =verbatim=
*** +strikethrough+
*** Example^{superscript}
*** Example_{subscript}
** Formatting (LaTeX)
*** C-c C-x C-l        - Use LaTeX to preview fragments
*** $$ Cov(X_{i}, X_{k}) = 0 $$ iff X_{i} and X_{k} are independent
** Source code blocks
*** <s TAB
*** #+BEGIN_SRC lang
*** #+END_SRC
*** C-c '        - Edit source block in buffer with major mode of language
** Clock-in on TODO item
*** C-c C-x C-i    - Clock in on item
*** C-c C-x C-o    - Clock out on item
* Org-mode drawers/properties
  :PROPERTIES:
  :TYPE: Meta
  :END:
** Category property can be used to group information
** C-c C-x p        - New property
:PROPERTIES:
:TYPE: Create
:END:
** C-c C-x s        - Set property
** C-c C-x d        - Delete property
```

## Integrations

`org-agenda` allows you to create templates for different "spontaneous" thoughts/replys/todo/respecifications that you need to capture, using capture templates.

`org-roam` allows zettlekasten and a brilliant web interface to collections of notes, broken down into the roam system. org-roam and org-roam-ui together provide a unique way of creating a "digital-brain", an archive of notes and concepts, mapped together and visually accessible zettlekasten note networks.

## Tips

Focus on your templating, they are as needlessly or as casually different from markdown via the [Tab] key toggle of the primary node syntax with `.org` plaintext markup. That's what makes `.org` shine over markdown flavors. That's the essence of the convenience that org-mode provides

6. Offer tips for getting started with org-mode for productivity.


7. Mention any challenges I've found

Definitely templating, due to my lack of knowledge of elisp more than so could gift one to confiure templating menus as conveniently as other GUI systems.

Also hot-keys, so I'm still studying my own cheat-sheet as needed to keep pace with my other engagements.








