# Awesome Video Based Streaming Avatar Generation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

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

- **Advancements in Talking Head Generation: A Comprehensive Review of Techniques, Metrics, and Challenges**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)
  ![Evaluation](https://img.shields.io/badge/-Evaluation-0ea5e9?style=flat-square)  
  *The Visual Computer 2026 / Published 2025.12*  
  A systematic review of talking-head generation methods, metrics, and open challenges, covering 2D, 3D, NeRF, diffusion, and real-time-oriented approaches with emphasis on realism, identity preservation, motion accuracy, and temporal smoothness.  
  [Paper](https://link.springer.com/article/10.1007/s00371-025-04232-w)

- **TalkingHeadBench: A Multi-Modal Benchmark & Analysis of Talking-Head DeepFake Detection**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)
  ![Deepfake Detection](https://img.shields.io/badge/-Deepfake%20Detection-dc2626?style=flat-square)  
  *WACV 2026*  
  A curated multi-generator benchmark for modern talking-head deepfake detection, focusing on detector robustness under identity and generator distribution shifts, with analysis across CNN, ViT, and temporal detectors.  
  [Paper](https://arxiv.org/abs/2505.24866)

- **AIGVE-Tool: AI-Generated Video Evaluation Toolkit with Multifaceted Benchmark**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Toolkit](https://img.shields.io/badge/-Toolkit-334155?style=flat-square)
  ![Evaluation](https://img.shields.io/badge/-Evaluation-0ea5e9?style=flat-square)  
  *VISAPP 2026 / arXiv 2025.03*  
  A unified toolkit and benchmark for AI-generated video evaluation, organizing metrics under a five-category taxonomy and proposing AIGVE-Bench across nine quality dimensions using videos from five SOTA generators.  
  [Paper](https://arxiv.org/abs/2503.14064)

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

- **A Survey of Interactive Generative Video**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)  
  *arXiv 2025.04*  
  A modular survey of interactive generative video systems, covering generation, control, and dynamics, with applications to embodied AI, gaming, and beyond.

- **Video-Bench: Human-Aligned Video Generation Benchmark**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![MLLM Evaluation](https://img.shields.io/badge/-MLLM%20Evaluation-9333ea?style=flat-square)
  ![Human Alignment](https://img.shields.io/badge/-Human%20Alignment-10b981?style=flat-square)  
  *CVPR 2025*  
  A human-aligned video generation benchmark that uses MLLM-based evaluation, few-shot scoring, and chain-of-query techniques to assess video-condition alignment and video quality across modern generators.  
  [Paper](https://arxiv.org/abs/2504.04907)

- **T2V-CompBench: A Comprehensive Benchmark for Compositional Text-to-Video Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Compositionality](https://img.shields.io/badge/-Compositionality-ec4899?style=flat-square)
  ![Text-to-Video](https://img.shields.io/badge/-Text--to--Video-f59e0b?style=flat-square)  
  *CVPR 2025*  
  A benchmark for compositional T2V generation, covering attribute binding, spatial relationships, motion binding, action binding, object interaction, and numeracy with MLLM-, detection-, and tracking-based metrics.  
  [Paper](https://arxiv.org/abs/2407.14505)

- **VBench-2.0: Advancing Video Generation Benchmark Suite for Intrinsic Faithfulness**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Physics](https://img.shields.io/badge/-Physics-ef4444?style=flat-square)
  ![Commonsense](https://img.shields.io/badge/-Commonsense-8b5cf6?style=flat-square)  
  *arXiv 2025.03*  
  A next-generation VBench benchmark targeting intrinsic faithfulness, evaluating whether generated videos obey human fidelity, controllability, creativity, physics, and commonsense constraints rather than only looking visually plausible.  
  [Paper](https://arxiv.org/abs/2503.21755)

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

- **VBench++: Comprehensive and Versatile Benchmark Suite for Video Generative Models**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Text-to-Video](https://img.shields.io/badge/-Text--to--Video-f59e0b?style=flat-square)
  ![Image-to-Video](https://img.shields.io/badge/-Image--to--Video-2563eb?style=flat-square)  
  *arXiv 2024.11 / TPAMI 2025*  
  An extension of VBench that supports both text-to-video and image-to-video evaluation, adding adaptive image suites and broader trustworthiness-oriented evaluation for video generative models.  
  [Paper](https://arxiv.org/abs/2411.13503)

- **PhyGenBench: Crafting Physical Commonsense-Based Benchmark for Video Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Physics](https://img.shields.io/badge/-Physics-ef4444?style=flat-square)
  ![World Model](https://img.shields.io/badge/-World%20Model-8b5cf6?style=flat-square)  
  *arXiv 2024.10*  
  A physics-focused benchmark for T2V world-simulator evaluation, using 160 prompts across 27 physical laws and four physical domains, paired with PhyGenEval for automated physical commonsense assessment.  
  [Paper](https://arxiv.org/abs/2410.05363)

- **GenAI-Bench: Evaluating and Improving Compositional Text-to-Visual Generation**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Text-to-Visual](https://img.shields.io/badge/-Text--to--Visual-64748b?style=flat-square)
  ![Compositionality](https://img.shields.io/badge/-Compositionality-ec4899?style=flat-square)  
  *arXiv 2024.06*  
  A compositional text-to-visual benchmark for both image and video generation, targeting attributes, relationships, counting, comparison, differentiation, and logic, with large-scale human ratings and VQAScore-based evaluation.  
  [Paper](https://arxiv.org/abs/2406.13743)

- **VBench: Comprehensive Benchmark Suite for Video Generative Models**  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Video Generation](https://img.shields.io/badge/-Video%20Generation-64748b?style=flat-square)
  ![Human Alignment](https://img.shields.io/badge/-Human%20Alignment-10b981?style=flat-square)  
  *CVPR 2024*  
  A widely used fine-grained benchmark that decomposes video generation quality into 16 dimensions, including subject consistency, motion smoothness, temporal flickering, and spatial relationships, with human preference annotations for validation.  
  [Paper](https://arxiv.org/abs/2311.17982)

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

- **What Comprises a Good Talking-Head Video Generation?: A Survey and Benchmark**  
  ![Survey](https://img.shields.io/badge/-Survey-purple?style=flat-square)
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  *arXiv 2020.05*  
  A foundational benchmark for talking-head video generation, proposing standardized preprocessing and evaluation around identity preservation, lip synchronization, video quality, and natural spontaneous motion.  
  [Paper](https://arxiv.org/abs/2005.03201)

---

## Causal Video Generation & Streaming Architecture

- **Speculative Decoding for Autoregressive Video Generation** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.17397)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  Adapts speculative decoding to block-based autoregressive video diffusion with draft generation and verification for faster long-video synthesis.

- **Long-Horizon Streaming Video Generation via Hybrid Attention with Decoupled Distillation** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.10103)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  Hybrid attention and decoupled distillation framework for long-horizon streaming video generation with real-time throughput.

- **SoulX-LiveAct** · *arXiv 2026.03* · [Paper](https://arxiv.org/abs/2603.11746) · [Project](https://soul-ailab.github.io/soulx-liveact/) · [Code](https://github.com/Soul-AILab/SoulX-LiveAct)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/Soul-AILab/SoulX-LiveAct?style=flat-square)  
  Hour-scale real-time human animation using Neighbor Forcing and ConvKV Memory, supporting long-duration streaming inference.

- **Streaming Autoregressive Video Generation via Diagonal Distillation** · *arXiv 2026.03* · [Paper](https://arxiv.org/abs/2603.09488) · [Project](https://spherelab.ai/diagdistill/) · [Code](https://github.com/Sphere-AI-Lab/diagdistill)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/Sphere-AI-Lab/diagdistill?style=flat-square)  
  Introduces DiagDistill with diagonal denoising, diagonal forcing, and progressive step reduction for faster streaming AR video generation.

- **HiAR: Efficient Autoregressive Long Video Generation via Hierarchical Denoising** · *arXiv 2026.03* · [Paper](https://arxiv.org/abs/2603.08703) · [Project](https://jacky-hate.github.io/HiAR/) · [Code](https://github.com/Jacky-hate/HiAR)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![GitHub Repo stars](https://img.shields.io/github/stars/Jacky-hate/HiAR?style=flat-square)  
  Hierarchical denoising framework that conditions on matched-noise-level context to mitigate error propagation and support pipelined AR inference.

- **Helios: Real Real-Time Long Video Generation Model** · *arXiv 2026.03* · [Paper](https://arxiv.org/abs/2603.04379) · [Project](https://pku-yuangroup.github.io/Helios-Page/) · [Code](https://github.com/PKU-YuanGroup/Helios)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Long Video](https://img.shields.io/badge/-Long%20Video-8b5cf6?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/PKU-YuanGroup/Helios?style=flat-square)  
  A 14B autoregressive diffusion model for real-time minute-scale video generation, supporting unified T2V, I2V, and V2V generation with long-video robustness.

- **Train Short, Inference Long: Training-free Horizon Extension for Autoregressive Video Generation** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.14027) · [Project](https://ga-lee.github.io/FLEX_demo/)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  Proposes FLEX, a plug-and-play inference-time extension method using Frequency-aware RoPE Modulation, Antiphase Noise Sampling, and Attention Sink for long-horizon AR video generation.

- **High-Fidelity Causal Video Diffusion Models for Real-Time Ultra-Low-Bitrate Semantic Communication** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.13837)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  Supports causal, real-time video synthesis under ultra-low-bitrate semantic communication constraints via Semantic Control, Restoration Adapter, Temporal Adapter, and temporal distillation.

- **EchoTorrent** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.13669) · [Related Code](https://github.com/antgroup/echomimic_v3)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/antgroup/echomimic_v3?style=flat-square)  
  Multi-modal streaming video generation with Multi-Teacher Training, ACC-DMD, Hybrid Long Tail Forcing, and VAE Decoder Refiner.

- **FlowCache: Flow Caching for Autoregressive Video Generation** · *ICLR 2026 / arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.10825) · [Code](https://github.com/mikeallen39/FlowCache)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/mikeallen39/FlowCache?style=flat-square)  
  Chunkwise caching framework for AR video generation, combining adaptive recomputation policies with KV cache compression for real-time ultra-long synthesis.

- **Context Forcing: Consistent Autoregressive Video Generation with Long Context** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.06028) · [Project](https://chenshuo20.github.io/Context_Forcing/) · [Code](https://github.com/TIGER-AI-Lab/Context-Forcing)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/TIGER-AI-Lab/Context-Forcing?style=flat-square)  
  Aligns long-context students with long-context teachers and introduces Slow-Fast Memory to preserve global consistency in long AR video generation.

- **Pathwise Test-Time Correction for Autoregressive Long Video Generation** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.05871) · [Code](https://github.com/xbxsxp9/Pathwise_TTC)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/xbxsxp9/Pathwise_TTC?style=flat-square)  
  Training-free test-time correction that anchors intermediate stochastic states to the initial frame to suppress long-term drift in distilled AR diffusion models.

- **Light Forcing: Accelerating Autoregressive Video Diffusion via Sparse Attention** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.04789) · [Code](https://github.com/chengtao-lv/LightForcing)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/chengtao-lv/LightForcing?style=flat-square)  
  Sparse attention solution tailored for AR video diffusion, using Chunk-Aware Growth and Hierarchical Sparse Attention to improve quality-efficiency trade-offs.

- **Quant VideoGen: Auto-Regressive Long Video Generation via 2-Bit KV-Cache Quantization** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.02958)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  Reduces the memory footprint of long autoregressive video generation through 2-bit semantic-aware KV-cache quantization.

- **Causal Forcing** · *ICML 2026 / arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.02214) · [Project](https://thu-ml.github.io/CausalForcing.github.io/) · [Code](https://github.com/thu-ml/Causal-Forcing)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/thu-ml/Causal-Forcing?style=flat-square)  
  Autoregressive diffusion distillation for high-quality real-time interactive video generation, bridging the architectural gap between bidirectional teachers and causal AR students.

- **Past- and Future-Informed KV Cache Policy with Salience Estimation in Autoregressive Video Diffusion** · *arXiv 2026.01* · [Paper](https://arxiv.org/abs/2601.21896)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  Introduces PaFu-KV, a salience-aware KV cache policy distilled from a bidirectional teacher to retain informative tokens and reduce memory footprint during long-horizon generation.

- **LoL: Longer than Longer, Scaling Video Generation to Hour** · *arXiv 2026.01* · [Paper](https://arxiv.org/abs/2601.16914) · [Code](https://github.com/justincui03/LoL)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/justincui03/LoL?style=flat-square)  
  Tackles sink-collapse in autoregressive long-video generation with multi-head RoPE jitter, enabling hour-scale streaming generation with reduced quality decay.

- **VideoAR: Autoregressive Video Generation via Next-Frame & Scale Prediction** · *arXiv 2026.01* · [Paper](https://arxiv.org/abs/2601.05966)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  Autoregressive video generation framework that combines next-frame and multi-scale prediction for efficient causal video synthesis.

- **Vid2World: Crafting Video Diffusion Models to Interactive World Models** · *ICLR 2026* · [Paper](https://openreview.net/forum?id=pFyzqbUiF9) · [Code](https://github.com/thuml/Vid2World)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/thuml/Vid2World?style=flat-square)  
  Converts non-causal video diffusion backbones into autoregressive, temporally causal architectures with frame-level action conditioning for interactive world models.

- **Towards One-step Causal Video Generation via Adversarial Self-Distillation** · *arXiv 2025.11* · [Paper](https://arxiv.org/abs/2511.01419) · [Code](https://github.com/BigAandSmallq/SAD)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/BigAandSmallq/SAD?style=flat-square)  
  Adversarial Self-Distillation aligns a student model’s n-step and n+1-step outputs for stable one-step or few-step causal video synthesis.

- **Self-Forcing++: Towards Minute-Scale High-Quality Video Generation** · *arXiv 2025.10* · [Paper](https://arxiv.org/abs/2510.02283) · [Project](https://self-forcing-plus-plus.github.io/) · [Code](https://github.com/justincui03/Self-Forcing-Plus-Plus)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/justincui03/Self-Forcing-Plus-Plus?style=flat-square)  
  Extends Self Forcing to minute-scale long video generation through self-generated long rollouts and teacher correction on sampled local segments.

- **Rolling Forcing: Autoregressive Long Video Diffusion in Real Time** · *ICLR 2026 / arXiv 2025.09* · [Paper](https://arxiv.org/abs/2509.25161) · [Project](https://kunhao-liu.github.io/Rolling_Forcing_Webpage/) · [Code](https://github.com/TencentARC/RollingForcing)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/TencentARC/RollingForcing?style=flat-square)  
  Uses rolling-window joint denoising, attention sinks, and self-generated histories to reduce long-horizon drift in real-time streaming video generation.

- **LongLive: Real-time Interactive Long Video Generation** · *ICLR 2026 / arXiv 2025.09* · [Paper](https://arxiv.org/abs/2509.22622) · [Project](https://nvlabs.github.io/LongLive/) · [Code](https://github.com/NVlabs/LongLive)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/NVlabs/LongLive?style=flat-square)  
  Frame-level causal AR framework with KV-recache, streaming long tuning, short-window attention, and frame sinks for real-time interactive long-video generation.

- **Self Forcing: Bridging the Train-Test Gap in Autoregressive Video Diffusion** · *arXiv 2025.06* · [Paper](https://arxiv.org/abs/2506.08009) · [Project](https://self-forcing.github.io/) · [Code](https://github.com/guandeh17/Self-Forcing)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/guandeh17/Self-Forcing?style=flat-square)  
  Trains AR video diffusion models by simulating inference-time rollouts with KV caching, reducing exposure bias for real-time streaming generation.

- **MAGI-1: Autoregressive Video Generation at Scale** · *arXiv 2025.05* · [Paper](https://arxiv.org/abs/2505.13211) · [Code](https://github.com/SandAI-org/MAGI-1)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/SandAI-org/MAGI-1?style=flat-square)  
  Scales AR video generation through chunk-wise prediction, monotonic per-chunk noise, causal temporal modeling, streaming generation, and constant peak inference cost.

- **SkyReels-V2: Infinite-Length Film Generative Model** · *arXiv 2025.04* · [Paper](https://arxiv.org/abs/2504.13074) · [Code](https://github.com/SkyworkAI/SkyReels-V2)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/SkyworkAI/SkyReels-V2?style=flat-square)  
  Open-source infinite-length film generation model using AutoRegressive Diffusion-Forcing architecture for long-form text-to-video and image-to-video generation.

- **History-Guided Video Diffusion** · *ICML 2025 / arXiv 2025.02* · [Paper](https://arxiv.org/abs/2502.06764) · [Project](https://www.boyuan.space/history-guidance/) · [Code](https://github.com/kwsong0113/diffusion-forcing-transformer)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/kwsong0113/diffusion-forcing-transformer?style=flat-square)  
  Introduces DFoT and History Guidance for variable-length history conditioning, improving temporal consistency, motion dynamics, and extremely long rollout stability.

- **CausVid / From Slow Bidirectional to Fast Autoregressive Video Diffusion Models** · *CVPR 2025 / arXiv 2024.12* · [Paper](https://arxiv.org/abs/2412.07772) · [Project](https://causvid.github.io/) · [Code](https://github.com/tianweiy/CausVid)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/tianweiy/CausVid?style=flat-square)  
  Distills a bidirectional video diffusion transformer into a fast autoregressive generator with causal attention, KV caching, and streaming inference.

- **ARLON: Boosting Diffusion Transformers with Autoregressive Models for Long Video Generation** · *ICLR 2025 / arXiv 2024.10* · [Paper](https://arxiv.org/abs/2410.20502) · [Project](https://www.microsoft.com/en-us/research/articles/efficiently-generating-long-high-quality-and-dynamic-videos-using-text-prompts/)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  Boosts diffusion transformers with AR-generated coarse spatial and long-range temporal guidance for efficient, dynamic, and temporally consistent long-video generation.

- **Diffusion Forcing: Next-token Prediction Meets Full-Sequence Diffusion** · *NeurIPS 2024 / arXiv 2024.07* · [Paper](https://arxiv.org/abs/2407.01392) · [Project](https://www.boyuan.space/diffusion-forcing/) · [Code](https://github.com/buoyancy99/diffusion-forcing)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/buoyancy99/diffusion-forcing?style=flat-square)  
  Foundational sequence-generation paradigm combining causal next-token prediction with full-sequence diffusion through independent per-token noise levels.

- **FIFO-Diffusion: Generating Infinite Videos from Text without Training** · *NeurIPS 2024 / arXiv 2024.05* · [Paper](https://arxiv.org/abs/2405.11473) · [Project](https://jjihwan.github.io/projects/FIFO-Diffusion/) · [Code](https://github.com/jjihwan/FIFO-Diffusion_public)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/jjihwan/FIFO-Diffusion_public?style=flat-square)  
  Training-free infinite video generation via first-in-first-out diagonal denoising, maintaining constant memory regardless of target video length.

- **StreamingT2V: Consistent, Dynamic, and Extendable Long Video Generation from Text** · *CVPR 2025 / arXiv 2024.03* · [Paper](https://arxiv.org/abs/2403.14773) · [Project](https://streamingt2v.github.io/) · [Code](https://github.com/Picsart-AI-Research/StreamingT2V)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/Picsart-AI-Research/StreamingT2V?style=flat-square)  
  Autoregressive long-video generation with short-term memory, long-term appearance preservation, and randomized blending for smooth chunk transitions.

---

## Real-Time & Streaming Talking Head Generation

- **Hallo-Live: Real-Time Streaming Joint Audio-Video Avatar Generation with Asynchronous Dual-Stream and Human-Centric Preference Distillation** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.23632) · [Code](https://github.com/fudan-generative-vision/Hallo-Live)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/fudan-generative-vision/Hallo-Live?style=flat-square)  
  Real-time joint audio-video avatar generation using asynchronous dual-stream diffusion, future-expanding attention, and human-centric preference-guided distillation.

- **TurboTalk: Progressive Distillation for One-Step Audio-Driven Talking Avatar Generation** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.14580)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Compresses multi-step audio-driven avatar diffusion into a one-step generator through progressive distillation for fast talking-avatar synthesis.

- **SoulX-FlashHead: Oracle-guided Generation of Infinite Real-time Streaming Talking Heads** · *arXiv 2026.02* · [Paper](https://arxiv.org/abs/2602.07449) · [Code](https://github.com/Soul-AILab/SoulX-FlashHead)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/Soul-AILab/SoulX-FlashHead?style=flat-square)  
  Oracle-guided 1.3B streaming portrait model with temporal audio context caching and bidirectional distillation for infinite real-time talking heads.

- **SoulX-FlashTalk: Real-Time Infinite Streaming of Audio-Driven Avatars via Self-Correcting Bidirectional Distillation** · *arXiv 2025.12* · [Paper](https://arxiv.org/abs/2512.23379) · [Project](https://soul-ailab.github.io/soulx-flashtalk/) · [Code](https://github.com/Soul-AILab/SoulX-FlashTalk)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/Soul-AILab/SoulX-FlashTalk?style=flat-square)  
  Real-time infinite audio-driven avatar generation with self-correcting bidirectional distillation and retrospective correction for long streaming stability.

- **REST: Diffusion-based Real-time End-to-end Streaming Talking Head Generation via ID-Context Caching and Asynchronous Streaming Distillation** · *arXiv 2025.12* · [Paper](https://arxiv.org/abs/2512.11229)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Diffusion-based end-to-end streaming talking-head framework using ID-Context Cache and Asynchronous Streaming Distillation for real-time long-form generation.

- **StableAvatar: Infinite-Length Audio-Driven Avatar Video Generation** · *arXiv 2025.08* · [Paper](https://arxiv.org/abs/2508.08248) · [Project](https://francis-rings.github.io/StableAvatar) · [Code](https://github.com/Francis-Rings/StableAvatar)  
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/Francis-Rings/StableAvatar?style=flat-square)  
  Infinite-length audio-driven avatar video generation using a time-step-aware audio adapter, audio-native guidance, and weighted sliding-window fusion.

- **TalkingMachines: Real-Time Audio-Driven FaceTime-Style Video via Autoregressive Diffusion Models** · *arXiv 2025.06* · [Paper](https://arxiv.org/abs/2506.03099) · [Project](https://aaxwaz.github.io/TalkingMachines/) · [Code](https://github.com/aaxwaz/TalkingMachines)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/aaxwaz/TalkingMachines?style=flat-square)  
  Real-time FaceTime-style audio-driven video system that distills bidirectional video diffusion into a sparse causal AR student for infinite streaming.

---

## Interactive & Full-Duplex Conversational Avatars

- **EmbodiedHead: Real-Time Listening and Speaking Avatar for Conversational Agents** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.17211)  
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Single-stream listening-speaking avatar interface with per-frame state conditioning, Streaming Audio Scheduler, Rectified-Flow DiT, and differentiable renderer.

- **Beyond Monologue: Interactive Talking-Listening Avatar Generation with Conversational Audio Context-Aware Kernels** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.10367) · [Project](https://warmcongee.github.io/beyond-monologue/)  
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Full-duplex talking-listening avatar generation with conversational audio context-aware kernels and VoxHear dataset for decoupled speech/background audio.

- **LPM 1.0: Video-based Character Performance Model** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.07823) · [Project](https://large-performance-model.github.io)  
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)  
  17B-parameter full-duplex conversational avatar system with Online LPM for low-latency infinite-length interaction and LPM-Bench for interactive character performance evaluation.

- **SentiAvatar: Towards Expressive and Interactive Digital Humans** · *arXiv 2026.04* · [Paper](https://arxiv.org/abs/2604.02908) · [Project](https://sentiavatar.github.io/) · [Code](https://github.com/SentiAvatar/SentiAvatar)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/SentiAvatar/SentiAvatar?style=flat-square)  
  Expressive interactive digital-human framework with an audio-aware plan-then-infill architecture for real-time speech, gesture, and emotion generation.

- **GDPO-Listener: Expressive Interactive Head Generation via Auto-Regressive Flow Matching and Group reward-Decoupled Policy Optimization** · *arXiv 2026.03* · [Paper](https://arxiv.org/abs/2603.25020)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Auto-regressive flow matching plus group reward-decoupled policy optimization for expressive speaking and listening head motion generation.

- **τ-Voice: Benchmarking Full-Duplex Voice Agents on Real-World Domains** · *arXiv 2026.03* · [Paper](https://arxiv.org/abs/2603.13686)  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  Real-world full-duplex voice-agent benchmark extending task-completion evaluation with grounded domains, realistic audio, and conversational dynamics.

- **MANGO: Natural Multi-speaker 3D Talking Head Generation via 2D-Lifted Enhancement** · *arXiv 2026.01* · [Paper](https://arxiv.org/abs/2601.01749)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Multi-speaker 3D talking-head generation for bidirectional listen-and-speak interaction, using dual-audio fusion and 3D Gaussian rendering.

- **Avatar Forcing: Real-Time Interactive Head Avatar Generation for Natural Conversation** · *CVPR 2026 / arXiv 2026.01* · [Paper](https://arxiv.org/abs/2601.00664) · [Project](https://taekyungki.github.io/AvatarForcing/) · [Code](https://github.com/TaekyungKi/AvatarForcing)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/TaekyungKi/AvatarForcing?style=flat-square)  
  Diffusion forcing with causal low-latency multimodal interaction and DPO-style preference optimization for expressive avatar reactions.

- **DyStream: Streaming Dyadic Talking Heads Generation via Flow Matching-based Autoregressive Model** · *arXiv 2025.12* · [Paper](https://arxiv.org/abs/2512.24408) · [Project](https://robinwitch.github.io/DyStream-Page/)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Flow-matching autoregressive dyadic talking-head model for streaming dual-track audio input, targeting sub-100ms system latency.

- **UniLS** · *arXiv 2025.12* · [Paper](https://arxiv.org/abs/2512.09327) · [Project](https://xg-chu.site/project_unils/) · [Code](https://github.com/xg-chu/UniLS)  
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/xg-chu/UniLS?style=flat-square)  
  End-to-end speaking-and-listening avatar generation driven only by dual-track audio, improving listener motion diversity and naturalness.

- **FLEXI: Benchmarking Full-duplex Human-LLM Speech Interaction** · *arXiv 2025.09* · [Paper](https://arxiv.org/abs/2509.22243) · [Code](https://github.com/ChristineCHEN274/FLEXI)  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/ChristineCHEN274/FLEXI?style=flat-square)  
  Full-duplex human-LLM speech interaction benchmark covering latency, response quality, conversational effectiveness, and emergency interruption scenarios.

- **EAI-Avatar: Emotion-Aware Interactive Talking Head Generation** · *arXiv 2025.08* · [Paper](https://arxiv.org/abs/2508.18337)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Emotion-aware dyadic talking-head generation with LLM-guided emotional dynamics and smooth transitions between speaking and listening states.

- **FD-Bench: A Full-Duplex Benchmarking Pipeline Designed for Full Duplex Spoken Dialogue Systems** · *Interspeech 2025 / arXiv 2025.07* · [Paper](https://arxiv.org/abs/2507.19040) · [Project](https://pengyizhou.github.io/FD-Bench/) · [Code](https://github.com/pengyizhou/FD-Bench)  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/pengyizhou/FD-Bench?style=flat-square)  
  Benchmarking pipeline for full-duplex spoken dialogue systems, focusing on interruptions, latency, noisy scenarios, and robustness under real-time interaction.

- **ARIG: Autoregressive Interactive Head Generation for Real-time Conversations** · *ICCV 2025 / arXiv 2025.07* · [Paper](https://arxiv.org/abs/2507.00472) · [Project](https://jinyugy21.github.io/ARIG/)  
  ![Causal](https://img.shields.io/badge/-Causal-1f6feb?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Autoregressive frame-wise interactive head generation with interactive behavior understanding and conversational state understanding for smooth listening-speaking transitions.

- **OmniResponse: Online Multimodal Conversational Response Generation in Dyadic Interactions** · *NeurIPS 2025 / arXiv 2025.05* · [Paper](https://arxiv.org/abs/2505.21724) · [Project](https://omniresponse.github.io/) · [Code](https://github.com/awakening-ai/OmniResponse)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Streaming](https://img.shields.io/badge/-Streaming-0ea5e9?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/awakening-ai/OmniResponse?style=flat-square)  
  Online multimodal conversational response generation that jointly produces verbal and non-verbal listener feedback from speaker multimodal inputs.

- **Full-Duplex-Bench: A Benchmark to Evaluate Full-duplex Spoken Dialogue Models on Turn-taking Capabilities** · *arXiv 2025.03* · [Paper](https://arxiv.org/abs/2503.04721) · [Project](https://full-duplex-bench.github.io/) · [Code](https://github.com/DanielLin94144/Full-Duplex-Bench)  
  ![Benchmark](https://img.shields.io/badge/-Benchmark-6f42c1?style=flat-square)
  ![Full-duplex](https://img.shields.io/badge/-Full--duplex-dc2626?style=flat-square)
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Real-time](https://img.shields.io/badge/-Real--time-16a34a?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/DanielLin94144/Full-Duplex-Bench?style=flat-square)  
  Benchmark suite for full-duplex spoken dialogue models, evaluating pause handling, backchanneling, turn-taking, and interruption management.

- **Diffusion-based Realistic Listening Head Generation via Hybrid Motion Modeling** · *CVPR 2025* · [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_Diffusion-based_Realistic_Listening_Head_Generation_via_Hybrid_Motion_Modeling_CVPR_2025_paper.html) · [Project](https://nuo1wang.github.io/DiffListener/)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Diffusion-based listening-head generation with hybrid explicit and implicit motion modeling for expressive non-verbal listener responses.

- **DualTalk** · *CVPR 2025* · [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Peng_DualTalk_Dual-Speaker_Interaction_for_3D_Talking_Head_Conversations_CVPR_2025_paper.html) · [Project](https://ziqiaopeng.github.io/dualtalk) · [Code](https://github.com/ZiqiaoPeng/DualTalk)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  ![GitHub Repo stars](https://img.shields.io/github/stars/ZiqiaoPeng/DualTalk?style=flat-square)  
  Multi-round dual-speaker 3D talking-head generation with seamless speaking/listening role transitions and a 50-hour interaction dataset.

- **LLM-driven Multimodal and Multi-Identity Listening Head Generation** · *CVPR 2025* · [Paper](https://openaccess.thecvf.com/content/CVPR2025/papers/Lai_LLM-driven_Multimodal_and_Multi-Identity_Listening_Head_Generation_CVPR_2025_paper.pdf) · [Project](https://www.sysu-hcp.net/projects/Multimodal/161.html)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  LLM-driven listening-head generation that integrates speech content, prosody, and speaker emotion while supporting multi-identity listener control.

- **INFP: Audio-Driven Interactive Head Generation in Dyadic Conversations** · *CVPR 2025 / arXiv 2024.12* · [Paper](https://arxiv.org/abs/2412.04037) · [Project](https://grisoon.github.io/INFP/)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Audio-driven dyadic head generation that dynamically alternates between speaking and listening states without explicit role switching, introducing the DyConv dataset.

- **DialogueNeRF: Towards Realistic Avatar Face-to-Face Conversation Video Generation** · *Visual Intelligence 2024 / arXiv 2022.03* · [Paper](https://arxiv.org/abs/2203.07931)  
  ![Interactive](https://img.shields.io/badge/-Interactive-f59e0b?style=flat-square)
  ![Talking Head](https://img.shields.io/badge/-Talking%20Head-64748b?style=flat-square)  
  Early face-to-face conversational avatar framework using NeRF to model both speaker and listener, including responsive listener behavior conditioned on visual and acoustic cues.

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
