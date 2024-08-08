---
author: Matt Ralston
image: "/images/dna3.gif"
title: Network Attached Storage (NAS) vs storage server
subtitle: A comparison of costs and features.
category: Hardware
tags: AMD storage SSD prose opinion
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

The suggest solution is actually to assemble and configure a custom workhorse+storage server combo, and use it for both.

| Total cost | Name                                       | Number | individual unit cost | Manufacturer           | Note       |
|        650 | Seagate IronWolf 8Tb NAS HDD hard drive    |      5 |                  130 | Seagate                |            |
|        650 | 2U Server chassis                          |      1 |                  650 | SilverStone Technology |            |
|    300-600 | 12U rack-mount server cabinet              |      1 |                  600 | Sysracks               |            |
|        410 | ASRock WRX80D8-2T ATX Server Motherboard   |      1 |                  410 | ASRock                 | SP3 Socket |
|       1700 | AMD 3rd gen Epyc 64c 7773X 2.2GHz 768Mb L3 |      1 |                1700+ | AMD                    | SP3 Socket |
|        150 | 64Gb kit GDDR5 ECC RAM                     |      1 |                  150 |                        |            |
|  Subtotal: |                                            |        |                      |                        |            |
|     ~ 4200 |                                            |        |                      |                        |            |



