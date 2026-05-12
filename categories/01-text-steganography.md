# Text Steganography

<!-- TOC -->
## Contents (3 algorithms)

**[Structural Methods](#structural-methods)**
- [Whitespace coding](#whitespace-coding)
- [Zero-width Unicode](#zero-width-unicode)
- [Homoglyphs](#homoglyphs)

**[Semantic Methods](#semantic-methods)**
- [Mimic Functions](#mimic-functions)

**[LLM-Based Methods](#llm-based-methods)**
- [Meteor](#meteor)
- [Discop](#discop)
- [ChatStega](#chatstega)
<!-- /TOC -->

## Structural Methods

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
