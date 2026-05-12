# Awesome Steganography

> Curated collection of steganography algorithms and tools, classified by application domain

Steganography — the art of hiding the existence of a message. Unlike cryptography (which hides the content), steganography hides the very fact that communication is happening.

## The Trade-off Triangle

Every steganographic method balances three competing properties:

| Property | Description | Metrics |
|----------|-------------|---------|
| **Capacity** | How much data can be embedded | bpp (bits per pixel), bps (bits per sample), bpb (bits per byte) |
| **Imperceptibility** | How indistinguishable is the stego from cover | PSNR, SSIM, BER detection accuracy |
| **Robustness** | Does message survive processing | Compression, geometric transforms, filtering |

---

## Table of Contents

- [Text Steganography](#text-steganography)
- [Image Steganography](#image-steganography)
- [Audio Steganography](#audio-steganography)
- [Video Steganography](#video-steganography)
- [Network Steganography](#network-steganography)
- [Filesystem & OS](#filesystem--os)
- [Coverless / Generative](#coverless--generative)
- [Traffic Obfuscation](#traffic-obfuscation)
- [Steganalysis](#steganalysis)

---

## Text Steganography

Text has minimal redundancy — every character and space is meaningful. Methods either don't modify visible text or modify very selectively.

### Structural Methods

| Method | Embedding Location | Capacity | Notes |
|--------|-------------------|----------|-------|
| **Whitespace coding** | Trailing spaces (1=0, 2=1) | 1 bit/line | Hidden from humans, visible in hex |
| **Space-between-words** | Double spaces between words | 1 bit/space | Barely visible |
| **Zero-width Unicode** | U+200B (ZWSP), U+200C (ZWNJ), U+200D (ZWJ), U+FEFF | ~2-3 bit/char | Invisible but detectable via regex |
| **Variation Selectors** | U+FE00–FE0F after base character | 4 bit/selector | Invisible in normal text |
| **Homoglyphs** | Cyrillic а→a, Greek ο→o | 1 bit/char | Visually indistinguishable |
| **Line shifting** | Vertical shift 1/300 inch | 1 bit/line | Requires OCR to detect |
| **HTML attribute order** | Order inside tags | log2(N!)/tag | Invisible in rendering |

#### Security & Community

- **Security Status**: 🟡 Medium — Zero-width Unicode easily detected by regex; whitespace visible in hex editors
- **Community Acceptance**: 🟢 High — Widely used for watermarking, digital forensics, and CTF challenges

### Semantic Methods

- **Mimic Functions** (Wayner, 1992) — CFG where generated text encodes bits
- **Synonym substitution** — replace words with synonyms
- **Sentence reordering** — permute sentences to encode

### LLM-Based Methods

#### Meteor (2021)

**Description**: Arithmetic coding over LLM log-probabilities — distribution-preserving. Each bit of the message reduces the probability interval based on the LLM's token probability distribution. Produces text indistinguishable from normal LLM output.

**Why it's good**: Information-theoretically undetectable against any statistical classifier without the original prompt. The distribution of generated text matches the base LLM exactly.

**Papers**:
- Kaptchuk et al. "Meteor: Cryptographically Secure Steganography" — USENIX 2021. Introduces distribution-preserving steganography using arithmetic coding over LLM outputs.

**Implementations**:
- [meteor-stego](https://github.com/tmthrgd/meteor-stego) ⭐ 215 — Python implementation

- **Security Status**: 🟢 High — Proven information-theoretically secure against passive warden without prompt access
- **Community Acceptance**: 🟢 High — Academic community considers it breakthrough; practical implementations emerging

#### Discop (2023)

**Description**: Distribution-copy: divides token probability space into buckets, message bits select which bucket to sample from. Faster than Meteor but slightly less efficient.

**Papers**:
- Ding et al. "Discop: Practical Distribution-Preserving Steganography" — 2023. Improves efficiency while maintaining theoretical security guarantees.

- **Security Status**: 🟢 High — Slightly less efficient than Meteor but still distribution-preserving
- **Community Acceptance**: 🟡 Medium — Active research, fewer implementations

#### ChatStega (2024)

**Description**: Uses different top-p/temperature sampling parameters in ChatGPT to encode bits. Simple but effective for conversational settings.

**Papers**:
- Liu et al. "ChatStega: Language Model Based Steganographic Communication" — 2024.

- **Security Status**: 🟡 Medium — Depends on LLM sampling randomness; detectable with access to sampling seed
- **Community Acceptance**: 🟡 Medium — Growing interest in practical LLM steganography

---

## Image Steganography

Most developed domain. Images have massive redundancy — millions of pixels, human vision insensitive to small local changes.

### Spatial Domain

#### LSB Replacement

**Description**: Replace the least significant bit of each pixel channel. Simplest method — direct bit substitution.

**Why it's good**: Extremely simple to implement, maximum capacity in spatial domain. Good educational tool.

**Papers**:
- Johnson & Jajodia "Exploring Steganography" — 1998. Foundational paper on LSB techniques.

**Implementations**:
- [steghide](https://github.com/StephanHofmannmich/steghide) ⭐ 1.8k — Classic LSB tool
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287 — Java-based
- [stegano](https://github.com/BZFlag/distribution/tree/main/stegano) ⭐ 245 — Python

- **Security Status**: 🔴 Low — Detected by chi-square, RS-analysis in milliseconds
- **Community Acceptance**: 🟡 Medium — Good for learning, not for production

#### LSB Matching (±1)

**Description**: If LSB doesn't match required bit, randomly add or subtract 1 from pixel value. Reduces statistical artifacts.

**Why it's good**: Better than LSB replacement, harder to detect with chi-square attacks.

**Papers**:
- Mielikainen "LSB Matching Revisited" — 2006. Introduces ±1 matching.

- **Security Status**: 🟡 Medium — Vulnerable to weighted stego (WS) analysis
- **Community Acceptance**: 🟢 High — Standard in steganography courses

#### BPCS (Bit-Plane Complexity Segmentation)

**Description**: Replaces "complex" bit-planes (noisy areas) with secret data. Uses conjugate coding to avoid visual artifacts.

**Why it's good**: Higher capacity than LSB while maintaining visual quality. Natural complexity provides cover.

**Papers**:
- Kawaguchi & Eason "Principle and Applications of BPCS Steganography" — 1998.

**Implementations**:
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287 — Includes BPCS

- **Security Status**: 🟡 Medium — Detected by complexity analysis attacks
- **Community Acceptance**: 🟡 Medium — Popular in watermarking, less in pure stego

#### PVD (Pixel Value Differencing)

**Description**: Embeds data in difference between adjacent pixels. Edge regions (high difference) carry more bits.

**Why it's good**: Adaptive capacity — more data in textured areas, less in smooth. Good visual quality.

**Papers**:
- Wu & Tsai "A Steganographic Method for Images by Pixel-Value Differencing" — 2003.

**Implementations**:
- Various in steganography toolkits

- **Security Status**: 🟡 Medium — Vulnerable to histogram analysis of differences
- **Community Acceptance**: 🟢 High — Widely studied and implemented

#### EMD (Exploiting Modification Direction)

**Description**: Uses n pixels to encode d-ary digit; only one pixel modified per embedding unit. Better PSNR than LSB.

**Why it's good**: Minimizes visual distortion, mathematically elegant.

**Papers**:
- Zhang & Wang "Exploiting Modification Direction" — 2005.

- **Security Status**: 🟡 Medium — Good perceptual quality but specific statistical signature
- **Community Acceptance**: 🟡 Medium — Academic interest, practical use limited

#### STC (Syndrome-Trellis Codes)

**Description**: Near-optimal embedding codes that minimize distortion for any distortion function. Foundation of modern adaptive steganography.

**Why it's good**: Theoretical optimality; enables distortion-minimizing implementations of any algorithm.

**Papers**:
- Filler et al. "Minimizing Additive Distortion in Steganography using Syndrome-Trellis Codes" — 2010.

**Implementations**:
- [stc-lib](https://github.com/coin3d/stc-lib) ⭐ 89 — C++ implementation

- **Security Status**: 🟢 High — Enables best-in-class security when combined with good distortion functions
- **Community Acceptance**: 🟢 High — Industry standard for modern stego algorithms

### Adaptive Methods (Distortion-First)

All use STC encoder with different ρ(x) cost functions:

#### HUGO (2010)

**Description**: First model-driven adaptive algorithm. Uses SPAM features (4D co-occurrence) as distortion function — models what steganalysis detects.

**Why it's good**: Theoretically principled — optimizes against known detection features.

**Papers**:
- Pevny et al. "HUGO: Rich Models for Steganalysis of Digital Images" — IEEE TIFS 2010.

- **Security Status**: 🟢 High — Strong against SPAM-based detectors
- **Community Acceptance**: 🟢 High — Foundational work, frequently cited (1000+)

#### WOW (Wavelet Obtained Weights) (2012)

**Description**: Uses directional wavelet filters to compute modification cost. Embeds primarily in edge regions.

**Why it's good**: Edge regions are "safer" from detection. Good balance of capacity and security.

**Papers**:
- Holub & Fridrich "Designing Steganographic Distortion Using Directional Filters" — 2012.

**Implementations**:
- [Wow- Steganography](https://github.com/3xpl01tc0d3r/WOW-steganography) ⭐ 156

- **Security Status**: 🟢 High — Competitive security
- **Community Acceptance**: 🟢 High — Widely implemented

#### S-UNIWARD (2013)

**Description**: Universal Wavelet Relative Distortion — applies directional filters in spatial domain, minimizes weighted sum of changes.

**Why it's good**: Works in both spatial and JPEG domain. Often cited as best-in-class security.

**Papers**:
- Holub et al. "Universal Distortion Function for Steganography" — 2013.
- Filler & Fridrich "On the Cost of Reliability of Detectors in Adaptive Steganography" — shows S-UNIWARD superiority.

**Implementations**:
- [nsf5sim](https://github.com/goxman/nsf5sim) ⭐ 78 — Includes S-UNIWARD

- **Security Status**: 🟢 Very High — Often achieves best detection resistance
- **Community Acceptance**: 🟢 Very High — De facto standard, most cited adaptive algorithm

#### HILL (2014)

**Description**: High-pass, Low-pass, Low-pass — applies high-pass filter then averages to get cost map. Spreads changes.

**Why it's good**: Distributes modifications to avoid concentrating in edges.

**Papers**:
- Li et al. "HILL: A Novel Image Steganography Framework" — 2014.

- **Security Status**: 🟢 High — Competitive with S-UNIWARD
- **Community Acceptance**: 🟢 High — Popular in implementations

#### MiPOD (2016)

**Description**: Minimizer of the Probabilistic Of Detection. Uses multivariate Gaussian model and Fisher information.

**Why it's good**: Theoretically optimal under Gaussian assumptions. Strong theoretical foundation.

**Papers**:
- Sedighi et al. "MiPOD: A Framework for Probabilistic Steganography" — 2016.

- **Security Status**: 🟢 High — Strong theoretical guarantees
- **Community Acceptance**: 🟡 Medium — Academic interest, fewer practical implementations

### JPEG Domain

#### JSteg (1993)

**Description**: Original JPEG steganography — LSB replacement in DCT coefficients.

**Why it's good**: Simple, historical significance.

**Papers**:
- Upham "JSteg Algorithm" — 1993.

- **Security Status**: 🔴 Very Low — One of first detected by histogram analysis
- **Community Acceptance**: 🟡 Medium — Historical importance, not recommended

#### F5 (2001)

**Description**: Matrix encoding + coefficient decrement. Embeds more efficiently than LSB, shrinks zeros.

**Why it's good**: Better efficiency than LSB methods.

**Papers**- Westfeld "F5 — A Steganographic Algorithm" — 2001.

**Implementations**:
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287

- **Security Status**: 🔴 Low — Vulnerable to shrinkage attack, blockiness analysis
- **Community Acceptance**: 🟡 Medium — Historically important

#### nsF5 (2007)

**Description**: F5 without shrinkage (wet paper codes). Better visual quality.

**Papers**:
- Fridrich et al. "Statistically Undetectable JPEG Steganography" — 2007.

- **Security Status**: 🟡 Medium — Better than F5 but still detected by CCJRM
- **Community Acceptance**: 🟡 Medium

#### OutGuess (2001)

**Description**: Preserves global DCT histogram during embedding.

**Papers**:
- Provos "Defending Against Statistical Steganalysis" — 2001.

- **Security Status**: 🔴 Low — Vulnerable to local statistics attacks
- **Community Acceptance**: 🟡 Medium

#### J-UNIWARD (2013)

**Description**: UNIWARD distortion applied to DCT coefficients.

**Why it's good**: Best JPEG steganography against JRM-feature steganalysis.

**Papers**:
- Holub et al. — Same paper as S-UNIWARD.

- **Security Status**: 🟢 High — State-of-art for JPEG
- **Community Acceptance**: 🟢 High

#### UED/UERD (2014)

**Description**: Uniform Embedding Distortion — distributes changes uniformly across AC coefficients.

**Papers**:
- Guo et al. "Uniform Embedding for Efficient JPEG Steganography" — 2014.

- **Security Status**: 🟢 High — Competitive with J-UNIWARD
- **Community Acceptance**: 🟡 Medium

### Transform Domain

#### DWT (Discrete Wavelet Transform)

**Description**: Embed in high-frequency wavelet subbands (HH, HL, LH).

**Why it's good**: Good robustness to compression, multi-resolution analysis.

**Papers**:
- Barni et al. "Improved Wavelet-Based Watermarking" — 2001.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

#### DFT (Discrete Fourier Transform)

**Description**: Embed in magnitude/phase spectrum.

**Why it's good**: Robust to geometric transforms (rotation, scaling).

**Papers**:
- Ru et al. "Robust Image Watermarking Based on DFT" — 2005.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

#### SVD (Singular Value Decomposition)

**Description**: Modify singular values.

**Why it's good**: Very robust to noise and filtering. Often combined with DWT.

**Papers**:
- Gorodetski et al. "SVD-based Watermarking Scheme" — 2001.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

### Reversible Methods

#### Histogram Shifting (2006)

**Description**: Shifts histogram peak to create space for embedding.

**Papers**:
- Ni et al. "Reversible Data Hiding" — IEEE TCSVT 2006.

- **Security Status**: 🟢 High — Lossless recovery
- **Community Acceptance**: 🟢 High — Important for medical/legal imaging

#### Difference Expansion (2003)

**Description**: Expands differences between adjacent pixels to embed.

**Papers**:
- Tian "Reversible Data Embedding" — 2003.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟢 High

#### Prediction Error Expansion (2007)

**Description**: Embeds in prediction error, not raw difference.

**Papers**:
- Thodi & Rodríguez "Expansion Embedding Techniques for Reversible Watermarking" — 2007.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟢 High

### Deep Learning Methods

#### HiDDeN (2018)

**Description**: First end-to-end deep learning steganography. Encoder-decoder with noise layer for robustness.

**Why it's good**: End-to-end trainable, learns to hide data optimally.

**Papers**:
- Baluja "Hiding Images in Plain Sight: Deep Steganography" — NeurIPS 2017.
- Extended in "HiDDeN: Hiding Data with Deep Networks" — 2018.

**Implementations**:
- [HiDDeN](https://github.com/tancik/HiDDeN) ⭐ 892

- **Security Status**: 🟡 Medium — Vulnerable to CNN steganalysis
- **Community Acceptance**: 🟢 High — Foundational work in DL stego

#### SteganoGAN (2019)

**Description**: GAN architecture with critic network for imperceptibility.

**Why it's good**: 2-4 bpp capacity, defeats XuNet steganalysis.

**Papers**:
- Shi et al. "SteanoGAN: Generative Steganography" — 2019.

**Implementations**:
- [SteganoGAN](https://github.com/DAI-Lab/SteganoGAN) ⭐ 428

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

#### StegaStamp (2020)

**Description**: Robust encoder with perspective augmentation. Survives print+photo.

**Why it's good**: First practical robust steganography — survives physical transmission.

**Papers**:
- Tancik et al. "StegaStamp: Robust Invisible Information Embedding" — CVPR 2020.

**Implementations**:
- [StegaStamp](https://github.com/tancik/StegaStamp) ⭐ 1.2k

- **Security Status**: 🟢 High — Robust to printing/photo
- **Community Acceptance**: 🟢 Very High — Most practical DL method

#### CRoSS (2023)

**Description**: Diffusion-based steganography. Cover generated by diffusion, message controls seed/path.

**Why it's good**: Diffusion provides natural cover distribution, robust to transmission.

**Papers**:
- Cao et al. "CRoSS: Diffusion-based Image Steganography" — NeurIPS 2023.

- **Security Status**: 🟢 High — State-of-art in generative stego
- **Community Acceptance**: 🟢 High — Growing rapidly

#### StegNet (2024)

**Description**: Multi-scale CNN achieving 98.2% decoding, 23.57 bpp.

**Papers**:
- Various 2024 papers on high-capacity DL stego.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium — Research active

---

## Audio Steganography

Human auditory system is sensitive but has limitations (sound masking, frequency ranges).

### Time Domain

#### LSB Audio

**Description**: Replace LSB of 16-bit PCM samples.

**Why it's good**: Maximum capacity, simple.

**Implementations**:
- [steghide](https://github.com/StephanHofmannmich/steghide) ⭐ 1.8k — Also supports audio

- **Security Status**: 🔴 Low — Easily detected
- **Community Acceptance**: 🟡 Medium

#### Parity Coding

**Description**: Parity of group of samples encodes one bit.

**Why it's good**: More robust than raw LSB.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

#### Echo Hiding

**Description**: Adds echoes with different delays to represent bits.

**Why it's good**: Takes advantage of auditory masking.

**Papers**:
- Bender et al. "Techniques for Data Hiding" — 1996.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

#### Phase Coding

**Description**: Replaces initial phase of segments.

**Why it's good**: Human ear is insensitive to phase changes.

**Papers**:
- Bender et al. — Same foundational paper.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

### Frequency Domain

#### Spread Spectrum

**Description**: Message spread via PN sequence across wide frequency band.

**Why it's good**: Robust to filtering and compression.

**Papers**:
- Malvar & Florencio "Improved Spread Spectrum Watermarking" — 2003.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟢 High

### Compressed Formats

#### MP3Stego

**Description**: Embeds during MP3 encoding process.

**Papers**:
- Petitcolas "MP3Stego" — 1998.

**Implementations**:
- [mp3stego](http://www.petitcolas.net/steganography/mp3stego/) — Official

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

### Neural Network Methods

#### DeepSound

**Description**: Autoencoder on spectrograms.

**Implementations**:
- [DeepSound](https://github.com/ElsebyCoder/DeepSound) ⭐ 312

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

#### WavMark (Microsoft 2023)

**Description**: Invertible network for watermarking, robust to re-encoding.

**Papers**:
- Wenger et al. "WavMark: Watermarking for Audio Generation" — 2023.

- **Security Status**: 🟢 High — Robust to re-encoding
- **Community Acceptance**: 🟢 High

#### AudioSeal (Meta 2024)

**Description**: Detection + localization watermark for AI-generated audio.

**Papers**:
- "AudioSeal: Audio Watermarking for Generation Detection and Localization" — 2024.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟢 High

---

## Video Steganography

Video = frames + audio + motion vectors + prediction modes. Massive capacity, but re-encoding destroys LSB.

| Method | Embedding Location | Robustness |
|--------|-------------------|------------|
| **Frame LSB/DCT** | Each frame as image | Low |
| **Motion Vector** | MPEG/H.264/H.265 MV | Medium |
| **Intra Prediction Mode** | HEVC 33→35 directions | High |
| **QP Modulation** | Quantization parameter | High |
| **CABAC** | Entropy coding order | High |
| **HEVC PU Partition** | Partition pattern selection | High |

#### Security & Community

- **Security Status**: 🟡 Medium overall — Format-specific methods (HEVC, CABAC) more secure
- **Community Acceptance**: 🟢 High for research, limited practical use due to re-encoding

---

## Network Steganography

Cover = network traffic (packets, headers, timing). Data is ephemeral — disappears after transmission.

### Header Fields

| Protocol | Field | Bits/Packet |
|----------|-------|-------------|
| IPv4 | Identification | 16 |
| IPv4 | TTL | 1-2 |
| IPv4 | DSCP/ToS | 6 |
| IPv4 | Options | up to 40 bytes |
| IPv6 | Flow Label | 20 |
| IPv6 | Extension Headers | flexible |
| TCP | ISN | 32/connection |
| TCP | Timestamp | 4-8 |
| TCP | Window Size | ~1 |
| HTTP | Header order | log2(N!) |
| QUIC | Connection ID | 0-20 bytes |

### Timing Channels

- **IPD encoding** — Inter-packet delay (bit 0 = delay < T, bit 1 = delay > T)
- **Jitterbug** — Keystroke timing modulation
- **On-off timing** — Presence/absence in time window

### DNS Tunneling

| Tool | Method | Throughput | Implementations |
|------|--------|------------|-----------------|
| **iodine** | IP-over-DNS via TXT/NULL | ~100 KB/s | [iodine](https://github.com/yarrick/iodine) ⭐ 3.8k |
| **dnscat2** | C2 in TXT records | 1-10 KB/s | [dnscat2](https://github.com/zbetcheckin/dnscat2) ⭐ 2.1k |
| **dns2tcp** | TCP over DNS | 10-50 KB/s | [dns2tcp](https://github.com/alexbakker/dns2tcp) ⭐ 289 |
| **DNScat-DoH** | DNS over HTTPS | Higher | Part of dnscat2 |

#### Security & Community

- **Security Status**: 🟡 Medium — iodine/dns2tcp highly detectable; DoH variant lower
- **Community Acceptance**: 🟢 High in red-teaming, deprecated for operational security

### QUIC/HTTP3

#### QuicCourier (2024)

**Description**: 20 new covert channels in QUIC including Connection ID, Packet Number gaps, PADDING length, Frame ordering, ACK delay, etc.

**Papers**:
- "QuicCourier: Hiding Data in QUIC" — 2024.

- **Security Status**: 🟢 High — New protocol, less detection tooling
- **Community Acceptance**: 🟡 Medium — Research active, few implementations

### VoIP / RTP

- **LACK** (Mazurczyk 2008) — Intentional packet loss carries stego
- **SteganoRTP** — Padding bit or CSRC list
- **SIP-stego** — SIP signaling headers

**Papers**:
- Mazurczyk "LACK: VoIP Steganography" — 2008.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### Blockchain

- **OP_RETURN** — Up to 80 bytes in Bitcoin tx
- **Address generation** — Pre-image as message
- **Transaction amount LSB** — Bits in satoshis
- **Ethereum calldata** — Arbitrary data in input

- **Security Status**: 🟢 High for persistence, 🔴 Low for detectability (all transactions visible)
- **Community Acceptance**: 🟢 High — Active use in NFT/metadata

---

## Filesystem & OS

| Method | Platform | Principle |
|--------|----------|-----------|
| **File slack** | Any FS with fixed cluster | Unused space in cluster |
| **Volume slack** | FAT, NTFS | Between partitions |
| **NTFS ADS** | NTFS | Alternate Data Streams |
| **HPA/DCO** | HDD/SSD ATA | Protected area invisible to OS |
| **StegFS** | Linux loopback | Transparent FS indistinguishable from empty |
| **VeraCrypt hidden volume** | Volume-level | Plausible deniability |
| **Metadata** | Universal | EXIF, ID3, etc. |

#### VeraCrypt Hidden Volume

**Description**: Hidden volume inside outer VeraCrypt container. Plausible deniability — can reveal outer password while hidden volume remains undetectable.

**Implementations**:
- [VeraCrypt](https://github.com/veracrypt/VeraCrypt) ⭐ 4.5k

- **Security Status**: 🟢 Very High — Mathematically cannot prove existence
- **Community Acceptance**: 🟢 Very High — Standard for deniable encryption

#### NTFS ADS

- **Security Status**: 🔴 Low — Detectable by all NTFS tools
- **Community Acceptance**: 🟡 Medium — Known but limited use

---

## Coverless / Generative

Don't modify existing cover — generate new one or select from collection.

#### Coverless Image (2015)

**Description**: Shared hash dictionary, find image with matching hash. Alice hashes message, finds matching image in shared collection, sends it.

**Papers**:
- Zhou et al. "Coverless Image Steganography Based on Image Retrieval" — 2015.

- **Security Status**: 🟢 Very High — No modified pixels to detect
- **Community Acceptance**: 🟡 Medium — Requires large shared image database

#### StyleGAN Stego

**Description**: Latent vector encodes bits, generates face/landscape via StyleGAN.

**Papers**:
- Various 2020+ papers on GAN-based steganography.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium — Computationally expensive

#### CRoSS (2023)

See Image Steganography section.

#### MIDAS (2025)

**Description**: Training-free diffusion-based coverless with multi-image hiding and user-specific access control.

**Papers**:
- "MIDAS: Multi-Image Diffusion Steganography" — 2025.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium — Very recent

---

## Traffic Obfuscation

Make traffic *look* like legitimate protocol. Overlaps with steganography.

### Tor Pluggable Transports

| Transport | Mimics | Implementations |
|-----------|--------|-----------------|
| **obfs4** | Random noise | [obfs4](https://gitlab.com/yawning/obfs4) ⭐ 892 |
| **meek** | HTTPS to CDN | Part of Tor |
| **Snowflake** | WebRTC P2P | [snowflake](https://gitweb.torproject.org/pluggable-transports/snowflake.git) ⭐ 234 |
| **WebTunnel** | HTTPS + WebSocket | [WebTunnel](https://github.com/Arkanic/WebTunnel) ⭐ 156 |

- **Security Status**: 🟡 Medium — obfs4 detectable by probing; meek domain-fronted
- **Community Acceptance**: 🟢 High — Essential for circumvention

### V2Ray / Xray / REALITY

```
V2Ray + VMess (2018) → VLESS (2022) → REALITY (2023) → XTLS-Vision (2024)
```

#### REALITY (2023)

**Description**: Spoofs TLS handshake to real site (google.com), uses SNI fingerprinting. MitM-resistant — if warden tries to MitM, client sees certificate mismatch.

**Implementations**:
- [Xray-core](https://github.com/XTLS/Xray-core) ⭐ 8.2k
- [sing-box](https://github.com/SagerNet/sing-box) ⭐ 4.1k

- **Security Status**: 🟢 Very High — Best current circumvention protocol
- **Community Acceptance**: 🟢 Very High — Dominant in China/ Iran circumvention

### Other Protocols

| Protocol | Implementations |
|----------|-----------------|
| **Trojan-GFW** | [trojan-go](https://github.com/p4gefau1t/trojan-go) ⭐ 3.2k |
| **Hysteria 2** | [hysteria](https://github.com/apernet/hysteria) ⭐ 4.8k |
| **NaiveProxy** | [naiveproxy](https://github.com/klzgrad/naiveproxy) ⭐ 2.9k |
| **Shadowsocks** | [shadowsocks](https://github.com/shadowsocks/shadowsocks) ⭐ 3.5k |
| **OutlineVPN** | [outline](https://github.com/Jigsaw-Code/outline-server) ⭐ 2.1k |

- **Security Status**: 🟢 High overall for TLS-wrapped protocols
- **Community Acceptance**: 🟢 High

### ICMP Tunnels

- [icmptunnel](https://github.com/rozet/icmptunnel) ⭐ 423
- [PingTunnel](https://github.com/rozet/PingTunnel) ⭐ 312

- **Security Status**: 🔴 Low — Easy to detect
- **Community Acceptance**: 🟡 Medium

---

## Steganalysis

Detecting hidden data — the adversarial discipline.

### Classical (Images)

| Method | Year | Description |
|--------|------|-------------|
| **χ² (chi-square)** | 1999 | Detects LSB pairing anomalies |
| **RS-analysis** | 2001 | Regular/Singular group analysis |
| **WS (Weighted Stego)** | 2005 | Estimates embedding rate |
| **SPAM** | 2007 | 686D co-occurrence features |
| **SRM** | 2011 | 34,671D rich model features |
| **DCTR** | 2015 | DCT residuals for JPEG |
| **PHARM** | 2016 | Phase-aware features |

- **Community Acceptance**: 🟢 High — SRM standard for years

### Deep Learning

| Method | Year | Papers | Implementations |
|--------|------|--------|-----------------|
| **XuNet** | 2016 | Xu et al. "CNN-based Steganalysis" | [xunet](https://github.com/umich-vrl/gsi) ⭐ 156 |
| **YeNet** | 2017 | Ye et al. — SRM-like first layer | — |
| **SRNet** | 2019 | Boroumand et al. | [SRNet](https://github.com/Chris铎/SRNet) ⭐ 234 |
| **ZhuNet** | 2020 | Covariance pooling | — |

- **Community Acceptance**: 🟢 High — SRNet current state-of-art

### Network

- Tor traffic classifier (CNN)
- DPI + ML fingerprinting (JA3/JA4)
- Traffic shaping analysis
- Randomness analysis

---

## Additional Image Methods

### Quantization-Based Methods

#### QIM (Quantization Index Modulation)

**Description**: Embeds bits by quantizing DCT coefficients using quantizers indexed by secret bits. Each coefficient is quantized to one of two quantizers depending on the bit to embed.

**Why it's good**: Theoretically optimal under certain assumptions, robust to compression.

**Papers**:
- Chen & Wornell "Quantization Index Modulation: A Class of Provably Good Methods for Digital Watermarking and Information Embedding" — IEEE T-IT 2001.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟢 High

### 1-bit Q-Table Modification

**Description**: Embeds 1 bit by modifying JPEG quantization table values by ±1 while maintaining JPEG compatibility.

**Why it's good**: Exploits quantization table redundancy.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### Sudoku-based Steganography

**Description**: Uses Sudoku puzzle solutions as mapping keys for embedding.

**Papers**:
- "Sudoku-based Steganography" — 2018+.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### Fuzzy Logic-based (FuzzyStego)

**Description**: Uses fuzzy logic to categorize pixels into intensity levels for adaptive embedding.

**Papers**:
- "FuzzyStego: Fuzzy Logic Based Image Steganography" — 2025.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### Chaotic Map LSB

**Description**: Uses 1D/2D chaotic maps combined with LSB for enhanced security.

**Papers**:
- "Chaotic Map Based LSB Steganography" — 2024.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### Transform Domain (Advanced)

#### Contourlet Transform

**Description**: Embedding in contourlet coefficients — multi-directional transform.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

#### Non-subsampled Contourlet Transform (NSCT)

**Description**: Shift-invariant transform for robust embedding.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

---

## Additional Audio Methods

### Vocoder-Based Methods

#### LPC (Linear Predictive Coding) Steganography

**Description**: Embeds in LPC coefficients or residual signals.

**Why it's good**: Takes advantage of speech compression characteristics.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

#### CELP (Code Excited Linear Prediction) Steganography

**Description**: Modifies codebook indices or pitch values in CELP coders.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### Audio Diffusion Methods

#### PRoADS (2025)

**Description**: Provably secure robust audio steganography based on audio diffusion models. Embeds in initial noise via orthogonal matrix projection.

**Papers**:
- "PRoADS: Provably Secure Audio Diffusion Steganography" — 2025.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium — Very recent

---

## Additional Network Methods

### HTTP/3 Frame Padding

**Description**: Embeds in frame padding patterns in HTTP/3.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium

### WireGuard Steganography

**Description**: Embedding in WireGuard handshake messages.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### 5G/6G Cellular

#### SteaLTE (2021)

**Description**: First full-stack LTE steganography for Private 5G Cellular Connectivity.

**Papers**:
- "SteaLTE: LTE Steganography for Private 5G" — 2021.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium

#### 5G Slice Steganography

**Description**: Embeds in network slice allocation messages.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### CYPRESS (2025)

**Description**: Framework creating covert channels by mounting secret packets on regular packets, achieving up to 1.6MB/s throughput.

**Papers**:
- "CYPRESS: High-Speed Covert Channels" — 2025.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

### Wi-Fi CSI Steganography (2026)

**Description**: Embeds secrets within Channel State Information using FIR filters.

**Papers**:
- "Wi-Fi CSI Steganography" — 2026.

- **Security Status**: 🟡 Medium
- **Community Acceptance**: 🟡 Medium

---

## Additional Coverless Methods

### MIDAS (2025)

**Description**: Training-free diffusion-based coverless framework with multi-image hiding and user-specific access control via latent-level fusion.

**Papers**:
- "MIDAS: Multi-Image Diffusion Steganography" — 2025.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium

### StegoNGP (2024)

**Description**: 3D cryptographic steganography using Instant-NGP (Neural Graphics Primitives), key-controlled scene switcher.

**Papers**:
- "StegoNGP: 3D Neural Graphics Steganography" — 2024.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium

### Splats in Splats++ (2026)

**Description**: Robust 3D Gaussian Splatting Steganography — embeds 3D/4D content in native 3DGS representation.

**Papers**:
- "3DGS Steganography" — 2026.

- **Security Status**: 🟢 High
- **Community Acceptance**: 🟡 Medium

---

## Physical & Social Steganography

### Printer Steganography (Yellow Dots)

**Description**: Color laser printers add tiny yellow dots containing serial number and timestamp. Not classical steganography but related.

**Implementations**:
- [Printer Steganography Detector](https://github.com/abe-modyo/printer-steganography) ⭐ 89

- **Security Status**: 🔴 Low for privacy (intentional tracking)
- **Community Acceptance**: 🟢 High — Well-documented

### Social Steganography

**Description**: Hiding messages in cultural references, idiom, pop culture — visible only to those who know the context.

**Examples**: Watermelon as Palestinian symbol, misspelled names suggesting alternative meaning.

- **Security Status**: 🟢 Very High — No technical detection possible
- **Community Acceptance**: 🟢 High — Active in censored communities

---

## Key Papers & Resources

### Foundational

- [Wikipedia: Steganography](https://en.wikipedia.org/wiki/Steganography)
- [List of Steganography Techniques](https://en.wikipedia.org/wiki/List_of_steganography_techniques)

### Surveys

- [Survey on DL-based Image Steganography (2024)](https://www.sciencedirect.com/science/article/abs/pii/S0957417424012569)
- [Network Steganography Survey (2015)](https://ieeexplore.ieee.org/document/7315017)

### Key Papers

- [Meteor: Cryptographically Secure Steganography](https://arxiv.org/abs/2105.13080) — USENIX 2021
- [CRoSS: Diffusion Steganography](https://arxiv.org/abs/2309.14201) — NeurIPS 2023
- [StegaStamp: Robust Invisible Embedding](https://arxiv.org/abs/1912.04088) — CVPR 2020
- [QuicCourier: QUIC Covert Channels](https://lib.jucs.org/article/154672/) — 2024
- [S-UNIWARD Security Study](http://dde.binghamton.edu/tomasD/pdf/SPIE14_Further_Study_on_Security_of_S-UNIWARD.pdf)

### Implementations Collections

- [Steganography Software Wiki](https://www.jjtc.com/Steganography)
- [OpenStego](https://github.com/syvaidya/openstego) ⭐ 287
- [steghide](https://github.com/StephanHofmannmich/steghide) ⭐ 1.8k

### Python Libraries

- [stegano](https://github.com/BZFlag/distribution/tree/main/stegano) ⭐ 245 — Pure Python steganography
- [steganography](https://github.com/7thByte/steganography) ⭐ 178 — Simple LSB
- [lsb-steganography](https://github.com/RobinDavid/LSB-steganography) ⭐ 156
- [py-steg](https://github.com/b3ny0ng/py-steg) ⭐ 89

### Steganalysis Tools

- [aletheia](https://github.com/8dcc/aletheia) ⭐ 456 — Steganalysis tool
- [stegdetect](https://github.com/abeluck/stegdetect) ⭐ 234 — Classical steganalysis
- [stegano](https://github.com/BZFlag/distribution/tree/main/stegano) — Includes detection

### Network Stego Tools

- [Cloak](https://github.com/cretz/coffee-and-tea) ⭐ 234 — Covert tunnel
- [dnscat2](https://github.com/zbetcheckin/dnscat2) ⭐ 2.1k
- [iodine](https://github.com/yarrick/iodine) ⭐ 3.8k
- [dns2tcp](https://github.com/alexbakker/dns2tcp) ⭐ 289

### Deep Learning

- [HiDDeN](https://github.com/tancik/HiDDeN) ⭐ 892
- [StegaStamp](https://github.com/tancik/StegaStamp) ⭐ 1.2k
- [SteganoGAN](https://github.com/DAI-Lab/SteganoGAN) ⭐ 428
- [DeepSound](https://github.com/ElsebyCoder/DeepSound) ⭐ 312

---

## Security Status Legend

| Rating | Meaning |
|--------|---------|
| 🟢 Very High | State-of-art, theoretically provable security |
| 🟢 High | Strong security, widely trusted |
| 🟡 Medium | Moderate security, known vulnerabilities |
| 🔴 Low | Easily detected, not recommended |
| 🔴 Very Low | Severely compromised, historical only |

## Community Acceptance Legend

| Rating | Meaning |
|--------|---------|
| 🟢 Very High | Industry standard, widely implemented |
| 🟢 High | Popular, well-tested |
| 🟡 Medium | Academic interest, limited practical use |
| 🔴 Low | Deprecated, not recommended |

---

## License

MIT
