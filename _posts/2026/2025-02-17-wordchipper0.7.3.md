---
layout: post
title: "wordchipper 0.7.3"
date: 2026-02-17 18:30:00 -0800
---

Announcing: [wordchipper 0.7.3](https://crates.io/crates/wordchipper)
- much work on docs / interface unification.
- 2x `tiktoken-rs` speed on non-harmony models (it's the nasty regex)

This is a high-performance rust BPE tokenizer trainer/encoder/decoder.

This is ready for alpha users, and is 2x the speed of `tiktoken-rs`
for many current models.

The productionization towards an LTR stable release can be
tracked in the
[Alpha Release Tracking Issue](https://github.com/crutcher/wordchipper/issues/2).

| Model         | wordchipper   | tiktoken-rs   | tokenizers   |
|---------------|---------------|---------------|--------------|
| r50k_base     | 239.19 MiB/s  | 169.30 MiB/s  | 22.03 MiB/s  |
| p50k_base     | 250.55 MiB/s  | 163.07 MiB/s  | 22.23 MiB/s  |
| p50k_edit     | 241.69 MiB/s  | 169.76 MiB/s  | 21.27 MiB/s  |
| cl100k_base   | 214.26 MiB/s  | 125.43 MiB/s  | 21.62 MiB/s  |
| o200k_base    | 119.49 MiB/s  | 123.75 MiB/s  | 22.03 MiB/s  |
| o200k_harmony | 121.80 MiB/s  | 121.54 MiB/s  | 22.08 MiB/s  |

Loading pre-trained models:
```rust
use std::sync::Arc;

use wordchipper::{
    get_model,
    TokenDecoder,
    TokenEncoder,
    UnifiedTokenVocab,
    disk_cache::WordchipperDiskCache,
};

fn example() -> anyhow::Result<(
        Arc<dyn TokenEncoder<u32>>,
        Arc<dyn TokenDecoder<u32>>
)> {
    let mut disk_cache = WordchipperDiskCache::default();
    let vocab: UnifiedTokenVocab<u32> =
        get_model("openai/o200k_harmony", &mut disk_cache)?;
    let encoder = vocab.to_default_encoder();
    let decoder = vocab.to_default_decoder();
    Ok((encoder, decoder))
}
```
