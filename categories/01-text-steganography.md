# Text Steganography

<!-- TOC -->
## Contents (3 algorithms)

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
