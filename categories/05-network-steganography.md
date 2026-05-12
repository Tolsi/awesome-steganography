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
<!-- /TOC -->

## Header Fields

---

### IPv4/IPv6 Headers

**Goal:** Use protocol header fields for data embedding.

| Algorithm | Year | Field | Bits/Packet |
|----------|------|-------|-------------|
| **IPv4/IPv6 Headers** | 2000 | ID, TTL, DSCP, Flow Label | 1-20 bit/pkt |

**State of the art:** Simple but limited capacity.

**Production readiness:** Experimental

**Security status:** Caution — Easily monitored

**Community acceptance:** Niche

---

### TCP Headers

**Goal:** Use TCP header fields for covert communication.

| Algorithm | Year | Field | Bits/Packet |
|----------|------|-------|-------------|
| **TCP Headers** | 2000 | ISN, Timestamp, Window | 4-32 bit/conn |

**State of the art:** Common approach for TCP-based channels.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### HTTP Headers

**Goal:** Use HTTP header order/content for embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HTTP Headers** | 2005 | Header order, case | log2(N!)/req |

**State of the art:** Works in HTTP traffic.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

## Timing Channels

---

### IPD Encoding

**Goal:** Encode data in inter-packet delays.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **IPD Encoding** | 2000 | Delay < T = 0, > T = 1 | 1-10 bps |

**State of the art:** Classic timing channel.

**Production readiness:** Experimental

**Security status:** Caution — Noisy channel

**Community acceptance:** Niche

---

### LAN Covert Channels (Girling)

**Goal:** First study of covert channels in LAN.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Girling** | 1987 | Storage + timing channels | Academic |

**State of the art:** Foundational research.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Niche — Historical importance

---

### Wolf Covert Channels

**Goal:** Implement covert channels in TCP/IP.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Wolf** | 1989 | Reserved fields | LAN protocols |

**State of the art:** Early implementation.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Niche

---

### Jitterbug

**Goal:** Modulate keystroke timing for covert channels.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Jitterbug** | 2006 | Keystroke timing | Low bandwidth |

**State of the art:** Academic curiosity.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Niche

---

### Keypress Timing Channel

**Goal:** Encode data in keyboard timing delays.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Keypress Timing** | 2000 | Network delay encoding | 1-10 bps |

**State of the art:** Uses telnet/remote desktop timing.

**Production readiness:** Experimental

**Security status:** Caution

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

**Goal:** Hide data in QUIC protocol.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **QuicCourier** | 2024 | 20 covert channels in QUIC | Connection ID, packet gaps, etc. |

**State of the art:** Latest in network steganography.

**Production readiness:** Research

**Security status:** Secure — New protocol, less detection

**Community acceptance:** Emerging — Active research

---

### LACK

**Goal:** Hide data in intentionally lost VoIP packets.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LACK** | 2008 | Lost Audio Packets Steganography | VoIP |

**State of the art:** VoIP-specific steganography.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### SteganoRTP

**Goal:** Embed in RTP protocol fields.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SteganoRTP** | 2010 | Padding bit or CSRC list | RTP |

**State of the art:** RTP-specific embedding.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Niche

---

### VoIP Steganography

**Goal:** General steganography in Voice over IP streams.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **VoIP Steganography** | 2008 | Codec-based, timing | Multiple methods |

**State of the art:** Active research area.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

### WireGuard Steganography

**Goal:** Hide data in WireGuard VPN protocol.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **WireGuard Stego** | 2020 | WireGuard handshake | Modern VPN |

**State of the art:** Newer approach using WireGuard.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

## Alternative Protocols

---

### 5G/6G Cellular

**Goal:** Covert channels in cellular networks.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SteaLTE** | 2021 | LTE steganography | Private 5G |

**State of the art:** Emerging cellular steganography.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### Wi-Fi CSI

**Goal:** Embed in Wi-Fi Channel State Information.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Wi-Fi CSI** | 2026 | CSI using FIR filters | High capacity |

**State of the art:** Very recent research.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### CYPRESS

**Goal:** High-speed covert channels mounting on regular packets.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **CYPRESS** | 2025 | Secret packets on regular packets | 1.6 MB/s |

**State of the art:** Highest throughput network stego.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Emerging

---

### HICCUPS

**Goal:** Hide data in WLAN networks using corrupted frames.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HICCUPS** | 2003 | Hidden Communication System for Corrupted Networks | WLAN steganography |

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
| **Inter-protocol** | 2010 | Cross-protocol embedding | Complex detection |

**State of the art:** Harder to detect than single-protocol methods.

**Production readiness:** Research

**Security status:** Secure — Cross-protocol correlation required

**Community acceptance:** Emerging

---

### Quantum Gatekeeper

**Goal:** Post-quantum secure network steganography against quantum-enabled detectors.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Quantum Gatekeeper** | 2025 | Lattice-based encoding + timing modulation | Quantum-resistant |

**State of the art:** First quantum-resistant network steganography method.

**Production readiness:** Research

**Security status:** Secure — Lattice-based security assumptions

**Community acceptance:** Emerging

---

### Intellicise Wireless Network

**Goal:** Coverless semantic steganography for 6G intelligent wireless networks using Agentic AI.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Intellicise Wireless Network** | 2026 | Agentic AI + diffusion models + semantic codec | Coverless, no key required |

**State of the art:** AgentSemSteCom scheme uses semantic extraction, digital token controlled reference image generation, and coverless steganography without requiring cover images or private semantic keys.

**Production readiness:** Research

**Implementations:** None found

**Security status:** Secure — No cover images or keys to infer

**Community acceptance:** Emerging
