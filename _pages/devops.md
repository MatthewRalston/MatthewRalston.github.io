---
permalink: /cloud_native
title: "Cloud native architectures, containers, DevOps, and SysAdmin"
author_profile: true
toc: true
---


{% include page_header.md %}

Consider my recent blog post on [Docker containers and kubernetes)(/machine_learning_infrastructure_deployment_and_notebook_management) for a more current discussion of DevOps and k8s.


The discussion begins with consideration of classical (ca. 2000 server-side system administrative practices) systems administration. Most of the early web ran on bare metal on-prem, or on early cloud systems. Knowledge required includes OSX/Linux operating systems, HTTP2.0 communications, REST/SOAP systems, relational databases (MySQL, MariaDB, SQLite3, PostgreSQL, Oracle, Microsoft SQL server), filesystems (ext4, xfs, zfs, btrfs), source tarball installation, and more.

During the mid 2010s there was a movement to cloud-native platforms for price sensitivity. This gave rise to the modern `git` with Github/Gitlab, Google Colab, and Markdown-driven documentation style to software development. For some applications and systems, more complex configuration is necessary to ensure the proper interplay of meshed services. Enter the [Docker container](/machine_learning_infrastructure_deployment_and_notebook_management#enter-docker).

Most application code and service configurations are stashed away in a version control systems (VCS) such as `git`, 'mercurial', or 'subversion' `svn` repositories. The code and documentation provide implementation details for deploying an application, migrating data, and system maintainance.

During the period after the coronavirus pandemic of March 2020, the convention for cloud-native application architectures relies on some combination of VMs, containers, orchestration tools (Chef, Ansible, Puppet), and cloud-vendor (AWS, GCP, Azure) specific configuration. 

Common knowledge would suggest that the best option for cloud agnostic and cloud-native architectures includes Docker and kubernetes at some level. Dockerfiles are considerably similar to shell scripts that would have done the heavy lifting of sysadmin roles in the 2000s, in that they primarily deal with shell-level configuration of environments for a specific single-feature single-purpose design.

"Development Operations", or simply devops, involves the configuration of system for application stacks within the context of the goals of the entire app. Primary tools for devops include Docker, kubernetes, Ansible, Chef, Puppet, and the boto3 AWS SDK for Python. Goals for devops positions include decreasing the load of technical debt, to make application subsystems reusable and long-lasting during a program's lifecycle, and packaging services or subsystems for the application according to their goals diagrammed during requirements discovery and fine-tuning.





