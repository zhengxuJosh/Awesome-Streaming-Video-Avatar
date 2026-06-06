# Streaming Avatar Models: Resolution & Streaming Modes

This note summarizes the current streaming and real-time avatar models in the list, with a focus on:

- reported or inferable output / training resolution
- streaming granularity and causality
- reported latency or throughput
- practical deployment implications

> Note: many papers report training crop resolution, VAE compression ratio, or benchmark settings rather than a guaranteed production output resolution. In those cases, the resolution is marked as not explicitly stated.

## High-Level Takeaways

- **512x512 is the clearest practical target** among current pixel-level diffusion-style streaming avatar systems.
- **720p+ low-latency streaming is not yet consistently demonstrated** for these avatar diffusion systems; several works explicitly reduce resolution to satisfy real-time constraints.
- **One-step / few-step streaming avatars are becoming the 2026 trend**, with AvatarForcing and TurboTalk pushing audio-driven avatar generation toward one-step inference.
- **Long-form identity stability is now a first-class metric**, especially in AsymTalker, AvatarForcing, SoulX-FlashTalk, StableAvatar, and related long-rollout systems.
- **Frame-level or very short chunk autoregressive systems** are best suited for live interaction latency.
- **GPT-style AR and in-context control are emerging alternatives** to diffusion-only streaming, especially for frame-wise control and arbitrary-length interactive generation.
- **Pixel-level diffusion systems** generally provide stronger visual fidelity but require heavier serving infrastructure.
- **Motion / renderer based systems** can reach much lower latency, but may trade off full pixel-level generative flexibility.
- **KV-cache and attention policy design is moving from uniform to head-aware**, as shown by 2026 real-time AR video backbones such as Head Forcing and Pyramid Forcing.
- **System-level streaming is now a first-class research axis**, with StreamAvatar, StreamDiffusionV2, and SANA-Streaming focusing on real-time schedules, causal caches, and serving constraints rather than only model quality.
- **Memory and token efficiency are becoming as important as denoising-step reduction**, with QVG, CoReDiT, DC-VideoGen, AnyFlow, and related work attacking KV cache size, token count, latent compression, and flexible step budgets.
- **Temporal super sampling is a practical path to 1080p+ delivery**: generate at 540p / 720p when needed, then upscale with temporal neural super sampling instead of forcing the base generator to run at native high resolution.

## Model Comparison

| Model | Reported Resolution | Use Case | Streaming Mode | Reported Speed | Practical Read |
| --- | --- | --- | --- | --- | --- |
| [StreamAvatar](https://arxiv.org/abs/2512.22065) | High-resolution claim; exact production resolution not explicitly summarized here | Real-time interactive human avatar, including talking and listening behaviors with gestures | Converts a bidirectional human video diffusion teacher into a block-causal streaming student through autoregressive distillation and adversarial refinement. Uses Reference Sink, Reference-Anchored Positional Re-encoding, and a consistency-aware discriminator for long-term stability. | Real-time claim; project / CVPR text emphasizes low latency but exact FPS not summarized here | One of the most directly relevant CVPR 2026 avatar systems because it targets full-body interactive streaming rather than only head-and-shoulder talking heads. |
| [AsymTalker](https://arxiv.org/abs/2605.02948) | Not explicitly stated in inspected text | Long-term talking-head generation | Asymmetric distillation with Temporal Reference Encoding. Converts the static identity reference into pseudo-video latent context to reduce identity-reference / audio-stream mismatch. | 66 FPS; reported consistency up to 10 minutes | Strong long-form identity-stability reference for diffusion-based talking heads. |
| [AvatarForcing](https://arxiv.org/abs/2603.14331) | Not explicitly stated in inspected text | One-step audio-driven talking avatar | Local-future sliding-window denoising with heterogeneous noise levels. Emits one clean block per step and uses dual-anchor temporal forcing plus two-stage streaming distillation. | 34 ms/frame with a 1.3B student | One of the clearest 2026 examples of one-step streaming pixel-level avatar generation. |
| [Hallo-Live](https://arxiv.org/abs/2604.23632) | Not explicitly stated in inspected text | Text-to-audio-video joint generation | Asynchronous dual-stream diffusion. The video stream commits the current block, while the audio stream carries current plus temporary future audio. Uses Future-Expanding Attention. | 20.38 FPS, 0.94s latency on 2xH200 | True streaming with one-block / one-frame audio look-ahead. |
| [EARTalking](https://arxiv.org/abs/2603.20307) | Not explicitly stated in inspected abstract | Interactive audio-driven talking head | End-to-end GPT-style autoregressive model. Generates frame-by-frame with Sink Frame Window Attention and streaming Frame Condition In-Context control. | Not stated in inspected abstract | Important non-diffusion streaming direction: frame-wise in-context control and variable-length identity consistency. |
| [SentiAvatar](https://arxiv.org/abs/2604.02908) | Not explicitly stated in inspected abstract | Expressive interactive 3D digital human | Audio-aware plan-then-infill motion architecture. Decouples sentence-level semantic planning from frame-level prosody-driven interpolation. | 6s output in 0.3s; unlimited multi-turn streaming claim | Strong reference for real-time expressive full-body / gesture behavior, but more motion/digital-human oriented than pixel-level diffusion. |
| [TurboTalk](https://arxiv.org/abs/2604.14580) | Not explicitly stated | Audio-driven talking avatar | Two-stage progressive distillation: first Distribution Matching Distillation to a 4-step student, then progressive adversarial distillation to a 1-step generator. | 120x inference speedup; 1 NFE; exact FPS/latency not stated in inspected abstract | Important Stage-1 acceleration method; not a complete streaming-mode design by itself. |
| [TAVR / Generate Your Talking Avatar from Video Reference](https://arxiv.org/abs/2604.27918) | Not explicitly stated in inspected abstract | Customized talking avatar from video reference | Uses cross-scene video reference rather than a static image. Includes token selection plus three-stage training for same-scene pretraining, cross-scene fine-tuning, and task adaptation. | Not stated in inspected abstract | Useful data/conditioning direction; not primarily a low-latency streaming system. |
| [SDTalk](https://arxiv.org/abs/2605.09956) | Not explicitly stated in inspected abstract | Generalizable Gaussian talking head | One-shot 3D Gaussian Splatting pipeline with structured facial priors and dual-branch motion fields for coarse/fine facial dynamics. | Real-time claim; exact FPS not found in inspected abstract | Renderer-based direction for cross-identity generalization; complementary to pixel diffusion systems. |
| [SoulX-FlashHead](https://arxiv.org/abs/2602.07449) | 512x512 reported training / data crop | Audio-driven portrait | Autoregressive streaming DiT with Temporal Audio Context Cache. Lite uses LTX-style 32x32x8 compression. Uses Oracle-Guided Bidirectional Distillation. | Lite: 96 FPS on RTX 4090 | Strong consumer-GPU candidate among diffusion-style portrait models. |
| [SoulX-FlashTalk](https://arxiv.org/abs/2512.23379) | Reduced spatial resolution; exact output size not stated | Audio-driven full-body / avatar | Chunk-based streaming. Retains bidirectional attention inside the current chunk, with self-correcting bidirectional distillation and multi-step retrospective correction. | 32 FPS, 0.87s startup on 8xH800 | High-quality 14B route; heavy multi-GPU serving. |
| [REST](https://arxiv.org/abs/2512.11229) | 512x512, 97-frame training chunks | Audio-driven talking head | Semi-autoregressive diffusion. Uses temporal VAE 32x32x8, ID-Sink plus previous-chunk Context Cache, and ASD from a non-streaming teacher to a streaming student. | 4.416s runtime for 121 frames on A100 setup | Strong explicit 512x512 streaming diffusion setup with single-GPU real-time claim. |
| [TalkingMachines](https://arxiv.org/abs/2506.03099) | 512x512 target; supports aspect ratios within the same pixel area | FaceTime-style audio-driven character video | Sparse causal AR diffusion student. An 81-frame clip is split into 7 chunks of 3 latent frames; each chunk attends to the current chunk, previous chunk, and first-image anchor. | Real-time via 2-step distillation plus DiT/VAE disaggregation; exact FPS not stated in inspected text | Practical serving-oriented design; explicitly notes 720x720 is much more expensive. |
| [DyStream](https://arxiv.org/abs/2512.24408) | Not explicitly stated | Dyadic talking head | Frame-by-frame autoregressive audio-to-motion generation with LivePortrait/LIA-style warp decoder. Uses causal Wav2Vec2 with about 60ms look-ahead. | Less than 34ms per frame; less than 40ms per incoming audio packet | Lowest-latency interaction shape; more motion / renderer based than full pixel diffusion. |
| [EmbodiedHead](https://arxiv.org/abs/2604.17211) | Rendered avatar resolution not stated | 3D head avatar for LLM conversation | Single audio stream with per-frame listening/speaking state. Uses Streaming Audio Scheduler, Rectified-Flow DiT over FLAME motion, and differentiable renderer. | 59 FPS full pipeline on RTX 3090; motion module over 900 FPS; 4 sampling steps | Good architecture for LLM turn-taking because it avoids dual-audio look-ahead dependency. |
| [PikaStream1.0](https://pika.me/blog/introducing-real-time-video-chat) | 480p reported by Pika blog | Real-time video face / voice layer for AI agents | Real-time personalized video stream for agent video calls, decoupling the reasoning agent from the avatar / voice rendering layer. | 24 FPS and about 1.5s end-to-end speech-to-video latency on one H100 reported by Pika | Important product-facing reference for agent avatars: practical conversational latency may be closer to 1-2s than sub-100ms when full generative video is used. |
| [Beyond Monologue](https://arxiv.org/abs/2604.10367) | Not explicitly stated | Full-duplex talking/listening human video | Wan2.2 5B backbone with dual talking/listening audio streams, 4x16x16 VAE compression, conversational audio context-aware Gaussian kernels, and diffusion forcing. Introduces VoxHear with 1,206 hours of decoupled speech/background audio. | No explicit FPS/latency found in inspected text | More focused on full-duplex behavior modeling and data construction than low-latency serving. |
| [UniLS](https://arxiv.org/abs/2512.09327) | Not explicitly stated | Unified speaking/listening audio-driven avatar | End-to-end dual-track-audio model. First learns an audio-free autoregressive internal motion prior, then fine-tunes with dual-track audio for speaking and listening modulation. | No explicit FPS/latency found in inspected text | Strong end-to-end full-duplex modeling reference; less explicit about streaming infrastructure. |
| [GaussianHeadTalk](https://arxiv.org/abs/2512.10939) | Not explicitly stated in inspected abstract | Real-time 3D talking head | Audio-driven Gaussian Splatting with 3DMM-based Gaussian mapping and transformer prediction of facial parameters from audio. | Real-time claim; exact FPS not found in inspected abstract | Practical 3DGS route for temporally stable interactive talking heads. |
| [StableAvatar](https://arxiv.org/abs/2508.08248) | Not explicitly stated in inspected text | Long-form audio-driven avatar | Weighted sliding-window denoising with audio-native guidance, designed for infinite-length consistency. | 30 FPS examples; 3500+ frames / 3+ minutes reported | Long-video stability oriented, not necessarily interactive streaming. |
| [Wan-S2V](https://arxiv.org/abs/2508.18621) | 480p / 720p support reported by model release materials | Audio-driven cinematic character animation | Wan-based audio-driven video generation for expressive human character animation, long-form generation, and precise lip-sync editing. Uses text for global motion control and audio for fine expression timing. | Exact FPS/latency not found in inspected abstract | Important high-fidelity / cinematic reference; not positioned as a low-latency interactive streaming baseline. |
| [InfiniteTalk](https://arxiv.org/abs/2508.14033) | 480p / 720p support reported by project materials | Sparse-frame video dubbing and long-form talking video | Uses sparse reference frames to preserve identity, emotional cadence, gestures, and camera trajectory while generating audio-aligned lips, face, head, and body motion. | Unlimited-length claim; exact FPS/latency not found in inspected abstract | Strong long-form dubbing reference; more about identity-preserving long sequence synthesis than live low-latency response. |
| [OmniAvatar](https://arxiv.org/abs/2506.18866) | Not explicitly stated in inspected abstract | Audio-driven full-body avatar video | Uses audio pack latent embedding, multi-hierarchical audio embedding, LoRA adaptation, frame overlap, and reference-image embedding for adaptive body animation. | Not stated in inspected abstract | Useful full-body conditioning reference; less explicit about streaming latency. |
| [FlowPortrait](https://arxiv.org/abs/2603.00159) | Not explicitly stated in inspected abstract | Audio-driven portrait video quality optimization | Reinforcement learning post-training for an autoregressive audio-to-video generator, using MLLM-based human-aligned rewards for lip sync, expressiveness, and motion quality. | Not stated in inspected abstract | Evaluation/alignment direction rather than a streaming architecture, but relevant for quality tuning of AR portrait models. |
| [THEval](https://arxiv.org/abs/2511.04520) | Evaluation framework, not a generator | Talking-head video generation evaluation | Defines 8 fine-grained metrics across quality, naturalness, and synchronization, validated against human ratings on generated videos from 17 methods. | Spearman correlation 0.870 with human ratings reported | Useful benchmark reference because many streaming avatar systems optimize FPS while still needing expressiveness, head motion, and artifact diagnostics beyond lip sync. |

## Related Streaming Video Backbones

These are not all avatar-specific systems, but they are highly relevant because streaming avatar models increasingly inherit their causal attention, forcing, distillation, and KV-cache designs.

| Model | Relevance to Avatars | Streaming / Memory Mode | Reported Speed or Efficiency | Practical Read |
| --- | --- | --- | --- | --- |
| [StreamDiffusionV2](https://arxiv.org/abs/2511.07399) | System-level reference for live video diffusion serving | Training-free streaming system with SLO-aware batching / block scheduling, sink-token-guided rolling KV cache, motion-aware noise control, and multi-GPU pipeline orchestration. | TTFF within 0.5s; 58.28 FPS with 14B and 64.52 FPS with 1.3B on 4xH100 in 1-step mode; MLSys 2026 Best Paper | Strongest current serving-system reference for turning offline video diffusion into live streams under latency deadlines. |
| [Streaming Video Generation: From Pipelines to Operators](https://cvpr26-edge.github.io/) | Research talk framing the shift from pipeline-level streaming to lower-level operator / system design | Workshop talk by Chenfeng Xu (UT Austin / Together AI) connecting StreamDiffusion-style pipeline ideas to operator-level streaming video generation systems. | Talk / workshop item; no standalone FPS in this note | Useful roadmap item for tracking where streaming generation systems are heading beyond model papers. |
| [SANA-Streaming](https://arxiv.org/abs/2605.30409) | Real-time streaming video editing backbone for interactive avatar filters, stylization, or live relighting | Hybrid Diffusion Transformer with Gated DeltaNet global memory plus softmax-attention local alignment; uses Cycle-Reverse Regularization and Blackwell-oriented fused kernels / mixed-precision quantization. | 1280x704 at 24 end-to-end FPS on a single RTX 5090; DiT core 58 FPS | Important evidence that high-resolution real-time video-to-video diffusion is feasible when model architecture and kernels are co-designed. |
| [Quant VideoGen / QVG](https://arxiv.org/abs/2602.02958) | Long-horizon AR avatar sessions are often KV-cache limited | Training-free 2-bit KV-cache quantization using Semantic-Aware Smoothing and Progressive Residual Quantization. | Up to 7.0x KV-cache memory reduction with less than 4% end-to-end latency overhead; code: https://github.com/svg-project/Quant-VideoGen | Directly relevant to long interactive avatars where identity, layout, and motion consistency depend on retaining more history. |
| [DC-VideoGen](https://arxiv.org/abs/2509.25182) | High-resolution / long-video avatar generation can benefit from deeper latent compression | Post-training acceleration through Deep Compression Video Autoencoder with chunk-causal temporal modeling and AE-Adapt-V transfer into the compressed latent space. | Up to 14.8x lower inference latency; 2160x3840 generation on one H100 reported | Useful route if native 720p / 1080p avatar diffusion is too expensive at standard latent compression ratios. |
| [STARFlow-V](https://starflow-v.github.io/) | Alternative to diffusion for causal AR video generation | Autoregressive normalizing-flow video model with global-local latent architecture, flow-score matching, and video-aware Jacobi iteration for accelerated sampling. | Up to 480p / 81-frame examples reported in public materials; exact real-time FPS not summarized here | Important non-diffusion direction because invertible flow models provide native likelihoods and robust causal prediction. |
| [CoReDiT](https://arxiv.org/abs/2605.14191) | Token-pruning acceleration for DiT-based image / video avatar backbones | Spatial-coherence-guided token pruning plus reconstruction of skipped attention outputs; progressive, block-adaptive pruning schedule. | Up to 55% self-attention FLOPs reduction; 1.33x cloud GPU and 1.72x mobile NPU speedups reported | Practical accelerator when high-resolution avatar frames create too many spatial tokens for self-attention. |
| [AnyFlow](https://nvlabs.github.io/AnyFlow/) | Any-step video diffusion distillation for latency / quality trade-offs | Flow-map distillation learns transitions over arbitrary time intervals, with Flow Map Backward Simulation for on-policy distillation across bidirectional and causal architectures. | Supports 1.3B to 14B Wan2.1 variants; public materials report 480p checkpoints and flexible step budgets | Relevant when avatar systems need a single model that can move between ultra-low-latency and higher-quality modes. |
| [Neural Super Sampling / NSS](https://huggingface.co/Arm/neural-super-sampling) | Post-generation temporal upscaling for 1080p / 1440p delivery | Neural temporal super sampling reconstructs high-resolution output from lower-resolution temporal inputs; aimed at graphics / mobile real-time pipelines. | 540p to 1080p with up to 50% GPU savings; Arm blog reports about 4ms in a demo setup | Practical deployment lever: generate avatars at 540p / 720p, then temporally upscale instead of forcing native high-res generation. |
| [Causal Forcing++](https://arxiv.org/abs/2605.15141) | Few-step causal video backbone for interactive systems | Frame-wise autoregression with 1-2 sampling steps. Uses causal consistency distillation for scalable AR student initialization. | Reduces first-frame latency by 50% and Stage-2 training cost by about 4x versus the cited baseline setting | Important update to the Stage-1 + Stage-2 pipeline; likely relevant to future low-latency avatars. |
| [Delta Forcing](https://arxiv.org/abs/2605.14382) | Interactive AR video steering | Trust-region steering for dynamically changing conditions, aiming to balance responsiveness and long-horizon stability. | Not summarized as FPS in inspected abstract | Useful for avatars that need to react to changing dialogue or control signals without drifting. |
| [Head Forcing](https://arxiv.org/abs/2605.14487) | Long-rollout AR video stability | Training-free head-specific KV-cache policies: local, anchor, and memory heads receive different retention strategies plus RoPE re-encoding. | Training-free; efficiency numbers not extracted from inspected abstract | Strong evidence that future avatar streaming stacks should not use one-size-fits-all KV retention. |
| [Pyramid Forcing](https://arxiv.org/abs/2605.13111) | KV-cache policy for long video | Head-aware pyramidal KV cache with Anchor, Wave, and Veil head types and ragged-cache attention. | Improves long-horizon quality in Self Forcing and Causal Forcing settings; exact FPS not inspected | Complements Head Forcing; points toward structured memory policies for long avatar sessions. |
| [CausalCine](https://arxiv.org/abs/2605.12496) | Open-ended interactive video generation | Causal multi-shot AR generation with online prompt updates and Content-Aware Memory Routing. | Few-step distilled generator; exact FPS not inspected | Less avatar-specific, but useful for session-level scene, camera, or background evolution. |
| [Hybrid Forcing](https://arxiv.org/abs/2604.10103) | Long-horizon streaming video backbone | Hybrid attention combines lightweight linear temporal attention for evicted long-range history with block-sparse local sliding-window attention, plus decoupled distillation. | 832x480 unbounded video at 29.5 FPS on a single H100 | Highly relevant for avatar sessions where long memory and real-time throughput are both needed. |
| [PackForcing](https://arxiv.org/abs/2603.25730) | Long-context AR video generation | Three-partition KV-cache strategy: full-resolution sink tokens, compressed mid tokens, and full-resolution recent tokens with top-k context selection and Temporal RoPE adjustment. | 2-minute 832x480 video at 16 FPS on a single H200; bounded 4 GB KV cache | Useful template for bounded-memory long avatar sessions and short-to-long extrapolation. |
| [ShotStream](https://arxiv.org/abs/2603.25746) | Interactive multi-shot video continuity | Causal next-shot generation with streaming prompts, global/local dual-cache memory, RoPE discontinuity indicators, and two-stage self-forcing. | 16 FPS on a single GPU; sub-second latency claim | Relevant for avatars with evolving scenes, camera shots, or narrative context. |
| [Self Forcing](https://arxiv.org/abs/2506.08009) | AR video diffusion train-test gap | Trains with autoregressive rollouts and KV caching so the model conditions on its own generated outputs; uses stochastic gradient truncation and rolling KV cache. | 17 FPS with sub-second latency on a single H100 | Foundational forcing reference for reducing exposure bias in streaming avatar rollouts. |
| [Diagonal Distillation](https://arxiv.org/abs/2603.09488) | Streaming AR diffusion acceleration | Diagonal denoising schedule across chunks and denoising steps, with asymmetric early/later chunk computation. | 5-second video in 2.61s, up to 31 FPS, 277.3x speedup over undistilled model | Useful template for reducing exposure bias in long streaming rollouts. |

## Practical Buckets

### Lowest Latency

- **DyStream**: frame-by-frame AR generation with minimal audio look-ahead.
- **EmbodiedHead**: 3D/motion-first pipeline for real-time LLM turn-taking; reports 59 FPS full pipeline on RTX 3090.
- **AvatarForcing**: one-step sliding-window pixel generation at 34 ms/frame, but still heavier than motion/renderer-only pipelines.
- **StreamAvatar**: full-body interactive streaming diffusion route for talking/listening behavior, with stronger pixel-level flexibility than renderer-only systems.
- **EARTalking**: frame-by-frame GPT-style AR talking head generation with in-context control.
- **SentiAvatar**: real-time expressive 3D digital human motion with unlimited multi-turn streaming claim.
- **PikaStream1.0**: product-facing single-GPU agent avatar stream at 480p / 24 FPS with about 1.5s end-to-end speech-to-video latency.

These are better references for conversational responsiveness than for full pixel-level video generation.

### One-Step / Few-Step / Frame-Level Avatar Generation

- **AvatarForcing**: one-step streaming diffusion with local-future windows and dual-anchor temporal forcing.
- **StreamAvatar**: autoregressive distillation plus adversarial refinement from bidirectional teacher to block-causal streaming student.
- **TurboTalk**: one-step audio-driven avatar generation through progressive distillation, mainly an acceleration method.
- **AsymTalker**: asymmetric distillation for long-term identity consistency at high reported FPS.
- **EARTalking**: non-diffusion AR route for frame-level streaming and control.

These are the most relevant 2026 references for low-step diffusion distillation and frame-level streaming generation.

### Strong 512x512 Pixel-Level References

- **REST**: explicit 512x512 streaming diffusion training setup.
- **SoulX-FlashHead**: 512x512 portrait data/crop and very high reported FPS for the Lite version.
- **TalkingMachines**: explicitly targets 512x512 and discusses why higher resolution is harder for streaming.

These are the clearest references for practical high-fidelity streaming avatar video at current compute levels.

### Systems, Compression, and Upscaling Levers

- **StreamDiffusionV2**: SLO-aware scheduling, rolling KV cache, motion-aware noise, and multi-GPU pipeline orchestration for live video diffusion.
- **SANA-Streaming**: high-resolution video-to-video streaming with hybrid DiT blocks and system co-design.
- **Quant VideoGen / QVG**: 2-bit KV-cache compression for long AR video sessions with minimal latency overhead.
- **DC-VideoGen**: deep-compression video autoencoder route for high-resolution generation with much lower latency.
- **CoReDiT**: token pruning and reconstruction for reducing self-attention cost in DiT backbones.
- **AnyFlow**: any-step flow-map distillation for flexible latency / quality budgets.
- **Neural Super Sampling**: temporal upscaling from 540p / 720p generation toward 1080p / 1440p delivery.

These are the most useful references when the bottleneck is serving cost, memory, or output resolution rather than avatar conditioning itself.

### Heavy High-Fidelity Serving

- **SoulX-FlashTalk**: 14B model, 8xH800 reported setup.
- **Hallo-Live**: joint audio-video generation on 2xH200 with sub-second latency.
- **Wan-S2V**: cinematic 14B-style direction with 480p / 720p support reported in release materials.

These are more suitable as high-quality service architectures than consumer deployment baselines.

### Long-Form / Dubbing-Oriented Avatars

- **InfiniteTalk**: sparse-frame dubbing for identity-preserving long-form talking video.
- **Wan-S2V**: cinematic audio-driven character animation, long-form generation, and lip-sync editing.
- **StableAvatar**: infinite-length consistency for long audio-driven avatar video.
- **OmniAvatar**: full-body adaptive animation with audio-conditioned latent embedding.

These are important references for production-style long-form avatar generation, but they should not be read as proof of sub-100ms interactive latency.

## Resolution Trend

Current streaming avatar systems mostly converge around **512x512** for real-time or near-real-time pixel-level generation. Higher resolutions such as 720p or 1080p remain costly because the video token count grows quickly, increasing transformer attention cost, VAE decoding cost, and activation memory. New system and compression work changes the deployment calculus: SANA-Streaming reports 1280x704 real-time video editing on a single RTX 5090, StreamDiffusionV2 reports live video diffusion throughput on multi-H100 setups, DC-VideoGen shows that deeper latent compression can unlock much higher resolution, and NSS-style temporal super sampling makes 540p / 720p generation plus 1080p / 1440p upscaling a realistic product path. Cinematic or dubbing-oriented systems such as Wan-S2V and InfiniteTalk report 480p / 720p support, but their latency profile is different from live conversational streaming.

For practical product design today:

- use **512x512** as the default target for pixel-level diffusion avatar streaming
- consider **540p / 720p plus temporal super sampling** when the product requires 1080p / 1440p output but the generator cannot run natively at that resolution
- use **motion/renderer-based systems** when sub-100ms response is more important than generative flexibility
- treat **720p+** as an upscaling or post-processing target unless the serving stack has substantial multi-GPU capacity
- treat **one-step diffusion** as promising but still not automatically sufficient: long-form identity stability, cache policy, and causal audio handling remain decisive
- track **head-aware and quantized KV-cache policies** because long avatar sessions are increasingly memory-policy limited rather than only denoising-step limited
