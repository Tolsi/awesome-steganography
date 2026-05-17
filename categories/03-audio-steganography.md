# Audio Steganography

<!-- TOC -->
## Contents (41 algorithms)

**[Time Domain](#time-domain)**
- [LPC (Linear Predictive Coding)](#lpc-linear-predictive-coding)
- [LSB Audio](#lsb-audio)
- [Parity Coding](#parity-coding)
- [Echo Hiding](#echo-hiding)
- [Phase Coding](#phase-coding)
- [Tone Insertion](#tone-insertion)
- [Adaptive Phase Coding](#adaptive-phase-coding)
- [Audio Steganography: LSB Technique Using a Pyramid Structure and Range of Bytes](#audio-steganography-lsb-technique-using-a-pyramid-structure-and-range-of-bytes)

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
- [Audio Steganography (GAN-based)](#audio-steganography-gan-based)
- [Deep Audio Steganography](#deep-audio-steganography)
- [WavMark](#wavmark)
- [AudioSeal](#audioseal)
- [PRoADS](#proads)
- [FGAS: Fixed Decoder Network-Based Audio Steganography](#fgas-fixed-decoder-network-based-audio-steganography)
- [AAG-Stega: Automatic Audio Generation-based Steganography](#aag-stega-automatic-audio-generation-based-steganography)
- [Hide and Speak: Deep Neural Networks for Speech Steganography](#hide-and-speak-deep-neural-networks-for-speech-steganography)
- [Spectrogram Steganography](#spectrogram-steganography)
- [FGAS](#fgas)
- [SteganoSNN](#steganosnn)
- [HHO-Optimized Audio Steganography](#hho-optimized-audio-steganography)
- [Image Steganography For Securing Intellicise Wireless Networks: "Invisible Encryption" Against Eavesdroppers](#image-steganography-for-securing-intellicise-wireless-networks-invisible-encryption-against-eavesdroppers)
- [V2A-Mark: Versatile Deep Visual-Audio Watermarking for Manipulation Localization and Copyright Protection](#v2a-mark-versatile-deep-visual-audio-watermarking-for-manipulation-localization-and-copyright-protection)
- [Secure Semantic Communication for Image Transmission in the Presence of Eavesdroppers](#secure-semantic-communication-for-image-transmission-in-the-presence-of-eavesdroppers)
- [NUANCE: Near Ultrasound Attack On Networked Communication Environments](#nuance-near-ultrasound-attack-on-networked-communication-environments)
- [Source Mixing and Separation Robust Audio Steganography](#source-mixing-and-separation-robust-audio-steganography)
- [PixInWav: Residual Steganography for Hiding Pixels in Audio](#pixinwav-residual-steganography-for-hiding-pixels-in-audio)
- [Multi-Stage Residual Hiding for Image-into-Audio Steganography](#multi-stage-residual-hiding-for-image-into-audio-steganography)
- [Utilizing Pileup Effect and Intermittently Nonlinear Filtering in Synthesis of Covert and Hard-to-Intercept Communication Links](#utilizing-pileup-effect-and-intermittently-nonlinear-filtering-in-synthesis-of-covert-and-hard-to-intercept-communication-links)
- [Heard More Than Heard: An Audio Steganography Method Based on GAN](#heard-more-than-heard-an-audio-steganography-method-based-on-gan)
- [Developing a Video Steganography Toolkit](#developing-a-video-steganography-toolkit)
- [A Two Intermediates Audio Steganography Technique](#a-two-intermediates-audio-steganography-technique)
- [Design And Implementation Of Multilevel Access Control In Medical Image Transmission Using Symmetric Polynomial Based Audio Steganography](#design-and-implementation-of-multilevel-access-control-in-medical-image-transmission-using-symmetric-polynomial-based-audio-steganography)

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

### Audio Steganography: LSB Technique Using a Pyramid Structure and Range of Bytes

**Goal:** Improve LSB audio steganography to balance payload capacity, robustness, and imperceptibility.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Audio Steganography: LSB Technique Using a Pyramid Structure** | 2015 | cs.MM | Satish Bhalshankar, Avinash K. Gulve [[1]](https://arxiv.org/abs/1509.02630) |

**State of the art:** Uses pyramid structure and range of bytes to improve payload capacity while maintaining robustness and imperceptibility. Divides cover audio bytes into ranges to hide secret bits appropriately. Published in IJACR.

**Production readiness:** Experimental
Published research; implementation details in paper.

**Security status:** Broken
LSB methods are easily detected by steganalysis.

**Community acceptance:** Niche
Published in 2015; superseded by modern methods.

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
- [ElsebyCoder/DeepSound](https://github.com/ElsebyCoder/DeepSound) ⭐ 312 — Python, autoencoder on spectrograms

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### Audio Steganography (GAN-based)

**Goal:** Audio steganography using Generative Adversarial Networks.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Audio Stego GAN** | 2018 | GAN for cover generation | Learning to Generate Steganographic Cover [[1]](https://github.com/Chenlang2018/Audio-Steganography-using-GAN) |

**State of the art:** First GAN-based approach for generating steganographic audio covers.

**Production readiness:** Research

**Implementations:**
- [Chenlang2018/Audio-Steganography-using-GAN](https://github.com/Chenlang2018/Audio-Steganography-using-GAN) ⭐ 16 — Python, official implementation

**Security status:** Caution

**Community acceptance:** Emerging

---

### Deep Audio Steganography

**Goal:** End-to-end deep neural network for audio steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Deep Audio Stego** | 2020 | DNN encoder-decoder | Training pipeline on TIMIT dataset [[1]](https://github.com/ppartarr/audioSteganography) |

**State of the art:** Full train/predict pipeline with DNN for audio steganography.

**Production readiness:** Research

**Implementations:**
- [ppartarr/audioSteganography](https://github.com/ppartarr/audioSteganography) ⭐ 4 — Python, train/predict pipeline

**Security status:** Caution

**Community acceptance:** Emerging

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

### FGAS: Fixed Decoder Network-Based Audio Steganography

**Goal:** Fixed decoder audio steganography with adversarial perturbation generation.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **FGAS** | 2025 | Fixed decoder + A2PG | SOTA anti-steganalysis, 10dB PSNR gain [[1]](https://arxiv.org/abs/2505.22266) |

**State of the art:** Uses fixed decoder with adversarial perturbations. Achieves >10dB PSNR improvement over SOTA, strong anti-steganalysis performance.

**Production readiness:** Research

**Implementations:**
- No public GitHub repository yet

**Security status:** Secure — Improved anti-steganalysis

**Community acceptance:** Emerging — ICASSP 2025

---

### AAG-Stega: Automatic Audio Generation-based Steganography

**Goal:** Generate audio covers automatically from secret bits.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **AAG-Stega** | 2018 | Auto-generation | First generation-based audio stego [[1]](https://arxiv.org/abs/1809.03463) |

**State of the art:** First work to generate audio covers automatically rather than modify existing audio.

**Production readiness:** Research

**Implementations:**
- No public GitHub repository

**Security status:** Caution

**Community acceptance:** Emerging — AAAI 2019

---

### Hide and Speak: Deep Neural Networks for Speech Steganography

**Goal:** End-to-end speech steganography using neural networks.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Hide and Speak** | 2019 | STFT-based encoder-decoder | Neural speech stego [[1]](https://arxiv.org/abs/1902.03083) |

**State of the art:** Uses STFT/ISTFT as differentiable layers; first DL speech steganography.

**Production readiness:** Research

**Implementations:**
- No public GitHub repository

**Security status:** Caution

**Community acceptance:** Emerging

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

### Image Steganography For Securing Intellicise Wireless Networks: "Invisible Encryption" Against Eavesdroppers

**Goal:** Apply image steganography to secure semantic communication in intelligent wireless networks against eavesdroppers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography For Securing Intellicise Wireless Networ** | 2026 | eess.SP | Rui Meng et al. [[1]](https://arxiv.org/abs/2505.04467) |

**State of the art:** First comprehensive exploration of image steganography integration in semantic communication. Covers JSCC-based steganographic models, training strategies, and coverless approaches for "invisible encryption" in SemCom.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Novel application; security analysis pending.

**Community acceptance:** Emerging
First work in this domain; limited peer review.

---

### V2A-Mark: Versatile Deep Visual-Audio Watermarking for Manipulation Localization and Copyright Protection

**Goal:** Address limitations of current video tampering forensics—poor generalizability, singular function, and single modality focus—with multimodal watermarking.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **V2A-Mark: Versatile Deep Visual-Audio Watermarking for Manip** | 2024 | cs.CV | Xuanyu Zhang et al. [[1]](https://arxiv.org/abs/2404.16824) |

**State of the art:** Combines video-into-video steganography with deep robust watermarking for visual-audio localization and copyright protection. Uses temporal alignment, fusion module, and cross-modal extraction. Accepted at ACM MM 2024.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Accepted at ACM MM 2024; significant for AIGC video era.

---

### Secure Semantic Communication for Image Transmission in the Presence of Eavesdroppers

**Goal:** Protect image transmission in semantic communication from eavesdropping using steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secure Semantic Communication for Image Transmission in the ** | 2024 | eess.SP, cs.IT | Shunpu Tang et al. [[1]](https://arxiv.org/abs/2404.12170) |

**State of the art:** Proposes INN-based signal steganography to embed private image signals into host image signals. Legitimate receiver reconstructs private image; eavesdropper only sees host image. Maintains comparable reconstruction quality.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Significant for 6G secure communications.

---

### NUANCE: Near Ultrasound Attack On Networked Communication Environments

**Goal:** Investigate inaudible attack vectors on voice assistants using near-ultrasound and explore steganography potential.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **NUANCE: Near Ultrasound Attack On Networked Communication En** | 2023 | cs.CR, cs.LG, cs.SD | Forrest McKee, David Noever [[1]](https://arxiv.org/abs/2305.10358) |

**State of the art:** Uses Single Upper Sideband Amplitude Modulation (SUSBAM) to generate inaudible commands (16-22 kHz). 100% success with unprocessed commands, 58% with processed. Mapped to MITRE ATT&CK framework. Demonstrates demodulation for alerting and audio steganography potential.

**Production readiness:** Research
Academic prototype; no public implementation.

**Security status:** Caution
Attack vector demonstrated; defense methods proposed but not widely deployed.

**Community acceptance:** Emerging
Raises awareness of voice assistant attack surface.

---

### Source Mixing and Separation Robust Audio Steganography

**Goal:** Embed information into individual sound sources in audio mixtures that survives source separation attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Source Mixing and Separation Robust Audio Steganography** | 2022 | cs.SD, cs.CR, eess.AS | Naoya Takahashi, Mayank Kumar Singh, Yuki Mitsufuji [[1]](https://arxiv.org/abs/2110.05054) |

**State of the art:** First method robust against mixing and source separation. Uses time-domain model with curriculum learning to decode from separated sources. Successfully embeds info into multiple sources simultaneously. Accepted at ICASSP 2022.

**Production readiness:** Experimental
Academic research; implementation details in paper.

**Security status:** Caution
Robust against source separation but not evaluated against steganalysis.

**Community acceptance:** Emerging
Accepted at ICASSP 2022; novel approach to audio steganography.

---

### PixInWav: Residual Steganography for Hiding Pixels in Audio

**Goal:** Hide images in audio signals using residual architecture on STDCT spectrograms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **PixInWav: Residual Steganography for Hiding Pixels in Audio** | 2021 | cs.MM, cs.SD, eess.AS | Margarita Geleta et al. [[1]](https://arxiv.org/abs/2106.09814) |

**State of the art:** Novel residual architecture on spectrograms allows independent encoding of hidden image from host audio. Can encode images offline and later hide as residual. Tested over air from speaker to microphone. Presented at CVPR 2021 WiCV Workshop.

**Production readiness:** Experimental
Academic research; implementation details in paper.

**Security status:** Caution
Novel approach; security analysis limited.

**Community acceptance:** Emerging
Presented at CVPR 2021 WiCV Workshop; notable multimodal steganography.

---

### Multi-Stage Residual Hiding for Image-into-Audio Steganography

**Goal:** Hide image content into audio carriers while preserving perceptual fidelity of the cover audio.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Multi-Stage Residual Hiding for Image-into-Audio Steganograp** | 2021 | cs.CV, cs.CR | Wenxue Cui et al. [[1]](https://arxiv.org/abs/2101.01872) |

**State of the art:** Uses two multi-stage networks: encoder embeds residual errors into audio subsequences, decoder extracts them. Multi-stage design provides flexible payload control. Modifications unnoticeable to human listeners. Published at ICASSP 2020.

**Production readiness:** Experimental
Academic research; implementation in paper.

**Security status:** Caution
Novel approach; limited security analysis.

**Community acceptance:** Emerging
Published at ICASSP 2020; cross-modal steganography.

---

### Utilizing Pileup Effect and Intermittently Nonlinear Filtering in Synthesis of Covert and Hard-to-Intercept Communication Links

**Goal:** Physical-layer steganography where low-power stego messages are statistically indistinguishable from Gaussian channel noise.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Utilizing Pileup Effect and Intermittently Nonlinear Filteri** | 2020 | eess.SP | Alexei V. Nikitin, Ruslan L. Davidchack [[1]](https://arxiv.org/abs/2004.13610) |

**State of the art:** Uses channel noise as cover signal. Cover and stego signals have matching spectral/temporal properties. Linear and nonlinear filtering separates cover, payload, and jamming signals even when all have identical characteristics.

**Production readiness:** Research
Theoretical framework; no public implementation.

**Security status:** Secure
Theoretically secure—stego indistinguishable from thermal noise.

**Community acceptance:** Niche
Physical-layer steganography; specialized audience.

---

### Heard More Than Heard: An Audio Steganography Method Based on GAN

**Goal:** Use adversarial training to automatically generate audio steganography instead of handcrafting methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Heard More Than Heard: An Audio Steganography Method Based o** | 2019 | cs.MM, cs.CR, eess.AS | Dengpan Ye, Shunzhi Jiang, Jiaqin Huang [[1]](https://arxiv.org/abs/1907.04986) |

**State of the art:** Uses three neural networks: encoder embeds secret message, decoder extracts it, discriminator determines if carrier contains secret. All trained simultaneously. Produces high-fidelity steganographic audio containing secret audio. Verified robustness and security.

**Production readiness:** Experimental
Academic research; implementation in paper.

**Security status:** Caution
GAN-based approach; security not independently verified.

**Community acceptance:** Emerging
Early GAN-based audio steganography work.

---

### Developing a Video Steganography Toolkit

**Goal:** Review current state of video steganography and develop a practical video steganography system.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Developing a Video Steganography Toolkit** | 2014 | cs.MM | James Ridgway, Mike Stannett [[1]](https://arxiv.org/abs/1409.4883) |

**State of the art:** Reviews video steganography field and describes key issues in developing practical systems. Includes supporting video demonstration. Provides foundation for video steganography toolkit development.

**Production readiness:** Research
Survey paper; toolkit concept only.

**Security status:** Caution
Survey paper; no specific security guarantees.

**Community acceptance:** Niche
Early video steganography survey (2014).

---

### A Two Intermediates Audio Steganography Technique

**Goal:** Hide data in audio using two intermediates: random audio samples and a generated English text encoding their locations.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Two Intermediates Audio Steganography Technique** | 2012 | cs.CR | Youssef Bassil [[1]](https://arxiv.org/abs/1212.2207) |

**State of the art:** Uses randomized algorithm to select audio samples, then generates grammatically correct English text (via CFG) to encode sample locations. Two intermediates make detection and recovery difficult. Published in Journal of Emerging Trends in CIS.

**Production readiness:** Research
Paper proposes technique; no implementation available.

**Security status:** Broken
Novel but untested; likely detectable by modern steganalysis.

**Community acceptance:** Niche
Older technique (2012); limited adoption.

---

### Design And Implementation Of Multilevel Access Control In Medical Image Transmission Using Symmetric Polynomial Based Audio Steganography

**Goal:** Hide medical images in audio with hierarchical access control using symmetric polynomial key derivation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Design And Implementation Of Multilevel Access Control In Me** | 2010 | cs.MM | J. Nafeesa Begum, K. Kumar, V. Sumathy [[1]](https://arxiv.org/abs/1004.1682) |

**State of the art:** Uses symmetric polynomial for hierarchical key derivation. Higher-level users can derive keys for lower levels. Uses two bit positions dictated by key, not conventional LSB. Published in IJCSIT (IEEE format). Claims dynamic, scalable system.

**Production readiness:** Research
Published in 2010; no current implementations known.

**Security status:** Deprecated
Outdated approach; no modern security analysis.

**Community acceptance:** Niche
Older medical imaging steganography work.

---

## CTF Audio Tools

---

### WavSteg

**Goal:** Hide arbitrary data in WAV audio files using LSB substitution and extract it with matching parameters.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **WavSteg** | 2018 | LSB substitution in WAV samples | Python3 CLI; embed and extract mode [[1]](https://github.com/ragibson/Steganography#WavSteg) |

**State of the art:** Simple, widely used for WAV-based CTF challenges. Supports multi-bit LSB embedding.

**Production readiness:** Mature
Stable Python3 tool; standard for WAV stego in CTF.

**Implementations:**
- [ragibson/Steganography](https://github.com/ragibson/Steganography) ⭐ 648 — Python3

**Security status:** Caution
LSB changes detectable via statistical analysis of sample LSBs.

**Community acceptance:** Widely trusted
Standard CTF audio stego tool.

---

### Sonic Visualizer

**Goal:** Visualize audio files as spectrograms and waveforms to reveal hidden images or patterns encoded in audio.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Sonic Visualizer** | 2006 | Spectrogram/waveform visualization | Reveals hidden images in audio spectrogram [[1]](https://www.sonicvisualiser.org/) |

**State of the art:** Primary tool for discovering spectrogram steganography in CTF. Hidden images in audio are trivially revealed by switching to spectrogram view.

**Production readiness:** Production
Actively maintained; cross-platform GUI application.

**Security status:** Caution
Only reveals visually encoded patterns; encrypted audio stego invisible to spectrogram analysis.

**Community acceptance:** Standard
Universal CTF tool for audio stego analysis.

---

## Software Tools

---

### AudioStego

**Goal:** Hide and retrieve data files in MP3 and WAV audio using LSB manipulation via the `hideme` CLI.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **AudioStego (hideme)** | 2016 | LSB in MP3/WAV audio samples | Simple hide/reveal CLI; included in stego-toolkit [[1]](https://github.com/DominicBreuker/stego-toolkit) |

**State of the art:** Bundled in the stego-toolkit Docker container. Commands: `hideme cover.mp3 secret.txt` and `hideme stego.mp3 -f`.

**Production readiness:** Mature
Stable; actively used in CTF environments via Docker container.

**Security status:** Caution
LSB in audio detectable via statistical analysis of sample LSBs.

**Community acceptance:** Niche
Known primarily through stego-toolkit Docker container.

---

### spectrology

**Goal:** Encode an image into the spectrogram of a WAV audio file so the image becomes visible in a spectrogram viewer.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **spectrology** | 2015 | Image-to-spectrogram audio encoding | Hidden image revealed by Sonic Visualizer or Audacity [[1]](https://github.com/solusipse/spectrology) |

**State of the art:** Primary tool for creating CTF audio stego challenges where an image is hidden as a spectrogram. Decode side uses any spectrogram viewer.

**Production readiness:** Mature
Stable Python script; widely used to create CTF challenges.

**Implementations:**
- [solusipse/spectrology](https://github.com/solusipse/spectrology) ⭐ 277 — Python

**Security status:** Caution
Trivially revealed by any spectrogram viewer (Sonic Visualizer, Audacity).

**Community acceptance:** Standard
Standard CTF audio stego creation tool; spectrogram challenges are a CTF staple.

---

### audio-steganography-algorithms

**Goal:** MATLAB/C reference library implementing classical audio steganography algorithms: LSB, phase coding, echo hiding, spread spectrum, and tone insertion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **audio-steganography-algorithms** | 2018 | Multi-algorithm academic reference library | Covers 5 classical methods with unified evaluation framework [[1]](https://github.com/ktekeli/audio-steganography-algorithms) |

**State of the art:** Most comprehensive open-source reference for classical audio stego algorithms. Each method implemented with capacity and SNR metrics. Useful for benchmarking and academic study.

**Production readiness:** Research
Academic library; no production CLI; MATLAB required.

**Implementations:**
- [ktekeli/audio-steganography-algorithms](https://github.com/ktekeli/audio-steganography-algorithms) ⭐ 287 — MATLAB/C

**Security status:** Caution
Classical methods (LSB, phase, echo) are all detectable by modern steganalysis; see [Classical Methods](#time-domain).

**Community acceptance:** Niche
Primary academic reference for comparing classical audio stego methods.

---

