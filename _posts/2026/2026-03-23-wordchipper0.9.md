---
layout: post
title:  "Wordchipper 0.9: Fastest Gun in the West"
date:   2026-03-23 09:00:00 -0800
---

[`wordchipper`](https://github.com/zspacelabs/wordchipper/) 0.9 is out!

`wordchipper` is a high-performance Rust byte-pair encoder tokenizer for the OpenAI GPT-2 tokenizer family.
With throughput speedups relative to [tiktoken-rs](https://github.com/zurawiki/tiktoken-rs) in rust on a 64 core machine of ~4.3-5.7x
(4 to 64 cores) for general regex BPE vocabularies, and ~6.9x-9.2x when using custom DFA lexers for specific OpenAI
vocabularies. Under python wrappers, we see a range of ~2x-4x (4 to 64 cores) speedups
over [tiktoken](https://github.com/openai/tiktoken).

We're publishing a paper on this work:

* [wordchipper: Fast BPE Tokenization with Substitutable Internals](https://zspacelabs.ai/wordchipper/articles/substitutable/)
