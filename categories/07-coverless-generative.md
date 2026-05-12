# Coverless / Generative Steganography

<!-- TOC -->
## Contents (6 algorithms)

**[Hash-based](#hash-based)**
- [Coverless Image](#coverless-image)
- [INR Stego](#inr-stego)

**[GAN-based](#gan-based)**
- [StyleGAN Stego](#stylegan-stego)

**[Diffusion-based](#diffusion-based)**
- [CRoSS](#cross)
- [MIDAS](#midas)

**[3D/Neural Graphics](#3dneural-graphics)**
- [StegoNGP](#stegongp)
- [3DGS Steganography](#3dgs-steganography)
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
