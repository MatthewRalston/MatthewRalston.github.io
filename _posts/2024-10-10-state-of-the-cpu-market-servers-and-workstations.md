---
author: Matt Ralston
header-image: "/images/dna1.gif"
hero-title: Server CPUs, market differentiation, the e-thread hatetrain, and power efficiency
hero-subtitle: AMD dominance, Intel solid contender, ARM reaches new markets and continues to advance towards traditionally Intel and x86_64 dominant areas such as supercomputing.
category: Opinion
tags: AMD Intel CPU prose opinion meta
---


## What is the state of the CPU market
 - consider server CPUs and workstations or small PC CPU architectures for high-performance compute.


 Well, you typically dont consider small PC or workstations CPU product SKUs for the high-performance computing market...


Consider non-server strenuous CPU demanding tasks, such as processing information related to metrics, observables, distributions of data
 or simulations of distributions and their associated outputs, which may then be used to model or simulate errors and noise profiles useful
 for rigorous testing of edge cases and simulated errors and their frequencies. Simulating such distributions and analyzing the data requires
 considerable memory and resources become quickly exhausted. At the CPU level, the best advantage is a large local cache. The AMD Epyc parts
 and Zen 3+ architectures are considered revolutionary because of their 3D VCACHE solutions for stacking memory inside the various components of the dye
 and its associated microarchitectures, primarily the L3 cache. Which at modest SKUs for the AMD Epyc architectures Milan(Gen 3 or 4), Genoa(Gen 4), and Turin (Zen 5)
 such as the Milan Epyc 7703 CPU part, which is the winner of the value proposition for a 64-core, 128-thread part. For intensive server applications,
 scientific compute, simulation, video and illustration editing, animation, etc. the quality of the server part may be categorized into roughly clock-speed (3.35Ghz; most parts are between 2-4 Ghz for ca. 2019 - 2024)
 instruction sets (x86_64 vs ARM), L3 cache, PCIe lanes (128?), and additional features.

 My recommendation, as stated, is the Milan Epyc 7--- series models. 8-64 core solutions. it's like 128Mb L3 cache. Obvious winner.


 Yeah Intel parts are there, but the area of compute that interests me is distinctively memory heavy and resource constrained: high-performance compute. And there's a lot of buzz and hype and micro-rationalizations about AMD hype.

 It's not hype. I have a friend that uses Threadripper exclusively and the part burns. If you're doing data-science or statistics, or other mathematics workflows, then the AMD part market is dominant in this generation, marginally, over Intel products.

 I'm over it.
 
 It's the obvious choice for most hardcore computing workloads and burst potential. Yeah so the guy in the hackneyed blog up the way says well, Matt's being elitist and Intel is trying new things, and their market dominance for years put the best know-how 

 Specifically, the multithreading would be terrific with the appropriate backplane.
## The obvious is x86_64

The x86_64 instruction set architecture and intermediary forms grants AMD and other licensed partners the ability to use largely optimized-for-intel binaries, historically awesome programs written for earlier versions of intel chips running Windows or Linux. It means we get better ecosystems of software that largely don't affect you and me at all.
## It's actually the PCIe lanes
Yeah, you can run an extraordinary number of different applications on a single motherboard and while multi-GPU still remains the punchline, much like AMDs GPU and compute support,
though modernizing... I'm aware that there are big moves towards better libraries for the graphics developers as well as quality of life for game devs, graphics engine support and... well there's a lot of players modernizing and it's hard not to miss the bus on choosing Nvidia for graphics compute.

And I'm not even at that level completely, modestly so. I haven't written my first CUDA kernel yet, I'm still working on Leetcode fundamentals. I write clean program and defensively "lean" tdd? But the topic wasn't me.
## So yeah the sauce is actually the PCIe connectivity
and gen3 vs gen4 is essentially the entire issue. High-speed doesn't mean high-IOPS and I'm not as of yet network certified by Cisco, IBM, AWS, or others, I'm pursuing my CompTIA A+ and SCSP to get a good start at where I might want to be.

Storage and cacheing are evergreen areas of compute, because data locality is a system-level (as opposed to subsystem) issue in desigining data-center or data-center aware bottom-up solutions.
My thoughts are, get in to switches and fabric, specifically Mellanox Infiniband because I'd like the right connection.

We'll see how things form as I learn about storage, networking, fabric, switches, and servers.
## But it's actually the instruction set

ARM stands out for its low-power profile CPUs, made famous by the power pc market and Apples early MacBook Pro and Macbook products in the early 2000s. But low-power typically means, lower boosting and reactive workloads. Server processes and asynchronous tasks are better suited for lower clock speeds. While these PC parts remain strong, even with small form-factor competitors such as the Raspberry Pi in different markets that ARM excels in, IMO these aren't the parts your looking for in servers yet.

So the x86_64 intel owned architecture brings in essentially nothing for the average person, aside from the ability to run standard x86_64 operating systems, such as Fedora, CentOS, Debian, Ubuntu, Manjaro, Gentoo, Arch, Slackware and others. BSD even, hell.

SO yeah the sauce is in the clockspeed. Higher juice means the CPU is tuned and power profiled differently than other parts. It's a modern part.
## So in conclusion, it's the L3 cache

All you have to worry about is what's in your lane.

Fin.


## Just kidding, so what about Windows Server?

Windows server remains a viable option on permissive systems, homelabs and rackmount servers. Just host a virtual machine service, assume responsibility for all of the hardening, and launch Windows servers (and others) with no obstacle. VMware remains a popular vendor.


## For the other kind of people

You need some perspective on what the current server market looks like. Xeons are still heavy-hitters, and pack hundreds of processors into a single dye. 

Without a clear leader, vendors including AMD and Intel are free to raise prices, that's why you see so many HP and Dell laptops in the $1-3k price range these days. The processes have become *more* efficient, and prices have obviously gone up on the consumer end. The chips are better and newer too, so you see some true value there, just like the average customer has with a portable office or home hardware solution. 

Without that leader, it's just a matter of time before we run out of Angstrom's to shave off the transistors and we'll be on to new challenges with optimizing what we can. 


## Conclusion

But seriously it was the massive L3 cache.

--------------------------------------------------------------------------------------------------------


 
