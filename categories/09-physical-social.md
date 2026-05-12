# Physical & Social Steganography

<!-- TOC -->
## Contents (13 algorithms)

**[Physical Methods](#physical-methods)**
- [Morse Code Yarn](#morse-code-yarn)
- [Music Cipher](#music-cipher)
- [Printer Steganography](#printer-steganography)
- [Microdots](#microdots)
- [Invisible Ink](#invisible-ink)
- [Cyber-Physical Steganography](#cyber-physical-steganography)
- [Polarization Steganography](#polarization-steganography)
- [POSERS](#posers-dna-molecular-tagging)

**[Social Steganography](#social-steganography)**
- [Cultural References](#cultural-references)
- [Contextual Hiding](#contextual-hiding)
- [Steganography in Game Actions](#steganography-in-game-actions)

**[Recent arXiv Papers (2024–2026)](#recent-arxiv-papers-20242026)**
- [Pulsed Waveforms and Intermittently Nonlinear Filtering in S...](#pulsed-waveforms-and-intermittently-nonlinear-filtering-in-synthesis-of-low-snr-and-covert-communications)

**[Visual / Esoteric Languages](#visual-esoteric-languages)**
- [Piet / npiet Online](#piet-npiet-online)
<!-- /TOC -->

## Physical Methods

---

### Morse Code Yarn

**Goal:** Hide messages in knitted clothing using Morse code patterns.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Morse Yarn** | 1940s | Knit/purl stitches encode Morse dots/dashes | WWII spy technique [[1]](https://www.bbc.com/future/article/20170315-the-women-who-knitted-secret-messages-in-wartime) |

**State of the art:** Historical method; documented WWII intelligence technique.

**Production readiness:** Deprecated
Historical technique; no modern deployment.

**Security status:** Caution — Detectable by those aware of the encoding convention

**Community acceptance:** Niche — Historical curiosity

---

### Music Cipher

**Goal:** Hide messages by encoding them in musical note pitches or rhythms.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Music Cipher** | 1560s | Note pitch/rhythm encodes alphabet | Historical; used by Gustavus Selenus [[1]](https://www.cryptomuseum.com/crypto/music/index.htm) |

**State of the art:** Historical technique; modern digital audio steganography supersedes it. See [03-audio-steganography.md](03-audio-steganography.md).

**Production readiness:** Deprecated
Historical technique only.

**Security status:** Caution — Detectable by musical analysis

**Community acceptance:** Niche — Historical curiosity

---

### Printer Steganography

**Goal:** Track documents via hidden dots.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Printer Dots** | 2005 | Yellow dot matrix | Serial + timestamp |

**State of the art:** Standard in color laser printers.

**Production readiness:** Production

**Implementations:**
- [Printer Steganography Detector](https://github.com/abe-modyo/printer-steganography) ⭐ 89

**Security status:** Broken — Documented tracking

**Community acceptance:** Standard — Well-documented

---

### Microdots

**Goal:** Hide microscopic images or text in documents, reduced photographically to dot size.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Microdots** | 1870s | Photographic reduction to ~1mm dot | WWII intelligence use; documented by FBI [[1]](https://www.fbi.gov/history/famous-cases/hollow-nickel-case-rudolf-abel) |

**State of the art:** Historical spy technique; superseded by digital steganography.

**Production readiness:** Deprecated
No modern practical application; purely historical.

**Security status:** Caution — Detectable under magnification

**Community acceptance:** Niche — Historical intelligence technique

---

### Invisible Ink

**Goal:** Hidden writing revealed only under specific conditions (heat, UV, chemical reaction).

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Invisible Ink** | ~50 BCE | Chemical or physical concealment; revealed by heat/UV/reagent | Ancient technique; documented from Pliny the Elder [[1]](https://www.sciencehistory.org/stories/magazine/the-chemistry-of-invisible-ink/) |

**State of the art:** Historical method; still used in novelty and educational contexts.

**Production readiness:** Deprecated
No serious operational use; superseded by digital methods.

**Security status:** Caution — Detectable under UV or chemical testing

**Community acceptance:** Niche — Historical and educational use only

---

### Cyber-Physical Steganography

**Goal:** Hide information in robotic motion control systems as a new steganographic medium.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Cyber-Physical** | 2025 | Robotic motion trajectory encodes secret data | Chang et al. arXiv 2025 [[1]](https://arxiv.org/abs/2501.04541) |

**State of the art:** First steganography paradigm using robotic motion as the carrier medium.

**Production readiness:** Research
Preprint January 2025; laboratory concept only.

**Security status:** Caution — Novel medium; detection methods not yet studied

**Community acceptance:** Emerging — Very recent paradigm

---

## Social Steganography

---

### Cultural References

**Goal:** Hide meaning in cultural symbols, memes, or shared references understood only by intended recipients.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Cultural References** | 2013 | Pop culture symbols encode meaning | boyd & Marwick 2011 social steganography [[1]](https://www.danah.org/papers/2011/SocialSteganography-Draft.pdf) |

**State of the art:** Active in censored communities; documented in social media research.

**Production readiness:** Production
Actively used in censored regions (China, Iran) for covert communication.

**Security status:** Secure — No technical detection possible; requires cultural context

**Community acceptance:** Standard — Active in censored communities; academically documented

---

### Contextual Hiding

**Goal:** Hide messages in contextual meaning via idioms, memes, or coded language visible only to initiates.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Contextual Hiding** | 2013 | Idioms, memes, coded language | Social steganography; Marwick & boyd 2014 [[1]](https://doi.org/10.1080/1369118X.2014.943249) |

**State of the art:** Used in protest movements and censored communities worldwide.

**Production readiness:** Production
Actively used in real-world covert communication.

**Security status:** Secure — No technical detection; requires insider cultural knowledge

**Community acceptance:** Standard — Active in censored communities; peer-reviewed social media research

---

### Polarization Steganography

**Goal:** Hide information using polarization states of partially polarized vector beams on the Poincaré sphere.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Polarization Steganography** | 2026 | Spatially dependent polarization structure of vector beam | Physical layer security [[1]](https://arxiv.org/abs/2603.11427) |

**State of the art:** Novel approach using Poincaré sphere polarization engineering; information retrieved by spatially resolved polarization analysis.

**Production readiness:** Research
Laboratory demonstration only; preprint March 2026.

**Implementations:** Laboratory prototypes only

**Security status:** Caution — Novel medium; detection by polarimetric analysis not yet characterized

**Community acceptance:** Emerging — Very recent optical steganography concept

---

### POSERS (DNA Molecular Tagging)

**Goal:** Molecular tagging using randomized DNA sequences for anti-counterfeiting steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **POSERS** | 2025 | Steganography-driven randomized DNA sequence encoding | Tafazoli Yazdi et al. [[1]](https://arxiv.org/abs/2503.00638) |

**State of the art:** Uses random DNA sequences for enhanced security against replication via sequencing; addresses vulnerability of predefined-sequence DNA tags.

**Production readiness:** Experimental
Preprint March 2025; laboratory prototype stage.

**Implementations:** Research prototypes only

**Security status:** Caution — Secure against sequencing-based replication; physical security depends on DNA synthesis access

**Community acceptance:** Emerging — Novel molecular steganography paradigm

---

### Steganography in Game Actions

**Goal:** Hide information within video game actions and mechanics as a novel steganographic medium.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Game Actions** | 2025 | Gameplay mechanics encode secret data | Chang & Echizen, IEEE Access 2025 [[1]](https://doi.org/10.1109/ACCESS.2025.3530961) |

**State of the art:** Novel concept using video game actions as information carrier; addresses the evolutionary interplay between steganography and steganalysis via new medium.

**Production readiness:** Research
IEEE Access 2025; concept demonstration only.

**Implementations:** None yet

**Security status:** Caution — Novel medium; no known detection methods yet, but also no formal security analysis

**Community acceptance:** Emerging — Very recent; peer-reviewed IEEE Access publication

## Recent arXiv Papers (2024–2026)

---

### Pulsed Waveforms and Intermittently Nonlinear Filtering in Synthesis of Low-SNR and Covert Communications

**Goal:** signal (e.g. to reduce the burden on the power amplifier), and/or made statistically indistinguishable from Gaussian noise (e.g.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Pulsed Waveforms and Intermittently Nonlinear Filtering in S** | 2020 | eess.SP | Alexei V. Nikitin, Ruslan L. Davidchack [[1]](https://arxiv.org/abs/2008.06390) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

## Visual / Esoteric Languages

---

### Piet / npiet Online

**Goal:** Execute programs encoded as bitmap images using the Piet esoteric programming language, where color transitions encode instructions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Piet** | 2001 | Color-based esoteric language; images = programs | Programs look like abstract art [[1]](https://www.bertnase.de/npiet/npiet-execute.php) [[2]](http://www.dangermouse.net/esoteric/piet.html) |

**State of the art:** Niche but recognizable CTF technique. Secret messages can be programs encoded as abstract images; requires npiet or similar interpreter to run.

**Production readiness:** Research
Academic curiosity; no production applications.

**Security status:** Caution
Trivially identified by anyone aware of Piet language; security by obscurity only.

**Community acceptance:** Niche
Recognized in CTF community; occasionally used in stego-style challenges.

---

