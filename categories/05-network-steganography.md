# Network Steganography

<!-- TOC -->
## Contents (59 algorithms)

**[Header Fields](#header-fields)**
- [IPv4/IPv6 Headers](#ipv4ipv6-headers)
- [TCP Headers](#tcp-headers)
- [HTTP Headers](#http-headers)

**[Timing Channels](#timing-channels)**
- [IPD Encoding](#ipd-encoding)
- [LAN Covert Channels (Girling)](#lan-covert-channels-girling)
- [Wolf Covert Channels](#wolf-covert-channels)
- [Jitterbug](#jitterbug)
- [Keypress Timing Channel](#keypress-timing-channel)

**[DNS Tunneling](#dns-tunneling)**
- [iodine](#iodine)
- [dnscat2](#dnscat2)
- [dns2tcp](#dns2tcp)
- [A Lightweight Adaptable DNS Channel for Covert Data Transmission](#a-lightweight-adaptable-dns-channel-for-covert-data-transmission)

**[Protocol-specific](#protocol-specific)**
- [QuicCourier](#quiccourier)
- [LACK](#lack)
- [SteganoRTP](#steganortp)
- [VoIP Steganography](#voip-steganography)
- [WireGuard Steganography](#wireguard-steganography)
- [Combining Different Existing Methods for Describing Steganography Hiding Methods](#combining-different-existing-methods-for-describing-steganography-hiding-methods)
- [Quantum Hilbert Transform](#quantum-hilbert-transform)
- [RFNNS: Robust Fixed Neural Network Steganography with Universal Text-to-Image Models](#rfnns-robust-fixed-neural-network-steganography-with-universal-text-to-image-models)
- [Multichannel Steganography: A Provably Secure Hybrid Steganographic Model for Secure Communication](#multichannel-steganography-a-provably-secure-hybrid-steganographic-model-for-secure-communication)
- [Cover-separable Fixed Neural Network Steganography via Deep Generative Models](#cover-separable-fixed-neural-network-steganography-via-deep-generative-models)
- [Synthetic Embedding of Hidden Information in Industrial Control System Network Protocols for Evaluation of Steganographic Malware](#synthetic-embedding-of-hidden-information-in-industrial-control-system-network-protocols-for-evaluation-of-steganographic-malware)
- [Purified and Unified Steganographic Network](#purified-and-unified-steganographic-network)
- [Towards Deep Network Steganography: From Networks to Networks](#towards-deep-network-steganography-from-networks-to-networks)
- [Unified Description for Network Information Hiding Methods](#unified-description-for-network-information-hiding-methods)
- [A Second Order Derivatives based Approach for Steganography](#a-second-order-derivatives-based-approach-for-steganography)
- [Why Johnny Can't Use Stego: a Human-oriented Perspective on the Application of Steganography](#why-johnny-cant-use-stego-a-human-oriented-perspective-on-the-application-of-steganography)
- [Trends toward real-time network data steganography](#trends-toward-real-time-network-data-steganography)
- [StegBlocks: ensuring perfect undetectability of network steganography](#stegblocks-ensuring-perfect-undetectability-of-network-steganography)
- [Hidden and Uncontrolled - On the Emergence of Network Steganographic Threats](#hidden-and-uncontrolled-on-the-emergence-of-network-steganographic-threats)
- [On Importance of Steganographic Cost For Network Steganography](#on-importance-of-steganographic-cost-for-network-steganography)
- [Adaptive Software Radio Steganography](#adaptive-software-radio-steganography)
- [Principles and Overview of Network Steganography](#principles-and-overview-of-network-steganography)
- [Direct Sequence Spread Spectrum Steganographic Scheme for IEEE 802.15.4](#direct-sequence-spread-spectrum-steganographic-scheme-for-ieee-802154)
- [How Hidden Can Be Even More Hidden?](#how-hidden-can-be-even-more-hidden)
- [Sending Hidden Data via Google Suggest](#sending-hidden-data-via-google-suggest)
- [Stegobot: construction of an unobservable communication network leveraging social behavior](#stegobot-construction-of-an-unobservable-communication-network-leveraging-social-behavior)
- [Proposed System for data hiding using Cryptography and Steganography Proposed System for data hiding using Cryptography and Steganography](#proposed-system-for-data-hiding-using-cryptography-and-steganography-proposed-system-for-data-hiding-using-cryptography-and-steganography)
- [Retransmission Steganography Applied](#retransmission-steganography-applied)
- [Stream Control Transmission Protocol Steganography](#stream-control-transmission-protocol-steganography)
- [Information Hiding Using Improper Frame Padding](#information-hiding-using-improper-frame-padding)
- [Perfect Z2Z4-linear codes in Steganography](#perfect-z2z4-linear-codes-in-steganography)
- [Steganography in Handling Oversized IP Packets](#steganography-in-handling-oversized-ip-packets)
- [SecMon: End-to-End Quality and Security Monitoring System](#secmon-end-to-end-quality-and-security-monitoring-system)
- [New security and control protocol for VoIP based on steganography and digital watermarking](#new-security-and-control-protocol-for-voip-based-on-steganography-and-digital-watermarking)
- [Lightweight security mechanism for PSTN-VoIP cooperation](#lightweight-security-mechanism-for-pstn-voip-cooperation)
- [Environment Based Secure Transfer of Data in Wireless Sensor Networks](#environment-based-secure-transfer-of-data-in-wireless-sensor-networks)
- [Steganography: A Secure way for Transmission in Wireless Sensor Networks](#steganography-a-secure-way-for-transmission-in-wireless-sensor-networks)

**[Alternative Protocols](#alternative-protocols)**
- [5G/6G Cellular](#5g6g-cellular)
- [Wi-Fi CSI](#wi-fi-csi)
- [CYPRESS](#cypress)
- [HICCUPS](#hiccups)
- [Inter-protocol Steganography](#inter-protocol-steganography)
- [Quantum Gatekeeper](#quantum-gatekeeper)
- [Intellicise Wireless Network](#intellicise-wireless-network)
- [VeriPHY](#veriphy)
- [Hiding Data in Plain Sight: Undetectable Wireless Communications Through Pseudo-Noise Asymmetric Shift Keying](#hiding-data-in-plain-sight-undetectable-wireless-communications-through-pseudo-noise-asymmetric-shift-keying)
- ["The Good, The Bad And The Ugly": Evaluation of Wi-Fi Steganography](#the-good-the-bad-and-the-ugly-evaluation-of-wi-fi-steganography)

<!-- /TOC -->

## Header Fields

---

### IPv4/IPv6 Headers

**Goal:** Use protocol header fields for data embedding.

| Algorithm | Year | Field | Bits/Packet |
|----------|------|-------|-------------|
| **IPv4/IPv6 Headers** | 1997 | ID, TTL, DSCP, Flow Label | 1-20 bit/pkt [[1]](https://firstmonday.org/ojs/index.php/fm/article/view/528) [[2]](https://link.springer.com/chapter/10.1007/11558859_19) |

**State of the art:** Simple but limited capacity. Rowland (1997) first demonstrated IP ID and TCP ISN as covert channels; Murdoch & Lewis (2005) refined undetectability.

**Production readiness:** Experimental

**Security status:** Caution — Easily monitored by deep packet inspection

**Community acceptance:** Niche

---

### TCP Headers

**Goal:** Use TCP header fields for covert communication.

| Algorithm | Year | Field | Bits/Packet |
|----------|------|-------|-------------|
| **TCP Headers** | 1997 | ISN, Timestamp, Window | 4-32 bit/conn [[1]](https://firstmonday.org/ojs/index.php/fm/article/view/528) [[2]](https://link.springer.com/chapter/10.1007/11558859_19) |

**State of the art:** Common approach for TCP-based channels. Rowland (1997) first showed ISN and ACK fields can carry covert data; Murdoch & Lewis (2005) developed OS-mimicking transforms to avoid detection.

**Production readiness:** Experimental

**Security status:** Caution — Detectable by ISN statistical analysis

**Community acceptance:** Niche

---

### HTTP Headers

**Goal:** Use HTTP header order/content for embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HTTP Headers** | 2005 | Header order, case | log2(N!)/req [[1]](https://link.springer.com/chapter/10.1007/11558859_19) |

**State of the art:** Works in HTTP traffic. Murdoch & Lewis (2005) surveyed TCP/IP embedding techniques including HTTP-level channels.

**Production readiness:** Experimental

**Security status:** Caution — Header ordering detectable by traffic classifiers

**Community acceptance:** Niche

---

## Timing Channels

---

### IPD Encoding

**Goal:** Encode data in inter-packet delays.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **IPD Encoding** | 2007 | Delay < T = 0, > T = 1 | 1-10 bps [[1]](https://dl.acm.org/doi/10.1145/1315245.1315280) |

**State of the art:** Classic timing channel. Gianvecchio & Wang (2007) introduced the entropy-based detection method for IPD covert channels at ACM CCS.

**Production readiness:** Experimental

**Security status:** Caution — Detectable by entropy and regularity analysis

**Community acceptance:** Niche

---

### LAN Covert Channels (Girling)

**Goal:** First study of covert channels in LAN.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Girling** | 1987 | Storage + timing channels | Foundational [[1]](https://ieeexplore.ieee.org/document/1702208/) |

**State of the art:** Foundational research identifying both storage and timing covert channels in IEEE 802 LAN protocols.

**Production readiness:** Research

**Security status:** Caution — Historical reference; modern LANs have additional monitoring

**Community acceptance:** Niche — Historical importance, widely cited

---

### Wolf Covert Channels

**Goal:** Implement covert channels in LAN protocol reserved fields.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Wolf** | 1989 | Reserved/unused fields in IEEE 802.2/3/4/5 | LAN protocols [[1]](https://link.springer.com/content/pdf/10.1007/3-540-51754-5_33.pdf) |

**State of the art:** Early demonstration that unused bandwidth in IEEE 802 LAN frame fields can be exploited as covert channels.

**Production readiness:** Research

**Security status:** Caution — Fields now monitored by modern IDS

**Community acceptance:** Niche — Historical, precedes TCP/IP-focused work

---

### Jitterbug

**Goal:** Modulate keystroke timing for covert channels.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Jitterbug** | 2006 | Keystroke inter-arrival timing modulation | Low bandwidth [[1]](https://www.usenix.org/conference/15th-usenix-security-symposium/keyboards-and-covert-channels) |

**State of the art:** Shah, Molina & Blaze (USENIX Security 2006) showed hardware keyloggers can leak passwords through SSH timing without compromising the host OS. Best Student Paper award.

**Production readiness:** Research

**Security status:** Caution — Detectable by partial entropy tests

**Community acceptance:** Niche — Influential in covert channel research

---

### Keypress Timing Channel

**Goal:** Encode data in keyboard timing delays observable over the network.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Keypress Timing** | 2001 | Inter-keystroke delays leak via SSH/Telnet | 1-10 bps [[1]](https://www.usenix.org/conference/10th-usenix-security-symposium/timing-analysis-keystrokes-and-timing-attacks-ssh) |

**State of the art:** Song, Wagner & Tian (USENIX Security 2001) demonstrated statistical recovery of passwords from SSH keystroke timing. Related to Jitterbug but passive (eavesdropping rather than injection).

**Production readiness:** Experimental

**Security status:** Caution — Mitigated by SSH keystroke bundling; active injection variant (Jitterbug) harder to detect

**Community acceptance:** Niche

---

## DNS Tunneling

---

### iodine

**Goal:** IP-over-DNS tunnel.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **iodine** | 2006 | IP-over-DNS via TXT/NULL | ~100 KB/s |

**State of the art:** Classic DNS tunneling tool.

**Production readiness:** Deprecated

**Implementations:**
- [iodine](https://github.com/yarrick/iodine) ⭐ 3.8k

**Security status:** Broken — Highly detectable

**Community acceptance:** Widely trusted — Classic tool

---

### dnscat2

**Goal:** C2 channel over DNS.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **dnscat2** | 2015 | C2 in TXT records | 1-10 KB/s |

**State of the art:** Modern DNS tunneling for C2.

**Production readiness:** Experimental

**Implementations:**
- [dnscat2](https://github.com/zbetcheckin/dnscat2) ⭐ 2.1k

**Security status:** Caution — Detectable patterns

**Community acceptance:** Widely trusted — Red teaming

---

### dns2tcp

**Goal:** TCP tunneling over DNS.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **dns2tcp** | 2004 | TCP over DNS | 10-50 KB/s |

**State of the art:** Early DNS tunneling.

**Production readiness:** Deprecated

**Implementations:**
- [dns2tcp](https://github.com/alexbakker/dns2tcp) ⭐ 289

**Security status:** Broken — Highly detectable

**Community acceptance:** Niche

---

### A Lightweight Adaptable DNS Channel for Covert Data Transmission

**Goal:** Create a DNS-based storage covert channel for stealthy data transfer.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Lightweight Adaptable DNS Channel for Covert Data Transmis** | 2020 | cs.CR | Mahboubeh Nazari, Sousan Tarahomi, Sobhan Aliabady [[1]](https://arxiv.org/abs/2003.14094) |

**State of the art:** DNS storage covert channel with connection establishment, adaptability, lightweight obfuscation, and HMAC for confidentiality/integrity. Statistics well adapted to normal traffic. Average capacity 2.65 bytes/packet.

**Production readiness:** Experimental
Academic research; no public implementation.

**Security status:** Caution
DNS tunneling known to be monitored by security tools.

**Community acceptance:** Niche
DNS covert channel research.

---

## Protocol-specific

---

### QuicCourier

**Goal:** Hide data in QUIC protocol traffic via proxy-encapsulated web browsing behavior.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **QuicCourier** | 2025 | Generative model mimics QUIC browsing patterns | Exceptional undetectability [[1]](https://ieeexplore.ieee.org/document/10916752/) [[2]](https://lib.jucs.org/article/154672/) |

**State of the art:** Huang et al. (IEEE TDSC 2025) use a generative model to mimic legitimate QUIC web browsing; Velinov et al. (JUCS 2026) systematically identify 20 covert channels in QUIC/HTTP3.

**Production readiness:** Research

**Security status:** Secure — QUIC encryption limits DPI; proxy encapsulation further obscures patterns

**Community acceptance:** Emerging — Active research

---

### LACK

**Goal:** Hide data in intentionally lost VoIP packets.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LACK** | 2008 | Lost Audio PaCKets — delayed RTP packets carry payload | VoIP [[1]](https://arxiv.org/abs/0811.4138) |

**State of the art:** Mazurczyk & Lubacz (2008) introduced LACK; subsequent work analyzed steganographic bandwidth vs. voice quality trade-offs. See also [SteganoRTP](#steganortp) and [VoIP Steganography](#voip-steganography).

**Production readiness:** Experimental

**Security status:** Caution — Detectable by timing analysis of late packet patterns

**Community acceptance:** Niche — Well-cited foundational VoIP steganography paper

---

### SteganoRTP

**Goal:** Embed in RTP protocol fields.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SteganoRTP** | 2008 | Unused RTP/RTCP fields (padding bit, CSRC list) | RTP [[1]](https://arxiv.org/abs/0805.2938) |

**State of the art:** Mazurczyk & Szczypiorski (2008) first applied unused-field steganography to RTP/RTCP, previously only studied for IP/UDP/TCP. See also [LACK](#lack).

**Production readiness:** Experimental

**Security status:** Caution — Unused field manipulation detectable by RTP-aware monitors

**Community acceptance:** Niche

---

### VoIP Steganography

**Goal:** General steganography in Voice over IP streams.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **VoIP Steganography** | 2008 | Codec LSBs, silence periods, transcoding | Multiple methods [[1]](https://arxiv.org/abs/1203.4374) |

**State of the art:** Mazurczyk (ACM CSUR 2013, arXiv:1203.4374) surveys all VoIP steganography methods including codec-based, timing, and protocol-field approaches. Active steganalysis research using deep learning (FCEM, 2024).

**Production readiness:** Experimental

**Security status:** Caution — Deep learning steganalysis achieving high detection rates on QIM-based methods

**Community acceptance:** Emerging — Growing research community

---

### WireGuard Steganography

**Goal:** Hide data in WireGuard VPN protocol fields or timing.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **WireGuard Stego** | 2020 | Handshake initiator/responder fields, padding | Modern VPN [[1]](https://www.wireguard.com/papers/wireguard.pdf) |

**State of the art:** Exploratory research leveraging WireGuard's encrypted, fixed-format handshake and data packets; no dedicated published paper confirmed — references the WireGuard protocol spec as the technical basis.

**Production readiness:** Research

**Security status:** Secure — WireGuard's encryption limits detectability; channel capacity very low

**Community acceptance:** Emerging — No peer-reviewed steganography paper confirmed; based on general network steganography principles

---

### Combining Different Existing Methods for Describing Steganography Hiding Methods

**Goal:** Provide a tutorial on combining existing descriptive methods and taxonomies for steganography techniques.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Combining Different Existing Methods for Describing Steganog** | 2025 | cs.CR, cs.NI | Steffen Wendzel et al. [[1]](https://arxiv.org/abs/2506.01700) |

**State of the art:** Tutorial paper explaining how to combine existing taxonomies and description methods for steganography. Addresses overlapping terminology in literature and helps categorize novel hiding approaches. To appear at ARES 2025.

**Production readiness:** Research
Tutorial/survey paper; no implementation.

**Security status:** N/A
Survey paper; no security claims.

**Community acceptance:** Emerging
Co-authored by leading steganography researchers; to be published at ARES 2025.

---

### Quantum Hilbert Transform

**Goal:** Introduce quantum analogue of Hilbert transform and apply to quantum steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Quantum Hilbert Transform** | 2025 | cs.CR, cs.DM, cs.NI | Nitin Jha, Abhishek Parakh [[1]](https://arxiv.org/abs/2505.23581) |

**State of the art:** First quantum analogue of Hilbert transform (QHT). Bridges classical phase-shift techniques with quantum operations. Applied to quantum steganography protocol. Opens pathways for quantum signal processing and secure information hiding.

**Production readiness:** Research
Very recent preprint; no implementation.

**Security status:** Caution
Novel quantum approach; security analysis pending.

**Community acceptance:** Emerging
First quantum Hilbert transform; limited peer review.

---

### RFNNS: Robust Fixed Neural Network Steganography with Universal Text-to-Image Models

**Goal:** Improve robustness of Fixed Neural Network Steganography (FNNS) while preserving visual quality.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **RFNNS: Robust Fixed Neural Network Steganography with Univer** | 2025 | cs.MM | Yu Cheng et al. [[1]](https://arxiv.org/abs/2505.04116) |

**State of the art:** Uses texture-aware localization to embed perturbations in complex texture regions. Robust steganographic perturbation generation (RSPG) enhances decoding under attacks. 23% SSIM improvement under common attacks; LPIPS reduced to 39% of SOTA against unknown attacks.

**Production readiness:** Research
Very recent preprint; no implementation available.

**Security status:** Caution
Research prototype; security analysis in paper.

**Community acceptance:** Emerging
Novel robust FNNS approach.

---

### Multichannel Steganography: A Provably Secure Hybrid Steganographic Model for Secure Communication

**Goal:** purely distortion-free or invertible schemes fail under the same threat model, underscoring the necessity of hybrid designs.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Multichannel Steganography: A Provably Secure Hybrid Stegano** | 2025 | cs.CR, cs.MM | Obinna Omego, Michal Bosy [[1]](https://arxiv.org/abs/2501.04511) |

**State of the art:** Hybrid framework combining cover synthesis and modification. Secret-seeded PRNG with Markov-chain generates cover parameters; variance-aware LSB embedding maintains natural statistical properties. Formal MC-ATTACK model proves negligible distinguishing advantage. PSNR~100dB, SSIM>0.99, BER<5×10⁻³.

**Production readiness:** Research
Academic preprint; no implementation available.

**Security status:** Secure
Provably secure under standard assumptions; formal proof provided.

**Community acceptance:** Emerging
Novel provably secure hybrid approach.

---

### Cover-separable Fixed Neural Network Steganography via Deep Generative Models

**Goal:** Reduce stego-image distortion in Fixed Neural Network Steganography (FNNS) while maintaining no training requirement.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Cover-separable Fixed Neural Network Steganography via Deep ** | 2024 | cs.CR, cs.CV | Guobiao Li et al. [[1]](https://arxiv.org/abs/2407.11405) |

**State of the art:** Uses Steganographic Perturbation Search (SPS) to encode secret data into perturbations. Receiver reproduces cover image using deep generative models and key to separate perturbation. Better visual quality and undetectable. Can hide multiple secret images for different receivers. Accepted at ACMMM 2024.

**Production readiness:** Research
Academic research; implementation details in paper.

**Security status:** Caution
FNNS-based; security against steganalysis demonstrated.

**Community acceptance:** Emerging
Accepted at ACMMM 2024; notable FNNS improvement.

---

### Synthetic Embedding of Hidden Information in Industrial Control System Network Protocols for Evaluation of Steganographic Malware

**Goal:** Generate synthetic steganographic network data for training and evaluating defense mechanisms against ICS steganographic malware.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Synthetic Embedding of Hidden Information in Industrial Cont** | 2024 | cs.CR | Tom Neubert et al. [[1]](https://arxiv.org/abs/2406.19338) |

**State of the art:** Generates synthetic steganographic network data for ICS protocols. Enables manipulation of network packets anywhere needed. Outperforms state-of-the-art in embedding speed. Addresses need for training data without real-time embedding in production ICS networks.

**Production readiness:** Research
Academic prototype; concept for data generation.

**Security status:** Caution
Tool for generating test data; not for covert communication.

**Community acceptance:** Emerging
Important for ICS security research.

---

### Purified and Unified Steganographic Network

**Goal:** Hide steganographic networks inside ordinary ML networks for imperceptible transmission.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Purified and Unified Steganographic Network** | 2024 | cs.CR, cs.CV | Guobiao Li et al. [[1]](https://arxiv.org/abs/2402.17210) |

**State of the art:** PUSNet performs ordinary ML task (image denoising) in purified network. Using different keys, it switches to steganographic mode for secret embedding/recovery. Formulated as sparse weight filling problem. Code available on GitHub. Accepted at CVPR 2024.

**Production readiness:** Experimental
Has GitHub implementation available.

**Security status:** Caution
Network hidden in another network; novel approach.

**Community acceptance:** Emerging
Accepted at CVPR 2024; innovative concept.

---

### Towards Deep Network Steganography: From Networks to Networks

**Goal:** Covertly transmit DNN models trained for secret-learning tasks through public channels.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Deep Network Steganography: From Networks to Network** | 2023 | cs.CR, cs.AI | Guobiao Li et al. [[1]](https://arxiv.org/abs/2307.03444) |

**State of the art:** First deep network steganography scheme. Disguises secret-learning task as ordinary stego-learning task. Uses gradient-based filter insertion to insert interference filters into secret DNN to form stego DNN. Supports both intra-task and inter-task steganography.

**Production readiness:** Research
Academic research; no implementation available.

**Security status:** Caution
Novel approach; security analysis in paper.

**Community acceptance:** Emerging
First work on DNN model steganography.

---

### Unified Description for Network Information Hiding Methods

**Goal:** Create a unified framework for describing network steganography methods to enable comparison.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Unified Description for Network Information Hiding Methods** | 2017 | cs.CR | Steffen Wendzel, Wojciech Mazurczyk, Sebastian Zander [[1]](https://arxiv.org/abs/1512.07438) |

**State of the art:** First unified description method for network steganography. Based on comprehensive analysis of existing publications. Enables easier categorization, comparison, and evaluation of novelty. Published in J.UCS.

**Production readiness:** Research
Survey/taxonomy paper; no implementation.

**Security status:** N/A
Taxonomy paper; no security claims.

**Community acceptance:** Widely trusted
Classic paper by leading researchers; widely cited.

---

### A Second Order Derivatives based Approach for Steganography

**Goal:** Improve steganography by using second-order derivatives as distortion function to better identify embedding regions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Second Order Derivatives based Approach for Steganography** | 2016 | cs.MM | Jean-François Couchot et al. [[1]](https://arxiv.org/abs/1611.08397) |

**State of the art:** Uses second-order derivatives to evaluate level curves. Modifications in texture/noisy regions are less detectable than in smooth regions. Two methods for computing partial derivatives. Accepted at SECRYPT 2016.

**Production readiness:** Research
Academic research; no implementation.

**Security status:** Caution
Theoretical approach; limited evaluation.

**Community acceptance:** Niche
Academic paper; specialized audience.

---

### Why Johnny Can't Use Stego: a Human-oriented Perspective on the Application of Steganography

**Goal:** Analyze steganography application from individual human perspective.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Why Johnny Can't Use Stego: a Human-oriented Perspective on ** | 2016 | cs.CR | Steffen Wendzel [[1]](https://arxiv.org/abs/1609.06664) |

**State of the art:** Presents a phase model explaining preconditions, decision-making, and termination of steganographic communication. Can determine if an individual can/wants to use steganography. Useful for teaching and research categorization.

**Production readiness:** Research
Conceptual/framework paper.

**Security status:** N/A
Human factors research; no security claims.

**Community acceptance:** Emerging
Human-centered steganography research.

---

### Trends toward real-time network data steganography

**Goal:** Review classical network steganography and introduce real-time network data steganography concept.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Trends toward real-time network data steganography** | 2016 | cs.MM, cs.CR | James Collins, Sos Agaian [[1]](https://arxiv.org/abs/1604.02778) |

**State of the art:** Reviews classical network steganography methods. Introduces real-time network data steganography concept. Compares classical methods with endpoint multimedia embedding. Provides framework for real-time covert network operations.

**Production readiness:** Research
Survey paper; conceptual framework.

**Security status:** N/A
Survey paper; no security claims.

**Community acceptance:** Emerging
Introduces new research direction.

---

### StegBlocks: ensuring perfect undetectability of network steganography

**Goal:** Define general concept for constructing perfectly undetectable network steganography methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegBlocks: ensuring perfect undetectability of network steg** | 2015 | cs.MM, cs.CR | Wojciech Fraczek, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1506.02311) |

**State of the art:** General approach for constructing undetectable network steganography. Uses objects with defined properties based on specific protocols. Based on rules of general steganography. Accepted at IWCC 2015.

**Production readiness:** Research
Theoretical framework.

**Security status:** Secure
Theoretically grounded approach to perfect detectability.

**Community acceptance:** Emerging
Accepted at IWCC 2015.

---

### Hidden and Uncontrolled - On the Emergence of Network Steganographic Threats

**Goal:** Analyze potential malicious use of network steganography by malware and other threats.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hidden and Uncontrolled - On the Emergence of Network Stegan** | 2014 | cs.CR | Steffen Wendzel et al. [[1]](https://arxiv.org/abs/1407.2029) |

**State of the art:** Survey of network steganography for malicious purposes (malware, data leakage, illegal content). Discusses countermeasures and challenges. Published at ISSE 2014.

**Production readiness:** Research
Survey/threat analysis paper.

**Security status:** N/A
Threat analysis; no security claims.

**Community acceptance:** Widely trusted
Classic paper on network steganography threats.

---

### On Importance of Steganographic Cost For Network Steganography

**Goal:** Introduce steganographic cost as metric for carrier degradation in network steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On Importance of Steganographic Cost For Network Steganograp** | 2014 | cs.MM, cs.CR | Wojciech Mazurczyk et al. [[1]](https://arxiv.org/abs/1406.2519) |

**State of the art:** Introduces steganographic cost as indicator for carrier degradation (similar to MSE/PSNR for digital media). Analyzes single and multi-method cost. Helps analyze relationships between steganographic methods.

**Production readiness:** Research
Theoretical framework.

**Security status:** N/A
Metric/framework paper.

**Community acceptance:** Emerging
Novel metric for network steganography.

---

### Adaptive Software Radio Steganography

**Goal:** Present adaptable steganography method for digital radio communication at physical layer.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Adaptive Software Radio Steganography** | 2013 | cs.MM | David E. Robillard [[1]](https://arxiv.org/abs/1304.7324) |

**State of the art:** Physical layer steganography for radio. Protocol-independent (unlike higher layer methods). Adaptive covertness controlled by single continuous parameter. Several variations evaluated by simulation.

**Production readiness:** Research
Theoretical/simulation work.

**Security status:** Caution
Physical layer approach; limited evaluation.

**Community acceptance:** Niche
Early physical layer radio steganography.

**Goal:** Present evolution of steganography from ancient times to present day with emphasis on network steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Development Trends in Steganography** | 2013 | cs.MM | Elzbieta Zielinska, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1202.5289) |

**State of the art:** Survey of steganography evolution. Covers digital media and network protocol carriers. Traces development from ancient techniques to modern methods. Important for understanding field.

**Production readiness:** Research
Survey paper.

**Security status:** N/A
Survey paper.

**Community acceptance:** Widely trusted
Classic survey by leading researchers.

---

### Principles and Overview of Network Steganography

**Goal:** Present basic principles and classification of network steganography methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Principles and Overview of Network Steganography** | 2012 | cs.CR | Jozef Lubacz, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1207.0917) |

**State of the art:** Foundational paper presenting basic principles of network steganography and classification of methods. Key reference for the field.

**Production readiness:** Research
Survey paper.

**Security status:** N/A
Survey paper.

**Community acceptance:** Widely trusted
Classic foundational paper.

---

### Direct Sequence Spread Spectrum Steganographic Scheme for IEEE 802.15.4

**Goal:** Create covert channel in IEEE 802.15.4 WPAN using Direct Sequence Spread Spectrum.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Direct Sequence Spread Spectrum Steganographic Scheme for IE** | 2011 | cs.CR | Elzbieta Zielinska, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4230) |

**State of the art:** Uses illicit DSSS code sequences for steganographic transmission. Balances disclosure probability, robustness, and data rate. Comparable to raw data rate with minimal impact on receiver sensitivity.

**Production readiness:** Research
Theoretical analysis.

**Security status:** Caution
Older approach; limited modern evaluation.

**Community acceptance:** Niche
Early work on 802.15.4 steganography.

---

### How Hidden Can Be Even More Hidden?

**Goal:** The paper presents Deep Hiding Techniques (DHTs) that define general techniques that can be applied to every network steganography method to improve its undetectability and make steganogram extract...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **How Hidden Can Be Even More Hidden?** | 2011 | cs.CR | Wojciech Fraczek, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4065) |

**State of the art:** Presents Deep Hiding Techniques (DHTs) to improve network steganography detectability and extraction resistance. Defines five groups of techniques with examples. First systematic approach to general steganography hardening.

**Production readiness:** Research
Framework paper.

**Security status:** N/A
Framework paper.

**Community acceptance:** Emerging
Foundational work on steganography hardening.

---

### Sending Hidden Data via Google Suggest

**Goal:** Use Google Suggest as hidden data carrier for network steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Sending Hidden Data via Google Suggest** | 2011 | cs.CR | Piotr Bialczak, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4062) |

**State of the art:** StegSuggest uses Google Suggest suggestions as carrier. Uses TCP Window Scale and Timestamp options. Can embed ~100 bits per suggestions list.

**Production readiness:** Research
Theoretical work.

**Security status:** Caution
Uses external service; may be blocked.

**Community acceptance:** Niche
Novel carrier approach.

---

### Stegobot: construction of an unobservable communication network leveraging social behavior

**Goal:** using social networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegobot: construction of an unobservable communication netw** | 2011 | cs.CR, cs.NI, cs.SI | Shishir Nagaraja et al. [[1]](https://arxiv.org/abs/1107.2031) |

**State of the art:** Foundational work in social network-based steganography. Later work expanded on botnet architectures and cover selection strategies, but Stegobot remains a key reference for overlay steganographic networks.

**Production readiness:** Research
Academic prototype demonstrating feasibility; no production deployment.

**Security status:** Caution
Traffic analysis can detect unusual image sharing patterns; social graph metadata may reveal botnet structure.

**Community acceptance:** Niche
Highly cited in network steganography literature (~400 citations); influential but specialized.

---

### Proposed System for data hiding using Cryptography and Steganography Proposed System for data hiding using Cryptography and Steganography

**Goal:** Steganography and Cryptography are two popular ways of sending vital information in a secret way.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Proposed System for data hiding using Cryptography and Stega** | 2010 | cs.CR | Dipti Kapoor Sarmah, Neha Bajpai [[1]](https://arxiv.org/abs/1009.2826) |

**State of the art:** Early work in TCP retransmission-based covert channels. The concept influenced later work on protocol-level steganography, though modern methods use more sophisticated timing channels.

**Production readiness:** Research
Proof-of-concept implementation; no production tools.

**Security status:** Broken
Retransmission behavior is detectable by network monitoring; modern intrusion detection systems can identify anomalous retransmission patterns.

**Community acceptance:** Niche
Cited in network steganography surveys; superseded by more sophisticated methods.

---

### Retransmission Steganography Applied

**Goal:** This paper presents experimental results of the implementation of network steganography method called RSTEG (Retransmission Steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Retransmission Steganography Applied** | 2010 | cs.CR | Wojciech Mazurczyk, Milosz Smolarczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1007.0767) |

**State of the art:** Foundational work in SCTP steganography. Remains the primary reference for multi-homing and multi-streaming based covert channels, though SCTP adoption remains limited in practice.

**Production readiness:** Research
Theoretical analysis; no widely available implementations.

**Security status:** Caution
SCTP is rarely deployed at scale, limiting practical utility; steganographic methods may be detectable with deep packet inspection.

**Community acceptance:** Niche
Limited adoption of SCTP means limited follow-up work; cited primarily in academic surveys.

---

### Stream Control Transmission Protocol Steganography

**Goal:** Stream Control Transmission Protocol (SCTP) is a new transport layer protocol that is due to replace TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) protocols in future IP netw...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stream Control Transmission Protocol Steganography** | 2010 | cs.CR | Wojciech Fraczek, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1006.0247) |

**State of the art:** First inter-protocol steganography method using ARP and TCP together with Etherleak vulnerability. Demonstrated feasibility but requires specific network conditions (Etherleak-affected hardware).

**Production readiness:** Research
Proof-of-concept only; modern hardware has largely patched Etherleak.

**Security status:** Superseded
Etherleak vulnerability has been patched in most modern network cards; method is largely historical.

**Community acceptance:** Niche
Important historical contribution; rarely used today due to patched vulnerabilities.

---

### Information Hiding Using Improper Frame Padding

**Goal:** Hiding information in network traffic may lead to leakage of confidential information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information Hiding Using Improper Frame Padding** | 2010 | cs.CR | Bartosz Jankowski, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1005.1925) |

**State of the art:** Theoretically optimal coding method for +/-1 steganography using Z2Z4-linear codes. Achieves theoretical upper bound on hiding capacity for distortion-constrained scenarios.

**Production readiness:** Research
Theoretical contribution; no production implementations available.

**Security status:** Secure
Theoretical framework; security depends on embedding algorithm using the codes.

**Community acceptance:** Niche
Important theoretical contribution but limited practical adoption; cited in coding-theoretic steganography work.

---

### Perfect Z2Z4-linear codes in Steganography

**Goal:** Steganography is an information hiding application which aims to hide secret data imperceptibly into a commonly used media.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Perfect Z2Z4-linear codes in Steganography** | 2010 | cs.IT, cs.CR | H. Rifà-Pous, J. Rifà, L. Ronquillo [[1]](https://arxiv.org/abs/1002.0026) |

**State of the art:** First systematic treatment of IP fragmentation and PMTUD-based steganography. Methods remain relevant for IPv4/IPv6 transition scenarios but see limited practical use.

**Production readiness:** Research
Theoretical framework; no production implementations.

**Security status:** Caution
Fragmentation-based channels can be detected by network analyzers; firewall rules can block fragment-based tunnels.

**Community acceptance:** Niche
Foundational work in IP-layer steganography; cited in network covert channel surveys.

---

### Steganography in Handling Oversized IP Packets

**Goal:** This paper identifies new class of network steganography methods that utilize mechanisms to handle oversized packets in IP networks: IP fragmentation, PMTUD (Path MTU Discovery) and PLPMTUD (Packet...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography in Handling Oversized IP Packets** | 2009 | cs.CR | Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/0907.0313) |

**State of the art:** First systematic treatment of IP fragmentation and PMTUD-based steganography. Methods remain relevant for IPv4/IPv6 transition scenarios but see limited practical use.

**Production readiness:** Research
Theoretical framework; no production implementations.

**Security status:** Caution
Fragmentation-based channels can be detected by network analyzers; firewall rules can block fragment-based tunnels.

**Community acceptance:** Niche
Foundational work in IP-layer steganography; cited in network covert channel surveys.

---

### SecMon: End-to-End Quality and Security Monitoring System

**Goal:** a self-organizing capability.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SecMon: End-to-End Quality and Security Monitoring System** | 2008 | cs.MM | Tomasz Ciszkowski et al. [[1]](https://arxiv.org/abs/0804.0134) |

**State of the art:** Early work combining watermarking and network steganography for VoIP QoS. Novel approach but superseded by dedicated VoIP security frameworks and SDN-based monitoring.

**Production readiness:** Research
Proof-of-concept; not deployed in production VoIP systems.

**Security status:** Caution
Method depends on steganographic channels that may be detected; not a standalone security solution.

**Community acceptance:** Niche
Pioneering work in covert channel-based monitoring; limited follow-up due to complexity.

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

### Steganography: A Secure way for Transmission in Wireless Sensor Networks

**Goal:** network Internet is very sensitive and vulnerable to various attacks and risks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography: A Secure way for Transmission in Wireless Sen** | 2015 | cs.MM | Khan Muhammad [[1]](https://arxiv.org/abs/1511.08865) |

**State of the art:** Addressing the security concerns in wireless sensor networks (WSN) is a challenging task, which has attracted the attent

**Production readiness:** Research
Academic research prototype; evaluation in progress.

**Security status:** Caution
Security properties under evaluation.

**Community acceptance:** Emerging
Preprint; peer review ongoing.
---

## Alternative Protocols

---

### 5G/6G Cellular

**Goal:** Covert channels in cellular networks.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SteaLTE** | 2021 | Full-stack wireless steganography disguising data as noise | Private 5G [[1]](https://arxiv.org/abs/2102.05606) |

**State of the art:** Bonati et al. (IEEE INFOCOM 2021) presented SteaLTE, the first full-stack cellular steganography system enabling private network slices invisible to adversarial receivers.

**Production readiness:** Research

**Security status:** Secure — Data disguised as noise; requires physical layer access to detect

**Community acceptance:** Emerging

---

### Wi-Fi CSI

**Goal:** Embed in Wi-Fi Channel State Information.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Wi-Fi CSI** | 2026 | CSI quotient with learned FIR filters | High capacity [[1]](https://arxiv.org/abs/2604.20521) |

**State of the art:** Guo et al. (arXiv:2604.20521, Apr 2026) propose embedding secrets in the quotient of consecutive CSI measurements using an encoder-decoder neural network; prototype on ANTSDR and ESP32 hardware.

**Production readiness:** Research

**Security status:** Secure — Modifications blend with natural channel variation

**Community acceptance:** Emerging

---

### CYPRESS

**Goal:** High-speed covert channels mounting on regular packets.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CYPRESS** | 2025 | Secret network entity packets ride inside regular visible packets | 1.6 MB/s [[1]](https://arxiv.org/abs/2511.06540) |

**State of the art:** Shahini & Ricci (arXiv:2511.06540, Nov 2025) demonstrate practical covert channels far exceeding prior work in throughput, protocol-agnostic and deployable in real networks.

**Production readiness:** Research

**Security status:** Caution — High throughput increases statistical detectability; no published countermeasure evaluation yet

**Community acceptance:** Emerging

---

### HICCUPS

**Goal:** Hide data in WLAN networks using corrupted frames.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HICCUPS** | 2003 | Hidden Communication System for Corrupted Networks | WLAN steganography [[1]](https://www.semanticscholar.org/paper/HICCUPS:-Hidden-Communication-System-for-Corrupted-Szczypiorski/cb42073a770527059d2b597560547bf926777c7f) |

**State of the art:** First practical WLAN steganography.

**Production readiness:** Experimental

**Implementations:**
- [HICCUPS](http://www.tele.pw.edu.pl/~krzysiek/pdf/steg-seminar-2003.pdf) — Original paper

**Security status:** Caution — Uses corrupted packets

**Community acceptance:** Niche

---

### Inter-protocol Steganography

**Goal:** Use relationships between multiple protocols for covert channels.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **PadSteg** | 2011 | ARP + TCP Etherleak padding cross-correlation | First inter-protocol system [[1]](https://arxiv.org/abs/1104.0422) |

**State of the art:** Jankowski, Mazurczyk & Szczypiorski (arXiv:1104.0422, 2011) introduced PadSteg as the first inter-protocol steganography system, exploiting Etherleak in LAN ARP/TCP interactions. Harder to detect than single-protocol methods.

**Production readiness:** Research

**Security status:** Secure — Requires cross-protocol correlation to detect

**Community acceptance:** Emerging

---

### Quantum Gatekeeper

**Goal:** Multi-factor context-bound image steganography with VQC-based key derivation on quantum hardware.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Quantum Gatekeeper** | 2026 | LSB embedding + variational quantum circuit key derivation | Quantum-resistant [[1]](https://arxiv.org/abs/2604.26413) |

**State of the art:** Tomar & Kumar (arXiv:2604.26413, Apr 2026) combine LSB steganography with a deterministic VQC-derived gate key; payload recovery requires four factors (password, shared secret, context string, reference image).

**Production readiness:** Research

**Security status:** Secure — VQC-derived key; silent rejection on any factor mismatch

**Community acceptance:** Emerging

---

### Intellicise Wireless Network

**Goal:** Coverless semantic steganography for 6G intelligent wireless networks using Agentic AI.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **AgentSemSteCom** | 2026 | Agentic AI + diffusion models + semantic codec | Coverless, no key required [[1]](https://arxiv.org/abs/2601.16472) |

**State of the art:** Meng et al. (arXiv:2601.16472, Jan 2026) propose AgentSemSteCom: semantic extraction, digital token controlled reference image generation, and coverless steganography that eliminates the need for cover images and private semantic keys.

**Production readiness:** Research

**Security status:** Secure — No cover images or private keys to infer; resistant to traditional steganalysis

**Community acceptance:** Emerging

---

### VeriPHY

**Goal:** Physical layer signal authentication for wireless communication using steganographic signatures.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **VeriPHY** | 2025 | Deep learning + steganography in I/Q signals | 5G device identification [[1]](https://arxiv.org/abs/2508.09213) |

**State of the art:** Embeds unique pseudo-random signatures in wireless I/Q transmissions using GMM sampling.

**Production readiness:** Experimental

**Implementations:** Academic prototypes only

**Security status:** Secure — Unique per-device signatures

**Community acceptance:** Emerging

### Hiding Data in Plain Sight: Undetectable Wireless Communications Through Pseudo-Noise Asymmetric Shift Keying

**Goal:** Undetectable wireless transmissions are fundamental to avoid eavesdroppers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Data in Plain Sight: Undetectable Wireless Communicat** | 2019 | cs.CR, cs.NI, eess.SP | Salvatore D'Oro, Francesco Restuccia, Tommaso Melodia [[1]](https://arxiv.org/abs/1905.02250) |

**State of the art:** State-of-the-art in wireless steganography using PN-ASK modulation. First method to demonstrate covert transmission over live IEEE 802.11g WiFi with 8x throughput improvement over prior art. Published at IEEE INFOCOM 2019.

**Production readiness:** Experimental
Proof-of-concept with USRP SDR implementation; no production wireless steganography tools.

**Security status:** Caution
Method is experimentally demonstrated to be undetectable byagnostic receivers but may be vulnerable to advanced RF fingerprinting.

**Community acceptance:** Emerging
Published at top-tier venue (INFOCOM); growing interest in wireless covert channels.

---

### "The Good, The Bad And The Ugly": Evaluation of Wi-Fi Steganography

**Goal:** Propose evaluation method for Wi-Fi steganography using "moving observer" concept with three levels of undetectability.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **"The Good, The Bad And The Ugly": Evaluation of Wi-Fi Stegan** | 2015 | cs.MM, cs.CR | Krzysztof Szczypiorski, Artur Janicki, Steffen Wendzel [[1]](https://arxiv.org/abs/1508.04978) |

**State of the art:** Reviews Wi-Fi steganography state-of-the-art. Introduces "moving observer" concept for evaluation. Proposes MoveSteg detection system. Published at ICNIT 2015.

**Production readiness:** Research
Survey/evaluation paper.

**Security status:** N/A
Evaluation framework; no security claims.

**Community acceptance:** Emerging
Wi-Fi steganography evaluation framework.

---

## Network Stego Tools

---

### ST3GG

**Goal:** All-in-one network steganography suite covering DNS, ICMP, TCP header fields, HTTP, UDP, and 20+ covert channel detection functions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ST3GG** | 2024 | Multi-protocol covert channel toolkit | Modular: each protocol is a plugin; includes detection [[1]](https://github.com/elder-plinius/ST3GG) |

**State of the art:** Most comprehensive open-source network stego toolkit. Covers DNS TXT encoding, ICMP payload hiding, TCP timestamp/sequence channels, and HTTP header steganography in one tool.

**Production readiness:** Experimental
Active development; 2024 release; growing community.

**Implementations:**
- [elder-plinius/ST3GG](https://github.com/elder-plinius/ST3GG) ⭐ 1.4k — Python

**Security status:** Caution
DPI and behavioral analysis can detect covert channels; encrypted payload adds confidentiality.

**Community acceptance:** Emerging
Rapidly growing interest since 2024 release; not yet peer-reviewed.

---

### icmptunnel

**Goal:** Tunnel IP traffic transparently over ICMP echo/reply packets to bypass firewalls that block all traffic except ping.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **icmptunnel** | 2015 | IP-in-ICMP payload encapsulation | Creates TUN interface; fully transparent TCP/UDP over ping [[1]](https://github.com/DhavalKapil/icmptunnel) |

**State of the art:** Most widely referenced open-source ICMP tunnel. Encapsulates full IP packets inside ICMP payload. Requires root on both ends; works across strict firewalls that permit ping.

**Production readiness:** Mature
Stable C implementation; well-documented setup; used in penetration testing.

**Implementations:**
- [DhavalKapil/icmptunnel](https://github.com/DhavalKapil/icmptunnel) ⭐ 3.3k — C

**Security status:** Caution
Detectable by DPI inspecting ICMP payload size and rate anomalies. Not encrypted by default — combine with VPN payload.

**Community acceptance:** Widely trusted
Most-starred open-source ICMP tunnel; referenced in network steganography research and pentesting courses.

---

### ptunnel-ng

**Goal:** Tunnel reliable TCP connections through ICMP echo/reply packets with password authentication and reverse tunneling support.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ptunnel-ng** | 2017 | TCP-over-ICMP with HMAC authentication | Password protection; reverse tunnel mode; successor to original ptunnel [[1]](https://github.com/utoni/ptunnel-ng) |

**State of the art:** Modernized successor to the original ptunnel (2004). Adds HMAC-MD5 authentication and reverse tunneling. Widely used in penetration testing engagements.

**Production readiness:** Mature
Actively maintained; packaged in Kali Linux.

**Implementations:**
- [utoni/ptunnel-ng](https://github.com/utoni/ptunnel-ng) ⭐ 576 — C

**Security status:** Caution
ICMP traffic pattern detectable by DPI; payload not encrypted (use with SSH forwarding over the tunnel).

**Community acceptance:** Widely trusted
Included in Kali Linux; standard tool for ICMP covert channel demonstrations.

---

### hans

**Goal:** Tunnel IP over ICMP (like icmptunnel) with client/server mode, multiple simultaneous clients, and optional password authentication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **hans** | 2009 | IP-over-ICMP with multi-client server mode | Handles multiple clients; password auth; Linux and macOS support [[1]](https://github.com/friedrich/hans) |

**State of the art:** Alternative to icmptunnel with multi-client support. Creates TUN/TAP interface. Useful where icmptunnel's single-client limitation is a constraint.

**Production readiness:** Mature
Stable; no active development since 2014 but well-tested.

**Implementations:**
- [friedrich/hans](https://github.com/friedrich/hans) ⭐ 472 — C++

**Security status:** Caution
Same ICMP covert channel detectability as icmptunnel; password auth prevents unauthorized use.

**Community acceptance:** Niche
Alternative to icmptunnel; used in scenarios requiring multi-client ICMP tunneling.

---

### fraud-bridge

**Goal:** Covert tunnel over ICMP, DNS, or NTP protocols supporting both IPv4 and IPv6, designed for bypassing restrictive firewalls.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **fraud-bridge** | 2019 | Multi-protocol covert relay (ICMP/DNS/NTP over IPv4/IPv6) | Protocol agnostic; swap transport without changing endpoints [[1]](https://github.com/stealth/fraud-bridge) |

**State of the art:** Unique multi-protocol approach — use ICMP, DNS, or NTP as covert transport interchangeably. IPv6 support differentiates it from icmptunnel/hans. Designed for adversarial bypass scenarios.

**Production readiness:** Experimental
Active development; targeted at advanced users and security researchers.

**Implementations:**
- [stealth/fraud-bridge](https://github.com/stealth/fraud-bridge) ⭐ 233 — C++

**Security status:** Caution
Protocol diversity makes it harder to block; each transport detectable by dedicated DPI signatures.

**Community acceptance:** Niche
Used in offensive security research; less mainstream than icmptunnel but covers more protocols.

---

