# Text Steganography

<!-- TOC -->
## Contents (16 algorithms)

**[Structural Methods](#structural-methods)**
- [ASCII Art Steganography](#ascii-art-steganography)
- [Word Change Tracking](#word-change-tracking)
- [Bacon's Cipher](#bacons-cipher)
- [Null Cipher](#null-cipher)
- [Whitespace coding](#whitespace-coding)
- [Zero-width Unicode](#zero-width-unicode)
- [Homoglyphs](#homoglyphs)

**[Semantic Methods](#semantic-methods)**
- [Chaffing and Winnowing](#chaffing-and-winnowing)
- [Mimic Functions](#mimic-functions)

**[LLM-Based Methods](#llm-based-methods)**
- [Meteor](#meteor)
- [Discop](#discop)
- [ChatStega](#chatstega)
- [Blog-Steganography](#blog-steganography)
- [Range Coding](#range-coding)
- [Anchored Sliding Window](#anchored-sliding-window-asw)
- [ReTokSync](#retoksync)
- [Entropy-Driven](#entropy-driven-rank-token-mapping)
- [Auto-Stega](#auto-stega)
- [Dynamic Codebook](#dynamic-codebook)
- [OD-Stega](#od-stega)
- [Shifting-Merging](#shifting-merging)
- [Semantic Steganography](#semantic-steganography-llm)
- [Content-Preserving Linguistic](#content-preserving-linguistic-steganography)
- [Raster Domain Text](#raster-domain-text-steganography)
- [Alkaid](#alkaid)
- [SparSamp](#sparsamp)
- [Kolmogorov Complexity Bounds](#kolmogorov-complexity-bounds)
- [STEAD](#stead-robust-provably-secure-linguistic-steganography)
- [Hide and Seek in Embedding Space](#hide-and-seek-in-embedding-space)
- [StegoStylo](#stegastylo)
- [Undetectable Conversations](#undetectable-conversations)
- [TrojanStego](#trojanstego)
- [GTSD](#gtsd-generative-text-steganography-via-diffusion)
- [List Decoding](#provably-secure-steganography-based-on-list-decoding)
<!-- /TOC -->

## Structural Methods

---

### ASCII Art Steganography

**Goal:** Hide data in ASCII art representations.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **ASCII Art** | 2010 | Character density | Survives printing |

**State of the art:** Novel approach surviving print.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

### Word Change Tracking

**Goal:** Hide data using word processor change tracking feature.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Change Tracking** | 2007 | Deliberate errors | Word docs |

**State of the art:** Uses Word change tracking.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### Bacon's Cipher

**Goal:** Hide data using two different typefaces in text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Bacon's Cipher** | 1605 | Bold/italic encode 0/1 | 5 bits/letter |

**State of the art:** Classic historical method, still used in puzzles.

**Production readiness:** Deprecated

**Security status:** Broken — Easily detected visually

**Community acceptance:** Niche — Historical importance

---

### Null Cipher

**Goal:** Hide message as first letters of words in innocent text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Null Cipher** | 1901 | Acrostic/first letters | Requires long cover |

**State of the art:** Simple but requires careful cover text selection.

**Production readiness:** Deprecated

**Security status:** Broken — Detectable by statistical analysis

**Community acceptance:** Niche

---

### Whitespace Coding

**Goal:** Hide data in whitespace characters of plain text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Whitespace coding** | 1998 | Trailing spaces (1=0, 2=1) | 1 bit/line |

**State of the art:** Simple but easily detectable. Limited capacity but works in any text format.

---

### Zero-width Unicode

**Goal:** Hide data using invisible Unicode characters.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Zero-width Unicode** | 2005 | U+200B, U+200C, U+200D, U+FEFF | ~2-3 bit/char |

**State of the art:** Popular for CTF challenges. Easily detected by regex.

---

### Homoglyphs

**Goal:** Hide data using visually identical characters from different scripts.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Homoglyphs** | 2000 | Cyrillic а→a, Greek ο→o | 1 bit/char |

**State of the art:** Visually indistinguishable but detectable via script analysis.

---

## Semantic Methods

---

### Chaffing and Winnowing

**Goal:** Separate authentic from chaff messages.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chaffing** | 1998 | MAC authentication | Rivest |

**State of the art:** Unique authentication-based approach.

**Production readiness:** Mature

**Security status:** Secure

**Community acceptance:** Widely trusted

---

### Mimic Functions

**Goal:** Generate text that encodes secret data using grammar rules.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Mimic Functions** | 1992 | CFG where generated text encodes bits | Wayner |

**State of the art:** Early approach, text often sounds unnatural.

**Production readiness:** Deprecated

**Security status:** Low — Detectable as machine-generated

**Community acceptance:** Low — Historical importance only

---

## LLM-Based Methods

---

### Meteor

**Goal:** Information-theoretically secure steganography using LLM probability distributions.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Meteor** | 2021 | Arithmetic coding over LLM log-probabilities [[1]](https://arxiv.org/abs/2105.13080) |

**State of the art:** Best theoretical security. Distribution-preserving — text indistinguishable from normal LLM output without original prompt.

**Production readiness:** Experimental

**Implementations:**
- [meteor-stego](https://github.com/tmthrgd/meteor-stego) ⭐ 215 — Python implementation

**Security status:** Secure — Proven information-theoretically secure against passive warden without prompt access

**Community acceptance:** Widely trusted — Academic breakthrough; practical implementations emerging

---

### Discop

**Goal:** Efficient distribution-preserving steganography using bucket-based sampling.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Discop** | 2023 | Distribution-copy: buckets over token probabilities [[2]](https://arxiv.org/abs/2305.19103) |

**State of the art:** Faster than Meteor but slightly less efficient.

**Production readiness:** Experimental

**Security status:** Secure — Slightly less efficient than Meteor but still distribution-preserving

**Community acceptance:** Emerging — Active research, fewer implementations

---

### ChatStega

**Goal:** Steganography using LLM sampling parameters.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **ChatStega** | 2024 | Sampling with different top-p/temperature in ChatGPT |

**State of the art:** Simple but depends on LLM sampling randomness.

**Production readiness:** Experimental

**Security status:** Caution — Detectable with access to sampling seed

**Community acceptance:** Emerging — Growing interest in practical LLM steganography

---

### Blog-Steganography

**Goal:** Hide messages in blog comments across the internet.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Blog-Stego** | 2011 | Fractionalized + blog selection | Key = blog set |

**State of the art:** Uses blogosphere as carrier.

**Production readiness:** Experimental

**Security status:** Secure — Distributed

**Community acceptance:** Niche

---

### Range Coding

**Goal:** Provably secure linguistic steganography using range coding.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Range Coding** | 2025 | Efficient provably secure linguistic steganography via range coding [[1]](https://arxiv.org/abs/2604.08052) |

**State of the art:** Combines theoretical security with practical efficiency.

**Production readiness:** Experimental

**Security status:** Secure — Provably secure

**Community acceptance:** Emerging — Active research

---

### Anchored Sliding Window (ASW)

**Goal:** Robust linguistic steganography resistant to text modifications.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **ASW** | 2026 | Anchored sliding window for robustness against edits [[1]](https://arxiv.org/abs/2604.09066) |

**State of the art:** Addresses fragility of previous methods to minor text modifications.

**Production readiness:** Experimental

**Security status:** Secure — Robust to modifications

**Community acceptance:** Emerging

---

### ReTokSync

**Goal:** Solve tokenization disambiguation in generative linguistic steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **ReTokSync** | 2026 | Self-synchronizing tokenization disambiguation [[1]](https://arxiv.org/abs/2604.25486) |

**State of the art:** Fixes decoding failures from tokenization ambiguity.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Entropy-Driven Rank-Token Mapping

**Goal:** High-capacity linguistic steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Entropy-Driven** | 2025 | Entropy-driven rank-token mapping [[1]](https://arxiv.org/abs/2510.23035) |

**State of the art:** Addresses capacity limitations in prior methods.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

### Auto-Stega

**Goal:** Agent-driven system for adaptive steganography strategy.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Auto-Stega** | 2025 | Agent-driven lifelong strategy evolution [[1]](https://arxiv.org/abs/2510.06565) |

**State of the art:** Dynamic strategy selection for varying conditions.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Dynamic Codebook

**Goal:** Text steganography with dynamic codebook using LLMs.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Dynamic Codebook** | 2026 | Text steganography with dynamic codebook [[1]](https://arxiv.org/abs/2604.20269) |

**State of the art:** Addresses white-box paradigm limitations.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### OD-Stega

**Goal:** Relatively secure steganography via optimized distributions.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **OD-Stega** | 2024 | LLM-based relatively secure steganography [[1]](https://arxiv.org/abs/2410.04328) |

**State of the art:** Uses optimized distributions for better security.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Shifting-Merging

**Goal:** Secure, high-capacity and efficient LLM-based steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Shifting-Merging** | 2025 | Shifting-merging approach [[1]](https://arxiv.org/abs/2501.00786) |

**State of the art:** Combines high capacity with efficiency.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Semantic Steganography (LLM)

**Goal:** Robust and high-capacity information hiding using LLMs.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Semantic Stega** | 2025 | Semantic steganography framework [[1]](https://arxiv.org/abs/2412.11043) |

**State of the art:** Bridges semantic richness with steganographic capacity.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Content-Preserving Linguistic Steganography

**Goal:** Preserve original content while embedding secret messages.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Content-Preserving** | 2025 | Content-preserving secure linguistic steganography [[1]](https://arxiv.org/abs/2511.12565) |

**State of the art:** Reduces detectable deviations between normal and stego text.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Raster Domain Text Steganography

**Goal:** Embed heterogeneous data directly into pixel space of rendered textual glyphs.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Raster Domain Text** | 2025 | Unified framework for multimodal secure embedding into glyph bitmaps [[1]](https://arxiv.org/abs/2512.21698) |

**State of the art:** Operates after font rasterization, treating each glyph as a cover.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Alkaid (Provably Secure Steganography)

**Goal:** Resilience to edit errors via distance-constrained encoding.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Alkaid** | 2026 | Distance-constrained encoding for edit error resilience [[1]](https://arxiv.org/abs/2603.06169) |

**State of the art:** Bridges gap between provably secure steganography and real-world edit errors.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging

---

### SparSamp (Sparse Sampling)

**Goal:** Efficient provably secure steganography via sparse sampling.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **SparSamp** | 2025 | Sparse sampling for efficient provable security [[1]](https://arxiv.org/abs/2503.19499) |

**State of the art:** Improves efficiency of provably secure steganography.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging

---

### Kolmogorov Complexity Bounds

**Goal:** Information-theoretic cost bounds for LLM steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Kolmogorov Bounds** | 2026 | Theoretical framework for LLM steganography cost [[1]](https://arxiv.org/abs/2603.21567) |

**State of the art:** First formal analysis of LLM steganography complexity.

**Production readiness:** Research

**Security status:** Theoretical foundation

**Community acceptance:** Emerging

---

### STEAD (Robust Provably Secure Linguistic Steganography)

**Goal:** Robust provably secure linguistic steganography with diffusion language models.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **STEAD** | 2026 | Diffusion LM-based robust PSLS [[1]](https://arxiv.org/abs/2601.14778) |

**State of the art:** Combines provable security with diffusion model robustness.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### Hide and Seek in Embedding Space

**Goal:** Low-recoverability steganography using embedding-space geometry.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Embedding Space** | 2026 | Geometry-based steganography in LLM embeddings [[1]](https://arxiv.org/abs/2601.22818) |

**State of the art:** Replaces arbitrary mappings with embedding-derived ones.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### StegoStylo

**Goal:** Evade stylometric analysis through adversarial steganographic stitching.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **StegoStylo** | 2026 | Adversarial stylometry combined with steganography [[1]](https://arxiv.org/abs/2601.09056) |

**State of the art:** Uses adversarial attack to confound stylometric analysis.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Emerging

---

### Undetectable Conversations

**Goal:** Covert communication between AI agents using pseudorandom noise-resilient key exchange.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Undetectable Conversations** | 2026 | Optimal-rate covert conversation with interaction-unique keys [[1]](https://arxiv.org/abs/2604.04757) |

**State of the art:** Combines watermarking and steganography for hidden channel.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### TrojanStego

**Goal:** LLM as steganographic channel for privacy leaking via fine-tuning.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **TrojanStego** | 2025 | Fine-tuned LLM embeds sensitive context into outputs [[1]](https://arxiv.org/abs/2505.20118) |

**State of the art:** Compromised LLM maintains safety facade while leaking data.

**Production readiness:** Research — Security threat model

**Security status:** Caution

**Community acceptance:** Controversial

---

### GTSD (Generative Text Steganography via Diffusion)

**Goal:** Generative text steganography using diffusion language models.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **GTSD** | 2025 | Diffusion model-based text steganography addressing autoregressive limitations [[1]](https://arxiv.org/abs/2504.19433) |

**State of the art:** Overcomes sequential generation limitations of autoregressive models.

**Production readiness:** Research

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Provably Secure Steganography Based on List Decoding

**Goal:** Theoretical foundation for steganography using list decoding.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **List Decoding** | 2026 | Provably secure steganography with theoretical guarantees [[1]](https://arxiv.org/abs/2604.21394) |

**State of the art:** Provides mathematical security proofs for steganographic schemes.

**Production readiness:** Research

**Security status:** Secure — Provably secure

**Community acceptance:** Emerging
