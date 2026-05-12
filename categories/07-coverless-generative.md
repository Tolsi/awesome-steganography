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
| **Coverless Image** | 2015 | Hash dictionary lookup | Zhou et al. |

**State of the art:** Requires large shared image database.

**Production readiness:** Research

**Implementations:**
- Various academic implementations

**Security status:** Secure — No modified pixels to detect

**Community acceptance:** Emerging — Requires infrastructure

---

### INR Stego

**Goal:** Image in residual network representation steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **INR Stego** | 2022 | Implicit neural representations | Novel approach |

**State of the art:** Uses neural implicit representations.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

## GAN-based

---

### StyleGAN Stego

**Goal:** Generate cover images using GAN latent space.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **StyleGAN Stego** | 2020 | Latent vector encodes bits | GAN generation |

**State of the art:** Computationally expensive but secure.

**Production readiness:** Research

**Security status:** Secure

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

**Goal:** Training-free diffusion coverless with multi-image hiding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MIDAS** | 2025 | Latent-level fusion | User-specific access |

**State of the art:** Latest in coverless diffusion methods.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging — Very recent

---

### Training-Free Coverless Multi-Image Steganography

**Goal:** Access-controlled hidden content revelation for multiple users.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Coverless Multi-Image** | 2026 | Training-free multi-image hiding | Access control |

**State of the art:** First training-free CIS with robust access control.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

## 3D/Neural Graphics

---

### StegoNGP

**Goal:** 3D steganography using Instant-NGP.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **StegoNGP** | 2024 | Neural Graphics Primitives | Key-controlled scene |

**State of the art:** Novel 3D application.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### 3DGS Steganography

**Goal:** Embed data in 3D Gaussian Splatting representation.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **3DGS Steganography** | 2026 | Gaussian Splatting | 3D/4D content |

**State of the art:** Cutting-edge 3D steganography.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### SecureGS

**Goal:** Boosting security and fidelity of 3D Gaussian Splatting steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SecureGS** | 2025 | 3DGS attribute protection | ICLR 2025 |

**State of the art:** Improves both security and visual quality.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### GS-Hider

**Goal:** Hide messages into 3D Gaussian Splatting.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **GS-Hider** | 2024 | 3DGS point cloud protection | NeurIPS 2024 |

**State of the art:** Protects 3D asset privacy.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### SemSteDiff

**Goal:** Coverless semantic steganography communication using diffusion models.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SemSteDiff** | 2025 | Diffusion-based semantic | No pre-selected cover |

**State of the art:** Uses semantic extraction for coverless communication.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### DDIM-Driven Coverless Steganography

**Goal:** Generate stego images using DDIM inversion without modification.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DDIM-Driven** | 2024 | DDIM inversion | Real key support |

**State of the art:** Uses deterministic diffusion for coverless generation.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### INR-Based Generative Steganography

**Goal:** Generate stego-media through secret message-driven generation using INR.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **INR-Based GS** | 2024 | Implicit neural representation | High capacity |

**State of the art:** Higher hiding capacity than traditional methods.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### Splats in Splats++

**Goal:** Robust and generalizable 3D Gaussian Splatting steganography framework.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Splats in Splats++** | 2026 | 3DGS hash encoding | Pipeline-agnostic |

**State of the art:** Unified framework embedding 3D/4D content in native 3DGS representation.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging
