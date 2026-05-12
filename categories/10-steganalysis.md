# Steganalysis

<!-- TOC -->
## Contents (92 algorithms)

**[Classical Methods](#classical-methods)**
- [Visual Attack](#visual-attack)
- [Structural Attack](#structural-attack)
- [Chi-square](#chi-square)
- [RS-analysis](#rs-analysis)
- [Weighted Stego](#weighted-stego)
- [SPAM](#spam)
- [SRM](#srm)
- [DCTR](#dctr)

**[Deep Learning](#deep-learning)**
- [XuNet](#xunet)
- [YeNet](#yenet)
- [SRNet](#srnet)
- [ZhuNet](#zhunet)

**[Network Steganalysis](#network-steganalysis)**
- [Tor Traffic Detection](#tor-traffic-detection)
- [DNS Tunnel Detection](#dns-tunnel-detection)

**[Detection Benchmarks](#detection-benchmarks)**
- [Stego Battlefield](#stego-battlefield)
- [Zero-Shot Interpretable Image Steganalysis](#zero-shot-interpretable-image-steganalysis)
- [Targeted Pooled Latent-Space Steganalysis](#targeted-pooled-latent-space-steganalysis)
- [Systematically Deconstructing APVD Steganography](#systematically-deconstructing-apvd-steganography)

**[Recent arXiv Papers (2024–2026)](#recent-arxiv-papers-20242026)**
- [A Game-Theoretic Approach for Adversarial Information Fusion...](#a-game-theoretic-approach-for-adversarial-information-fusion-in-distributed-sensor-networks)
- [Exploring AI in Steganography and Steganalysis: Trends, Clus...](#exploring-ai-in-steganography-and-steganalysis-trends-clusters-and-sustainable-development-potential)
- [GSDFuse: Capturing Cognitive Inconsistencies from Multi-Dime...](#gsdfuse-capturing-cognitive-inconsistencies-from-multi-dimensional-weak-signals-in-social-media-steganalysis)
- [A study on audio synchronous steganography detection and dis...](#a-study-on-audio-synchronous-steganography-detection-and-distributed-guide-inference-model-based-on-sliding-spectral-features-and-intelligent-inference-drive)
- [TSCL:Multi-party loss Balancing scheme for deep learning Ima...](#tsclmulti-party-loss-balancing-scheme-for-deep-learning-image-steganography-based-on-curriculum-learning)
- [Efficient Streaming Voice Steganalysis in Challenging Detect...](#efficient-streaming-voice-steganalysis-in-challenging-detection-scenarios)
- [Linguistic Steganalysis via LLMs: Two Modes for Efficient De...](#linguistic-steganalysis-via-llms-two-modes-for-efficient-detection-of-strongly-concealed-stego)
- [Blind Data Adaptation to tackle Covariate Shift in Operation...](#blind-data-adaptation-to-tackle-covariate-shift-in-operational-steganalysis)
- [Towards Next-Generation Steganalysis: LLMs Unleash the Power...](#towards-next-generation-steganalysis-llms-unleash-the-power-of-detecting-steganography)
- [Double-Flow-based Steganography without Embedding for Image-...](#double-flow-based-steganography-without-embedding-for-image-to-image-hiding)
- [A One-dimensional HEVC video steganalysis method using the O...](#a-one-dimensional-hevc-video-steganalysis-method-using-the-optimality-of-predicted-motion-vectors)
- [Green Steganalyzer: A Green Learning Approach to Image Stega...](#green-steganalyzer-a-green-learning-approach-to-image-steganalysis)
- [Forensic Video Steganalysis in Spatial Domain by Noise Resid...](#forensic-video-steganalysis-in-spatial-domain-by-noise-residual-convolutional-neural-network)
- [CNN-Assisted Steganography -- Integrating Machine Learning w...](#cnn-assisted-steganography-integrating-machine-learning-with-established-steganographic-techniques)
- [3D-VFD: A Victim-free Detector against 3D Adversarial Point ...](#3d-vfd-a-victim-free-detector-against-3d-adversarial-point-clouds)
- [Deniable Steganography](#deniable-steganography)
- [Steganalysis of Image with Adaptively Parametric Activation](#steganalysis-of-image-with-adaptively-parametric-activation)
- [Secret-to-Image Reversible Transformation for Generative Ste...](#secret-to-image-reversible-transformation-for-generative-steganography)
- [Text Steganalysis with Attentional LSTM-CNN](#text-steganalysis-with-attentional-lstm-cnn)
- [Generalized Local Optimality for Video Steganalysis in Motio...](#generalized-local-optimality-for-video-steganalysis-in-motion-vector-domain)
- [Universal Deep Network for Steganalysis of Color Image based...](#universal-deep-network-for-steganalysis-of-color-image-based-on-channel-representation)
- [Stegomalware: A Systematic Survey of MalwareHiding and Detec...](#stegomalware-a-systematic-survey-of-malwarehiding-and-detection-in-images-machine-learningmodels-and-research-challenges)
- [JPEG Steganography with Embedding Cost Learning and Side-Inf...](#jpeg-steganography-with-embedding-cost-learning-and-side-information-estimation)
- [Three-Dimensional Mesh Steganography and Steganalysis: A Rev...](#three-dimensional-mesh-steganography-and-steganalysis-a-review)
- [Image Steganography based on Iteratively Adversarial Samples...](#image-steganography-based-on-iteratively-adversarial-samples-of-a-synchronized-directions-sub-image)
- [F3SNet: A Four-Step Strategy for QIM Steganalysis of Compres...](#f3snet-a-four-step-strategy-for-qim-steganalysis-of-compressed-speech-based-on-hierarchical-attention-network)
- [PixelSteganalysis: Pixel-wise Hidden Information Removal wit...](#pixelsteganalysis-pixel-wise-hidden-information-removal-with-low-visual-degradation)
- [Analysis of the Scalability of a Deep-Learning Network for S...](#analysis-of-the-scalability-of-a-deep-learning-network-for-steganography-into-the-wild)
- [Coverless Video Steganography based on Maximum DC Coefficien...](#coverless-video-steganography-based-on-maximum-dc-coefficients)
- [FCEM: A Novel Fast Correlation Extract Model For Real Time S...](#fcem-a-novel-fast-correlation-extract-model-for-real-time-steganalysis-of-voip-stream-via-multi-head-attention)
- [Evolutionary Algorithms and Efficient Data Analytics for Ima...](#evolutionary-algorithms-and-efficient-data-analytics-for-image-processing)
- [Destruction of Image Steganography using Generative Adversar...](#destruction-of-image-steganography-using-generative-adversarial-networks)
- [CIS-Net: A Novel CNN Model for Spatial Image Steganalysis vi...](#cis-net-a-novel-cnn-model-for-spatial-image-steganalysis-via-cover-image-suppression)
- [Hierarchical Representation Network for Steganalysis of QIM ...](#hierarchical-representation-network-for-steganalysis-of-qim-steganography-in-low-bit-rate-speech-signals)
- [CNN-based Steganalysis and Parametric Adversarial Embedding:...](#cnn-based-steganalysis-and-parametric-adversarial-embedding-a-game-theoretic-framework)
- [Deep Learning in steganography and steganalysis from 2015 to...](#deep-learning-in-steganography-and-steganalysis-from-2015-to-2018)
- [PixelSteganalysis: Destroying Hidden Information with a Low ...](#pixelsteganalysis-destroying-hidden-information-with-a-low-degree-of-visual-degradation)
- [Decode and Transfer: A New Steganalysis Technique via Condit...](#decode-and-transfer-a-new-steganalysis-technique-via-conditional-generative-adversarial-networks)
- [Spec-ResNet: A General Audio Steganalysis scheme based on De...](#spec-resnet-a-general-audio-steganalysis-scheme-based-on-deep-residual-network-of-spectrogram)
- [Steganographic Generative Adversarial Networks](#steganographic-generative-adversarial-networks)
- [Usage of analytic hierarchy process for steganographic inser...](#usage-of-analytic-hierarchy-process-for-steganographic-inserts-detection-in-images)
- [Feature Bagging for Steganographer Identification](#feature-bagging-for-steganographer-identification)
- [TS-CNN: Text Steganalysis from Semantic Space Based on Convo...](#ts-cnn-text-steganalysis-from-semantic-space-based-on-convolutional-neural-network)
- [Spatial Image Steganography Based on Generative Adversarial ...](#spatial-image-steganography-based-on-generative-adversarial-network)
- [DNA Steganalysis Using Deep Recurrent Neural Networks](#dna-steganalysis-using-deep-recurrent-neural-networks)
- [Coverless Information Hiding Based on Generative adversarial...](#coverless-information-hiding-based-on-generative-adversarial-networks)
- [A Novel Convolutional Neural Network for Image Steganalysis ...](#a-novel-convolutional-neural-network-for-image-steganalysis-with-shared-normalization)
- [Convolutional Neural Network Steganalysis's Application to S...](#convolutional-neural-network-steganalysiss-application-to-steganography)
- [A new adaptive method for hiding data in images](#a-new-adaptive-method-for-hiding-data-in-images)
- [On the usefulness of information hiding techniques for wirel...](#on-the-usefulness-of-information-hiding-techniques-for-wireless-sensor-networks-security)
- [Further Study on GFR Features for JPEG Steganalysis](#further-study-on-gfr-features-for-jpeg-steganalysis)
- [MoveSteg: A Method of Network Steganography Detection](#movesteg-a-method-of-network-steganography-detection)
- [Steganalyzer performances in operational contexts](#steganalyzer-performances-in-operational-contexts)
- [Steganalysis via a Convolutional Neural Network using Large ...](#steganalysis-via-a-convolutional-neural-network-using-large-convolution-filters-for-embedding-process-with-same-stego-key)
- [Steganalysis: Detecting LSB Steganographic Techniques](#steganalysis-detecting-lsb-steganographic-techniques)
- [Steganalysis of Transcoding Steganography](#steganalysis-of-transcoding-steganography)
- [Towards Steganography Detection Through Network Traffic Visu...](#towards-steganography-detection-through-network-traffic-visualisation)
- [Steganalysis Using Color Model Conversion](#steganalysis-using-color-model-conversion)
- [Stego-Image Generator (SIG) - Building Steganography Image D...](#stego-image-generator-sig-building-steganography-image-database)
- [Application of Steganography for Anonymity through the Inter...](#application-of-steganography-for-anonymity-through-the-internet)
- [Steganography and Steganalysis: Different Approaches](#steganography-and-steganalysis-different-approaches)
- [Effective Steganography Detection Based On Data Compression](#effective-steganography-detection-based-on-data-compression)
- [Spectral Estimation Methods Comparison and Performance Analy...](#spectral-estimation-methods-comparison-and-performance-analysis-on-a-steganalysis-application)
- [On the Unicity Distance of Stego Key](#on-the-unicity-distance-of-stego-key)

**[CTF Forensics Toolbox](#ctf-forensics-toolbox)**
- [Steghide](#steghide)
- [Foremost](#foremost)
- [Stegsolve](#stegsolve)
- [ExifTool](#exiftool)
- [Exiv2](#exiv2)
- [Binwalk](#binwalk)
- [Zsteg](#zsteg)
- [StegCracker](#stegcracker)
- [Fcrackzip](#fcrackzip)
- [dcode.fr](#dcodefr)
<!-- /TOC -->

## Classical Methods

---

### Visual Attack

**Goal:** Detect steganography by visual inspection of LSB planes or statistical anomalies.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Visual Attack** | 2000 | Amplified LSB plane visualization | Westfeld & Pfitzmann 2000 [[1]](https://link.springer.com/chapter/10.1007/10719724_5) |

**State of the art:** Basic but still useful for initial analysis and triage.

**Production readiness:** Production
Implemented in StegExpose, StegSpy, and most steganalysis toolkits.

**Security status:** Broken — Easily defeats naive LSB replacement; ineffective against adaptive methods

**Community acceptance:** Standard — Foundational pedagogical method

---

### Structural Attack

**Goal:** Detect steganography by analysing file structure anomalies introduced by embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Structural Attack** | 2000 | File format & histogram analysis | Westfeld & Pfitzmann 2000 [[1]](https://link.springer.com/chapter/10.1007/10719724_5) |

**State of the art:** Effective against simple LSB replacement; complementary to chi-square attack.

**Production readiness:** Production
Widely implemented in steganalysis tools.

**Security status:** Broken — Ineffective against adaptive or content-aware steganography

**Community acceptance:** Standard — Classic method; still taught and used for tool-based detection

---

### Chi-square

**Goal:** Detect LSB steganography via pair-of-values (PoV) chi-square statistical analysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chi-square** | 2000 | Pair-of-values histogram equalization test | Westfeld & Pfitzmann, IH 1999/2000 [[1]](https://link.springer.com/chapter/10.1007/10719724_5) |

**State of the art:** Classic detection method; effective only against sequential LSB replacement.

**Production readiness:** Production
Implemented in StegExpose, StegSpy, Stegdetect, and many toolkits.

**Implementations:**
- [stegdetect](https://github.com/abeluck/stegdetect) ⭐ 156 — C, classic CLI steganalysis tool

**Security status:** Broken — Defeated by random pixel selection or adaptive embedding

**Community acceptance:** Standard — Foundational method; every steganalysis course covers it

---

### RS-analysis

**Goal:** Detect and estimate LSB steganography payload via Regular/Singular group analysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **RS-analysis** | 2001 | Regular/Singular group flipping analysis of LSB and shifted-LSB planes | Fridrich, Goljan & Du, ACM MM&Sec 2001 [[1]](https://dl.acm.org/doi/10.1145/1232454.1232466) |

**State of the art:** Very effective against both sequential and random LSB embedding; can detect messages as short as 0.03 bpp.

**Production readiness:** Production
Implemented in StegExpose and most forensic steganalysis tools.

**Security status:** Broken against naive LSB — Effective detector; defeated only by content-adaptive embedding (HUGO, WOW, etc.)

**Community acceptance:** Standard — Widely cited; de facto LSB steganalysis benchmark

---

### Weighted Stego

**Goal:** Estimate LSB embedding rate using a weighted stego-image predictor.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Weighted Stego (WS)** | 2004 | Weighted prediction of cover pixels to estimate payload length | Fridrich & Goljan, SPIE 5306 2004 [[1]](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/5306/1/On-estimation-of-secret-message-length-in-LSB-steganography-in/10.1117/12.521350.short) |

**State of the art:** Quantitative estimator for LSB replacement payload; more precise than chi-square or RS for rate estimation.

**Production readiness:** Production
Implemented in academic toolkits; available from Binghamton DDE Lab.

**Security status:** Broken against naive LSB — Effective estimator; defeated by non-LSB-replacement schemes

**Community acceptance:** Standard — Foundational quantitative steganalysis method

---

### SPAM

**Goal:** Detect spatial-domain steganography using subtractive pixel adjacency matrix co-occurrence features.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SPAM** | 2010 | 686-dimensional Markov chain co-occurrence features of pixel differences | Pevný, Bas & Fridrich, IEEE TIFS 2010 [[1]](https://ieeexplore.ieee.org/document/5437325/) |

**State of the art:** Predecessor to SRM rich model; superior to chi-square/RS for LSB matching detection.

**Production readiness:** Production
Available from Binghamton DDE Lab feature extractor suite.

**Security status:** Caution — Effective against LSB matching; weaker against adaptive embedding (HUGO, WOW)

**Community acceptance:** Standard — Foundational rich-model steganalysis; widely reproduced

---

### SRM

**Goal:** Comprehensive spatial rich model for steganalysis using 34,671-dimensional feature ensemble.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SRM** | 2012 | Union of 106 diverse submodels from quantized noise residuals | Fridrich & Kodovský, IEEE TIFS 2012 [[1]](https://ieeexplore.ieee.org/document/6197267/) |

**State of the art:** De facto standard spatial-domain steganalysis feature set for years; now complemented/superseded by deep learning (YeNet, SRNet).

**Production readiness:** Production
Available from Binghamton DDE Lab; implemented in many open-source tools.

**Implementations:**
- [ALASKA2 steganalysis tools](https://github.com/YassineYousfi/alaska2-steganalysis) ⭐ 312 — Python, includes SRM features

**Security status:** Caution — Effective against most spatial-domain schemes; weaker against WOW/S-UNIWARD at low payloads

**Community acceptance:** Standard — De facto standard for over a decade

---

### DCTR

**Goal:** Detect JPEG steganography using low-complexity undecimated DCT residual features.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DCTR** | 2015 | First-order statistics of 64 undecimated DCT kernel residuals | Holub & Fridrich, IEEE TIFS 2015 [[1]](https://www.semanticscholar.org/paper/Low-Complexity-Features-for-JPEG-Steganalysis-Using-Holub-Fridrich/7caf1fd0a02d9f111be720efe053a6d83b8afc45) |

**State of the art:** Low-complexity JPEG-specific rich model; competitive with JPEG-domain SRM at fraction of dimensionality.

**Production readiness:** Production
Available from Binghamton DDE Lab feature extractor suite.

**Security status:** Caution — Effective against J-UNIWARD and nsF5; weaker at very low payloads

**Community acceptance:** Standard — Widely adopted JPEG steganalysis baseline

---

## Deep Learning

---

### XuNet

**Goal:** First CNN steganalyser purpose-designed with steganalysis-specific architectural choices.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **XuNet** | 2016 | 5-layer CNN with abs activation + TanH saturation + 1×1 convolutions | Xu, Wu & Shi, IEEE SPL 2016 [[1]](https://ieeexplore.ieee.org/document/7444146/) |

**State of the art:** Foundational deep learning steganalysis; competitive with SRM on BOSSbase; superseded by YeNet and SRNet.

**Production readiness:** Production
Multiple open-source implementations available.

**Implementations:**
- [xunet](https://github.com/brijeshiitg/XuNet-Structural-Design-of-Convolutional-Neural-Networksfor-Steganalysis) ⭐ 89 — Python/PyTorch

**Security status:** Caution — Effective at moderate payloads; weaker than SRM at low payloads

**Community acceptance:** Standard — Foundational DL steganalysis paper

---

### YeNet

**Goal:** CNN steganalyser with SRM-initialised preprocessing layer and TLU activation.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **YeNet** | 2017 | 8-layer CNN + SRM-filter preprocessing + TLU activation | Ye, Ni & Yi, IEEE TIFS 2017 [[1]](https://ieeexplore.ieee.org/document/7937836/) |

**State of the art:** ~10% accuracy improvement over XuNet; superseded by SRNet (2019) and transformer-based detectors.

**Production readiness:** Production
Multiple open-source implementations available.

**Implementations:**
- [TensorFlow-YeNet](https://github.com/changshihyoung/TensorFlow-YeNet) ⭐ 156 — Python/TensorFlow
- [Pytorch-YeNet](https://github.com/brijeshiitg/Pytorch-Implementation-of-YeNet-Deep-Learning-Hierarchical-Representations-for-Image-Steganalysis-) ⭐ 89 — Python/PyTorch

**Security status:** Caution — Effective against spatial-domain schemes; weaker against content-adaptive embedding

**Community acceptance:** Standard — Widely reproduced benchmark

---

### SRNet

**Goal:** End-to-end deep residual CNN steganalysis without heuristic preprocessing.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SRNet** | 2019 | Deep residual network; expanded front part with no pooling | Boroumand, Chen & Fridrich, IEEE TIFS 2019 [[1]](https://ieeexplore.ieee.org/document/8470101/) |

**State of the art:** State-of-the-art 2019–2022 for both spatial and JPEG domains; universal detector design.

**Production readiness:** Production
Multiple open-source implementations available.

**Implementations:**
- [Deep-Steganalysis](https://github.com/albblgb/Deep-Steganalysis) ⭐ 156 — Python/PyTorch, includes SRNet

**Security status:** Caution — Strong universal detector; weaker against content-adaptive embedding at very low payloads

**Community acceptance:** Standard — De facto DL steganalysis baseline 2019–2022

---

### ZhuNet

**Goal:** Efficient spatial CNN steganalyser using depth-wise separable convolutions and multi-level pooling.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **ZhuNet** | 2020 | Depth-wise separable convolutions + multi-level pooling | Zhang et al., IEEE TIFS 2020 [[1]](https://ieeexplore.ieee.org/document/8809687/) |

**State of the art:** Competitive with SRNet at lower computational cost; efficient spatial-domain steganalysis.

**Production readiness:** Production
Official implementation available on GitHub.

**Implementations:**
- [Zhu-Net-image-steganalysis](https://github.com/1204BUPT/Zhu-Net-image-steganalysis) ⭐ 89 — Python/PyTorch, official implementation

**Security status:** Caution — Effective against standard spatial-domain schemes; performance drops at very low payloads

**Community acceptance:** Standard — Published in IEEE TIFS; widely cited

---

## Network Steganalysis

---

### Tor Traffic Detection

**Goal:** Detect Tor and pluggable transport traffic via machine learning on network flow features.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Tor Detection** | 2015 | CNN/ML on packet sizes, timing, flow statistics | Ling et al. 2015; reviewed in [[1]](https://arxiv.org/abs/2311.16276) |

**State of the art:** Modern approaches use deep learning on packet-level features; effective against vanilla Tor but harder against obfs4/REALITY.

**Production readiness:** Production
Used in national-level DPI systems and academic research.

**Security status:** Caution — Effective against unobfuscated Tor; partially defeated by pluggable transports

**Community acceptance:** Standard — Active research area; many published systems

---

### DNS Tunnel Detection

**Goal:** Detect DNS tunneling covert channels via statistical analysis of query patterns.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DNS Tunnel Detection** | 2010 | Query length, entropy, frequency, hostname count statistics | Born & Gustafson 2010; reviewed in [[1]](https://scispace.com/pdf/dns-tunneling-detection-techniques-classification-and-2j1hj4gxsm.pdf) |

**State of the art:** Effective against tools like iodine and dnscat2; modern ML-based detectors achieve >99% accuracy.

**Production readiness:** Production
Deployed in enterprise firewalls and DNS security platforms (Cisco Umbrella, etc.).

**Security status:** Caution — Effective against high-bandwidth tunnels; low-throughput exfiltration harder to detect

**Community acceptance:** Standard — Well-studied; multiple production implementations

---

### Stego Battlefield

**Goal:** Evaluate image steganography attacks and steganalysis defenses in a standardized framework.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Stego Battlefield** | 2026 | Comprehensive attack/defense evaluation benchmark | Sun et al., arXiv May 2026 [[1]](https://arxiv.org/abs/2605.05789) |

**State of the art:** Provides standardized evaluation framework covering both attack and defense perspectives; addresses covert channel abuse in large model pipelines.

**Production readiness:** Research
Preprint May 2026; benchmark suite under development.

**Implementations:** Academic benchmark — code not yet publicly released

**Security status:** Caution — Benchmark reveals gaps in current steganalysis defenses

**Community acceptance:** Emerging — Very recent; addresses timely LLM-era threat model

---

### Zero-Shot Interpretable Image Steganalysis

**Goal:** Zero-shot detection of invertible image hiding methods with interpretability.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Zero-Shot Interpretable** | 2026 | Zero-shot learning | Invertible image hiding [[1]](https://arxiv.org/abs/2605.01331) |

**State of the art:** Addresses detectability of emerging invertible image hiding approaches.

**Production readiness:** Research
Preprint 2026; no public implementation.

**Security status:** Caution — Effective against invertible hiding; applicability to other schemes unclear

**Community acceptance:** Emerging — Very recent

---

### Targeted Pooled Latent-Space Steganalysis

**Goal:** Detect steganography in latent space of generative models.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Pooled Latent-Space** | 2025 | Latent space analysis | Generative steganography [[1]](https://arxiv.org/abs/2510.12414) |

**State of the art:** Analyzes statistical distribution of latent vector norm to detect embedding.

**Production readiness:** Research
Preprint 2025; research prototype.

**Security status:** Caution — Targets generative steganography specifically; limited to latent-space embedding methods

**Community acceptance:** Emerging

---

### Systematically Deconstructing APVD Steganography

**Goal:** Detect Adaptive Pixel Value Differencing steganography using deep learning.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **APVD Detection** | 2025 | Deep learning approach | APVD steganography [[1]](https://arxiv.org/abs/2511.16604) |

**State of the art:** Unified deep learning paradigm for APVD detection.

**Production readiness:** Research
Preprint 2025; no public implementation.

**Security status:** Caution — Effective against APVD family; applicability to other PVD variants needs verification

**Community acceptance:** Emerging

## Recent arXiv Papers (2024–2026)

---

### A Game-Theoretic Approach for Adversarial Information Fusion in Distributed Sensor Networks

**Goal:** disciplines of signal processing have received increasing attention in the last decades: multimedia forensics, digital watermarking, biometrics, network monitoring, steganography and steganalysis a...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Game-Theoretic Approach for Adversarial Information Fusion** | 2025 | cs.CR, cs.GT, cs.MA | Kassem Kallas [[1]](https://arxiv.org/abs/2511.23026) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Exploring AI in Steganography and Steganalysis: Trends, Clusters, and Sustainable Development Potential

**Goal:** Steganography and steganalysis are strongly related subjects of information security.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Exploring AI in Steganography and Steganalysis: Trends, Clus** | 2025 | cs.CR, cs.AI | Aditya Kumar Sahu et al. [[1]](https://arxiv.org/abs/2511.12052) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### GSDFuse: Capturing Cognitive Inconsistencies from Multi-Dimensional Weak Signals in Social Media Steganalysis

**Goal:** The ubiquity of social media platforms facilitates malicious linguistic steganography, posing significant security risks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **GSDFuse: Capturing Cognitive Inconsistencies from Multi-Dime** | 2025 | cs.CR, cs.AI, cs.CL | Kaibo Huang et al. [[1]](https://arxiv.org/abs/2505.17085) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A study on audio synchronous steganography detection and distributed guide inference model based on sliding spectral features and intelligent inference drive

**Goal:** data in audio synchronization streams has emerged as a new covert communication method.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A study on audio synchronous steganography detection and dis** | 2025 | cs.SD, cs.AI, cs.CR | Wei Meng [[1]](https://arxiv.org/abs/2505.03193) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### TSCL:Multi-party loss Balancing scheme for deep learning Image steganography based on Curriculum learning

**Goal:** For deep learning-based image steganography frameworks, in order to ensure the invisibility and recoverability of the information embedding, the loss function usually contains several losses such a...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **TSCL:Multi-party loss Balancing scheme for deep learning Ima** | 2025 | cs.CV, cs.AI, cs.CR | Fengchun Liu. Tong Zhang, Chunying Zhang [[1]](https://arxiv.org/abs/2504.18348) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Efficient Streaming Voice Steganalysis in Challenging Detection Scenarios

**Goal:** stream segments, making the steganographic features of hard-to-detect samples more pronounced and easier to learn.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Efficient Streaming Voice Steganalysis in Challenging Detect** | 2024 | cs.CR, cs.LG, cs.SD | Pengcheng Zhou et al. [[1]](https://arxiv.org/abs/2411.13612) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Linguistic Steganalysis via LLMs: Two Modes for Efficient Detection of Strongly Concealed Stego

**Goal:** in complex scenarios, linguistic steganalysis (LS) with various motivations has been proposed and achieved excellent performance.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Linguistic Steganalysis via LLMs: Two Modes for Efficient De** | 2024 | cs.CL | Yifan Tang et al. [[1]](https://arxiv.org/abs/2406.04218) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Blind Data Adaptation to tackle Covariate Shift in Operational Steganalysis

**Goal:** The proliferation of image manipulation for unethical purposes poses significant challenges in social networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Blind Data Adaptation to tackle Covariate Shift in Operation** | 2024 | eess.IV, cs.AI, cs.CR | Rony Abecidan et al. [[1]](https://arxiv.org/abs/2405.16961) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Towards Next-Generation Steganalysis: LLMs Unleash the Power of Detecting Steganography

**Goal:** Linguistic steganography provides convenient implementation to hide messages, particularly with the emergence of AI generation technology.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Next-Generation Steganalysis: LLMs Unleash the Power** | 2024 | cs.CR | Minhao Bai. Jinshuai Yang et al. [[1]](https://arxiv.org/abs/2405.09090) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Double-Flow-based Steganography without Embedding for Image-to-Image Hiding

**Goal:** As an emerging concept, steganography without embedding (SWE) hides a secret message without directly embedding it into a cover.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Double-Flow-based Steganography without Embedding for Image-** | 2023 | cs.CV | Bingbing Song et al. [[1]](https://arxiv.org/abs/2311.15027) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A One-dimensional HEVC video steganalysis method using the Optimality of Predicted Motion Vectors

**Goal:** Among steganalysis techniques, detection against motion vector (MV) domain-based video steganography in High Efficiency Video Coding (HEVC) standard remains a hot and challenging issue.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A One-dimensional HEVC video steganalysis method using the O** | 2023 | cs.CR, cs.LG, cs.MM | Jun Li et al. [[1]](https://arxiv.org/abs/2308.06464) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Green Steganalyzer: A Green Learning Approach to Image Steganalysis

**Goal:** to make final image-level classification.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Green Steganalyzer: A Green Learning Approach to Image Stega** | 2023 | eess.IV, cs.CR, cs.LG | Yao Zhu et al. [[1]](https://arxiv.org/abs/2306.04008) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Forensic Video Steganalysis in Spatial Domain by Noise Residual Convolutional Neural Network

**Goal:** This research evaluates a convolutional neural network (CNN) based approach to forensic video steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Forensic Video Steganalysis in Spatial Domain by Noise Resid** | 2023 | cs.CV, cs.CR | Mart Keizer, Zeno Geradts, Meike Kombrink [[1]](https://arxiv.org/abs/2305.18070) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### CNN-Assisted Steganography -- Integrating Machine Learning with Established Steganographic Techniques

**Goal:** We propose a method to improve steganography by increasing the resilience of stego-media to discovery through steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CNN-Assisted Steganography -- Integrating Machine Learning w** | 2023 | cs.CR, cs.LG, cs.MM | Andrew Havard et al. [[1]](https://arxiv.org/abs/2304.12503) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### 3D-VFD: A Victim-free Detector against 3D Adversarial Point Clouds

**Goal:** in computer vision. However, recent studies have shown they are vulnerable to 3D adversarial point clouds.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **3D-VFD: A Victim-free Detector against 3D Adversarial Point ** | 2023 | cs.MM, cs.CV, eess.IV | Jiahao Zhu et al. [[1]](https://arxiv.org/abs/2205.08738) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Deniable Steganography

**Goal:** Steganography conceals the secret message into the cover media, generating a stego media which can be transmitted on public channels without drawing suspicion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Deniable Steganography** | 2022 | cs.CR, cs.CV | Yong Xu et al. [[1]](https://arxiv.org/abs/2205.12587) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganalysis of Image with Adaptively Parametric Activation

**Goal:** Steganalysis as a method to detect whether image contains se-cret message, is a crucial study avoiding the imperils from abus-ing steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis of Image with Adaptively Parametric Activation** | 2022 | cs.MM, cs.CR, cs.CV | Hai Su et al. [[1]](https://arxiv.org/abs/2203.12843) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Secret-to-Image Reversible Transformation for Generative Steganography

**Goal:** Recently, generative steganography that transforms secret information to a generated image has been a promising technique to resist steganalysis detection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secret-to-Image Reversible Transformation for Generative Ste** | 2022 | cs.CR | Zhili Zhou et al. [[1]](https://arxiv.org/abs/2203.06598) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Text Steganalysis with Attentional LSTM-CNN

**Goal:** With the rapid development of Natural Language Processing (NLP) technologies, text steganography methods have been significantly innovated recently, which poses a great threat to cybersecurity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Text Steganalysis with Attentional LSTM-CNN** | 2022 | cs.MM | YongJian Bao et al. [[1]](https://arxiv.org/abs/1912.12871) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generalized Local Optimality for Video Steganalysis in Motion Vector Domain

**Goal:** motion vectors (MVs) is an intrinsic property in video coding, and any modifications to the MVs will inevitably destroy this optimality, making it a sensitive indicator of steganography in the MV d...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generalized Local Optimality for Video Steganalysis in Motio** | 2021 | cs.CV, cs.CR | Liming Zhai et al. [[1]](https://arxiv.org/abs/2112.11729) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Universal Deep Network for Steganalysis of Color Image based on Channel Representation

**Goal:** in each color channel, in preprocessing module, we firstly separate the input image into three channels according to the corresponding embedding spaces (i.e.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Universal Deep Network for Steganalysis of Color Image based** | 2021 | cs.CV, cs.CR | Kangkang Wei et al. [[1]](https://arxiv.org/abs/2111.12231) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Stegomalware: A Systematic Survey of MalwareHiding and Detection in Images, Machine LearningModels and Research Challenges

**Goal:** malware analysis, and the malware detection capabilities of these files has been well advanced for real-time detection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegomalware: A Systematic Survey of MalwareHiding and Detec** | 2021 | cs.CR | Rajasekhar Chaganti et al. [[1]](https://arxiv.org/abs/2110.02504) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### JPEG Steganography with Embedding Cost Learning and Side-Information Estimation

**Goal:** A great challenge to steganography has arisen with the wide application of steganalysis methods based on convolutional neural networks (CNNs).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **JPEG Steganography with Embedding Cost Learning and Side-Inf** | 2021 | cs.MM | Jianhua Yang et al. [[1]](https://arxiv.org/abs/2107.13151) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Three-Dimensional Mesh Steganography and Steganalysis: A Review

**Goal:** and volumes. Over the past decade, 3-D meshes have emerged in industrial, medical, and entertainment applications, being of large practical significance for 3-D mesh steganography and steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Three-Dimensional Mesh Steganography and Steganalysis: A Rev** | 2021 | cs.CR, cs.GR | Hang Zhou et al. [[1]](https://arxiv.org/abs/2104.10203) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography based on Iteratively Adversarial Samples of A Synchronized-directions Sub-image

**Goal:** Nowadays a steganography has to face challenges of both feature based staganalysis and convolutional neural network (CNN) based steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography based on Iteratively Adversarial Samples** | 2021 | cs.CV | Xinghong Qin et al. [[1]](https://arxiv.org/abs/2101.05209) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### F3SNet: A Four-Step Strategy for QIM Steganalysis of Compressed Speech Based on Hierarchical Attention Network

**Goal:** which vectors have a greater impact on the final classification result.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **F3SNet: A Four-Step Strategy for QIM Steganalysis of Compres** | 2021 | cs.CR | Chuanpeng Guo, Wei Yang, Liusheng Huang [[1]](https://arxiv.org/abs/2101.05105) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### PixelSteganalysis: Pixel-wise Hidden Information Removal with Low Visual Degradation

**Goal:** Recently, the field of steganography has experienced rapid developments based on deep learning (DL).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **PixelSteganalysis: Pixel-wise Hidden Information Removal wit** | 2021 | cs.MM, cs.CR, cs.CV | Dahuin Jung et al. [[1]](https://arxiv.org/abs/1902.10905) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Analysis of the Scalability of a Deep-Learning Network for Steganography "Into the Wild"

**Goal:** Since the emergence of deep learning and its adoption in steganalysis fields, most of the reference articles kept using small to medium size CNN, and learn them on relatively small databases.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Analysis of the Scalability of a Deep-Learning Network for S** | 2020 | cs.CR | Hugo Ruiz et al. [[1]](https://arxiv.org/abs/2012.14816) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Coverless Video Steganography based on Maximum DC Coefficients

**Goal:** Coverless steganography has been a great interest in recent years, since it is a technology that can absolutely resist the detection of steganalysis by not modifying the carriers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Coverless Video Steganography based on Maximum DC Coefficien** | 2020 | cs.MM, cs.CR | Laijin Meng et al. [[1]](https://arxiv.org/abs/2012.06809) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### FCEM: A Novel Fast Correlation Extract Model For Real Time Steganalysis of VoIP Stream via Multi-head Attention

**Goal:** to their highly parallelizable computation and flexibility in modeling correlation in sequence, to tackle steganalysis problem of Quantization Index Modulation (QIM) based steganography in compress...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **FCEM: A Novel Fast Correlation Extract Model For Real Time S** | 2020 | cs.MM | Hao Yang et al. [[1]](https://arxiv.org/abs/1911.00682) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Evolutionary Algorithms and Efficient Data Analytics for Image Processing

**Goal:** Steganography algorithms facilitate communication between a source and a destination in a secret manner.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Evolutionary Algorithms and Efficient Data Analytics for Ima** | 2020 | cs.CV, cs.LG, cs.MM | Farid Ghareh Mohammadi et al. [[1]](https://arxiv.org/abs/1907.12914) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Destruction of Image Steganography using Generative Adversarial Networks

**Goal:** Digital image steganalysis, or the detection of image steganography, has been studied in depth for years and is driven by Advanced Persistent Threat (APT) groups', such as APT37 Reaper, utilization...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Destruction of Image Steganography using Generative Adversar** | 2019 | cs.MM, cs.CR, cs.LG | Isaac Corley, Jonathan Lwowski, Justin Hoffman [[1]](https://arxiv.org/abs/1912.10070) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### CIS-Net: A Novel CNN Model for Spatial Image Steganalysis via Cover Image Suppression

**Goal:** classification of cover images and stego images easier is the key of this task.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CIS-Net: A Novel CNN Model for Spatial Image Steganalysis vi** | 2019 | cs.MM, eess.IV | Songtao Wu et al. [[1]](https://arxiv.org/abs/1912.06540) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hierarchical Representation Network for Steganalysis of QIM Steganography in Low-Bit-Rate Speech Signals

**Goal:** With the Volume of Voice over IP (VoIP) traffic rises shapely, more and more VoIP-based steganography methods have emerged in recent years, which poses a great threat to the security of cyberspace.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hierarchical Representation Network for Steganalysis of QIM ** | 2019 | cs.MM | Hao Yang et al. [[1]](https://arxiv.org/abs/1910.04433) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### CNN-based Steganalysis and Parametric Adversarial Embedding: a Game-Theoretic Framework

**Goal:** CNN-based steganalysis has recently achieved very good performance in detecting content-adaptive steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CNN-based Steganalysis and Parametric Adversarial Embedding:** | 2019 | cs.MM, cs.GT | Xiaoyu Shi et al. [[1]](https://arxiv.org/abs/1906.00697) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Deep Learning in steganography and steganalysis from 2015 to 2018

**Goal:** of a deep neural network, in a generic way and present the networks proposed in existing literature for the different scenarios of steganalysis, and finally, we will discuss steganography by deep l...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Deep Learning in steganography and steganalysis from 2015 to** | 2019 | cs.CR | Marc Chaumont [[1]](https://arxiv.org/abs/1904.01444) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### PixelSteganalysis: Destroying Hidden Information with a Low Degree of Visual Degradation

**Goal:** Steganography is the science of unnoticeably concealing a secret message within a certain image, called a cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **PixelSteganalysis: Destroying Hidden Information with a Low ** | 2019 | cs.MM, cs.CR, cs.LG | Dahuin Jung et al. [[1]](https://arxiv.org/abs/1902.11113) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Decode and Transfer: A New Steganalysis Technique via Conditional Generative Adversarial Networks

**Goal:** to discover the secret image using conventional methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Decode and Transfer: A New Steganalysis Technique via Condit** | 2019 | cs.CR | Parisa Babaheidarian, Mark Wallace [[1]](https://arxiv.org/abs/1901.09746) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Spec-ResNet: A General Audio Steganalysis scheme based on Deep Residual Network of Spectrogram

**Goal:** are only effective in the specific embedded domain.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Spec-ResNet: A General Audio Steganalysis scheme based on De** | 2019 | cs.MM | Yanzhen Ren et al. [[1]](https://arxiv.org/abs/1901.06838) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganographic Generative Adversarial Networks

**Goal:** Steganography is collection of methods to hide secret information ("payload") within non-secret information "container").

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganographic Generative Adversarial Networks** | 2019 | cs.MM, cs.CR, cs.CV | Denis Volkhonskiy, Ivan Nazarov, Evgeny Burnaev [[1]](https://arxiv.org/abs/1703.05502) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Usage of analytic hierarchy process for steganographic inserts detection in images

**Goal:** This article presents the method of steganography detection, which is formed by replacing the least significant bit (LSB).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Usage of analytic hierarchy process for steganographic inser** | 2018 | cs.MM, cs.CV, cs.GR | S. V. Belim, D. E. Vilkhovskiy [[1]](https://arxiv.org/abs/1902.11100) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Feature Bagging for Steganographer Identification

**Goal:** Traditional steganalysis algorithms focus on detecting the existence of steganography in a single object.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Feature Bagging for Steganographer Identification** | 2018 | cs.MM | Hanzhou Wu [[1]](https://arxiv.org/abs/1810.11973) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### TS-CNN: Text Steganalysis from Semantic Space Based on Convolutional Neural Network

**Goal:** cybersecurity that helps to identify covert attacks in public network.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **TS-CNN: Text Steganalysis from Semantic Space Based on Convo** | 2018 | cs.CR | Zhongliang Yang et al. [[1]](https://arxiv.org/abs/1810.08136) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Spatial Image Steganography Based on Generative Adversarial Network

**Goal:** With the recent development of deep learning on steganalysis, embedding secret information into digital images faces great challenges.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Spatial Image Steganography Based on Generative Adversarial ** | 2018 | cs.MM | Jianhua Yang et al. [[1]](https://arxiv.org/abs/1804.07939) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### DNA Steganalysis Using Deep Recurrent Neural Networks

**Goal:** Recent advances in next-generation sequencing technologies have facilitated the use of deoxyribonucleic acid (DNA) as a novel covert channels in steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **DNA Steganalysis Using Deep Recurrent Neural Networks** | 2018 | cs.LG, cs.MM | Ho Bae et al. [[1]](https://arxiv.org/abs/1704.08443) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Coverless Information Hiding Based on Generative adversarial networks

**Goal:** Traditional image steganography modifies the content of the image more or less, it is hard to resist the detection of image steganalysis tools.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Coverless Information Hiding Based on Generative adversarial** | 2017 | cs.CR, cs.MM | Ming-ming Liu et al. [[1]](https://arxiv.org/abs/1712.06951) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Convolutional Neural Network for Image Steganalysis with Shared Normalization

**Goal:** attracted increasing attentions in recent years.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Convolutional Neural Network for Image Steganalysis ** | 2017 | cs.MM | Songtao Wu, Sheng-hua Zhong, Yan Liu [[1]](https://arxiv.org/abs/1711.07306) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Convolutional Neural Network Steganalysis's Application to Steganography

**Goal:** This paper presents a novel approach to increase the performance bounds of image steganography under the criteria of minimizing distortion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Convolutional Neural Network Steganalysis's Application to S** | 2017 | cs.MM | Mehdi Sharifzadeh et al. [[1]](https://arxiv.org/abs/1711.02581) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A new adaptive method for hiding data in images

**Goal:** LSB method is one of the well-known steganography methods which hides the message bits into the least significant bit of pixel values.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A new adaptive method for hiding data in images** | 2017 | cs.MM, cs.CR | Kazem Qazanfari, Reza Safabaksh [[1]](https://arxiv.org/abs/1709.06729) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On the usefulness of information hiding techniques for wireless sensor networks security

**Goal:** the whole network at a certain time snapshot can be visualized as an image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On the usefulness of information hiding techniques for wirel** | 2017 | cs.MM, cs.SE | Rola Al-Sharif et al. [[1]](https://arxiv.org/abs/1706.08136) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Further Study on GFR Features for JPEG Steganalysis

**Goal:** Filter Residual) features, built as histograms of quantized residuals obtained with 2D Gabor filters, can achieve competitive detection performance against adaptive JPEG steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Further Study on GFR Features for JPEG Steganalysis** | 2017 | cs.MM | Xia Chao, Guan Qingxiao, Zhao Xianfeng [[1]](https://arxiv.org/abs/1706.07576) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### MoveSteg: A Method of Network Steganography Detection

**Goal:** This article presents a new method for detecting a source point of time based network steganography - MoveSteg.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **MoveSteg: A Method of Network Steganography Detection** | 2016 | cs.MM, cs.CR | Krzysztof Szczypiorski, Tomasz Tyl [[1]](https://arxiv.org/abs/1610.01955) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganalyzer performances in operational contexts

**Goal:** Steganography and steganalysis are two important branches of the information hiding field of research.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalyzer performances in operational contexts** | 2016 | cs.MM, cs.CR | Yousra A. Fadil et al. [[1]](https://arxiv.org/abs/1608.05850) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganalysis via a Convolutional Neural Network using Large Convolution Filters for Embedding Process with Same Stego Key

**Goal:** For the past few years, in the race between image steganography and steganalysis, deep learning has emerged as a very promising alternative to steganalyzer approaches based on rich image models com...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis via a Convolutional Neural Network using Large ** | 2016 | cs.MM | Jean-François Couchot et al. [[1]](https://arxiv.org/abs/1605.07946) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganalysis: Detecting LSB Steganographic Techniques

**Goal:** Steganalysis means analysis of stego images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis: Detecting LSB Steganographic Techniques** | 2014 | cs.MM, cs.CR | Tanmoy Sarkar, Sugata Sanyal [[1]](https://arxiv.org/abs/1405.5119) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganalysis of Transcoding Steganography

**Goal:** TranSteg (Trancoding Steganography) is a fairly new IP telephony steganographic method that functions by compressing overt (voice) data to make space for the steganogram by means of transcoding.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis of Transcoding Steganography** | 2012 | cs.CR, cs.MM | Artur Janicki, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1210.5888) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Towards Steganography Detection Through Network Traffic Visualisation

**Goal:** the proposed approach is the lack of direct, linear time dependencies for the created network traffic visualisations.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Steganography Detection Through Network Traffic Visu** | 2012 | cs.CR | Wojciech Mazurczyk, Krzysztof Szczypiorski, Bartosz Jankowski [[1]](https://arxiv.org/abs/1208.2861) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganalysis Using Color Model Conversion

**Goal:** Bit Steganographic algorithms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis Using Color Model Conversion** | 2012 | cs.CR | P. Thiyagarajan, G. Aghila, V. Prasanna Venkatesan [[1]](https://arxiv.org/abs/1206.2914) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Stego-Image Generator (SIG) - Building Steganography Image Database

**Goal:** Steganographic algorithms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stego-Image Generator (SIG) - Building Steganography Image D** | 2012 | cs.CR | P. Thiyagarajan, G. Aghila, V. Prasanna Venkatesan [[1]](https://arxiv.org/abs/1206.2586) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Application of Steganography for Anonymity through the Internet

**Goal:** the highest level of security in a well defined and studied category of attacks called "watermark-only attack".

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Application of Steganography for Anonymity through the Inter** | 2012 | cs.CR, cs.IT | Jacques M. Bahi et al. [[1]](https://arxiv.org/abs/1202.5302) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography and Steganalysis: Different Approaches

**Goal:** Steganography is the technique of hiding confidential information within any media.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography and Steganalysis: Different Approaches** | 2011 | cs.CR | Soumyendu Das et al. [[1]](https://arxiv.org/abs/1111.3758) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Effective Steganography Detection Based On Data Compression

**Goal:** This article describes novel text steganalysis method.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Effective Steganography Detection Based On Data Compression** | 2011 | cs.CR | Ivan Nechta [[1]](https://arxiv.org/abs/1110.3466) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint stage; community evaluation ongoing.

---

### Spectral Estimation Methods Comparison and Performance Analysis on a Steganalysis Application

**Goal:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the intended recipient knows of the existence of the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Spectral Estimation Methods Comparison and Performance Analy** | 2011 | cs.CR | Tolga Mataracioglu, Unal Tatar [[1]](https://arxiv.org/abs/1108.2152) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On the Unicity Distance of Stego Key

**Goal:** Steganography is about how to send secret message covertly.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On the Unicity Distance of Stego Key** | 2005 | cs.CR | Zhang Weiming, Li Shiqu [[1]](https://arxiv.org/abs/cs/0504083) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

## CTF Forensics Toolbox

---

### Steghide

**Goal:** Embed and extract secret data in JPEG, BMP, WAV, and AU files using passphrase encryption.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steghide** | 2003 | DCT/spatial LSB with AES-128 | Passphrase-protected extraction [[1]](https://github.com/StefanoDeVuono/steghide) |

**State of the art:** De facto standard for simple passphrase-based image/audio stego in CTF contexts. Widely available via apt.

**Production readiness:** Mature
Widely deployed in CTF challenges; stable, no active development.

**Implementations:**
- [StefanoDeVuono/steghide](https://github.com/StefanoDeVuono/steghide) ⭐ 310 — C++, canonical mirror
- [StegHigh/steghide](https://github.com/StegHigh/steghide) ⭐ 727 — C++, active fork

**Security status:** Caution
Passphrase brute-forceable with StegCracker; detectable via RS-analysis if payload is large.

**Community acceptance:** Standard
Universally recognized CTF tool; academic baseline for steganalysis benchmarks.

---

### Foremost

**Goal:** Recover files from binary streams by matching known file headers and footers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Foremost** | 2001 | Header/footer pattern matching | Recovers embedded files without filesystem [[1]](https://github.com/korczis/foremost) |

**State of the art:** Standard forensic carving tool. Used alongside binwalk for extracting files hidden by appending or concatenation.

**Production readiness:** Mature
Stable tool, available in major distro repos.

**Implementations:**
- [korczis/foremost](https://github.com/korczis/foremost) ⭐ 367 — C, Linux/macOS

**Security status:** Caution
Only recovers files with known signatures; custom containers evade detection.

**Community acceptance:** Standard
Industry-standard forensic carving tool used in law enforcement and CTF alike.

---

### Stegsolve

**Goal:** Apply color-channel filters and bit-plane analysis to images to visually reveal hidden data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegsolve** | 2010 | Bit-plane/color-filter visualization | Interactive Java GUI for LSB analysis [[1]](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve) |

**State of the art:** Essential CTF image steg tool. Pairs with zsteg for automated detection. No equivalent one-click GUI alternative.

**Production readiness:** Mature
Widely used in CTF; archived but functional.

**Implementations:**
- [eugenekolo/sec-tools](https://github.com/eugenekolo/sec-tools) ⭐ 684 — Java, contains stegsolve jar

**Security status:** Caution
Reveals only visually encoded data; ineffective against encrypted or transform-domain stego.

**Community acceptance:** Standard
Referenced in virtually every CTF stego write-up.

---

### ExifTool

**Goal:** Read, write, and edit metadata in image, audio, video, and document files.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ExifTool** | 2003 | Metadata parser for 100+ formats | Supports EXIF, IPTC, XMP, GPS, and custom tags [[1]](https://exiftool.org/) |

**State of the art:** Gold standard for metadata inspection. Flags hidden data stored in EXIF comments, GPS fields, or custom tags.

**Production readiness:** Production
Actively maintained; used in professional digital forensics.

**Implementations:**
- [exiftool.org](https://exiftool.org/) — Perl, cross-platform

**Security status:** Caution
Metadata can be stripped or forged; does not detect payload in pixel data.

**Community acceptance:** Standard
Universally trusted in forensics and photography workflows.

---

### Exiv2

**Goal:** Inspect and manipulate EXIF, IPTC, and XMP metadata in image files.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Exiv2** | 2004 | C++ metadata library | Fast CLI and library interface [[1]](https://www.exiv2.org/) [[2]](https://github.com/Exiv2/exiv2) |

**State of the art:** Lightweight alternative to ExifTool for metadata inspection. Used in CTF when ExifTool is unavailable.

**Production readiness:** Mature
Stable C++ library with active maintenance.

**Implementations:**
- [Exiv2/exiv2](https://github.com/Exiv2/exiv2) ⭐ 1.1k — C++, cross-platform

**Security status:** Caution
Same limitations as ExifTool for pixel-level stego.

**Community acceptance:** Widely trusted
Used in image processing pipelines and CTF forensics.

---

### Binwalk

**Goal:** Search binary files for embedded files and executable code using signature matching.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Binwalk** | 2010 | Magic-byte signature scan + recursive extract | Auto-extracts with `-e` flag [[1]](https://github.com/ReFirmLabs/binwalk) |

**State of the art:** Standard firmware analysis and CTF stego tool. Often the first step in analyzing unknown binary blobs or images.

**Production readiness:** Production
Industry standard in firmware reverse engineering and CTF.

**Implementations:**
- [ReFirmLabs/binwalk](https://github.com/ReFirmLabs/binwalk) ⭐ 14k — Python, cross-platform

**Security status:** Caution
Signature-based; custom file formats without known magic bytes evade detection.

**Community acceptance:** Standard
Ubiquitous in CTF, firmware security, and IoT research.

---

### Zsteg

**Goal:** Detect steganographic data hidden in PNG and BMP files using multiple channel/bit combinations.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Zsteg** | 2014 | Brute-force channel/bitorder/LSB scan | Detects LSB, LSBA, zlib-compressed payloads [[1]](https://github.com/zed-0xff/zsteg) |

**State of the art:** Best automated tool for LSB stego detection in PNG/BMP. Complements stegsolve with non-interactive scanning.

**Production readiness:** Mature
Stable Ruby gem, widely used in CTF.

**Implementations:**
- [zed-0xff/zsteg](https://github.com/zed-0xff/zsteg) ⭐ 1.6k — Ruby, `gem install zsteg`

**Security status:** Caution
Effective against LSB schemes; misses encrypted or non-LSB payloads.

**Community acceptance:** Standard
Default tool for PNG stego in CTF write-ups.

---

### StegCracker

**Goal:** Brute-force steghide-protected files using a wordlist.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegCracker** | 2019 | Dictionary attack on steghide passphrase | Multi-threaded steghide wrapper [[1]](https://github.com/Paradoxis/StegCracker) |

**State of the art:** Go-to tool for cracking steghide-protected CTF files. Superseded for speed by stegseek.

**Production readiness:** Mature
Stable; largely replaced by stegseek for speed but still widely used.

**Implementations:**
- [Paradoxis/StegCracker](https://github.com/Paradoxis/StegCracker) ⭐ 594 — Python
- [RickdeJager/stegseek](https://github.com/RickdeJager/stegseek) ⭐ 1.3k — C++, faster alternative

**Security status:** Caution
Only effective against weak/dictionary passphrases.

**Community acceptance:** Standard
Standard CTF tool for steghide cracking.

---

### Fcrackzip

**Goal:** Brute-force password-protected ZIP archives using dictionary or brute-force attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Fcrackzip** | 1997 | Dictionary/brute-force ZIP cracker | Supports wordlist and charset modes [[1]](https://github.com/hyc/fcrackzip) |

**State of the art:** Standard CTF tool for cracking ZIP passwords. Superseded by hashcat/John for speed on modern hardware.

**Production readiness:** Mature
Available via apt; stable, minimal maintenance.

**Implementations:**
- [hyc/fcrackzip](https://github.com/hyc/fcrackzip) ⭐ 469 — C, Linux/macOS

**Security status:** Caution
Dictionary attacks succeed against weak passwords; AES-256 ZIP encryption is computationally infeasible without weak password.

**Community acceptance:** Standard
Standard CTF tool; referenced in forensics guides and write-ups.

---

### dcode.fr

**Goal:** Provide an online collection of cipher decoders and text analysis tools for cryptography and steganography CTF challenges.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **dcode.fr** | 2009 | Web-based cipher/encoding reference | Covers 500+ ciphers, codes, and encodings [[1]](https://www.dcode.fr/) |

**State of the art:** Essential web reference for CTF stego and crypto. Decodes Morse, Braille, Bacon, Polybius, and hundreds of other encodings in seconds.

**Production readiness:** Production
Actively maintained web service; widely available.

**Security status:** Caution
Web-based tool; do not submit sensitive data.

**Community acceptance:** Standard
Referenced in nearly every CTF write-up involving encoding or cipher identification.

---

