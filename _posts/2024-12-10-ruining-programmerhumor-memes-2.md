---
author: ralston
#image: "/assets/img/dna1.gif"
permalink: /blog/ruining_r-programmerhumor_memes-2
title: Ruining /r/programmerhumor memes
date: 2024-12-10 22:11:00 +0400
description: The best of reddit meets fuNnY cOmmenTary. /s But you may find it informative.
categories: [Opinion, shitposting]
tags: [reddit, prose, opinion, meta, shitposting]
pin: true
hidden: false
---




# monolithGang

![MonolithGang](/images/monolithgang.webp)

[Monoliths](https://en.wikipedia.org/wiki/Monorepo) are an important part of modern programming. When deciding how to structure a web application, a choice has to be made concerning the uses of [microservices](https://en.wikipedia.org/wiki/Microservices), which are arguably easy to construct, maintain, and scale. From wikipedia: "This pattern is characterized by the ability to develop and deploy services independently, improving modularity, scalability, and adaptability.". These are typically [REST-APIs](https://en.wikipedia.org/wiki/REST) and follow a single-purpose paradigm. However, projects that may benefit from independent scaling and maintenance from this kind of refactoring aren't always suitable for microservice frameworks. In this case, restructuring as microservices isn't always suitable for your application, especially if down-time and stability or developer happiness and productivity are at stake. Carefully consider the timelines, feasibility, and desired structure with your engineers before jumping ahead to the microservice pattern.

# Gotta catch 'em all!

![catchallerrors.jpg](/images/catchalltheerrors.webp)


Error handling strategies are becoming very popular with the rise of statically typed programming languages like [Rust](https://en.wikipedia.org/wiki/Rust_(programming_language)), [Scala](https://en.wikipedia.org/wiki/Scala_(programming_language)), [Haskell](https://en.wikipedia.org/wiki/Haskell), [Clojure](https://en.wikipedia.org/wiki/Clojure), and others. These languages rely on strict [static typing](https://en.wikipedia.org/wiki/Type_system) to avoid checking multiple possible types of user or programmer input to a function/method simultaneously. During the programs compilation step (as opposed to 'dynamically typed' languages like Python) the [compiler](https://en.wikipedia.org/wiki/Compiler) will check for compatiblity and explicit type matching throughout the program; the compiler will crash if a program isn't typed correctly.

An easy way to ruin your production codebase (eventually) is to '[catch](https://en.wikipedia.org/wiki/Java_syntax#try-catch-finally_statements)' the errors and ignore or minimally document what errors may arise from improper input types. Catch all the thing and then ignore all the things often leads to unforseen behavior, pushed deadlines, and upset management and developers.



# Threads

![HumorProgrammingAdvanceThisIs](/images/threadshumorprogramming.webp)

The problem with [concurrency](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) is often user error. Also, the problem with concurrency is often concurrency itself. When using programming threads (true threads, green threads, etc.) to solve a particular programming problem, results from side effects and data flow may be unexpected as far as timing goes. IYKYK.


# Programmers love cooking

![Programmers and cooking](/images/programmercooking.webp)

Dependency hell is a common occurence when working with slightly older legacy codebases. Often an update to one version of a library is not necessarily compatible with another, i.e. multiple versions of a dependency are required by the software. The downside to working with older codebases is often offset in some regard to the existing solution simply needing to be maintained.


# DifferentError.jpg

![A different error is sometimes everything](/images/differenterror.webp)

The belief that programmers know exactly how to solve certain problems is a misconecption. Sometimes we spend days trying to untangle messes of library errors, nested functions mishandling errors, tricky dependencies, and errors regarding invalid inputs to functions. A common result can be seen in the meme above. Unforeseen errors and function outcomes often result in different outputs to the console, with obscure or undocumented bugs cascading in program or application failures. Sometimes your manager won't quite understand the nature of delays or unexpected revisions to timeline. Communication is key!

