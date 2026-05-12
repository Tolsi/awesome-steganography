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

### Sudoku-based Steganography

**Goal:** Use Sudoku puzzle solutions as encoding key.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Sudoku** | 2009 | Sudoku grid key | High key space |

**State of the art:** Large key space provides security.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### FuzzyStego

**Goal:** Use fuzzy logic for adaptive embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **FuzzyStego** | 2010 | Fuzzy logic rules | Adaptive |

**State of the art:** Adaptive approach using fuzzy logic.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### Chaotic Map LSB

**Goal:** Use chaotic maps for secure LSB embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chaotic Map LSB** | 2008 | Chaos-based embedding | Increased security |

**State of the art:** Chaotic sequences add security layer.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### Content-Aware Steganography

**Goal:** Hide data based on semantic content of image.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Content-Aware** | 2013 | Human-assigned semantics | Secure against non-human |

**State of the art:** Uses semantic understanding.

**Production readiness:** Experimental

**Security status:** Secure — Human adversary required

**Community acceptance:** Emerging

---

### Skin Tone Adaptive

**Goal:** Embed in skin-tone regions using secret angle.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Skin Tone Adaptive** | 2009 | Face detection | Adaptive embedding |

**State of the art:** Adaptive based on image content.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

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

---

### SMILENet

**Goal:** Extra-large capacity image steganography via synergistic mosaic.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SMILENet** | 2025 | Synergistic mosaic invertible hiding | 25x image hiding |

**State of the art:** Achieves 25x image hiding capacity.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Emerging

---

### DTAMS

**Goal:** High-capacity generative steganography via dynamic multi-timestep selection.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DTAMS** | 2026 | Dynamic multi-timestep + adaptive deviation mapping | Latent diffusion |

**State of the art:** High capacity with good security at higher rates.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Approximate Gaussian Mapping

**Goal:** Generative image steganography using approximate Gaussian mapping.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Approximate Gaussian** | 2025 | ODE-based diffusion models | Deterministic synthesis |

**State of the art:** Reduces numerical inversion errors.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### PSyDUCK

**Goal:** Training-free steganography for latent diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PSyDUCK** | 2025 | Training-free latent diffusion | Message projection |

**State of the art:** No training required.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### CIF

**Goal:** Reliable message extraction in diffusion-based generative steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **CIF** | 2025 | Constrained inversion framework | High-capacity embedding |

**State of the art:** Improves extraction accuracy in lossy scenarios.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### STCL (Spatial-Temporal Curriculum Learning)

**Goal:** Improve image steganography quality through progressive multi-scale curriculum learning.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **STCL** | 2025 | Progressive multi-scale convolutional | Better convergence |

**State of the art:** Addresses poor quality and slow convergence issues.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### GIFDL (Generated Image Fluctuation Distortion Learning)

**Goal:** Enhance steganographic security through fluctuation distortion learning.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **GIFDL** | 2025 | Distortion learning framework | Enhanced security |

**State of the art:** Improves minimum distortion steganography security.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging

---

### StegaFFD (Steganography-based Face Forgery Detection)

**Goal:** Privacy-preserving face forgery detection via steganographic domain lifting.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaFFD** | 2026 | Steganography-based FFD framework | Privacy protection |

**State of the art:** Protects privacy without raising suspicion.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Arbitrary-Resolution Deep Image Steganography

**Goal:** Hide secret images with different resolutions than cover images.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Arb-Resolution DIS** | 2026 | Resolution-flexible framework | No resampling required |

**State of the art:** Solves resolution mismatch problem in deep steganography.

**Production readiness:** Research

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Adaptive Fuzzy Logic Steganography

**Goal:** Adaptive embedding using fuzzy logic for better capacity-fidelity trade-off.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Fuzzy Logic Stego** | 2026 | Fuzzy logic-based embedding | Adaptive depth |

**State of the art:** Better imperceptibility than fixed-depth LSB.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Emerging

---

### Memristive In-Memory Image Steganography

**Goal:** Hardware-based steganography using memristive circuits.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Memristive Stego** | 2026 | In-memory computing | 42-44% energy reduction |

**State of the art:** First hardware implementation of steganography.

**Production readiness:** Experimental

**Implementations:** Custom circuit prototypes

**Security status:** Emerging

**Community acceptance:** Emerging

---

### StegaVision

**Goal:** Enhance steganography using attention mechanisms for better capacity-quality balance.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaVision** | 2024 | Attention-based network | Improved capacity |

**State of the art:** Uses attention to balance image quality and embedding capacity.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Foveation Steganography

**Goal:** Improve payload capacity using foveated rendering and latent representations.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Foveation** | 2025 | Foveated rendering + latent | 100→500 bits capacity |

**State of the art:** Achieves up to 500 bits with 1 failure bit out of 2000.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### StegaINR (Steganography by Implicit Neural Representations)

**Goal:** Hide functions within functions using INR without additional extractors.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaINR** | 2023 | INR-based | No message extractor needed |

**State of the art:** Uses implicit neural representations for hiding.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### StegaINR4MIH (INR for Multi-Image Hiding)

**Goal:** Embed multiple secret images into a cover image with high quality recovery.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaINR4MIH** | 2024 | INR multi-image | High capacity |

**State of the art:** Addresses contour shadowing and color distortion issues.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### DiffStega (Training-Free Diffusion Steganography)

**Goal:** Training-free coverless image steganography using diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DiffStega** | 2024 | Diffusion-based | Training-free |

**State of the art:** First training-free diffusion generative steganography.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Stable Messenger

**Goal:** Message-concealed image generation with high message accuracy.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Stable Messenger** | 2023 | Message-driven generation | Full message recovery |

**State of the art:** Evaluates entire message accuracy, not just bit accuracy.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### DKiS (Decay weight Invertible image Steganography)

**Goal:** Private key-based image steganography with decay weight mechanism.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DKiS** | 2023 | Invertible network | Private key security |

**State of the art:** Uses decay weights for enhanced security.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging

---

### PRIS (Practical Robust Invertible Network for Image Steganography)

**Goal:** Robust and invertible network for image steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PRIS** | 2023 | Invertible network | Robust + invertible |

**State of the art:** Combines robustness with reversibility.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Multi-User Multi-Key Image Steganography

**Goal:** Image steganography with key isolation for multi-user scenarios.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Multi-User Multi-Key** | 2026 | Unified network with key isolation | Selective hidden content reveal |

**State of the art:** Enables different authorized users to extract different hidden contents from the same stego image.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure — Key-based access control

**Community acceptance:** Emerging

---

### StegaPos

**Goal:** Prevent unwanted image crops and replacements by embedding imperceptible positional signatures.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaPos** | 2021 | Learned encoder/decoder CNN | Anti-tampering watermarking |

**State of the art:** Embeds distinct positional signatures in every local image region. Detects crops, splices, and inpainting by identifying inconsistencies in hidden positional signatures.

**Production readiness:** Research

**Implementations:** Academic prototype (CVPR 2022 submission)

**Security status:** Caution — Detects tampering but not traditional steganalysis

**Community acceptance:** Emerging — Useful for image authentication

---

### Rethinking Security of Diffusion-based Generative Steganography

**Goal:** Analyze and improve security of diffusion model-based generative image steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Rethinking Security of DM-GIS** | 2026 | Diffusion model analysis | Security enhancement |

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
| **Intelligent Carrier Allocation** | 2025 | Cross-modal reasoning | Adaptive carrier selection |

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
| **Secure Audio Embedding** | 2025 | LSB with Harris Hawks Optimization | Audio-in-image |

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
| **ICAO Data Hiding** | 2025 | Watermarking/steganography for biometric images | ICAO compliant |

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
| **Stegomalware Defense** | 2025 | Permutation symmetry defense | Corrupts embedded payloads |

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
| **Image-in-Image Detectability** | 2026 | ICA-based detection | High embedding rate |

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
| **Latent Iterative Optimization** | 2026 | Latent-space iterative refinement | Robust message extraction |

**State of the art:** Improves message extraction accuracy through iterative latent refinement.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure — Provably secure framework

**Community acceptance:** Emerging
