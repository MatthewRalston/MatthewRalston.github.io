---
permalink: /machine_learning_infrastructure_deployment_and_notebook_management
title: "Thoughts on ML deployments, containerized workflows, and notebooks."
author_profile: true
toc: true
---


This article hopes to bring the reader up to date (ca. 2017-2022) on modern cloud-native and scalable solutions for data science and natural science research application stacks using the Docker container standard for container specification (vs Singularity, Podman, or `containerd` containers that are equally valid). First I will provide a brief description of the goal of Docker containers. Next I'll touch on the kubernetes architecture for distributed data processing and application service management. Finally, I'll describe code repository, container registries, and Markdown/Rmarkdown/LaTeX documentation as it purtains to a service's lifespan w.r.t. notebooks and documentation of custom services and their orchestration. 


## Top 3 prerequisite topics:

* [Docker: the container standard](#enter-docker)
* [Kubernetes/k8s, kubectl, and related](#kubernetes)
* [Documentation: Markdown/Pandoc/LaTeX](#documentation-and-notebooks)

## Enter Docker

On March 20, 2013 Docker was released as a first-in-class containerization solution for managing application architecture and dependency networks, install processes, and much of what was typically relegated to Linux systems administrators as sets of related code, protocols, documentation, and configuration and designed on a case-by-case basis. The following 10 years of containerized code, system services, and application architectures have made standards for reproducibile software builds the center of designing modern service architectures for maintainable, scalable, and flexible deployment processes.

Key concerns for any application include the needs of the client, required servers, and involved low-level libraries managed at bare-metal, VM-level, or container-level integrations. The code at those levels must have access to (and awareness of) installed systems made available to the logged-in user at that level (the 'service' user). By containerizing you can run a single service as the collection of the application code and required system depdendencies and deploy this on a production kubernetes environment.

From Arthur Busser at [theodo.com](https://cloud.theodo.com/en/blog/container-docker-oci): 

>"The software industry has a myriad of boxes into which to put code. Boxes like Debian software packages (.deb files) or Java Archives (.jar archives) allow developers to package their applications so that they can easily be copied to and run on different machines.
>But these boxes have limitations: Java Archives can only hold Java code, and Debian packages only work on the Debian family of Linux distributions. Modern applications rely on a variety of programming languages and operating systems: the industry needs a box that is multilingual and multi-platform.


>For example, a Django web application needs the Python code interpreter to run, but may also rely on system libraries, which can be different depending on the operating system. The code must be packaged with its entire environment to run reliably everywhere. In other words, every single dependency must fit into the application's box.

>This idea is not new to the software industry. For many years now, operators have used virtual machines as this kind of box. Everything fits inside a VM: the code, its dependencies, and even the operating system. The critical insight here is to ship the application alongside the entire system.

>A developer's choice of distribution affects the behavior of their application, and swapping out these system libraries would change the behavior of the software. The system is part of any application a developer writes.

>The issue with virtual machines is that they also contain virtual hardware. A developer should not decide how storage or networking is going to work, or what kind of processor to use. Such overreach would hinder the infrastructure provider's freedom to make hardware decisions based on where the application is being deployed and would break the separation of concerns between developers and operators.

>Think back to the metaphor of the shipping container. A shipping company should be free to use whichever train or warehouse they wish to move and store containers; the contents of a container should not be a factor when deciding what infrastructure to use. Another problem with virtual machines is that they use a lot of CPU and memory, and take a long time to boot. A virtual machine is still a machine. It is not a suitable unit for software delivery."

>DotCloud — now Docker, Inc. — released Docker as an attempt to leverage Linux namespacing to provide software engineers with a standard box. Linux namespaces are a feature of the Linux kernel that allows for one set of programs to see one set of computing resources, and another set of programs to see another set of computing resources.

>This feature was present in the kernel long before Docker was released, but using raw kernel capabilities directly is not high on the list of priorities of most developers. However, Docker provided an interface that made almost no mention of Linux namespaces and aimed to be as easy to use as possible.

>Docker open-sourced three things that allowed their container tools to be widely adopted: A standard container format; Tools for developers to build containers; Tools for operators to run containers;

>Docker's standard box for packaging software is a file archive inside of which developers can put all that their program needs — code, libraries, or any other file — as well as basic instructions for starting the application. This archive is called a container image. Once built, images are static: they never change.

>This immutability is essential because it allows developers to version their images, and operators not to worry about an image changing when the application it contains is running. Docker's image format uses a copy-on-write filesystem to make images immutable, but this is an implementation detail and goes beyond the scope of this article."



As described concisely by Mr Busser, containers are a production-grade solution to Virtual Machine management platforms and their often vendor-specific specifications. By simplifying the OS management aspect, Docker and Kubernetes are able to deploy across a large number of hardware specifications, application requirements, and software architectures.

Typical concerns of the application architecture tend to be systems administration topics. Choice of host operating system, the service mesh, networking, security, and code audits. When doing so, there are two distinctions between aspects of "the code base": the IaC (infrastructure as code) and service (k8s, bare metal, VM, per-machine, etc.) level code vs the application code. The application itself is a network of services, code, data processing steps, and even AI applications. The infrastructure code provides backend orchestration for the proper networking of the various components of the application code.








## Kubernetes




## Documentation and notebooks
