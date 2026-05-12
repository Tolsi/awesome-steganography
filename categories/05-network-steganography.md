# Network Steganography

<!-- TOC -->
## Contents (63 algorithms)

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

**[Protocol-specific](#protocol-specific)**
- [QuicCourier](#quiccourier)
- [LACK](#lack)
- [SteganoRTP](#steganortp)
- [VoIP Steganography](#voip-steganography)
- [WireGuard Steganography](#wireguard-steganography)

**[Alternative Protocols](#alternative-protocols)**
- [5G/6G Cellular](#56g-cellular)
- [Wi-Fi CSI](#wi-fi-csi)
- [CYPRESS](#cypress)
- [HICCUPS](#hiccups)
- [Inter-protocol Steganography](#inter-protocol-steganography)
- [Quantum Gatekeeper](#quantum-gatekeeper)
- [Intellicise Wireless Network](#intellicise-wireless-network)
- [VeriPHY](#veriphy)

**[Recent arXiv Papers (2024–2026)](#recent-arxiv-papers-20242026)**
- [Combining Different Existing Methods for Describing Steganog...](#combining-different-existing-methods-for-describing-steganography-hiding-methods)
- [Quantum Hilbert Transform](#quantum-hilbert-transform)
- [RFNNS: Robust Fixed Neural Network Steganography with Univer...](#rfnns-robust-fixed-neural-network-steganography-with-universal-text-to-image-models)
- [Multichannel Steganography: A Provably Secure Hybrid Stegano...](#multichannel-steganography-a-provably-secure-hybrid-steganographic-model-for-secure-communication)
- [Cover-separable Fixed Neural Network Steganography via Deep ...](#cover-separable-fixed-neural-network-steganography-via-deep-generative-models)
- [Synthetic Embedding of Hidden Information in Industrial Cont...](#synthetic-embedding-of-hidden-information-in-industrial-control-system-network-protocols-for-evaluation-of-steganographic-malware)
- [Purified and Unified Steganographic Network](#purified-and-unified-steganographic-network)
- [Towards Deep Network Steganography: From Networks to Network...](#towards-deep-network-steganography-from-networks-to-networks)
- [DWT-GBT-SVD-based Robust Speech Steganography](#dwt-gbt-svd-based-robust-speech-steganography)
- [A Lightweight Adaptable DNS Channel for Covert Data Transmis...](#a-lightweight-adaptable-dns-channel-for-covert-data-transmission)
- [Deep Residual Neural Networks for Image in Speech Steganogra...](#deep-residual-neural-networks-for-image-in-speech-steganography)
- [Hide and Speak: Towards Deep Neural Networks for Speech Steg...](#hide-and-speak-towards-deep-neural-networks-for-speech-steganography)
- [Hiding Data in Plain Sight: Undetectable Wireless Communicat...](#hiding-data-in-plain-sight-undetectable-wireless-communications-through-pseudo-noise-asymmetric-shift-keying)
- [AAG-Stega: Automatic Audio Generation-based Steganography](#aag-stega-automatic-audio-generation-based-steganography)
- [Unified Description for Network Information Hiding Methods](#unified-description-for-network-information-hiding-methods)
- [A Second Order Derivatives based Approach for Steganography](#a-second-order-derivatives-based-approach-for-steganography)
- [Why Johnny Can't Use Stego: a Human-oriented Perspective on ...](#why-johnny-cant-use-stego-a-human-oriented-perspective-on-the-application-of-steganography)
- [Trends toward real-time network data steganography](#trends-toward-real-time-network-data-steganography)
- ["The Good, The Bad And The Ugly": Evaluation of Wi-Fi Stegan...](#the-good-the-bad-and-the-ugly-evaluation-of-wi-fi-steganography)
- [StegBlocks: ensuring perfect undetectability of network steg...](#stegblocks-ensuring-perfect-undetectability-of-network-steganography)
- [Micro protocol engineering for unstructured carriers: On the...](#micro-protocol-engineering-for-unstructured-carriers-on-the-embedding-of-steganographic-control-protocols-into-audio-transmissions)
- [Hidden and Uncontrolled - On the Emergence of Network Stegan...](#hidden-and-uncontrolled-on-the-emergence-of-network-steganographic-threats)
- [On Importance of Steganographic Cost For Network Steganograp...](#on-importance-of-steganographic-cost-for-network-steganography)
- [Adaptive Software Radio Steganography](#adaptive-software-radio-steganography)
- [Development Trends in Steganography](#development-trends-in-steganography)
- [Principles and Overview of Network Steganography](#principles-and-overview-of-network-steganography)
- [Dynamic Pattern Based Image Steganography](#dynamic-pattern-based-image-steganography)
- [Direct Sequence Spread Spectrum Steganographic Scheme for IE...](#direct-sequence-spread-spectrum-steganographic-scheme-for-ieee-802154)
- [How Hidden Can Be Even More Hidden?](#how-hidden-can-be-even-more-hidden)
- [Sending Hidden Data via Google Suggest](#sending-hidden-data-via-google-suggest)
- [Stegobot: construction of an unobservable communication netw...](#stegobot-construction-of-an-unobservable-communication-network-leveraging-social-behavior)
- [Proposed System for data hiding using Cryptography and Stega...](#proposed-system-for-data-hiding-using-cryptography-and-steganography-proposed-system-for-data-hiding-using-cryptography-and-steganography)
- [Retransmission Steganography Applied](#retransmission-steganography-applied)
- [Stream Control Transmission Protocol Steganography](#stream-control-transmission-protocol-steganography)
- [Information Hiding Using Improper Frame Padding](#information-hiding-using-improper-frame-padding)
- [Perfect Z2Z4-linear codes in Steganography](#perfect-z2z4-linear-codes-in-steganography)
- [Steganography in Handling Oversized IP Packets](#steganography-in-handling-oversized-ip-packets)
- [SecMon: End-to-End Quality and Security Monitoring System](#secmon-end-to-end-quality-and-security-monitoring-system)

**[Network Stego Tools](#network-stego-tools)**
- [ST3GG](#st3gg)
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

## Recent arXiv Papers (2024–2026)

---

### Combining Different Existing Methods for Describing Steganography Hiding Methods

**Goal:** The proliferation of digital carriers that can be exploited to conceal arbitrary data has greatly increased the number of techniques for implementing network steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Combining Different Existing Methods for Describing Steganog** | 2025 | cs.CR, cs.NI | Steffen Wendzel et al. [[1]](https://arxiv.org/abs/2506.01700) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Quantum Hilbert Transform

**Goal:** does not exist any quantum analogue for the Hilbert transform.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Quantum Hilbert Transform** | 2025 | cs.CR, cs.DM, cs.NI | Nitin Jha, Abhishek Parakh [[1]](https://arxiv.org/abs/2505.23581) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### RFNNS: Robust Fixed Neural Network Steganography with Universal Text-to-Image Models

**Goal:** With the rapid development of generative AI, image steganography has garnered widespread attention due to its unique concealment.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **RFNNS: Robust Fixed Neural Network Steganography with Univer** | 2025 | cs.MM | Yu Cheng et al. [[1]](https://arxiv.org/abs/2505.04116) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Multichannel Steganography: A Provably Secure Hybrid Steganographic Model for Secure Communication

**Goal:** purely distortion-free or invertible schemes fail under the same threat model, underscoring the necessity of hybrid designs.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Multichannel Steganography: A Provably Secure Hybrid Stegano** | 2025 | cs.CR, cs.MM | Obinna Omego, Michal Bosy [[1]](https://arxiv.org/abs/2501.04511) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Cover-separable Fixed Neural Network Steganography via Deep Generative Models

**Goal:** Image steganography is the process of hiding secret data in a cover image by subtle perturbation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Cover-separable Fixed Neural Network Steganography via Deep ** | 2024 | cs.CR, cs.CV | Guobiao Li et al. [[1]](https://arxiv.org/abs/2407.11405) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Synthetic Embedding of Hidden Information in Industrial Control System Network Protocols for Evaluation of Steganographic Malware

**Goal:** infrastructures have increased protection requirements.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Synthetic Embedding of Hidden Information in Industrial Cont** | 2024 | cs.CR | Tom Neubert et al. [[1]](https://arxiv.org/abs/2406.19338) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Purified and Unified Steganographic Network

**Goal:** Steganography is the art of hiding secret data into the cover media for covert communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Purified and Unified Steganographic Network** | 2024 | cs.CR, cs.CV | Guobiao Li et al. [[1]](https://arxiv.org/abs/2402.17210) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Towards Deep Network Steganography: From Networks to Networks

**Goal:** covertly transmit the DNN models in public channels brings us the attention, especially for those trained for secret-learning tasks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Deep Network Steganography: From Networks to Network** | 2023 | cs.CR, cs.AI | Guobiao Li et al. [[1]](https://arxiv.org/abs/2307.03444) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### DWT-GBT-SVD-based Robust Speech Steganography

**Goal:** Steganography is a method that can improve network security and make communications safer.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **DWT-GBT-SVD-based Robust Speech Steganography** | 2020 | cs.MM, cs.SD, eess.AS | Noshin Amiri, Iman Naderi [[1]](https://arxiv.org/abs/2004.12569) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Lightweight Adaptable DNS Channel for Covert Data Transmission

**Goal:** secret data such as keys.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Lightweight Adaptable DNS Channel for Covert Data Transmis** | 2020 | cs.CR | Mahboubeh Nazari, Sousan Tarahomi, Sobhan Aliabady [[1]](https://arxiv.org/abs/2003.14094) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Deep Residual Neural Networks for Image in Speech Steganography

**Goal:** Steganography is the art of hiding a secret message inside a publicly visible carrier message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Deep Residual Neural Networks for Image in Speech Steganogra** | 2020 | cs.MM, cs.SD, eess.AS | Shivam Agarwal, Siddarth Venkatraman [[1]](https://arxiv.org/abs/2003.13217) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hide and Speak: Towards Deep Neural Networks for Speech Steganography

**Goal:** Steganography is the science of hiding a secret message within an ordinary public message, which is referred to as Carrier.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hide and Speak: Towards Deep Neural Networks for Speech Steg** | 2020 | cs.SD, cs.CR, cs.LG | Felix Kreuk et al. [[1]](https://arxiv.org/abs/1902.03083) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Data in Plain Sight: Undetectable Wireless Communications Through Pseudo-Noise Asymmetric Shift Keying

**Goal:** Undetectable wireless transmissions are fundamental to avoid eavesdroppers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Data in Plain Sight: Undetectable Wireless Communicat** | 2019 | cs.CR, cs.NI, eess.SP | Salvatore D'Oro, Francesco Restuccia, Tommaso Melodia [[1]](https://arxiv.org/abs/1905.02250) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### AAG-Stega: Automatic Audio Generation-based Steganography

**Goal:** Steganography, as one of the three basic information security systems, has long played an important role in safeguarding the privacy and confidentiality of data in cyberspace.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **AAG-Stega: Automatic Audio Generation-based Steganography** | 2018 | cs.CR | Zhongliang Yang et al. [[1]](https://arxiv.org/abs/1809.03463) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Unified Description for Network Information Hiding Methods

**Goal:** Until now hiding methods in network steganography have been described in arbitrary ways, making them difficult to compare.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Unified Description for Network Information Hiding Methods** | 2017 | cs.CR | Steffen Wendzel, Wojciech Mazurczyk, Sebastian Zander [[1]](https://arxiv.org/abs/1512.07438) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Second Order Derivatives based Approach for Steganography

**Goal:** Steganography schemes are designed with the objective of minimizing a defined distortion function.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Second Order Derivatives based Approach for Steganography** | 2016 | cs.MM | Jean-François Couchot et al. [[1]](https://arxiv.org/abs/1611.08397) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Why Johnny Can't Use Stego: a Human-oriented Perspective on the Application of Steganography

**Goal:** Steganography is the discipline that deals with concealing the existence of secret communications.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Why Johnny Can't Use Stego: a Human-oriented Perspective on ** | 2016 | cs.CR | Steffen Wendzel [[1]](https://arxiv.org/abs/1609.06664) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Trends toward real-time network data steganography

**Goal:** Network steganography has been a well-known covert data channeling method for over three decades.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Trends toward real-time network data steganography** | 2016 | cs.MM, cs.CR | James Collins, Sos Agaian [[1]](https://arxiv.org/abs/1604.02778) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### "The Good, The Bad And The Ugly": Evaluation of Wi-Fi Steganography

**Goal:** In this paper we propose a new method for the evaluation of network steganography algorithms based on the new concept of "the moving observer".

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **"The Good, The Bad And The Ugly": Evaluation of Wi-Fi Stegan** | 2015 | cs.MM, cs.CR | Krzysztof Szczypiorski, Artur Janicki, Steffen Wendzel [[1]](https://arxiv.org/abs/1508.04978) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegBlocks: ensuring perfect undetectability of network steganography

**Goal:** paper presents StegBlocks, which defines a new concept for performing undetectable hidden communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegBlocks: ensuring perfect undetectability of network steg** | 2015 | cs.MM, cs.CR | Wojciech Fraczek, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1506.02311) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Micro protocol engineering for unstructured carriers: On the embedding of steganographic control protocols into audio transmissions

**Goal:** Network steganography conceals the transfer of sensitive information within unobtrusive data in computer networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Micro protocol engineering for unstructured carriers: On the** | 2015 | cs.MM, cs.CY | Matthias Naumann et al. [[1]](https://arxiv.org/abs/1505.07757) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hidden and Uncontrolled - On the Emergence of Network Steganographic Threats

**Goal:** Network steganography is the art of hiding secret information within innocent network transmissions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hidden and Uncontrolled - On the Emergence of Network Stegan** | 2014 | cs.CR | Steffen Wendzel et al. [[1]](https://arxiv.org/abs/1407.2029) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On Importance of Steganographic Cost For Network Steganography

**Goal:** Network steganography encompasses the information hiding techniques that can be applied in communication network environments and that utilize hidden data carriers for this purpose.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On Importance of Steganographic Cost For Network Steganograp** | 2014 | cs.MM, cs.CR | Wojciech Mazurczyk et al. [[1]](https://arxiv.org/abs/1406.2519) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Adaptive Software Radio Steganography

**Goal:** This paper presents an adaptable steganography (information hiding) method for digital radio communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Adaptive Software Radio Steganography** | 2013 | cs.MM | David E. Robillard [[1]](https://arxiv.org/abs/1304.7324) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Development Trends in Steganography

**Goal:** Steganography is a general term referring to all methods for the embedding of additional secret content into some form of carrier, with the aim of concealment of the introduced alterations.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Development Trends in Steganography** | 2013 | cs.MM | Elzbieta Zielinska, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1202.5289) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Principles and Overview of Network Steganography

**Goal:** The paper presents basic principles of network steganography, which is a comparatively new research subject in the area of information hiding, followed by a concise overview and classification of n...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Principles and Overview of Network Steganography** | 2012 | cs.CR | Jozef Lubacz, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1207.0917) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint stage; community evaluation ongoing.

---

### Dynamic Pattern Based Image Steganography

**Goal:** Steganography is the art of hiding secret information in media such as image, audio and video.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Dynamic Pattern Based Image Steganography** | 2012 | cs.CR | P. Thiyagarajan, G. Aghila, V. Prasanna Venkatesan [[1]](https://arxiv.org/abs/1206.2583) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Direct Sequence Spread Spectrum Steganographic Scheme for IEEE 802.15.4

**Goal:** This work addresses the issues related to network steganography in IEEE 802.15.4 Wireless Personal Area Networks (WPAN).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Direct Sequence Spread Spectrum Steganographic Scheme for IE** | 2011 | cs.CR | Elzbieta Zielinska, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4230) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### How Hidden Can Be Even More Hidden?

**Goal:** The paper presents Deep Hiding Techniques (DHTs) that define general techniques that can be applied to every network steganography method to improve its undetectability and make steganogram extract...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **How Hidden Can Be Even More Hidden?** | 2011 | cs.CR | Wojciech Fraczek, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4065) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Sending Hidden Data via Google Suggest

**Goal:** Google Web Search which was created to help user find the right search phrase by proposing the autocompleting popular phrases while typing.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Sending Hidden Data via Google Suggest** | 2011 | cs.CR | Piotr Bialczak, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4062) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Stegobot: construction of an unobservable communication network leveraging social behavior

**Goal:** using social networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegobot: construction of an unobservable communication netw** | 2011 | cs.CR, cs.NI, cs.SI | Shishir Nagaraja et al. [[1]](https://arxiv.org/abs/1107.2031) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Proposed System for data hiding using Cryptography and Steganography Proposed System for data hiding using Cryptography and Steganography

**Goal:** Steganography and Cryptography are two popular ways of sending vital information in a secret way.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Proposed System for data hiding using Cryptography and Stega** | 2010 | cs.CR | Dipti Kapoor Sarmah, Neha Bajpai [[1]](https://arxiv.org/abs/1009.2826) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Retransmission Steganography Applied

**Goal:** This paper presents experimental results of the implementation of network steganography method called RSTEG (Retransmission Steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Retransmission Steganography Applied** | 2010 | cs.CR | Wojciech Mazurczyk, Milosz Smolarczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1007.0767) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Stream Control Transmission Protocol Steganography

**Goal:** Stream Control Transmission Protocol (SCTP) is a new transport layer protocol that is due to replace TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) protocols in future IP netw...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stream Control Transmission Protocol Steganography** | 2010 | cs.CR | Wojciech Fraczek, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1006.0247) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Information Hiding Using Improper Frame Padding

**Goal:** Hiding information in network traffic may lead to leakage of confidential information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information Hiding Using Improper Frame Padding** | 2010 | cs.CR | Bartosz Jankowski, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1005.1925) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Perfect Z2Z4-linear codes in Steganography

**Goal:** Steganography is an information hiding application which aims to hide secret data imperceptibly into a commonly used media.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Perfect Z2Z4-linear codes in Steganography** | 2010 | cs.IT, cs.CR | H. Rifà-Pous, J. Rifà, L. Ronquillo [[1]](https://arxiv.org/abs/1002.0026) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography in Handling Oversized IP Packets

**Goal:** This paper identifies new class of network steganography methods that utilize mechanisms to handle oversized packets in IP networks: IP fragmentation, PMTUD (Path MTU Discovery) and PLPMTUD (Packet...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography in Handling Oversized IP Packets** | 2009 | cs.CR | Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/0907.0313) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### SecMon: End-to-End Quality and Security Monitoring System

**Goal:** a self-organizing capability.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SecMon: End-to-End Quality and Security Monitoring System** | 2008 | cs.MM | Tomasz Ciszkowski et al. [[1]](https://arxiv.org/abs/0804.0134) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

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

