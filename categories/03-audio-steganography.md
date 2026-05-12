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
| **LPC** | 2004 | Modify prediction coefficients | Speech-specific |

**State of the art:** Good for voice steganography.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

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
| **Parity Coding** | 2000 | Parity of group of samples | 1 bit/group |

**State of the art:** More robust than raw LSB.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Niche

---

### Echo Hiding

**Goal:** Embed data using audio echoes with different delays.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Echo Hiding** | 1996 | Add echoes with different delays | ~16 bps |

**State of the art:** Takes advantage of auditory masking.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### Phase Coding

**Goal:** Replace initial phase of audio segments.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Phase Coding** | 1996 | Replace initial phase of segment | ~30 bps |

**State of the art:** Human ear is insensitive to phase changes.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### Tone Insertion

**Goal:** Insert tones in inaudible frequency regions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Tone Insertion** | 1999 | Inaudible frequency tones | Simple |

**State of the art:** Simple but limited capacity.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Niche

---

### Adaptive Phase Coding

**Goal:** Adaptive phase modification based on audio content.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Adaptive Phase Coding** | 2008 | Content-aware phase | Improved quality |

**State of the art:** Better than standard phase coding.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

## Frequency Domain

---

### Spread Spectrum

**Goal:** Spread message across wide frequency band.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Spread Spectrum** | 2003 | Message spread via PN sequence | Robust |

**State of the art:** Robust to filtering and compression.

**Production readiness:** Mature

**Security status:** Secure

**Community acceptance:** Widely trusted

---

### MDCT-domain

**Goal:** Embed in MDCT coefficients (used in AAC, AC-3).

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MDCT-domain** | 2005 | Embed in MDCT coefficients | Compressed audio |

**State of the art:** Works with compressed audio formats.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### Wavelet Packet

**Goal:** Modify wavelet coefficients of audio.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Wavelet Packet** | 2005 | Modify wavelet coefficients | Multi-resolution |

**State of the art:** Good for audio-specific embedding.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Niche

---

### CELP

**Goal:** Embed in Code Excited Linear Prediction coefficients.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CELP** | 2006 | CELP codebook | Low bitrate audio |

**State of the art:** Works with CELP-based codecs.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### Patchwork

**Goal:** Embed data by modifying pseudo-random pairs of samples.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Patchwork** | 1996 | Random sample pairs | Watermarking |

**State of the art:** Robust to some attacks.

**Production readiness:** Mature

**Security status:** Caution

**Community acceptance:** Widely trusted

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
| **AAC-stego** | 2005 | Huffman codebook or SBR | Modern audio |

**State of the art:** Works with modern audio codecs.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

### Opus-stego

**Goal:** Embed in Opus audio codec.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Opus-stego** | 2015 | SILK/CELT switching points | Voice over IP |

**State of the art:** Designed for VoIP applications.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

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
| **WavMark** | 2023 | Invertible network | Robust to re-encoding |

**State of the art:** Microsoft research, robust to re-encoding.

**Production readiness:** Experimental

**Security status:** Secure — Robust to re-encoding

**Community acceptance:** Widely trusted

---

### AudioSeal

**Goal:** Detection and localization watermark for AI-generated audio.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **AudioSeal** | 2024 | Detection + localization | Meta research |

**State of the art:** State-of-art for audio watermarking.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Widely trusted

---

### PRoADS

**Goal:** Provably secure audio steganography using diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PRoADS** | 2025 | Audio diffusion + orthogonal matrix | Provably secure |

**State of the art:** Latest research in audio steganography.

**Production readiness:** Research

**Security status:** Secure — Theoretical guarantees

**Community acceptance:** Emerging — Very recent

---

### Spectrogram Steganography

**Goal:** Hide data in audio spectrograms.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Spectrogram Steganography** | 2010 | Image in spectrogram | Visual+audio |

**State of the art:** Novel approach using spectrogram representation.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging
