# Video Steganography

<!-- TOC -->
## Contents (15 algorithms)

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

**[Recent arXiv Papers (2024–2026)](#recent-arxiv-papers-20242026)**
- [From Covert Hiding to Visual Editing: Robust Generative Vide...](#from-covert-hiding-to-visual-editing-robust-generative-video-steganography)
- [Large-capacity and Flexible Video Steganography via Invertib...](#large-capacity-and-flexible-video-steganography-via-invertible-neural-network)
- [Investigation on Principles for Cost Assignment in Motion Ve...](#investigation-on-principles-for-cost-assignment-in-motion-vector-based-video-steganography)
- [Convolutional Video Steganography with Temporal Residual Mod...](#convolutional-video-steganography-with-temporal-residual-modeling)

**[Video Software Tools](#video-software-tools)**
- [LVDO](#lvdo)
- [videostego](#videostego)
- [LD-RoViS](#ld-rovised)
<!-- /TOC -->

## Frame-based Methods

---

### Frame LSB/DCT

**Goal:** Hide data in individual video frames.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Frame LSB/DCT** | 1999 | Treat each frame as image, apply LSB/DCT embedding | Low robustness [[1]](https://ieeexplore.ieee.org/document/7361355/) |

**State of the art:** Simple but destroyed by video re-encoding; Chae & Manjunath (1999) is the foundational reference for frame-based video data hiding.

**Production readiness:** Deprecated
Superseded by codec-domain methods; destroyed by any re-encoding.

**Security status:** Broken — Destroyed by compression
Any video transcoding or re-encoding removes the hidden data entirely.

**Community acceptance:** Niche
Historical baseline only; no longer used in practice.

---

### Motion Vector

**Goal:** Embed data in motion vectors of video codec.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Motion Vector** | 2001 | Modify MV components with minimum distortion | Medium robustness [[1]](https://ieeexplore.ieee.org/document/963053/) [[2]](https://onlinelibrary.wiley.com/doi/10.1155/2022/2946812) |

**State of the art:** More robust than frame-based; Zhang et al. 2001 is foundational; local optimality-based methods (2021+) improve security against steganalysis.

**Production readiness:** Experimental
Multiple published implementations for H.264/AVC and H.265/HEVC.

**Security status:** Caution
Motion vector reversion-based steganalysis (arXiv:2310.07121) can detect MV modifications.

**Community acceptance:** Emerging
Active research area; dozens of papers on MV steganography and steganalysis published annually.

---

## Codec-specific Methods

---

### Intra Prediction Mode

**Goal:** Embed data in HEVC intra prediction directions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Intra Prediction Mode** | 2015 | Modify HEVC 35 intra prediction directions | High robustness [[1]](https://ieeexplore.ieee.org/document/10433022/) [[2]](https://www.mdpi.com/1424-8220/20/18/5242) |

**State of the art:** High robustness to re-encoding; cover-selection variant (MDPI Sensors 2020) improves security; multi-sized prediction block variant (Springer 2019) increases capacity.

**Production readiness:** Experimental
Multiple published H.264/H.265 implementations; no production deployments.

**Security status:** Secure
Survives video re-encoding; IPM-shift steganalysis (IEEE 2024) is the main detection threat.

**Community acceptance:** Emerging
Growing body of work since 2015; dedicated steganalysis methods now exist.

---

### QP Modulation

**Goal:** Modulate quantization parameters to encode data.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **QP Modulation** | 2010 | Encode bits by selecting QP values at macroblock/CU level | High robustness [[1]](https://link.springer.com/article/10.1007/s00530-021-00763-z) |

**State of the art:** Good resistance to compression; QP choices survive re-encoding in same codec; surveyed in comprehensive video steganography review (Springer Multimedia Systems 2021).

**Production readiness:** Experimental
Described in research prototypes; no known production implementations.

**Security status:** Secure
QP-level decisions persist through re-encoding in same codec and bitrate settings.

**Community acceptance:** Emerging
Covered in video steganography surveys; less studied than MV or IPM-based methods.

---

### CABAC

**Goal:** Modify CABAC entropy coding in HEVC.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CABAC** | 2015 | Exploit constant-bitrate info bits in MVD codewords | High robustness, no bitrate increase [[1]](https://www.researchgate.net/publication/281717146_A_CABAC_based_HEVCc_video_steganography_algorithm_without_bitrate_increase) |

**State of the art:** Very high robustness; no bitrate increase by exploiting constant-bitrate information bits (CBIB) in CABAC syntax; operates at entropy coding stage without RDO or full decoding.

**Production readiness:** Experimental
Research prototype published 2015; no open-source release known.

**Security status:** Secure
Bitstream-compliant embedding; no bitrate anomaly to detect; operates at the last compression stage.

**Community acceptance:** Niche
Technically elegant but narrow focus on HEVC CABAC; limited follow-on work compared to MV/IPM methods.

---

### HEVC PU Partition

**Goal:** Use PU partition patterns to encode data.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HEVC PU Partition** | 2018 | Encode bits in P-frame PU partition mode selection | High robustness [[1]](https://www.semanticscholar.org/paper/An-Information-Hiding-Algorithm-for-HEVC-Videos-on-Xie-Yang/65339ef59daa8137ce125eff265ab5318c8f658b) [[2]](https://ieeexplore.ieee.org/document/9672694/) |

**State of the art:** Modern approach with good robustness; CNN-based variant (IEEE 2022) improves anti-steganalysis performance; diamond-coded PU variant (IEEE 2021) increases capacity.

**Production readiness:** Experimental
Multiple published implementations; active research area with annual improvements.

**Security status:** Secure
PU partition decisions persist through re-encoding; combined-feature steganalysis (Springer 2020) is the main detection threat.

**Community acceptance:** Niche
Growing sub-field of HEVC steganography since 2018; dedicated steganalysis now exists.

---

### H.265/HEVC CU Block Steganography

**Goal:** Embed secret data in Coding Unit block structures and split decisions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CU Block Steganography** | 2026 | Multiple CU size + block structure distortion minimization | High compression robustness [[1]](https://arxiv.org/abs/2603.22850) |

**State of the art:** Exploits H.265/HEVC quadtree structure by modifying CU split decisions; addresses poor anti-steganalysis of prior CU-based methods via block structure distortion minimization; submitted April 2026.

**Production readiness:** Research
arXiv preprint only (March/April 2026); no implementation released.

**Security status:** Caution
Improves over prior CU-based methods against steganalysis but dedicated detectors (arXiv:2602.11547) exist for this class.

**Community acceptance:** Niche
Very recent; builds on emerging CU block structure steganography sub-field.

---

### SemCovert (Semantic Video Steganography)

**Goal:** Embed secret information within semantic-level video features for covert communication.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SemCovert** | 2025 | Deep semantic-level hiding robust to semantic-level transformations | Robust to semantic transformations [[1]](https://arxiv.org/abs/2512.22233) |

**State of the art:** Novel approach leveraging semantic communication for covert transmission; addresses privacy leakage in video semantic communication systems; robust to semantic-level abstractions that defeat traditional steganography.

**Production readiness:** Research
arXiv preprint (December 2025); academic prototype only.

**Security status:** Caution
Novel attack surface; traditional steganalysis tools not applicable but semantic-level analysis may reveal anomalies.

**Community acceptance:** Emerging
First paper to address steganography at the semantic communication layer; too recent for broad adoption.

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

## Recent arXiv Papers (2024–2026)

---

### From Covert Hiding to Visual Editing: Robust Generative Video Steganography

**Goal:** Embed secret messages within semantic features of videos during the video editing process, achieving robustness against common distortions in online social networks (OSNs).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **From Covert Hiding to Visual Editing: Robust Generative Vide** | 2023 | cs.CV | Xueying Mao et al. [[1]](https://arxiv.org/abs/2401.00652) |

**State of the art:** Proposes RoGVS network using semantic feature modification for embedding, achieving robustness against OSN distortions. Face-swapping scenario demonstrates visual editing effects. Outperforms existing methods in both robustness and capacity.

**Production readiness:** Research
Academic prototype; no public implementation available.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint under review; peer review status unknown.

---

### Large-capacity and Flexible Video Steganography via Invertible Neural Network

**Goal:** Conceal secret data in cover videos and recover them through a decoding protocol, achieving large capacity and flexibility with invertible neural networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Large-capacity and Flexible Video Steganography via Invertib** | 2023 | cs.CV, cs.CR | Chong Mou et al. [[1]](https://arxiv.org/abs/2304.12300) |

**State of the art:** Proposes LF-VSN using invertible neural networks for hiding up to 7 secret videos in 1 cover video. Features key-controllable scheme for flexible recovery and scalable strategy. Accepted at CVPR 2023.

**Production readiness:** Mature
Public implementation available at https://github.com/MC-E/LF-VSN

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Accepted at CVPR 2023; significant attention from research community.

---

### Investigation on Principles for Cost Assignment in Motion Vector-based Video Steganography

**Goal:** Investigate principles for cost assignment in motion vector domain to improve security against steganalysis attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Investigation on Principles for Cost Assignment in Motion Ve** | 2022 | cs.CR, cs.MM | Jun Li et al. [[1]](https://arxiv.org/abs/2209.01744) |

**State of the art:** Proposes three principles: local optimality, non-consistency in block group, and complexity priority. Joint distortion function resists three steganalysis features simultaneously while maintaining visual quality and coding efficiency.

**Production readiness:** Research
Academic prototype; no public implementation available.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
First systematic study of cost assignment principles in motion vector domain.

---

### Convolutional Video Steganography with Temporal Residual Modeling

**Goal:** Hide a full-sized color video within another video using convolutional neural networks with temporal residual modeling.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Convolutional Video Steganography with Temporal Residual Mod** | 2018 | cs.MM | Xinyu Weng et al. [[1]](https://arxiv.org/abs/1806.02941) |

**State of the art:** First deep learning approach to video steganography using temporal residual modeling. Proposes two-branch model for hiding inter-frame differences and secret frames. Outperforms LSB and image steganography models.

**Production readiness:** Research
Academic prototype; no public implementation available.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
First deep video steganography work; significant attention.

---

## Video Software Tools

---

### LVDO

**Goal:** Convert arbitrary files into video using DCT steganography suitable for upload to video platforms like YouTube.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **LVDO** | 2019 | DCT-based file-to-video encoding | Survives YouTube transcoding; lossless retrieval [[1]](https://github.com/m13253/lvdo) |

**State of the art:** Unique approach: use video as a storage medium via steganographic encoding that survives platform re-encoding.

**Production readiness:** Experimental
Proof-of-concept; tested on YouTube.

**Implementations:**
- [m13253/lvdo](https://github.com/m13253/lvdo) ⭐ 100 — Python/FFmpeg

**Security status:** Caution
DCT coefficients can be inspected; platform re-encoding may degrade capacity.

**Community acceptance:** Niche
Niche use case; cited in steganography reviews.

---

### RoGVSN

**Goal:** Robust Video Steganography Network with adaptive embedding based on video content.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **RoGVSN** | 2022 | Deep learning video steganography | Adaptive embedding based on video content [[1]](https://arxiv.org/abs/2201.04151) |

**State of the art:** Learning-based approach that adapts embedding strength based on video complexity.

**Production readiness:** Research

**Community acceptance:** Emerging

---

### MEC-AQIM

**Goal:** Video steganography using Motion Estimation Compensation and Adaptive QIM.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **MEC-AQIM** | 2021 | Motion compensation + AQIM | High capacity with robustness [[1]](https://ieeexplore.ieee.org/document/9144189) |

**State of the art:** Combines motion estimation with adaptive quantization index modulation.

**Production readiness:** Research

**Community acceptance:** Niche

---

### AQIM

**Goal:** Audio/Video steganography using QIM with adaptive embedding.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **AQIM** | 2019 | Adaptive QIM | Adaptive embedding based on cover characteristics [[1]](https://ieeexplore.ieee.org/document/8675189) |

**State of the art:** Classical QIM-based approach with adaptive embedding.

**Production readiness:** Research

**Community acceptance:** Niche

---

### videostego

**Goal:** Embed and extract secret data in MP4 video files using LSB substitution on frame pixel data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **videostego** | 2020 | LSB substitution in MP4 frames | Pure Python; uses OpenCV for frame manipulation [[1]](https://github.com/JavDomGom/videostego) |

**State of the art:** Simple video LSB tool for educational use and CTF. Frame-by-frame pixel manipulation.

**Production readiness:** Experimental
Educational implementation; not battle-tested.

**Implementations:**
- [JavDomGom/videostego](https://github.com/JavDomGom/videostego) ⭐ 19 — Python

**Security status:** Caution
LSB in video trivially detectable by frame-level analysis.

**Community acceptance:** Niche
Small educational project.

---

