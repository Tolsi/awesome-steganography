# Tools & Implementations

<!-- TOC -->
## Contents

**[Text Steganography](#text-steganography)**
- [ascii-steganography](#ascii-steganography)
- [snow](#snow)
- [zwsp-steg-js](#zwsp-steg-js)
- [stegtext](#stegtext)
- [SpamMimic](#spammimic)
- [meteor-stego](#meteor-stego)
- [stegcloak](#stegcloak)
- [Cloakify](#cloakify)

**[Image Steganography](#image-steganography)**
- [steghide](#steghide)
- [openstego](#openstego)
- [stegolab](#stegolab)
- [pvd_steganography](#pvd_steganography)
- [EMD](#emd)
- [Chaos_LSB](#chaos_lsb)
- [stc-lib](#stc-lib)
- [conseal](#conseal)
- [WOW-steganography](#wow-steganography)
- [nsf5sim](#nsf5sim)
- [UERD](#uerd)
- [aletheia](#aletheia)
- [outguess](#outguess)
- [HiDDeN](#hidden)
- [SteganoGAN](#steganogan)
- [StegaStamp](#stegastamp)
- [CRoSS](#cross)
- [stegify](#stegify)
- [tweetable-polyglot-png](#tweetable-polyglot-png)
- [stego-toolkit](#stego-toolkit)

**[Audio Steganography](#audio-steganography)**
- [DeepSound](#deepsound)
- [mp3stego](#mp3stego)
- [wavmark](#wavmark)
- [audioseal](#audioseal)
- [WavSteg](#wavsteg)
- [spectrology](#spectrology)
- [audio-steganography-algorithms](#audio-steganography-algorithms)

**[Video Steganography](#video-steganography)**
- [LVDO](#lvdo)
- [videostego](#videostego)
- [SteganographierGUI](#steganographiergui)

**[Network Steganography](#network-steganography)**
- [iodine](#iodine)
- [dnscat2](#dnscat2)
- [dns2tcp](#dns2tcp)

**[Filesystem & OS](#filesystem--os)**
- [bmap](#bmap)
- [VeraCrypt](#veracrypt)
- [ExifTool](#exiftool)
- [hydan](#hydan)

**[Traffic Obfuscation](#traffic-obfuscation)**
- [obfs4](#obfs4)
- [Snowflake](#snowflake)
- [WebTunnel](#webtunnel)
- [uTLS](#utls)
- [Xray-core](#xray-core)
- [sing-box](#sing-box)
- [trojan-go](#trojan-go)
- [hysteria](#hysteria)
- [Shadowsocks](#shadowsocks)
- [NaiveProxy](#naiveproxy)
- [icmptunnel](#icmptunnel)

**[Physical & Social](#physical--social)**
- [Printer Steganography Detector](#printer-steganography-detector)

**[Steganalysis](#steganalysis)**
- [stegdetect](#stegdetect)
- [ALASKA2 steganalysis tools](#alaska2-steganalysis-tools)
- [XuNet](#xunet)
- [TensorFlow-YeNet](#tensorflow-yenet)
- [Pytorch-YeNet](#pytorch-yenet)
- [Deep-Steganalysis](#deep-steganalysis)
- [Zhu-Net](#zhu-net)
<!-- /TOC -->

---

## Text Steganography

---

### ascii-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [ascii-steganography](https://github.com/vgmoose/ascii-steganography) | Python | Hides data in plain ASCII art |

**Note:** Encodes hidden messages within ASCII art compositions.

**Star count:** ⭐ 18

---

### snow

| Tool | Language | Description |
|------|----------|-------------|
| [snow](https://github.com/mattkwan-zz/snow) | C | Original SNOW by Matthew Kwan - whitespace steganography |

**Note:** Uses invisible whitespace characters in text to hide data.

**Star count:** ⭐ 50

---

### zwsp-steg-js

| Tool | Language | Description |
|------|----------|-------------|
| [zwsp-steg-js](https://github.com/offdev/zwsp-steg-js) | JavaScript | Encode/decode hidden messages using zero-width spaces |

**Note:** Modern implementation of zero-width character steganography.

**Star count:** ⭐ 153

---

### stegtext

| Tool | Language | Description |
|------|----------|-------------|
| [stegtext](https://github.com/btimby/stegtext) | Python | Homoglyph substitution steganography |

**Note:** Uses Unicode homoglyphs to hide messages in text.

**Star count:** ⭐ 3

---

### SpamMimic

| Tool | Language | Description |
|------|----------|-------------|
| [SpamMimic](https://www.spammimic.com/) | Online | Encodes messages as spam-like text |

**Note:** Implements Wayner's context-free grammar approach to generate spam text from hidden messages.

**Star count:** —

---

### meteor-stego

| Tool | Language | Description |
|------|----------|-------------|
| [meteor-stego](https://github.com/tmthrgd/meteor-stego) | Python | Implementation of Meteor steganography |

**Note:** LLM-based text steganography using Meteor approach.

**Star count:** ⭐ 215

---

### stegcloak

| Tool | Language | Description |
|------|----------|-------------|
| [stegcloak](https://github.com/KuroLabs/stegcloak) | JavaScript | Hide secrets with invisible characters in plain text securely |

**Note:** Hide secrets with invisible characters in plain text using zero-width characters with password protection.

**Star count:** ⭐ 3.8k

---

### Cloakify

| Tool | Language | Description |
|------|----------|-------------|
| [Cloakify](https://github.com/TryCatchHCF/Cloakify) | Python | Data exfiltration using text-based steganography |

**Note:** Converts any filetype into list of everyday strings. Evades DLP/MLS devices and data whitelisting.

**Star count:** ⭐ 1.7k

---

## Image Steganography

---

### steghide

| Tool | Language | Description |
|------|----------|-------------|
| [steghide](https://github.com/StephanHofmannmich/steghide) | C++ | Classic LSB tool for image and audio |

**Note:** One of the most well-known open-source steganography tools.

**Star count:** ⭐ 1.8k

---

### openstego

| Tool | Language | Description |
|------|----------|-------------|
| [openstego](https://github.com/syvaidya/openstego) | Java | Supports LSB, BPCS, F5 algorithms |

**Note:** Full-featured GUI steganography tool with multiple algorithms.

**Star count:** ⭐ 287

---

### stegolab

| Tool | Language | Description |
|------|----------|-------------|
| [stegolab](https://github.com/daniellerch/stegolab) | Python | Includes LSB matching, HILL, J-UNIWARD, and steganalysis |

**Note:** Comprehensive steganography research framework by Daniel Lerch.

**Star count:** ⭐ 51

---

### pvd_steganography

| Tool | Language | Description |
|------|----------|-------------|
| [pvd_steganography](https://github.com/tony-josi/pvd_steganography) | Python | PVD method for PNG cover images |

**Note:** Implementation of Pixel Value Differencing steganography.

**Star count:** ⭐ 22

---

### EMD

| Tool | Language | Description |
|------|----------|-------------|
| [EMD](https://github.com/cagatayavsar/EMD) | Python/C++ | Implementation of Zhang & Wang (2006) EMD method |

**Note:** Exploiting Modification Direction algorithm.

**Star count:** ⭐ 0

---

### Chaos_LSB

| Tool | Language | Description |
|------|----------|-------------|
| [Chaos_LSB](https://github.com/FifthEpoch/Chaos_LSB) | Python | AES encryption + chaotic pixel selection |

**Note:** Enhanced LSB with cryptographic and chaotic dynamics.

**Star count:** ⭐ 0

---

### stc-lib

| Tool | Language | Description |
|------|----------|-------------|
| [stc-lib](https://github.com/coin3d/stc-lib) | C++ | Syndrome-Trellis Codes implementation |

**Note:** Optimal coding for steganography with minimal distortion.

**Star count:** ⭐ 89

---

### conseal

| Tool | Language | Description |
|------|----------|-------------|
| [conseal](https://github.com/uibk-uncover/conseal) | Python | HUGO, HILL, MiPOD, nsF5, J-UNIWARD, UERD simulators |

**Note:** Comprehensive modern steganography simulator library.

**Star count:** ⭐ 17

---

### WOW-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [WOW-steganography](https://github.com/3xpl01tc0d3r/WOW-steganography) | Python | Wavelet Obtained Weights algorithm |

**Note:** Implementation of the WOW steganographic algorithm.

**Star count:** ⭐ 156

---

### nsf5sim

| Tool | Language | Description |
|------|----------|-------------|
| [nsf5sim](https://github.com/goxman/nsf5sim) | C/Matlab | Includes S-UNIWARD for JPEG steganography |

**Note:** Non-shifted F5 steganography simulator.

**Star count:** ⭐ 78

---

### UERD

| Tool | Language | Description |
|------|----------|-------------|
| [UERD](https://github.com/vazswk/UERD) | Matlab | Uniform Embedding Revisited Distortion |

**Note:** Implementation of UERD steganography method.

**Star count:** ⭐ 0

---

### aletheia

| Tool | Language | Description |
|------|----------|-------------|
| [aletheia](https://github.com/daniellerch/aletheia) | Python | Steganalysis tool with JSteg detection |

**Note:** Also includes steganography capabilities and comprehensive steganalysis.

**Star count:** ⭐ 204

---

### outguess

| Tool | Language | Description |
|------|----------|-------------|
| [outguess](https://github.com/crorvick/outguess) | C | Original tool by Niels Provos |

**Note:** Classic JPEG steganography tool with statistical attacks.

**Star count:** ⭐ 0

---

### HiDDeN

| Tool | Language | Description |
|------|----------|-------------|
| [HiDDeN](https://github.com/tancik/HiDDeN) | PyTorch | End-to-end deep learning steganography |

**Note:** Pioneering neural steganography paper and implementation.

**Star count:** ⭐ 892

---

### SteganoGAN

| Tool | Language | Description |
|------|----------|-------------|
| [SteganoGAN](https://github.com/DAI-Lab/SteganoGAN) | Python | GAN-based steganography with high capacity 2-4 bpp |

**Note:** Generates stego images with embedded secret data using GANs.

**Star count:** ⭐ 428

---

### StegaStamp

| Tool | Language | Description |
|------|----------|-------------|
| [StegaStamp](https://github.com/tancik/StegaStamp) | PyTorch | Robust encoder surviving print+photo transmission |

**Note:** Invisible watermark that survives geometric distortions and photo capture.

**Star count:** ⭐ 1.2k

---

### CRoSS

| Tool | Language | Description |
|------|----------|-------------|
| [CRoSS](https://github.com/yujiwen/CRoSS) | PyTorch | Coverless steganography via diffusion models (NeurIPS 2023) |

**Note:** Generates images that inherently contain hidden information.

**Star count:** ⭐ 157

---

### stegify

| Tool | Language | Description |
|------|----------|-------------|
| [stegify](https://github.com/DimitarPetrov/stegify) | Go | LSB steganography tool for hiding files in images |

**Note:** Go tool for LSB steganography, capable of hiding any file within an image.

**Star count:** ⭐ 1.3k

---

### tweetable-polyglot-png

| Tool | Language | Description |
|------|----------|-------------|
| [tweetable-polyglot-png](https://github.com/DavidBuchanan314/tweetable-polyglot-png) | Python | Pack up to 3MB of data into a tweetable PNG polyglot |

**Note:** Embeds ZIP, MP3, or other files into PNG images that remain valid and viewable.

**Star count:** ⭐ 2.6k

---

### stego-toolkit

| Tool | Language | Description |
|------|----------|-------------|
| [stego-toolkit](https://github.com/DominicBreuker/stego-toolkit) | Shell | Collection of steganography tools for CTF challenges |

**Note:** Docker-based collection of steganography tools. Helps with CTF challenges.

**Star count:** ⭐ 2.7k

---

## Audio Steganography

---

### DeepSound

| Tool | Language | Description |
|------|----------|-------------|
| [DeepSound](https://github.com/ElsebyCoder/DeepSound) | Python | Autoencoder-based audio steganography |

**Note:** Neural network approach to hiding data in audio.

**Star count:** ⭐ 312

---

### mp3stego

| Tool | Language | Description |
|------|----------|-------------|
| [mp3stego](http://www.petitcolas.net/steganography/mp3stego/) | C | Embeds data during MP3 encoding |

**Note:** Classic MP3 steganography by Fabien Petitcolas.

**Star count:** —

---

### wavmark

| Tool | Language | Description |
|------|----------|-------------|
| [wavmark](https://github.com/wavmark/wavmark) | Python/PyTorch | Invertible network for robust audio watermarking |

**Note:** State-of-the-art audio watermarking with high robustness.

**Star count:** ⭐ 310

---

### audioseal

| Tool | Language | Description |
|------|----------|-------------|
| [audioseal](https://github.com/facebookresearch/audioseal) | Python/PyTorch | Generator/detector with localization loss |

**Note:** Meta's audio watermarking library with precise location detection.

**Star count:** ⭐ 717

---

### WavSteg

| Tool | Language | Description |
|------|----------|-------------|
| [WavSteg](https://github.com/ragibson/Steganography) | Python3 | LSB substitution in WAV samples |

**Note:** Simple but effective LSB audio steganography.

**Star count:** ⭐ 648

---

### spectrology

| Tool | Language | Description |
|------|----------|-------------|
| [spectrology](https://github.com/solusipse/spectrology) | Python | Encode image into audio spectrogram |

**Note:** Visual audio steganography - images encoded as audio spectrograms.

**Star count:** ⭐ 277

---

### audio-steganography-algorithms

| Tool | Language | Description |
|------|----------|-------------|
| [audio-steganography-algorithms](https://github.com/ktekeli/audio-steganography-algorithms) | MATLAB/C | Reference library for classical audio stego algorithms |

**Note:** Comprehensive collection of audio steganography implementations.

**Star count:** ⭐ 287

---

## Video Steganography

---

### LVDO

| Tool | Language | Description |
|------|----------|-------------|
| [LVDO](https://github.com/m13253/lvdo) | Python/FFmpeg | DCT-based file-to-video encoding |

**Note:** Hides any file format inside video using DCT coefficients.

**Star count:** ⭐ 100

---

### videostego

| Tool | Language | Description |
|------|----------|-------------|
| [videostego](https://github.com/JavDomGom/videostego) | Python | LSB substitution in MP4 frames |

**Note:** Simple video steganography using least significant bits.

**Star count:** ⭐ 19

---

### SteganographierGUI

| Tool | Language | Description |
|------|----------|-------------|
| [SteganographierGUI](https://github.com/cenglin123/SteganographierGUI) | Python | Embed files into MP4/MKV video files |

**Note:** Hides files in MP4/MKV video files using video steganography.

**Star count:** ⭐ 823

---

## Network Steganography

---

### iodine

| Tool | Language | Description |
|------|----------|-------------|
| [iodine](https://github.com/yarrick/iodine) | C | IP-over-DNS tunnel |

**Note:** Tunnel IP traffic through DNS queries, ~100 KB/s bandwidth.

**Star count:** ⭐ 3.8k

---

### dnscat2

| Tool | Language | Description |
|------|----------|-------------|
| [dnscat2](https://github.com/zbetcheckin/dnscat2) | Ruby/Java | C2 channel over DNS |

**Note:** Command & control over DNS with 1-10 KB/s throughput.

**Star count:** ⭐ 2.1k

---

### dns2tcp

| Tool | Language | Description |
|------|----------|-------------|
| [dns2tcp](https://github.com/alexbakker/dns2tcp) | C | TCP tunneling over DNS |

**Note:** TCP tunneling through DNS with 10-50 KB/s.

**Star count:** ⭐ 289

---

## Filesystem & OS

---

### bmap

| Tool | Language | Description |
|------|----------|-------------|
| [bmap](https://github.com/CameronLonsdale/bmap) | Python | File slack reader/writer |

**Note:** Exploits filesystem slack space for hidden data storage.

**Star count:** ⭐ 45

---

### VeraCrypt

| Tool | Language | Description |
|------|----------|-------------|
| [VeraCrypt](https://github.com/veracrypt/VeraCrypt) | C/C++ | Hidden volume support for plausible deniability |

**Note:** Fork of TrueCrypt with hidden volumes and plausible deniability.

**Star count:** ⭐ 4.5k

---

### ExifTool

| Tool | Language | Description |
|------|----------|-------------|
| [ExifTool](https://exiftool.org/) | Perl/C++ | Universal metadata read/write tool |

**Note:** Read, write, and edit metadata in various file formats.

**Star count:** —

---

### hydan

| Tool | Language | Description |
|------|----------|-------------|
| [hydan](http://www.crazyboy.com/hydan/) | C | Instruction-level steganography in binaries |

**Note:** Hides data in executable instructions via NOPs and semantic equivalents.

**Star count:** —

---

## Traffic Obfuscation

---

### obfs4

| Tool | Language | Description |
|------|----------|-------------|
| [obfs4](https://gitlab.com/yawning/obfs4) | Go | Obfuscated Tor bridge looking like random noise |

**Note:** Pluggable transport with uniform random-looking output.

**Star count:** ⭐ 892

---

### Snowflake

| Tool | Language | Description |
|------|----------|-------------|
| [Snowflake](https://gitweb.torproject.org/pluggable-transports/snowflake.git) | Go/JavaScript | WebRTC-based PT with volunteer proxies |

**Note:** Uses volunteer-run proxies for Tor bridge connections.

**Star count:** ⭐ 234

---

### WebTunnel

| Tool | Language | Description |
|------|----------|-------------|
| [WebTunnel](https://github.com/Arkanic/WebTunnel) | Go | HTTPS + WebSocket obfuscation |

**Note:** Looks like normal HTTPS traffic with WebSocket tunnel.

**Star count:** ⭐ 156

---

### uTLS

| Tool | Language | Description |
|------|----------|-------------|
| [uTLS](https://github.com/refraction-networking/utls) | Go | TLS fingerprint mimicry library |

**Note:** Spoofs TLS client fingerprints to appear as common browsers.

**Star count:** ⭐ 1.5k

---

### Xray-core

| Tool | Language | Description |
|------|----------|-------------|
| [Xray-core](https://github.com/XTLS/Xray-core) | Go | Primary VLESS implementation with REALITY |

**Note:** Leading V2Ray fork with REALITY TLS fingerprint bypass.

**Star count:** ⭐ 8.2k

---

### sing-box

| Tool | Language | Description |
|------|----------|-------------|
| [sing-box](https://github.com/SagerNet/sing-box) | Go | Universal proxy platform |

**Note:** All-in-one proxy solution supporting multiple protocols.

**Star count:** ⭐ 4.1k

---

### trojan-go

| Tool | Language | Description |
|------|----------|-------------|
| [trojan-go](https://github.com/p4gefau1t/trojan-go) | Go | TLS-wrapped protocol with decoy website |

**Note:** Trojan protocol with TLS tunnel and website mimicry.

**Star count:** ⭐ 3.2k

---

### hysteria

| Tool | Language | Description |
|------|----------|-------------|
| [hysteria](https://github.com/apernet/hysteria) | Go | QUIC-based protocol with obfuscation |

**Note:** High-performance protocol with built-in obfuscation.

**Star count:** ⭐ 4.8k

---

### Shadowsocks

| Tool | Language | Description |
|------|----------|-------------|
| [Shadowsocks](https://github.com/shadowsocks/shadowsocks) | Python/C | SOCKS5-based AEAD protocol |

**Note:** Lightweight encrypted SOCKS5 proxy protocol.

**Star count:** ⭐ 3.5k

---

### NaiveProxy

| Tool | Language | Description |
|------|----------|-------------|
| [NaiveProxy](https://github.com/klzgrad/naiveproxy) | Go/C++ | Chrome-like HTTP/2 fingerprint |

**Note:** Uses Chrome's network stack for traffic mimicry.

**Star count:** ⭐ 2.9k

---

### icmptunnel

| Tool | Language | Description |
|------|----------|-------------|
| [icmptunnel](https://github.com/rozet/icmptunnel) | Go | Tunnel IP traffic over ICMP |

**Note:** Exploits ICMP echo (ping) for data exfiltration.

**Star count:** ⭐ 423

---

## Physical & Social

---

### Printer Steganography Detector

| Tool | Language | Description |
|------|----------|-------------|
| [Printer Steganography Detector](https://github.com/abe-modyo/printer-steganography) | Python | Detect yellow dot matrix printer steganography |

**Note:** Analyzes printer dot patterns for forensic investigation.

**Star count:** ⭐ 89

---

## Steganalysis

---

### stegdetect

| Tool | Language | Description |
|------|----------|-------------|
| [stegdetect](https://github.com/abeluck/stegdetect) | C | Classic CLI steganalysis tool |

**Note:** Detects various steganography methods in images.

**Star count:** ⭐ 156

---

### ALASKA2 steganalysis tools

| Tool | Language | Description |
|------|----------|-------------|
| [ALASKA2 steganalysis tools](https://github.com/YassineYousfi/alaska2-steganalysis) | Python | Includes SRM features for ALASKA2 benchmark |

**Note:** State-of-the-art steganalysis benchmark framework.

**Star count:** ⭐ 312

---

### XuNet

| Tool | Language | Description |
|------|----------|-------------|
| [XuNet](https://github.com/brijeshiitg/XuNet-Structural-Design-of-Convolutional-Neural-Networksfor-Steganalysis) | PyTorch | First CNN steganalyser |

**Note:** Pioneering CNN-based steganalysis architecture.

**Star count:** ⭐ 89

---

### TensorFlow-YeNet

| Tool | Language | Description |
|------|----------|-------------|
| [TensorFlow-YeNet](https://github.com/changshihyoung/TensorFlow-YeNet) | TensorFlow | CNN with SRM-filter preprocessing |

**Note:** Deep learning steganalysis with rich model preprocessing.

**Star count:** ⭐ 156

---

### Pytorch-YeNet

| Tool | Language | Description |
|------|----------|-------------|
| [Pytorch-YeNet](https://github.com/brijeshiitg/Pytorch-Implementation-of-YeNet-Deep-Learning-Hierarchical-Representations-for-Image-Steganalysis-) | PyTorch | PyTorch implementation of YeNet |

**Note:** Efficient CNN steganalysis architecture.

**Star count:** ⭐ 89

---

### Deep-Steganalysis

| Tool | Language | Description |
|------|----------|-------------|
| [Deep-Steganalysis](https://github.com/albblgb/Deep-Steganalysis) | PyTorch | Includes SRNet implementation |

**Note:** Modern deep learning steganalysis framework.

**Star count:** ⭐ 156

---

### Zhu-Net

| Tool | Language | Description |
|------|----------|-------------|
| [Zhu-Net](https://github.com/1204BUPT/Zhu-Net-image-steganalysis) | PyTorch | Efficient spatial CNN steganalyser |

**Note:** Lightweight yet effective CNN steganalysis.

**Star count:** ⭐ 89

---
