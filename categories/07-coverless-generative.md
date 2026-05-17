# Coverless / Generative Steganography

<!-- TOC -->
## Contents (17 algorithms)

**[Hash-based](#hash-based)**
- [INR Stego](#inr-stego)

**[GAN-based](#gan-based)**
- [StyleGAN Stego](#stylegan-stego)

**[Diffusion-based](#diffusion-based)**
- [CRoSS](#cross)
- [MIDAS](#midas)
- [Dual Model Replacement:invisible Multi-target Backdoor Attack based on Federal Learning](#dual-model-replacementinvisible-multi-target-backdoor-attack-based-on-federal-learning)

**[3D/Neural Graphics](#3dneural-graphics)**
- [StegoNGP](#stegongp)
- [3DGS Steganography](#3dgs-steganography)
- [SecureGS](#securegs)
- [GS-Hider](#gs-hider)
- [SemSteDiff](#semstediff)
- [DDIM-Driven Coverless Steganography](#ddim-driven-coverless-steganography)
- [INR-Based Generative Steganography](#inr-based-generative-steganography)
- [Splats in Splats++](#splats-in-splats)
- [All That Glitters Is Not Gold: Key-Secured 3D Secrets within 3D Gaussian Splatting](#all-that-glitters-is-not-gold-key-secured-3d-secrets-within-3d-gaussian-splatting)
- [Splats in Splats: Robust and Effective 3D Steganography towards Gaussian Splatting](#splats-in-splats-robust-and-effective-3d-steganography-towards-gaussian-splatting)
- [Noise-NeRF: Hide Information in Neural Radiance Fields using Trainable Noise](#noise-nerf-hide-information-in-neural-radiance-fields-using-trainable-noise)
- [Steganography for Neural Radiance Fields by Backdooring](#steganography-for-neural-radiance-fields-by-backdooring)

<!-- /TOC -->

## Hash-based

---

### INR Stego

**Goal:** Steganography using implicit neural representations (INR) as the stego medium.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **INR Stego (StegaINR)** | 2023 | Implicit neural representations | First INR steganography [[1]](https://arxiv.org/abs/2312.04743) |

**State of the art:** Uses neural implicit representations; capacity higher than traditional methods. See also [INR-Based Generative Steganography](#inr-based-generative-steganography).

**Production readiness:** Research
Academic prototype only.

**Security status:** Secure — No explicit cover image modifications

**Community acceptance:** Emerging — Novel paradigm introduced 2023

---

## GAN-based

---

### StyleGAN Stego

**Goal:** Generate cover images using GAN latent space to encode secret bits.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **StyleGAN Stego** | 2021 | Latent vector encodes bits | Coverless, no pixel modification [[1]](https://arxiv.org/abs/1802.03528) |

**State of the art:** Computationally expensive but secure. Superseded by diffusion-based methods. See [CRoSS](#cross) and [MIDAS](#midas).

**Production readiness:** Research
Academic prototype; computationally expensive for deployment.

**Security status:** Secure — No stego artifacts in pixel domain

**Community acceptance:** Emerging — Computationally expensive

---

## Diffusion-based

---

### CRoSS

**Goal:** Diffusion-based steganography with message controlling seed/path.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CRoSS** | 2023 | Diffusion model | NeurIPS 2023 |

**State of the art:** State-of-art in generative steganography.

**Production readiness:** Experimental

**Implementations:**
- [CRoSS](https://github.com/) — Official

**Security status:** Secure — Natural cover distribution

**Community acceptance:** Widely trusted — Growing rapidly

---

### MIDAS

**Goal:** Training-free diffusion coverless steganography with multi-image hiding and user access control.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MIDAS** | 2024 | Latent-level fusion in diffusion model | User-specific access control [[1]](https://arxiv.org/abs/2407.10459) |

**State of the art:** Training-free approach using DiffStega-style diffusion inversion; supports selective multi-user reveal.

**Production readiness:** Research
No public implementation available.

**Security status:** Secure — Coverless; no pixel-level stego signal

**Community acceptance:** Emerging — Very recent

---

### Dual Model Replacement:invisible Multi-target Backdoor Attack based on Federal Learning

**Goal:** Design backdoor attack method for federated learning using steganography to encode attack information as invisible noise.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Dual Model Replacement:invisible Multi-target Backdoor Attac** | 2024 | cs.LG | Rong Wang et al. [[1]](https://arxiv.org/abs/2404.13946) |

**State of the art:** Proposes TrojanGan steganography model with encoder-decoder structure for invisible backdoor triggers. Uses dual model replacement for improved attack success rate in federated learning. Achieves high concealment and multi-target attack capability.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Security research; discusses vulnerabilities and detection risks.

**Community acceptance:** Emerging
Novel application of steganography to backdoor attacks; significant for security research.

---

## 3D/Neural Graphics

---

### StegoNGP

**Goal:** 3D steganography using Instant-NGP hash encoding as a key-controlled scene switcher.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **StegoNGP** | 2026 | Neural Graphics Primitives hash encoding | Key-controlled scene [[1]](https://arxiv.org/abs/2603.00949) |

**State of the art:** Parameter-free approach; leverages NGP's hash grid as steganographic medium.

**Production readiness:** Research
Preprint; no public code available.

**Security status:** Secure — Stego scene indistinguishable without correct key

**Community acceptance:** Emerging — Novel 3D paradigm (2026)

---

### 3DGS Steganography

**Goal:** Embed data in 3D Gaussian Splatting representation using spherical harmonics.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **3DGS Steganography (Splats in Splats)** | 2024 | Gaussian SH coefficient hiding | 3D/4D content [[1]](https://arxiv.org/abs/2405.15118) |

**State of the art:** Cutting-edge 3D steganography; see also [GS-Hider](#gs-hider), [SecureGS](#securegs), [Splats in Splats++](#splats-in-splats).

**Production readiness:** Research
NeurIPS 2024 work; research code only.

**Security status:** Secure — Hidden scenes inaccessible without decoder

**Community acceptance:** Emerging — Active research area (2024–2026)

---

### SecureGS

**Goal:** Boosting security and fidelity of 3D Gaussian Splatting steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SecureGS** | 2025 | 3DGS attribute protection via hybrid decoupled Gaussian encryption | Anchor-point design [[1]](https://arxiv.org/abs/2503.06118) |

**State of the art:** Improves both security and visual quality over [GS-Hider](#gs-hider) and prior 3DGS steganography.

**Production readiness:** Research
Preprint March 2025; no public code found.

**Security status:** Secure — Hidden Gaussian positions encrypted; geometry not exposed

**Community acceptance:** Emerging

---

### GS-Hider

**Goal:** Hide messages into 3D Gaussian Splatting using coupled secured feature attributes.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **GS-Hider** | 2024 | Coupled secured feature replacing SH coefficients; dual-decoder | NeurIPS 2024 [[1]](https://arxiv.org/abs/2405.15118) |

**State of the art:** First dedicated 3DGS steganography framework; protects 3D asset privacy with multimodal message hiding.

**Production readiness:** Research
NeurIPS 2024; project page at xuanyuzhang21.github.io/project/gshider/.

**Security status:** Secure — Hidden messages require private decoder; no visible artifacts

**Community acceptance:** Emerging — Foundational NeurIPS 2024 paper

---

### SemSteDiff

**Goal:** Coverless semantic steganography communication using diffusion models without a pre-selected cover image.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SemSteDiff** | 2025 | Diffusion-based semantic extraction | No pre-selected cover [[1]](https://arxiv.org/abs/2509.04803) |

**State of the art:** Uses semantic extraction to confuse intelligent eavesdroppers; no cover image required.

**Production readiness:** Research
Preprint September 2025; no public implementation.

**Security status:** Secure — Coverless; defeats semantic analysis attacks

**Community acceptance:** Emerging

---

### DDIM-Driven Coverless Steganography

**Goal:** Generate stego images using DDIM inversion without modification, with real key support.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DDIM-Driven** | 2024 | DDIM inversion for coverless generation | Real key (not pseudo-key) [[1]](https://arxiv.org/abs/2411.06486) |

**State of the art:** Addresses pseudo-key weakness of prior generation-based methods; uses deterministic DDIM for real key support.

**Production readiness:** Research
Preprint November 2024; no public code.

**Security status:** Secure — Coverless; stego object generated rather than modified

**Community acceptance:** Emerging

---

### INR-Based Generative Steganography

**Goal:** Generate stego-media through secret message-driven generation using implicit neural representations (point cloud).

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **INR-Based GS** | 2024 | Point cloud implicit neural representation | High hiding capacity [[1]](https://arxiv.org/abs/2410.11673) |

**State of the art:** Higher hiding capacity than traditional methods; uses point cloud as generative medium.

**Production readiness:** Research
Preprint October 2024; no public implementation.

**Security status:** Secure — Generation-based; no detectable embedding signal

**Community acceptance:** Emerging

---

### Splats in Splats++

**Goal:** Robust and generalizable 3D Gaussian Splatting steganography framework.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Splats in Splats++** | 2026 | 3DGS hash encoding | Pipeline-agnostic [[1]](https://arxiv.org/abs/2604.15862) |

**State of the art:** Unified framework embedding 3D/4D content in native 3DGS representation.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging

### All That Glitters Is Not Gold: Key-Secured 3D Secrets within 3D Gaussian Splatting

**Goal:** Hide 3D secrets within 3D Gaussian Splatting covers while ensuring imperceptibility and high-fidelity reconstruction with key-secured access control.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **All That Glitters Is Not Gold: Key-Secured 3D Secrets within** | 2025 | cs.GR, cs.CR, cs.CV | Yan Ren, Shilin Lu, Adams Wai-Kin Kong [[1]](https://arxiv.org/abs/2503.07191) |

**State of the art:** Proposes KeySS framework with key-controllable mechanism for multi-secret hiding. Introduces 3D-Sinkhorn distance for evaluating steganographic imperceptibility. Achieves state-of-the-art in both cover and secret reconstruction.

**Production readiness:** Research
Public implementation available at https://github.com/RY-Paper/KeySS

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Very recent; peer review status unknown.

---

### Splats in Splats: Robust and Effective 3D Steganography towards Gaussian Splatting

**Goal:** Embed 3D content in 3DGS without modifying attributes, addressing usability challenges in 3DGS copyright protection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Splats in Splats: Robust and Effective 3D Steganography towa** | 2025 | cs.CV, eess.IV | Yijia Guo et al. [[1]](https://arxiv.org/abs/2412.03121) |

**State of the art:** First 3DGS steganography framework embedding 3D content in 3DGS itself. Uses importance-graded SH coefficient encryption. Achieves 5.31% higher scene fidelity and 3x faster rendering. Accepted at AAAI 2026.

**Production readiness:** Research
Very recent; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Accepted at AAAI 2026; significant for 3D asset protection.

---

### Noise-NeRF: Hide Information in Neural Radiance Fields using Trainable Noise

**Goal:** Address information security issues in NeRF by hiding data within Neural Radiance Fields using trainable noise.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Noise-NeRF: Hide Information in Neural Radiance Fields using** | 2024 | cs.CV | Qinglong Huang et al. [[1]](https://arxiv.org/abs/2401.01216) |

**State of the art:** Proposes Noise-NeRF with Adaptive Pixel Selection and Pixel Perturbation strategies. Addresses low steganography quality and model weight damage issues. Achieves state-of-the-art in steganography quality and rendering quality.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
First systematic work on NeRF steganography; significant for 3D reconstruction security.

---

### Steganography for Neural Radiance Fields by Backdooring

**Goal:** Hide information in Neural Radiance Fields using backdoor approach for covert communications.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography for Neural Radiance Fields by Backdooring** | 2023 | cs.CR | Weina Dong et al. [[1]](https://arxiv.org/abs/2309.10503) |

**State of the art:** Uses viewpoint as key to generate secret images in NeRF. Trains message extractor using overfitting for one-to-one mapping. Achieves 100% accuracy in message extraction with high capacity and fast performance.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
First NeRF backdoor steganography; significant for implicit representation security.

---
