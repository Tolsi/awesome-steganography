# Text Steganography

<!-- TOC -->
## Contents (17 algorithms)

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
- [Addressing Tokenization Inconsistency](#addressing-tokenization-inconsistency)
<!-- /TOC -->

## Structural Methods

---

### ASCII Art Steganography

**Goal:** Hide data in ASCII art representations.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **ASCII Art** | 2010 | Character density | Survives printing [[1]](https://wayner.org/node/43) [[2]](https://arxiv.org/abs/1003.1470) |

**State of the art:** Novel approach surviving print. Peter Wayner's description at wayner.org remains the key reference; the 2010 arXiv survey provides broader context.

**Production readiness:** Experimental
Works as a proof-of-concept; no mainstream tooling or library support.

**Implementations:**
- [ascii-steganography](https://github.com/vgmoose/ascii-steganography) ⭐ 18 — Python, hides data in plain ASCII art

**Security status:** Caution
Visually convincing but detectable by automated density-analysis; printing reduces capacity significantly.

**Community acceptance:** Niche
Interesting novelty, cited in surveys but rarely used in practice.

---

### Word Change Tracking

**Goal:** Hide data using word processor change tracking feature.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Change Tracking** | 2007 | Deliberate errors | Word docs [[1]](https://people.cs.nycu.edu.tw/~whtsai/Journal%20Paper%20PDFs/Liu_&_Tsai_IEEE_T_IFS_2007.pdf) |

**State of the art:** Liu & Tsai (IEEE T-IFS 2007) propose hiding data by introducing synonym-based degradations in a document and tracking the revisions; the change-tracking metadata encodes the payload.

**Production readiness:** Experimental
Academic prototype; requires Microsoft Word and collaborative editing context.

**Security status:** Caution
Detectable if an adversary inspects revision metadata or compares against the clean document.

**Community acceptance:** Niche
Cited in text-steganography surveys but not adopted beyond academic settings.

---

### Bacon's Cipher

**Goal:** Hide data using two different typefaces in text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Bacon's Cipher** | 1605 | Bold/italic encode 0/1 | 5 bits/letter [[1]](https://en.wikipedia.org/wiki/Bacon%27s_cipher) [[2]](https://pi.math.cornell.edu/~morris/135/Bacon.pdf) |

**State of the art:** Classic historical method described by Francis Bacon in *De Augmentis Scientiarum* (1623); still used in CTF puzzles and historical cryptography courses.

**Production readiness:** Deprecated
Superseded by every modern method; retained only for educational and puzzle contexts.

**Security status:** Broken
Trivially detected by visual inspection or font-analysis tools; no practical security.

**Community acceptance:** Niche
Historically significant as an early binary encoding scheme; not used in modern steganography.

---

### Null Cipher

**Goal:** Hide message as first letters of words in innocent text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Null Cipher** | 1901 | Acrostic/first letters | Requires long cover [[1]](https://en.wikipedia.org/wiki/Null_cipher) [[2]](https://www.garykessler.net/library/steganography.html) |

**State of the art:** Ancient acrostic technique; the Wikipedia article and Kessler's steganography overview are the canonical modern references.

**Production readiness:** Deprecated
Requires careful, labour-intensive cover-text construction; no automated tooling.

**Security status:** Broken
Detectable by statistical analysis of first-letter frequency distributions.

**Community acceptance:** Niche
Historically notable (used in WWI/WWII messages); purely educational today.

---

### Whitespace Coding

**Goal:** Hide data in whitespace characters of plain text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Whitespace coding (SNOW)** | 1998 | Trailing spaces/tabs at end of lines | ~3 bits per 8 columns [[1]](https://darkside.com.au/snow/) |

**State of the art:** SNOW (Steganographic Nature Of Whitespace) by Matthew Kwan (1998) is the canonical implementation; simple but easily detectable. Limited capacity but works in any plain-text format.

**Production readiness:** Mature
SNOW is a stable, long-standing tool available on most Unix systems as `stegsnow`.

**Implementations:**
- [snow](https://github.com/mattkwan-zz/snow) ⭐ 50 — C, original SNOW by Matthew Kwan

**Security status:** Caution
Invisible to human readers but trivially detected by checking trailing whitespace; any text editor or diff tool reveals it.

**Community acceptance:** Widely trusted
One of the oldest and best-known text steganography tools; standard CTF challenge technique.

---

### Zero-width Unicode

**Goal:** Hide data using invisible Unicode characters.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Zero-width Unicode** | 2005 | U+200B, U+200C, U+200D, U+FEFF | ~2-3 bit/char [[1]](https://330k.github.io/misc_tools/unicode_steganography.html) |

**State of the art:** Popular for CTF challenges and document fingerprinting. Easily detected by regex or Unicode inspection tools.

**Production readiness:** Experimental
Widely used for document watermarking and leak detection; no formal standard.

**Implementations:**
- [zwsp-steg-js](https://github.com/offdev/zwsp-steg-js) ⭐ 153 — JavaScript, encode/decode hidden messages using zero-width spaces

**Security status:** Caution
Invisible to readers but trivially detected with a Unicode code-point dump or simple regex filter.

**Community acceptance:** Widely trusted
Standard technique in CTF competitions and document-leak tracking; broadly understood.

---

### Homoglyphs

**Goal:** Hide data using visually identical characters from different scripts.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Homoglyphs** | 2000 | Cyrillic а→a, Greek ο→o | 1 bit/char [[1]](https://link.springer.com/chapter/10.1007/978-3-319-22915-7_26) |

**State of the art:** "Dual Stage Text Steganography Using Unicode Homoglyphs" (SSCC 2015, Hosmani et al.) is the key academic reference. Visually indistinguishable but detectable via Unicode script analysis.

**Production readiness:** Experimental
Used for document fingerprinting and leak detection in practice; no standardised library.

**Implementations:**
- [stegtext](https://github.com/btimby/stegtext) ⭐ 3 — Python, homoglyph substitution steganography

**Security status:** Caution
Detected by Unicode normalization, script-mixing analysis, or copy-paste into an ASCII-only context.

**Community acceptance:** Niche
Recognised in security research and CTF; practical use is mainly document watermarking.

---

## Semantic Methods

---

### Chaffing and Winnowing

**Goal:** Separate authentic from chaff messages.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chaffing** | 1998 | MAC authentication | Rivest [[1]](https://people.csail.mit.edu/rivest/pubs/Riv98a.prepub.txt) |

**State of the art:** Ron Rivest's 1998 paper "Chaffing and Winnowing: Confidentiality without Encryption" remains the definitive reference. Unique authentication-based approach that achieves confidentiality without traditional encryption.

**Production readiness:** Mature
Well-studied theoretical technique; practical implementations exist but niche.

**Security status:** Secure
Security rests on the MAC; an attacker without the key cannot distinguish wheat from chaff.

**Community acceptance:** Widely trusted
Peer-reviewed, broadly cited in cryptography literature; recognised by Bruce Schneier and others.

---

### Mimic Functions

**Goal:** Generate text that encodes secret data using grammar rules.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Mimic Functions** | 1992 | CFG where generated text encodes bits | Wayner [[1]](https://www.tandfonline.com/doi/abs/10.1080/0161-119291866883) |

**State of the art:** Peter Wayner's 1992 Cryptologia paper is the canonical reference. SpamMimic (spammimic.com) is the best-known practical demonstration. Text often sounds unnatural; largely superseded by LLM-based methods.

**Production readiness:** Deprecated
Superseded by neural generative methods; SpamMimic is still online but purely for demonstration.

**Implementations:**
- [SpamMimic](https://www.spammimic.com/) — online demo, encodes messages as spam-like text (original Wayner CFG approach)

**Security status:** Broken
Generated text is statistically detectable as machine-generated; structural patterns are obvious to modern classifiers.

**Community acceptance:** Niche
Historically important as the first generative steganography approach; cited in every linguistic steganography survey.

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
| **ChatStega** | 2024 | Sampling with different top-p/temperature in ChatGPT [[1]](https://dl.acm.org/doi/10.1145/3664476.3670930) |

**State of the art:** "Natural Language Steganography by ChatGPT" (ARES 2024, Steinebach) demonstrates using ChatGPT 4.0 to generate stego covers. Simple but depends on LLM sampling randomness.

**Production readiness:** Experimental
Demonstrated in academic paper; no production tooling.

**Security status:** Caution
Detectable with access to the sampling seed or when stego covers are compared statistically against normal ChatGPT output.

**Community acceptance:** Emerging
Growing interest in practical LLM steganography; limited peer review so far.

---

### Blog-Steganography

**Goal:** Hide messages in blog comments across the internet.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Blog-Stego** | 2011 | Fractionalized + blog selection | Key = blog set [[1]](https://en.wikipedia.org/wiki/List_of_steganography_techniques) [[2]](https://cacm.acm.org/magazines/2014/3/172511-trends-in-steganography/fulltext) |

**State of the art:** Described in the steganography techniques literature and surveyed in "Trends in Steganography" (CACM 2014); encrypted message fragments are posted as comments on pre-agreed orphaned blogs, with the set of blogs acting as the symmetric key.

**Production readiness:** Experimental
No known production implementation; described as a concept in surveys.

**Security status:** Secure
Distributed nature makes traffic analysis hard; security relies on key (blog set) secrecy and encryption of payload.

**Community acceptance:** Niche
Mentioned in academic surveys; no tooling or adoption beyond conceptual description.

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

---

### Addressing Tokenization Inconsistency

**Goal:** Address tokenization inconsistency between steganography sender and receiver in LLM-based methods.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Addressing Tokenization Inconsistency** | 2025 | Resolves tokenization discrepancies between encoder/decoder in LLM steganography [[1]](https://arxiv.org/abs/2508.20718) |

**State of the art:** Proposes tokenization alignment methods for reliable message extraction.

**Production readiness:** Research

**Security status:** Caution — Requires synchronized tokenizers

**Community acceptance:** Emerging
