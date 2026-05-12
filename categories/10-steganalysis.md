# Steganalysis

<!-- TOC -->
## Contents (3 subcategories)

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
<!-- /TOC -->

## Classical Methods

---

### Visual Attack

**Goal:** Detect steganography by visual inspection.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Visual Attack** | 1998 | Visual inspection | Manual |

**State of the art:** Basic but still useful for initial analysis.

**Production readiness:** Production

**Community acceptance:** Standard

---

### Structural Attack

**Goal:** Detect changes in file structure.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Structural Attack** | 1999 | File format analysis | Effective for LSB |

**State of the art:** Effective against simple LSB methods.

**Production readiness:** Production

**Community acceptance:** Standard

---

### Chi-square

**Goal:** Detect LSB steganography via statistical analysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chi-square** | 1999 | Pair-of-values analysis | Westfeld & Pfitzmann |

**State of the art:** Classic detection method.

**Production readiness:** Production

**Implementations:**
- Various steganalysis tools

**Community acceptance:** Standard — Foundational method

---

### RS-analysis

**Goal:** Detect LSB via Regular/Singular group analysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **RS-analysis** | 2001 | Group flipping analysis | Fridrich |

**State of the art:** Very effective against LSB.

**Production readiness:** Production

**Community acceptance:** Standard

---

### Weighted Stego

**Goal:** Estimate embedding rate.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Weighted Stego** | 2005 | Weighted prediction | Fridrich |

**State of the art:** Estimates embedding amount.

**Production readiness:** Production

**Community acceptance:** Standard

---

### SPAM

**Goal:** Co-occurrence features for detection.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SPAM** | 2007 | 686D co-occurrence features | Pevny et al. |

**State of the art:** Rich model predecessor.

**Production readiness:** Production

**Community acceptance:** Standard

---

### SRM

**Goal:** Comprehensive rich model features.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SRM** | 2011 | 34,671D features | Fridrich |

**State of the art:** Standard for years.

**Production readiness:** Production

**Community acceptance:** Standard — De facto standard

---

### DCTR

**Goal:** DCT residual features for JPEG.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DCTR** | 2015 | DCT residuals | JPEG-specific |

**State of the art:** Modern JPEG detection.

**Production readiness:** Production

**Community acceptance:** Standard

---

## Deep Learning

---

### XuNet

**Goal:** First CNN steganalyser.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **XuNet** | 2016 | CNN | First DL steganalyser |

**State of the art:** Foundational deep learning steganalysis.

**Production readiness:** Production

**Implementations:**
- [xunet](https://github.com/umich-vrl/gsi) ⭐ 156

**Community acceptance:** Standard

---

### YeNet

**Goal:** CNN with SRM-like first layer.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **YeNet** | 2017 | CNN + SRM filters | Enhanced first layer |

**State of the art:** Improved XuNet.

**Production readiness:** Production

**Community acceptance:** Standard

---

### SRNet

**Goal:** End-to-end CNN steganalysis.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SRNet** | 2019 | End-to-end CNN | State-of-art 2019-2022 |

**State of the art:** State-of-art before transformers.

**Production readiness:** Production

**Implementations:**
- [SRNet](https://github.com/Chris铎/SRNet) ⭐ 234

**Community acceptance:** Standard

---

### ZhuNet

**Goal:** CNN with covariance pooling.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **ZhuNet** | 2020 | CNN + covariance pooling | Modern approach |

**State of the art:** Modern CNN steganalysis.

**Production readiness:** Production

**Community acceptance:** Standard

---

## Network Steganalysis

---

### Tor Traffic Detection

**Goal:** Detect Tor traffic via ML.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Tor Detection** | 2015 | CNN on packet sizes | Traffic classification |

**State of the art:** Effective against Tor.

**Production readiness:** Production

**Community acceptance:** Standard

---

### DNS Tunnel Detection

**Goal:** Detect DNS tunneling.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DNS Tunnel Detection** | 2010 | Query patterns | Statistical analysis |

**State of the art:** Effective against DNS tunnels.

**Production readiness:** Production

**Community acceptance:** Standard
