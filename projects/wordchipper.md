---
title: wordchipper
layout: default
permalink: /projects/rust/llms/wordchipper/
---
# wordchipper

[wordchipper][wc.repo] is a high-performance rust BPE tokenizer trainer/encoder/decoder.

- [wordchipper crate][wc.crate]
- [wordchipper repo][wc.repo]
- [wordchipper docs][wc.docs]

## Encode/Decode Side-by-Side Benchmarks

| Model         | wordchipper  | tiktoken-rs  | tokenizers  |
|---------------|--------------|--------------|-------------|
| r50k_base     | 239.19 MiB/s | 169.30 MiB/s | 22.03 MiB/s |
| p50k_base     | 250.55 MiB/s | 163.07 MiB/s | 22.23 MiB/s |
| p50k_edit     | 241.69 MiB/s | 169.76 MiB/s | 21.27 MiB/s |
| cl100k_base   | 214.26 MiB/s | 125.43 MiB/s | 21.62 MiB/s |
| o200k_base    | 119.49 MiB/s | 123.75 MiB/s | 22.03 MiB/s |
| o200k_harmony | 121.80 MiB/s | 121.54 MiB/s | 22.08 MiB/s |

* *Help?* - I'm assuming some bug on my part for `tokenizers` + `rayon`.
* Methodology; 90MB shards of 1024 samples each, 48 threads.

```terminaloutput
$ for m in openai/{r50k_base,p50k_base,p50k_edit,cl100k_base,o200k_base,o200k_harmony}; \
  do RAYON_NUM_THREADS=48 cargo run --release -p sample-timer -- \
   --dataset-dir $DATASET_DIR --shards 0 --model $m; done
```

[wc.repo]: https://github.com/crutcher/wordchipper
[wc.crate]: https://crates.io/crates/wordchipper
[wc.docs]: https://docs.rs/wordchipper/latest/wordchipper/
