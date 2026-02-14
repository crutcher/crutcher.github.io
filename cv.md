---
layout: page
title: CV
permalink: /cv/
---

My name is Crutcher Dunnavant.

I'm an HPC engineer and computer scientist; My career has been focused on the intersection
of formal language design, high performance computing, distributed systems engineering,
and machine learning.
I've worked for Red Hat, Google, Meta, 3Scan, McDonald's (in AI), OpenAI, and Atmo.


### Independent Rust AI Research

#### Image Processing / Models for Rust/Burn

I have been incrementally porting the underlying machinery needed to support modern SOTA image models in the [https://burn.dev](https://burn.dev) Rust AI framework. This constitutes two bodies of work:

* Extensions to Burn to support image models:  
  [https://github.com/tracel-ai/burn/pulls?q=is%3Apr+author%3Acrutcher+is%3Aclosed](https://github.com/tracel-ai/burn/pulls?q=is%3Apr+author%3Acrutcher+is%3Aclosed)
* Ports of image libraries to Rust/Burn:
    * [https://github.com/crutcher/bimm](https://github.com/crutcher/bimm)

#### Distributed Tensor Expression Theory

Since the 3Scan work in massive distributed tensor storage and processing; I’ve put years of effort into fleshing out the underlying machinery and math to support distributed tensor expression optimization.

* [https://github.com/crutcher/tapestry/tree/main/docs](https://github.com/crutcher/tapestry/tree/main/docs)

## Work History

### Atmo \- Principal Engineer

Atmo is a short-range regional AI weather forecasting company, focusing on bootstrapping global low-resolution forecasts (such as NOAA’s GFS) over the next 72 hours into high-resolution local regional forecasts, at significantly higher accuracy than interpolation.

I worked as Principal Engineer, focusing on AI research and scale. My responsibilities included:

* Designing the AI coupling model to bridge Swim-Transformer volumetric temporal causal transforms at different scales (the global boundary clipping region, and the local high-res region).
* Rebuilding our full AI model stack; making heavy use of unit testing and contract programming.
* Restructuring the full data load and transformation stack.
* Rebuilding the full training stack.
* Designing and extending the Metric and Loss surfaces.
* Tuning production models for several governments; including the Philippines.

I also picked up a number of side projects, including rebuilding our web map interface for a high-profile (but NDA shielded) contract when our FE Dev left the company, and we were constrained (by heavy use of virtual machines by our clients) to provide a non-GPU accelerated version of the web frontend.

### OpenAI \- Research Acceleration

I worked at OpenAI in the Research Acceleration group. My work focused on reduction of technical debt, adding unit tests and code stabilization, unifying shared libraries, and working to de-risk the serious branch proliferation the company was operating on (research was, at that time, 7 months diverged from the main branch in many projects).

I also wrote new bindings for NVIDIA’s **libverbs** RDMA library stack; by building a C/C++/nanobind/python library stack. This was developed to permit OpenAI to work around limitations in existing RDMA libs for pytorch.

### Meta \- AI, Various

I worked at Meta in several roles, during the pandemic ScaleUp/ScaleDown/Layoff cycle. Various responsibilities included:

* Auto-Tuning AI Model Stack
* Rebuilding the primary first-pass fast-scorer (used across FB and Instagram) for the next-gen AI training stack, and addressing numerous architecture bugs in that training stack.
* Working on the RayBan Glasses video “interest” optimization model for summary clips.
* Working on the next-gen LLM chat model in flight at the time.
* Working in the PyTorch group.

### Apprente / McDonald’s Tech Labs \- Infrastructure Director

I worked for an AI startup called Apprente, restructuring their demo AI into something we could scale and support; which was then sold to McDonald’s as an AI Drive Through Operator. I worked as the Infrastructure Director and Principal, with 8 reports overseeing the redesign of the AI into a kubernetes queue stream from sound collection, through phoneme models, action models, and the action state machine, along with the debugging tooling for distributed queue events; the telemetry collection framework and backend stats analysis, the build env and build / CI pipeline, and the packaging stack and release machinery.

See: [https://techcrunch.com/2019/09/10/mcdonalds-acquires-apprente/](https://techcrunch.com/2019/09/10/mcdonalds-acquires-apprente/)

### 3Scan \- Infrastructure Lead

I worked for a medical research development startup, 3Scan, which built a robotic microtome microscope. This device would produce terabytes of data for each tissue sample. I lead the design and implementation of the cloud storage and processing framework for uploading, storing, random access, and running tensor convolution operations over 40TB 4D tensors which were produced by that robotic tissue slicer. We were able to run 170TB pipelines in \~20 minutes, in 2018\. 3Scan merged to become Strateos.

### Google

I had a ten-year tenure at Google, during which I held four major roles.

#### Google: AI Research

My final position at Google was working as a researcher in Moshe Look’s Knowledge Graph anomaly detector auto-trainer; as part of Kurzweil’s AI research group. This system trained thousands of KG topic models, each bootstrapped via uncertainty curve mining, and evolved as Sum/Product network instances in a distributed Pareto optimization space; which we implemented all of.

An interesting side-project was my development of a C++ “number-like” extension library, still in heavy use today at Google as “FineNum”. This stored in a single 64 bit float; but was a log-space number replacement, making heavy use of C++ operator overloading and cast operators to permit log-space algorithms to be written as their normal-space algorithmic equivalents; for numerical stability in the accumulation of many partial factors.

#### Google: CiTC

I then worked as the designer, technical lead, and principal engineer on the CITC distributed development filesystem, a system that supports all of Google's server/infrastructure development workflows and holds millions of globally available workspaces. This system facilitates both desktop and web development, remote build farm tooling, and forms the basis for code review tooling. Part of my work is discussed in this ACM article: [https://cacm.acm.org/magazines/2016/7/204032-why-google-stores-billions-of-lines-of-code-in-a-single-repository/fulltext](https://cacm.acm.org/magazines/2016/7/204032-why-google-stores-billions-of-lines-of-code-in-a-single-repository/fulltext)

#### Google: Health Records

Backend/data semantics engineer for Google Health; focusing on integration and implementation of various health records interchange formats with our database storage. Did primary work on the Continuity of Care interchange document standards, and attended several conferences as Google Health’s rep on these documents.

#### Google: Content Ads Production / Scaling

I played a critical role in migrating content ads to the Borg distributed cluster scheduler, a new technology at the time that later inspired Kubernetes. My responsibilities included building much of the core infrastructure scaling rules, developing sophisticated reporting systems for telemetry data, and creating a production test cascade framework to probe data center software configurations.

### Red Hat

I worked as a core OS Developer on Red Hat Linux. My responsibilities included:

* Packaging, debugging, and coordinating upstream work for about 60 distribution RPM packages.
* Working on OS configuration automation for remote management.
* Fielding support bugs, and tracing them through the package stack to identify, repair, coordinate upstream fixes, and push package updates.

## Education

* B.S. Computer Science, University of Alabama, 2002
* M.S. Computer Science, University of Alabama, 2004
* Work towards PhD, University of Alabama, Aug 2004 \- June 2005

