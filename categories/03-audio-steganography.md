# Audio Steganography

<!-- TOC -->
## Contents (4 subcategories)

**[Time Domain](#time-domain)**
- [LPC](#lpc-linear-predictive-coding)
- [LSB Audio](#lsb-audio)
- [Parity Coding](#parity-coding)
- [Echo Hiding](#echo-hiding)
- [Phase Coding](#phase-coding)
- [Tone Insertion](#tone-insertion)
- [Adaptive Phase Coding](#adaptive-phase-coding)

**[Frequency Domain](#frequency-domain)**
- [Spread Spectrum](#spread-spectrum)
- [MDCT-domain](#mdct-domain)
- [Wavelet Packet](#wavelet-packet)
- [CELP](#celp)
- [Patchwork](#patchwork)

**[Compressed Formats](#compressed-formats)**
- [MP3Stego](#mp3stego)
- [AAC-stego](#aac-stego)
- [Opus-stego](#opus-stego)

**[Neural Network Methods](#neural-network-methods)**
- [DeepSound](#deepsound)
- [WavMark](#wavmark)
- [AudioSeal](#audioseal)
- [PRoADS](#proads)

**[Spectrogram Methods](#spectrogram-methods)**
- [Spectrogram Steganography](#spectrogram-steganography)
<!-- /TOC -->

## Time Domain

---

### LPC (Linear Predictive Coding)

**Goal:** Embed in linear prediction coefficients of speech.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LPC** | 2004 | Modify prediction coefficients | Speech-specific [[1]](https://link.springer.com/article/10.1007/s11042-016-3257-x) |

**State of the art:** Good for voice steganography.

**Production readiness:** Experimental
Usable in low-bitrate speech codecs; no production deployments known.

**Security status:** Caution
Modification of LPC residuals can be detected via statistical analysis.

**Community acceptance:** Niche
Applied mainly to narrow-band VoIP research; limited peer adoption.

---

### LSB Audio

**Goal:** Hide data in least significant bits of audio samples.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LSB Audio** | 1998 | Replace LSB of 16-bit PCM | 1 bit/sample → 44.1 kbps mono |

**State of the art:** Simple but easily detected.

**Production readiness:** Deprecated

**Implementations:**
- [steghide](https://github.com/StephanHofmannmich/steghide) ⭐ 1.8k

**Security status:** Broken — Easily detected

**Community acceptance:** Niche

---

### Parity Coding

**Goal:** Use parity of sample groups to encode bits.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Parity Coding** | 2003 | Parity of group of samples | 1 bit/group [[1]](https://ieeexplore.ieee.org/document/1220996/) |

**State of the art:** More robust than raw LSB.

**Production readiness:** Mature
Simple, well-understood method; implemented in several audio stego tools.

**Security status:** Caution
Detectable via statistical analysis of sample parity distributions.

**Community acceptance:** Niche
Covered in most audio steganography surveys; rarely used in isolation today.

---

### Echo Hiding

**Goal:** Embed data using audio echoes with different delays.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Echo Hiding** | 1996 | Add echoes with different delays | ~16 bps [[1]](https://dl.acm.org/doi/10.1147/sj.353.0313) |

**State of the art:** Takes advantage of auditory masking.

**Production readiness:** Mature
Classic technique; implementations exist in several audio watermarking toolkits.

**Security status:** Caution
Detectable via cepstrum analysis; improved variants (arXiv:2102.06774) address weaknesses.

**Community acceptance:** Widely trusted
Foundational method cited in every major audio steganography survey.

---

### Phase Coding

**Goal:** Replace initial phase of audio segments.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Phase Coding** | 1996 | Replace initial phase of segment | ~30 bps [[1]](https://dl.acm.org/doi/10.1147/sj.353.0313) |

**State of the art:** Human ear is insensitive to absolute phase changes; improved variant: arXiv:2408.13277.

**Production readiness:** Mature
Well-studied; multiple open-source implementations.

**Security status:** Caution
Phase relationships between segments can be exploited for detection.

**Community acceptance:** Widely trusted
Bender et al. 1996 is one of the most-cited papers in audio steganography.

---

### Tone Insertion

**Goal:** Insert tones in inaudible frequency regions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Tone Insertion** | 2003 | Inaudible frequency tones | Simple [[1]](https://ieeexplore.ieee.org/document/1220996/) [[2]](https://www.researchgate.net/publication/228610880_Audio_steganography_for_covert_data_transmission_by_imperceptible_tone_insertion) |

**State of the art:** Simple but limited capacity; improved capacity methods proposed in IEEE 2025 (doi:10.1109/11071041).

**Production readiness:** Mature
Straightforward to implement; used in early covert VoIP research.

**Security status:** Caution
Tones visible in spectrogram; detectable by frequency analysis.

**Community acceptance:** Niche
Covered in surveys; superseded by more robust methods for most applications.

---

### Adaptive Phase Coding

**Goal:** Adaptive phase modification based on audio content.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Adaptive Phase Coding** | 2019 | Content-aware multi-level phase | Improved quality [[1]](https://ieeexplore.ieee.org/document/8830467/) [[2]](https://arxiv.org/abs/2408.13277) |

**State of the art:** Better than standard phase coding; AMPC (2019) achieves 33 Kbps at 35 dB SNR.

**Production readiness:** Experimental
Research implementations exist; not in production deployments.

**Security status:** Caution
More resistant to detection than basic phase coding but still vulnerable to phase-correlation analysis.

**Community acceptance:** Emerging
Active research area; improved variants published through 2024.

---

## Frequency Domain

---

### Spread Spectrum

**Goal:** Spread message across wide frequency band.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Spread Spectrum** | 1997 | Message spread via PN sequence into perceptually significant components | Robust [[1]](https://ieeexplore.ieee.org/document/650120/) |

**State of the art:** Robust to filtering and compression; Cox et al. 1997 is the canonical formulation.

**Production readiness:** Mature
Well-studied; used in broadcast watermarking and some DRM systems.

**Security status:** Secure
Key-based PN sequence makes blind removal difficult without knowledge of the key.

**Community acceptance:** Widely trusted
Cox et al. 1997 has over 6000 citations; foundational to digital watermarking field.

---

### MDCT-domain

**Goal:** Embed in MDCT coefficients (used in AAC, AC-3).

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MDCT-domain** | 2021 | Embed in small-value MDCT coefficients via genetic algorithm | Compressed audio [[1]](https://ieeexplore.ieee.org/document/9327974/) |

**State of the art:** Works with compressed audio formats; genetic-algorithm variant improves imperceptibility.

**Production readiness:** Mature
Multiple published implementations for AAC and MP3 formats.

**Security status:** Caution
MDCT coefficient statistics are exploitable; dedicated steganalysis exists.

**Community acceptance:** Widely trusted
Standard embedding domain for compressed audio steganography research.

---

### Wavelet Packet

**Goal:** Modify wavelet coefficients of audio.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Wavelet Packet** | 2005 | Modify wavelet coefficients adaptively | Multi-resolution [[1]](https://ieeexplore.ieee.org/document/1505680/) [[2]](https://ieeexplore.ieee.org/document/4798397/) |

**State of the art:** Good for audio-specific embedding; adaptive wavelet packet variant (2009) selects subbands based on data history.

**Production readiness:** Mature
Several IEEE-published implementations; integrates well with audio codecs.

**Security status:** Caution
Wavelet coefficient statistics can be analyzed; dedicated steganalysis methods exist.

**Community acceptance:** Niche
Used in academic research; less popular than MDCT-domain methods for compressed audio.

---

### CELP

**Goal:** Embed in Code Excited Linear Prediction coefficients.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CELP** | 2006 | CELP codebook index substitution | Low bitrate audio [[1]](https://ieeexplore.ieee.org/document/7925046/) [[2]](https://www.researchgate.net/publication/224312993_High_rate_data_hiding_in_ACELP_speech_codecs) |

**State of the art:** Works with CELP-based codecs (AMR, iLBC, G.729); ACELP variant achieves up to 2 kbit/s covert rate.

**Production readiness:** Experimental
Prototype implementations for iLBC and AMR; no known production deployments.

**Security status:** Caution
Codebook index statistics deviate from natural speech distributions under embedding.

**Community acceptance:** Niche
Relevant for VoIP covert channels; limited adoption outside speech codec research.

---

### Patchwork

**Goal:** Embed data by modifying pseudo-random pairs of samples.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Patchwork** | 1996 | Pseudo-random sample pairs; raise one, lower other | Watermarking [[1]](https://dl.acm.org/doi/10.1147/sj.353.0313) |

**State of the art:** Robust to some attacks; wavelet-domain variant improves robustness.

**Production readiness:** Mature
Described in Bender et al. 1996; implemented in various watermarking toolkits.

**Security status:** Caution
Statistical analysis of pseudo-random pair differences can detect embedding.

**Community acceptance:** Widely trusted
One of the original techniques from the landmark Bender et al. 1996 paper.

---

## Compressed Formats

---

### MP3Stego

**Goal:** Embed data during MP3 encoding process.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MP3Stego** | 1998 | Embed during MP3 encoding | Format-specific |

**State of the art:** Classic method for MP3 files.

**Production readiness:** Mature

**Implementations:**
- [mp3stego](http://www.petitcolas.net/steganography/mp3stego/) — Official

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### AAC-stego

**Goal:** Embed in AAC audio streams.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **AAC-stego** | 2010 | Huffman codebook escape sequences or section-based hiding | Modern audio [[1]](https://ieeexplore.ieee.org/document/5671308/) [[2]](https://scialert.net/fulltext/?doi=itj.2011.1983.1988) |

**State of the art:** Works with modern audio codecs; adaptive distortion-minimization variant (2020) improves security.

**Production readiness:** Experimental
Several published implementations; not in production audio software.

**Security status:** Caution
Calibrated Markov model steganalysis (IEEE 2016) can detect Huffman-based embedding.

**Community acceptance:** Emerging
Active research since 2010; growing number of papers and steganalysis countermeasures.

---

### Opus-stego

**Goal:** Embed in Opus audio codec.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Opus-stego** | 2015 | SILK/CELT switching points or codec mode bits | Voice over IP [[1]](https://arxiv.org/abs/1203.4374) |

**State of the art:** Designed for VoIP applications; survey of VoIP steganography covers Opus vectors (arXiv:1203.4374).

**Production readiness:** Experimental
Prototype-level only; Opus codec described at arXiv:1602.04845.

**Security status:** Caution
Mode-switching patterns may be statistically anomalous under high embedding rates.

**Community acceptance:** Emerging
Growing interest as Opus replaces older VoIP codecs; limited dedicated literature.

---

## Neural Network Methods

---

### DeepSound

**Goal:** Autoencoder-based audio steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DeepSound** | 2019 | Autoencoder on spectrograms | Deep learning |

**State of the art:** First major DL audio steganography.

**Production readiness:** Experimental

**Implementations:**
- [DeepSound](https://github.com/ElsebyCoder/DeepSound) ⭐ 312

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### WavMark

**Goal:** Invertible network for robust audio watermarking.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **WavMark** | 2023 | Invertible network | Robust to re-encoding [[1]](https://arxiv.org/abs/2308.12770) |

**State of the art:** Microsoft research; encodes 32 bits/second with 0.48% BER across 10 attack types; 2800% BER improvement over prior SOTA.

**Production readiness:** Experimental
Open-source Python/PyTorch implementation available.

**Implementations:**
- [wavmark/wavmark](https://github.com/wavmark/wavmark) ⭐ 310 — Python/PyTorch, official implementation

**Security status:** Secure — Robust to re-encoding
Withstands Gaussian noise, MP3 compression, low-pass filtering, and speed variation.

**Community acceptance:** Widely trusted
Widely cited; demo on HuggingFace Spaces; adopted as baseline in subsequent audio watermarking work.

---

### AudioSeal

**Goal:** Detection and localization watermark for AI-generated audio.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **AudioSeal** | 2024 | Generator/detector with localization loss | Meta research [[1]](https://arxiv.org/abs/2401.17264) |

**State of the art:** First audio watermark with sample-level localization; detection up to 2 orders of magnitude faster than prior methods; presented at ICML 2024.

**Production readiness:** Experimental
Official open-source implementation from Meta; actively maintained.

**Implementations:**
- [facebookresearch/audioseal](https://github.com/facebookresearch/audioseal) ⭐ 717 — Python, official Meta implementation

**Security status:** Secure
Robust to real-world audio manipulations; perceptual loss based on auditory masking ensures imperceptibility.

**Community acceptance:** Widely trusted
Published at ICML 2024; adopted in AI-generated audio provenance research.

---

### PRoADS

**Goal:** Provably secure audio steganography using diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PRoADS** | 2026 | Audio diffusion + orthogonal matrix projection + backward Euler inversion | Provably secure [[1]](https://arxiv.org/abs/2603.10314) |

**State of the art:** Accepted at ICASSP 2026; embeds via initial noise of diffusion model using orthogonal matrix projection; addresses diffusion inversion reconstruction errors via latent optimization.

**Production readiness:** Research
Academic prototype; accepted conference paper but no public implementation yet.

**Security status:** Secure — Theoretical guarantees
Provable security derived from orthogonal matrix projection into diffusion model noise space.

**Community acceptance:** Emerging — Very recent
ICASSP 2026 acceptance signals peer validation; too new for broad adoption.

---

### Spectrogram Steganography

**Goal:** Hide data in audio spectrograms.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Spectrogram Steganography** | 2010 | Map image pixels to frequency/time via inverse STFT | Visual+audio [[1]](https://link.springer.com/article/10.1186/1687-4722-2012-25) |

**State of the art:** Novel approach using spectrogram representation; popularized by Aphex Twin's hidden face in "Windowlicker" (1999); documented in comparative survey (Springer 2012).

**Production readiness:** Experimental
Simple tools available (e.g. online SSTV encoders); not used in security-critical applications.

**Security status:** Caution
Visible in spectrogram view with any audio analysis tool; provides obscurity not true security.

**Community acceptance:** Emerging
Well known in CTF and art communities; limited formal academic treatment.

---

### FGAS

**Goal:** Fixed decoder network-based audio steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **FGAS** | 2025 | Fixed decoder + adversarial perturbation generation | High fidelity audio [[1]](https://arxiv.org/abs/2505.22266) |

**State of the art:** Leverages AIGC high-fidelity audio as cover; fixed decoder ensures consistent extraction; adversarial perturbation generation maximizes imperceptibility.

**Production readiness:** Experimental
arXiv preprint (2025); no public implementation released yet.

**Security status:** Secure
Adversarial perturbation design makes statistical detection harder than conventional DL stego.

**Community acceptance:** Emerging
Very recent arXiv submission; peer review pending.

---

### SteganoSNN

**Goal:** SNN-based audio-in-image steganography with encryption.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SteganoSNN** | 2025 | Spiking neural network | Edge-AI, IoT efficient [[1]](https://arxiv.org/abs/2511.06573) |

**State of the art:** Neuromorphic approach for energy-efficient steganography; achieves >35 dB PSNR and SSIM >0.97; outperforms SteganoGAN in computational efficiency.

**Production readiness:** Experimental
arXiv preprint (November 2025); targeted at Edge-AI and IoT hardware.

**Security status:** Secure
Combines steganography with encryption; SNN-based approach adds hardware-level security for IoT deployments.

**Community acceptance:** Emerging — Novel approach
First SNN-based audio steganography paper; too recent for broad peer adoption.

---

### HHO-Optimized Audio Steganography

**Goal:** Hide audio in images using Harris Hawks Optimization for pixel selection.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **HHO Audio Stego** | 2025 | Nature-inspired optimization over LSB pixel selection | LSB enhancement [[1]](https://arxiv.org/abs/2512.08299) |

**State of the art:** Uses Harris Hawks Optimization to find optimal LSB pixel positions for hiding audio in images; improves imperceptibility over naive LSB.

**Production readiness:** Experimental
arXiv preprint (December 2025); no public implementation released.

**Security status:** Caution
Underlying LSB technique remains detectable; optimization only improves pixel choice, not fundamental detectability.

**Community acceptance:** Emerging
Novel combination of metaheuristic optimization and audio-in-image steganography; limited peer adoption so far.
