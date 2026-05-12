# Image Steganography

<!-- TOC -->
## Contents (6 subcategories)

**[Spatial Domain](#spatial-domain)**
- [LSB Replacement](#lsb-replacement)
- [LSB Matching](#lsb-matching)
- [BPCS](#bpcs)
- [PVD](#pvd)
- [EMD](#emd)
- [Sudoku-based](#sudoku-based-steganography)
- [FuzzyStego](#fuzzystego)
- [Chaotic Map LSB](#chaotic-map-lsb)
- [Content-Aware Steganography](#content-aware-steganography)
- [Skin Tone Adaptive](#skin-tone-adaptive)
- [STC](#stc)

**[Adaptive Methods](#adaptive-methods)**
- [HUGO](#hugo)
- [WOW](#wow)
- [S-UNIWARD](#s-uniward)
- [HILL](#hill)
- [MiPOD](#mipod)
- [QIM](#qim)
- [MG/MVG](#mgmvg)

**[JPEG Domain](#jpeg-domain)**
- [JSteg](#jsteg)
- [F5](#f5)
- [nsF5](#nsf5)
- [OutGuess](#outguess)
- [J-UNIWARD](#j-uniward)
- [UED/UERD](#ueduerd)

**[Transform Domain](#transform-domain)**
- [DWT](#dwt)
- [DFT](#dft)
- [SVD](#svd)

**[Reversible Methods](#reversible-methods)**
- [Histogram Shifting](#histogram-shifting)
- [Difference Expansion](#difference-expansion)
- [Prediction Error Expansion](#prediction-error-expansion)

**[Deep Learning Methods](#deep-learning-methods)**
- [HiDDeN](#hidden)
- [SteganoGAN](#steganogan)
- [StegaStamp](#stegastamp)
- [CRoSS](#cross)
- [StegNet](#stegnet)
- [SMILENet](#smilenet)
- [StegoNGP](#stegongp)
- [DTAMS](#dtams)
- [PSyDUCK](#psyduck)
- [CIF](#cif)
- [STCL](#stcl)
- [GIFDL](#gifdl)
- [StegaFFD](#stegaffd)
- [Arbitrary-Resolution Deep Image Steganography](#arbitrary-resolution-deep-image-steganography)
- [Adaptive Fuzzy Logic Steganography](#adaptive-fuzzy-logic-steganography)
- [Memristive In-Memory Image Steganography](#memristive-in-memory-image-steganography)
- [StegaVision](#stegavision)
- [Foveation Steganography](#foveation-steganography)
- [StegaINR](#stegainr-steeganography-by-implicit-neural-representations)
- [StegaINR4MIH](#stegainr4mih-inr-for-multi-image-hiding)
- [DiffStega](#diffstega-training-free-diffusion-steganography)
- [Stable Messenger](#stable-messenger)
- [DKiS](#dkis-decay-weight-invertible-image-steganography)
- [PRIS](#pris-practical-robust-invertible-network-for-image-steganography)
- [Multi-User Multi-Key](#multi-user-multi-key-image-steganography)
- [StegaPos](#stegapos)
- [Rethinking Security of Diffusion-based Generative Steganography](#rethinking-security-of-diffusion-based-generative-steganography)
- [Intelligent Carrier Allocation](#intelligent-carrier-allocation)
- [Secure Audio Embedding in Images](#secure-audio-embedding-in-images)
- [Deep Data Hiding for ICAO-Compliant Face Images](#deep-data-hiding-for-icao-compliant-face-images)
- [Defending against Stegomalware](#defending-against-stegomalware)
- [On the Possible Detectability of Image-in-Image Steganography](#on-the-possible-detectability-of-image-in-image-steganography)
- [Robust Provably Secure Image Steganography via Latent Iterative Optimization](#robust-provably-secure-image-steganography-via-latent-iterative-optimization)
<!-- /TOC -->

## Spatial Domain

---

### LSB Replacement

**Goal:** Hide data by replacing the least significant bit of each pixel.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LSB Replacement** | 1998 | Replace LSB of pixel | 1 bpp (3 bpp RGB) |

**State of the art:** Simplest method. Good for learning but easily detected.

**Production readiness:** Deprecated

**Implementations:**
- [steghide](https://github.com/StephanHofmannmich/steghide) ⭐ 1.8k — Classic LSB tool
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287

**Security status:** Broken — Detected by chi-square, RS-analysis in milliseconds

**Community acceptance:** Niche — Good for learning, not for production

---

### LSB Matching

**Goal:** Hide data with reduced statistical artifacts compared to LSB replacement.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LSB Matching** | 2006 | Random +/-1 if LSB ≠ bit | 1 bpp [[1]](https://ieeexplore.ieee.org/document/1618698/) |

**State of the art:** Better than replacement, still vulnerable to WS analysis.

**Production readiness:** Mature
Well-studied; preferred over LSB replacement for its reduced statistical signature.

**Implementations:**
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, includes LSB matching variants and steganalysis

**Security status:** Caution — Vulnerable to weighted stego (WS) analysis

**Community acceptance:** Widely trusted — Standard in steganography courses

---

### BPCS

**Goal:** Hide data in complex bit-planes of the image.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **BPCS** | 1998 | Replace complex bit-planes | 10-40% capacity |

**State of the art:** Higher capacity than LSB while maintaining visual quality.

**Production readiness:** Mature

**Implementations:**
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287 — Includes BPCS

**Security status:** Caution — Detected by complexity analysis attacks

**Community acceptance:** Niche — Popular in watermarking, less in pure stego

---

### PVD

**Goal:** Adaptively embed more data in edge regions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **PVD** | 2003 | Embed in pixel difference | 3-5 bpp [[1]](https://dl.acm.org/doi/10.1016/S0167-8655(02)00402-6) |

**State of the art:** Adaptive capacity based on local contrast.

**Production readiness:** Mature
Widely implemented with well-known range-table variants; good tradeoff between capacity and quality.

**Implementations:**
- [tony-josi/pvd_steganography](https://github.com/tony-josi/pvd_steganography) ⭐ 22 — Python, PNG cover images

**Security status:** Caution — Vulnerable to histogram analysis of differences

**Community acceptance:** Widely trusted — Widely studied and implemented

---

### EMD

**Goal:** Encode data using multiple pixels with minimal modification.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **EMD** | 2006 | n pixels encode d-ary digit | log2(2n+1)/n bpp [[1]](https://www.researchgate.net/publication/3417888_Efficient_Steganographic_Embedding_by_Exploiting_Modification_Direction) |

**State of the art:** Better PSNR than LSB, mathematically elegant.

**Production readiness:** Mature
Frequently re-implemented in academic papers; not commonly used in production tools.

**Implementations:**
- [cagatayavsar/EMD](https://github.com/cagatayavsar/EMD) ⭐ 0 — Python/C++, direct implementation of Zhang & Wang (2006)

**Security status:** Caution — Good perceptual quality but specific statistical signature

**Community acceptance:** Niche — Academic interest, practical use limited

---

### Sudoku-based Steganography

**Goal:** Use Sudoku puzzle solutions as encoding key.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Sudoku** | 2009 | Sudoku grid key | High key space [[1]](https://dl.acm.org/doi/10.1109/ARTCom.2009.116) |

**State of the art:** Large key space provides security.

**Production readiness:** Experimental
Academic prototypes only; the large Sudoku key space improves robustness against brute-force steganalysis.

**Security status:** Caution
Security relies on key secrecy; no dedicated steganalysis attacks published, but underlying pixel modification is detectable.

**Community acceptance:** Niche
Cited in academic literature but no mainstream adoption.

---

### FuzzyStego

**Goal:** Use fuzzy logic for adaptive embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **FuzzyStego** | 2025 | Fuzzy logic intensity classification | Adaptive [[1]](https://doi.org/10.32604/cmc.2025.061246) |

**State of the art:** Adaptive approach using fuzzy logic; achieves average PSNR of 58.6 dB.

**Production readiness:** Experimental
Proposed in 2025; no production deployments; promising PSNR results at lower payloads.

**Security status:** Caution
Uses LSB-derived embedding; underlying pixel modification is vulnerable to standard steganalysis.

**Community acceptance:** Niche
Recent publication; limited citations so far.

---

### Chaotic Map LSB

**Goal:** Use chaotic maps for secure LSB embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chaotic Map LSB** | 2008 | Chaos-based pixel selection | Increased security [[1]](https://www.sciencedirect.com/science/article/abs/pii/S0045790624004932) |

**State of the art:** Chaotic sequences add security layer by randomizing embedding positions.

**Production readiness:** Experimental
Used in academic work; not production-hardened; chaotic key sensitivity is both a strength and implementation risk.

**Implementations:**
- [FifthEpoch/Chaos_LSB](https://github.com/FifthEpoch/Chaos_LSB) ⭐ 0 — Python, AES + chaotic pixel selection

**Security status:** Caution
Chaotic key randomizes positions but underlying LSB embedding is still detectable by calibration attacks.

**Community acceptance:** Niche
Popular research topic; many variant papers published but no standard definition.

---

### Content-Aware Steganography

**Goal:** Hide data based on semantic content of image.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Content-Aware** | 2006 | Human-assigned semantics | Secure against non-human [[1]](https://link.springer.com/chapter/10.1007/978-3-540-74124-4_8) |

**State of the art:** Uses semantic understanding; embeds secrets in human-interpretable cover meaning rather than pixel values.

**Production readiness:** Experimental
Theoretical framework; no widely adopted tooling exists.

**Security status:** Secure — Human adversary required; automated steganalysis is ineffective

**Community acceptance:** Emerging
Influential theoretical paper but limited practical implementations.

---

### Skin Tone Adaptive

**Goal:** Embed in skin-tone regions using secret angle.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Skin Tone Adaptive** | 2009 | Skin region detection via colour space | Adaptive embedding [[1]](https://www.sciencedirect.com/science/article/abs/pii/S0165168409001686) |

**State of the art:** Adaptive based on image content; psychovisual redundancy in skin tones reduces perceptibility.

**Production readiness:** Experimental
Academic prototype; requires reliable skin detection as pre-processing step.

**Security status:** Caution
Skin region detection can be replicated by an attacker; embedding within detected regions is not invisible to trained classifiers.

**Community acceptance:** Emerging
Cited in adaptive steganography surveys; not widely deployed.

---

### STC

**Goal:** Near-optimal embedding with minimal distortion.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **STC** | 2010 | Syndrome-Trellis Codes | Near rate-distortion bound |

**State of the art:** Foundation of modern adaptive steganography. Theoretical optimality.

**Production readiness:** Mature

**Implementations:**
- [stc-lib](https://github.com/coin3d/stc-lib) ⭐ 89 — C++ implementation

**Security status:** Secure — Enables best-in-class security with good distortion functions

**Community acceptance:** Widely trusted — Industry standard for modern stego algorithms

---

## Adaptive Methods

---

### HUGO

**Goal:** Model-driven adaptive steganography using detection features.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HUGO** | 2010 | SPAM features (4D co-occurrence) | First model-driven [[1]](https://link.springer.com/chapter/10.1007/978-3-642-16435-4_13) |

**State of the art:** Theoretically principled — optimizes against known detection features.

**Production readiness:** Mature
Reference Matlab implementation from DDE Binghamton; widely used as research baseline.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, includes HUGO, HILL, MiPOD simulators
- [dde.binghamton.edu](http://dde.binghamton.edu/download/stego_algorithms/) — original Matlab/MEX reference code

**Security status:** Secure — Strong against SPAM-based detectors

**Community acceptance:** Widely trusted — Foundational work, frequently cited (1000+)

---

### WOW

**Goal:** Embed primarily in edge regions using wavelet filters.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **WOW** | 2012 | Wavelet directional filters | Edge-only embedding |

**State of the art:** Good balance of capacity and security.

**Production readiness:** Mature

**Implementations:**
- [WOW-steganography](https://github.com/3xpl01tc0d3r/WOW-steganography) ⭐ 156

**Security status:** Secure — Competitive security

**Community acceptance:** Widely trusted — Widely implemented

---

### S-UNIWARD

**Goal:** Universal distortion function for steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **S-UNIWARD** | 2013 | Universal wavelet relative distortion | Best security |

**State of the art:** Works in both spatial and JPEG domain. Often cited as best-in-class.

**Production readiness:** Mature

**Implementations:**
- [nsf5sim](https://github.com/goxman/nsf5sim) ⭐ 78 — Includes S-UNIWARD

**Security status:** Secure — Often achieves best detection resistance

**Community acceptance:** Standard — De facto standard, most cited adaptive algorithm

---

### HILL

**Goal:** Distribute modifications to avoid concentrating in edges.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HILL** | 2014 | High-pass + low-pass smoothing | Distributes changes [[1]](https://ieeexplore.ieee.org/document/7025854/) |

**State of the art:** Competitive with S-UNIWARD.

**Production readiness:** Mature
Frequently used benchmark in steganalysis research; Matlab reference implementation available from DDE.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, HILL simulator matching DDE Matlab output
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, includes HILL

**Security status:** Secure — Competitive with S-UNIWARD

**Community acceptance:** Widely trusted — Popular in implementations

---

### MiPOD

**Goal:** Theoretically optimal embedding under Gaussian assumptions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MiPOD** | 2016 | Multivariate Gaussian | Fisher information optimal [[1]](https://dl.acm.org/doi/10.1109/tifs.2015.2486744) |

**State of the art:** Strong theoretical foundation; minimizes power of optimal Bayesian detector.

**Production readiness:** Experimental
Academic prototype; Matlab reference from DDE; Python reimplementation in conseal.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, MiPOD simulator
- [dde.binghamton.edu](http://dde.binghamton.edu/download/stego_algorithms/) — original Matlab reference

**Security status:** Secure — Strong theoretical guarantees

**Community acceptance:** Emerging — Academic interest, fewer practical implementations

---

## JPEG Domain

---

### JSteg

**Goal:** Original JPEG steganography using LSB.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **JSteg** | 1997 | LSB on DCT coefficients | Historical [[1]](http://www.cosy.sbg.ac.at/~uhl/jsteg.html) |

**State of the art:** Deprecated due to easy detection.

**Production readiness:** Deprecated
No longer recommended; the original tool by Derek Upham (1997) is still referenced in academic literature.

**Implementations:**
- [daniellerch/aletheia](https://github.com/daniellerch/aletheia) ⭐ 204 — Python steganalysis tool, includes JSteg detection

**Security status:** Broken — One of first detected by histogram analysis

**Community acceptance:** Niche — Historical importance, not recommended

---

### F5

**Goal:** Matrix encoding for efficient JPEG steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **F5** | 2001 | Matrix encoding + decrement | Better efficiency |

**State of the art:** Historically important but vulnerable to attacks.

**Production readiness:** Deprecated

**Implementations:**
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287

**Security status:** Broken — Vulnerable to shrinkage attack, blockiness analysis

**Community acceptance:** Niche — Historically important

---

### nsF5

**Goal:** F5 without shrinkage for better quality.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **nsF5** | 2007 | F5 without shrinkage (wet paper) | Better visual quality [[1]](https://dde.binghamton.edu/download/nsf5simulator/) [[2]](https://dl.acm.org/doi/10.1145/1341811.1341814) |

**State of the art:** Better than F5 but still detected.

**Production readiness:** Deprecated
Simulator available from DDE Binghamton; not for production use.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, nsF5 simulator
- [dde.binghamton.edu/download/nsf5simulator/](https://dde.binghamton.edu/download/nsf5simulator/) — original Matlab simulator (2008)

**Security status:** Caution — Better than F5 but still detected by CCJRM

**Community acceptance:** Niche
Used as baseline in JPEG steganalysis research.

---

### OutGuess

**Goal:** Preserve global DCT histogram during embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **OutGuess** | 2001 | Preserves global histogram | Statistical preservation [[1]](https://en.wikipedia.org/wiki/OutGuess) [[2]](https://ws2.binghamton.edu/fridrich/Research/acm_outguess.pdf) |

**State of the art:** Vulnerable to local statistics attacks.

**Production readiness:** Deprecated
Historically used in real cases (e.g. Annanet spy ring); now easily detected.

**Implementations:**
- [outguess](https://github.com/crorvick/outguess) ⭐ 0 — C, original tool by Niels Provos

**Security status:** Broken — Vulnerable to local statistics attacks

**Community acceptance:** Niche
Historically significant but superseded by adaptive methods.

---

### J-UNIWARD

**Goal:** Best JPEG steganography against modern steganalysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **J-UNIWARD** | 2014 | UNIWARD on DCT | Best for JPEG [[1]](https://jis-eurasipjournals.springeropen.com/articles/10.1186/1687-417X-2014-1) |

**State of the art:** State-of-art for JPEG domain.

**Production readiness:** Mature
Reference Matlab code from DDE Binghamton; Python in conseal and stegolab.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, J-UNIWARD simulator
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, J-UNIWARD implementation

**Security status:** Secure — State-of-art for JPEG

**Community acceptance:** Widely trusted
De facto standard JPEG steganography method in research.

---

### UED/UERD

**Goal:** Uniform distribution of changes across AC coefficients.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **UED/UERD** | 2014/2015 | Uniform embedding across DCT magnitudes | Competitive [[1]](https://ieeexplore.ieee.org/document/6776485/) [[2]](https://dl.acm.org/doi/abs/10.1109/tifs.2015.2473815) |

**State of the art:** Competitive with J-UNIWARD.

**Production readiness:** Mature
UERD rivals J-UNIWARD with significantly lower computational cost.

**Implementations:**
- [vazswk/UERD](https://github.com/vazswk/UERD) ⭐ 0 — Matlab, UERD simulator
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, UERD simulator

**Security status:** Secure — Competitive with J-UNIWARD

**Community acceptance:** Emerging
Growing use in JPEG steganalysis benchmarks.

---

### QIM

**Goal:** Embed data using quantization index modulation.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **QIM** | 2001 | Quantization-based | High robustness [[1]](https://ieeexplore.ieee.org/document/923725/) |

**State of the art:** Robust to compression, mathematically principled.

**Production readiness:** Mature
Foundational watermarking technique; used in audio/video watermarking pipelines.

**Security status:** Caution — Detectable by trained classifiers

**Community acceptance:** Widely trusted — Foundational watermarking method

---

### MG/MVG

**Goal:** Multi-grade variable group embedding for high capacity.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MG/MVG** | 2011 | Multi-variable groups | High capacity [[1]](https://www.researchgate.net/publication/261601440_Uniform_Embedding_for_Efficient_JPEG_Steganography) |

**State of the art:** High capacity with good visual quality.

**Production readiness:** Experimental
Academic prototypes only; not widely deployed.

**Security status:** Caution
High capacity often trades off against detectability.

**Community acceptance:** Emerging
Cited in capacity-focused steganography literature.

---

## Transform Domain

---

### DWT

**Goal:** Embed in wavelet domain for robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DWT** | 1996 | High-frequency wavelet subbands | HH, HL, LH bands [[1]](https://dl.acm.org/doi/abs/10.1145/240178.240217) |

**State of the art:** Good robustness to compression.

**Production readiness:** Mature
Basis for many practical watermarking systems; widely implemented in toolkits.

**Implementations:**
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, multiple transform-domain methods

**Security status:** Caution
Modified wavelet coefficients are detectable by statistical feature extractors.

**Community acceptance:** Widely trusted
Core technique in digital watermarking standards.

---

### DFT

**Goal:** Embed in frequency domain for geometric robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DFT** | 2005 | Magnitude/phase spectrum | Robust to rotation [[1]](https://www.researchgate.net/publication/269705199_Digital_Image_Steganography_An_FFT_Approach) |

**State of the art:** Robust to geometric transforms.

**Production readiness:** Mature
Used in geometric-robust watermarking; less common in pure steganography due to limited capacity.

**Security status:** Caution
DFT modifications are detectable by frequency-domain steganalysis.

**Community acceptance:** Niche
Preferred for geometric robustness applications; limited adoption in steganography.

---

### SVD

**Goal:** Modify singular values for robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SVD** | 2002 | Modify singular values | Often combined with DWT [[1]](https://link.springer.com/article/10.1007/s11042-017-4947-8) |

**State of the art:** Very robust to noise and filtering.

**Production readiness:** Mature
Frequently combined with DWT (DWT-SVD hybrid) for improved robustness and imperceptibility.

**Security status:** Caution
Singular value modifications can be detected; known false-positive issues in some SVD watermarking schemes.

**Community acceptance:** Widely trusted
Extensively studied; standard in robust watermarking literature.

---

## Reversible Methods

---

### Histogram Shifting

**Goal:** Lossless data hiding by shifting histogram.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Histogram Shifting** | 2006 | Shift histogram peak | Lossless [[1]](https://web.njit.edu/~ansari/papers/06TCAS.pdf) |

**State of the art:** Important for medical/legal imaging.

**Production readiness:** Mature
Foundational reversible data hiding technique; base for many subsequent improvements.

**Security status:** Secure — Lossless recovery guaranteed

**Community acceptance:** Widely trusted — Critical for sensitive imaging

---

### Difference Expansion

**Goal:** Expand pixel differences to embed data.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Difference Expansion** | 2003 | Expand differences | Lossless [[1]](https://ieeexplore.ieee.org/document/1227616/) |

**State of the art:** Foundational reversible method.

**Production readiness:** Mature
Tian (2003) is one of the most cited RDH papers; basis for many subsequent schemes.

**Security status:** Secure
Lossless pixel recovery; no known attacks that compromise cover/hidden content.

**Community acceptance:** Widely trusted
Foundational method; extensively cited in reversible data hiding literature.

---

### Prediction Error Expansion

**Goal:** Embed in prediction error for better efficiency.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Prediction Error Expansion** | 2007 | Embed in prediction error | Better than DE [[1]](https://ieeexplore.ieee.org/document/4099409/) |

**State of the art:** Improved efficiency over difference expansion.

**Production readiness:** Mature
Thodi & Rodriguez (2007) significantly improved on DE; widely used as baseline for RDH advances.

**Security status:** Secure
Lossless recovery guaranteed; no practical attacks on the hiding mechanism.

**Community acceptance:** Widely trusted
Extensively cited; considered standard alongside histogram shifting.

---

## Deep Learning Methods

---

### HiDDeN

**Goal:** End-to-end deep learning steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **HiDDeN** | 2018 | Encoder-decoder + noise | First end-to-end DL |

**State of the art:** Foundational work in DL steganography.

**Production readiness:** Experimental

**Implementations:**
- [HiDDeN](https://github.com/tancik/HiDDeN) ⭐ 892

**Security status:** Caution — Vulnerable to CNN steganalysis

**Community acceptance:** Widely trusted — Foundational work in DL stego

---

### SteganoGAN

**Goal:** GAN-based steganography with high capacity.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SteganoGAN** | 2019 | GAN + critic | 2-4 bpp |

**State of the art:** High capacity, defeats XuNet.

**Production readiness:** Experimental

**Implementations:**
- [SteganoGAN](https://github.com/DAI-Lab/SteganoGAN) ⭐ 428

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### StegaStamp

**Goal:** Robust steganography surviving physical transmission.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaStamp** | 2020 | Robust encoder + augmentation | Survives print+photo |

**State of the art:** First practical robust steganography.

**Production readiness:** Experimental

**Implementations:**
- [StegaStamp](https://github.com/tancik/StegaStamp) ⭐ 1.2k

**Security status:** Secure — Robust to printing/photo

**Community acceptance:** Standard — Most practical DL method

---

### CRoSS

**Goal:** Diffusion-based steganography with natural cover distribution.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **CRoSS** | 2023 | Diffusion-based | Message controls seed/path [[1]](https://arxiv.org/abs/2305.16936) |

**State of the art:** State-of-art in generative stego.

**Production readiness:** Experimental
NeurIPS 2023 paper with official implementation; widely referenced in generative steganography literature.

**Implementations:**
- [CRoSS](https://github.com/yujiwen/CRoSS) ⭐ 157 — PyTorch, official NeurIPS 2023 implementation

**Security status:** Secure — State-of-art in generative stego; first to use diffusion models for controllable, robust, secure hiding

**Community acceptance:** Emerging — Growing rapidly; cited as foundational in diffusion-based steganography

---

### StegNet

**Goal:** High-capacity deep learning steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegNet** | 2018 | Multi-scale CNN | 98.2% decoding, 23.57 bpp [[1]](https://arxiv.org/abs/1806.06357) |

**State of the art:** Very high capacity image-in-image steganography using deep convolutional networks.

**Production readiness:** Research
Academic prototype; published 2018 in MDPI Future Internet journal.

**Security status:** Caution — Resistant to 5 classical steganalysis methods but not evaluated against modern CNN detectors

**Community acceptance:** Emerging — Research active; frequently cited in DL steganography surveys

---

### SMILENet

**Goal:** Extra-large capacity image steganography via synergistic mosaic.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SMILENet** | 2025 | Synergistic mosaic invertible hiding | 25x image hiding [[1]](https://arxiv.org/abs/2503.05118) |

**State of the art:** Achieves 25x image hiding capacity, first to hide 25 secret images simultaneously.

**Production readiness:** Research
arXiv preprint March 2025; no production deployments known.

**Security status:** Caution — Security against modern steganalysis not yet evaluated

**Community acceptance:** Emerging — Very recent; addresses fundamental capacity limitations of prior methods

---

### DTAMS

**Goal:** High-capacity generative steganography via dynamic multi-timestep selection.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DTAMS** | 2026 | Dynamic multi-timestep + adaptive deviation mapping | Latent diffusion [[1]](https://arxiv.org/abs/2602.01160) |

**State of the art:** High capacity with good security at higher rates; addresses limitations of existing generative steganography at low embedding rates only.

**Production readiness:** Experimental
arXiv preprint February 2026; no production deployments known.

**Security status:** Secure — Maintains acceptable security and robustness at higher embedding rates

**Community acceptance:** Emerging — Recent paper addressing capacity-security tradeoff in latent diffusion steganography

---

### Approximate Gaussian Mapping

**Goal:** Generative image steganography using approximate Gaussian mapping.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Approximate Gaussian** | 2025 | ODE-based diffusion models | Deterministic synthesis [[1]](https://arxiv.org/abs/2510.07219) |

**State of the art:** Reduces numerical inversion errors in ODE-based diffusion steganography by allowing controlled deviations from standard normal prior.

**Production readiness:** Experimental
arXiv preprint October 2025; academic prototype only.

**Security status:** Secure — Controlled deviation from Gaussian prior reduces inversion errors without compromising security

**Community acceptance:** Emerging — Addresses a specific inversion error problem in diffusion-based steganography

---

### PSyDUCK

**Goal:** Training-free steganography for latent diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PSyDUCK** | 2025 | Training-free latent diffusion | Message projection [[1]](https://arxiv.org/abs/2501.19172) |

**State of the art:** No training required; extends generative steganography to latent-space video diffusion models.

**Production readiness:** Experimental
arXiv preprint January 2025; model-agnostic, no fine-tuning needed.

**Security status:** Secure — Dynamically adapts embedding strength to balance accuracy and detectability

**Community acceptance:** Emerging — Addresses scalability limitation of prior training-dependent approaches

---

### CIF

**Goal:** Reliable message extraction in diffusion-based generative steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **CIF** | 2025 | Constrained inversion framework | High-capacity embedding [[1]](https://arxiv.org/abs/2508.00434) |

**State of the art:** Improves extraction accuracy in lossy scenarios by iteratively recovering secret-embedded latent vectors.

**Production readiness:** Experimental
arXiv preprint August 2025; addresses extraction failure in high-capacity or lossy-transmission scenarios.

**Security status:** Secure — Constrained inversion maintains indistinguishability of generated images

**Community acceptance:** Emerging — Solves a practical extraction accuracy problem in diffusion-based generative steganography

---

### STCL (Spatial-Temporal Curriculum Learning)

**Goal:** Improve image steganography quality through progressive multi-scale curriculum learning.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **STCL** | 2025 | Progressive multi-scale convolutional | Better convergence [[1]](https://arxiv.org/abs/2504.17609) |

**State of the art:** Addresses poor quality and slow convergence issues in deep learning image steganography.

**Production readiness:** Research
arXiv preprint April 2025; academic prototype only.

**Security status:** Caution — Security properties not fully evaluated; focus is on quality and convergence

**Community acceptance:** Emerging — Part of a series of curriculum learning approaches for deep image steganography

---

### GIFDL (Generated Image Fluctuation Distortion Learning)

**Goal:** Enhance steganographic security through fluctuation distortion learning.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **GIFDL** | 2025 | Distortion learning framework | Enhanced security [[1]](https://arxiv.org/abs/2504.15139) |

**State of the art:** Improves minimum distortion steganography security; accepted by IEEE TIFS.

**Production readiness:** Research
Accepted by IEEE Transactions on Information Forensics and Security; academic prototype only.

**Security status:** Secure — Specifically designed to enhance security of minimum distortion steganography

**Community acceptance:** Emerging — IEEE TIFS acceptance indicates peer-reviewed quality

---

### StegaFFD (Steganography-based Face Forgery Detection)

**Goal:** Privacy-preserving face forgery detection via steganographic domain lifting.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaFFD** | 2026 | Steganography-based FFD framework | Privacy protection [[1]](https://arxiv.org/abs/2603.02886) |

**State of the art:** Protects privacy without raising suspicion; accepted by Machine Intelligence Research.

**Production readiness:** Research
arXiv preprint March 2026; accepted by Machine Intelligence Research journal.

**Security status:** Caution — Designed for forensic use, not covert communication; detection resistance not primary goal

**Community acceptance:** Emerging — Novel application of steganography to privacy-preserving deepfake detection

---

### Arbitrary-Resolution Deep Image Steganography

**Goal:** Hide secret images with different resolutions than cover images.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Arb-Resolution DIS** | 2026 | Resolution-flexible framework | No resampling required [[1]](https://arxiv.org/abs/2601.15739) |

**State of the art:** Solves resolution mismatch problem in deep steganography; eliminates detail loss from resampling.

**Production readiness:** Research
arXiv preprint January 2026; academic prototype only.

**Security status:** Caution — Security properties not yet fully characterized; focus is on resolution flexibility

**Community acceptance:** Emerging — Addresses a practical limitation in current deep image steganography frameworks

---

### Adaptive Fuzzy Logic Steganography

**Goal:** Adaptive embedding using fuzzy logic for better capacity-fidelity trade-off.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Fuzzy Logic Stego** | 2026 | Fuzzy logic-based embedding | Adaptive depth [[1]](https://arxiv.org/abs/2603.18105) |

**State of the art:** Better imperceptibility than fixed-depth LSB by adapting embedding depth based on local texture complexity.

**Production readiness:** Research
arXiv preprint March 2026; academic prototype only.

**Security status:** Caution — Adaptive LSB variant; improved over fixed-depth but still vulnerable to statistical steganalysis

**Community acceptance:** Emerging — Experimental evaluation demonstrates improved PSNR/SSIM over fixed-depth LSB

---

### Memristive In-Memory Image Steganography

**Goal:** Hardware-based steganography using memristive circuits.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Memristive Stego** | 2026 | In-memory computing | 42-44% energy reduction [[1]](https://arxiv.org/abs/2605.03494) |

**State of the art:** First hardware implementation of steganography using memristive in-memory computing circuits.

**Production readiness:** Experimental
arXiv preprint May 2026; custom circuit prototypes only, not software-deployable.

**Security status:** Caution — Hardware-level hiding; security depends on physical access constraints rather than algorithmic hardness

**Community acceptance:** Emerging — Novel hardware approach; bridges steganography and in-memory computing research

---

### StegaVision

**Goal:** Enhance steganography using attention mechanisms for better capacity-quality balance.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaVision** | 2024 | Attention-based network | Improved capacity [[1]](https://arxiv.org/abs/2411.05838) |

**State of the art:** Uses parallel channel and spatial attention to simultaneously improve image quality and hiding capacity.

**Production readiness:** Research
arXiv preprint November 2024 (AAAI 2025 Student Abstract); academic prototype only.

**Security status:** Caution — Attention-based architecture; security against CNN steganalysis not fully evaluated

**Community acceptance:** Emerging — Demonstrates that attention mechanisms overcome the quality-capacity tradeoff seen in prior methods

---

### Foveation Steganography

**Goal:** Improve payload capacity using foveated rendering and latent representations.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Foveation** | 2025 | Foveated rendering + latent | 100→500 bits capacity [[1]](https://arxiv.org/abs/2510.13151) |

**State of the art:** Achieves up to 500 bits with 1 failure bit out of 2000; presented at SIGGRAPH Asia 2025.

**Production readiness:** Research
SIGGRAPH Asia 2025 Posters; academic prototype only.

**Security status:** Caution — Focus on capacity improvement; steganalysis resistance not primary evaluation criterion

**Community acceptance:** Emerging — SIGGRAPH Asia venue indicates visibility in graphics/vision community

---

### StegaINR (Steganography by Implicit Neural Representations)

**Goal:** Hide functions within functions using INR without additional extractors.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaINR** | 2023 | INR-based | No message extractor needed [[1]](https://arxiv.org/abs/2312.04743) |

**State of the art:** First work to introduce INR into steganography; hides secret function inside stego function using a shared key.

**Production readiness:** Research
arXiv preprint December 2023; academic prototype only.

**Security status:** Caution — Novel paradigm; security properties under active investigation

**Community acceptance:** Emerging — First exploration of hiding information in INR model weights

---

### StegaINR4MIH (INR for Multi-Image Hiding)

**Goal:** Embed multiple secret images into a cover image with high quality recovery.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaINR4MIH** | 2024 | INR multi-image | High capacity [[1]](https://arxiv.org/abs/2410.10117) |

**State of the art:** Addresses contour shadowing and color distortion issues; achieves PSNR >42 for 2 secret images, >39 for 5 secret images.

**Production readiness:** Research
arXiv preprint October 2024; academic prototype with code available.

**Security status:** Caution — Security against steganalysis not primary focus; designed for high-quality multi-image hiding

**Community acceptance:** Emerging — Extends StegaINR to practical multi-image hiding with quantified quality guarantees

---

### DiffStega (Training-Free Diffusion Steganography)

**Goal:** Training-free coverless image steganography using diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DiffStega** | 2024 | Diffusion-based | Training-free [[1]](https://arxiv.org/abs/2407.10459) |

**State of the art:** Universal training-free coverless diffusion steganography; uses password-dependent reference image and Noise Flip technique; IJCAI 2024.

**Production readiness:** Research
Published at IJCAI 2024; official implementation available.

**Implementations:**
- [DiffStega](https://github.com/evtricks/DiffStega) ⭐ 49 — PyTorch, official IJCAI 2024 implementation

**Security status:** Secure — Password-dependent reference image prevents unauthorized decryption; no risk of text prompt leakage

**Community acceptance:** Emerging — IJCAI 2024 acceptance; addresses key limitations of prior CRoSS-style prompt-based methods

---

### Stable Messenger

**Goal:** Message-concealed image generation with high message accuracy.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Stable Messenger** | 2023 | Message-driven generation | Full message recovery [[1]](https://arxiv.org/abs/2312.01284) |

**State of the art:** Introduces message accuracy metric evaluating entirety of decoded messages; uses latent-aware encoding with Stable Diffusion.

**Production readiness:** Research
arXiv preprint December 2023; academic prototype only.

**Security status:** Caution — Focuses on message accuracy and image quality; steganalysis resistance not primary evaluation

**Community acceptance:** Emerging — Proposes novel holistic evaluation metric for generative steganography

---

### DKiS (Decay weight Invertible image Steganography)

**Goal:** Private key-based image steganography with decay weight mechanism.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DKiS** | 2023 | Invertible network | Private key security [[1]](https://arxiv.org/abs/2311.18243) |

**State of the art:** First high-capacity invertible steganography with private key; decay weight mechanism controls information transfer from secret to host pipeline.

**Production readiness:** Research
arXiv November 2023; published in Neural Networks (Elsevier) 2025; code available.

**Implementations:**
- [DKiS](https://github.com/yanghangAI/DKiS) ⭐ 7 — PyTorch, official implementation

**Security status:** Secure — Private key required for extraction; decay weight filters out irrelevant information leakage

**Community acceptance:** Emerging — Published in Neural Networks journal; introduces key-based security to invertible steganography

---

### PRIS (Practical Robust Invertible Network for Image Steganography)

**Goal:** Robust and invertible network for image steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PRIS** | 2023 | Invertible network | Robust + invertible [[1]](https://arxiv.org/abs/2309.13620) |

**State of the art:** Combines robustness with reversibility; addresses rounding error (ignored by existing methods) via gradient approximation function (GAF); published in Engineering Applications of AI.

**Production readiness:** Research
arXiv September 2023; published in Engineering Applications of Artificial Intelligence (Elsevier) 2024; code available.

**Implementations:**
- [PRIS](https://github.com/yanghangAI/PRIS) ⭐ 46 — PyTorch, official implementation

**Security status:** Caution — Focuses on robustness against distortions (Gaussian noise, lossy compression); steganalysis resistance not primary goal

**Community acceptance:** Emerging — Journal-published; outperforms state-of-the-art in robustness benchmarks

---

### Multi-User Multi-Key Image Steganography

**Goal:** Image steganography with key isolation for multi-user scenarios.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Multi-User Multi-Key** | 2026 | Unified network with key isolation | Selective hidden content reveal [[1]](https://arxiv.org/abs/2603.23005) |

**State of the art:** Enables different authorized users to extract different hidden contents from the same stego image; extends PUSNet paradigm.

**Production readiness:** Research
arXiv March 2026; 6-page conference paper; academic prototype only.

**Security status:** Secure — Key isolation ensures different users cannot access each other's hidden content

**Community acceptance:** Emerging — Novel multi-user access control for steganography; addresses real-world multi-party use cases

---

### StegaPos

**Goal:** Prevent unwanted image crops and replacements by embedding imperceptible positional signatures.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaPos** | 2021 | Learned encoder/decoder CNN | Anti-tampering watermarking [[1]](https://arxiv.org/abs/2104.12290) |

**State of the art:** Embeds distinct positional signatures in every local image region. Detects crops, splices, and inpainting by identifying inconsistencies in hidden positional signatures.

**Production readiness:** Research
arXiv April 2021 (updated December 2022); academic prototype only.

**Security status:** Caution — Designed for tamper detection, not covert communication; positional signatures detectable if steganalysis is applied

**Community acceptance:** Emerging — Useful for image authentication and provenance verification

---

### Rethinking Security of Diffusion-based Generative Steganography

**Goal:** Analyze and improve security of diffusion model-based generative image steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Rethinking Security of DM-GIS** | 2026 | Diffusion model analysis | Security enhancement [[1]](https://arxiv.org/abs/2602.10219) |

**State of the art:** Identifies vulnerabilities in existing DM-GIS methods and proposes improvements.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Caution — Known vulnerabilities identified

**Community acceptance:** Emerging

---

### Intelligent Carrier Allocation

**Goal:** Cross-modal reasoning framework for adaptive multimodal steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Intelligent Carrier Allocation** | 2025 | Cross-modal reasoning | Adaptive carrier selection [[1]](https://arxiv.org/abs/2511.09552) |

**State of the art:** Uses AI reasoning to select optimal carrier media for different message types.

**Production readiness:** Experimental

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Secure Audio Embedding in Images

**Goal:** Hide audio files in images using nature-inspired optimization.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Secure Audio Embedding** | 2025 | LSB with Harris Hawks Optimization | Audio-in-image [[1]](https://arxiv.org/abs/2512.08299) |

**State of the art:** Uses HHO algorithm to optimize LSB embedding for audio in images.

**Production readiness:** Experimental

**Implementations:** Academic prototypes only

**Security status:** Caution — LSB-based methods are detectable

**Community acceptance:** Niche

---

### Deep Data Hiding for ICAO-Compliant Face Images

**Goal:** Embed data in ICAO-compliant face images while maintaining biometric standards.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **ICAO Data Hiding** | 2025 | Watermarking/steganography for biometric images | ICAO compliant [[1]](https://arxiv.org/abs/2508.19324) |

**State of the art:** Enables persistent verification without compromising ICAO compliance.

**Production readiness:** Experimental

**Implementations:** Academic prototypes only

**Security status:** Caution — Must maintain biometric standards

**Community acceptance:** Emerging

---

### Defending against Stegomalware

**Goal:** Protect deep neural networks from steganographic malware embedding.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Stegomalware Defense** | 2025 | Permutation symmetry defense | Corrupts embedded payloads [[1]](https://arxiv.org/abs/2509.20399) |

**State of the art:** Uses layer permutation to corrupt stegomalware payloads without accuracy loss.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure — Effective against state-of-the-art methods

**Community acceptance:** Emerging

---

### On the Possible Detectability of Image-in-Image Steganography

**Goal:** Analyze detectability of embedding one image inside another.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Image-in-Image Detectability** | 2026 | ICA-based detection | High embedding rate [[1]](https://arxiv.org/abs/2603.11876) |

**State of the art:** Shows embedding is identifiable by independent component analysis.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Caution — Easily detectable

**Community acceptance:** Emerging

---

### Robust Provably Secure Image Steganography via Latent Iterative Optimization

**Goal:** Robust and provably secure image steganography using latent-space iterative optimization.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Latent Iterative Optimization** | 2026 | Latent-space iterative refinement | Robust message extraction [[1]](https://arxiv.org/abs/2603.09348) |

**State of the art:** Improves message extraction accuracy through iterative latent refinement.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure — Provably secure framework

**Community acceptance:** Emerging
