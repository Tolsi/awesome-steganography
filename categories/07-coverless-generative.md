# Coverless / Generative Steganography

<!-- TOC -->
## Contents (7 algorithms)

**[Hash-based](#hash-based)**
- [Coverless Image](#coverless-image)
- [INR Stego](#inr-stego)

**[GAN-based](#gan-based)**
- [StyleGAN Stego](#stylegan-stego)

**[Diffusion-based](#diffusion-based)**
- [CRoSS](#cross)
- [MIDAS](#midas)
- [Training-Free Coverless Multi-Image Steganography](#training-free-coverless-multi-image-steganography)

**[3D/Neural Graphics](#3dneural-graphics)**
- [StegoNGP](#stegongp)
- [3DGS Steganography](#3dgs-steganography)
- [Splats in Splats++](#splats-in-splats)
<!-- /TOC -->

## Hash-based

---

### Coverless Image

**Goal:** Find pre-existing image matching message hash without modification.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Coverless Image** | 2015 | Hash dictionary lookup | Zhou et al. [[1]](https://link.springer.com/chapter/10.1007/978-3-319-27051-7_11) |

**State of the art:** Requires large shared image database.

**Production readiness:** Research
Academic prototype; no production-grade deployment known.

**Implementations:**
- Various academic implementations

**Security status:** Secure — No modified pixels to detect

**Community acceptance:** Emerging — Requires infrastructure

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

### Training-Free Coverless Multi-Image Steganography

**Goal:** Access-controlled hidden content revelation for multiple users without model training.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Coverless Multi-Image** | 2026 | Training-free multi-image hiding | Access control [[1]](https://arxiv.org/abs/2603.09390) |

**State of the art:** First training-free CIS with robust access control for multiple authorized users.

**Production readiness:** Research
Preprint only; no implementation released.

**Security status:** Secure — Coverless; no pixel-level embedding

**Community acceptance:** Emerging — Very recent (2026)

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
