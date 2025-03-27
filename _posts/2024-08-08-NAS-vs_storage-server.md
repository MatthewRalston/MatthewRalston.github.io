---
author: ralston
title: Network Attached Storage (NAS) vs storage server
description: A cost and features.
date: 2022-03-16 16:16:00 +0400
categories: [Hardware]
tags: [copypasta, prose, opinion]
hidden: false
pin: true
---


## What is Network Attached Storage (NAS)?

Okay, let's begin briefly on the topic of Network Attached Storage. A NAS can be inside a larger server cage within a much larger server rack. This is called a NAS *server* as is different from a consumer grade, standalone NAS unit. 

Such units typically have 2-8 Hard Drive bays. They have their own 2-8 core CPU, 8-16Gb RAM preinstalled, and the standalone units essentially can only serve files.

Small businesses with more robust needs than can be met by these home office products should instead choose to purchase a pre-built server (1-10k USD), or construct their own from components meeting their budget.

## Major Players

A NAS can be a standalone unit, rather than a full server, and popular brands include:

- QNAP
- Synology
- TrueNAS
- BUFFALO
- Western Digital
- Asustor
- TERRAMASTER

and others.

These so called "standalone" units are small, 25" x 17" x 3.5", typically have 2-8 bays of storage, and are small 2x4' standalone storage drive devices for home and small-business "convenience" data storage segments. These are not production ready devices, and sell for 200-500 on the small end (2-4, 3.5" hot-swappable drive bays), and up to 500-1500 USD on the larger side (4-8,  3.5" drive bays).



## What is a "Home" version of a Network Attached Storage (NAS) device

These brands often bundle simpler and cheaper CPUs with simpler RAM configurations and design their units primarility for personal, home office, or very small business, say 1-5 people's worth of storage for say 3 years, if they are all not 'big' data professionals, and work in the MB to GB range, for years, accumulating 10s of terrabytes of data at a time, vs data professional (100s of Tb), a small data group (1000s of Tb/year), and groups and divisions of companies working on millions of terrabytes or more ("big data" groups/companies).


Because of this, the units primarily serve as file servers and are customarily designed to have simple, cheaper chips that are under 8 cores. RAM configurations under 16Gb are common, as they are only serving a small volume of requests to the devices local to the personal, home-office, or small business setting where the NAS is on network, say maybe 5-20 devices.

Beneath a certain point, most businesses prefer to go with a storage server that is pre-built, consumer-grade, and that has simple redundancy.


For this reason, the storage comes with it's own 'computer chip' that is minimal and sufficient for typical personal needs. But in our case, we need a better server. Why? Because spending money on a half-assed solution won't get the work done: the prototype pipelines cannot be tested on a 4Gb server reliably. Instead, a 64-core configuration is necessary, with costs optimized as follows.

## Why skipping the "Home" NAS makes more sense

Don't spend on mediocre hardware, because the drives to put in these "simple" $500-1500 home-NAS solutions aren't free either. You have to buy them separately.

I'd like to talk to you about my rationale on why it is necessary to abstain from spending any capital on stop-gap solutions, and try going to market, and a suggestion regarding the financing and work scheduling to offset majority (2.5k) of total expense regarding the prototype.

A computer or server's core needs are the same: a Central Processing Unit (CPU), Random Access Memory (RAM or DRAM), Motherboard, Boot Devices (SATA SSD or NVMe), Storage Devices for the backplane (SATA SSD, NVMe SSD, HDD), Power (2x 2U 240W Power Supplies), and networking.

The smaller "home" NAS solutions come with simplified hardware, insufficient memory requirements, and light-weight < 8-core CPUs. For workloads involving hundreds or thousands of samples, this won't meet client requirements when the pipeline can be scaled up.




## Suggested Solution

The suggest solution is actually to assemble and configure a custom workhorse+storage server combo, and use it for both. The server would be used to prototype workloads for high-performance computing tasks, specifically, running pipelines and HPC computing tasks in somewhat more controlled environments called "Docker containers".

I won't discuss how I plan to accomplish this publicly. 

## What about the prototyping stage and how would you research your market?

I plan to consider a few options for prototyping the first pipelines. I will segment the market according to the service package requested, and produce additional software and EULA for the non-standard service packages.

I plan to target compatible labs with a combination of traditional marketing and digital setters. The marketing channels primarily funnel to my store's page on Stripe. There may be free consultations/project work/or other proactive and reputation centric services provided early on, to attract future business, and start grassroots interest in academic partners at University of Delaware, and this tri-state area.

The way I'd establish it, is offer 1-month or 2-month structures. I'd ask the PI to fill out a small questionaire, with appropriate language for requirements gathering to continue under NDA, and other contingencies be addressable by policy and procedure.

1-month structures would be, fast turn-around, fairly generic analyses and deliverable packages, less than 200 samples, for now. Upgrade structures may include, additional pipelines, encryption options, public-cloud, data warehousing services, etc.

## What is being developed currently

The primary deliverable under development is a pipeline of reproducible components for each package. Currently there is 1 package regarding this pipeline with most 16/20 components implemented, but it is nearly impossible to test without the correct infrastructure.

That said, the pipeline itself exists as a shell script on my system, and I am prepared to start taking clients shortly.


## Could you deliver if, say, next week someone offered you a $3000 contract for your standard 200-sample RNA-sequencing development?

Yes. I would deliver graphics and a 5-10 page Quarto or Rmarkdown report describing methodology, results, and describing value in an executive summary about insights gained, obstacles to analysis or characterization and how they were addressed, how the quality of the samples were assessed, and what steps were used to capture the results and how that could be done again.

However, a collection of shell scripts and statistical reports and generated reports in a archive is far from the long term goal for each deliverable, even if the turn around time was 1 month or less.

I couldn't deliver the more advanced prototype of the reproducibility framework by next week, but that's on the charts.


> Yeah I immmmeeeeeeediiiateeely regret buying into ANY of this stuff. (2/15/25)

