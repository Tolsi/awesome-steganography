# Network Steganography

<!-- TOC -->
## Contents (5 subcategories)

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
