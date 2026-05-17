# Steganalysis

<!-- TOC -->
## Contents (88 algorithms)

**[Classical Methods](#classical-methods)**
- [Visual Attack](#visual-attack)
- [Structural Attack](#structural-attack)
- [Chi-square](#chi-square)
- [RS-analysis](#rs-analysis)
- [Weighted Stego](#weighted-stego)
- [SPAM](#spam)
- [SRM](#srm)
- [DCTR](#dctr)
- [A Game-Theoretic Approach for Adversarial Information Fusion in Distributed Sensor Networks](#a-game-theoretic-approach-for-adversarial-information-fusion-in-distributed-sensor-networks)
- [Exploring AI in Steganography and Steganalysis: Trends, Clusters, and Sustainable Development Potential](#exploring-ai-in-steganography-and-steganalysis-trends-clusters-and-sustainable-development-potential)
- [Efficient Streaming Voice Steganalysis in Challenging Detection Scenarios](#efficient-streaming-voice-steganalysis-in-challenging-detection-scenarios)
- [Linguistic Steganalysis via LLMs: Two Modes for Efficient Detection of Strongly Concealed Stego](#linguistic-steganalysis-via-llms-two-modes-for-efficient-detection-of-strongly-concealed-stego)
- [Blind Data Adaptation to tackle Covariate Shift in Operational Steganalysis](#blind-data-adaptation-to-tackle-covariate-shift-in-operational-steganalysis)
- [Towards Next-Generation Steganalysis: LLMs Unleash the Power of Detecting Steganography](#towards-next-generation-steganalysis-llms-unleash-the-power-of-detecting-steganography)
- [Double-Flow-based Steganography without Embedding for Image-to-Image Hiding](#double-flow-based-steganography-without-embedding-for-image-to-image-hiding)
- [A One-dimensional HEVC video steganalysis method using the Optimality of Predicted Motion Vectors](#a-one-dimensional-hevc-video-steganalysis-method-using-the-optimality-of-predicted-motion-vectors)
- [Green Steganalyzer: A Green Learning Approach to Image Steganalysis](#green-steganalyzer-a-green-learning-approach-to-image-steganalysis)
- [3D-VFD: A Victim-free Detector against 3D Adversarial Point Clouds](#3d-vfd-a-victim-free-detector-against-3d-adversarial-point-clouds)
- [Deniable Steganography](#deniable-steganography)
- [Steganalysis of Image with Adaptively Parametric Activation](#steganalysis-of-image-with-adaptively-parametric-activation)
- [Secret-to-Image Reversible Transformation for Generative Steganography](#secret-to-image-reversible-transformation-for-generative-steganography)
- [Generalized Local Optimality for Video Steganalysis in Motion Vector Domain](#generalized-local-optimality-for-video-steganalysis-in-motion-vector-domain)
- [Stegomalware: A Systematic Survey of MalwareHiding and Detection in Images, Machine LearningModels and Research Challenges](#stegomalware-a-systematic-survey-of-malwarehiding-and-detection-in-images-machine-learningmodels-and-research-challenges)
- [Three-Dimensional Mesh Steganography and Steganalysis: A Review](#three-dimensional-mesh-steganography-and-steganalysis-a-review)
- [Coverless Video Steganography based on Maximum DC Coefficients](#coverless-video-steganography-based-on-maximum-dc-coefficients)
- [Evolutionary Algorithms and Efficient Data Analytics for Image Processing](#evolutionary-algorithms-and-efficient-data-analytics-for-image-processing)
- [Destruction of Image Steganography using Generative Adversarial Networks](#destruction-of-image-steganography-using-generative-adversarial-networks)
- [PixelSteganalysis: Destroying Hidden Information with a Low Degree of Visual Degradation](#pixelsteganalysis-destroying-hidden-information-with-a-low-degree-of-visual-degradation)
- [Decode and Transfer: A New Steganalysis Technique via Conditional Generative Adversarial Networks](#decode-and-transfer-a-new-steganalysis-technique-via-conditional-generative-adversarial-networks)
- [Steganographic Generative Adversarial Networks](#steganographic-generative-adversarial-networks)
- [Usage of analytic hierarchy process for steganographic inserts detection in images](#usage-of-analytic-hierarchy-process-for-steganographic-inserts-detection-in-images)
- [Feature Bagging for Steganographer Identification](#feature-bagging-for-steganographer-identification)
- [Coverless Information Hiding Based on Generative adversarial networks](#coverless-information-hiding-based-on-generative-adversarial-networks)
- [A new adaptive method for hiding data in images](#a-new-adaptive-method-for-hiding-data-in-images)
- [Further Study on GFR Features for JPEG Steganalysis](#further-study-on-gfr-features-for-jpeg-steganalysis)
- [Steganalyzer performances in operational contexts](#steganalyzer-performances-in-operational-contexts)
- [Steganalysis: Detecting LSB Steganographic Techniques](#steganalysis-detecting-lsb-steganographic-techniques)
- [Steganalysis Using Color Model Conversion](#steganalysis-using-color-model-conversion)
- [Stego-Image Generator (SIG) - Building Steganography Image Database](#stego-image-generator-sig-building-steganography-image-database)
- [Application of Steganography for Anonymity through the Internet](#application-of-steganography-for-anonymity-through-the-internet)
- [Steganography and Steganalysis: Different Approaches](#steganography-and-steganalysis-different-approaches)
- [Effective Steganography Detection Based On Data Compression](#effective-steganography-detection-based-on-data-compression)
- [Spectral Estimation Methods Comparison and Performance Analysis on a Steganalysis Application](#spectral-estimation-methods-comparison-and-performance-analysis-on-a-steganalysis-application)
- [On the Unicity Distance of Stego Key](#on-the-unicity-distance-of-stego-key)

**[Deep Learning](#deep-learning)**
- [XuNet](#xunet)
- [YeNet](#yenet)
- [SRNet](#srnet)
- [ZhuNet](#zhunet)
- [CNN-Assisted Steganography -- Integrating Machine Learning with Established Steganographic Techniques](#cnn-assisted-steganography-integrating-machine-learning-with-established-steganographic-techniques)
- [Text Steganalysis with Attentional LSTM-CNN](#text-steganalysis-with-attentional-lstm-cnn)
- [JPEG Steganography with Embedding Cost Learning and Side-Information Estimation](#jpeg-steganography-with-embedding-cost-learning-and-side-information-estimation)
- [PixelSteganalysis: Pixel-wise Hidden Information Removal with Low Visual Degradation](#pixelsteganalysis-pixel-wise-hidden-information-removal-with-low-visual-degradation)
- [CNN-based Steganalysis and Parametric Adversarial Embedding: a Game-Theoretic Framework](#cnn-based-steganalysis-and-parametric-adversarial-embedding-a-game-theoretic-framework)
- [DNA Steganalysis Using Deep Recurrent Neural Networks](#dna-steganalysis-using-deep-recurrent-neural-networks)
- [Using Deep Learning to Detect Digitally Encoded DNA Trigger for Trojan Malware in Bio-Cyber Attacks](#using-deep-learning-to-detect-digitally-encoded-dna-trigger-for-trojan-malware-in-bio-cyber-attacks)
- [GSDFuse: Capturing Cognitive Inconsistencies from Multi-Dimensional Weak Signals in Social Media Steganalysis](#gsdfuse-capturing-cognitive-inconsistencies-from-multi-dimensional-weak-signals-in-social-media-steganalysis)
- [Robust Detection of Watermarks Under Human Edits (Tr-GoF)](#robust-detection-of-watermarks-under-human-edits-tr-gof)

**[Network Steganalysis](#network-steganalysis)**
- [Tor Traffic Detection](#tor-traffic-detection)
- [DNS Tunnel Detection](#dns-tunnel-detection)
- [Stego Battlefield](#stego-battlefield)
- [Zero-Shot Interpretable Image Steganalysis](#zero-shot-interpretable-image-steganalysis)
- [Targeted Pooled Latent-Space Steganalysis](#targeted-pooled-latent-space-steganalysis)
- [Systematically Deconstructing APVD Steganography](#systematically-deconstructing-apvd-steganography)
- [Forensic Video Steganalysis in Spatial Domain by Noise Residual Convolutional Neural Network](#forensic-video-steganalysis-in-spatial-domain-by-noise-residual-convolutional-neural-network)
- [Universal Deep Network for Steganalysis of Color Image based on Channel Representation](#universal-deep-network-for-steganalysis-of-color-image-based-on-channel-representation)
- [Image Steganography based on Iteratively Adversarial Samples of A Synchronized-directions Sub-image](#image-steganography-based-on-iteratively-adversarial-samples-of-a-synchronized-directions-sub-image)
- [F3SNet: A Four-Step Strategy for QIM Steganalysis of Compressed Speech Based on Hierarchical Attention Network](#f3snet-a-four-step-strategy-for-qim-steganalysis-of-compressed-speech-based-on-hierarchical-attention-network)
- [Analysis of the Scalability of a Deep-Learning Network for Steganography "Into the Wild"](#analysis-of-the-scalability-of-a-deep-learning-network-for-steganography-into-the-wild)
- [FCEM: A Novel Fast Correlation Extract Model For Real Time Steganalysis of VoIP Stream via Multi-head Attention](#fcem-a-novel-fast-correlation-extract-model-for-real-time-steganalysis-of-voip-stream-via-multi-head-attention)
- [CIS-Net: A Novel CNN Model for Spatial Image Steganalysis via Cover Image Suppression](#cis-net-a-novel-cnn-model-for-spatial-image-steganalysis-via-cover-image-suppression)
- [Hierarchical Representation Network for Steganalysis of QIM Steganography in Low-Bit-Rate Speech Signals](#hierarchical-representation-network-for-steganalysis-of-qim-steganography-in-low-bit-rate-speech-signals)
- [Deep Learning in steganography and steganalysis from 2015 to 2018](#deep-learning-in-steganography-and-steganalysis-from-2015-to-2018)
- [Spec-ResNet: A General Audio Steganalysis scheme based on Deep Residual Network of Spectrogram](#spec-resnet-a-general-audio-steganalysis-scheme-based-on-deep-residual-network-of-spectrogram)
- [TS-CNN: Text Steganalysis from Semantic Space Based on Convolutional Neural Network](#ts-cnn-text-steganalysis-from-semantic-space-based-on-convolutional-neural-network)
- [Spatial Image Steganography Based on Generative Adversarial Network](#spatial-image-steganography-based-on-generative-adversarial-network)
- [A Novel Convolutional Neural Network for Image Steganalysis with Shared Normalization](#a-novel-convolutional-neural-network-for-image-steganalysis-with-shared-normalization)
- [Convolutional Neural Network Steganalysis's Application to Steganography](#convolutional-neural-network-steganalysiss-application-to-steganography)
- [On the usefulness of information hiding techniques for wireless sensor networks security](#on-the-usefulness-of-information-hiding-techniques-for-wireless-sensor-networks-security)
- [MoveSteg: A Method of Network Steganography Detection](#movesteg-a-method-of-network-steganography-detection)
- [Steganalysis via a Convolutional Neural Network using Large Convolution Filters for Embedding Process with Same Stego Key](#steganalysis-via-a-convolutional-neural-network-using-large-convolution-filters-for-embedding-process-with-same-stego-key)
- [Steganalysis of Transcoding Steganography](#steganalysis-of-transcoding-steganography)
- [Towards Steganography Detection Through Network Traffic Visualisation](#towards-steganography-detection-through-network-traffic-visualisation)
- [DNS-HyXNet (xLSTM Real-Time DNS Tunnel Detection)](#dns-hyxnet-xlstm-real-time-dns-tunnel-detection)

**[Benchmark Datasets](#benchmark-datasets)**
- [BOSSBase](#bossbase)
- [BOWS2](#bows2)
- [ALASKA2](#alaska2)
- [VISION](#vision)
- [DVC](#dvc)

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

### A Game-Theoretic Approach for Adversarial Information Fusion in Distributed Sensor Networks

**Goal:** Address adversarial information fusion in distributed sensor networks using game-theoretic approaches.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Game-Theoretic Approach for Adversarial Information Fusion** | 2025 | cs.CR, cs.GT, cs.MA | Kassem Kallas [[1]](https://arxiv.org/abs/2511.23026) |

**State of the art:** PhD thesis addressing adversarial signal processing in distributed sensor networks. Develops soft isolation defense, optimum decision fusion strategy against Byzantine attackers, near-optimum message passing via factor graphs, and defense against data falsification attacks in consensus networks. Not directly related to steganography/steganalysis.

**Production readiness:** Research
PhD thesis; theoretical framework for adversarial sensor networks.

**Security status:** N/A
Not a steganography or steganalysis method; addresses security in sensor networks.

**Community acceptance:** Niche
Contributes to adversarial signal processing literature; not directly applicable to steganography.

---

### Exploring AI in Steganography and Steganalysis: Trends, Clusters, and Sustainable Development Potential

**Goal:** Scientometric analysis of AI-driven steganography research trends from 2017-2023.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Exploring AI in Steganography and Steganalysis: Trends, Clus** | 2025 | cs.CR, cs.AI | Aditya Kumar Sahu et al. [[1]](https://arxiv.org/abs/2511.12052) |

**State of the art:** Comprehensive scientometric analysis of 654 AI-driven steganography articles (2017-2023). Identifies 7 thematic clusters: steganographic image data hiding, deep image steganalysis, neural watermark robustness, linguistic steganography models, speech steganalysis algorithms, covert communication networks, and video steganography techniques. Maps to UN Sustainable Development Goals; only 18/654 articles align with SDGs (SDG9 leading).

**Production readiness:** Research
Survey/scientometric study; provides research trends analysis.

**Security status:** N/A
Analytical work; not a detection or embedding method.

**Community acceptance:** Emerging
First-of-its-kind scientometric study on AI-steganography; provides valuable overview of research landscape and gaps in SDG alignment.

---

### Efficient Streaming Voice Steganalysis in Challenging Detection Scenarios

**Goal:** stream segments, making the steganographic features of hard-to-detect samples more pronounced and easier to learn.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Efficient Streaming Voice Steganalysis in Challenging Detect** | 2024 | cs.CR, cs.LG, cs.SD | Pengcheng Zhou et al. [[1]](https://arxiv.org/abs/2411.13612) |

**State of the art:** State-of-the-art in VoIP steganalysis with Dual-View VoIP Steganalysis Framework (DVSF). Addresses detection at low embedding rates (10%) and short durations (0.1s). Shows near-real-time performance with superior accuracy.

**Production readiness:** Research
Academic prototype; requires implementation verification.

**Security status:** Caution
New detection method; effectiveness against novel steganography unknown.

**Community acceptance:** Emerging
Recent work in streaming media steganalysis; promising results.

---

### Linguistic Steganalysis via LLMs: Two Modes for Efficient Detection of Strongly Concealed Stego

**Goal:** in complex scenarios, linguistic steganalysis (LS) with various motivations has been proposed and achieved excellent performance.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Linguistic Steganalysis via LLMs: Two Modes for Efficient De** | 2024 | cs.CL | Yifan Tang et al. [[1]](https://arxiv.org/abs/2406.04218) |

**State of the art:** Novel linguistic steganalysis using LLMs (LSGC) with two modes: generation mode uses LLM reasoning for detection, classification mode uses causalLM for efficient feature extraction. Achieves SOTA on strongly concealed stegos with reduced training time.

**Production readiness:** Research
Academic prototype; no production implementation.

**Security status:** Caution
New detection approach; requires validation on diverse datasets.

**Community acceptance:** Emerging
First LLM-based linguistic steganalysis; growing interest.

---

### Blind Data Adaptation to tackle Covariate Shift in Operational Steganalysis

**Goal:** The proliferation of image manipulation for unethical purposes poses significant challenges in social networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Blind Data Adaptation to tackle Covariate Shift in Operation** | 2024 | eess.IV, cs.AI, cs.CR | Rony Abecidan et al. [[1]](https://arxiv.org/abs/2405.16961) |

**State of the art:** Addresses critical covariate shift problem in operational steganalysis. TADA (Target Alignment through Data Adaptation) uses geometric alignment and distribution matching to adapt models to target datasets. Addresses real-world deployment gap between training and operational steganalysis.

**Production readiness:** Research
Academic prototype; addresses practical deployment challenge.

**Security status:** Caution
New adaptation method; requires validation on diverse operational scenarios.

**Community acceptance:** Emerging
Important practical contribution; addresses real-world steganalysis deployment.

---

### Towards Next-Generation Steganalysis: LLMs Unleash the Power of Detecting Steganography

**Goal:** Linguistic steganography provides convenient implementation to hide messages, particularly with the emergence of AI generation technology.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Next-Generation Steganalysis: LLMs Unleash the Power** | 2024 | cs.CR | Minhao Bai. Jinshuai Yang et al. [[1]](https://arxiv.org/abs/2405.09090) |

**State of the art:** First LLM-based linguistic steganalysis using generative paradigm. Models steganalysis as generation task rather than classification. Outperforms baselines significantly; provides domain-agnostic detection capability with open-source models.

**Production readiness:** Research
Academic prototype with open-source code available.

**Security status:** Caution
New approach; effectiveness against evolving steganography methods unknown.

**Community acceptance:** Emerging
Pioneering work in LLM-based steganalysis; significant interest.

---

### Double-Flow-based Steganography without Embedding for Image-to-Image Hiding

**Goal:** As an emerging concept, steganography without embedding (SWE) hides a secret message without directly embedding it into a cover.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Double-Flow-based Steganography without Embedding for Image-** | 2023 | cs.CV | Bingbing Song et al. [[1]](https://arxiv.org/abs/2311.15027) |

**State of the art:** Novel steganography without embedding (SWE) technique using reversible bijective transformation (DF-SWE). Achieves 24-72 BPP payload capacity, 8000-16000x higher than competitors, while producing diverse natural stego images. Domain-agnostic property allows application across various domains without training data.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Secure
SWE inherently resistant to typical steganalysis as it doesn't modify cover images.

**Community acceptance:** Emerging
Pioneering SWE approach; significant capacity improvements over prior work.

---

### A One-dimensional HEVC video steganalysis method using the Optimality of Predicted Motion Vectors

**Goal:** Among steganalysis techniques, detection against motion vector (MV) domain-based video steganography in High Efficiency Video Coding (HEVC) standard remains a hot and challenging issue.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A One-dimensional HEVC video steganalysis method using the O** | 2023 | cs.CR, cs.LG, cs.MM | Jun Li et al. [[1]](https://arxiv.org/abs/2308.06464) |

**State of the art:** Novel HEVC video steganalysis using optimality of predicted motion vectors. Uses 1D feature representing MVP optimality rate. Achieves 100% detection for covers vs <100% for stego. No training required, low computational complexity.

**Production readiness:** Research
Proof-of-concept; submitted to TCSVT journal.

**Security status:** Caution
New feature; requires validation on diverse video datasets.

**Community acceptance:** Emerging
Novel approach to video steganalysis; addresses practical deployment.

---

### Green Steganalyzer: A Green Learning Approach to Image Steganalysis

**Goal:** to make final image-level classification.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Green Steganalyzer: A Green Learning Approach to Image Stega** | 2023 | eess.IV, cs.CR, cs.LG | Yao Zhu et al. [[1]](https://arxiv.org/abs/2306.04008) |

**State of the art:** Green learning approach to image steganalysis with three modules: pixel-based anomaly prediction, embedding location detection, and decision fusion. Achieves comparable performance to deep learning with significantly lower complexity and smaller model size. Suitable for mobile/edge applications.

**Production readiness:** Research
Academic prototype; lower computational requirements enable broader deployment.

**Security status:** Caution
New paradigm; requires validation on diverse steganography methods.

**Community acceptance:** Emerging
Important contribution to efficient steganalysis; addresses practical deployment.

---

### 3D-VFD: A Victim-free Detector against 3D Adversarial Point Clouds

**Goal:** in computer vision. However, recent studies have shown they are vulnerable to 3D adversarial point clouds.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **3D-VFD: A Victim-free Detector against 3D Adversarial Point ** | 2023 | cs.MM, cs.CV, eess.IV | Jiahao Zhu et al. [[1]](https://arxiv.org/abs/2205.08738) |

**State of the art:** First victim-free detector (3D-VFD) against 3D adversarial point clouds using steganalysis perspective. Captures discrepancies in residual geometric feature distributions between benign and adversarial point clouds. Achieves SOTA detection without relying on victim 3D model outputs.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Novel approach; effectiveness against evolving 3D adversarial attacks requires validation.

**Community acceptance:** Emerging
First work applying steganalysis to 3D adversarial point cloud detection; pioneering approach.

---

### Deniable Steganography

**Goal:** Steganography conceals the secret message into the cover media, generating a stego media which can be transmitted on public channels without drawing suspicion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Deniable Steganography** | 2022 | cs.CR, cs.CV | Yong Xu et al. [[1]](https://arxiv.org/abs/2205.12587) |

**State of the art:** First work on deniable steganography - allows receiver to extract fake message under coercive attack while hiding real message. Uses DNN-based receiver-deniable scheme with separate extraction modules for real and fake messages. Addresses novel threat model of coercive attack.

**Production readiness:** Research
Novel concept; proof-of-concept implementation with DNN.

**Security status:** Caution
New threat model; requires more research on practical deployment.

**Community acceptance:** Emerging
Introduces new research direction; novel application of deniable encryption concepts to steganography.

---

### Steganalysis of Image with Adaptively Parametric Activation

**Goal:** Steganalysis as a method to detect whether image contains se-cret message, is a crucial study avoiding the imperils from abus-ing steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis of Image with Adaptively Parametric Activation** | 2022 | cs.MM, cs.CR, cs.CV | Hai Su et al. [[1]](https://arxiv.org/abs/2203.12843) |

**State of the art:** Image steganalysis with Adaptively Parametric Activation (APA) module to preserve negative embedding signals. Uses constraint-based high-pass filters for residual diversity and contrastive learning loss. Competitive performance on BOSSbase against WOW and S-UNIWARD.

**Production readiness:** Research
Academic prototype; no production implementation.

**Security status:** Caution
New activation approach; requires validation on more datasets.

**Community acceptance:** Emerging
Novel approach to improving steganalysis features.

---

### Secret-to-Image Reversible Transformation for Generative Steganography

**Goal:** Recently, generative steganography that transforms secret information to a generated image has been a promising technique to resist steganalysis detection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secret-to-Image Reversible Transformation for Generative Ste** | 2022 | cs.CR | Zhili Zhou et al. [[1]](https://arxiv.org/abs/2203.06598) |

**State of the art:** Secret-to-Image Reversible Transformation (S2IRT) for generative steganography using Glow model. Achieves high hiding capacity (up to 4 bpp) and near 100% extraction accuracy. Includes SE-S2IRT variant for robustness against image attacks.

**Production readiness:** Research
Academic prototype; addresses reversibility challenge in generative steganography.

**Security status:** Caution
New approach; requires steganalysis evaluation on diverse datasets.

**Community acceptance:** Emerging
Novel approach to generative steganography; addresses practical limitations.

---

### Generalized Local Optimality for Video Steganalysis in Motion Vector Domain

**Goal:** motion vectors (MVs) is an intrinsic property in video coding, and any modifications to the MVs will inevitably destroy this optimality, making it a sensitive indicator of steganography in the MV d...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generalized Local Optimality for Video Steganalysis in Motio** | 2021 | cs.CV, cs.CR | Liming Zhai et al. [[1]](https://arxiv.org/abs/2112.11729) |

**State of the art:** Generalized Local Optimality for video steganalysis. Extends concept from static to dynamic estimation and from MV to PMV domain. Achieves SOTA accuracy and robustness against cover source mismatch, video prediction methods, codecs, and resolutions.

**Production readiness:** Research
Academic prototype; addresses practical video steganalysis challenges.

**Security status:** Caution
New feature framework; requires validation on diverse video datasets.

**Community acceptance:** Emerging
Significant contribution to video steganalysis; addresses real-world deployment.

---

### Stegomalware: A Systematic Survey of MalwareHiding and Detection in Images, Machine LearningModels and Research Challenges

**Goal:** malware analysis, and the malware detection capabilities of these files has been well advanced for real-time detection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegomalware: A Systematic Survey of MalwareHiding and Detec** | 2021 | cs.CR | Rajasekhar Chaganti et al. [[1]](https://arxiv.org/abs/2110.02504) |

**State of the art:** First systematic survey of stegomalware (malware using image steganography). Covers history, generation tools, file formats, GAN-based steganography, and DL-based detection. Proposes enterprise stegomalware detection framework. Addresses critical security gap.

**Production readiness:** Research
Survey paper; provides comprehensive overview and detection framework.

**Security status:** N/A
Survey; provides background and detection approach recommendations.

**Community acceptance:** Widely trusted
Important security survey; addresses practical malware detection gap.

---

### Three-Dimensional Mesh Steganography and Steganalysis: A Review

**Goal:** and volumes. Over the past decade, 3-D meshes have emerged in industrial, medical, and entertainment applications, being of large practical significance for 3-D mesh steganography and steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Three-Dimensional Mesh Steganography and Steganalysis: A Rev** | 2021 | cs.CR, cs.GR | Hang Zhou et al. [[1]](https://arxiv.org/abs/2104.10203) |

**State of the art:** Comprehensive survey of 3D mesh steganography and steganalysis. Proposes new taxonomy: two-state, LSB, permutation, and transform domains. Covers universal and specific steganalysis. Accepted to TVCG journal.

**Production readiness:** Research
Survey paper; comprehensive overview of the field.

**Security status:** N/A
Survey; provides taxonomy and future directions.

**Community acceptance:** Widely trusted
Published in IEEE TVCG; authoritative survey.

---

### Coverless Video Steganography based on Maximum DC Coefficients

**Goal:** Coverless steganography has been a great interest in recent years, since it is a technology that can absolutely resist the detection of steganalysis by not modifying the carriers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Coverless Video Steganography based on Maximum DC Coefficien** | 2020 | cs.MM, cs.CR | Laijin Meng et al. [[1]](https://arxiv.org/abs/2012.06809) |

**State of the art:** First coverless video steganography using maximum DC coefficients. Uses Gaussian distribution model of DC coefficients and hash sequence generation. Addresses capacity, robustness, and security. Better than prior coverless algorithms.

**Production readiness:** Research
Academic prototype; addresses coverless video steganography gap.

**Security status:** Secure
Coverless approach inherently resistant to steganalysis detection.

**Community acceptance:** Emerging
Novel approach; addresses practical coverless video steganography.

---

### Evolutionary Algorithms and Efficient Data Analytics for Image Processing

**Goal:** Steganography algorithms facilitate communication between a source and a destination in a secret manner.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Evolutionary Algorithms and Efficient Data Analytics for Ima** | 2020 | cs.CV, cs.LG, cs.MM | Farid Ghareh Mohammadi et al. [[1]](https://arxiv.org/abs/1907.12914) |

**State of the art:** Survey of evolutionary algorithms for addressing curse of dimensionality in universal steganalysis. Discusses deep learning and evolutionary approaches for real-time steganalysis. Addresses NP-hard feature selection problem.

**Production readiness:** Research
Survey paper; provides overview of EA for steganalysis.

**Security status:** N/A
Survey; provides research directions.

**Community acceptance:** Emerging
Provides research directions for practical steganalysis.

---

### Destruction of Image Steganography using Generative Adversarial Networks

**Goal:** Digital image steganalysis, or the detection of image steganography, has been studied in depth for years and is driven by Advanced Persistent Threat (APT) groups', such as APT37 Reaper, utilization...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Destruction of Image Steganography using Generative Adversar** | 2019 | cs.MM, cs.CR, cs.LG | Isaac Corley, Jonathan Lwowski, Justin Hoffman [[1]](https://arxiv.org/abs/1912.10070) |

**State of the art:** Deep Digital Steganography Purifier (DDSP) uses GAN to destroy steganographic content while preserving image quality. Addresses APT threats like APT37. Shows high destruction rate with visual quality preservation. Transfer learning capability for unseen steganography.

**Production readiness:** Research
Academic prototype; addresses practical steganography destruction.

**Security status:** Caution
New approach; effectiveness against novel steganography unknown.

**Community acceptance:** Emerging
Important active steganalysis approach; practical security implications.

---

### PixelSteganalysis: Destroying Hidden Information with a Low Degree of Visual Degradation

**Goal:** Steganography is the science of unnoticeably concealing a secret message within a certain image, called a cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **PixelSteganalysis: Destroying Hidden Information with a Low ** | 2019 | cs.MM, cs.CR, cs.LG | Dahuin Jung et al. [[1]](https://arxiv.org/abs/1902.11113) |

**State of the art:** Active steganalysis for DL-based steganography using pixel distribution restoration. Withdrawn; superseded by arXiv:1902.10905 (published in IEEE TDSC). Shows up to 20% improvement in decoding rate. Addresses DL steganography detection.

**Production readiness:** Research
Withdrawn paper; superseded by updated version.

**Security status:** Deprecated
Paper withdrawn; use updated version arXiv:1902.10905.

**Community acceptance:** Niche
Withdrawn paper; limited current relevance.

---

### Decode and Transfer: A New Steganalysis Technique via Conditional Generative Adversarial Networks

**Goal:** to discover the secret image using conventional methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Decode and Transfer: A New Steganalysis Technique via Condit** | 2019 | cs.CR | Parisa Babaheidarian, Mark Wallace [[1]](https://arxiv.org/abs/1901.09746) |

**State of the art:** Novel steganalysis technique using conditional GANs to recover hidden secret images from steganographic images. Uses deep neural network to decode approximate estimate, then domain adaptation via GAN to enhance to high-quality RGB image with visible details. Can serve as attack model for evaluating steganography security.

**Production readiness:** Research
Academic prototype; no production implementation.

**Security status:** Caution
Novel recovery approach; requires validation on diverse steganography methods.

**Community acceptance:** Emerging
First work using cGAN for steganalysis recovery; pioneering approach.

---

### Steganographic Generative Adversarial Networks

**Goal:** Steganography is collection of methods to hide secret information ("payload") within non-secret information "container").

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganographic Generative Adversarial Networks** | 2019 | cs.MM, cs.CR, cs.CV | Denis Volkhonskiy, Ivan Nazarov, Evgeny Burnaev [[1]](https://arxiv.org/abs/1703.05502) |

**State of the art:** Uses DCGAN to generate image-like containers that are more secure against steganalysis. First application of GANs to steganography. Embedding using standard algorithms in generated images shows improved resistance to steganalysis. Presented at NIPS 2016 Workshop on Adversarial Training.

**Production readiness:** Research
Proof-of-concept; 15-page paper with experimental validation.

**Security status:** Caution
Early work; more recent approaches have superseded this.

**Community acceptance:** Emerging
Pioneering work applying deep generative models to steganography; frequently cited.

---

### Usage of analytic hierarchy process for steganographic inserts detection in images

**Goal:** This article presents the method of steganography detection, which is formed by replacing the least significant bit (LSB).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Usage of analytic hierarchy process for steganographic inser** | 2018 | cs.MM, cs.CV, cs.GR | S. V. Belim, D. E. Vilkhovskiy [[1]](https://arxiv.org/abs/1902.11100) |

**State of the art:** Uses analytic hierarchy process to detect LSB steganography. Analyzes zero-layer of adjacent bits. Can detect messages in bounded rectangular areas with <10% fill rate. Localizes message location with <5 pixel error. Effective where statistical methods fail.

**Production readiness:** Research
Published in 2016 conference proceedings; proof-of-concept.

**Security status:** Caution
Limited to specific attack scenarios; requires known message location.

**Community acceptance:** Niche
Alternative approach to LSB detection; limited adoption.

---

### Feature Bagging for Steganographer Identification

**Goal:** Traditional steganalysis algorithms focus on detecting the existence of steganography in a single object.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Feature Bagging for Steganographer Identification** | 2018 | cs.MM | Hanzhou Wu [[1]](https://arxiv.org/abs/1810.11973) |

**State of the art:** First work on steganographer identification (SIP) problem. Uses feature bagging to merge results from multiple sub-models with randomly sampled feature spaces. Creates ImgNetEase dataset (5108 images). Uses PEV-274 features with nsF5 steganography. Significantly improves detection accuracy over single models in high-dimensional feature space.

**Production readiness:** Research
Proof-of-concept with custom dataset.

**Security status:** Caution
New problem formulation; requires validation on more scenarios.

**Community acceptance:** Emerging
Introduces novel SIP problem; first work addressing this scenario.

---

### Coverless Information Hiding Based on Generative adversarial networks

**Goal:** Traditional image steganography modifies the content of the image more or less, it is hard to resist the detection of image steganalysis tools.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Coverless Information Hiding Based on Generative adversarial** | 2017 | cs.CR, cs.MM | Ming-ming Liu et al. [[1]](https://arxiv.org/abs/1712.06951) |

**State of the art:** First coverless information hiding using GAN. Replaces class label with secret information to drive image generation. Extracts secret through discriminator. No content modification - inherently resistant to steganalysis. Addresses limitations of traditional steganography that modify cover images.

**Production readiness:** Research
Proof-of-concept; arXiv note: overlap with 1703.05502 by different authors.

**Security status:** Caution
Novel approach; capacity and extraction reliability need improvement.

**Community acceptance:** Emerging
Pioneering coverless approach; spawned significant follow-up research.

---

### A new adaptive method for hiding data in images

**Goal:** LSB method is one of the well-known steganography methods which hides the message bits into the least significant bit of pixel values.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A new adaptive method for hiding data in images** | 2017 | cs.MM, cs.CR | Kazem Qazanfari, Reza Safabaksh [[1]](https://arxiv.org/abs/1709.06729) |

**State of the art:** Adaptive LSB method - varies amount and method per image area based on local characteristics. Higher security than basic LSB by reducing statistical changes. May increase capacity in some images. Originally from 2011 Iranian conference.

**Production readiness:** Research
Older work; proof-of-concept adaptive LSB method.

**Security status:** Broken
Basic LSB-based; vulnerable to modern steganalysis.

**Community acceptance:** Niche
Limited impact; superseded by modern adaptive methods.

---

### Further Study on GFR Features for JPEG Steganalysis

**Goal:** Filter Residual) features, built as histograms of quantized residuals obtained with 2D Gabor filters, can achieve competitive detection performance against adaptive JPEG steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Further Study on GFR Features for JPEG Steganalysis** | 2017 | cs.MM | Xia Chao, Guan Qingxiao, Zhao Xianfeng [[1]](https://arxiv.org/abs/1706.07576) |

**State of the art:** Improved GFR (Gabor Filter Residual) features for JPEG steganalysis. Novel histogram merging using Gabor filter symmetries for compact features. Weighted histogram considering residual quantization position. Also designs CNN with improved GFR + ensemble classifier.

**Production readiness:** Research
Academic research; builds on established GFR framework.

**Security status:** Caution
Incremental improvement; requires validation on diverse datasets.

**Community acceptance:** Emerging
Extends well-known GFR approach; cited in JPEG steganalysis literature.

---

### Steganalyzer performances in operational contexts

**Goal:** Steganography and steganalysis are two important branches of the information hiding field of research.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalyzer performances in operational contexts** | 2016 | cs.MM, cs.CR | Yousra A. Fadil et al. [[1]](https://arxiv.org/abs/1608.05850) |

**State of the art:** Investigates universal steganalyzer without knowledge of steganography method. Evaluates effects of parameter/method modifications between learning and testing stages. Studies merging multiple methods during learning to improve classification. Published in IIH-MSP 2015.

**Production readiness:** Research
Survey and experimental evaluation; published at conference.

**Security status:** Caution
Addresses practical deployment scenarios; requires validation on diverse data.

**Community acceptance:** Emerging
Addresses operational context of steganalysis deployment.

---

### Steganalysis: Detecting LSB Steganographic Techniques

**Goal:** Steganalysis means analysis of stego images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis: Detecting LSB Steganographic Techniques** | 2014 | cs.MM, cs.CR | Tanmoy Sarkar, Sugata Sanyal [[1]](https://arxiv.org/abs/1405.5119) |

**State of the art:** Survey paper on LSB steganalysis techniques. Discusses different steganalysis methods and their applicability based on scenarios. 5-page overview paper helping understand when to use which technique.

**Production readiness:** Research
Survey/educational; provides overview of LSB steganalysis.

**Security status:** Broken
Survey of older techniques; LSB methods are largely broken by modern steganalysis.

**Community acceptance:** Niche
Educational resource; limited current research relevance.

---

### Steganalysis Using Color Model Conversion

**Goal:** Bit Steganographic algorithms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis Using Color Model Conversion** | 2012 | cs.CR | P. Thiyagarajan, G. Aghila, V. Prasanna Venkatesan [[1]](https://arxiv.org/abs/1206.2914) |

**State of the art:** Universal image steganalysis method using RGB to HSI color model conversion. Detects LSB steganography by analyzing color space transformations. Published in Signal and Image Processing: An International Journal.

**Production readiness:** Research
Academic prototype; limited to LSB detection.

**Security status:** Broken
Effective only against basic LSB steganography; defeated by modern adaptive methods.

**Community acceptance:** Niche
Limited impact; superseded by modern steganalysis approaches.

---

### Stego-Image Generator (SIG) - Building Steganography Image Database

**Goal:** Steganographic algorithms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stego-Image Generator (SIG) - Building Steganography Image D** | 2012 | cs.CR | P. Thiyagarajan, G. Aghila, V. Prasanna Venkatesan [[1]](https://arxiv.org/abs/1206.2586) |

**State of the art:** First stego-image database (SIG) for testing steganalysis algorithms. Generates stego-images using various LSB steganographic algorithms with configurable parameters (rows infected, bits modified, channel affected). Addresses gap in existing datasets by providing ground truth for algorithm evaluation.

**Production readiness:** Research
Dataset creation; no active implementation needed.

**Security status:** N/A
Resource/dataset; not a detection or embedding method.

**Community acceptance:** Niche
Provides testing infrastructure; limited citation impact.

---

### Application of Steganography for Anonymity through the Internet

**Goal:** the highest level of security in a well defined and studied category of attacks called "watermark-only attack".

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Application of Steganography for Anonymity through the Inter** | 2012 | cs.CR, cs.IT | Jacques M. Bahi et al. [[1]](https://arxiv.org/abs/1202.5302) |

**State of the art:** Novel steganographic scheme based on chaotic iterations for anonymity through the Internet. Achieves "stego-secure" status (highest security level in watermark-only attack category). Includes steganalysis study demonstrating security in real test framework.

**Production readiness:** Research
Academic prototype; theoretical framework.

**Security status:** Caution
Novel approach; requires validation against modern steganalysis methods.

**Community acceptance:** Emerging
First work on chaotic iteration-based steganography for anonymity.

---

### Steganography and Steganalysis: Different Approaches

**Goal:** Steganography is the technique of hiding confidential information within any media.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography and Steganalysis: Different Approaches** | 2011 | cs.CR | Soumyendu Das et al. [[1]](https://arxiv.org/abs/1111.3758) |

**State of the art:** Survey paper covering different approaches to steganography and steganalysis using multimedia (text, static image, audio, video) and network IP datagrams as covers. Discusses various steganography implementations and detection methods. Published in International Journal of Computers, Information Technology and Engineering (IJCITAE) 2008.

**Production readiness:** Research
Survey paper; provides educational overview.

**Security status:** N/A
Survey; provides background and taxonomy.

**Community acceptance:** Niche
Educational resource; limited current research relevance.

---

### Effective Steganography Detection Based On Data Compression

**Goal:** This article describes novel text steganalysis method.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Effective Steganography Detection Based On Data Compression** | 2011 | cs.CR | Ivan Nechta [[1]](https://arxiv.org/abs/1110.3466) |

**State of the art:** Novel text steganalysis method using Bzip2 data compression to detect stegotext generated by Texto stegosystem. Achieves 99.98% detection accuracy for text segments with 400 bytes. Published in Vestnik SIBSUTIS journal.

**Production readiness:** Research
Academic prototype; targets specific stegosystem.

**Security status:** Caution
Effective against Texto but limited to text steganography methods.

**Community acceptance:** Niche
Specialized approach; limited adoption beyond specific use case.

---

### Spectral Estimation Methods Comparison and Performance Analysis on a Steganalysis Application

**Goal:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the intended recipient knows of the existence of the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Spectral Estimation Methods Comparison and Performance Analy** | 2011 | cs.CR | Tolga Mataracioglu, Unal Tatar [[1]](https://arxiv.org/abs/1108.2152) |

**State of the art:** Introduces spectral estimation methods for audio steganalysis. Compares performance of various spectral estimation techniques. Demonstrates hiding and extracting information from sound signals using frequency analysis. Educational work on applying signal processing to steganalysis.

**Production readiness:** Research
Proof-of-concept; educational demonstration.

**Security status:** Caution
Basic approach; limited to specific audio steganography methods.

**Community acceptance:** Niche
Educational resource; limited current research relevance.

---

### On the Unicity Distance of Stego Key

**Goal:** Steganography is about how to send secret message covertly.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On the Unicity Distance of Stego Key** | 2005 | cs.CR | Zhang Weiming, Li Shiqu [[1]](https://arxiv.org/abs/cs/0504083) |

**State of the art:** Information-theoretic analysis of stego key extraction difficulty. Derives lower bound for unicity distance showing relations between key rate, message rate, hiding capacity, and extraction difficulty. Proposes effective method for recovering stego key of LSB replacing steganography by combining steganalysis detection with cryptanalysis correlation attack.

**Production readiness:** Research
Theoretical analysis with proof-of-concept attack.

**Security status:** Broken
LSB replacement is obsolete; defeated by modern steganalysis and replaced by adaptive methods.

**Community acceptance:** Niche
Early work from 2005; limited current relevance.

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

### CNN-Assisted Steganography -- Integrating Machine Learning with Established Steganographic Techniques

**Goal:** We propose a method to improve steganography by increasing the resilience of stego-media to discovery through steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CNN-Assisted Steganography -- Integrating Machine Learning w** | 2023 | cs.CR, cs.LG, cs.MM | Andrew Havard et al. [[1]](https://arxiv.org/abs/2304.12503) |

**State of the art:** Uses steganographic assistant CNN (SA-CNN) to customize parametric steganographic algorithms based on cover media characteristics. Shows reduced detection rates by Yedroudj-Net when integrated with S-UNIWARD. Adaptive approach that configures steganography per cover image.

**Production readiness:** Research
Proof-of-concept; 6-page preprint with experimental evaluation.

**Security status:** Caution
New approach; requires validation on diverse datasets and steganalyzers.

**Community acceptance:** Emerging
Integrates ML with classical S-UNIWARD; CC BY-NC-SA 4.0 license.

---

### Text Steganalysis with Attentional LSTM-CNN

**Goal:** With the rapid development of Natural Language Processing (NLP) technologies, text steganography methods have been significantly innovated recently, which poses a great threat to cybersecurity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Text Steganalysis with Attentional LSTM-CNN** | 2022 | cs.MM | YongJian Bao et al. [[1]](https://arxiv.org/abs/1912.12871) |

**State of the art:** Attentional LSTM-CNN for text steganalysis combining semantic word embeddings with CNN for local features and LSTM for long-distance context. Uses attention mechanism to identify important steganographic clues. Note: Paper has been withdrawn from arXiv.

**Production readiness:** Research
Withdrawn paper; no active implementation available.

**Security status:** Deprecated
Paper withdrawn; methodology should be verified from other sources.

**Community acceptance:** Niche
Withdrawn paper; limited current relevance.

---

### JPEG Steganography with Embedding Cost Learning and Side-Information Estimation

**Goal:** A great challenge to steganography has arisen with the wide application of steganalysis methods based on convolutional neural networks (CNNs).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **JPEG Steganography with Embedding Cost Learning and Side-Inf** | 2021 | cs.MM | Jianhua Yang et al. [[1]](https://arxiv.org/abs/2107.13151) |

**State of the art:** JPEG steganography with embedding cost learning via GAN (JS-GAN). Includes estimated side-information (ESI) for asymmetric cost adjustment. Shows 2.58% detection error improvement over J-UNIWARD, and 11.25% further improvement with ESI.

**Production readiness:** Research
Academic prototype; addresses JPEG steganography anti-detection.

**Security status:** Caution
New approach; requires validation against modern steganalysis.

**Community acceptance:** Emerging
Novel approach to JPEG steganography; addresses practical deployment.

---

### PixelSteganalysis: Pixel-wise Hidden Information Removal with Low Visual Degradation

**Goal:** Recently, the field of steganography has experienced rapid developments based on deep learning (DL).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **PixelSteganalysis: Pixel-wise Hidden Information Removal wit** | 2021 | cs.MM, cs.CR, cs.CV | Dahuin Jung et al. [[1]](https://arxiv.org/abs/1902.10905) |

**State of the art:** First DL-based steganalysis that removes hidden information at pixel level. Uses pixel and edge distribution restoration. Published in IEEE TDSC. Shows 10-20% improvement in decoded rate and destruction rate.

**Production readiness:** Research
Published in IEEE TDSC; addresses practical steganalysis removal.

**Security status:** Caution
New approach; effectiveness against novel steganography unknown.

**Community acceptance:** Emerging
Important contribution to active steganalysis; practical implications.

---

### CNN-based Steganalysis and Parametric Adversarial Embedding: a Game-Theoretic Framework

**Goal:** CNN-based steganalysis has recently achieved very good performance in detecting content-adaptive steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CNN-based Steganalysis and Parametric Adversarial Embedding:** | 2019 | cs.MM, cs.GT | Xiaoyu Shi et al. [[1]](https://arxiv.org/abs/1906.00697) |

**State of the art:** Game-theoretic framework for CNN steganalysis and adversarial embedding. Models as non-zero sum game between steganographer and steganalyst. Shows equilibrium solution reduces to zero-sum game. Provides strategy to improve steganalysis reliability.

**Production readiness:** Research
Theoretical framework; addresses adversarial steganography.

**Security status:** Caution
Game-theoretic approach; practical implementation complex.

**Community acceptance:** Emerging
Novel framework for adversarial steganalysis; theoretical contribution.

---

### DNA Steganalysis Using Deep Recurrent Neural Networks

**Goal:** Recent advances in next-generation sequencing technologies have facilitated the use of deoxyribonucleic acid (DNA) as a novel covert channels in steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **DNA Steganalysis Using Deep Recurrent Neural Networks** | 2018 | cs.LG, cs.MM | Ho Bae et al. [[1]](https://arxiv.org/abs/1704.08443) |

**State of the art:** First DNA steganalysis using deep RNN. Addresses limitations of frequency analysis methods for DNA steganography. Learns intrinsic distribution of coding/non-coding sequences. Detects hidden messages by exploiting distribution variations. More robust than existing biological sequence analysis methods. Updated v3 in 2018.

**Production readiness:** Research
Proof-of-concept; extensively revised over 3 versions.

**Security status:** Caution
Novel domain; requires validation on more DNA steganography methods.

**Community acceptance:** Emerging
First work on DNA steganalysis; pioneering in this niche area.

---

### Using Deep Learning to Detect Digitally Encoded DNA Trigger for Trojan Malware in Bio-Cyber Attacks

**Goal:** from trojan attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Deep Learning to Detect Digitally Encoded DNA Trigger ** | 2022 | cs.CR, cs.LG | Mohd Siblee Islam et al. [[1]](https://arxiv.org/abs/2202.11824) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

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

---

### Robust Detection of Watermarks Under Human Edits (Tr-GoF)

**Goal:** Detect LLM-generated text watermarks even when human editors substantially modify the text. Standard watermark detection degrades sharply under edits; Tr-GoF (truncated goodness-of-fit) is robust without requiring prior knowledge of edit level or LLM model.

| Algorithm | Year | Architecture | Notable Feature |
|-----------|------|--------------|-----------------|
| **Tr-GoF (Li et al.)** | 2024 | Truncated goodness-of-fit test | Detects Gumbel/Red-Green watermarks under heavy human editing; optimal without model knowledge [[1]](https://arxiv.org/abs/2411.13868) |

**State of the art:** Pennsylvania-led collaboration. Establishes that watermark detection under adversarial edits has provable optimal procedures; Tr-GoF achieves the upper bound asymptotically.

**Production readiness:** Research
Statistical framework with reference implementation; ready for integration into watermark detection pipelines.

**Security status:** Effective
Optimal in the adversarial-edit regime up to constant factors.

**Community acceptance:** Emerging
Cited in subsequent watermarking literature; influences design of robustness benchmarks (e.g., MarkMyWords).

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

**State of the art:** SADBench benchmark with 4 core tasks: steganography attack capability, steganalysis defense capability, efficiency, and transferability evaluation. Evaluates image-payload and text-payload steganography across diverse cover distributions. Key findings: INN and autoencoder methods show superior stability, in-domain detection is near-perfect but transferability is asymmetric (attacks generalize better than detectors), real-world threats persist on social media.

**Production readiness:** Research
Preprint May 2026; benchmark suite under development.

**Implementations:** Academic benchmark — code not yet publicly released

**Security status:** Caution — Benchmark reveals gaps in current steganalysis defenses against LLM-generated steganography

**Community acceptance:** Emerging — Very recent; addresses timely LLM-era threat model with systematic evaluation framework

---

### Zero-Shot Interpretable Image Steganalysis

**Goal:** Zero-shot detection of invertible image hiding methods with interpretability and secret recovery capability.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Zero-Shot Interpretable** | 2026 | Zero-shot learning | Invertible image hiding [[1]](https://arxiv.org/abs/2605.01331) |

**State of the art:** Proposes interpretable steganalysis framework for invertible image hiding under zero-shot setting. Integrates image hiding, revealing, and steganalysis into unified framework with ability to recover embedded secret information. Uses residual augmentation strategy for cross-dataset and cross-architecture generalization. Accepted to IEEE SPL.

**Production readiness:** Research
Preprint 2026; accepted to IEEE SPL; no public implementation yet.

**Security status:** Caution — Effective against invertible hiding; applicability to other schemes needs validation

**Community acceptance:** Emerging — Very recent; addresses emerging invertible image hiding threat

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

---

### Forensic Video Steganalysis in Spatial Domain by Noise Residual Convolutional Neural Network

**Goal:** This research evaluates a convolutional neural network (CNN) based approach to forensic video steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Forensic Video Steganalysis in Spatial Domain by Noise Resid** | 2023 | cs.CV, cs.CR | Mart Keizer, Zeno Geradts, Meike Kombrink [[1]](https://arxiv.org/abs/2305.18070) |

**State of the art:** CNN-based video steganalysis using noise residual approach. Achieves 99.96% detection rate on MSU StegoVideo dataset for spatial domain steganography. Uses CNN to detect pixel modifications from embedding.

**Production readiness:** Research
Academic prototype; trained on synthetic video steganography dataset.

**Security status:** Caution
Detection evaluated on limited dataset; may vary with different steganography tools.

**Community acceptance:** Emerging
Novel application of CNN to video steganalysis; CC BY 4.0 license.

---

### Universal Deep Network for Steganalysis of Color Image based on Channel Representation

**Goal:** in each color channel, in preprocessing module, we firstly separate the input image into three channels according to the corresponding embedding spaces (i.e.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Universal Deep Network for Steganalysis of Color Image based** | 2021 | cs.CV, cs.CR | Kangkang Wei et al. [[1]](https://arxiv.org/abs/2111.12231) |

**State of the art:** Universal color image steganalysis network (UCNet) for both spatial and JPEG domains. Uses channel representation (RGB/YCbCr) and group convolution. Achieves SOTA on ALASKA II with fewer parameters than SRNet and J-YeNet.

**Production readiness:** Research
Academic prototype; addresses color image steganalysis gap.

**Security status:** Caution
New approach; requires validation on diverse color image datasets.

**Community acceptance:** Emerging
Important contribution addressing real-world color image steganalysis.

---

### Image Steganography based on Iteratively Adversarial Samples of A Synchronized-directions Sub-image

**Goal:** Nowadays a steganography has to face challenges of both feature based staganalysis and convolutional neural network (CNN) based steganalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography based on Iteratively Adversarial Samples** | 2021 | cs.CV | Xinghong Qin et al. [[1]](https://arxiv.org/abs/2101.05209) |

**State of the art:** Novel steganography (ITE-SYN) using iteratively adversarial samples on synchronized-directions sub-images. Enhances security against both feature-based and CNN-based steganalysis by fooling target CNN classifiers.

**Production readiness:** Research
Academic prototype; addresses dual threat from classical and deep learning steganalysis.

**Security status:** Caution
New approach; requires validation on diverse steganalysis methods.

**Community acceptance:** Emerging
Novel approach to adversarial steganography; addresses practical security concerns.

---

### F3SNet: A Four-Step Strategy for QIM Steganalysis of Compressed Speech Based on Hierarchical Attention Network

**Goal:** which vectors have a greater impact on the final classification result.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **F3SNet: A Four-Step Strategy for QIM Steganalysis of Compres** | 2021 | cs.CR | Chuanpeng Guo, Wei Yang, Liusheng Huang [[1]](https://arxiv.org/abs/2101.05105) |

**State of the art:** QIM steganalysis using hierarchical attention network (F3SNet). Four-step strategy: Embedding, Encoding, Attention, Classification. Addresses small sample and low embedding rate challenges. Note: Paper has been withdrawn due to major error in conclusions.

**Production readiness:** Research
Withdrawn paper; no active implementation.

**Security status:** Deprecated
Paper withdrawn; methodology should not be used.

**Community acceptance:** Niche
Withdrawn paper; limited current relevance.

---

### Analysis of the Scalability of a Deep-Learning Network for Steganography "Into the Wild"

**Goal:** Since the emergence of deep learning and its adoption in steganalysis fields, most of the reference articles kept using small to medium size CNN, and learn them on relatively small databases.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Analysis of the Scalability of a Deep-Learning Network for S** | 2020 | cs.CR | Hugo Ruiz et al. [[1]](https://arxiv.org/abs/2012.14816) |

**State of the art:** Analyzes scalability of deep learning steganalysis networks on large diverse databases. Shows error power-law holds in steganalysis. Addresses minimum database/CNN size for better-than-random performance. Published at ICPR 2021.

**Production readiness:** Research
Academic analysis; provides guidelines for database and network sizing.

**Security status:** N/A
Analytical work; not a detection or embedding method.

**Community acceptance:** Emerging
Important analysis for DL steganalysis research; practical implications.

---

### FCEM: A Novel Fast Correlation Extract Model For Real Time Steganalysis of VoIP Stream via Multi-head Attention

**Goal:** to their highly parallelizable computation and flexibility in modeling correlation in sequence, to tackle steganalysis problem of Quantization Index Modulation (QIM) based steganography in compress...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **FCEM: A Novel Fast Correlation Extract Model For Real Time S** | 2020 | cs.MM | Hao Yang et al. [[1]](https://arxiv.org/abs/1911.00682) |

**State of the art:** Fast Correlation Extract Model (FCEM) for VoIP steganalysis using multi-head attention. Outperforms RNNs and CNNs in accuracy and speed. Detects low embedding rates and short samples (0.1s). Published at ICASSP 2020.

**Production readiness:** Research
Published at ICASSP; addresses real-time VoIP steganalysis.

**Security status:** Caution
New approach; requires validation on diverse VoIP datasets.

**Community acceptance:** Emerging
Important contribution to real-time steganalysis; practical implications.

---

### CIS-Net: A Novel CNN Model for Spatial Image Steganalysis via Cover Image Suppression

**Goal:** classification of cover images and stego images easier is the key of this task.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CIS-Net: A Novel CNN Model for Spatial Image Steganalysis vi** | 2019 | cs.MM, eess.IV | Songtao Wu et al. [[1]](https://arxiv.org/abs/1912.06540) |

**State of the art:** Cover Image Suppression Network (CIS-Net) for spatial image steganalysis. Uses Single-value Truncation Layer (STL) and Sub-linear Pooling Layer (SPL) to suppress cover content. Outperforms rich model classifiers and CNN models on challenging steganography.

**Production readiness:** Research
Academic prototype; addresses cover suppression for better detection.

**Security status:** Caution
New approach; requires validation on diverse datasets.

**Community acceptance:** Emerging
Novel network architecture; contributes to spatial steganalysis.

---

### Hierarchical Representation Network for Steganalysis of QIM Steganography in Low-Bit-Rate Speech Signals

**Goal:** With the Volume of Voice over IP (VoIP) traffic rises shapely, more and more VoIP-based steganography methods have emerged in recent years, which poses a great threat to the security of cyberspace.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hierarchical Representation Network for Steganalysis of QIM ** | 2019 | cs.MM | Hao Yang et al. [[1]](https://arxiv.org/abs/1910.04433) |

**State of the art:** Hierarchical Representation Network for QIM steganalysis in low-bit-rate speech. Uses CNN with three-level attention for hierarchical structure. Outperforms state-of-the-art on short and low embedding rate samples with lower computation.

**Production readiness:** Research
Academic prototype; addresses VoIP steganalysis.

**Security status:** Caution
New approach; requires validation on diverse VoIP datasets.

**Community acceptance:** Emerging
Important contribution to speech steganalysis; practical implications.

---

### Deep Learning in steganography and steganalysis from 2015 to 2018

**Goal:** of a deep neural network, in a generic way and present the networks proposed in existing literature for the different scenarios of steganalysis, and finally, we will discuss steganography by deep l...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Deep Learning in steganography and steganalysis from 2015 to** | 2019 | cs.CR | Marc Chaumont [[1]](https://arxiv.org/abs/1904.01444) |

**State of the art:** Comprehensive survey of deep learning in steganalysis (2015-2018). Covers CNN-based steganalysis, Rich Models, spatial/JPEG/selection-channel-aware steganalysis. Shows evolution from traditional methods to deep learning approaches. Published as book chapter in "Digital Media Steganography".

**Production readiness:** Research
Survey/book chapter; comprehensive overview of field.

**Security status:** N/A
Survey; provides research overview.

**Community acceptance:** Widely trusted
Authoritative survey by Marc Chaumont; widely cited.

---

### Spec-ResNet: A General Audio Steganalysis scheme based on Deep Residual Network of Spectrogram

**Goal:** are only effective in the specific embedded domain.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Spec-ResNet: A General Audio Steganalysis scheme based on De** | 2019 | cs.MM | Yanzhen Ren et al. [[1]](https://arxiv.org/abs/1901.06838) |

**State of the art:** First audio steganalysis using spectrogram + deep residual network (Spec-ResNet). Generalizes across AAC and MP3 steganography domains. Uses spectrogram as input to extract universal features from steganographic modifications. Better detection accuracy than hand-crafted and CNN-based methods.

**Production readiness:** Research
Academic prototype; 12-page paper with extensive evaluation.

**Security status:** Caution
Novel approach; requires validation on more audio codecs.

**Community acceptance:** Emerging
First work combining spectrogram analysis with deep residual networks for audio steganalysis.

---

### TS-CNN: Text Steganalysis from Semantic Space Based on Convolutional Neural Network

**Goal:** cybersecurity that helps to identify covert attacks in public network.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **TS-CNN: Text Steganalysis from Semantic Space Based on Convo** | 2018 | cs.CR | Zhongliang Yang et al. [[1]](https://arxiv.org/abs/1810.08136) |

**State of the art:** First text steganalysis for coverless steganography. Uses CNN to extract high-level semantic features. Detects subtle distribution differences in semantic space. Achieves nearly 100% precision/recall on CT-Steg dataset (216K texts). Can estimate hidden information capacity. Submitted to AAAI 2019.

**Production readiness:** Research
Published dataset CT-Steg; proof-of-concept model.

**Security status:** Caution
Only evaluated on specific coverless steganography methods.

**Community acceptance:** Emerging
Novel approach to text steganalysis; widely cited in coverless steganography research.

---

### Spatial Image Steganography Based on Generative Adversarial Network

**Goal:** With the recent development of deep learning on steganalysis, embedding secret information into digital images faces great challenges.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Spatial Image Steganography Based on Generative Adversarial ** | 2018 | cs.MM | Jianhua Yang et al. [[1]](https://arxiv.org/abs/1804.07939) |

**State of the art:** GAN-based steganography with generator (U-NET), embedding simulator (Tanh-simulator), and discriminator with SCA. Outperforms ASDL-GAN by 30% training time reduction. Beats S-UNIWARD in security. First to incorporate selection-channel awareness in GAN steganography framework.

**Production readiness:** Research
7-page paper; proof-of-concept with GAN architecture.

**Security status:** Caution
Novel approach; requires validation on diverse datasets.

**Community acceptance:** Emerging
Pioneering work in GAN-based steganography; frequently cited.

---

### A Novel Convolutional Neural Network for Image Steganalysis with Shared Normalization

**Goal:** attracted increasing attentions in recent years.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Convolutional Neural Network for Image Steganalysis ** | 2017 | cs.MM | Songtao Wu, Sheng-hua Zhong, Yan Liu [[1]](https://arxiv.org/abs/1711.07306) |

**State of the art:** Proposes Shared Normalization (SN) layer for CNN steganalysis. Addresses generalization issue in paired learning by sharing statistics across training/test batches. Stable training and better detection than prior methods on state-of-the-art steganography. Submitted to IEEE Transactions on Multimedia.

**Production readiness:** Research
Proof-of-concept CNN architecture; submitted to journal.

**Security status:** Caution
Novel normalization technique; requires more validation.

**Community acceptance:** Emerging
Addresses fundamental challenge in steganalysis deep learning.

---

### Convolutional Neural Network Steganalysis's Application to Steganography

**Goal:** This paper presents a novel approach to increase the performance bounds of image steganography under the criteria of minimizing distortion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Convolutional Neural Network Steganalysis's Application to S** | 2017 | cs.MM | Mehdi Sharifzadeh et al. [[1]](https://arxiv.org/abs/1711.02581) |

**State of the art:** Uses steganalysis CNN to identify less detectable regions for embedding. Calculates derivatives of image statistical model w.r.t. embedding changes. Outperforms HUGO, S-UNIWARD, HILL at low payloads. Note: overlap with arXiv:1705.08616.

**Production readiness:** Research
Proof-of-concept; novel application of steganalysis to steganography.

**Security status:** Caution
Practical implementation challenges; requires further validation.

**Community acceptance:** Emerging
Creative approach using detection network for embedding guidance.

---

### On the usefulness of information hiding techniques for wireless sensor networks security

**Goal:** the whole network at a certain time snapshot can be visualized as an image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On the usefulness of information hiding techniques for wirel** | 2017 | cs.MM, cs.SE | Rola Al-Sharif et al. [[1]](https://arxiv.org/abs/1706.08136) |

**State of the art:** Review of steganography/steganalysis for wireless sensor networks. Visualizes WSN sensory data as images. Shows sink cannot detect nsF5 attacks on sensed data. Novel application domain for information hiding.

**Production readiness:** Research
Survey paper; identifies research gaps in WSN steganography.

**Security status:** Caution
New attack vector; requires detection methods specific to WSN.

**Community acceptance:** Emerging
First review of WSN-specific steganography and steganalysis.

---

### MoveSteg: A Method of Network Steganography Detection

**Goal:** This article presents a new method for detecting a source point of time based network steganography - MoveSteg.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **MoveSteg: A Method of Network Steganography Detection** | 2016 | cs.MM, cs.CR | Krzysztof Szczypiorski, Tomasz Tyl [[1]](https://arxiv.org/abs/1610.01955) |

**State of the art:** Network steganalysis for time-based steganography. Detects source point of steganographic streams by analyzing packet delays. Can locate steganography source in networks under management. Novel approach to timing channel detection.

**Production readiness:** Research
Proof-of-concept detection method for time-based channels.

**Security status:** Caution
Limited to managed networks; specific to timing channels.

**Community acceptance:** Niche
First work on detecting source of time-based network steganography.

---

### Steganalysis via a Convolutional Neural Network using Large Convolution Filters for Embedding Process with Same Stego Key

**Goal:** For the past few years, in the race between image steganography and steganalysis, deep learning has emerged as a very promising alternative to steganalyzer approaches based on rich image models com...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis via a Convolutional Neural Network using Large ** | 2016 | cs.MM | Jean-François Couchot et al. [[1]](https://arxiv.org/abs/1605.07946) |

**State of the art:** CNN steganalysis with large convolution filters for "same embedding key" scenario. Outperforms other CNN steganalyzers and defeats state-of-the-art steganography. More general - handles larger images and lower payloads. Revised 3 versions on arXiv.

**Production readiness:** Research
Extensively revised; proof-of-concept CNN architecture.

**Security status:** Caution
Specific to known embedding key; less generalizable.

**Community acceptance:** Emerging
Pioneering work on CNN steganalysis with large filters.

---

### Steganalysis of Transcoding Steganography

**Goal:** TranSteg (Trancoding Steganography) is a fairly new IP telephony steganographic method that functions by compressing overt (voice) data to make space for the steganogram by means of transcoding.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganalysis of Transcoding Steganography** | 2012 | cs.CR, cs.MM | Artur Janicki, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1210.5888) |

**State of the art:** Steganalysis of VoIP transcoding steganography (TranSteg) using MFCC parameters and GMMs. Efficient detection for some codec pairs (G.711/G729), more resistant for others (iLBC/AMR). First steganalysis method for TranSteg.

**Production readiness:** Research
Proof-of-concept for VoIP steganalysis.

**Security status:** Caution
Codec-dependent detection rates; some pairs harder to detect.

**Community acceptance:** Niche
First work on TranSteg detection; specialized to VoIP.

---

### Towards Steganography Detection Through Network Traffic Visualisation

**Goal:** the proposed approach is the lack of direct, linear time dependencies for the created network traffic visualisations.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Steganography Detection Through Network Traffic Visu** | 2012 | cs.CR | Wojciech Mazurczyk, Krzysztof Szczypiorski, Bartosz Jankowski [[1]](https://arxiv.org/abs/1208.2861) |

**State of the art:** First use of network traffic visualization for steganalysis. Uses steg-tomography methodology without linear time dependencies. Novel approach to network steganography detection using visual analysis. Dedicated visualization tool developed.

**Production readiness:** Research
Novel concept; proof-of-concept visualization tool.

**Security status:** Caution
Early-stage research; requires more validation.

**Community acceptance:** Emerging
First work on traffic visualization for steganalysis; pioneering approach.

---

### DNS-HyXNet (xLSTM Real-Time DNS Tunnel Detection)

**Goal:** Detect DNS tunneling attacks in real time using a sequential xLSTM model that processes DNS packet sequences directly, avoiding the computational overhead of graph-based approaches while preserving high accuracy.

| Algorithm | Year | Architecture | Notable Feature |
|-----------|------|--------------|-----------------|
| **DNS-HyXNet** | 2025 | xLSTM sequential model | 99.99% accuracy; 0.041 ms detection latency per sample; deployable on commodity hardware [[1]](https://arxiv.org/abs/2512.09565) |

**State of the art:** Ali et al. (2025) — current best for real-time DNS tunnel detection by combining temporal dynamics modeling with low-latency inference. Extends naturally to DoH (DNS over HTTPS) and DoT (DNS over TLS) where payload is encrypted.

**Production readiness:** Mature
Deployable on standard hardware; suitable for inline NIDS deployment.

**Implementations:**
- No public reference release yet; benchmark code described in paper.

**Security status:** Effective
99.99% benchmark accuracy on standard DNS tunnel datasets (iodine, dnscat2, dns2tcp).

**Community acceptance:** Emerging
Recent (Dec 2025); xLSTM-based approach gaining attention as Transformer alternative for sequential network data.

---

## Benchmark Datasets

---

### BOSSBase

**Description:** Standard benchmark for steganography and steganalysis research.

| Dataset | Images | Size | Format | Note |
|---------|--------|------|--------|------|
| BOSSBase 1.01 | 10,000 | 512×512 | PNG (grayscale) | Original BOSS |

**Use:** Training and testing steganalysis algorithms. Widely used in academic research.

**Reference:** [BOSSBase website](https://agents.ucd.edu.pl/)

---

### BOWS2

**Description:** Break Our Watermarking System - second edition.

| Dataset | Images | Size | Format | Note |
|---------|--------|------|--------|------|
| BOWS2 | 10,000 | 512×512 | PNG | Contest variant |

**Use:** Watermarking and steganography competitions. Higher diversity than BOSSBase.

**Reference:** [BOWS2 website](https://bows2.ec-lille.fr/)

---

### ALASKA2

**Description:** Kaggle competition dataset for color image steganalysis.

| Dataset | Images | Size | Format | Note |
|---------|--------|------|--------|------|
| ALASKA2 | 80,000 | 512×512 | JPEG | Includes cover and stego variants |

**Use:** Training deep learning steganalysis models. Includes J-UNIWARD, UERD, nsf5 variants.

**Reference:** [ALASKA2 Kaggle](https://www.kaggle.com/c/alaska2-image-steganalysis)

---

### VISION

**Description:** Video steganalysis benchmark dataset.

| Dataset | Frames | Resolution | Note |
|---------|--------|------------|------|
| VISION | ~6,000 videos | Various | Standard for video stego |

**Use:** Video steganography detection research.

**Reference:** [VISION dataset](http://wins.huang.es/vision/)

---

### DVC

**Description:** Digital Video Corpus for steganalysis research.

| Dataset | Videos | Note |
|---------|--------|------|
| DVC | ~1,000 | Frame-based video stego |

**Use:** Video steganography detection and benchmarking.

**Reference:** Academic dataset; check relevant papers for access.

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

## Steganalysis Software Tools

---

### stegoVeritas

**Goal:** Automated multi-check steganalysis of JPEG, PNG, GIF, TIFF, and BMP files including metadata, LSB brute-force, and color-plane analysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **stegoVeritas** | 2019 | Multi-method automated scanner | LSB brute-force, metadata, color checks in one pass [[1]](https://github.com/bannsec/stegoVeritas) |

**State of the art:** Go-to automated pre-screening tool in CTF. Runs 20+ checks and saves results/extracted data per check automatically.

**Production readiness:** Mature
Stable Python tool; available via pip.

**Implementations:**
- [bannsec/stegoVeritas](https://github.com/bannsec/stegoVeritas) ⭐ 403 — Python, `pip install stegoveritas`

**Security status:** Caution
Detection-only tool; cannot defeat encrypted or exotic embedding schemes.

**Community acceptance:** Standard
Included in every major CTF stego toolkit.

---

### stegbreak

**Goal:** Brute-force crack JPEG images hidden with OutGuess, JPHide, or JSteg using a wordlist.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **stegbreak** | 2003 | Dictionary attack on JPEG stego | Targets outguess, jphide, jsteg simultaneously [[1]](https://github.com/DominicBreuker/stego-toolkit) |

**State of the art:** Classic JPEG stego cracker. Bundled in stego-toolkit Docker container. Largely superseded by stegseek for steghide but still unique for outguess/jphide targets.

**Production readiness:** Mature
Stable; available in stego-toolkit container and legacy repos.

**Security status:** Caution
Effective only against weak passphrases; strong keys resist dictionary attack.

**Community acceptance:** Standard
CTF standard for attacking password-protected JPEG stego files.

---

### pngcheck

**Goal:** Verify PNG file integrity and display detailed chunk-level structure for forensic analysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **pngcheck** | 1995 | PNG chunk parser and validator | Detects corrupted/modified chunk structure [[1]](http://www.libpng.org/pub/png/apps/pngcheck.html) |

**State of the art:** Standard PNG forensics tool. Useful for detecting non-standard chunks that carry hidden data.

**Production readiness:** Production
Stable, widely available via apt.

**Security status:** Caution
Only inspects structure; cannot detect LSB-level stego.

**Community acceptance:** Standard
Standard tool in PNG analysis workflows.

---

### Steganabara

**Goal:** Interactively transform and analyze images to reveal hidden steganographic content through visual inspection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganabara** | 2014 | Java GUI with interactive image transformations | Manual visual analysis; complement to automated tools [[1]](https://github.com/DominicBreuker/stego-toolkit) |

**State of the art:** GUI alternative to stegsolve. Bundled in stego-toolkit. Useful for manual visual inspection when automated tools miss non-standard encodings.

**Production readiness:** Mature
Stable Java tool; no active development but fully functional.

**Security status:** Caution
Reveals only visually encoded data; ineffective against encrypted stego.

**Community acceptance:** Niche
Known in CTF community; less popular than stegsolve.

---

### AperiSolve

**Goal:** Online multi-tool image steganalysis platform combining binwalk, exiftool, steghide, zsteg, foremost, and strings into one interface.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **AperiSolve** | 2019 | Web platform aggregating multiple steganalysis tools | Single URL submission returns output from 10+ tools [[1]](https://www.aperisolve.com) [[2]](https://github.com/Zeecka/AperiSolve) |

**State of the art:** Fastest CTF stego pre-screening: upload once, get results from all major tools simultaneously. Self-hostable.

**Production readiness:** Production
Actively maintained; public instance at aperisolve.com.

**Implementations:**
- [Zeecka/AperiSolve](https://github.com/Zeecka/AperiSolve) ⭐ 817 — Python/Flask, self-hostable

**Security status:** Caution
Public web tool; do not submit sensitive files to public instance.

**Community acceptance:** Standard
Widely referenced in CTF write-ups; the first tool many CTF players try.

---

### stego-toolkit

**Goal:** Docker container with 25+ pre-installed steganography and steganalysis tools plus automated screening scripts for CTF use.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **stego-toolkit** | 2017 | Docker image with curated tool collection | One-command install of entire stego CTF toolkit [[1]](https://github.com/DominicBreuker/stego-toolkit) |

**State of the art:** De facto standard CTF stego environment. Includes jphide, jsteg, outguess, steghide, stegano, cloackedpixel, openstego, mp3stego, spectrology, SonicVisualiser, and many more.

**Production readiness:** Production
Widely used; Docker image available on Docker Hub.

**Implementations:**
- [DominicBreuker/stego-toolkit](https://github.com/DominicBreuker/stego-toolkit) ⭐ 2.7k — Docker, `docker pull dominicbreuker/stego-toolkit`

**Security status:** Caution
Container with many tools; review individual tool security before use in sensitive environments.

**Community acceptance:** Standard
Referenced in CTF tutorials and write-ups worldwide.

---

### Stegdetect

**Goal:** Detect JPEG steganography from F5, JSteg, JPHide, and OutGuess using statistical signature analysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **stegdetect** | 2001 | Statistical JPEG stego detector | Simultaneously detects 4 major JPEG schemes; sensitivity tunable via `-t` flag [[1]](https://github.com/abeluck/stegdetect) |

**State of the art:** Pioneering JPEG stego detection tool by Niels Provos. Targets the same methods as stegbreak but for detection (not cracking). Superseded by ML-based tools but historically significant and still functional.

**Production readiness:** Deprecated
Unmaintained since ~2004; archived on GitHub; functional on modern Linux with minor patches.

**Implementations:**
- [abeluck/stegdetect](https://github.com/abeluck/stegdetect) ⭐ 425 — C, archived mirror

**Security status:** Caution
Only covers F5/JSteg/JPHide/OutGuess; misses modern adaptive methods. Use Aletheia for broader coverage.

**Community acceptance:** Niche
Historical reference; paired with stegbreak for JPEG stego analysis in CTF contexts.

---

### StegExpose

**Goal:** Batch-detect LSB steganography in PNG/BMP images using four statistical tests: Sample Pairs, RS analysis, Chi-Square, and Primary Sets.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegExpose** | 2014 | Multi-test LSB detector with threshold tuning | Combines 4 statistical tests; batch-processes entire directories [[1]](https://github.com/b3dk7/StegExpose) [[2]](https://arxiv.org/abs/1410.6656) |

**State of the art:** Best standalone Java tool for LSB detection. Outperforms single-test approaches by fusing multiple statistical signals. Threshold adjustable for precision/recall tradeoff.

**Production readiness:** Mature
Stable Java JAR; runs on any JVM; no installation needed.

**Implementations:**
- [b3dk7/StegExpose](https://github.com/b3dk7/StegExpose) ⭐ 240 — Java, `java -jar StegExpose.jar <dir>`

**Security status:** Secure
Detector (not hider); designed to break LSB security assumptions.

**Community acceptance:** Widely trusted
Peer-reviewed paper; referenced in academic steganalysis literature; standard CTF analysis step.

---

### Aletheia

**Goal:** Machine learning image steganalysis tool that detects steganography from F5, Steghide, LSB, J-UNIWARD, HUGO, WOW, and other modern adaptive methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Aletheia** | 2019 | ML-based steganalysis with ensemble classifiers and GAN-based calibration | Covers spatial and JPEG domain; includes training pipelines [[1]](https://github.com/daniellerch/aletheia) |

**State of the art:** Most advanced open-source steganalysis tool. Uses SRM/DCTR features with ensemble classifiers. Supports detector training on custom datasets. Active research tool from Daniel Lerch-Hostalot.

**Production readiness:** Experimental
Research-grade; requires training data for best accuracy; not plug-and-play.

**Implementations:**
- [daniellerch/aletheia](https://github.com/daniellerch/aletheia) ⭐ 204 — Python, `pip install aletheia`

**Security status:** Secure
Detector; ML models can be fooled by adversarial adaptive stego but represents state of art in open-source steganalysis.

**Community acceptance:** Emerging
Academic recognition; active development; covers widest range of modern stego schemes of any open tool.

---

### StegoForge

**Goal:** All-in-one Python steganography framework covering image, audio, video, documents, and network channels with 11 built-in detection engines.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegoForge** | 2024 | Multi-format stego + detection toolkit | Encode/decode + detect across 5 media types in one tool [[1]](https://github.com/Nour833/StegoForge) |

**State of the art:** Broadest-coverage single-tool stego framework. Combines embedding and detection across image (PNG/JPEG/BMP), audio (WAV/MP3), video (MP4/AVI), documents (PDF/DOCX), and network (DNS/HTTP headers).

**Production readiness:** Experimental
Active 2024 development; growing feature set; API not yet stable.

**Implementations:**
- [Nour833/StegoForge](https://github.com/Nour833/StegoForge) ⭐ 336 — Python

**Security status:** Caution
Broad coverage but methods are classical; detectable by dedicated per-format analyzers.

**Community acceptance:** Emerging
Newest multi-format toolkit; growing interest for CTF and research use.

---

