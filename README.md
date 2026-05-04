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

- **Advancements in Talking Head Generation: A Comprehensive Review of Techniques, Metrics, and Challenges**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)
  ![Evaluation](https://img.shields.io/badge/-Evaluation-0ea5e9?style=flat-square)  
  *The Visual Computer 2026 / Published 2025.12*  
  A systematic review of talking-head generation methods, metrics, and open challenges, covering 2D, 3D, NeRF, diffusion, and real-time-oriented approaches with emphasis on realism, identity preservation, motion accuracy, and temporal smoothness.  
  [Paper](https://link.springer.com/article/10.1007/s00371-025-04232-w)

- **THEval: Evaluation Framework for Talking Head Video Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)
  ![Human Alignment](https://img.shields.io/badge/-Human%20Alignment-10b981?style=flat-square)  
  *arXiv 2025.11*  
  A dedicated talking-head evaluation framework with 8 metrics across quality, naturalness, and synchronization, evaluated on 85,000 videos from 17 state-of-the-art models to better align automatic scores with human preference.  
  [Paper](https://arxiv.org/abs/2511.04520)

- **TalkVid: A Large-Scale Diversified Dataset for Audio-Driven Talking Head Synthesis**  
  ![Dataset](https://img.shields.io/badge/-Dataset-2563eb?style=flat-square)
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  *arXiv 2025.08*  
  Introduces TalkVid and TalkVid-Bench, a 500-clip stratified benchmark balanced across demographic and linguistic axes, designed to expose fairness, robustness, and cross-domain generalization gaps in audio-driven talking-head synthesis.  
  [Paper](https://arxiv.org/html/2508.13618v1)

- **TalkingHeadBench: A Multi-Modal Benchmark & Analysis of Talking-Head DeepFake Detection**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)
  ![Deepfake Detection](https://img.shields.io/badge/-Deepfake%20Detection-dc2626?style=flat-square)  
  *WACV 2026*  
  A curated multi-generator benchmark for modern talking-head deepfake detection, focusing on detector robustness under identity and generator distribution shifts, with analysis across CNN, ViT, and temporal detectors.  
  [Paper](https://arxiv.org/abs/2505.24866)

- **What Comprises a Good Talking-Head Video Generation?: A Survey and Benchmark**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  *arXiv 2020.05*  
  A foundational benchmark for talking-head video generation, proposing standardized preprocessing and evaluation around identity preservation, lip synchronization, video quality, and natural spontaneous motion.  
  [Paper](https://arxiv.org/abs/2005.03201)

- **A Survey of AI-Generated Video Evaluation**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Video Generation](https://img.shields.io/badge/-Video%20Generation-64748b?style=flat-square)
  ![Evaluation](https://img.shields.io/badge/-Evaluation-0ea5e9?style=flat-square)  
  *arXiv 2024.10 / Revised 2026.03*  
  A broad survey of AI-generated video evaluation, organizing metric-based, human-involved, and model-centered evaluation methods around video quality, semantic delivery, human-intent alignment, and physical-world consistency.  
  [Paper](https://arxiv.org/abs/2410.19884)

- **A Survey: Spatiotemporal Consistency in Video Generation**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Temporal Coherence](https://img.shields.io/badge/-Temporal%20Coherence-14b8a6?style=flat-square)
  ![Video Generation](https://img.shields.io/badge/-Video%20Generation-64748b?style=flat-square)  
  *arXiv 2025.02 / Revised 2026.02*  
  A focused survey on spatiotemporal consistency in video generation, covering foundation models, representations, generation schemes, post-processing, training strategies, benchmarks, and evaluation metrics.  
  [Paper](https://arxiv.org/abs/2502.17863)

- **VBench: Comprehensive Benchmark Suite for Video Generative Models**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Video Generation](https://img.shields.io/badge/-Video%20Generation-64748b?style=flat-square)
  ![Human Alignment](https://img.shields.io/badge/-Human%20Alignment-10b981?style=flat-square)  
  *CVPR 2024*  
  A widely used fine-grained benchmark that decomposes video generation quality into 16 dimensions, including subject consistency, motion smoothness, temporal flickering, and spatial relationships, with human preference annotations for validation.  
  [Paper](https://arxiv.org/abs/2311.17982)

- **VBench++: Comprehensive and Versatile Benchmark Suite for Video Generative Models**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Text-to-Video](https://img.shields.io/badge/-Text--to--Video-f59e0b?style=flat-square)
  ![Image-to-Video](https://img.shields.io/badge/-Image--to--Video-2563eb?style=flat-square)  
  *arXiv 2024.11 / TPAMI 2025*  
  An extension of VBench that supports both text-to-video and image-to-video evaluation, adding adaptive image suites and broader trustworthiness-oriented evaluation for video generative models.  
  [Paper](https://arxiv.org/abs/2411.13503)

- **VBench-2.0: Advancing Video Generation Benchmark Suite for Intrinsic Faithfulness**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Physics](https://img.shields.io/badge/-Physics-ef4444?style=flat-square)
  ![Commonsense](https://img.shields.io/badge/-Commonsense-8b5cf6?style=flat-square)  
  *arXiv 2025.03*  
  A next-generation VBench benchmark targeting intrinsic faithfulness, evaluating whether generated videos obey human fidelity, controllability, creativity, physics, and commonsense constraints rather than only looking visually plausible.  
  [Paper](https://arxiv.org/abs/2503.21755)

- **Video-Bench: Human-Aligned Video Generation Benchmark**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![MLLM Evaluation](https://img.shields.io/badge/-MLLM%20Evaluation-9333ea?style=flat-square)
  ![Human Alignment](https://img.shields.io/badge/-Human%20Alignment-10b981?style=flat-square)  
  *CVPR 2025*  
  A human-aligned video generation benchmark that uses MLLM-based evaluation, few-shot scoring, and chain-of-query techniques to assess video-condition alignment and video quality across modern generators.  
  [Paper](https://arxiv.org/abs/2504.04907)

- **EvalCrafter: Benchmarking and Evaluating Large Video Generation Models**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Text-to-Video](https://img.shields.io/badge/-Text--to--Video-f59e0b?style=flat-square)
  ![Leaderboard](https://img.shields.io/badge/-Leaderboard-0ea5e9?style=flat-square)  
  *CVPR 2024*  
  A comprehensive T2V evaluation pipeline using 700 prompts and 17 objective metrics across visual quality, content quality, motion quality, and text-video alignment, with human-aligned coefficient fitting for final ranking.  
  [Paper](https://arxiv.org/abs/2310.11440)

- **FETV: A Benchmark for Fine-Grained Evaluation of Open-Domain Text-to-Video Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Text-to-Video](https://img.shields.io/badge/-Text--to--Video-f59e0b?style=flat-square)
  ![Fine-Grained](https://img.shields.io/badge/-Fine--Grained-06b6d4?style=flat-square)  
  *NeurIPS 2023 Datasets & Benchmarks*  
  A temporally aware benchmark for open-domain T2V generation, categorizing prompts by major content, attribute control, prompt complexity, and temporal categories, while also testing the reliability of automatic metrics against human evaluation.  
  [Paper](https://arxiv.org/abs/2311.01813)

- **T2V-CompBench: A Comprehensive Benchmark for Compositional Text-to-Video Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Compositionality](https://img.shields.io/badge/-Compositionality-ec4899?style=flat-square)
  ![Text-to-Video](https://img.shields.io/badge/-Text--to--Video-f59e0b?style=flat-square)  
  *CVPR 2025*  
  A benchmark for compositional T2V generation, covering attribute binding, spatial relationships, motion binding, action binding, object interaction, and numeracy with MLLM-, detection-, and tracking-based metrics.  
  [Paper](https://arxiv.org/abs/2407.14505)

- **GenAI-Bench: Evaluating and Improving Compositional Text-to-Visual Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Text-to-Visual](https://img.shields.io/badge/-Text--to--Visual-64748b?style=flat-square)
  ![Compositionality](https://img.shields.io/badge/-Compositionality-ec4899?style=flat-square)  
  *arXiv 2024.06*  
  A compositional text-to-visual benchmark for both image and video generation, targeting attributes, relationships, counting, comparison, differentiation, and logic, with large-scale human ratings and VQAScore-based evaluation.  
  [Paper](https://arxiv.org/abs/2406.13743)

- **AIGVE-Tool: AI-Generated Video Evaluation Toolkit with Multifaceted Benchmark**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Toolkit](https://img.shields.io/badge/-Toolkit-334155?style=flat-square)
  ![Evaluation](https://img.shields.io/badge/-Evaluation-0ea5e9?style=flat-square)  
  *VISAPP 2026 / arXiv 2025.03*  
  A unified toolkit and benchmark for AI-generated video evaluation, organizing metrics under a five-category taxonomy and proposing AIGVE-Bench across nine quality dimensions using videos from five SOTA generators.  
  [Paper](https://arxiv.org/abs/2503.14064)

- **PhyGenBench: Crafting Physical Commonsense-Based Benchmark for Video Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Physics](https://img.shields.io/badge/-Physics-ef4444?style=flat-square)
  ![World Model](https://img.shields.io/badge/-World%20Model-8b5cf6?style=flat-square)  
  *arXiv 2024.10*  
  A physics-focused benchmark for T2V world-simulator evaluation, using 160 prompts across 27 physical laws and four physical domains, paired with PhyGenEval for automated physical commonsense assessment.  
  [Paper](https://arxiv.org/abs/2410.05363)

- **VideoPhy-2: A Challenging Action-Centric Physical Commonsense Evaluation in Video Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Physics](https://img.shields.io/badge/-Physics-ef4444?style=flat-square)
  ![Action-Centric](https://img.shields.io/badge/-Action--Centric-0ea5e9?style=flat-square)  
  *arXiv 2025.03*  
  An action-centric physical commonsense benchmark for video generation, using diverse real-world actions and human evaluation to test semantic adherence, physical rule grounding, and failure modes such as conservation-law violations.  
  [Paper](https://arxiv.org/abs/2503.06800)

- **WorldModelBench: Judging Video Generation Models as World Models**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![World Model](https://img.shields.io/badge/-World%20Model-8b5cf6?style=flat-square)
  ![Physical Adherence](https://img.shields.io/badge/-Physical%20Adherence-ef4444?style=flat-square)  
  *arXiv 2025.02*  
  A benchmark for judging video generators as world models, focusing on instruction following, commonsense, and physics adherence with large-scale human labels and an automated judge for world-modeling violations.  
  [Paper](https://arxiv.org/abs/2502.20694)

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
