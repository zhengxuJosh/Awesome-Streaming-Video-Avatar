# Awesome Video-Based Streaming Avatar Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of papers, projects, and resources for **video-based streaming** and **real-time interactive avatar generation**.

This repository focuses on recent advances in making **video diffusion models** and **autoregressive video generation architectures** more **causal**, **streamable**, and suitable for **real-time full-duplex interaction**, with an emphasis on the 2024–2026 wave of progress.

> Contributions are welcome. Please read the [Contributing](#contributing) section before submitting a pull request.

---

## Badges

![Coverage](https://img.shields.io/badge/coverage-2024--2026-blue?style=flat-square)
![Topic](https://img.shields.io/badge/topic-streaming%20avatars-0A66C2?style=flat-square)
![Focus](https://img.shields.io/badge/focus-real--time%20interactive-success?style=flat-square)
![Maintenance](https://img.shields.io/badge/status-actively%20curated-brightgreen?style=flat-square)

### Tag Legend

- ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
- ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
- ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
- ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
- ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
- ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
- ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
- ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)

---

## Table of Contents

- [Surveys \& Benchmarks](#surveys--benchmarks)
- [Causal Video Generation \& Streaming Architecture](#causal-video-generation--streaming-architecture)
- [Real-Time \& Streaming Talking Head Generation](#real-time--streaming-talking-head-generation)
- [Interactive \& Full-Duplex Conversational Avatars](#interactive--full-duplex-conversational-avatars)
- [Contributing](#contributing)
- [License](#license)

---

## Surveys & Benchmarks

- **Talking-Head Generation in Practice**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)  
  *ACM TheWebConf Workshop 2026*  
  A comprehensive longitudinal analysis of over 100 influential works from 2021 to 2025, highlighting the field’s shift toward semantic alignment, temporal coherence, and the need for rigorous benchmarks for real-time systems.

- **A Survey of Interactive Generative Video**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)  
  *arXiv 2025.04*  
  A modular survey of interactive generative video systems, covering generation, control, and dynamics, with applications to embodied AI, gaming, and beyond.

---

## Causal Video Generation & Streaming Architecture

- **Causal Forcing** · *arXiv 2026.02* · [Project / Code](https://thu-ml.github.io/CausalForcing.github.io/)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/thu-ml/CausalForcing?style=flat-square)  
  Autoregressive diffusion distillation for real-time streaming on a single GPU.

- **SoulX-LiveAct** · *arXiv 2026.03* · [Code](https://github.com/Soul-AILab/SoulX-LiveAct)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/Soul-AILab/SoulX-LiveAct?style=flat-square)  
  Hour-scale animation using Neighbor Forcing + ConvKV memory, achieving 20 FPS real-time inference.

- **EchoTorrent** · *arXiv 2026.02* · [Code](https://github.com/antgroup/echomimic_v3)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/antgroup/echomimic_v3?style=flat-square)  
  Multi-modal streaming video generation with Multi-Teacher Training and Hybrid Long Tail Forcing.

- **Towards One-step Causal Video Generation via Adversarial Self-Distillation** · *arXiv 2025.11*  
  Aligns student model's n-step denoising output with (n+1)-step for high-quality synthesis with minimal steps.

- **High-Fidelity Causal Video Diffusion Models** · *arXiv 2026.02*  
  Supports causal synthesis under ultra-low bitrate conditions.

---

## Real-Time & Streaming Talking Head Generation

- **StreamAvatar** · *CVPR 2026* · [Project](https://streamavatar.github.io)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/streamavatar/streamavatar?style=flat-square)  
  Converts high-fidelity non-causal diffusion models into streaming architectures.

- **Live Avatar** · *arXiv 2025.12*  
  14B-parameter audio-driven avatar generation at 20 FPS end-to-end.

- **REST** · *arXiv 2025.12*  
  Real-time audio-driven talking head diffusion on a single GPU using ID-Context Cache.

- **PersonaLive!** · *CVPR 2026* · [Code](https://github.com/GVCLab/PersonaLive)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/GVCLab/PersonaLive?style=flat-square)  
  Micro-chunk streaming, 22× faster portrait animation.

- **Knot Forcing** · *arXiv 2025.12* · [Code](https://github.com/HumanAIGC)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/HumanAIGC/KnotForcing?style=flat-square)  
  Infinite-sequence interactive portrait animation on consumer GPUs.

- **LLIA** · *arXiv 2025.06* · [Project](https://meigen-ai.github.io/llia/)  
  Low-latency INT8 quantized avatars, 78 FPS.

---

## Interactive & Full-Duplex Conversational Avatars

- **LPM 1.0** · *arXiv 2026.04* · [Project](https://large-performance-model.github.io)  
  17B-parameter full-duplex conversational avatar system.

- **EmbodiedHead** · *arXiv 2026.04*  
  Single-stream listening-speaking interface with differentiable renderer.

- **Avatar Forcing** · *CVPR 2026* · [Code](https://github.com/TaekyungKi/AvatarForcing)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/TaekyungKi/AvatarForcing?style=flat-square)  
  Diffusion forcing + Direct Preference Optimization for expressive avatar reactions.

- **ARIG** · *ICCV 2025* · [Project](https://jinyugy21.github.io/ARIG/)  
  Autoregressive interactive head generation with deep CSU module.

---

## Contributing

- Add resources relevant to video-based streaming avatars.  
- Prefer official project pages, paper links, and code repositories.  
- Keep entries concise.  
- Follow the existing table format.  
- Avoid duplicates.  
- For major additions, include title, venue/year, links, and a short summary.

[Awesome guidelines](https://github.com/sindresorhus/awesome/blob/main/awesome.md)

---

## License

MIT License. See [LICENSE](LICENSE).

---

## Acknowledgement

Curated for researchers and practitioners in:

- streaming video generation  
- real-time talking head synthesis  
- interactive avatar systems  
- full-duplex conversational agents  
- causal video modeling
