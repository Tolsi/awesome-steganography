# Steganalysis

<!-- TOC -->
## Contents (4 subcategories)

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
