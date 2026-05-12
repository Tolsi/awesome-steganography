# Traffic Obfuscation

<!-- TOC -->
## Contents (3 subcategories)

**[Tor Pluggable Transports](#tor-pluggable-transports)**
- [obfs4](#obfs4)
- [meek](#meek)
- [Snowflake](#snowflake)
- [WebTunnel](#webtunnel)

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
| **meek** | 2015 | HTTPS to CDN | Azure/Cloudflare |

**State of the art:** Hard to block without blocking CDN.

**Production readiness:** Production (deprecated)

**Security status:** Secure — Domain fronting

**Community acceptance:** Standard — Top for Iran/China

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

**Goal:** Lightweight V2Ray protocol without internal encryption.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **VLESS** | 2022 | External TLS | Lightweight |

**State of the art:** Simplified V2Ray protocol.

**Production readiness:** Production

**Security status:** Secure — TLS wrapped

**Community acceptance:** Widely trusted

---

### XTLS-Vision

**Goal:** Enhanced REALITY with padding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **XTLS-Vision** | 2024 | Random padding | Improved statistics |

**State of the art:** Latest in Xray family.

**Production readiness:** Production

**Security status:** Secure

**Community acceptance:** Emerging

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
