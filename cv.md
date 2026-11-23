---
layout: page
title: CV/Resume
permalink: /cv/
---

# Crutcher Dunnavant

- [Long Resume](cv/CrutcherDunnavant.resume.long.pdf)
- [Short Resume](cv/CrutcherDunnavant.resume.short.pdf)

Nov 5, 2026 · @Crutcher

**Principal Engineer — ML Infrastructure & Distributed Systems**

San Francisco, CA · (205) 887-2552 · crutcher+resume@gmail.com · [github.com/crutcher](https://github.com/crutcher) · [linkedin.com/in/crutcher-dunnavant-4841ba9](https://www.linkedin.com/in/crutcher-dunnavant-4841ba9) · [crutcher.github.io](https://crutcher.github.io)

## Summary

Systems engineer who designs and leads the infrastructure rebuilds companies get acquired on. Three startups — 3Scan, Apprente, and Atmo — sold on top of data, model, and production platforms I architected and led; before that, ten years at Google including design and technical leadership of CiTC, the distributed development filesystem behind the monorepo. Currently a top-5 contributor to the Burn Rust GPU tensor framework and maintainer of `bunsen`, the batteries-included model library for Burn (pretrained language, speech, and vision models on \~60 modular blocks). Two decades across HPC tensor systems, AI training stacks, real-time transaction systems, and large-scale dataflow, including 10+ years as tech lead and 5+ as engineering director with budget authority; doctoral-trained in distributed algorithms and type theory.

## Selected impact

- **Turned a demo into the product McDonald's acquired.** Led 8 engineers rebuilding Apprente's AI drive-through operator from prototype into a Kubernetes queue-stream production system with telemetry, CI/CD, and release machinery; acquired by McDonald's, Sep 2019.
- **Made terabyte-scale microscopy tractable.** Designed and led 3Scan's cloud storage and compute platform for 40 TB 4D tensors, running 170 TB pipelines in \~20 minutes (2018); the data platform 3Scan carried into its merger with Strateos.
- **Rebuilt Atmo's entire AI stack and shipped it to governments.** Re-architected the model, data, and training stacks and designed the global→regional transformer coupling model behind production forecasts for several national customers, including the Philippines; Atmo was acquired by Vaisala for $70M plus up to $60M earn-out (announced Jun 2026).
- **Designed the filesystem Google develops on.** Designer, tech lead, and principal engineer of CiTC, serving millions of globally available workspaces and underpinning build-farm and code-review tooling (ACM CACM, 2016).
- **Top-5 contributor to Burn**, the Rust GPU tensor framework: 100+ merged PRs including GPU kernels, optimizer composition, and backend operations; author and maintainer of bunsen, its batteries-included model library: pretrained language, speech, and vision models over a framework of \~60 modular blocks.

## Experience

### Independent Rust / AI Research · Feb 2025 – present

*Open-source infrastructure for the Burn Rust GPU tensor ecosystem, and ongoing research on distributed tensor expression optimization.*

**Built and maintain the community standard library for Burn, while ranking among Burn's top-5 contributors.**

- **[bunsen](https://github.com/zspacelabs/bunsen) — author and maintainer.** Batteries-included model library for Burn: an extensible core foundation, with extensions providing built-in loading and inference for pretrained models across language (Qwen, Gemma, NanoChat), speech — ASR (Parakeet, Voxtral, Whisper, Qwen3-ASR, Sortformer), TTS (Qwen3-TTS, Zonos3), VAD (Silero) — decision models (Laya), and image classification (ResNet, Swin V2), with tokenization via my wordchipper crate; built on a framework of \~60 modular combinator blocks, with runtime shape contracts and columnar dataloaders
- **[Burn](https://github.com/tracel-ai/burn) — core contributor.** 100+ merged PRs, top-5 contributor on burn.dev (Feb 2025 – Sep 2026): wrote and maintain the CubeCL GPU `unfold` kernel; `unfold` and `repeat_interleave` across the ndarray and candle backends; `GroupOptimizerAdaptor` for composite optimizers (Muon + AdamW on separate parameter groups) and `LrSchedulerMap`; nanochat port at f16
- **[Tapestry](https://github.com/crutcher/tapestry) — ongoing research.** A polyhedral calculus for distributed tensor expressions: affine index-projection signatures give mechanical sharding derivations under a strict-equivalence contract, continuing the 3Scan distributed-tensor work. Research stage; not yet externally usable

### Atmo — Principal Engineer · 2024 – 2025

*Regional AI weather forecasting: global low-resolution forecasts (NOAA GFS) → high-resolution 72-hour local forecasts; TIME Best Inventions 2024. Acquired by Vaisala, Jun 2026 ([release](https://www.vaisala.com/en/stock-exchange-releases/2026-06/inside-information-vaisala-acquires-ai-weather-company-atmo-inc-lead-transformation-meteorology)).*

**Rebuilt the full AI stack and shipped production forecasts to national governments.**

- Designed the AI coupling model: Swin-style volumetric temporal-causal transformers linking the global boundary region to the local high-resolution domain
- Re-architected the model stack (unit-tested, contract-programmed), the data load/transform stack, and the training stack end to end; designed and extended the metric and loss surfaces
- Tuned and delivered production models for several governments, including the Philippines
- Rebuilt the web map frontend for an NDA-covered contract after the FE engineer left, in a non-GPU rendering path so it ran inside clients' VMs

### OpenAI — Research Acceleration · 2023

**Cut research-branch divergence and unblocked RDMA for PyTorch.**

- Wrote new C/C++/nanobind/Python bindings for NVIDIA libverbs RDMA, working around limits in existing PyTorch RDMA libraries
- Reduced research-branch divergence from main (then \~7 months in many projects) by unifying shared libraries and stabilizing core code

### Meta — AI, several roles · 2021 – 2022

**Rebuilt the first-pass fast-scorer serving Facebook and Instagram.**

- Rebuilt the primary first-pass ranking fast-scorer for the next-gen AI training stack serving ranking across Facebook and Instagram, and fixed numerous architecture bugs in that stack
- Auto-tuning of the AI model stack; Ray-Ban Glasses video-interest model for summary clips; next-gen LLM chat model; PyTorch group

### Apprente / McDonald's Tech Labs — Infrastructure Director & Principal · 2018 – 2020

*Voice-AI startup; acquired by McDonald's as its AI drive-through operator ([TechCrunch, 2019-09-10](https://techcrunch.com/2019/09/10/mcdonalds-acquires-apprente/)).*

**Turned a demo AI into the production system McDonald's acquired.**

- Led 8 engineers redesigning the system as a Kubernetes queue stream: sound capture → phoneme models → action models → action state machine
- Built the telemetry collection framework, backend stats analysis, and distributed-queue event debugging tooling
- Owned build environment, CI pipeline, packaging, and release machinery

### 3Scan — Infrastructure Lead · 2016 – 2018

*Robotic microtome microscopy producing terabytes per tissue sample; merged into Strateos.*

**Made terabyte-scale 4D tensor microscopy data storable, addressable, and computable.**

- Designed and led the cloud storage and processing framework for upload, storage, random access, and tensor convolution over 40 TB 4D tensors
- Ran 170 TB pipelines in \~20 minutes (2018)
- Seeded the distributed tensor expression theory later developed as Tapestry

### Google — Software Engineer, four roles · 2005 – 2015

**AI Research (Kurzweil group).** Researcher on the Knowledge Graph anomaly-detector auto-trainer: thousands of topic models bootstrapped by uncertainty-curve mining and evolved as Sum/Product networks in a distributed Pareto space. Authored FineNum, a log-space C++ numeric library still in heavy use.

**CiTC (Clients in the Cloud) — designer, tech lead, principal engineer.** Designed the distributed development filesystem for Google's monorepo: millions of globally available workspaces; the substrate for desktop/web development, remote build-farm tooling, and code review (ACM CACM 2016, "Why Google Stores Billions of Lines of Code in a Single Repository").

**Google Health.** Backend/data semantics for health-record interchange (Continuity of Care Document standards); represented Google Health at standards conferences.

**Content Ads Production/Scaling.** Key engineer in migrating content ads to Borg; built core scaling rules, telemetry reporting, and a production test-cascade framework.

### Red Hat — Core OS Developer · 2000 – 2001

One of \~8 core OS developers on Red Hat Linux: packaged and maintained \~60 RPM packages with upstream coordination; built OS configuration automation for remote management.

## Education

- M.S. Computer Science, University of Alabama, 2004; doctoral work (ABD), 2004–2005
- B.S. Computer Science, University of Alabama, 2002

## Skills

**Languages:** Rust, Python, C++, C, Java, TypeScript, Haskell · **ML systems:** PyTorch internals, Burn, TensorFlow, CUDA kernels, RDMA, training-stack and loss/metric design, transformers · **Distributed systems:** Kubernetes, Borg, MapReduce, Paxos, Bigtable, queue-stream and real-time transaction architectures, distributed filesystems, terabyte-scale tensor storage · **Systems:** Linux kernel contributions, RPM, low-level OS and networking · **Theory:** distributed algorithms, transaction theory, type theory, polyhedral/affine index analysis, formal language and DSL design
