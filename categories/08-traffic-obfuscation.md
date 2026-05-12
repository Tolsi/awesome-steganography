# Traffic Obfuscation

<!-- TOC -->
## Contents (14 algorithms)

**[Tor Pluggable Transports](#tor-pluggable-transports)**
- [obfs4](#obfs4)
- [meek](#meek)
- [Snowflake](#snowflake)
- [WebTunnel](#webtunnel)
- [Grain](#grain)
- [Thomae](#thomae)

**[V2Ray/Xray Family](#v2rayxray-family)**
- [REALITY](#reality)
- [VLESS](#vless)
- [XTLS-Vision](#xtls-vision)

**[Other Protocols](#other-protocols)**
- [Trojan-GFW](#trojan-gfw)
- [Hysteria 2](#hysteria-2)
- [Shadowsocks](#shadowsocks)
- [NaiveProxy](#naiveproxy)
- [ICMP Tunnel](#icmp-tunnel)
<!-- /TOC -->

## Tor Pluggable Transports

---

### obfs4

**Goal:** Obfuscated Tor bridge looking like random noise.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **obfs4** | 2014 | Random-looking bytestream | ScrambleSuit fork |

**State of the art:** Classic obfuscation transport.

**Production readiness:** Production

**Implementations:**
- [obfs4](https://gitlab.com/yawning/obfs4) ⭐ 892

**Security status:** Caution — Detectable by active probing

**Community acceptance:** Standard — Essential for circumvention

---

### meek

**Goal:** Domain-fronted Tor bridge through CDNs.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **meek** | 2015 | HTTPS to CDN (domain fronting) | Fifield et al. PETS 2015 [[1]](https://petsymposium.org/popets/2015/popets-2015-0009.php) |

**State of the art:** Hard to block without blocking CDN. Largely superseded by [WebTunnel](#webtunnel) due to CDN policy changes.

**Production readiness:** Production (deprecated)
Operational but most CDN providers now ban domain fronting.

**Implementations:**
- [meek](https://gitlab.com/yawning/obfs4) — Part of Tor PT suite; shipped with Tor Browser

**Security status:** Secure — Domain fronting hides true destination

**Community acceptance:** Standard — Top for Iran/China; foundational circumvention technique

---

### Snowflake

**Goal:** WebRTC-based Pluggable Transport.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Snowflake** | 2017 | WebRTC P2P video | Volunteer proxies |

**State of the art:** Uses volunteer proxies for resistance.

**Production readiness:** Production

**Implementations:**
- [snowflake](https://gitweb.torproject.org/pluggable-transports/snowflake.git) ⭐ 234

**Security status:** Secure — Large proxy pool

**Community acceptance:** Standard — Essential for circumvention

---

### WebTunnel

**Goal:** HTTPS + WebSocket obfuscation.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **WebTunnel** | 2023 | HTTPS + WebSocket | Modern replacement |

**State of the art:** Modern meek replacement.

**Production readiness:** Production

**Implementations:**
- [WebTunnel](https://github.com/Arkanic/WebTunnel) ⭐ 156

**Security status:** Secure

**Community acceptance:** Emerging

---

### Grain

**Goal:** Stream cipher-based traffic obfuscation using the Grain-128 lightweight cipher.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Grain** | 2014 | Grain-128 stream cipher for bytestream obfuscation | eSTREAM finalist [[1]](https://www.semanticscholar.org/paper/A-Stream-Cipher-Proposal%3A-Grain-128-Hell-Johansson/72d20a8b5ba95095b58a407b86d47632da123396) |

**State of the art:** Lightweight stream cipher approach; less widely deployed than obfs4.

**Production readiness:** Production
Used in some PT implementations; not as mainstream as obfs4.

**Security status:** Caution — Cipher-level security sound, but traffic patterns may be detectable

**Community acceptance:** Niche — Limited to specific circumvention tools

---

### Thomae

**Goal:** Protocol obfuscation by mimicking TLS fingerprints of legitimate clients.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Thomae** | 2019 | TLS ClientHello fingerprint mimicry (uTLS) | Frolov & Wustrow NDSS 2019 [[1]](https://www.ndss-symposium.org/ndss-paper/the-use-of-tls-in-censorship-circumvention/) |

**State of the art:** Mimics legitimate TLS patterns using the uTLS library; widely adopted in modern censorship circumvention tools.

**Production readiness:** Production
uTLS library integrated into many active PT implementations.

**Implementations:**
- [uTLS](https://github.com/refraction-networking/utls) ⭐ 1.5k — Go, TLS fingerprint mimicry library

**Security status:** Secure — Indistinguishable from target browser TLS fingerprint

**Community acceptance:** Emerging — Growing adoption in circumvention ecosystem

---

## V2Ray/Xray Family

---

### REALITY

**Goal:** TLS handshake spoofing to real website.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **REALITY** | 2023 | SNI fingerprint spoofing | MitM-resistant |

**State of the art:** Best current circumvention. Spoofs TLS to google.com.

**Production readiness:** Production

**Implementations:**
- [Xray-core](https://github.com/XTLS/Xray-core) ⭐ 8.2k
- [sing-box](https://github.com/SagerNet/sing-box) ⭐ 4.1k

**Security status:** Secure — MitM-resistant during handshake

**Community acceptance:** Standard — Dominant in China/Iran

---

### VLESS

**Goal:** Lightweight V2Ray protocol without internal encryption, relying on external TLS.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **VLESS** | 2020 | Stateless lightweight proxy protocol; external TLS | RPRX/Project X [[1]](https://github.com/RPRX/v2ray-vless) |

**State of the art:** Simplified VMess replacement; lower CPU overhead. Typically paired with XTLS-Vision or REALITY.

**Production readiness:** Production
Widely deployed; integrated into Xray-core and sing-box.

**Implementations:**
- [Xray-core](https://github.com/XTLS/Xray-core) ⭐ 8.2k — Go, primary VLESS implementation
- [sing-box](https://github.com/SagerNet/sing-box) ⭐ 4.1k — Go, universal proxy platform

**Security status:** Secure — Relies on TLS for confidentiality; no built-in encryption layer

**Community acceptance:** Widely trusted — De facto standard in Project X ecosystem

---

### XTLS-Vision

**Goal:** Enhanced REALITY transport with random padding to defeat traffic-length statistical analysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **XTLS-Vision** | 2022 | Probabilistic random padding inserted into TLS stream | Project X / Xray-core [[1]](https://xtls.github.io/en/config/outbounds/vless.html) |

**State of the art:** Latest flow-control mode in Xray family; addresses length-based DPI fingerprinting of REALITY.

**Production readiness:** Production
Shipped in Xray-core; widely used in China/Iran censorship circumvention.

**Implementations:**
- [Xray-core](https://github.com/XTLS/Xray-core) ⭐ 8.2k — Go, official implementation

**Security status:** Secure — Padding randomizes packet-length statistics

**Community acceptance:** Emerging — Growing rapidly as REALITY successor

---

## Other Protocols

---

### Trojan-GFW

**Goal:** TLS-wrapped protocol with decoy website.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Trojan-GFW** | 2018 | TLS + HTTP/2 | Decoy on wrong password |

**State of the art:** Proven protocol.

**Production readiness:** Production

**Implementations:**
- [trojan-go](https://github.com/p4gefau1t/trojan-go) ⭐ 3.2k

**Security status:** Secure

**Community acceptance:** Widely trusted

---

### Hysteria 2

**Goal:** QUIC-based protocol with obfuscation.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Hysteria 2** | 2023 | QUIC + HTTP/3 | UDP, low latency |

**State of the art:** Modern UDP-based protocol.

**Production readiness:** Production

**Implementations:**
- [hysteria](https://github.com/apernet/hysteria) ⭐ 4.8k

**Security status:** Secure

**Community acceptance:** Widely trusted

---

### Shadowsocks

**Goal:** SOCKS5-based AEAD protocol.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Shadowsocks** | 2014 | SOCKS5 + AEAD | Classic |

**State of the art:** Classic but now detectable by modern DPI.

**Production readiness:** Deprecated

**Implementations:**
- [shadowsocks](https://github.com/shadowsocks/shadowsocks) ⭐ 3.5k

**Security status:** Broken — Detectable by modern DPI

**Community acceptance:** Widely trusted — Historical importance

---

### NaiveProxy

**Goal:** Chrome-like HTTP/2 fingerprint.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **NaiveProxy** | 2019 | HTTP/2 CONNECT | Chromium fingerprint |

**State of the art:** Uses Chromium stack for identical fingerprint.

**Production readiness:** Production

**Implementations:**
- [naiveproxy](https://github.com/klzgrad/naiveproxy) ⭐ 2.9k

**Security status:** Secure

**Community acceptance:** Widely trusted

---

### ICMP Tunnel

**Goal:** Tunnel IP traffic over ICMP.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **ICMP Tunnel** | 2000 | Echo request/response | Easy to detect |

**State of the art:** Simple but highly detectable.

**Production readiness:** Deprecated

**Implementations:**
- [icmptunnel](https://github.com/rozet/icmptunnel) ⭐ 423

**Security status:** Broken — Easy to detect

**Community acceptance:** Niche
