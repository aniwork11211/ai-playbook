# Colibri

Source: JustVugg, posted by @fullstackparody. A pure-C inference engine for Mixture-of-Experts models. Repo: `github.com/JustVugg/colibri`. Apache 2.0. The post shows about 37.8k stars. No dependencies. It builds with gcc or clang and OpenMP. Prebuilt releases exist too.

Use this file when the work is running a large MoE model on a machine you already have. Open it from `C:\Users\ANISH\Documents\ai-playbook\LIBRARY.md`.

It runs on a laptop or a workstation. The claim on the slides is a 744B model on the laptop, and nine families from a 35B Qwen up to Kimi K3 at 2.8 trillion parameters, on as little as 8 to 16 GB of RAM. CPU-only works.

## How it fits

Disk, RAM, and VRAM are one memory pool. Only the routed experts are streamed from disk, so the whole model does not have to sit in memory.

The slide’s example is `glm-5.2-744b`, 61 layers, 256 experts, 8 active. That panel shows 12,448 routed tokens, 420 MB read from disk, 28.4 tokens per second, 6.2 GB of 24 GB VRAM, 14.8 GB of 64 GB RAM, and 312 GB of experts on a 1.2 TB disk. Those figures are the example on the slide.

## Setup

```
git clone https://github.com/JustVugg/colibri
cd colibri/c
./setup.sh
COLI_MODEL=/path/to/model ./coli chat
```

`./coli list-models` prints the families. `./coli chat` loads metadata and streams experts from disk. Ctrl+C exits.

## Nine families

| Model | Params | Type |
| --- | --- | --- |
| GLM-5.2-744B | 744B | MoE |
| DeepSeek-V4 | 671B | MoE |
| Qwen3.6-35B | 35B | Dense |
| Kimi-K3 | 2.8T | MoE |
| Qwen3-235B | 235B | MoE |
| Llama-4-Scout | 109B | MoE |
| Mistral-Large | 123B | MoE |
| Mixtral-8x22B | 176B | MoE |
| DeepSeek-V3 | 671B | MoE |
