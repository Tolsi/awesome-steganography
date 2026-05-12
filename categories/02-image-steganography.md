# Image Steganography

<!-- TOC -->
## Contents (6 subcategories)

**[Spatial Domain](#spatial-domain)**
- [LSB Replacement](#lsb-replacement)
- [LSB Matching](#lsb-matching)
- [BPCS](#bpcs)
- [PVD](#pvd)
- [EMD](#emd)
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
| **LSB Matching** | 2006 | Random +/-1 if LSB ≠ bit | 1 bpp |

**State of the art:** Better than replacement, still vulnerable to WS analysis.

**Production readiness:** Mature

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
| **PVD** | 2003 | Embed in pixel difference | 3-5 bpp |

**State of the art:** Adaptive capacity based on local contrast.

**Production readiness:** Mature

**Security status:** Caution — Vulnerable to histogram analysis of differences

**Community acceptance:** Widely trusted — Widely studied and implemented

---

### EMD

**Goal:** Encode data using multiple pixels with minimal modification.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **EMD** | 2005 | n pixels encode d-ary digit | log2(2n+1)/n bpp |

**State of the art:** Better PSNR than LSB, mathematically elegant.

**Production readiness:** Mature

**Security status:** Caution — Good perceptual quality but specific statistical signature

**Community acceptance:** Niche — Academic interest, practical use limited

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
| **HUGO** | 2010 | SPAM features (4D co-occurrence) | First model-driven |

**State of the art:** Theoretically principled — optimizes against known detection features.

**Production readiness:** Mature

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
| **HILL** | 2014 | High-pass + low-pass smoothing | Distributes changes |

**State of the art:** Competitive with S-UNIWARD.

**Production readiness:** Mature

**Security status:** Secure — Competitive with S-UNIWARD

**Community acceptance:** Widely trusted — Popular in implementations

---

### MiPOD

**Goal:** Theoretically optimal embedding under Gaussian assumptions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MiPOD** | 2016 | Multivariate Gaussian | Fisher information optimal |

**State of the art:** Strong theoretical foundation.

**Production readiness:** Experimental

**Security status:** Secure — Strong theoretical guarantees

**Community acceptance:** Emerging — Academic interest, fewer practical implementations

---

## JPEG Domain

---

### JSteg

**Goal:** Original JPEG steganography using LSB.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **JSteg** | 1993 | LSB on DCT coefficients | Historical |

**State of the art:** Deprecated due to easy detection.

**Production readiness:** Deprecated

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
| **nsF5** | 2007 | F5 without shrinkage (wet paper) | Better visual quality |

**State of the art:** Better than F5 but still detected.

**Production readiness:** Deprecated

**Security status:** Caution — Better than F5 but still detected by CCJRM

**Community acceptance:** Niche

---

### OutGuess

**Goal:** Preserve global DCT histogram during embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **OutGuess** | 2001 | Preserves global histogram | Statistical preservation |

**State of the art:** Vulnerable to local statistics attacks.

**Production readiness:** Deprecated

**Security status:** Broken — Vulnerable to local statistics attacks

**Community acceptance:** Niche

---

### J-UNIWARD

**Goal:** Best JPEG steganography against modern steganalysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **J-UNIWARD** | 2013 | UNIWARD on DCT | Best for JPEG |

**State of the art:** State-of-art for JPEG domain.

**Production readiness:** Mature

**Security status:** Secure — State-of-art for JPEG

**Community acceptance:** Widely trusted

---

### UED/UERD

**Goal:** Uniform distribution of changes across AC coefficients.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **UED/UERD** | 2014 | Uniform embedding | Competitive |

**State of the art:** Competitive with J-UNIWARD.

**Production readiness:** Mature

**Security status:** Secure — Competitive with J-UNIWARD

**Community acceptance:** Emerging

---

### QIM

**Goal:** Embed data using quantization index modulation.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **QIM** | 2003 | Quantization-based | High robustness |

**State of the art:** Robust to compression, mathematically principled.

**Production readiness:** Mature

**Implementations:**
- Various implementations in steganography toolkits

**Security status:** Caution — Detectable by trained classifiers

**Community acceptance:** Widely trusted — Foundational watermarking method

---

### MG/MVG

**Goal:** Multi-grade variable group embedding for high capacity.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MG/MVG** | 2011 | Multi-variable groups | High capacity |

**State of the art:** High capacity with good visual quality.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

## Transform Domain

---

### DWT

**Goal:** Embed in wavelet domain for robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DWT** | 2000 | High-frequency wavelet subbands | HH, HL, LH bands |

**State of the art:** Good robustness to compression.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### DFT

**Goal:** Embed in frequency domain for geometric robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DFT** | 2005 | Magnitude/phase spectrum | Robust to rotation |

**State of the art:** Robust to geometric transforms.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Niche

---

### SVD

**Goal:** Modify singular values for robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SVD** | 2001 | Modify singular values | Often combined with DWT |

**State of the art:** Very robust to noise and filtering.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Widely trusted

---

## Reversible Methods

---

### Histogram Shifting

**Goal:** Lossless data hiding by shifting histogram.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Histogram Shifting** | 2006 | Shift histogram peak | Lossless |

**State of the art:** Important for medical/legal imaging.

**Production readiness:** Mature

**Implementations:**
- Various in RDH toolkits

**Security status:** Secure — Lossless recovery

**Community acceptance:** Widely trusted — Critical for sensitive imaging

---

### Difference Expansion

**Goal:** Expand pixel differences to embed data.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Difference Expansion** | 2003 | Expand differences | Lossless |

**State of the art:** Foundational reversible method.

**Production readiness:** Mature

**Security status:** Secure

**Community acceptance:** Widely trusted

---

### Prediction Error Expansion

**Goal:** Embed in prediction error for better efficiency.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Prediction Error Expansion** | 2007 | Embed in prediction error | Better than DE |

**State of the art:** Improved efficiency over difference expansion.

**Production readiness:** Mature

**Security status:** Secure

**Community acceptance:** Widely trusted

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
| **CRoSS** | 2023 | Diffusion-based | Message controls seed/path |

**State of the art:** State-of-art in generative stego.

**Production readiness:** Experimental

**Security status:** Secure — State-of-art in generative stego

**Community acceptance:** Emerging — Growing rapidly

---

### StegNet

**Goal:** High-capacity deep learning steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegNet** | 2024 | Multi-scale CNN | 98.2% decoding, 23.57 bpp |

**State of the art:** Very high capacity.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Emerging — Research active
