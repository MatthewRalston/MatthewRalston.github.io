---
permalink: /cloud_native
title: "Cloud native architectures, containers, DevOps, and SysAdmin"
date: 2025-03-15 03:44:00 +0400
layout: post
categories: [About, Cloud, DevOps, Docker, SysAdmin]
tags: [About, Cloud, DevOps, Docker, SysAdmin]
render_with_liquid: false
---


Consider my recent blog post on [Docker containers and kubernetes](/machine_learning_infrastructure_deployment_and_notebook_management) for a more current discussion of DevOps and k8s.


The discussion begins with consideration of classical (ca. 2000 server-side system administrative practices) systems administration. Most of the early web ran on bare metal on-prem, or on early cloud systems. Knowledge required includes OSX/Linux operating systems, HTTP2.0 communications, REST/SOAP systems, relational databases (MySQL, MariaDB, SQLite3, PostgreSQL, Oracle, Microsoft SQL server), filesystems (ext4, xfs, zfs, btrfs), source tarball installation, programming language conventions and dependency troubleshooting, and more.

During the mid 2010s there was a movement to cloud-native platforms for price sensitivity. This gave rise to the modern `git` or `svn` version control systems, coupled with sourceforge, bitbucket, or Github/Gitlab, Google Colab, and Markdown-driven documentation style to software development. For some applications and systems, more complex configuration is necessary to ensure the proper interplay of meshed services. Enter the [Docker container](/machine_learning_infrastructure_deployment_and_notebook_management#enter-docker).

Most application code and service configurations are stashed away in a version control systems (VCS) such as `git`, 'mercurial', or 'subversion' `svn` repositories. The code and documentation provide implementation details for deploying an application, migrating data, and system maintainance.

During the period after the coronavirus pandemic of March 2020, the convention for cloud-native application architectures relies on some combination of VMs, containers, orchestration tools (Chef, Ansible, Puppet), and cloud-vendor (AWS, GCP, Azure) specific configuration. 

Common knowledge practices suggest that the best option for cloud agnostic and cloud-native architectures includes Docker and kubernetes at some level. Dockerfiles are similar to shell scripts that would have done the heavy lifting of sysadmin roles in the 2000s, in that they primarily deal with shell-level configuration of environments for a specific single-feature single-purpose design and compilation or install target.

## devops

"Development Operations", or simply devops, involves the configuration of system for application stacks within the context of the goals of the entire app. Primary tools for devops include Docker, kubernetes, Ansible, Chef, Puppet, and the boto3 AWS SDK for Python. Goals for devops positions include decreasing the load of technical debt, to make application subsystems reusable and long-lasting during a program's lifecycle, and packaging services or subsystems for the application according to their goals diagrammed during requirements discovery and fine-tuning.

## Docker containers

Containers, and more specifically Docker containers, use kernel virtualization in Linux systems to produce so-called "lightweight" virtualization. These containers are lightweight operating system images, stored as binary artifacts associated with repositories in the Docker image "registry". Associated with a repostiory are container components, dependencies, and the `Dockerfile`, a recipe for creating the image artifacts and resulting operating system and application configuration from known and packaged assets in the registry's repository.

From [Wikipedia.org/wiki/Docker_(software)](https://wikipedia.org/wiki/Docker_(software)): 

>"The Docker software as a service offering consists of three components:

>[Software]: The Docker daemon, called dockerd, is a persistent process that manages Docker containers and handles container objects. The daemon listens for requests sent via the Docker Engine API.[22][23] The Docker client program, called docker, provides a command-line interface (CLI) that allows users to interact with Docker daemons.[22][24]
>[Objects]: Docker objects are various entities used to assemble an application in Docker. The main classes of Docker objects are images, containers, and services. A Docker container is a standardized, encapsulated environment that runs applications. A container is managed using the Docker API or CLI. A Docker image is a read-only template used to build containers. Images are used to store and ship applications. A Docker service allows containers to be scaled across multiple Docker daemons. The result is known as a swarm, a set of cooperating daemons that communicate through the Docker API.

>[Registries]: A Docker registry is a repository for Docker images. Docker clients connect to registries to download ("pull") images for use or upload ("push") images that they have built. Registries can be public or private. The main public registry is Docker Hub. Docker Hub is the default registry where Docker looks for images."


## devops vs sysadmin

Systems administration has traditionally involved subject matter expertise and experience with varieties of systems and their configurations. Reproducing a system configuration was a principle concern of early "lift-and-shift" cloud deployments and was often done through the knowledge of both local and cloud systems, storage options, caching, object storage (static assets), CDNs, and other subject area expertise.


## Commodity cloud vendors: AWS, GCP, MS Azure, Oracle

Modern cloud vendors often rely on data centers in different 'availability zones' to host and store infrastructure for clients on, what is referred to as, the 'commodity' cloud. Vendors such as Amazon have very large presence in the market for services such as object-storage (Amazon S3), block-storage (EBS), container services (ECS, ECR, EKS), and monitoring (Cloudwatch). 


### Cloud costs 

Storage in per GB per month (object/block)
Compute considers a VM with 2vCPU and 4GB memory

| Service   | AWS    | GCP    | Azure    | Oracle   | 
| ----------| -------| -------| -------- | -------- | 
| Object    | 0.023  | 0.023  | 0.01     | 0.0255   | 
| Block     | 0.08   | 0.068  | 0.018    | 0.0255   |
| Compute   | 0.033  | 0.045  | 0.041    | 0.03     |




Many services are available on different commodity cloud vendors for specific applications such as HPC, GPU compute, block and object storage, container/k8s services, VMs, serverless, and managed databases. This can make cost comparisons difficult at face value, and depends instead on your application architectures and lock-in to certain vendor services and pricing.

By leveraging so called 'cloud-native' technologies such as Istio and kubernetes/k8s, developers can create amazing applications and deploy them on Commodity cloud to take advantage of audit features from the vendor, as well as 'good' prices. Amazing prices can be found on other cloud vendors, but the guarantees that suffice for large enterprises are not always there.
