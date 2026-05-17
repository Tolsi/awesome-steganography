# Text Steganography

<!-- TOC -->
## Contents (158 algorithms)

**[Structural Methods](#structural-methods)**
- [ASCII Art Steganography](#ascii-art-steganography)
- [Word Change Tracking](#word-change-tracking)
- [Bacon's Cipher](#bacons-cipher)
- [Null Cipher](#null-cipher)
- [Whitespace Coding](#whitespace-coding)
- [Zero-width Unicode](#zero-width-unicode)
- [Homoglyphs](#homoglyphs)
- [Inter-letter Spacing](#inter-letter-spacing)
- [DataGlyphs / GlyphCode](#dataglyphs-glyphcode)

**[Semantic Methods](#semantic-methods)**
- [Chaffing and Winnowing](#chaffing-and-winnowing)
- [Mimic Functions](#mimic-functions)

**[LLM-Based Methods](#llm-based-methods)**
- [Meteor](#meteor)
- [Discop](#discop)
- [ChatStega](#chatstega)
- [Blog-Steganography](#blog-steganography)
- [Range Coding](#range-coding)
- [Anchored Sliding Window (ASW)](#anchored-sliding-window-asw)
- [ReTokSync](#retoksync)
- [Entropy-Driven Rank-Token Mapping](#entropy-driven-rank-token-mapping)
- [Auto-Stega](#auto-stega)
- [Dynamic Codebook](#dynamic-codebook)
- [OD-Stega](#od-stega)
- [Shifting-Merging](#shifting-merging)
- [Semantic Steganography (LLM)](#semantic-steganography-llm)
- [Content-Preserving Linguistic Steganography](#content-preserving-linguistic-steganography)
- [Raster Domain Text Steganography](#raster-domain-text-steganography)
- [Alkaid (Provably Secure Steganography)](#alkaid-provably-secure-steganography)
- [SparSamp (Sparse Sampling)](#sparsamp-sparse-sampling)
- [Kolmogorov Complexity Bounds](#kolmogorov-complexity-bounds)
- [STEAD (Robust Provably Secure Linguistic Steganography)](#stead-robust-provably-secure-linguistic-steganography)
- [Hide and Seek in Embedding Space](#hide-and-seek-in-embedding-space)
- [StegoStylo](#stegostylo)
- [Undetectable Conversations](#undetectable-conversations)
- [TrojanStego](#trojanstego)
- [GTSD (Generative Text Steganography via Diffusion)](#gtsd-generative-text-steganography-via-diffusion)
- [Provably Secure Steganography Based on List Decoding](#provably-secure-steganography-based-on-list-decoding)
- [Addressing Tokenization Inconsistency](#addressing-tokenization-inconsistency)
- [Safeguarding LLMs Against Misuse and AI-Driven Malware Using Steganographic Canaries](#safeguarding-llms-against-misuse-and-ai-driven-malware-using-steganographic-canaries)
- [A Decision-Theoretic Formalisation of Steganography With Applications to LLM Monitoring](#a-decision-theoretic-formalisation-of-steganography-with-applications-to-llm-monitoring)
- [AndroWasm: an Empirical Study on Android Malware Obfuscation through WebAssembly](#androwasm-an-empirical-study-on-android-malware-obfuscation-through-webassembly)
- [Verifying LLM Inference to Detect Model Weight Exfiltration](#verifying-llm-inference-to-detect-model-weight-exfiltration)
- [Plug-and-Hide: Provable and Adjustable Diffusion Generative Steganography](#plug-and-hide-provable-and-adjustable-diffusion-generative-steganography)
- [Odysseus: Jailbreaking Commercial Multimodal LLM-integrated Systems via Dual Steganography](#odysseus-jailbreaking-commercial-multimodal-llm-integrated-systems-via-dual-steganography)
- [Defining Cost Function of Steganography with Large Language Models](#defining-cost-function-of-steganography-with-large-language-models)
- [A High-Capacity and Secure Disambiguation Algorithm for Neural Linguistic Steganography](#a-high-capacity-and-secure-disambiguation-algorithm-for-neural-linguistic-steganography)
- [Invisible Injections: Exploiting Vision-Language Models Through Steganographic Prompt Embedding](#invisible-injections-exploiting-vision-language-models-through-steganographic-prompt-embedding)
- [Singularity Cipher: A Topology-Driven Cryptographic Scheme Based on Visual Paradox and Klein Bottle Illusions](#singularity-cipher-a-topology-driven-cryptographic-scheme-based-on-visual-paradox-and-klein-bottle-illusions)
- [Favicon Trojans: Executable Steganography Via Ico Alpha Channel Exploitation](#favicon-trojans-executable-steganography-via-ico-alpha-channel-exploitation)
- [Early Signs of Steganographic Capabilities in Frontier LLMs](#early-signs-of-steganographic-capabilities-in-frontier-llms)
- [Efficient Blockchain-based Steganography via Backcalculating Generative Adversarial Network](#efficient-blockchain-based-steganography-via-backcalculating-generative-adversarial-network)
- [Mixing Algorithm for Extending the Tiers of the Unapparent Information Send through the Audio Streams](#mixing-algorithm-for-extending-the-tiers-of-the-unapparent-information-send-through-the-audio-streams)
- [Steganography and Probabilistic Risk Analysis: A Game Theoretical Framework for Quantifying Adversary Advantage and Impact](#steganography-and-probabilistic-risk-analysis-a-game-theoretical-framework-for-quantifying-adversary-advantage-and-impact)
- [Hidden in Plain Text: Emergence & Mitigation of Steganographic Collusion in LLMs](#hidden-in-plain-text-emergence-mitigation-of-steganographic-collusion-in-llms)
- [Secret Collusion among AI Agents: Multi-Agent Deception via Steganography](#secret-collusion-among-ai-agents-multi-agent-deception-via-steganography)
- [Provably Robust and Secure Steganography in Asymmetric Resource Scenario](#provably-robust-and-secure-steganography-in-asymmetric-resource-scenario)
- [Image steganography based on generative implicit neural representation](#image-steganography-based-on-generative-implicit-neural-representation)
- [On the Steganographic Capacity of Selected Learning Models](#on-the-steganographic-capacity-of-selected-learning-models)
- [Introducing a New Evaluation Criteria for EMD-Base Steganography Method](#introducing-a-new-evaluation-criteria-for-emd-base-steganography-method)
- [Open Image Content Disarm And Reconstruction](#open-image-content-disarm-and-reconstruction)
- [Deep Cross-Modal Steganography Using Neural Representations](#deep-cross-modal-steganography-using-neural-representations)
- [Errorless Robust JPEG Steganography Using Steganographic Polar Codes](#errorless-robust-jpeg-steganography-using-steganographic-polar-codes)
- [Off-By-One Implementation Error in J-UNIWARD](#off-by-one-implementation-error-in-j-uniward)
- [The Realizations of Steganography in Encrypted Domain](#the-realizations-of-steganography-in-encrypted-domain)
- [ICStega: Image Captioning-based Semantically Controllable Linguistic Steganography](#icstega-image-captioning-based-semantically-controllable-linguistic-steganography)
- [Steganography of Steganographic Networks](#steganography-of-steganographic-networks)
- [A New Paradigm for Improved Image Steganography by using Adaptive Number of Dominant Discrete Cosine Transform Coefficients](#a-new-paradigm-for-improved-image-steganography-by-using-adaptive-number-of-dominant-discrete-cosine-transform-coefficients)
- [Blind Spots: Automatically detecting ignored program inputs](#blind-spots-automatically-detecting-ignored-program-inputs)
- [Image data hiding with multi-scale autoencoder network](#image-data-hiding-with-multi-scale-autoencoder-network)
- [SABMIS: Sparse approximation based blind multi-image steganography scheme](#sabmis-sparse-approximation-based-blind-multi-image-steganography-scheme)
- [A Brief Survey on Deep Learning Based Data Hiding](#a-brief-survey-on-deep-learning-based-data-hiding)
- [IoTSign: Protecting Privacy and Authenticity of IoT using Discrete Cosine Based Steganography](#iotsign-protecting-privacy-and-authenticity-of-iot-using-discrete-cosine-based-steganography)
- [Generating Steganographic Images via Adversarial Training](#generating-steganographic-images-via-adversarial-training)
- [A New Approach to SMS Steganography using Mathematical Equations](#a-new-approach-to-sms-steganography-using-mathematical-equations)
- [Natural Steganography: cover-source switching for better steganography](#natural-steganography-cover-source-switching-for-better-steganography)
- [High Capacity Image Steganography using Adjunctive Numerical Representations with Multiple Bit-Plane Decomposition Methods](#high-capacity-image-steganography-using-adjunctive-numerical-representations-with-multiple-bit-plane-decomposition-methods)
- [Steganography -- A Game of Hide and Seek in Information Communication](#steganography-a-game-of-hide-and-seek-in-information-communication)
- [Secure Image Steganography using Cryptography and Image Transposition](#secure-image-steganography-using-cryptography-and-image-transposition)
- [Steganography and Broadcasting](#steganography-and-broadcasting)
- [A Novel Approach for Image Steganography in Spatial Domain](#a-novel-approach-for-image-steganography-in-spatial-domain)
- [Using Facebook for Image Steganography](#using-facebook-for-image-steganography)
- [PDF Steganography based on Chinese Remainder Theorem](#pdf-steganography-based-on-chinese-remainder-theorem)
- [A Low-throughput Wavelet-based Steganography Audio Scheme](#a-low-throughput-wavelet-based-steganography-audio-scheme)
- [Environment Based Secure Transfer of Data in Wireless Sensor Networks](#environment-based-secure-transfer-of-data-in-wireless-sensor-networks)
- [A Secure Cyclic Steganographic Technique for Color Images using Randomization](#a-secure-cyclic-steganographic-technique-for-color-images-using-randomization)
- [How to Bootstrap Anonymous Communication](#how-to-bootstrap-anonymous-communication)
- [A Secure Electronic Prescription System Using Steganography with Encryption Key Implementation](#a-secure-electronic-prescription-system-using-steganography-with-encryption-key-implementation)
- [Steganography in Modern Smartphones and Mitigation Techniques](#steganography-in-modern-smartphones-and-mitigation-techniques)
- [StegExpose - A Tool for Detecting LSB Steganography](#stegexpose-a-tool-for-detecting-lsb-steganography)
- [An Approach for Text Steganography Based on Markov Chains](#an-approach-for-text-steganography-based-on-markov-chains)
- [High Security Image Steganography with Modified Arnold cat map](#high-security-image-steganography-with-modified-arnold-cat-map)
- [Reversible and Irreversible Data Hiding Technique](#reversible-and-irreversible-data-hiding-technique)
- [Steganography -- coding and intercepting the information from encoded pictures in the absence of any initial information](#steganography-coding-and-intercepting-the-information-from-encoded-pictures-in-the-absence-of-any-initial-information)
- [A Study of Various Steganographic Techniques Used for Information Hiding](#a-study-of-various-steganographic-techniques-used-for-information-hiding)
- [Dual Layer Textual Message Cryptosystem with Randomized Sequence of Symmetric Key](#dual-layer-textual-message-cryptosystem-with-randomized-sequence-of-symmetric-key)
- [Robust Steganography Using LSB-XOR and Image Sharing](#robust-steganography-using-lsb-xor-and-image-sharing)
- [Steganography using the Extensible Messaging and Presence Protocol (XMPP)](#steganography-using-the-extensible-messaging-and-presence-protocol-xmpp)
- [Comparison of secure and high capacity color image steganography techniques in RGB and YCbCr domains](#comparison-of-secure-and-high-capacity-color-image-steganography-techniques-in-rgb-and-ycbcr-domains)
- [A Novel Steganography Algorithm for Hiding Text in Image using Five Modulus Method](#a-novel-steganography-algorithm-for-hiding-text-in-image-using-five-modulus-method)
- [Enhanced Tiny Encryption Algorithm with Embedding (ETEA)](#enhanced-tiny-encryption-algorithm-with-embedding-etea)
- [One Time Pad Password Protection: Using T.E.C. Steganography and Secure Password Transmission Protocols](#one-time-pad-password-protection-using-tec-steganography-and-secure-password-transmission-protocols)
- [Image Steganography based on a Parameterized Canny Edge Detection Algorithm](#image-steganography-based-on-a-parameterized-canny-edge-detection-algorithm)
- [Image Steganography Method Based on Brightness Adjustment](#image-steganography-method-based-on-brightness-adjustment)
- [An Authentication Technique in Frequency Domain through Wavelet Transform (ATFDWT)](#an-authentication-technique-in-frequency-domain-through-wavelet-transform-atfdwt)
- [A Text Steganography Method Using Pangram and Image Mediums](#a-text-steganography-method-using-pangram-and-image-mediums)
- [A Lossless Data Hiding Technique based on AES-DWT](#a-lossless-data-hiding-technique-based-on-aes-dwt)
- [A Generation-based Text Steganography Method using SQL Queries](#a-generation-based-text-steganography-method-using-sql-queries)
- [An Image Steganography Scheme using Randomized Algorithm and Context-Free Grammar](#an-image-steganography-scheme-using-randomized-algorithm-and-context-free-grammar)
- [Embedding grayscale halftone pictures in QR Codes using Correction Trees](#embedding-grayscale-halftone-pictures-in-qr-codes-using-correction-trees)
- [Some New Methodologies for Image Hiding using Steganographic Techniques](#some-new-methodologies-for-image-hiding-using-steganographic-techniques)
- [Public key Steganography Using Discrete Cross-Coupled Chaotic Maps](#public-key-steganography-using-discrete-cross-coupled-chaotic-maps)
- [Multimedia Steganographic Scheme using Multiresolution Analysis](#multimedia-steganographic-scheme-using-multiresolution-analysis)
- [Security Architecture for Cluster based Ad Hoc Networks](#security-architecture-for-cluster-based-ad-hoc-networks)
- [Pixastic: Steganography based Anti-Phihsing Browser Plug-in](#pixastic-steganography-based-anti-phihsing-browser-plug-in)
- [A Survey on Various Data Hiding Techniques and their Comparative Analysis](#a-survey-on-various-data-hiding-techniques-and-their-comparative-analysis)
- [Text Steganography using LSB insertion method along with Chaos Theory](#text-steganography-using-lsb-insertion-method-along-with-chaos-theory)
- [Genetic Algorithm to Make Persistent Security and Quality of Image in Steganography from RS Analysis](#genetic-algorithm-to-make-persistent-security-and-quality-of-image-in-steganography-from-rs-analysis)
- [Experimenting with the Novel Approaches in Text Steganography](#experimenting-with-the-novel-approaches-in-text-steganography)
- [A Frequency Domain Steganography using Z Transform (FDSZT)](#a-frequency-domain-steganography-using-z-transform-fdszt)
- [Influence of Speech Codecs Selection on Transcoding Steganography](#influence-of-speech-codecs-selection-on-transcoding-steganography)
- [Information Hiding in CSS : A Secure Scheme Text-Steganography using Public Key Cryptosystem](#information-hiding-in-css-a-secure-scheme-text-steganography-using-public-key-cryptosystem)
- [Windtalking Computers: Frequency Normalization, Binary Coding Systems and Encryption](#windtalking-computers-frequency-normalization-binary-coding-systems-and-encryption)
- [Randomness Efficient Steganography](#randomness-efficient-steganography)
- [Chaotic iterations for steganography: Stego-security and topological-security](#chaotic-iterations-for-steganography-stego-security-and-topological-security)
- [Steganography Algorithm to Hide Secret Message inside an Image](#steganography-algorithm-to-hide-secret-message-inside-an-image)
- [Steganography: a Class of Algorithms having Secure Properties](#steganography-a-class-of-algorithms-having-secure-properties)
- [Steganography: a class of secure and robust algorithms](#steganography-a-class-of-secure-and-robust-algorithms)
- [Using Transcoding for Hidden Communication in IP Telephony](#using-transcoding-for-hidden-communication-in-ip-telephony)
- [Applying statistical methods to text steganography](#applying-statistical-methods-to-text-steganography)
- [An Approach for Message Hiding using Substitution Techniques and Audio Hiding in Steganography](#an-approach-for-message-hiding-using-substitution-techniques-and-audio-hiding-in-steganography)
- [Digital Forensics Analysis of Spectral Estimation Methods](#digital-forensics-analysis-of-spectral-estimation-methods)
- [Is Cloud Computing Steganography-proof?](#is-cloud-computing-steganography-proof)
- [Lost Audio Packets Steganography: The First Practical Evaluation](#lost-audio-packets-steganography-the-first-practical-evaluation)
- [Wet paper codes and the dual distance in steganography](#wet-paper-codes-and-the-dual-distance-in-steganography)
- [Hiding Secret Information in Movie Clip: A Steganographic Approach](#hiding-secret-information-in-movie-clip-a-steganographic-approach)
- [On Steganography in Lost Audio Packets](#on-steganography-in-lost-audio-packets)
- [Bio-Authentication based Secure Transmission System using Steganography](#bio-authentication-based-secure-transmission-system-using-steganography)
- [Improved information security using robust Steganography system](#improved-information-security-using-robust-steganography-system)
- [Overview: Main Fundamentals for Steganography](#overview-main-fundamentals-for-steganography)
- [New System for Secure Cover File of Hidden Data in the Image Page within Executable File Using Statistical Steganography Techniques](#new-system-for-secure-cover-file-of-hidden-data-in-the-image-page-within-executable-file-using-statistical-steganography-techniques)
- [M-Banking Security - a futuristic improved security approach](#m-banking-security-a-futuristic-improved-security-approach)
- [A Steganography Based on CT-CDMA Communication Scheme Using Complete Complementary Codes](#a-steganography-based-on-ct-cdma-communication-scheme-using-complete-complementary-codes)
- [Frame Selected Approach for Hiding Data within MPEG Video Using Bit Plane Complexity Segmentation](#frame-selected-approach-for-hiding-data-within-mpeg-video-using-bit-plane-complexity-segmentation)
- [Steganography An Art of Hiding Data](#steganography-an-art-of-hiding-data)
- [An approach to secure highly confidential documents of any size in the corporate or institutes having unsecured networks](#an-approach-to-secure-highly-confidential-documents-of-any-size-in-the-corporate-or-institutes-having-unsecured-networks)
- [A novel approach for implementing Steganography with computing power obtained by combining Cuda and Matlab](#a-novel-approach-for-implementing-steganography-with-computing-power-obtained-by-combining-cuda-and-matlab)
- [Efficient Steganography with Provable Security Guarantees](#efficient-steganography-with-provable-security-guarantees)
- [A Performance Analysis of HICCUPS - a Steganographic System for WLAN](#a-performance-analysis-of-hiccups-a-steganographic-system-for-wlan)
- [Hiding Information in Retransmissions](#hiding-information-in-retransmissions)
- [Using Kolmogorov Complexity for Understanding Some Limitations on Steganography](#using-kolmogorov-complexity-for-understanding-some-limitations-on-steganography)
- [Capacity of Steganographic Channels](#capacity-of-steganographic-channels)
- [TrustMAS: Trusted Communication Platform for Multi-Agent Systems](#trustmas-trusted-communication-platform-for-multi-agent-systems)
- [Image Steganography, a New Approach for Transferring Security Information](#image-steganography-a-new-approach-for-transferring-security-information)
- [Steganography from weak cryptography](#steganography-from-weak-cryptography)
- [Information Hiding Techniques: A Tutorial Review](#information-hiding-techniques-a-tutorial-review)
- [An Improved FPGA Implementation of the Modified Hybrid Hiding Encryption Algorithm (MHHEA) for Data Communication Security](#an-improved-fpga-implementation-of-the-modified-hybrid-hiding-encryption-algorithm-mhhea-for-data-communication-security)
- [Lightweight security mechanism for PSTN-VoIP cooperation](#lightweight-security-mechanism-for-pstn-voip-cooperation)
- [New security and control protocol for VoIP based on steganography and digital watermarking](#new-security-and-control-protocol-for-voip-based-on-steganography-and-digital-watermarking)
- [Content Based Image Retrieval with Mobile Agents and Steganography](#content-based-image-retrieval-with-mobile-agents-and-steganography)

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

### Inter-letter Spacing

**Goal:** Hide data using subtle micro-adjustments to kerning (inter-letter spacing).

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Inter-letter Spacing** | 2005 | ±0.1pt kerning shifts | Requires laser scanner with sub-pixel accuracy [[1]](https://www.researchgate.net/publication/216052617_DIGITAL_IMAGE_STEGANOGRAPHY) |

**State of the art:** Encodes bits by slightly adjusting spacing between letters. Requires specialized scanning equipment to read; visually imperceptible to humans.

**Production readiness:** Research
Requires specialized hardware for extraction; not practical for digital-only scenarios.

**Security status:** Caution
Very hard to detect without knowing the font and scanning equipment; practical implementations are rare.

**Community acceptance:** Niche
Academic curiosity; limited practical use due to hardware requirements.

---

### DataGlyphs / GlyphCode

**Goal:** Embed data using microscopic patterns in glyphs that appear as normal text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DataGlyphs** | 1998 | Xerox micro-patterns in glyphs | Looks like normal font, decoded by special software [[1]](https://www.researchgate.net/publication/1005499_DataGlyphs_Embedding_Byte_Streams_in_the_Visual_Appearance_of_Prints_of_Text_and_Graphical_Forms) |
| **GlyphCode** | 2001 | PDF417 2D barcode variant | Text appears normal, embedded 2D barcode [[2]](https://patents.google.com/patent/US6285779A/en) |

**State of the art:** Xerox DataGlyphs encode data as microscopic line patterns within character shapes. GlyphCode uses PDF417-style encoding. Both appear as ordinary text to casual observers.

**Production readiness:** Deprecated
Xerox commercial products discontinued; now mainly historical interest.

**Security status:** Broken
Patterns are detectable under magnification; superseded by digital steganography.

**Community acceptance:** Niche
Historical technique; relevant for document forensics and anti-counterfeiting research.

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

### Safeguarding LLMs Against Misuse and AI-Driven Malware Using Steganographic Canaries

**Goal:** Detect unauthorized LLM processing using steganographic canary files embedded in documents.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Safeguarding LLMs Against Misuse and AI-Driven Malware Using** | 2026 | cs.CR | Md Raz et al. [[1]](https://arxiv.org/abs/2603.28655) |

**State of the art:** Novel framework using steganographic canaries (Mode A: symbolic encoding, Mode B: linguistic steganography with GPT-2) to detect unauthorized LLM processing. Achieves 100% detection under benign conditions, 97% under adversarial transforms. First systematic combination of symbolic and linguistic text steganography for canary documents.

**Production readiness:** Research
Academic prototype; proof-of-concept implementation available. No production deployment.

**Security status:** Caution
Theoretical framework; adversarial robustness validated empirically but not independently verified.

**Community acceptance:** Emerging
Preprint; published at arXiv March 2026; peer review status unknown.

---

### A Decision-Theoretic Formalisation of Steganography With Applications to LLM Monitoring

**Goal:** Formalize steganography detection using decision theory and V-information to detect covert communication in LLMs.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Decision-Theoretic Formalisation of Steganography With App** | 2026 | cs.AI, cs.CL, cs.CR | Usman Anwar et al. [[1]](https://arxiv.org/abs/2602.23163) |

**State of the art:** Introduces "steganographic gap" measure quantifying asymmetry between agents who can/cannot decode hidden content. Formal framework for detecting steganographic reasoning in LLMs without requiring known reference distributions.

**Production readiness:** Research
Academic framework; no production implementation.

**Security status:** Secure — Theoretical framework with formal guarantees

**Community acceptance:** Emerging
Preprint; multiple revisions (v3); strong theoretical contribution to LLM monitoring.

---

### AndroWasm: an Empirical Study on Android Malware Obfuscation through WebAssembly

**Goal:** Investigate WebAssembly as a novel technique for hiding malicious payloads in Android apps.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **AndroWasm: an Empirical Study on Android Malware Obfuscation** | 2026 | cs.CR | Diego Soi et al. [[1]](https://arxiv.org/abs/2602.18082) |

**State of the art:** Empirical study demonstrating WebAssembly-based malware obfuscation in Android. Proof-of-concept evades VirusTotal and MobSF detection. Focuses on executable steganography rather than linguistic methods.

**Production readiness:** Research
Proof-of-concept; defensive countermeasures not yet developed.

**Security status:** Caution
Demonstrates practical attack vector; detection methods needed.

**Community acceptance:** Emerging
Academic study; no production implications for text steganography.

---

### Verifying LLM Inference to Detect Model Weight Exfiltration

**Goal:** Detect steganographic exfiltration of model weights from inference servers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Verifying LLM Inference to Detect Model Weight Exfiltration** | 2026 | cs.CR, cs.LG | Roy Rinberg et al. [[1]](https://arxiv.org/abs/2511.02620) |

**State of the art:** Formalizes model weight exfiltration as security game, proposes verification framework to detect steganographic attacks. Reduces exfiltratable information to <0.5% with <0.01% false positive rate on models up to 30B parameters.

**Production readiness:** Research
Open-source implementation available; practical deployment with minimal overhead.

**Security status:** Caution
Defense mechanism; effectiveness depends on trust assumptions specified in paper.

**Community acceptance:** Emerging
Published at arXiv Nov 2025; strong practical relevance for LLM providers.

---

### Plug-and-Hide: Provable and Adjustable Diffusion Generative Steganography

**Goal:** Diffusion model-based generative image steganography (DM-GIS) is an emerging paradigm that leverages the generative power of diffusion models to conceal secret messages without requiring pre-existi...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Plug-and-Hide: Provable and Adjustable Diffusion Generative ** | 2026 | cs.CR | Jiahao Zhu et al. [[1]](https://arxiv.org/abs/2409.04878) |

**State of the art:** Proposes dual steganography for embedding malicious queries/responses in images. Achieves up to 99% attack success rate against MLLM-integrated systems. Accepted at NDSS 2026.

**Production readiness:** Research
Academic research with extensive experiments; proof-of-concept level.

**Security status:** Caution
Demonstrates attack vector; security implications discussed.

**Community acceptance:** Emerging
Accepted at NDSS 2026; high-profile publication.

---

### Odysseus: Jailbreaking Commercial Multimodal LLM-integrated Systems via Dual Steganography

**Goal:** leading to a false sense of security in existing MLLM-integrated systems.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Odysseus: Jailbreaking Commercial Multimodal LLM-integrated ** | 2025 | cs.CR, cs.AI, cs.LG | Songze Li et al. [[1]](https://arxiv.org/abs/2512.20168) |

**State of the art:** First attempt at defining cost function of steganography with LLMs using two-stage strategy: LLM-guided program synthesis + evolutionary search. Published in IS&T Electronic Imaging 2026.

**Production readiness:** Research
Academic research with methodology; no production implementation.

**Security status:** Caution
Novel approach to cost function design; evaluated with steganalysis models.

**Community acceptance:** Emerging
Peer-reviewed publication; methodology may influence future designs.

---

### Defining Cost Function of Steganography with Large Language Models

**Goal:** In this paper, we make the first attempt towards defining cost function of steganography with large language models (LLMs), which is totally different from previous works that rely heavily on exper...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Defining Cost Function of Steganography with Large Language ** | 2025 | cs.CR | Hanzhou Wu, Yige Wang [[1]](https://arxiv.org/abs/2512.09769) |

**State of the art:** Proposes look-ahead Sync addressing SyncPool's capacity limitation while retaining provable security. Achieves >160% improvement in embedding rate in English, >25% in Chinese.

**Production readiness:** Experimental
Academic prototype with theoretical proofs; evaluated on Llama 3 and Qwen 2.5.

**Security status:** Secure
Retains provably secure guarantees from SyncPool.

**Community acceptance:** Emerging
Theoretical contribution to high-capacity PSS.

---

### A High-Capacity and Secure Disambiguation Algorithm for Neural Linguistic Steganography

**Goal:** Neural linguistic steganography aims to embed information into natural text while preserving statistical undetectability.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A High-Capacity and Secure Disambiguation Algorithm for Neur** | 2025 | cs.CL, cs.AI, cs.CR | Yapei Feng et al. [[1]](https://arxiv.org/abs/2510.02332) |

**State of the art:** Addresses tokenization ambiguity in neural linguistic steganography. Proposes look-ahead Sync overcoming SyncPool's capacity limitation while retaining provable security. Achieves >160% improvement in embedding rate in English, >25% in Chinese on Llama 3 and Qwen 2.5.

**Production readiness:** Experimental
Academic prototype with theoretical proofs; evaluated on real LLMs.

**Security status:** Secure
Retains provable security guarantees from SyncPool while improving capacity.

**Community acceptance:** Emerging
Strong theoretical contribution; actively cited in PSS literature.

---

### Invisible Injections: Exploiting Vision-Language Models Through Steganographic Prompt Embedding

**Goal:** steganographic methods, achieving an overall attack success rate of 24.3% (plus or minus 3.2%, 95% CI) across leading VLMs including GPT-4V, Claude, and LLaVA, with neural steganography methods rea...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invisible Injections: Exploiting Vision-Language Models Thro** | 2025 | cs.CR | Chetan Pathade [[1]](https://arxiv.org/abs/2507.22304) |

**State of the art:** First comprehensive study of steganographic prompt injection attacks against VLMs. Multi-domain embedding framework combining spatial, frequency, and neural steganography. Achieves 24.3% attack success rate (31.8% with neural methods) across GPT-4V, Claude, LLaVA with PSNR>38dB.

**Production readiness:** Research
Academic study; proof-of-concept implementation demonstrated.

**Security status:** Caution
Demonstrates practical attack vector; countermeasures proposed.

**Community acceptance:** Emerging
Novel attack vector; significant implications for VLM security.

---

### Singularity Cipher: A Topology-Driven Cryptographic Scheme Based on Visual Paradox and Klein Bottle Illusions

**Goal:** conventional ciphers that rely solely on algebraic complexity, the Singularity Cipher introduces a dual-layer approach: symbolic encryption rooted in topology and visual steganography designed for ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Singularity Cipher: A Topology-Driven Cryptographic Scheme B** | 2025 | cs.CR | Abraham Itzhak Weinberg [[1]](https://arxiv.org/abs/2507.21097) |

**State of the art:** Novel cryptographic-steganographic framework combining topological transformations with visual paradoxes (Klein bottle, missing square). Dual-layer approach: symbolic encryption rooted in topology + visual steganography for cognitive ambiguity.

**Production readiness:** Research
Theoretical framework with formal architecture; no implementation provided.

**Security status:** Caution
Novel theoretical approach; security properties require further analysis.

**Community acceptance:** Niche
Novel theoretical contribution; limited peer review to date.

---

### Favicon Trojans: Executable Steganography Via Ico Alpha Channel Exploitation

**Goal:** This paper presents a novel method of executable steganography using the alpha transparency layer of ICO image files to embed and deliver self-decompressing JavaScript payloads within web browsers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Favicon Trojans: Executable Steganography Via Ico Alpha Chan** | 2025 | cs.CR | David Noever, Forrest McKee [[1]](https://arxiv.org/abs/2507.09074) |

**State of the art:** Presents executable steganography using ICO alpha channel to embed JavaScript payloads. PoC demonstrates 512 bytes in 64x64 ICO, executed in memory on page load. Evades CSP and antivirus scanners. Targets 294B daily favicon requests.

**Production readiness:** Experimental
Proof-of-concept implementation demonstrated across desktop/mobile browsers.

**Security status:** Broken
Demonstrates practical attack vector; evades content security policies.

**Community acceptance:** Emerging
Security research with practical implications; significant attention.
Active research area; peer review in progress.

---

### Early Signs of Steganographic Capabilities in Frontier LLMs

**Goal:** Monitoring Large Language Model (LLM) outputs is crucial for mitigating risks from misuse and misalignment.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Early Signs of Steganographic Capabilities in Frontier LLMs** | 2025 | cs.CR, cs.AI, cs.CL | Artur Zolkowski et al. [[1]](https://arxiv.org/abs/2507.02737) |

**State of the art:** Blockchain-based steganography using backcalculating GAN for encoding covert data into blockchain transaction fields.

**Production readiness:** Research
Academic research; no production implementation.

**Security status:** Caution
Novel approach to blockchain steganography; not independently verified.

**Community acceptance:** Niche
Specialized application; limited peer review.

---

### Efficient Blockchain-based Steganography via Backcalculating Generative Adversarial Network

**Goal:** Blockchain-based steganography enables data hiding via encoding the covert data into a specific blockchain transaction field.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Efficient Blockchain-based Steganography via Backcalculating** | 2025 | cs.CR | Zhuo Chen et al. [[1]](https://arxiv.org/abs/2506.16023) |

**State of the art:** Proposes mixing algorithm for extending tiers of unapparent information transmission through audio streams.

**Production readiness:** Research
Academic research; no production implementation.

**Security status:** Caution
Novel audio steganography approach; theoretical analysis pending.

**Community acceptance:** Niche
Specialized audio application.

---

### Mixing Algorithm for Extending the Tiers of the Unapparent Information Send through the Audio Streams

**Goal:** the survival of the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Mixing Algorithm for Extending the Tiers of the Unapparent I** | 2025 | cs.CR | Sachith Dassanayaka [[1]](https://arxiv.org/abs/2502.12544) |

**State of the art:** Proposes mixing algorithm for extending data hiding tiers in audio streams. Focuses on message survival in covert communication scenarios.

**Production readiness:** Research
Conceptual framework; no implementation provided.

**Security status:** Caution
Theoretical approach; security analysis pending.

**Community acceptance:** Niche
Limited to audio steganography research.

---

### Steganography and Probabilistic Risk Analysis: A Game Theoretical Framework for Quantifying Adversary Advantage and Impact

**Goal:** enable the assessment of success rates, illustrating conditions under which the company benefits from hiding messages or faces increased risks when not implementing steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography and Probabilistic Risk Analysis: A Game Theore** | 2025 | cs.GT, cs.CR | Obinna Omego et al. [[1]](https://arxiv.org/abs/2412.17950) |

**State of the art:** Studies emergence and mitigation of steganographic collusion in LLMs for unsafe interactions.

**Production readiness:** Research
Analysis paper; no implementation.

**Security status:** Caution
Threat analysis; security implications discussed.

**Community acceptance:** Emerging
Active research on LLM collusion detection.

---

### Hidden in Plain Text: Emergence & Mitigation of Steganographic Collusion in LLMs

**Goal:** from unsafe interactions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hidden in Plain Text: Emergence & Mitigation of Steganograph** | 2025 | cs.CL, cs.CR, cs.LG | Yohan Mathew et al. [[1]](https://arxiv.org/abs/2410.03768) |

**State of the art:** Studies emergence and mitigation of steganographic collusion in LLMs for unsafe interactions. Analyzes how multiple LLMs can collude using steganography to evade detection.

**Production readiness:** Research
Analysis paper; no implementation.

**Security status:** Caution
Threat analysis; security implications discussed for LLM collusion.

**Community acceptance:** Emerging
Active research area on AI safety and collusion detection.

---

### Secret Collusion among AI Agents: Multi-Agent Deception via Steganography

**Goal:** the problem of secret collusion in systems of generative AI agents by drawing on relevant concepts from both AI and security literature.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secret Collusion among AI Agents: Multi-Agent Deception via ** | 2025 | cs.AI, cs.CR | Sumeet Ramesh Motwani et al. [[1]](https://arxiv.org/abs/2402.07510) |

**State of the art:** First systematic study of secret collusion among generative AI agents via steganography. Establishes threat model and explores detection countermeasures.

**Production readiness:** Research
Theoretical framework; no implementation.

**Security status:** Caution
Analysis of novel multi-agent attack vector.

**Community acceptance:** Emerging
Active research on AI agent security.

**Community acceptance:** Emerging
Theoretical contribution to PSS.

---

### Provably Robust and Secure Steganography in Asymmetric Resource Scenario

**Goal:** To circumvent the unbridled and ever-encroaching surveillance and censorship in cyberspace, steganography has garnered attention for its ability to hide private information in innocent-looking carr...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Provably Robust and Secure Steganography in Asymmetric Resou** | 2024 | cs.CR | Minhao Bai et al. [[1]](https://arxiv.org/abs/2407.13499) |

**State of the art:** Addresses asymmetric resource scenario where encoder has powerful models but decoder only reads carriers. Uses permutations of distribution for encoding; decoder uses sampling function independent of model input. Robustness over binary symmetric channels.

**Production readiness:** Research
Theoretical framework with implementation demonstration.

**Security status:** Secure
Provably secure under formal model; robust to channel errors.

**Community acceptance:** Emerging
Significant contribution to practical PSS deployment.

---

### Image steganography based on generative implicit neural representation

**Goal:** In the realm of advanced steganography, the scale of the model typically correlates directly with the resolution of the fundamental grid, necessitating the training of a distinct neural network for...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image steganography based on generative implicit neural repr** | 2024 | cs.CR | Zhong Yangjie et al. [[1]](https://arxiv.org/abs/2406.01918) |

**State of the art:** Analyzes steganographic capacity of selected learning models, including malware hiding in deep learning models.

**Production readiness:** Research
Theoretical analysis; no implementation.

**Security status:** Caution
Capacity analysis; security implications discussed.

**Community acceptance:** Emerging
Theoretical contribution to understanding steganographic capacity.

---

### On the Steganographic Capacity of Selected Learning Models

**Goal:** scenarios. For example, previous research has shown that malware can be hidden in deep learning models.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On the Steganographic Capacity of Selected Learning Models** | 2023 | cs.LG, cs.CR, cs.MM | Rishit Agrawal et al. [[1]](https://arxiv.org/abs/2308.15502) |

**State of the art:** Analyzes steganographic capacity of various learning models. Studies how malware can be hidden in deep learning models and evaluates capacity limits.

**Production readiness:** Research
Theoretical analysis; no implementation.

**Security status:** Caution
Analysis of novel attack vectors; implications for ML model security.

**Community acceptance:** Emerging
Relevant to ML model IP protection and malware detection.

---

### Introducing a New Evaluation Criteria for EMD-Base Steganography Method

**Goal:** Steganography is a technique to hide the presence of secret communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Introducing a New Evaluation Criteria for EMD-Base Steganogr** | 2023 | cs.CR, cs.MM | Hanieh Rafiee, Mojtaba Mahdavi, AhmadReza NaghshNilchi [[1]](https://arxiv.org/abs/2308.07970) |

**State of the art:** Proposes new evaluation criteria for EMD-based steganography methods. Addresses limitations in existing evaluation metrics.

**Production readiness:** Research
Theoretical contribution; no implementation.

**Security status:** Caution
Evaluation framework; security implications analyzed.

**Community acceptance:** Emerging

---

### Open Image Content Disarm And Reconstruction

**Goal:** cutting-edge Artificial Intelligence and content signature exist, evasive malware successfully bypasses next-generation malware detection using advanced methods like steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Open Image Content Disarm And Reconstruction** | 2023 | cs.CR, cs.AI | Eli Belkind, Ran Dubin, Amit Dvir [[1]](https://arxiv.org/abs/2307.14057) |

**State of the art:** Explores deep cross-modal steganography using neural representations for hiding data across modalities.

**Production readiness:** Research
Academic prototype; no production implementation.

**Security status:** Caution
Novel cross-modal approach; theoretical analysis pending.

**Community acceptance:** Emerging
Active research area.

---

### Deep Cross-Modal Steganography Using Neural Representations

**Goal:** Steganography is the process of embedding secret data into another message or data, in such a way that it is not easily noticeable.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Deep Cross-Modal Steganography Using Neural Representations** | 2023 | cs.CR, cs.AI | Gyojin Han et al. [[1]](https://arxiv.org/abs/2307.08671) |

**State of the art:** Proposes errorless robust JPEG steganography using steganographic polar codes for resilience against recompression.

**Production readiness:** Research
Academic prototype; no production implementation.

**Security status:** Caution
Novel approach; theoretical analysis pending verification.

**Community acceptance:** Niche
Specialized JPEG application.

---

### Errorless Robust JPEG Steganography Using Steganographic Polar Codes

**Goal:** Recently, a robust steganographic algorithm that achieves errorless robustness against JPEG recompression is proposed.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Errorless Robust JPEG Steganography Using Steganographic Pol** | 2023 | cs.CR, cs.MM | Jimin Zhang, Xianfeng Zhao, Xiaolei He [[1]](https://arxiv.org/abs/2306.15246) |

**State of the art:** Proposes errorless robust JPEG steganography using steganographic polar codes. Focuses on error correction for robust transmission.

**Production readiness:** Research
Academic prototype; implementation details provided.

**Security status:** Caution
Novel approach; security analysis required.

**Community acceptance:** Emerging

---

### Off-By-One Implementation Error in J-UNIWARD

**Goal:** J-UNIWARD is a popular steganography method for hiding secret messages in JPEG cover images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Off-By-One Implementation Error in J-UNIWARD** | 2023 | cs.CR, cs.LG, cs.MM | Benedikt Lorch [[1]](https://arxiv.org/abs/2305.19776) |

**State of the art:** Identifies and documents off-by-one implementation error in J-UNIWARD steganography method. Provides fix and analysis of impact on steganographic security.

**Production readiness:** Research
Bug fix documentation; implementation available.

**Security status:** Caution
Implementation vulnerability; patched versions available.

**Community acceptance:** Widely trusted
Important security fix widely adopted in steganography tools.

---

### The Realizations of Steganography in Encrypted Domain

**Goal:** in cloud service and social network, ciphertext has been gradually becoming a common platform for public to exchange data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **The Realizations of Steganography in Encrypted Domain** | 2023 | cs.CR | Yan Ke et al. [[1]](https://arxiv.org/abs/2304.02614) |

**State of the art:** Novel framework for encrypted domain steganography (SIED) with four application modes and security levels based on Simmons' prisoners' problem model.

**Production readiness:** Research
Academic prototype; four practical schemes provided with different security levels.

**Security status:** Caution
New framework with defined security levels; requires independent verification.

**Community acceptance:** Emerging
Published at arXiv; peer review status unknown.

---

### ICStega: Image Captioning-based Semantically Controllable Linguistic Steganography

**Goal:** Nowadays, social media has become the preferred communication platform for web users but brought security threats.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ICStega: Image Captioning-based Semantically Controllable Li** | 2023 | cs.CR | Xilong Wang et al. [[1]](https://arxiv.org/abs/2303.05830) |

**State of the art:** Novel generation-based linguistic steganography using image captioning with Two-Parameter Semantic Control Sampling to balance payload capacity and semantic preservation.

**Production readiness:** Research
Published at ICASSP 2023; implementation details in paper.

**Security status:** Caution
New approach; security not yet independently verified.

**Community acceptance:** Emerging
Peer-reviewed conference paper.

---

### Steganography of Steganographic Networks

**Goal:** Steganography is a technique for covert communication between two parties.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography of Steganographic Networks** | 2023 | cs.CR, cs.AI | Guobiao Li et al. [[1]](https://arxiv.org/abs/2302.14521) |

**State of the art:** Novel scheme for disguising steganographic DNN models into ordinary ML models for covert transmission, using filter selection and partial optimization.

**Production readiness:** Research
Academic prototype; experiments on various DNN models.

**Security status:** Caution
New concept; requires security analysis.

**Community acceptance:** Emerging
Preprint; novel concept in steganography.

---

### A New Paradigm for Improved Image Steganography by using Adaptive Number of Dominant Discrete Cosine Transform Coefficients

**Goal:** Image steganography camouflages secret messages in images by tampering image contents.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Paradigm for Improved Image Steganography by using Ada** | 2023 | cs.CR | Laeeq Aslam Sandhu et al. [[1]](https://arxiv.org/abs/2301.09185) |

**State of the art:** High-capacity image steganography using adaptive DCT coefficients, achieving up to 21.5 bpp payload with 38.24 dB PSNR.

**Production readiness:** Research
Academic prototype; focuses on capacity optimization.

**Security status:** Caution
Capacity-oriented approach; detection resistance not evaluated.

**Community acceptance:** Emerging
Preprint; high-capacity approach.

---

### Blind Spots: Automatically detecting ignored program inputs

**Goal:** A blind spot is any input to a program that can be arbitrarily mutated without affecting the program's output.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Blind Spots: Automatically detecting ignored program inputs** | 2023 | cs.CR, cs.PL | Henrik Brodin, Evan Sultanik, Marek Surovič [[1]](https://arxiv.org/abs/2301.08700) |

**State of the art:** Deep image steganography using conditional invertible neural networks; addresses visual similarity, statistical security, and lossless extraction; achieves 100% revealing accuracy.

**Production readiness:** Research
Novel approach using colorization and CINN; under review.

**Security status:** Caution
Claims resistance to steganalysis; needs independent verification.

**Community acceptance:** Emerging
Under review; innovative approach.

---

### Image data hiding with multi-scale autoencoder network

**Goal:** mage steganography is the process of hiding information which can be text, image, or video inside a cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image data hiding with multi-scale autoencoder network** | 2022 | cs.CR, cs.MM | Chen-Hsiu Huang, Ja-Ling Wu [[1]](https://arxiv.org/abs/2201.06038) |

**State of the art:** Deep image steganography is a data hiding technology that conceal data in digital images via deep neural networks.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### SABMIS: Sparse approximation based blind multi-image steganography scheme

**Goal:** We hide grayscale secret images into a grayscale cover image, which is considered to be a challenging steganography problem.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SABMIS: Sparse approximation based blind multi-image stegano** | 2022 | cs.CR | Rohit Agrawal et al. [[1]](https://arxiv.org/abs/2110.11418) |

**State of the art:** mage steganography is the process of hiding information which can be text, image, or video inside a cover image.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Brief Survey on Deep Learning Based Data Hiding

**Goal:** and outline three commonly used architectures.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Brief Survey on Deep Learning Based Data Hiding** | 2022 | cs.CR, cs.LG, cs.MM | Chaoning Zhang et al. [[1]](https://arxiv.org/abs/2103.01607) |

**State of the art:** Comprehensive survey of deep learning based data hiding; classifies methods by capacity, security, robustness; covers steganography, watermarking, light field messaging.

**Production readiness:** Research
Survey paper; comprehensive overview.

**Security status:** Caution
Survey; discusses security of different approaches.

**Community acceptance:** Emerging
Highly cited survey; useful overview.

---

### IoTSign: Protecting Privacy and Authenticity of IoT using Discrete Cosine Based Steganography

**Goal:** Remotely generated data by Intent of Things (IoT) has recently had a lot of attention for their huge benefits such as efficient monitoring and risk reduction.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **IoTSign: Protecting Privacy and Authenticity of IoT using Di** | 2022 | cs.CR | Sharif Abuadbba, Ayman Ibaida, Ibrahim Khalil [[1]](https://arxiv.org/abs/1911.00604) |

**State of the art:** Novel steganography using pseudorandomly sorted lists; embeds via permutation reordering; better capacity than existing methods.

**Production readiness:** Research
Theoretical framework with experimental validation.

**Security status:** Caution
Capacity-focused; security evaluation limited.

**Community acceptance:** Niche
Technical approach.

---

### Generating Steganographic Images via Adversarial Training

**Goal:** to generative tasks such as image synthesis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generating Steganographic Images via Adversarial Training** | 2017 | stat.ML, cs.CR, cs.MM | Jamie Hayes, George Danezis [[1]](https://arxiv.org/abs/1703.00371) |

**State of the art:** Remotely generated data by Intent of Things (IoT) has recently had a lot of attention for their huge benefits such as efficient monitoring and risk reduction.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Approach to SMS Steganography using Mathematical Equations

**Goal:** Short Message Service (SMS) are easily copied and hacked by using special software.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Approach to SMS Steganography using Mathematical Equat** | 2016 | cs.CR, cs.MM | Min Yang Lee, Vahab Iranmanesh, Juan C. Quiroz [[1]](https://arxiv.org/abs/1607.07947) |

**State of the art:** Adversarial training was recently shown to be competitive against supervised learning methods on computer vision tasks, however, studies have mainly been confined to generative tasks such as image ...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Natural Steganography: cover-source switching for better steganography

**Goal:** on the principle of cover-source switching, the key idea being that the embedding should switch from one cover-source to another.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Natural Steganography: cover-source switching for better ste** | 2016 | cs.MM, cs.CR | Patrick Bas [[1]](https://arxiv.org/abs/1607.07824) |

**State of the art:** In the era of Information Technology, cyber-crime has always been a worrying issue for online users.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### High Capacity Image Steganography using Adjunctive Numerical Representations with Multiple Bit-Plane Decomposition Methods

**Goal:** LSB steganography is a one of the most widely used methods for implementing covert data channels in image file exchanges [1][2].

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **High Capacity Image Steganography using Adjunctive Numerical** | 2016 | cs.MM, cs.CR | James Collins, Sos Agaian [[1]](https://arxiv.org/abs/1606.02312) |

**State of the art:** This paper proposes a new steganographic scheme relying on the principle of cover-source switching, the key idea being that the embedding should switch from one cover-source to another.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography -- A Game of Hide and Seek in Information Communication

**Goal:** important issues. In order to transfer data securely to the destination without unwanted disclosure or damage, nature inspired hide and seek tricks such as, cryptography and Steganography are heavi...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography -- A Game of Hide and Seek in Information Comm** | 2016 | cs.MM, cs.CR | Sanjeeb Kumar Behera, Minati Mishra [[1]](https://arxiv.org/abs/1604.00493) |

**State of the art:** LSB steganography is a one of the most widely used methods for implementing covert data channels in image file exchanges [1][2].

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Secure Image Steganography using Cryptography and Image Transposition

**Goal:** technological world.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secure Image Steganography using Cryptography and Image Tran** | 2015 | cs.MM, cs.CR | Khan Muhammad et al. [[1]](https://arxiv.org/abs/1510.04413) |

**State of the art:** With the growth of communication over computer networks, how to maintain the confidentiality and security of transmitted information have become some of the important issues.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography and Broadcasting

**Goal:** Informally, steganography is the process of exchanging a secret message between two communicating entities so that an eavesdropper may not know that a message has been sent.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography and Broadcasting** | 2015 | cs.CR | Fabrice P. Tachago, Stephane G. R. Ekodeck, Rene Ndoundam [[1]](https://arxiv.org/abs/1506.04502) |

**State of the art:** Information security is one of the most challenging problems in today&#39;s technological world.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Approach for Image Steganography in Spatial Domain

**Goal:** This paper presents a new approach for hiding information in digital image in spatial domain.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Approach for Image Steganography in Spatial Domain** | 2015 | cs.MM, cs.CR | Fatema Akhter [[1]](https://arxiv.org/abs/1506.03681) |

**State of the art:** Informally, steganography is the process of exchanging a secret message between two communicating entities so that an eavesdropper may not know that a message has been sent.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Facebook for Image Steganography

**Goal:** (from desktops and laptops running Windows, Unix, or OS X to hand held devices running iOS, Android, or Windows Phone), it would seem to be the perfect place to conduct steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Facebook for Image Steganography** | 2015 | cs.MM, cs.CR | Jason Hiney et al. [[1]](https://arxiv.org/abs/1506.02071) |

**State of the art:** This paper presents a new approach for hiding information in digital image in spatial domain.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### PDF Steganography based on Chinese Remainder Theorem

**Goal:** We propose different approaches of PDF files based steganography, essentially based on the Chinese Remainder Theorem.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **PDF Steganography based on Chinese Remainder Theorem** | 2015 | cs.CR | Rene Ndoundam, Stephane Gael Raymond Ekodeck [[1]](https://arxiv.org/abs/1506.01256) |

**State of the art:** Because Facebook is available on hundreds of millions of desktop and mobile computing platforms around the world and because it is available on many different kinds of platforms (from desktops and ...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Low-throughput Wavelet-based Steganography Audio Scheme

**Goal:** This paper presents the preliminary of a novel scheme of steganography, and introduces the idea of combining two secret keys in the operation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Low-throughput Wavelet-based Steganography Audio Scheme** | 2015 | cs.MM, cs.CR | P. Carrion, H. M. de Oliveira, R. M. Campello de Souza [[1]](https://arxiv.org/abs/1503.07551) |

**State of the art:** We propose different approaches of PDF files based steganography, essentially based on the Chinese Remainder Theorem.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Environment Based Secure Transfer of Data in Wireless Sensor Networks

**Goal:** technique named aggregate signature to validate the source of the message and also to protect the data against latest security attacks, cryptography technique combined with steganography has been i...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Environment Based Secure Transfer of Data in Wireless Sensor** | 2015 | cs.CR | B. Vidhya et al. [[1]](https://arxiv.org/abs/1503.03215) |

**State of the art:** This paper presents the preliminary of a novel scheme of steganography, and introduces the idea of combining two secret keys in the operation.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Secure Cyclic Steganographic Technique for Color Images using Randomization

**Goal:** want the security, confidentiality and integrity of their personal data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Secure Cyclic Steganographic Technique for Color Images us** | 2015 | cs.MM, cs.CR | Khan Muhammad et al. [[1]](https://arxiv.org/abs/1502.07808) |

**State of the art:** Most critical sensor readings (Top-k Monitoring) in environment monitoring system are important to many wireless sensor applications.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### How to Bootstrap Anonymous Communication

**Goal:** of anonymous communication and to the best of our knowledge this is the first formal study in this direction.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **How to Bootstrap Anonymous Communication** | 2015 | cs.CR | Sune K. Jakobsen, Claudio Orlandi [[1]](https://arxiv.org/abs/1502.05273) |

**State of the art:** Information Security is a major concern in today&#39;s modern era.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Secure Electronic Prescription System Using Steganography with Encryption Key Implementation

**Goal:** system that addresses some challenges pertaining to the prescription privacy protection in the process of drug prescription.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Secure Electronic Prescription System Using Steganography ** | 2015 | cs.CR, cs.CY, cs.MM | Adebayo Omotosho et al. [[1]](https://arxiv.org/abs/1502.01264) |

**State of the art:** We ask whether it is possible to anonymously communicate a large amount of data using only public (non-anonymous) communication together with a small anonymous channel.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography in Modern Smartphones and Mitigation Techniques

**Goal:** attacks and hazards to profile individuals or gather sensitive information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography in Modern Smartphones and Mitigation Technique** | 2014 | cs.MM, cs.CR | Wojciech Mazurczyk, Luca Caviglione [[1]](https://arxiv.org/abs/1410.6796) |

**State of the art:** Over the years health care has seen major improvement due to the introduction information and communication technology with electronic medical prescription being one the areas benefiting from it.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegExpose - A Tool for Detecting LSB Steganography

**Goal:** in saving time and providing new angles of attack for forensic analysts.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegExpose - A Tool for Detecting LSB Steganography** | 2014 | cs.MM, cs.CR | Benedikt Boehm [[1]](https://arxiv.org/abs/1410.6656) |

**State of the art:** By offering sophisticated services and centralizing a huge volume of personal data, modern smartphones changed the way we socialize, entertain and work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Approach for Text Steganography Based on Markov Chains

**Goal:** A text steganography method based on Markov chains is introduced, together with a reference implementation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Approach for Text Steganography Based on Markov Chains** | 2014 | cs.MM, cs.CL | H. Hernan Moraldo [[1]](https://arxiv.org/abs/1409.0915) |

**State of the art:** Steganalysis tools play an important part in saving time and providing new angles of attack for forensic analysts.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### High Security Image Steganography with Modified Arnold cat map

**Goal:** Information security is concerned with maintaining the secrecy, reliability and accessibility of data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **High Security Image Steganography with Modified Arnold cat m** | 2014 | cs.CR, cs.MM | Minati Mishra, Ashanta Ranjan Routray, Sunit Kumar [[1]](https://arxiv.org/abs/1408.3838) |

**State of the art:** A text steganography method based on Markov chains is introduced, together with a reference implementation.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Reversible and Irreversible Data Hiding Technique

**Goal:** Steganography (literally meaning covered writing) is the art and science of embedding secret message into seemingly harmless message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Reversible and Irreversible Data Hiding Technique** | 2014 | cs.CR | Tanmoy Sarkar, Sugata Sanyal [[1]](https://arxiv.org/abs/1405.2684) |

**State of the art:** Information security is concerned with maintaining the secrecy, reliability and accessibility of data.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography -- coding and intercepting the information from encoded pictures in the absence of any initial information

**Goal:** The work includes implementation and extraction algorithms capabilities test, without any additional data (starting position, the number of bits used, gap between the amount of data encoded) inform...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography -- coding and intercepting the information fro** | 2014 | cs.MM, cs.CR, cs.DC | Monika Kwiatkowska, Lukasz Swierczewski [[1]](https://arxiv.org/abs/1404.2237) |

**State of the art:** Steganography (literally meaning covered writing) is the art and science of embedding secret message into seemingly harmless message.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Study of Various Steganographic Techniques Used for Information Hiding

**Goal:** Steganography derives from the Greek word steganos, meaning covered or secret, and graphy (writing or drawing).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Study of Various Steganographic Techniques Used for Inform** | 2014 | cs.MM | C. P. Sumathi, T. Santanam, G. Umamaheswari [[1]](https://arxiv.org/abs/1401.5561) |

**State of the art:** The work includes implementation and extraction algorithms capabilities test, without any additional data (starting position, the number of bits used, gap between the amount of data encoded) inform...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Dual Layer Textual Message Cryptosystem with Randomized Sequence of Symmetric Key

**Goal:** concept of textual message encryption and decryption through a pool of randomized symmetric key and the dual layer cryptosystem with the concept of visual cryptography and steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Dual Layer Textual Message Cryptosystem with Randomized Sequ** | 2013 | cs.CR | Chandranath Adak [[1]](https://arxiv.org/abs/1312.5424) |

**State of the art:** Steganography derives from the Greek word steganos, meaning covered or secret, and graphy (writing or drawing).

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Robust Steganography Using LSB-XOR and Image Sharing

**Goal:** the secret digital information and data that are transmitted over the internet is of widespread and most challenging interest.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Robust Steganography Using LSB-XOR and Image Sharing** | 2013 | cs.CR | Chandranath Adak [[1]](https://arxiv.org/abs/1312.5417) |

**State of the art:** This paper introduces a new concept of textual message encryption and decryption through a pool of randomized symmetric key and the dual layer cryptosystem with the concept of visual cryptography a...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography using the Extensible Messaging and Presence Protocol (XMPP)

**Goal:** from one XMPP client to another, without raising the suspicion of any intermediaries.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography using the Extensible Messaging and Presence Pr** | 2013 | cs.MM, cs.CR | Reshad Patuck, Julio Hernandez-Castro [[1]](https://arxiv.org/abs/1310.0524) |

**State of the art:** Hiding and securing the secret digital information and data that are transmitted over the internet is of widespread and most challenging interest.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Comparison of secure and high capacity color image steganography techniques in RGB and YCbCr domains

**Goal:** Steganography is one of the methods used for secret communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Comparison of secure and high capacity color image steganogr** | 2013 | cs.MM, cs.CR | S. Hemalatha, U. Dinesh Acharya, A. Renuka [[1]](https://arxiv.org/abs/1307.3026) |

**State of the art:** We present here the first work to propose different mechanisms for hiding data in the Extensible Messaging and Presence Protocol (XMPP).

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Steganography Algorithm for Hiding Text in Image using Five Modulus Method

**Goal:** in size. Peak signal-to-noise ratio is captured for each of the images tested.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Steganography Algorithm for Hiding Text in Image usi** | 2013 | cs.MM, cs.CR | Firas A. Jassim [[1]](https://arxiv.org/abs/1307.0642) |

**State of the art:** Steganography is one of the methods used for secret communication.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Enhanced Tiny Encryption Algorithm with Embedding (ETEA)

**Goal:** Hence, in order to provide a better security mechanism, in this paper we propose Enhanced Tiny Encryption Algorithm with Embedding (ETEA), a data hiding technique called steganography along with th...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Enhanced Tiny Encryption Algorithm with Embedding (ETEA)** | 2013 | cs.MM, cs.CR | Deepali Virmani et al. [[1]](https://arxiv.org/abs/1306.6920) |

**State of the art:** The needs for steganographic techniques for hiding secret message inside images have been arise.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### One Time Pad Password Protection: Using T.E.C. Steganography and Secure Password Transmission Protocols

**Goal:** A while ago, I developed what I called an encryption method.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **One Time Pad Password Protection: Using T.E.C. Steganography** | 2013 | cs.CR | Givon Zirkind [[1]](https://arxiv.org/abs/1306.0497) |

**State of the art:** As computer systems become more pervasive and complex, security is increasingly important.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography based on a Parameterized Canny Edge Detection Algorithm

**Goal:** Steganography is the science of hiding digital information in such a way that no one can suspect its existence.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography based on a Parameterized Canny Edge Dete** | 2012 | cs.CR | Youssef Bassil [[1]](https://arxiv.org/abs/1212.6259) |

**State of the art:** A while ago, I developed what I called an encryption method.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography Method Based on Brightness Adjustment

**Goal:** Steganography is an information hiding technique in which secret data are secured by covering them into a computer carrier file without damaging the file or changing its size.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography Method Based on Brightness Adjustment** | 2012 | cs.CR, cs.MM | Youssef Bassil [[1]](https://arxiv.org/abs/1212.5801) |

**State of the art:** Steganography is the science of hiding digital information in such a way that no one can suspect its existence.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Authentication Technique in Frequency Domain through Wavelet Transform (ATFDWT)

**Goal:** In this paper a DWT based steganography in frequency domain, termed as ATFDWT has been proposed.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Authentication Technique in Frequency Domain through Wave** | 2012 | cs.CR | Madhumita Sengupta, J. K. Mandal, N. Ghoshal [[1]](https://arxiv.org/abs/1212.3719) |

**State of the art:** Steganography is an information hiding technique in which secret data are secured by covering them into a computer carrier file without damaging the file or changing its size.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Text Steganography Method Using Pangram and Image Mediums

**Goal:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the sender and the receiver would realize that a secret communicating is taking place.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Text Steganography Method Using Pangram and Image Mediums** | 2012 | cs.CR | Youssef Bassil [[1]](https://arxiv.org/abs/1212.2908) |

**State of the art:** In this paper a DWT based steganography in frequency domain, termed as ATFDWT has been proposed.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Lossless Data Hiding Technique based on AES-DWT

**Goal:** In this paper we propose a new data hiding technique.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Lossless Data Hiding Technique based on AES-DWT** | 2012 | cs.CR | Francisco Rubén Castillo Soria, Gustavo Fernández Torres, Ignacio Algredo-Badillo [[1]](https://arxiv.org/abs/1212.2669) |

**State of the art:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the sender and the receiver would realize that a secret communicating is taking place.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Generation-based Text Steganography Method using SQL Queries

**Goal:** Cryptography and Steganography are two techniques commonly used to secure and safely transmit digital data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Generation-based Text Steganography Method using SQL Queri** | 2012 | cs.CR | Youssef Bassil [[1]](https://arxiv.org/abs/1212.2067) |

**State of the art:** In this paper we propose a new data hiding technique.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Image Steganography Scheme using Randomized Algorithm and Context-Free Grammar

**Goal:** However, clearly visible encrypted messages, no matter how unbreakable, will arouse suspicions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Image Steganography Scheme using Randomized Algorithm and** | 2012 | cs.CR, cs.MM | Youssef Bassil [[1]](https://arxiv.org/abs/1212.2064) |

**State of the art:** Cryptography and Steganography are two techniques commonly used to secure and safely transmit digital data.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Embedding grayscale halftone pictures in QR Codes using Correction Trees

**Goal:** similar to finding the proper correction in error correction problem, but instead of single ensured possibility, there are now statistically expected some.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Embedding grayscale halftone pictures in QR Codes using Corr** | 2012 | cs.IT, cs.CR, cs.MM | Jarek Duda [[1]](https://arxiv.org/abs/1211.1572) |

**State of the art:** Currently, cryptography is in wide use as it is being exploited in various domains from data confidentiality to data integrity and message authentication.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Some New Methodologies for Image Hiding using Steganographic Techniques

**Goal:** devices like ipods, cell phones, pmps, iphones and digital cameras.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Some New Methodologies for Image Hiding using Steganographic** | 2012 | cs.CR, cs.MM | Rajesh Kumar Tiwari, Gadadhar Sahoo [[1]](https://arxiv.org/abs/1211.0377) |

**State of the art:** Barcodes like QR Codes have made that encoded messages have entered our everyday life, what suggests to attach them a second layer of information: directly available to human receiver for informati...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Public key Steganography Using Discrete Cross-Coupled Chaotic Maps

**Goal:** By cross-coupling two logistic maps a novel method is proposed for the public key steganography in JPEG image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Public key Steganography Using Discrete Cross-Coupled Chaoti** | 2012 | cs.CR, cs.MM, nlin.CD | Sodeif Ahadpour, Mahdiyeh Majidpour, Yaser Sadra [[1]](https://arxiv.org/abs/1211.0086) |

**State of the art:** Security and memory management are the major demands for electronics devices like ipods, cell phones, pmps, iphones and digital cameras.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Multimedia Steganographic Scheme using Multiresolution Analysis

**Goal:** Digital steganography or data hiding has emerged as a new area of research in connection to the communication in secured channel as well as intellectual property protection for multimedia signals.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Multimedia Steganographic Scheme using Multiresolution Analy** | 2012 | cs.CR | Tirtha sankar Das et al. [[1]](https://arxiv.org/abs/1207.2675) |

**State of the art:** By cross-coupling two logistic maps a novel method is proposed for the public key steganography in JPEG image.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Security Architecture for Cluster based Ad Hoc Networks

**Goal:** intra-cluster security.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Security Architecture for Cluster based Ad Hoc Networks** | 2012 | cs.CR | Preetida Vinayakray-Jani, Sugata Sanyal [[1]](https://arxiv.org/abs/1207.1701) |

**State of the art:** Digital steganography or data hiding has emerged as a new area of research in connection to the communication in secured channel as well as intellectual property protection for multimedia signals.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Pixastic: Steganography based Anti-Phihsing Browser Plug-in

**Goal:** world and effective anti-phishing technique is the need of the hour.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Pixastic: Steganography based Anti-Phihsing Browser Plug-in** | 2012 | cs.CR | P. Thiyagarajan, G. Aghila, V. Prasanna Venkatesan [[1]](https://arxiv.org/abs/1206.2445) |

**State of the art:** Mobile Ad hoc Networks (MANETs) are subject to various kinds of attacks.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Survey on Various Data Hiding Techniques and their Comparative Analysis

**Goal:** hiding like cryptography, hashing, authentication have been developed and are in practice today.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Survey on Various Data Hiding Techniques and their Compara** | 2012 | cs.CR | Harshavardhan Kayarkar, Sugata Sanyal [[1]](https://arxiv.org/abs/1206.1957) |

**State of the art:** In spite of existence of many standard security mechanisms for ensuring secure e-Commerce business, users still fall prey for online attacks.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Text Steganography using LSB insertion method along with Chaos Theory

**Goal:** The art of information hiding has been around nearly as long as the need for covert communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Text Steganography using LSB insertion method along with Cha** | 2012 | cs.MM | Bhavana S., K. L. Sudha [[1]](https://arxiv.org/abs/1205.1859) |

**State of the art:** With the explosive growth of internet and the fast communication techniques in recent years the security and the confidentiality of the sensitive data has become of prime and supreme importance and...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Genetic Algorithm to Make Persistent Security and Quality of Image in Steganography from RS Analysis

**Goal:** Retention of secrecy is one of the significant features during communication activity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Genetic Algorithm to Make Persistent Security and Quality of** | 2012 | cs.MM, cs.CR | T. R. Gopalakrishnan Nair, Suma V, Manas S [[1]](https://arxiv.org/abs/1204.2616) |

**State of the art:** The art of information hiding has been around nearly as long as the need for covert communication.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Experimenting with the Novel Approaches in Text Steganography

**Goal:** As is commonly known, the steganographic algorithms employ images, audio, video or text files as the medium to ensure hidden exchange of information between multiple contenders to protect the data ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Experimenting with the Novel Approaches in Text Steganograph** | 2012 | cs.CR, cs.MM | Shraddha Dulera, Devesh Jinwala, Aroop Dasgupta [[1]](https://arxiv.org/abs/1203.3644) |

**State of the art:** Retention of secrecy is one of the significant features during communication activity.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Frequency Domain Steganography using Z Transform (FDSZT)

**Goal:** Image steganography is art of hiding information onto the cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Frequency Domain Steganography using Z Transform (FDSZT)** | 2012 | cs.CR, cs.MM | J. K. Mandal [[1]](https://arxiv.org/abs/1202.4245) |

**State of the art:** As is commonly known, the steganographic algorithms employ images, audio, video or text files as the medium to ensure hidden exchange of information between multiple contenders to protect the data ...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Influence of Speech Codecs Selection on Transcoding Steganography

**Goal:** The typical approach to steganography is to compress the covert data in order to limit its size, which is reasonable in the context of a limited steganographic bandwidth.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Influence of Speech Codecs Selection on Transcoding Steganog** | 2012 | cs.CR, cs.MM | Artur Janicki, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1201.6218) |

**State of the art:** Image steganography is art of hiding information onto the cover image.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Information Hiding in CSS : A Secure Scheme Text-Steganography using Public Key Cryptosystem

**Goal:** by using CSS as a message hider.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information Hiding in CSS : A Secure Scheme Text-Steganograp** | 2012 | cs.CR | Herman Kabetta, B. Yudi Dwiandiyanta, Suyoto [[1]](https://arxiv.org/abs/1201.1968) |

**State of the art:** The typical approach to steganography is to compress the covert data in order to limit its size, which is reasonable in the context of a limited steganographic bandwidth.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Windtalking Computers: Frequency Normalization, Binary Coding Systems and Encryption

**Goal:** of a method for computers analogous to speaking another language.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Windtalking Computers: Frequency Normalization, Binary Codin** | 2012 | cs.CR | Givon Zirkind [[1]](https://arxiv.org/abs/0912.4080) |

**State of the art:** In many recent years, the programming world has been introduced about a new programming language for designing websites, it is CSS that can be be used together with HTML to develop a web interface.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Randomness Efficient Steganography

**Goal:** comes as an effect of the application of randomness extractors to stegosystem design.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Randomness Efficient Steganography** | 2012 | cs.CR, cs.IT | Aggelos Kiayias, Alexander Russell, Narasimha Shashidhar [[1]](https://arxiv.org/abs/0909.4575) |

**State of the art:** This paper discusses the application of known techniques, knowledge and technology in a novel way for encryption.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Chaotic iterations for steganography: Stego-security and topological-security

**Goal:** In this paper is proposed a novel steganographic scheme based on chaotic iterations.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Chaotic iterations for steganography: Stego-security and top** | 2011 | cs.CR, cs.MM, math.DS | Nicolas Friot, Christophe Guyeux, Jacques M. Bahi [[1]](https://arxiv.org/abs/1112.3873) |

**State of the art:** Steganographic protocols enable one to embed covert messages into inconspicuous data over a public communication channel in such a way that no one, aside from the sender and the intended receiver, ...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography Algorithm to Hide Secret Message inside an Image

**Goal:** In this paper, the authors propose a new algorithm to hide data inside image using steganography technique.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography Algorithm to Hide Secret Message inside an Ima** | 2011 | cs.MM, cs.CR | Rosziati Ibrahim, Teoh Suk Kuan [[1]](https://arxiv.org/abs/1112.2809) |

**State of the art:** In this paper is proposed a novel steganographic scheme based on chaotic iterations.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography: a Class of Algorithms having Secure Properties

**Goal:** Chaos-based approaches are frequently proposed in information hiding, but without obvious justification.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography: a Class of Algorithms having Secure Propertie** | 2011 | cs.DM, cs.CR | Jacques M. Bahi, Jean-François Couchot, Christophe Guyeux [[1]](https://arxiv.org/abs/1112.1675) |

**State of the art:** In this paper, the authors propose a new algorithm to hide data inside image using steganography technique.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography: a class of secure and robust algorithms

**Goal:** This research work presents a new class of non-blind information hiding algorithms that are stego-secure and robust.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography: a class of secure and robust algorithms** | 2011 | cs.CR | Jacques M. Bahi, Jean-François Couchot, Christophe Guyeux [[1]](https://arxiv.org/abs/1112.1260) |

**State of the art:** Chaos-based approaches are frequently proposed in information hiding, but without obvious justification.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Transcoding for Hidden Communication in IP Telephony

**Goal:** The paper presents a new steganographic method for IP telephony called TranSteg (Transcoding Steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Transcoding for Hidden Communication in IP Telephony** | 2011 | cs.CR, cs.MM | Wojciech Mazurczyk, Pawel Szaga, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1111.1250) |

**State of the art:** Novel IP telephony steganography (TranSteg) using transcoding to create space for hidden data; high bandwidth; difficult to detect.

**Production readiness:** Research
Proof of concept implementation; experimental results provided.

**Security status:** Caution
Network-based detection difficult; practical deployment limited.

**Community acceptance:** Emerging
Influential work in VoIP steganography.

---

### Applying statistical methods to text steganography

**Goal:** This paper presents a survey of text steganography methods used for hid- ing secret information inside some covertext.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Applying statistical methods to text steganography** | 2011 | cs.CR | Ivan Nechta, Andrei Fionov [[1]](https://arxiv.org/abs/1110.2654) |

**State of the art:** Survey of text steganography methods using statistical approaches.

**Production readiness:** Research
Survey paper; useful overview.

**Security status:** Caution
Survey; no new security claims.

**Community acceptance:** Niche
Educational resource.

---

### An Approach for Message Hiding using Substitution Techniques and Audio Hiding in Steganography

**Goal:** that an eavesdropper who overhears the encrypted messages will not be able to decode them.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Approach for Message Hiding using Substitution Techniques** | 2011 | cs.CR | Debajyoti Mukhopadhyay et al. [[1]](https://arxiv.org/abs/1109.4709) |

**State of the art:** This paper presents a survey of text steganography methods used for hid- ing secret information inside some covertext.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Digital Forensics Analysis of Spectral Estimation Methods

**Goal:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the intended recipient knows of the existence of the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Digital Forensics Analysis of Spectral Estimation Methods** | 2011 | cs.CR | Tolga Mataracioglu, Unal Tatar [[1]](https://arxiv.org/abs/1108.2151) |

**State of the art:** A crypto system can be used to encrypt messages sent between two communicating parties so that an eavesdropper who overhears the encrypted messages will not be able to decode them.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Is Cloud Computing Steganography-proof?

**Goal:** on characterisation of information hiding possibilities in Cloud Computing.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Is Cloud Computing Steganography-proof?** | 2011 | cs.CR | Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4077) |

**State of the art:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the intended recipient knows of the existence of the message.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Lost Audio Packets Steganography: The First Practical Evaluation

**Goal:** This paper presents first experimental results for an IP telephony-based steganographic method called LACK (Lost Audio PaCKets steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Lost Audio Packets Steganography: The First Practical Evalua** | 2011 | cs.CR, cs.MM | Wojciech Mazurczyk [[1]](https://arxiv.org/abs/1107.4076) |

**State of the art:** The paper focuses on characterisation of information hiding possibilities in Cloud Computing.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Wet paper codes and the dual distance in steganography

**Goal:** In 1998 Crandall introduced a method based on coding theory to secretly embed a message in a digital support such as an image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Wet paper codes and the dual distance in steganography** | 2011 | cs.CR, cs.IT | Carlos Munuera, Morgan Barbier [[1]](https://arxiv.org/abs/1104.1970) |

**State of the art:** This paper presents first experimental results for an IP telephony-based steganographic method called LACK (Lost Audio PaCKets steganography).

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Secret Information in Movie Clip: A Steganographic Approach

**Goal:** subject of discussion that has gained increasing importance nowadays with the development of the internet.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Secret Information in Movie Clip: A Steganographic Ap** | 2011 | cs.MM, cs.CR | G. Sahoo, Rajesh Kumar Tiwari [[1]](https://arxiv.org/abs/1103.0829) |

**State of the art:** In 1998 Crandall introduced a method based on coding theory to secretly embed a message in a digital support such as an image.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On Steganography in Lost Audio Packets

**Goal:** presents a new hidden data insertion procedure based on estimated probability of the remaining time of the call for steganographic method called LACK (Lost Audio PaCKets steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On Steganography in Lost Audio Packets** | 2011 | cs.CR, cs.MM | Wojciech Mazurczyk, Jozef Lubacz, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1102.0023) |

**State of the art:** Establishing hidden communication is an important subject of discussion that has gained increasing importance nowadays with the development of the internet.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Bio-Authentication based Secure Transmission System using Steganography

**Goal:** method for Fingerprint recognition is considered using a combination of Fast Fourier Transform (FFT) and Sobel Filters for improvement of a poor quality fingerprint image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Bio-Authentication based Secure Transmission System using St** | 2010 | cs.CR | Najme Zehra et al. [[1]](https://arxiv.org/abs/1005.4264) |

**State of the art:** The paper presents a new hidden data insertion procedure based on estimated probability of the remaining time of the call for steganographic method called LACK (Lost Audio PaCKets steganography).

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Improved information security using robust Steganography system

**Goal:** Steganography is an emerging area which is used for secured data transmission over any public media.Steganography is a process that involves hiding a message in an appropriate carrier like image or...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improved information security using robust Steganography sys** | 2010 | cs.CR | Mamta Juneja, Parvinder singh Sandhu [[1]](https://arxiv.org/abs/1004.2132) |

**State of the art:** Biometrics deals with identity verification of an individual by using certain physiological or behavioral features associated with a person.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Overview: Main Fundamentals for Steganography

**Goal:** threats. It is a big security and privacy issue, it become necessary to find appropriate protection because of the significance, accuracy and sensitivity of the information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Overview: Main Fundamentals for Steganography** | 2010 | cs.CR, cs.MM | Zaidoon Kh. AL-Ani et al. [[1]](https://arxiv.org/abs/1003.4086) |

**State of the art:** Steganography is an emerging area which is used for secured data transmission over any public media.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### New System for Secure Cover File of Hidden Data in the Image Page within Executable File Using Statistical Steganography Techniques

**Goal:** A Previously traditional methods were sufficient to protect the information, since it is simplicity in the past does not need complicated methods but with the progress of information technology, it...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **New System for Secure Cover File of Hidden Data in the Image** | 2010 | cs.CR, cs.MM | Rafiqul Islam et al. [[1]](https://arxiv.org/abs/1002.2416) |

**State of the art:** The rapid development of multimedia and internet allows for wide distribution of digital media data.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### M-Banking Security - a futuristic improved security approach

**Goal:** The aim of this work is to provide a secure environment in terms of security for transaction by various ways.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **M-Banking Security - a futuristic improved security approach** | 2010 | cs.CR | Geeta S. Navale, Swati S. Joshi, Aaradhana A. Deshmukh [[1]](https://arxiv.org/abs/1002.1174) |

**State of the art:** A Previously traditional methods were sufficient to protect the information, since it is simplicity in the past does not need complicated methods but with the progress of information technology, it...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Steganography Based on CT-CDMA Communication Scheme Using Complete Complementary Codes

**Goal:** users can be transmitted by using the same set of complementary codes through a single frequency band.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Steganography Based on CT-CDMA Communication Scheme Using ** | 2010 | cs.IT, cs.CR | Tetsuya Kojima, Yoshiya Horii [[1]](https://arxiv.org/abs/1001.2623) |

**State of the art:** In last few decades large technology development raised various new needs.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Frame Selected Approach for Hiding Data within MPEG Video Using Bit Plane Complexity Segmentation

**Goal:** Bit Plane Complexity Segmentation (BPCS) digital picture steganography is a technique to hide data inside an image file.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Frame Selected Approach for Hiding Data within MPEG Video Us** | 2009 | cs.CR | Hamid. A. Jalab, A. A Zaidan, B. B Zaidan [[1]](https://arxiv.org/abs/0912.3986) |

**State of the art:** It has been shown that complete complementary codes can be applied into some communication systems like approximately synchronized CDMA systems because of its good correlation properties.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography An Art of Hiding Data

**Goal:** these channels, an eavesdropper can identify encrypted streams through statistical tests and capture them for further cryptanalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography An Art of Hiding Data** | 2009 | cs.CR | Shashikala Channalli, Ajay Jadhav [[1]](https://arxiv.org/abs/0912.2319) |

**State of the art:** Bit Plane Complexity Segmentation (BPCS) digital picture steganography is a technique to hide data inside an image file.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An approach to secure highly confidential documents of any size in the corporate or institutes having unsecured networks

**Goal:** papers and many other confidential documents designed by their faculty members.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An approach to secure highly confidential documents of any s** | 2009 | cs.CR | Samir B. Patel, Shrikant N. Pradhan [[1]](https://arxiv.org/abs/0912.0954) |

**State of the art:** In today's world the art of sending & displaying the hidden information especially in public places, has received more attention and faced many challenges.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A novel approach for implementing Steganography with computing power obtained by combining Cuda and Matlab

**Goal:** available within. Our approach is to use the CUDA (Compute Unified Device Architecture) as backend and MATLAB as the front end to design an application for implementing steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A novel approach for implementing Steganography with computi** | 2009 | cs.CR | Samir B. Patel, Shrikant N. Pradhan, Saumitra U. Ambegaokar [[1]](https://arxiv.org/abs/0912.0947) |

**State of the art:** With the tremendous amount of computing because of the wide usage of internet it is observed that some user(s) are not able to manage their desktop with antivirus software properly installed.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Efficient Steganography with Provable Security Guarantees

**Goal:** We provide a new provably-secure steganographic encryption protocol that is proven secure in the complexity-theoretic framework of Hopper et al.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Efficient Steganography with Provable Security Guarantees** | 2009 | cs.CR, cs.IT | Aggelos Kiayias et al. [[1]](https://arxiv.org/abs/0909.3658) |

**State of the art:** With the current development of multiprocessor systems, strive for computing data on such processor have also increased exponentially.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Performance Analysis of HICCUPS - a Steganographic System for WLAN

**Goal:** The paper presents an analysis of performance features of the HICCUPS (HIdden Communication system for CorrUPted networkS) including the efficiency and the cost of the system in WLANs (Wireless Loc...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Performance Analysis of HICCUPS - a Steganographic System ** | 2009 | cs.CR, cs.PF | Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/0906.4217) |

**State of the art:** We provide a new provably-secure steganographic encryption protocol that is proven secure in the complexity-theoretic framework of Hopper et al.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint stage; community evaluation ongoing.

---

### Hiding Information in Retransmissions

**Goal:** The paper presents a new steganographic method called RSTEG (Retransmission Steganography), which is intended for a broad class of protocols that utilises retransmission mechanisms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Information in Retransmissions** | 2009 | cs.CR | Wojciech Mazurczyk, Milosz Smolarczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/0905.0363) |

**State of the art:** The paper presents an analysis of performance features of the HICCUPS (HIdden Communication system for CorrUPted networkS) including the efficiency and the cost of the system in WLANs (Wireless Loc...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Kolmogorov Complexity for Understanding Some Limitations on Steganography

**Goal:** Recently perfectly secure steganographic systems have been described for a wide class of sources of covertexts.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Kolmogorov Complexity for Understanding Some Limitatio** | 2009 | cs.CC, cs.CR | Boris Ryabko, Daniil Ryabko [[1]](https://arxiv.org/abs/0901.4023) |

**State of the art:** The paper presents a new steganographic method called RSTEG (Retransmission Steganography), which is intended for a broad class of protocols that utilises retransmission mechanisms.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Capacity of Steganographic Channels

**Goal:** This work investigates a central problem in steganography, that is: How much data can safely be hidden without being detected?

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Capacity of Steganographic Channels** | 2008 | cs.CR, cs.IT | Jeremiah J. Harmsen, William A. Pearlman [[1]](https://arxiv.org/abs/0810.4171) |

**State of the art:** Recently perfectly secure steganographic systems have been described for a wide class of sources of covertexts.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### TrustMAS: Trusted Communication Platform for Multi-Agent Systems

**Goal:** are able to perform various steganographic communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **TrustMAS: Trusted Communication Platform for Multi-Agent Sys** | 2008 | cs.CR, cs.MA | Krzysztof Szczypiorski et al. [[1]](https://arxiv.org/abs/0808.4060) |

**State of the art:** This work investigates a central problem in steganography, that is: How much data can safely be hidden without being detected? To answer this question, a formal definition of steganographic capacit...

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography, a New Approach for Transferring Security Information

**Goal:** Steganography is the art of hiding the fact that communication is taking place, by hiding information in other information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography, a New Approach for Transferring Securit** | 2008 | cs.CR | H. B. Bahar, Ali Aboutalebi [[1]](https://arxiv.org/abs/0808.1410) |

**State of the art:** The paper presents TrustMAS - Trusted Communication Platform for Multi-Agent Systems, which provides trust and anonymity for mobile agents.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography from weak cryptography

**Goal:** We introduce a problem setting which we call ``the freedom fighters' problem''.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography from weak cryptography** | 2008 | cs.CR | Boris Skoric [[1]](https://arxiv.org/abs/0804.0659) |

**State of the art:** Steganography is the art of hiding the fact that communication is taking place, by hiding information in other information.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Information Hiding Techniques: A Tutorial Review

**Goal:** The purpose of this tutorial is to present an overview of various information hiding techniques.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information Hiding Techniques: A Tutorial Review** | 2008 | cs.CR, cs.IR | Sabu M. Thampi [[1]](https://arxiv.org/abs/0802.3746) |

**State of the art:** We introduce a problem setting which we call ``the freedom fighters' problem''.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint stage; community evaluation ongoing.

---

### An Improved FPGA Implementation of the Modified Hybrid Hiding Encryption Algorithm (MHHEA) for Data Communication Security

**Goal:** The hybrid hiding encryption algorithm, as its name implies, embraces concepts from both steganography and cryptography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Improved FPGA Implementation of the Modified Hybrid Hidin** | 2007 | cs.CR | Hala A. Farouk, Magdy Saeb [[1]](https://arxiv.org/abs/0710.4800) |

**State of the art:** The purpose of this tutorial is to present an overview of various information hiding techniques.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Lightweight security mechanism for PSTN-VoIP cooperation

**Goal:** In this paper we describe a new, lightweight security mechanism for PSTN-VoIP cooperation that is based on two information hiding techniques: digital watermarking and steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Lightweight security mechanism for PSTN-VoIP cooperation** | 2006 | cs.CR, cs.MM | Wojciech Mazurczyk, Zbigniew Kotulski [[1]](https://arxiv.org/abs/cs/0612054) |

**State of the art:** The hybrid hiding encryption algorithm, as its name implies, embraces concepts from both steganography and cryptography.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### New security and control protocol for VoIP based on steganography and digital watermarking

**Goal:** this solution offers authentication and integrity, it is capable of exchanging and verifying QoS and security parameters.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **New security and control protocol for VoIP based on steganog** | 2006 | cs.CR, cs.MM | Wojciech Mazurczyk, Zbigniew Kotulski [[1]](https://arxiv.org/abs/cs/0602042) |

**State of the art:** Novel security and control protocol for VoIP using steganography and watermarking; offers authentication, integrity, QoS without additional bandwidth.

**Production readiness:** Research
Alternative to RTCP for real-time applications.

**Security status:** Caution
Network-based; practical deployment considerations.

**Community acceptance:** Niche
Published in Annales UMCS.

---

### Content Based Image Retrieval with Mobile Agents and Steganography

**Goal:** In this paper we present an image retrieval system based on Gabor texture features, steganography, and mobile agents..

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Content Based Image Retrieval with Mobile Agents and Stegano** | 2006 | cs.CR | Sabu . M Thampi, K. Chandra Sekaran [[1]](https://arxiv.org/abs/cs/0411041) |

**State of the art:** Image retrieval system combining Gabor texture features, steganography, and mobile agents for secure image search.

**Production readiness:** Research
Novel combination of techniques.

**Security status:** Caution
Application-specific; limited evaluation.

**Community acceptance:** Niche
Application-specific approach.

---

## Web Tools & References

---

### Irongeek Unicode Steganography

**Goal:** Encode and decode text-based steganographic messages using Unicode homoglyphs and invisible characters via a web interface.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Irongeek Unicode Stego** | 2012 | Homoglyph substitution + zero-width characters | Web encoder/decoder; no install required [[1]](https://www.irongeek.com/i.php?page=security/unicode-steganography-homoglyph-encoder) |

**State of the art:** Classic reference implementation for Unicode-based text steganography. Commonly used to generate challenge files in CTF competitions.

**Production readiness:** Mature
Web tool; stable but no active development.

**Security status:** Caution
Easily detected by inspecting raw bytes; homoglyph substitutions visible in hex editors.

**Community acceptance:** Niche
Well-known in CTF community; rarely used in production systems.

---

## Python Text Stego Libraries

---

### pyUnicodeSteganography

**Goal:** Encode messages in plaintext by inserting invisible Unicode zero-width characters between visible characters.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **pyUnicodeSteganography** | 2020 | Zero-width Unicode character substitution | Message survives copy-paste; visually undetectable [[1]](https://github.com/bunnylab/pyUnicodeSteganography) |

**State of the art:** Simple Python library for zero-width stego. Works by encoding bits as combinations of ZWSP, ZWNJ, ZWJ characters.

**Production readiness:** Experimental
Small project; functional but minimal documentation.

**Implementations:**
- [bunnylab/pyUnicodeSteganography](https://github.com/bunnylab/pyUnicodeSteganography) ⭐ 6 — Python

**Security status:** Caution
Detectable by inspecting raw bytes or using Unicode debuggers like the Irongeek tool.

**Community acceptance:** Niche
Small project; one of several similar implementations.

---

