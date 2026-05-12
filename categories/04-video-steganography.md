# Video Steganography

<!-- TOC -->
## Contents (9 algorithms)

**[Frame-based Methods](#frame-based-methods)**
- [Frame LSB/DCT](#frame-lsbdct)
- [Motion Vector](#motion-vector)

**[Codec-specific Methods](#codec-specific-methods)**
- [Intra Prediction Mode](#intra-prediction-mode)
- [QP Modulation](#qp-modulation)
- [CABAC](#cabac)
- [HEVC PU Partition](#hevc-pu-partition)
- [H.265/HEVC CU Block Steganography](#h265hevc-cu-block-steganography)
- [SemCovert](#semcovert-semantic-video-steganography)
- [Optimizing Region of Interest Selection](#optimizing-region-of-interest-selection)
<!-- /TOC -->

## Frame-based Methods

---

### Frame LSB/DCT

**Goal:** Hide data in individual video frames.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Frame LSB/DCT** | 2000 | Treat each frame as image | Low robustness |

**State of the art:** Simple but destroyed by video re-encoding.

**Production readiness:** Deprecated

**Security status:** Broken — Destroyed by compression

**Community acceptance:** Niche

---

### Motion Vector

**Goal:** Embed data in motion vectors of video codec.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Motion Vector** | 2005 | MPEG/H.264/H.265 MV | Medium robustness |

**State of the art:** More robust than frame-based.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

## Codec-specific Methods

---

### Intra Prediction Mode

**Goal:** Embed data in HEVC intra prediction directions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Intra Prediction Mode** | 2015 | HEVC 33→35 directions | High robustness |

**State of the art:** High robustness to re-encoding.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### QP Modulation

**Goal:** Modulate quantization parameters to encode data.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **QP Modulation** | 2010 | Quantization parameter | High robustness |

**State of the art:** Good resistance to compression.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### CABAC

**Goal:** Modify CABAC entropy coding in HEVC.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CABAC** | 2015 | Entropy coding order | High robustness |

**State of the art:** Very high robustness.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Niche

---

### HEVC PU Partition

**Goal:** Use PU partition patterns to encode data.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HEVC PU Partition** | 2017 | Partition pattern selection | High robustness |

**State of the art:** Modern approach with good robustness.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Niche

---

### H.265/HEVC CU Block Steganography

**Goal:** Embed secret data in Coding Unit block structures and split decisions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CU Block Steganography** | 2026 | CU split flags, depth selection | High compression robustness |

**State of the art:** Exploits H.265/HEVC quadtree structure by modifying CU split decisions; maintains video quality while achieving high embedding capacity.

**Production readiness:** Research

**Implementations:** Academic prototype

**Security status:** Emerging

**Community acceptance:** Niche

---

### SemCovert (Semantic Video Steganography)

**Goal:** Embed secret information within semantic-level video features for covert communication.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SemCovert** | 2025 | Semantic-level hiding via deep learning | Robust to semantic transformations |

**State of the art:** Novel approach leveraging semantic communication for covert transmission.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Optimizing Region of Interest Selection

**Goal:** Optimize ROI selection for effective embedding in video steganography using genetic algorithms.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **ROI Optimization** | 2025 | Genetic algorithm optimization | H.265/HEVC [[1]](https://arxiv.org/abs/2508.13710) |

**State of the art:** Uses GA to find optimal regions for embedding without visual degradation.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Niche
