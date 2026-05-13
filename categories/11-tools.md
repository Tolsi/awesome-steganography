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
- [Steg](#steg-text-steganography)

**[Image Steganography](#image-steganography)**
- [steghide](#steghide)
- [Stegsolve](#stegsolve)
- [stegano-rs](#stegano-rs)
- [Hermetic Stego](#hermetic-stego)
- [Steg (fabionet)](#steg-fabionet)
- [wbStego](#wbstego)
- [Ermis](#ermis)
- [SilentEye](#silenteye)
- [Stegosuite](#stegosuite)
- [jdvrif](#jdvrif)
- [StegHideX](#steghidex)
- [Steg-GO](#steg-go)
- [Stegify](#stegify)
- [OpenPuff](#openpuff)
- [east-tec InvisibleSecrets](#east-tec-invisiblesecrets)
- [Steganos](#steganos)
- [QuickStego](#quickstego)
- [Xiao Steganography](#xiao-steganography)
- [Stegano Pro](#stegano-pro)
- [SteganPEG](#steganpeg)
- [Pixelknot](#pixelknot) *(Android)*
- [Oversec](#oversec) *(Android)*
- [Steganize](#steganize) *(Android)*
- [Steganography: Hidden Message](#steganography-hidden-message) *(iOS)*
- [S-Tools](#s-tools)
- [Simple Image Steganography](#simple-image-steganography)
- [DevGlan](#devglan-image-steganography) *(Online)*
- [ToolPix](#toolpix) *(Online)*
- [8gwifi](#8gwifi-steganography) *(Online)*
- [StegZero](#stegzero) *(Online)*
- [Manytools](#manytools-steganography) *(Online)*
- [Mobilefish](#mobilefish-steganography) *(Online)*
- [imageonline.io](#imageonline-io-steganography) *(Online)*
- [futureboy.us](#futureboy-us-stegano) *(Online)*
- [Steganography Online Codec](#steganography-online-codec-pelock) *(Online)*
- [StegoApp](#stegoapp) *(Web)*
- [CryptoStego](#cryptostego) *(Web)*
- [SSuite Picsel](#ssuite-picsel)
- [CyberChef](#cyberchef) *(Online)*
- [ChameleonLab](#chameleonlab)
- [steganography (kelvins)](#steganography-kelvins)
- [steganography (stylesuxx)](#steganography-stylesuxx)
- [Deep-Steganography (harveyslash)](#deep-steganography-harveyslash)
- [steganography (kzykhys)](#steganography-kzykhys)
- [HIDEAGEM](#hideagem)
- [Steganography (cyberteach360)](#steganography-cyberteach360)
- [bpcs (mobeets)](#bpcs-mobeets)
- [steganography-app (aksel)](#steganography-app-aksel)
- [stegoVeritas](#stegoveritas)
- [stegtool](#stegtool)
- [Pictograph](#pictograph)
- [hide.py](#hidepy)
- [spatial-image-steganography](#spatial-image-steganography)
- [DCT-Image-Steganography](#dct-image-steganography)
- [fincher](#fincher)
- [DeepSteganography (krishvishal)](#deepsteganography-krishvishal)
- [steganography (mykeels)](#steganography-mykeels)
- [steganography (arjunsr)](#steganography-arjunsr)
- [Steganography (hktaskin)](#steganography-hktaskin)
- [emocrypt](#emocrypt)
- [StegoDisk](#stegodisk)
- [LSB-Audio-Steganography](#lsb-audio-steganography)
- [LSB-Image-Steganography (Monsef-Noubadji)](#lsb-image-steganography-monsef-noubadji)
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
- [steganography (auyer)](#steganography-auyer)
- [jsteg](#jsteg)
- [steganography (scholtes)](#steganography-scholtes)
- [zipography](#zipography)
- [F5-steganography](#f5-steganography-1)
- [AndroidWM](#androidwm)
- [Cryptography (kemingy)](#cryptography-kemingy)
- [steganography (woongbak)](#steganography-woongbak)
- [steganography-dotnet](#steganography-dotnet)
- [brute-force-steganography-tool](#brute-force-steganography-tool)
- [ImageStegano](#imagestegano)
- [Picture-Video-Info-Hiding-EnDecryption](#picture-video-info-hiding-endecryption)
- [Bit-Plane-Slicing-for-Information-Hiding](#bit-plane-slicing-for-information-hiding)
- [Audio-Steganography (Bebra777228)](#audio-steganography-bebra777228)
- [Steganography-Deep-Learning](#steganography-deep-learning)
- [DeepSteganography](#deepsteganography)
- [tweetable-polyglot-png](#tweetable-polyglot-png)
- [stego-toolkit](#stego-toolkit)
- [jphs](#jphs)
- [r5steg](#r5steg)
- [Sekreto](#sekreto)
- [imagemask](#imagemask)
- [lsb-steganography](#lsb-steganography)
- [Steganography-Tools](#steganography-tools)
- [7thSamurai/steganography](#7thsamurai-steganography)

**[QR Steganography](#qr-steganography)**
- [qr-stego](#qr-stego)
- [qrcode-steganography](#qrcode-steganography)
- [stegqr](#stegqr)
- [qrhide](#qrhide)

**[Audio Steganography](#audio-steganography)**
- [DeepSound](#deepsound)
- [mp3stego](#mp3stego)
- [wavmark](#wavmark)
- [audioseal](#audioseal)
- [WavSteg](#wavsteg)
- [spectrology](#spectrology)
- [audio-steganography-algorithms](#audio-steganography-algorithms)
- [HiddenWave](#hiddenwave)
- [Audio-Steganography-CLI](#audio-steganography-cli)
- [stegpy](#stegpy)
- [PixInWav](#pixinwav)
- [PixInWav2](#pixinwav2)
- [steganography-js](#steganography-js)
- [Steganography-Online](#steganography-online)
- [LSB-Steganography-Python](#lsb-steganography-python)
- [image-steganography (goelashwin36)](#image-steganography-goelashwin36)
- [emimg-GUI](#emimg-gui)
- [stegosaurus](#stegosaurus)
- [steganography (gunjannandy)](#steganography-gunjannandy)
- [zwsp-steg-py](#zwsp-steg-py)
- [steganography-png-decoder](#steganography-png-decoder)
- [steganography (atbuy)](#steganography-atbuy)
- [StegsnowBruteForcer](#stegsnowbruteforcer)
- [Steganography (Sanjipan)](#steganography-sanjipan)
- [neural-imaging](#neural-imaging)
- [sigBits](#sigbits)
- [Universal-Deep-Hiding](#universal-deep-hiding)
- [StegaPy](#stegapy)
- [The-A-Files](#the-a-files)
- [invisible-watermark-tool](#invisible-watermark-tool)
- [steganography (subc)](#steganography-subc)
- [steganos](#steganos)
- [LSB_Steganography](#lsb_steganography)
- [steg (surg0r)](#steg-surg0r)
- [fractal-image-steganography](#fractal-image-steganography)
- [LSB_Steganography (omriher)](#lsb_steganography-omriher)
- [lsb (marselester)](#lsb-marselester)
- [covertutils](#covertutils)
- [stegsleuth](#stegsleuth)

**[Video Steganography](#video-steganography)**
- [LVDO](#lvdo)
- [videostego](#videostego)
- [SteganographierGUI](#steganographiergui)
- [Video-Steganography (Amritaryal44)](#video-steganography-amritaryal44)
- [Video-Steganography (llopen-sourcell)](#video-steganography-llopen-sourcell)
- [Deep-Video-Steganography](#deep-video-steganography)

**[Network Steganography](#network-steganography)**
- [iodine](#iodine)
- [dnscat2](#dnscat2)
- [dns2tcp](#dns2tcp)
- [covertovert](#covertovert)
- [covert-tube](#covert-tube)
- [Ectoplasm-Steganography](#ectoplasm-steganography)
- [stegator](#stegator)
- [PacketWhisper](#packetwhisper)
- [Dissembling-Ferret](#dissembling-ferret)
- [StegoAuth](#stegoauth)
- [PyExfil](#pyexfil)
- [ICMPStegano](#icmpstegano)

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

**[Steganography Detection](#steganography-detection)**
- [StegExpose](#stegexpose)
- [StegSpy](#stegspy)
- [StegCracker](#stegcracker)
- [Stegbreak](#stegbreak)
- [StegVerifier](#stegverifier)

**[Steganalysis](#steganalysis)**
- [stegdetect](#stegdetect)
- [ALASKA2 steganalysis tools](#alaska2-steganalysis-tools)
- [XuNet](#xunet)
- [TensorFlow-YeNet](#tensorflow-yenet)
- [Pytorch-YeNet](#pytorch-yenet)
- [Deep-Steganalysis](#deep-steganalysis)
- [Zhu-Net](#zhu-net)
- [AperiSolve](#aperisolve)
- [Stegano](#stegano)
- [StegOnline](#stegonline)
- [steghide (Stegseek)](#steghide-stegseek)
- [cloacked-pixel](#cloacked-pixel)
- [StegoForge](#stegoforge)
- [LSB-Steganography](#lsb-steganography-1)
- [Matroschka](#matroschka)
- [Chaya](#chaya)
- [f5-steganography](#f5-steganography)
- [ch3r0](#ch3r0)
- [ReconEXIF](#reconexif)
- [Steganography-Software](#steganography-software)
- [binary_steganography](#binary_steganography)
- [node-stego](#node-stego)
- [photochat](#photochat)
- [PDFStego](#pdfstego)
- [ExeSteganography](#exesteganography)
- [exe2png](#exe2png)
- [stegify-mobile](#stegify-mobile)
- [stegbrute](#stegbrute)
- [stego-toolkit-nix](#stego-toolkit-nix)
- [euli_treasure_hunt](#euli_treasure_hunt)
- [Cipher-Sphere](#cipher-sphere)
- [steganography (teovoinea)](#steganography-teovoinea)
- [stegify-flutter-plugin](#stegify-flutter-plugin)
- [NeuralSteganography](#neuralsteganography)
- [PyTorch-Deep-Image-Steganography](#pytorch-deep-image-steganography)
- [VHiddenNet](#vhiddennet)
- [stegoTool (jonsalchichonnn)](#stegotool-jonsalchichonnn)
- [steganography (browningjp)](#steganography-browningjp)
- [Text-steganography (sakship31)](#text-steganography-sakship31)
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

### snow10

| Tool | Language | Description |
|------|----------|-------------|
| [snow10](https://github.com/andersonr/snow10) | Python | Modern SNOW whitespace steganography implementation |

**Note:** Python implementation of SNOW whitespace steganography.

**Star count:** ⭐ 12

---

### snow.js

| Tool | Language | Description |
|------|----------|-------------|
| [snow.js](https://github.com/MorseTheCode/snow.js) | JavaScript | JavaScript implementation of SNOW whitespace steganography |

**Note:** Browser-friendly SNOW whitespace steganography.

**Star count:** ⭐ 6

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

### acrostic-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [acrostic-steganography](https://github.com/utkarshp001/acrostic-steganography) | Python | Acrostic message encoding in text |

**Note:** Hides messages using first letters of each line (acrostic method).

**Star count:** ⭐ 12

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

### Steg (text steganography)

| Tool | Language | Description |
|------|----------|-------------|
| [Steg](https://github.com/geezee/steg) | D | Text steganography using whitespace encoding |

**Note:** Allows hiding information in ASCII text using different encodings for whitespace.

**Star count:** ⭐ 52

---

## Image Steganography

---

### steghide

| Tool | Language | Description |
|------|----------|-------------|
| [steghide](https://github.com/StegHigh/steghide) | C++ | Classic LSB tool for image and audio |

**Note:** One of the most well-known open-source steganography tools.

**Star count:** ⭐ 1.8k

---

### SteganoHide

| Tool | Language | Description |
|------|----------|-------------|
| [SteganoHide](https://github.com/GH0STH4CKER/SteganoHide) | Python | Image steganography tool with LSB encoding |

**Note:** Python tool for hiding data in images.

**Star count:** ⭐ 5

---

### zsteg

| Tool | Language | Description |
|------|----------|-------------|
| [zsteg](https://github.com/zed-0xff/zsteg) | Ruby | Detects hidden data in PNG and BMP images |

**Note:** Specialized in detecting LSB and other steganography methods in images. Supports zlib, bmp, lsb methods.

**Star count:** ⭐ 1.1k

---

### stegano-rs

| Tool | Language | Description |
|------|----------|-------------|
| [stegano-rs](https://github.com/steganogram/stegano-rs) | Rust | Cross-platform CLI tool for steganography focused on performance and simplicity |

**Note:** Rust-based steganography tool with focus on speed and ease of use.

**Star count:** ⭐ 6

---

### Hermetic Stego

| Tool | Type | Description |
|------|------|-------------|
| [Hermetic Stego](https://hermetic-stego.soft112.com/) | Freeware (Windows) | Steganography program with encryption for hiding data in images |

**Note:** Windows steganography tool with encryption capabilities.

---

### Steg (fabionet)

| Tool | Type | Description |
|------|------|-------------|
| [Steg](https://www.fabionet.org/) | Open Source (C++) | Cross-platform portable steganography software |

**Note:** Easy cross-platform steganography tool written in C++.

---

### wbStego

| Tool | Type | Description |
|------|------|-------------|
| [wbStego](http://bailer.at/wbstego/) | Open Source | Steganography tool for bitmaps, text and HTML files |

**Note:** Published under GNU GPL, supports multiple file formats.

---

### Ermis

| Tool | Type | Description |
|------|------|-------------|
| [Ermis](https://flathub.org/en/apps/io.github.alamahant.Ermis) | Open Source (Flathub) | Cross-platform steganography application for hiding content in images or audio |

**Note:** Modern cross-platform steganography app available on Flathub.

---

### Stegsolve

| Tool | Language | Description |
|------|----------|-------------|
| [Stegsolve](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve) | Java | Bit-plane/color-filter visualization GUI |

**Note:** Essential CTF tool for analyzing images through different color filters and bit-planes.

**Star count:** ⭐ 683 (sec-tools repo)

**Last commit:** 2016

---

### SilentEye

| Tool | Language | Description |
|------|----------|-------------|
| [SilentEye](https://github.com/achorein/silenteye) | C++ (Qt) | Cross-platform steganography tool for hiding data in images and audio |

**Note:** Easy-to-use GUI application supporting AES-256 encryption.

**Star count:** ⭐ 142

**Last commit:** 2023

---

### Stegosuite

| Tool | Language | Description |
|------|----------|-------------|
| [Stegosuite](https://github.com/osde8info/stegosuite) | Java | Open source steganography tool to hide information in image files |

**Star count:** ⭐ 45

**Last commit:** 2025

---

### jdvrif

| Tool | Language | Description |
|------|----------|-------------|
| [jdvrif](https://github.com/CleasbyCode/jdvrif) | C++ | Steganography tool for JPG images with metadata and zlib compression support |

**Star count:** ⭐ 66

**Last commit:** 2025

---

### StegHideX

| Tool | Language | Description |
|------|----------|-------------|
| [StegHideX](https://github.com/Rooted-Development/StegHideX) | Python | Python-based steganography tool for hiding files inside images securely |

**Note:** Modern Python tool for steganography with secure file hiding capabilities.

**Star count:** ⭐ 15

---

### Steg-GO

| Tool | Language | Description |
|------|----------|-------------|
| [Steg-GO](https://github.com/Uttkarsh-raj/Steg-GO) | Go | Open-source steganography tool built in Golang |

**Note:** Go-based CLI tool for image steganography.

**Star count:** ⭐ 10

---

### Stegify

| Tool | Language | Description |
|------|----------|-------------|
| [Stegify](https://github.com/DimitarPetrov/stegify) | Go | LSB steganography tool, capable of hiding any file within an image |

**Note:** Go-based CLI tool for LSB steganography in PNG and JPEG images.

**Star count:** ⭐ 1.3k

**Last commit:** 2023

---

### steganography (kelvins)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/kelvins/steganography) | Python | Educational steganography library |

**Note:** Comprehensive Python library for learning steganography.

**Star count:** ⭐ 365

---

### OpenPuff

| Tool | Type | Description |
|------|------|-------------|
| [OpenPuff](https://www.openpuff.com/) | Commercial (Windows) | Professional steganography tool supporting images, audio, and video carrier files |

**Note:** Windows-based tool with strong encryption and multi-carrier support.

---

### east-tec InvisibleSecrets

| Tool | Type | Description |
|------|------|-------------|
| [InvisibleSecrets](https://www.east-tec.com/invisiblesecrets/) | Commercial (Windows) | Steganography and file encryption software for hiding data in images, audio, and documents |

**Note:** Award-winning Windows steganography tool with encryption features. Supports various carrier formats.

---

### Steganos (Encrypt, Hide & Share)

| Tool | Type | Description |
|------|------|-------------|
| [Steganos](https://apps.microsoft.com/detail/9n4tj9j1ckn5) | Windows (Microsoft Store) | Mobile steganography app with AES-256 encryption and self-extracting archives |

**Note:** Modern Windows app combining encryption and steganography.

---

### QuickStego

| Tool | Type | Description |
|------|------|-------------|
| [QuickStego](http://quickstego.com/) | Freeware (Windows) | Simple steganography tool for hiding text and files in images |

**Note:** Beginner-friendly tool for basic steganography tasks.

---

### r5steg

| Tool | Type | Description |
|------|------|-------------|
| [r5steg](https://github.com/daniellerch/r5steg) | Windows | JPEG steganography tool using F5 algorithm |

**Note:** Windows tool implementing F5 steganography algorithm for JPEG images.

---

### Sekreto

| Tool | Type | Description |
|------|------|-------------|
| [Sekreto](https://github.com/guogbonncc/sekreto) | Windows/Android | Steganography tool for PC and Android |

**Note:** Cross-platform steganography tool supporting both desktop and mobile. Uses custom encoding method.

---

### Xiao Steganography

| Tool | Type | Description |
|------|------|-------------|
| [Xiao Steganography](https://xiao-steganography.en.softonic.com/) | Freeware (Windows) | Hide confidential data within image and audio files |

**Note:** Windows tool supporting BMP and WAV carriers.

---

### Stegano Pro

| Tool | Type | Description |
|------|------|-------------|
| [Stegano Pro](https://apps.microsoft.com/detail/9p6xh5xr280v) | Free (Windows Store) | Steganography made easy - securely hide texts and files |

**Note:** Modern Windows Store application for basic steganography.

---

### Pixelknot

| Tool | Type | Description |
|------|------|-------------|
| [Pixelknot](https://guardianproject.info/archives/pixelknot/) | Android | Hide encrypted messages in photos |

**Note:** Open source Android app by Guardian Project. Uses steganography to hide short messages in images.

---

### Oversec

| Tool | Type | Description |
|------|------|-------------|
| [Oversec](https://oversec.net/) | Android | Steganography app that encodes text into images in real-time + reads encrypted text from screen |

**Note:** Android app that can encode text directly into camera viewfinder or existing images. Supports both invisible ink mode and visible encoding. Can decrypt and read hidden text directly from screen and overlay decrypted content on top of the device screen in real-time.

---

### Steganize

| Tool | Type | Description |
|------|------|-------------|
| [Steganize](https://play.google.com/store/apps/details?id=com.byte9962.steganize) | Android | Hide text in images using LSB encoding |

**Note:** Android app for hiding secret messages in images with password protection.

---

### Steganography: Hidden Message

| Tool | Type | Description |
|------|------|-------------|
| [Steganography: Hidden Message](https://apps.apple.com/us/app/steganography-hidden-message/id1565634629) | iOS | Hide secret messages inside photos |

**Note:** iOS app for encoding hidden messages in images.

---

### SteganPEG

| Tool | Type | Description |
|------|------|-------------|
| [SteganPEG](https://steganpeg.apponic.com/) | Freeware (Windows) | Application of Steganography to JPEG images |

**Note:** Specializes in JPEG steganography.

---

### S-Tools

| Tool | Type | Description |
|------|------|-------------|
| [S-Tools](https://sourceforge.net/projects/steganographyv20/) | Freeware (Windows) | Classic steganography tool for hiding data in images and audio |

**Note:** One of the oldest steganography tools, supports BMP, GIF, WAV.

---

### Simple Image Steganography

| Tool | Type | Description |
|------|------|-------------|
| [Simple Image Steganography](https://www.softpedia.com/get/Security/Encrypting/Simple-Image-Steganography.shtml) | Freeware (Windows) | Hide data inside an image file |

**Note:** Lightweight tool for basic LSB steganography.

---

### Online Tools

#### DevGlan Image Steganography

| Tool | Type | Description |
|------|------|-------------|
| [DevGlan](https://www.devglan.com/online-tools/image-steganography-online) | Web | Online image steganography tool for embedding secret text |

**Note:** Browser-based tool using LSB encoding.

#### ToolPix

| Tool | Type | Description |
|------|------|-------------|
| [ToolPix](https://toolpix.pythonanywhere.com/image-editor/steganography) | Web | Image steganography tool on PythonAnywhere |

**Note:** Supports PNG and JPG images.

#### 8gwifi Steganography

| Tool | Type | Description |
|------|------|-------------|
| [8gwifi](https://8gwifi.org/steganography-tool.jsp) | Web | Advanced steganography tool for images and WAV audio |

**Note:** Online tool with multiple carrier formats.

#### StegZero

| Tool | Type | Description |
|------|------|-------------|
| [StegZero](https://stegzero.com) | Web | Zero-width steganography decoder and encoder |

**Note:** Specializes in zero-width character steganography for text.

#### Manytools Steganography

| Tool | Type | Description |
|------|------|-------------|
| [Manytools](https://manytools.org/hacker-tools/steganography-encode-text-into-image/) | Web | Hide text messages in images using LSB encoding |

**Note:** Free online tool for encoding text into images.

#### Mobilefish Steganography

| Tool | Type | Description |
|------|------|-------------|
| [Mobilefish](https://www.mobilefish.com/services/steganography/steganography.php) | Web | Online steganography service for hiding messages or files in images |

**Note:** Supports various image formats and file embedding.

#### imageonline.io Steganography

| Tool | Type | Description |
|------|------|-------------|
| [imageonline.io](https://imageonline.io/steganography-online/) | Web | Hide secret text messages in images online |

**Note:** Simple web-based steganography encoder and decoder.

#### futureboy.us Stegano

| Tool | Type | Description |
|------|------|-------------|
| [futureboy.us](https://futureboy.us/stegano/encinput.html) | Web | Steganographic encoder for hiding messages in images |

**Note:** Classic online tool by Alan Eliasen.

---

### Steganography Online Codec (PELock)

| Tool | Type | Description |
|------|------|-------------|
| [Steganography Online Codec](https://www.pelock.com/products/steganography-online-codec) | Web | Hide encrypted messages in images using AES-256 + PBKDF2 |

**Note:** Online steganography tool with strong encryption. Supports PNG, JPG, GIF, BMP formats. Client-side processing - images are not stored on server.

---

### ChameleonLab

| Tool | Type | Description |
|------|------|-------------|
| [ChameleonLab](https://chalab.ru/) | Windows/macOS | Professional steganography and cryptography suite with GUI |

**Note:** Russian tool supporting PNG, BMP, PDF, DOCX, XLSX, PPTX, and other formats. Includes both embedding/extraction and steganalysis features.

---

### CyberChef

| Tool | Type | Description |
|------|------|-------------|
| [CyberChef](https://gchq.github.io/CyberChef/) | Web | The Cyber Swiss Army Knife - includes steganography recipes for LSB extraction and more |

**Note:** Open source tool by GCHQ. Multi-purpose tool that includes steganography operations via recipes. Great for quick analysis and extraction tasks.

---

### steganography (stylesuxx)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/stylesuxx/steganography) | JavaScript | JavaScript steganography library |

**Note:** JavaScript library for image steganography.

**Star count:** ⭐ 160

---

### Deep-Steganography (harveyslash)

| Tool | Language | Description |
|------|----------|-------------|
| [Deep-Steganography](https://github.com/harveyslash/Deep-Steganography) | Python | Deep learning steganography |

**Note:** TensorFlow implementation of deep learning steganography.

**Star count:** ⭐ 214

---

### steganography (kzykhys)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/kzykhys/Steganography) | PHP | PHP steganography library (2023) |

**Note:** PHP library for steganography.

**Star count:** ⭐ 88

---

### HIDEAGEM

| Tool | Language | Description |
|------|----------|-------------|
| [HIDEAGEM](https://github.com/CYBERGEM777/HIDEAGEM) | Python | Multi-format steganography tool (2024) |

**Note:** Comprehensive steganography tool for multiple formats.

**Star count:** ⭐ 441

---

### Steganography (cyberteach360)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/cyberteach360/Steganography) | Python | Educational steganography tool (2022) |

**Note:** Teaching tool for learning steganography.

**Star count:** ⭐ 38

---

### bpcs (mobeets)

| Tool | Language | Description |
|------|----------|-------------|
| [bpcs](https://github.com/mobeets/bpcs) | Python | BPCS steganography implementation (2024) |

**Note:** BPCS (Bit-Plane Complexity Segmentation) steganography.

**Star count:** ⭐ 32

---

### steganography-app (aksel)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography-app](https://github.com/aksel/steganography-app) | Python | GUI steganography application (2021) [archived] |

**Note:** Desktop GUI application for steganography.

**Star count:** ⭐ 40

---

### stegoVeritas

| Tool | Language | Description |
|------|----------|-------------|
| [stegoVeritas](https://github.com/bannsec/stegoVeritas) | Python | Steganography analysis tool (2026) |

**Note:** Advanced steganography analysis and extraction tool.

**Star count:** —

---

### stegtool

| Tool | Language | Description |
|------|----------|-------------|
| [stegtool](https://github.com/djhworld/stegtool) | Python | Steganography tool (2020) |

**Note:** Simple steganography tool.

**Star count:** ⭐ 52

---

### Pictograph

| Tool | Language | Description |
|------|----------|-------------|
| [Pictograph](https://github.com/MrAdamBoyd/Pictograph) | Python | Image steganography tool (2021) |

**Note:** Tool for hiding messages in images.

**Star count:** ⭐ 77

---

### hide.py

| Tool | Language | Description |
|------|----------|-------------|
| [hide.py](https://github.com/nukeop/hide.py) | Python | Simple steganography tool (2018) [archived] |

**Note:** Easy-to-use steganography tool.

**Star count:** ⭐ 109

---

### spatial-image-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [spatial-image-steganography](https://github.com/JianhuaYang001/spatial-image-steganography) | Python | Spatial image steganography (2019) |

**Note:** Research implementation of spatial steganography.

**Star count:** ⭐ 34

---

### DCT-Image-Steganography

| Tool | Language | Description |
|------|----------|-------------|
| [DCT-Image-Steganography](https://github.com/MasonEdgar/DCT-Image-Steganography) | Python | DCT-based image steganography (2024) |

**Note:** Implementation of DCT steganography.

**Star count:** —

---

### fincher

| Tool | Language | Description |
|------|----------|-------------|
| [fincher](https://github.com/maxfierke/fincher) | Crystal | Crystal steganography library (2025) |

**Note:** Steganography library for Crystal language.

**Star count:** ⭐ 90

---

### DeepSteganography (krishvishal)

| Tool | Language | Description |
|------|----------|-------------|
| [DeepSteganography](https://github.com/krishvishal/DeepSteganography) | Python | Deep learning steganography (2018) |

**Note:** Implementation of deep learning steganography.

**Star count:** ⭐ 40

---

### steganography (mykeels)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/mykeels/steganography) | JavaScript | JavaScript steganography (2023) |

**Note:** JavaScript implementation of steganography.

**Star count:** ⭐ 20

---

### steganography (arjunsr)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/arjunsr/steganography) | Python | Python steganography (2011) [archived] |

**Note:** Early Python steganography tool.

**Star count:** ⭐ 4

---

### Steganography (hktaskin)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/hktaskin/Steganography) | Python | Python steganography (2013) |

**Note:** Simple steganography implementation.

**Star count:** —

---

### emocrypt

| Tool | Language | Description |
|------|----------|-------------|
| [emocrypt](https://github.com/degaart/emocrypt) | Python | Emoji-based steganography (2022) |

**Note:** Steganography using emojis to hide messages.

**Star count:** ⭐ 37

---

### StegoDisk

| Tool | Language | Description |
|------|----------|-------------|
| [StegoDisk](https://github.com/MatusKysel/StegoDisk) | Go | Go steganography library (2026) |

**Note:** Steganography library for disk files.

**Star count:** ⭐ 8

---

### LSB-Audio-Steganography

| Tool | Language | Description |
|------|----------|-------------|
| [LSB-Audio-Steganography](https://github.com/Ibrahim-Benkhedda/LSB-Audio-Steganography) | Python | LSB audio steganography (2024) |

**Note:** LSB steganography for WAV audio files.

**Star count:** ⭐ 5

---

### LSB-Image-Steganography (Monsef-Noubadji)

| Tool | Language | Description |
|------|----------|-------------|
| [LSB-Image-Steganography](https://github.com/Monsef-Noubadji/LSB-Image-Steganography) | PHP | LSB image steganography (2022) |

**Note:** PHP implementation of LSB steganography.

**Star count:** ⭐ 1

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
| [stegolab](https://github.com/daniellerch/stegolab) | Python | Comprehensive steganography, steganalysis, and watermarking framework |

**Features:**
- **Steganography:** Binary/Ternary Hamming codes, Wet Paper Codes, STC (Syndrome Trellis Codes), S-UNIWARD, J-UNIWARD, HILL, RBV
- **Steganalysis:** ATS attack, Calibration Attack, pyEC (Ensemble Classifiers)
- **Watermarking:** E-Blind, E-Fixed-LC, E-blk-Blind, E-Simple-8, E-Trellis-8, H[i]dden

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

### HiDDeN ( alternatives)

| Tool | Language | Description |
|------|----------|-------------|
| [TomTomTommi/HiNet](https://github.com/TomTomTommi/HiNet) | PyTorch | Official ICCV 2021 — invertible network ⭐205 |
| [TomTomTommi/DeepMIH](https://github.com/TomTomTommi/DeepMIH) | PyTorch | Official TPAMI 2022 — multiple image hiding ⭐131 |
| [Brittany-Chen/InvMIHNet](https://github.com/Brittany-Chen/InvMIHNet) | PyTorch | Large capacity image steganography ⭐12 |
| [zhangle408/CNGI-Net](https://github.com/zhangle408/CNGI-Net-Contrastive-Noise-Guided-Invertible-Network-for-Image-Steganography) | PyTorch | Contrastive noise-guided INN ⭐3 |
| [Cone-bottle-Cs/FastISN](https://github.com/Cone-bottle-Cs/FastISN) | PyTorch | Fast invertible network video stego ⭐2 |
| [zhangle408/EUIN-Net](https://github.com/zhangle408/EUIN-Net-EFFICIENT-U-SHAPE-INVERTIBLE-NEURAL-NETWORK-FOR-IMAGE-STEGANOGRAPHY) | PyTorch | Efficient U-shape INN ⭐1 |
| [c4Tch3r/HIANet](https://github.com/c4Tch3r/HIANet) | PyTorch | Auditory masking effect INN |
| [XU001006/MIRA](https://github.com/XU001006/MIRA) | PyTorch | Multi-scale video steganography |

**Note:** Original HiDDeN repo (tancik/HiDDeN) archived. HiNet/DeepMIH are official PyTorch implementations of state-of-the-art invertible network approaches.

---

### SteganoGAN ( alternatives)

| Tool | Language | Description |
|------|----------|-------------|
| [DAI-Lab/SteganoGAN](https://github.com/DAI-Lab/SteganoGAN) | Python | Original GAN-based steganography 2-4 bpp ⭐428 |
| [DAI-Lab/SteganoGAN forks](https://github.com/DAI-Lab/SteganoGAN/network/members) | Python | 100+ forks with variations |

**Note:** SteganoGAN generates stego images using GANs. Multiple forks exist with architectural variations.

---

### StegaStamp

| Tool | Language | Description |
|------|----------|-------------|
| [StegaStamp](https://github.com/tancik/StegaStamp) | TensorFlow | Robust encoder surviving print+photo transmission |
| [StegaStamp-pytorch](https://github.com/jsrdcht/StegaStamp-pytorch) | PyTorch | PyTorch reimplementation of StegaStamp |
| [StegaStamp (ytfrdfiw)](https://github.com/ytfrdfiw/StegaStamp) | TensorFlow | Fork with detector model for StegaStamp detection |
| [vadishev/stegastamp-original](https://huggingface.co/vadishev/stegastamp-original) | PyTorch | Pretrained model (COCO, 99.6% bit accuracy) |

**Note:** Invisible watermark that survives geometric distortions and photo capture. The pytorch version provides training/inference scripts. The ytfrdfiw fork adds detector model for detecting StegaStamps in images.

**Star count:** ⭐ 1.2k

---

### CRoSS

| Tool | Language | Description |
|------|----------|-------------|
| [CRoSS](https://github.com/yujiwen/CRoSS) | PyTorch | Coverless steganography via diffusion models (NeurIPS 2023) |

**Note:** Generates images that inherently contain hidden information.

**Star count:** ⭐ 157

---

### RoSteALS

| Tool | Language | Description |
|------|----------|-------------|
| [RoSteALS](https://github.com/TuBui/RoSteALS) | Python | Robust steganography using autoencoder latent space (CVPR 2023) [[Poster]](https://ningyu1991.github.io/homepage_files/poster_RoSteALS.pdf) |

**Note:** Uses frozen VQ autoencoder latent space for robust data hiding. Supports 100-bit payload with BCH error correction.

**Star count:** ⭐ 107

---

### BackdoorImageEditing

| Tool | Language | Description |
|------|----------|-------------|
| [BackdoorImageEditing](https://github.com/aiiu-lab/BackdoorImageEditing) | Python | Invisible backdoor triggers in image editing models via deep watermarking (AVSS 2025) |
| [yufengcccc/Backdoor_InstructPix2Pix_StegaStamp_CAT](https://huggingface.co/yufengcccc/Backdoor_InstructPix2Pix_StegaStamp_CAT) | Diffusers | Backdoor model for InstructPix2Pix [[1]](https://arxiv.org/abs/2506.04879) |

**Note:** Embeds invisible backdoors in image editing models using StegaStamp-based watermarking. When triggered, the model produces specific outputs controlled by the watermark.

**Star count:** ⭐ 7

---

### VINE

| Tool | Language | Description |
|------|----------|-------------|
| [VINE](https://github.com/Shilin-LU/VINE) | Python | Robust watermarking against image editing via SDXL-Turbo (ICLR 2025) |

**Note:** Uses frequency-based surrogate training and diffusion models for watermark robustness against regeneration, global/local editing, and image-to-video. Includes W-Bench benchmark.

**Star count:** ⭐ 383

---

### stegify

| Tool | Language | Description |
|------|----------|-------------|
| [stegify](https://github.com/DimitarPetrov/stegify) | Go | LSB steganography tool for hiding files in images |

**Note:** Go tool for LSB steganography, capable of hiding any file within an image.

**Star count:** ⭐ 1.3k

---

### steganography (auyer)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/auyer/steganography) | Go | Go library for image steganography |

**Note:** Pure Go implementation for hiding data in images.

**Star count:** ⭐ 354

---

### jsteg

| Tool | Language | Description |
|------|----------|-------------|
| [jsteg](https://github.com/lukechampine/jsteg) | Go | JPEG steganography in Go |

**Note:** Simple and fast JPEG steganography in Go.

**Star count:** ⭐ 639

---

### steganography (scholtes)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/scholtes/steganography) | Ruby | Ruby steganography library |

**Note:** Ruby implementation for image steganography.

**Star count:** ⭐ 3

---

### zipography

| Tool | Language | Description |
|------|----------|-------------|
| [zipography](https://github.com/gromnitsky/zipography) | Ruby | LSB steganography in Ruby |

**Note:** Ruby library for zip-based steganography.

**Star count:** ⭐ 10

---

### F5-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [F5-steganography](https://github.com/matthewgao/F5-steganography) | Java | F5 algorithm implementation in Java |

**Note:** Java implementation of F5 JPEG steganography.

**Star count:** ⭐ 263

---

### AndroidWM

| Tool | Language | Description |
|------|----------|-------------|
| [AndroidWM](https://github.com/huangyz0918/AndroidWM) | Java | Android watermark library |

**Note:** Android library for image watermarking and steganography.

**Star count:** ⭐ 1.6k

---

### Cryptography (kemingy)

| Tool | Language | Description |
|------|----------|-------------|
| [Cryptography](https://github.com/kemingy/Cryptography) | C | LSB steganography in C [archived] |

**Note:** Early C implementation of LSB steganography.

**Star count:** ⭐ 20

---

### steganography (woongbak)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/woongbak/Steganography) | C# | C# steganography implementation |

**Note:** C# implementation for image steganography.

**Star count:** ⭐ 6

---

### steganography-dotnet

| Tool | Language | Description |
|------|----------|-------------|
| [steganography-dotnet](https://github.com/suadev/steganography-dotnet) | C# | .NET steganography library |

**Note:** .NET library for image steganography.

**Star count:** ⭐ 25

---

### brute-force-steganography-tool

| Tool | Language | Description |
|------|----------|-------------|
| [brute-force-steganography-tool](https://github.com/bpotaman/brute-force-steganography-tool) | Python | Brute force tool for LSB steganography |

**Note:** Tool for brute-forcing LSB steganography passwords.

**Star count:** ⭐ 0

---

### ImageStegano

| Tool | Language | Description |
|------|----------|-------------|
| [ImageStegano](https://github.com/zabbidou/ImageStegano) | Python | Image steganography tool |

**Note:** Simple image steganography implementation.

**Star count:** ⭐ 0

---

### Picture-Video-Info-Hiding-EnDecryption

| Tool | Language | Description |
|------|----------|-------------|
| [Picture-Video-Info-Hiding-EnDecryption](https://github.com/HollowMan6/Picture-Video-Info-Hiding-EnDecryption) | Python | Multi-format info hiding for pictures and videos |

**Note:** Tool for information hiding in pictures and videos.

**Star count:** ⭐ 29

---

### Bit-Plane-Slicing-for-Information-Hiding

| Tool | Language | Description |
|------|----------|-------------|
| [Bit-Plane-Slicing-for-Information-Hiding](https://github.com/AbhishekPoojary/Bit-Plane-Slicing-for-Information-Hiding) | Python | Bit plane slicing technique for info hiding |

**Note:** Implementation of bit plane slicing for information hiding.

**Star count:** ⭐ 36

---

### Audio-Steganography (Bebra777228)

| Tool | Language | Description |
|------|----------|-------------|
| [Audio-Steganography](https://github.com/Bebra777228/Audio-Steganography) | Python | Audio steganography implementation |

**Note:** Simple audio steganography tool.

**Star count:** ⭐ 5

---

### Steganography-Deep-Learning

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-Deep-Learning](https://github.com/saadzia10/Steganography-Deep-Learning) | Python | Deep learning steganography research |

**Note:** Research project on deep learning for steganography.

**Star count:** ⭐ 15

---

### DeepSteganography

| Tool | Language | Description |
|------|----------|-------------|
| [DeepSteganography](https://github.com/JapsimarSinghWahi/DeepSteganography) | PyTorch | Deep neural network steganography |

**Note:** PyTorch implementation of neural steganography.

**Star count:** ⭐ 54

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

### jphs

| Tool | Language | Description |
|------|----------|-------------|
| [jphs](https://github.com/h3xx/jphs) | C | JStegHide Plus - JPEG steganography |

**Note:** JPEG steganography tool with improved implementation.

**Star count:** ⭐ 90

---

### imagemask

| Tool | Language | Description |
|------|----------|-------------|
| [imagemask](https://github.com/kingthy/imagemask) | Python | Image masking steganography |

**Note:** Hides data by masking regions in images.

**Star count:** ⭐ 68

---

### lsb-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [lsb-steganography](https://github.com/Aqcurate/lsb-steganography) | Python | LSB encoding/decoding for images |

**Note:** Simple LSB steganography implementation for PNG images.

**Star count:** ⭐ 79

---

### Steganography-Tools

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-Tools](https://github.com/Priyansh-15/Steganography-Tools) | Python | Multi-format steganography toolkit |

**Note:** Supports image, video, and text steganography with encryption.

**Star count:** ⭐ 111

---

### 7thSamurai/steganography

| Tool | Language | Description |
|------|----------|-------------|
| [7thSamurai/steganography](https://github.com/7thSamurai/steganography) | Python | Cryptography and steganography library |

**Note:** Comprehensive library with AES encryption and multiple stego methods.

**Star count:** ⭐ 1.1k

---

## QR Steganography

---

### qr-stego

| Tool | Language | Description |
|------|----------|-------------|
| [qr-stego](https://github.com/QR-Steganography/qr-stego) | Python | LSB in QR code padding/remainder, BCH-ECC |

**Note:** Hides data in QR code padding bytes with error correction.

**Star count:** ⭐ 12

---

### qrcode-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [qrcode-steganography](https://github.com/simonw/qrcode-stego) | Python | Dual payload: visible QR + hidden data, uses reedsolo |

**Note:** Embeds additional data in QR code with dual payload support.

**Star count:** ⭐ 89

---

### stegqr

| Tool | Language | Description |
|------|----------|-------------|
| [stegqr](https://github.com/ricmoo/stegqr) | Python | Masks data as artistic QR, error injection |

**Note:** Creates artistic QR codes with hidden data.

**Star count:** ⭐ 156

---

### qrhide

| Tool | Language | Description |
|------|----------|-------------|
| [qrhide](https://github.com/QRHide/qrhide) | Go | Fast LSB in QR EC blocks, print-robust |

**Note:** Hides data in QR error correction blocks, robust to printing.

**Star count:** ⭐ 34

---

### steganography-QRcode

| Tool | Language | Description |
|------|----------|-------------|
| [steganography-QRcode](https://github.com/MitanshiKshatriya/steganography-QRcode) | Python | QR code based steganography implementation |

**Note:** QR code steganography tool.

**Star count:** ⭐ 3

---

### StegoQR

| Tool | Language | Description |
|------|----------|-------------|
| [StegoQR](https://github.com/leonardean/StegoQR) | Python | QR steganography with visual patterns |

**Note:** Embeds hidden data in QR code visual patterns.

**Star count:** ⭐ 18

---

### StegoApp

| Tool | Type | Description |
|------|------|-------------|
| [StegoApp](https://stego.app) | Web | Browser-based steganography tool for PNG and JPG images |

**Note:** Runs in the browser with custom robust embedding method. Free tier with premium options.

---

### CryptoStego

| Tool | Type | Description |
|------|------|-------------|
| [CryptoStego](https://stego.js.org/) | Web | Browser-based steganography tool for PNG and JPG images |

**Note:** Uses LSB replacement for PNG and custom method for JPG. MIT licensed.

---

### SSuite Picsel

| Tool | Platform | Description |
|------|----------|-------------|
| [SSuite Picsel](https://www.ssuiteoffice.com/software/ssuitepicselsecurity.htm) | Windows/Mac/Linux | Steganography tool for BMP, PNG, and JPG images |

**Note:** Simple steganography tool with graphical interface. Freeware.

---

## Audio Steganography

---

### DeepSound

| Tool | Language | Description |
|------|----------|-------------|
| [DeepSound](https://github.com/Jpinsoft/DeepSound) | Python | Autoencoder-based audio steganography |

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

### LD-RoViS

| Tool | Language | Description |
|------|----------|-------------|
| [LD-RoViS](https://github.com/xiangkun1999/LD-RoViS) | Python | Learning-based RoViS (Robust Video Steganography) |

**Note:** Deep learning-based video steganography using adversarial training.

**Star count:** ⭐ 67

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

### Video-Steganography (Amritaryal44)

| Tool | Language | Description |
|------|----------|-------------|
| [Video-Steganography](https://github.com/Amritaryal44/Video-Steganography) | Python | Video steganography using LSB |

**Note:** Simple video steganography implementation using least significant bits.

**Star count:** ⭐ 72

---

### Video-Steganography (llopen-sourcell)

| Tool | Language | Description |
|------|----------|-------------|
| [Video-Steganography](https://github.com/llopen-sourcell/Video-Steganography) | Python | LSB-based video steganography |

**Note:** Frame-based video steganography for hiding data.

**Star count:** ⭐ 38

---

### Deep-Video-Steganography

| Tool | Language | Description |
|------|----------|-------------|
| [Deep-Video-Steganography](https://github.com/anilsathyan7/Deep-Video-Steganography-Hiding-Videos-in-Plain-Sight) | Python/TensorFlow | Neural network video steganography |

**Note:** Deep learning approach to hiding videos within videos.

**Star count:** ⭐ 56

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

### covertovert

| Tool | Language | Description |
|------|----------|-------------|
| [covertovert](https://github.com/cengwins/covertovert) | Python | Covert channel framework |

**Note:** Framework for creating and detecting covert channels.

**Star count:** ⭐ 1

---

### covert-tube

| Tool | Language | Description |
|------|----------|-------------|
| [covert-tube](https://github.com/ricardojoserf/covert-tube) | Python | YouTube-based covert channel |

**Note:** Covert channel implementation using YouTube.

**Star count:** ⭐ 105

---

### Ectoplasm-Steganography

| Tool | Language | Description |
|------|----------|-------------|
| [Ectoplasm-Steganography](https://github.com/thomas-xin/Ectoplasm-Steganography) | Python | Metadata-based steganography |

**Note:** Tool for metadata-based image steganography.

**Star count:** —

---

### stegator

| Tool | Language | Description |
|------|----------|-------------|
| [stegator](https://github.com/1modm/stegator) | Python | Server-based steganography tool |

**Note:** Tool for steganography in server environments.

**Star count:** ⭐ 25

---

### PacketWhisper

| Tool | Language | Description |
|------|----------|-------------|
| [PacketWhisper](https://github.com/TryCatchHCF/PacketWhisper) | Python | Steganography in network packets |

**Note:** Transforms data into packet timing patterns for covert communication.

**Star count:** ⭐ 650

---

### Dissembling-Ferret

| Tool | Language | Description |
|------|----------|-------------|
| [Dissembling-Ferret](https://github.com/clayball/Dissembling-Ferret) | Python | Protocol steganography tool |

**Note:** Tool for steganography in network protocols.

**Star count:** ⭐ 12

---

### StegoAuth

| Tool | Language | Description |
|------|----------|-------------|
| [StegoAuth](https://github.com/LabunskyA/StegoAuth) | Python | Authentication protocol steganography |

**Note:** Proof-of-concept for steganography-based authentication.

**Star count:** ⭐ 4

---

### PyExfil

| Tool | Language | Description |
|------|----------|-------------|
| [PyExfil](https://github.com/ytisf/PyExfil) | Python | Data exfiltration via steganography |

**Note:** Multi-protocol data exfiltration tool using steganography.

**Star count:** ⭐ 806

---

### ICMPStegano

| Tool | Language | Description |
|------|----------|-------------|
| [ICMPStegano](https://github.com/pshanoop/ICMPStegano) | Python | ICMP steganography [archived] |

**Note:** ICMP-based steganography for data exfiltration.

**Star count:** ⭐ 4

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

## Steganography Detection

---

### StegExpose

| Tool | Language | Description |
|------|----------|-------------|
| [StegExpose](https://github.com/b3dk7/StegExpose) | Python | LSB steganalysis tool for detecting hidden data in images |

**Note:** Specialized in detecting LSB steganography in PNG and BMP images.

**Star count:** ⭐ 245

---

### StegSpy

| Tool | Language | Description |
|------|----------|-------------|
| [StegSpy](https://github.com/AbhiDhabhai/StegSpy) | Python | Detects steganography in images and audio files |

**Note:** Detects hidden data using statistical analysis.

**Star count:** ⭐ 87

---

### StegCracker

| Tool | Language | Description |
|------|----------|-------------|
| [StegCracker](https://github.com/Paradoxis/StegCracker) | Python | Steganography brute-force utility to uncover hidden data inside files |

**Note:** Cracks steganography passwords using wordlists.

**Star count:** ⭐ 584

---

### Stegbreak

| Tool | Language | Description |
|------|----------|-------------|
| [Stegbreak](https://github.com/c0r3dump3d/stegbreak) | Python | Brute-force steganography password cracker |

**Note:** Uses dictionary attacks against steganography tools.

**Star count:** ⭐ 112

---

### StegVerifier

| Tool | Language | Description |
|------|----------|-------------|
| [StegVerifier](https://github.com/aseering/StegVerifier) | Python | Verifies steganography presence in media files |

**Note:** Multi-format steganography detection utility.

**Star count:** ⭐ 43

---

### foremost

| Tool | Language | Description |
|------|----------|-------------|
| [foremost](https://github.com/korczis/foremost) | C | File carving tool for extracting hidden files from images |

**Note:** Originally by the US Air Force. Extracts hidden files from JPEG, PNG, GIF, and other image formats.

**Star count:** ⭐ 412

---

### binwalk

| Tool | Language | Description |
|------|----------|-------------|
| [binwalk](https://github.com/ReFirmLabs/binwalk) | Python | Firmware analysis tool for finding embedded files and code |

**Note:** Useful for analyzing binary images to find hidden data, steganographic content, and embedded files.

**Star count:** ⭐ 4.6k

---

### The Sleuth Kit

| Tool | Language | Description |
|------|----------|-------------|
| [The Sleuth Kit](https://github.com/sleuthkit/sleuthkit) | C | Forensic toolkit for filesystem analysis and data recovery |

**Note:** Collection of command-line tools for digital forensics. Analyzes disk images for hidden data and deleted files.

**Star count:** ⭐ 2.3k

---

### Autopsy

| Tool | Language | Description |
|------|----------|-------------|
| [Autopsy](https://github.com/sleuthkit/autopsy) | Java | GUI frontend for The Sleuth Kit - digital forensics platform |

**Note:** Graphical interface for disk forensics. Supports steganography detection through file analysis.

**Star count:** ⭐ 1.6k

---

### bulk_extractor

| Tool | Language | Description |
|------|----------|-------------|
| [bulk_extractor](https://github.com/simsong/bulk_extractor) | C++ | Fast forensic tool for extracting features from disk images |

**Note:** Scans disk images for hidden data, emails, URLs, and steganographic content.

**Star count:** ⭐ 412

---

### dc3dd

| Tool | Language | Description |
|------|----------|-------------|
| [dc3dd](https://github.com/cfadams/dc3dd) | C | Enhanced version of dd for forensics |

**Note:** Forensic disk imaging tool with hashing and logging.

**Star count:** ⭐ 89

---

## Blind Steganalysis

---

### StegExpose

| Tool | Language | Description |
|------|----------|-------------|
| [StegExpose](https://github.com/b3dk7/StegExpose) | Python | Universal blind steganalysis detection |

**Note:** Generic steganalysis tool that detects hidden data without knowing the embedding method.

**Star count:** ⭐ 67

---

### steganalysis-ensemble

| Tool | Language | Description |
|------|----------|-------------|
| [steganalysis-ensemble](https://github.com/voidFP/steganalysis-ensemble) | Python | Ensemble classifier for steganalysis |

**Note:** Feature-based ensemble steganalysis using rich models.

**Star count:** ⭐ 45

---

### DCTR-feature-extraction

| Tool | Language | Description |
|------|----------|-------------|
| [DCTR-feature-extraction](https://github.com/abb3700/DCTR-feature-extraction) | Python | DCTR (Discrete Cosine Transform Residual) features |

**Note:** JPEG steganalysis using DCTR features from SRM family.

**Star count:** ⭐ 23

---

### SRM-feature-extraction

| Tool | Language | Description |
|------|----------|-------------|
| [SRM-feature-extraction](https://github.com/abb3700/SRM-feature-extraction) | Python | SRM (Spatial Rich Model) features |

**Note:** Rich model features for spatial steganalysis.

**Star count:** ⭐ 31

---

### steganalysis-CNN

| Tool | Language | Description |
|------|----------|-------------|
| [steganalysis-CNN](https://github.com/tanshuai0211/steganalysis-CNN) | Python | CNN-based universal steganalysis |

**Note:** Generic CNN architecture for steganalysis across multiple algorithms.

**Star count:** ⭐ 78

---

### steganalysis-toolkit

| Tool | Language | Description |
|------|----------|-------------|
| [steganalysis-toolkit](https://github.com/truongkma/steganalysis-toolkit) | Python | Collection of steganalysis tools |

**Note:** Multiple classical steganalysis methods in one toolkit.

**Star count:** ⭐ 89

---

### SPAM-feature-extraction

| Tool | Language | Description |
|------|----------|-------------|
| [SPAM-feature-extraction](https://github.com/abb3700/SPAM-feature-extraction) | Python | SPAM (Subtractive Pixel Adjacency Matrix) features |

**Note:** Second-order SPAM features for steganalysis.

**Star count:** ⭐ 18

---

### stegano-collector

| Tool | Language | Description |
|------|----------|-------------|
| [stegano-collector](https://github.com/nowotny/stegano-collector) | Python | Multi-method steganalysis collector |

**Note:** Combines multiple detection approaches for blind detection.

**Star count:** ⭐ 34

---

### stegalyzer

| Tool | Language | Description |
|------|----------|-------------|
| [stegalyzer](https://github.com/kn42io/stegalyzer) | Python | Blind steganalysis for detecting hidden content |

**Note:** Generic blind steganalysis tool for multiple formats.

**Star count:** ⭐ 28

---

### stegwatch

| Tool | Language | Description |
|------|----------|-------------|
| [stegwatch](https://github.com/nowotny/stegwatch) | Python | Real-time steganalysis monitoring |

**Note:** Monitors files for steganographic content.

**Star count:** ⭐ 19

---

### stegdetect-classic

| Tool | Language | Description |
|------|----------|-------------|
| [stegdetect-classic](https://github.com/abeluck/stegdetect) | C | Classic stegdetect with enhanced detection |

**Note:** Enhanced version of the original stegdetect tool.

**Star count:** ⭐ 156

---

### StegInspect

| Tool | Language | Description |
|------|----------|-------------|
| [StegInspect](https://github.com/nowotny/StegInspect) | Python | Multi-algorithm steganalysis inspector |

**Note:** Analyzes images for multiple steganography algorithms.

**Star count:** ⭐ 22

---

### steganalysis-CLI

| Tool | Language | Description |
|------|----------|-------------|
| [steganalysis-CLI](https://github.com/nowotny/steganalysis-CLI) | Python | Command-line steganalysis tool |

**Note:** CLI interface for various steganalysis methods.

**Star count:** ⭐ 15

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

### AperiSolve

| Tool | Language | Description |
|------|----------|-------------|
| [AperiSolve](https://github.com/Zeecka/AperiSolve) | Python | Steganalysis web platform |

**Note:** Online steganalysis platform with multiple detection methods. Active CTF tool.

**Star count:** ⭐ 817

---

### Stegano

| Tool | Language | Description |
|------|----------|-------------|
| [Stegano](https://github.com/cedricbonhomme/Stegano) | Python | Pure Python steganography module |

**Note:** Pure Python steganography library with LSB and other methods.

**Star count:** ⭐ 589

---

### StegOnline

| Tool | Language | Description |
|------|----------|-------------|
| [StegOnline](https://github.com/Ge0rg3/StegOnline) | TypeScript | Web-based steganalysis tool |

**Note:** Open-source port of StegSolve with additional features. Browser-based.

**Star count:** ⭐ 377

---

### steghide (Stegseek)

| Tool | Language | Description |
|------|----------|-------------|
| [stegseek](https://github.com/RickdeJager/stegseek) | C++ | World's fastest steghide cracker |

**Note:** Cracks steghide passwords at millions per second. Fast steganalysis tool.

**Star count:** ⭐ 1.3k

---

### cloacked-pixel

| Tool | Language | Description |
|------|----------|-------------|
| [cloacked-pixel](https://github.com/livz/cloacked-pixel) | Python | LSB steganography with AES-256 encryption |

**Note:** Secure steganography tool with encrypted payload in PNG images.

**Star count:** ⭐ 631

---

### StegoForge

| Tool | Language | Description |
|------|----------|-------------|
| [StegoForge](https://github.com/Nour833/StegoForge) | Python | Multi-format steganography + detection toolkit |

**Note:** Encodes and detects hidden data across 5 media types in one tool.

**Star count:** ⭐ 337

---

### LSB-Steganography

| Tool | Language | Description |
|------|----------|-------------|
| [LSB-Steganography](https://github.com/RobinDavid/LSB-Steganography) | Python | Classic LSB steganography in images [archived] |

**Note:** Simple and well-documented LSB steganography implementation.

**Star count:** ⭐ 953

---

### Matroschka

| Tool | Language | Description |
|------|----------|-------------|
| [Matroschka](https://github.com/fbngrm/Matroschka) | Python | LSB steganography with multiple carrier images |

**Note:** Spreads payload across multiple images for increased capacity.

**Star count:** ⭐ 438

---

### Chaya

| Tool | Language | Description |
|------|----------|-------------|
| [Chaya](https://github.com/xerohackcom/Chaya) | Python | Image steganography tool with GUI |

**Note:** User-friendly steganography tool for hiding data in images.

**Star count:** ⭐ 132

---

### f5-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [f5-steganography](https://github.com/jackfengji/f5-steganography) | Python | F5 algorithm implementation |

**Note:** Implementation of F5 JPEG steganography algorithm.

**Star count:** ⭐ 50

---

### HiddenWave

| Tool | Language | Description |
|------|----------|-------------|
| [HiddenWave](https://github.com/techchipnet/HiddenWave) | Python | Audio steganography for hiding messages in audio |

**Note:** Hides messages in audio files using various techniques.

**Star count:** ⭐ 184

---

### Audio-Steganography-CLI

| Tool | Language | Description |
|------|----------|-------------|
| [Audio-Steganography-CLI](https://github.com/sniperline047/Audio-Steganography-CLI) | Python | Command-line audio steganography |

**Note:** Simple CLI tool for audio steganography.

**Star count:** ⭐ 22

---

### stegpy

| Tool | Language | Description |
|------|----------|-------------|
| [stegpy](https://github.com/izcoser/stegpy) | Python | Steganography for images and audio |

**Note:** Multi-format steganography supporting images and WAV audio.

**Star count:** ⭐ 131

---

### PixInWav

| Tool | Language | Description |
|------|----------|-------------|
| [PixInWav](https://github.com/margaritageleta/PixInWav) | PyTorch | Hide images in audio using deep learning |

**Note:** Neural steganography for embedding images in audio signals.

**Star count:** ⭐ 28

---

### PixInWav2

| Tool | Language | Description |
|------|----------|-------------|
| [PixInWav2](https://github.com/migamic/PixInWav2) | PyTorch | Improved version of PixInWav |

**Note:** Enhanced neural audio steganography for hiding images.

**Star count:** ⭐ 24

---

### steganography-js

| Tool | Language | Description |
|------|----------|-------------|
| [steganography-js](https://github.com/thavixt/steganography-js) | JavaScript | Browser-based steganography |

**Note:** JavaScript library for web-based image steganography.

**Star count:** ⭐ 12

---

### Steganography-Online

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-Online](https://github.com/StuffJackMakes/Steganography-Online) | JavaScript | Web-based steganography tool |

**Note:** Online steganography tool running in the browser.

**Star count:** ⭐ 4

---

### LSB-Steganography-Python

| Tool | Language | Description |
|------|----------|-------------|
| [LSB-Steganography-Python](https://github.com/int-main/LSB-Steganography-Python) | Python | LSB steganography with GUI |

**Note:** Simple LSB steganography with graphical interface.

**Star count:** ⭐ 13

---

### image-steganography (goelashwin36)

| Tool | Language | Description |
|------|----------|-------------|
| [image-steganography](https://github.com/goelashwin36/image-steganography) | Python | Image steganography GUI tool |

**Note:** GUI-based image steganography tool.

**Star count:** ⭐ 10

---

### emimg-GUI

| Tool | Language | Description |
|------|----------|-------------|
| [emimg-GUI](https://github.com/bysiber/emimg-GUI) | Python | Image steganography desktop GUI |

**Note:** Desktop application for image steganography.

**Star count:** ⭐ 7

---

### stegosaurus

| Tool | Language | Description |
|------|----------|-------------|
| [stegosaurus](https://github.com/lemonyte/stegosaurus) | Python | Image steganography with GUI |

**Note:** Modern Python steganography tool with GUI.

**Star count:** —

---

### steganography (gunjannandy)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/gunjannandy/steganography) | Python | LSB steganography with encoding/decoding |

**Note:** Simple Python steganography for hiding messages in images.

**Star count:** ⭐ 61

---

### zwsp-steg-py

| Tool | Language | Description |
|------|----------|-------------|
| [zwsp-steg-py](https://github.com/enodari/zwsp-steg-py) | Python | Zero-width character steganography |

**Note:** Python implementation of zero-width character steganography.

**Star count:** ⭐ 39

---

### steganography-png-decoder

| Tool | Language | Description |
|------|----------|-------------|
| [steganography-png-decoder](https://github.com/s373r/steganography-png-decoder) | Python | PNG steganography decoder |

**Note:** Tool specifically for decoding PNG steganography.

**Star count:** ⭐ 17

---

### steganography (atbuy)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/atbuy/steganography) | Python | Basic steganography encoder/decoder |

**Note:** Simple steganography tool for encoding and decoding messages.

**Star count:** ⭐ 6

---

### StegsnowBruteForcer

| Tool | Language | Description |
|------|----------|-------------|
| [StegsnowBruteForcer](https://github.com/0p5cur/StegsnowBruteForcer) | Python | Brute force tool for SNOW whitespace steganography |

**Note:** Cracks passwords for SNOW steganography tool.

**Star count:** ⭐ 15

---

### Steganography (Sanjipan)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/Sanjipan/Steganography) | Python | Multi-format steganography for images, video, audio, text |

**Note:** Comprehensive steganography toolkit supporting multiple media types.

**Star count:** ⭐ 26

---

### neural-imaging

| Tool | Language | Description |
|------|----------|-------------|
| [neural-imaging](https://github.com/pkorus/neural-imaging) | Python | Research on JPEG compression and neural imaging |

**Note:** Academic framework for neural imaging and JPEG steganography research.

**Star count:** ⭐ 163

---

### sigBits

| Tool | Language | Description |
|------|----------|-------------|
| [sigBits](https://github.com/Pulho/sigBits) | Python | LSB steganography for JPEG, PNG, BMP |

**Note:** Simple but effective LSB steganography for multiple image formats.

**Star count:** ⭐ 40

---

### Universal-Deep-Hiding

| Tool | Language | Description |
|------|----------|-------------|
| [Universal-Deep-Hiding](https://github.com/ChaoningZhang/Universal-Deep-Hiding) | PyTorch | Universal deep learning steganography framework |

**Note:** Research framework for universal neural steganography.

**Star count:** ⭐ 123

---

### StegaPy

| Tool | Language | Description |
|------|----------|-------------|
| [StegaPy](https://github.com/MearaY/StegaPy) | Python | Python steganography library |

**Note:** Pure Python steganography library for hiding data in images.

**Star count:** ⭐ 328

---

### The-A-Files

| Tool | Language | Description |
|------|----------|-------------|
| [The-A-Files](https://github.com/pawel-kaczmarek/The-A-Files) | Python | Audio steganography and watermarking |

**Note:** Research on audio information hiding and watermarking.

**Star count:** ⭐ 27

---

### invisible-watermark-tool

| Tool | Language | Description |
|------|----------|-------------|
| [invisible-watermark-tool](https://github.com/nellx-io/invisible-watermark-tool) | Python | Invisible watermark with AES + SHA-256 |

**Note:** Tool for adding invisible watermarks with encryption.

**Star count:** ⭐ 2

---

### steganography (subc)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/subc/steganography) | Python | Multi-format steganography library |

**Note:** Python library for steganography in images and other media.

**Star count:** ⭐ 46

---

### steganos

| Tool | Language | Description |
|------|----------|-------------|
| [steganos](https://github.com/fastforwardlabs/steganos) | Python | Early Python steganography library |

**Note:** One of the early Python steganography libraries.

**Star count:** ⭐ 84

---

### LSB_Steganography

| Tool | Language | Description |
|------|----------|-------------|
| [LSB_Steganography](https://github.com/rahulsinghinfosec/LSB_Steganography) | Python | LSB steganography implementation |

**Note:** Simple LSB steganography tool.

**Star count:** ⭐ 12

---

### steg (surg0r)

| Tool | Language | Description |
|------|----------|-------------|
| [steg](https://github.com/surg0r/steg) | Python | Simple steganography tool [archived] |

**Note:** Basic steganography tool for hiding data in images.

**Star count:** ⭐ 10

---

### fractal-image-steganography

| Tool | Language | Description |
|------|----------|-------------|
| [fractal-image-steganography](https://github.com/supremepanda/fractal-image-steganography) | Python | Fractal-based image steganography |

**Note:** Uses fractal algorithms for image steganography.

**Star count:** ⭐ 3

---

### LSB_Steganography (omriher)

| Tool | Language | Description |
|------|----------|-------------|
| [LSB_Steganography](https://github.com/omriher/LSB_Steganography) | Python | LSB steganography implementation |

**Note:** Simple LSB steganography tool.

**Star count:** ⭐ 15

---

### lsb (marselester)

| Tool | Language | Description |
|------|----------|-------------|
| [lsb](https://github.com/marselester/lsb) | Python | LSB steganography in BMP images [archived] |

**Note:** Early LSB steganography tool for BMP images.

**Star count:** ⭐ 7

---

### covertutils

| Tool | Language | Description |
|------|----------|-------------|
| [covertutils](https://github.com/operatorequals/covertutils) | Python | Python framework for building covert channels |

**Note:** Comprehensive framework for creating covert communication channels.

**Star count:** ⭐ 435

---

### stegsleuth

| Tool | Language | Description |
|------|----------|-------------|
| [stegsleuth](https://github.com/4osp3l/stegsleuth) | Python | Steganalysis framework |

**Note:** Framework for detecting hidden data in various media.

**Star count:** ⭐ 14

---

### ch3r0

| Tool | Language | Description |
|------|----------|-------------|
| [ch3r0](https://github.com/tnt-wolve/ch3r0) | Python | Steganography detection tool |

**Note:** Tool for detecting steganography in images.

**Star count:** ⭐ 317

---

### ReconEXIF

| Tool | Language | Description |
|------|----------|-------------|
| [ReconEXIF](https://github.com/spider863644/ReconEXIF) | Python | EXIF metadata analysis tool |

**Note:** Tool for analyzing EXIF metadata for forensics.

**Star count:** ⭐ 9

---

### Steganography-Software

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-Software](https://github.com/Shlok-crypto/Steganography-Software) | Python | Binary steganography tool |

**Note:** Software for steganography using RGB values.

**Star count:** ⭐ 29

---

### binary_steganography

| Tool | Language | Description |
|------|----------|-------------|
| [binary_steganography](https://github.com/dinex-dev/binary_steganography) | Python | Binary file steganography |

**Note:** Tool for steganography in binary files.

**Star count:** ⭐ 2

---

### node-stego

| Tool | Language | Description |
|------|----------|-------------|
| [node-stego](https://github.com/uberscientist/node-stego) | JavaScript | Node.js steganography library [archived] |

**Note:** Early Node.js library for steganography.

**Star count:** ⭐ 5

---

### photochat

| Tool | Language | Description |
|------|----------|-------------|
| [photochat](https://github.com/tianhaoz95/photochat) | Swift/Kotlin | Photo messaging with steganography |

**Note:** Mobile app for hidden messaging in photos.

**Star count:** ⭐ 43

---

### PDFStego

| Tool | Language | Description |
|------|----------|-------------|
| [PDFStego](https://github.com/aagallag/PDFStego) | C | PDF steganography tool |

**Note:** Tool for hiding data in PDF files.

**Star count:** —

---

### ExeSteganography

| Tool | Language | Description |
|------|----------|-------------|
| [ExeSteganography](https://github.com/god233012yamil/ExeSteganography) | Python | EXE file steganography |

**Note:** Tool for steganography in executable files.

**Star count:** ⭐ 17

---

### exe2png

| Tool | Language | Description |
|------|----------|-------------|
| [exe2png](https://github.com/donno2048/exe2png) | Python | Convert EXE to PNG steganography |

**Note:** Embeds executable files into PNG images.

**Star count:** ⭐ 7

---

### stegify-mobile

| Tool | Language | Description |
|------|----------|-------------|
| [stegify-mobile](https://github.com/DimitarPetrov/stegify-mobile) | Dart | Mobile steganography app |

**Note:** Mobile implementation of stegify for Flutter/Dart.

**Star count:** ⭐ 8

---

### stegbrute

| Tool | Language | Description |
|------|----------|-------------|
| [stegbrute](https://github.com/R4yGM/stegbrute) | Rust | Docker-based steganography brute forcer |

**Note:** Fast steganography brute forcing tool in Rust.

**Star count:** ⭐ 244

---

### stego-toolkit-nix

| Tool | Language | Description |
|------|----------|-------------|
| [stego-toolkit-nix](https://github.com/qrxnz/stego-toolkit-nix) | Nix | NixOS steganography toolkit |

**Note:** Nix package for steganography tools.

**Star count:** —

---

### euli_treasure_hunt

| Tool | Language | Description |
|------|----------|-------------|
| [euli_treasure_hunt](https://github.com/ruppde/euli_treasure_hunt) | Python | Steganography puzzle game |

**Note:** Treasure hunt game using steganography puzzles.

**Star count:** ⭐ 44

---

### Cipher-Sphere

| Tool | Language | Description |
|------|----------|-------------|
| [Cipher-Sphere](https://github.com/nouralmulhem/Cipher-Sphere) | Python | Security and steganography learning platform |

**Note:** Educational platform for learning cryptography and steganography.

**Star count:** —

---

### steganography (teovoinea)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/teovoinea/steganography) | Rust | Rust steganography library |

**Note:** Rust library for image steganography.

**Star count:** ⭐ 103

---

### stegify-flutter-plugin

| Tool | Language | Description |
|------|----------|-------------|
| [stegify-flutter-plugin](https://github.com/DimitarPetrov/stegify-flutter-plugin) | Dart | Flutter plugin for stegify |

**Note:** Flutter plugin for mobile steganography.

**Star count:** ⭐ 10

---

### NeuralSteganography

| Tool | Language | Description |
|------|----------|-------------|
| [NeuralSteganography](https://github.com/harvardnlp/NeuralSteganography) | Python | Harvard NLP neural steganography |

**Note:** Neural steganography research from Harvard NLP.

**Star count:** ⭐ 212

---

### PyTorch-Deep-Image-Steganography

| Tool | Language | Description |
|------|----------|-------------|
| [PyTorch-Deep-Image-Steganography](https://github.com/arnoweng/PyTorch-Deep-Image-Steganography) | PyTorch | Deep image steganography with U-Net |

**Note:** Implementation of deep learning image steganography.

**Star count:** ⭐ 139

---

### VHiddenNet

| Tool | Language | Description |
|------|----------|-------------|
| [VHiddenNet](https://github.com/YoursIvan/VHiddenNet) | Python | Social network steganography |

**Note:** Steganography tool for social networks.

**Star count:** ⭐ 9

---

### stegoTool (jonsalchichonnn)

| Tool | Language | Description |
|------|----------|-------------|
| [stegoTool](https://github.com/jonsalchichonnn/stegoTool) | Python | General steganography tool |

**Note:** Multi-purpose steganography tool.

**Star count:** ⭐ 3

---

### steganography (browningjp)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/browningjp/steganography) | Python | OpenCV-based steganography [archived] |

**Note:** OpenCV-based image steganography tool.

**Star count:** ⭐ 12

---

### Text-steganography (sakship31)

| Tool | Language | Description |
|------|----------|-------------|
| [Text-steganography](https://github.com/sakship31/Text-steganography) | Python | Flask-based text steganography web app |

**Note:** Web application for text steganography.

**Star count:** ⭐ 29

---

### hackingtool (Z4nzu)

| Tool | Language | Description |
|------|----------|-------------|
| [hackingtool](https://github.com/Z4nzu/hackingtool) | Python | All-in-one hacking tool with steganography modules (2026) |

**Note:** Multi-purpose hacking framework with steganography capabilities.

**Star count:** ⭐ 73.9k

---

### ST3GG (elder-plinius)

| Tool | Language | Description |
|------|----------|-------------|
| [ST3GG](https://github.com/elder-plinius/ST3GG) | HTML | All-in-one steganography suite (2026) |

**Note:** Comprehensive steganography toolkit for various techniques.

**Star count:** ⭐ 1.4k

---

### stegify (DimitarPetrov)

| Tool | Language | Description |
|------|----------|-------------|
| [stegify](https://github.com/DimitarPetrov/stegify) | Go | Go tool for LSB steganography, capable of hiding any file within an image (2023) |

**Note:** LSB steganography tool written in Go.

**Star count:** ⭐ 1.3k

---

### StegCracker (Paradoxis)

| Tool | Language | Description |
|------|----------|-------------|
| [StegCracker](https://github.com/Paradoxis/StegCracker) | Python | Steganography brute-force utility to uncover hidden data inside files (2020) |

**Note:** Brute-force tool for cracking steganography passwords.

**Star count:** ⭐ 594

---

### covertchannels-steganography (mindcrypt)

| Tool | Language | Description |
|------|----------|-------------|
| [covertchannels-steganography](https://github.com/mindcrypt/covertchannels-steganography) | Python | Covert channels and steganography research toolkit (2022) |

**Note:** Research toolkit for covert channels and steganography.

**Star count:** ⭐ 103

---

### Tomato (user1342)

| Tool | Language | Description |
|------|----------|-------------|
| [Tomato](https://github.com/user1342/Tomato) | Python | Steganography tool with multiple techniques (2024) |

**Note:** Multi-technique steganography tool.

**Star count:** ⭐ 94

---

### chess-steg (jes)

| Tool | Language | Description |
|------|----------|-------------|
| [chess-steg](https://github.com/jes/chess-steg) | Python | Chess-based steganography using move notation (2021) |

**Note:** Unique steganography using chess game moves to encode messages.

**Star count:** ⭐ 91

---

### PolyZip (InfoSecREDD)

| Tool | Language | Description |
|------|----------|-------------|
| [PolyZip](https://github.com/InfoSecREDD/PolyZip) | Python | Steganography tool for hiding data in files (2025) |

**Note:** Data exfiltration tool using steganography.

**Star count:** ⭐ 89

---

### Bramble (marcrowProject)

| Tool | Language | Description |
|------|----------|-------------|
| [Bramble](https://github.com/marcrowProject/Bramble) | Python | Steganography tool for image processing (2020) |

**Note:** Image steganography using various techniques.

**Star count:** ⭐ 84

---

### Final-year-Project-steganography (Vatshayan)

| Tool | Language | Description |
|------|----------|-------------|
| [Final-year-Project-steganography](https://github.com/Vatshayan/Final-year-Project-steganography) | Python | Academic steganography project (2022) |

**Note:** Educational steganography implementation.

**Star count:** ⭐ 82

---

### ultrasonic (ruvnet)

| Tool | Language | Description |
|------|----------|-------------|
| [ultrasonic](https://github.com/ruvnet/ultrasonic) | Python | Ultrasonic steganography for data exfiltration (2025) |

**Note:** Steganography using ultrasonic sound frequencies.

**Star count:** ⭐ 83

---

### NativePayload_Image (DamonMohammadbagher)

| Tool | Language | Description |
|------|----------|-------------|
| [NativePayload_Image](https://github.com/DamonMohammadbagher/NativePayload_Image) | PowerShell | Image-based payload delivery via steganography (2023) |

**Note:** Steganography for red team operations.

**Star count:** ⭐ 81

---

### steganography (raffg)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/raffg/steganography) | Python | General-purpose steganography library (2018) |

**Note:** Python steganography library.

**Star count:** ⭐ 36

---

### Image-Stegano (varunon9)

| Tool | Language | Description |
|------|----------|-------------|
| [Image-Stegano](https://github.com/varunon9/Image-Stegano) | JavaScript | Image steganography in JavaScript (2017) |

**Note:** Browser-based image steganography.

**Star count:** ⭐ 36

---

### markovTextStego (hmoraldo)

| Tool | Language | Description |
|------|----------|-------------|
| [markovTextStego](https://github.com/hmoraldo/markovTextStego) | Python | Text steganography using Markov chains (2014) |

**Note:** Linguistic steganography using Markov models.

**Star count:** ⭐ 36

---

### js-steg (owencm)

| Tool | Language | Description |
|------|----------|-------------|
| [js-steg](https://github.com/owencm/js-steg) | JavaScript | JavaScript steganography library (2014) |

**Note:** Client-side steganography for web applications.

**Star count:** ⭐ 36

---

### Linguistic-Steganography-and-Steganalysis (YangzlTHU)

| Tool | Language | Description |
|------|----------|-------------|
| [Linguistic-Steganography-and-Steganalysis](https://github.com/YangzlTHU/Linguistic-Steganography-and-Steganalysis) | Python | Research on linguistic steganography and steganalysis (2022) |

**Note:** Academic research toolkit for linguistic steganography.

**Star count:** ⭐ 35

---

### Learning-Image-Steganography (TracyCuiq)

| Tool | Language | Description |
|------|----------|-------------|
| [Learning-Image-Steganography](https://github.com/TracyCuiq/Learning-Image-Steganography) | Python | Educational image steganography codebase (2024) |

**Note:** Learning resource for image steganography techniques.

**Star count:** ⭐ 35

---

### StegFormer (aoli-gei)

| Tool | Language | Description |
|------|----------|-------------|
| [StegFormer](https://github.com/aoli-gei/StegFormer) | Python | Transformer-based steganography (2024) |

**Note:** Deep learning steganography using transformer architecture.

**Star count:** ⭐ 35

---

### timeshifter (anfractuosity)

| Tool | Language | Description |
|------|----------|-------------|
| [timeshifter](https://github.com/anfractuosity/timeshifter) | Python | Temporal steganography tool (2022) |

**Note:** Time-based steganography techniques.

**Star count:** ⭐ 23

---

### Cs-FNNS (albblgb)

| Tool | Language | Description |
|------|----------|-------------|
| [Cs-FNNS](https://github.com/albblgb/Cs-FNNS) | C# | .NET steganography library (2024) |

**Note:** C# steganography implementation.

**Star count:** ⭐ 23

---

### stegjs (andmev)

| Tool | Language | Description |
|------|----------|-------------|
| [stegjs](https://github.com/andmev/stegjs) | JavaScript | JavaScript steganography library (2024) |

**Note:** Browser-based steganography in JavaScript.

**Star count:** ⭐ 23

---

### nanoboard (Karasiq)

| Tool | Language | Description |
|------|----------|-------------|
| [nanoboard](https://github.com/Karasiq/nanoboard) | Scala | Steganography toolkit in Scala (2020) |

**Note:** Multi-format steganography in Scala.

**Star count:** ⭐ 23

---

### Steganography- (BecauseY)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-](https://github.com/BecauseY/Steganography-) | Python | Steganography tool (2023) |

**Note:** General steganography implementation.

**Star count:** ⭐ 21

---

### secretbook (owencm)

| Tool | Language | Description |
|------|----------|-------------|
| [secretbook](https://github.com/owencm/secretbook) | JavaScript | Steganography for images (2018) |

**Note:** Image steganography in JavaScript.

**Star count:** ⭐ 21

---

### Explosive-Steganography (XlogicX)

| Tool | Language | Description |
|------|----------|-------------|
| [Explosive-Steganography](https://github.com/XlogicX/Explosive-Steganography) | Python | CTF steganography challenges (2014) |

**Note:** Educational steganography for CTF practice.

**Star count:** ⭐ 21

---

### mr-hyde (rafael-santiago)

| Tool | Language | Description |
|------|----------|-------------|
| [mr-hyde](https://github.com/rafael-santiago/mr-hyde) | Rust | Steganography in Rust (2020) |

**Note:** Steganography tool written in Rust.

**Star count:** ⭐ 15

---

### advsteg (jhayes14)

| Tool | Language | Description |
|------|----------|-------------|
| [advsteg](https://github.com/jhayes14/advsteg) | Python | Advanced steganography techniques (2018) |

**Note:** Advanced steganography implementation.

**Star count:** ⭐ 15

---

### image-steganography (subedigaurav)

| Tool | Language | Description |
|------|----------|-------------|
| [image-steganography](https://github.com/subedigaurav/image-steganography) | Python | Image steganography tool (2026) |

**Note:** Simple image steganography.

**Star count:** ⭐ 15

---

### PictureCrypt (waleko)

| Tool | Language | Description |
|------|----------|-------------|
| [PictureCrypt](https://github.com/waleko/PictureCrypt) | Python | Picture-based encryption and steganography (2022) |

**Note:** Steganography with encryption.

**Star count:** ⭐ 15

---

### cryptographic_methods (podkidyshev)

| Tool | Language | Description |
|------|----------|-------------|
| [cryptographic_methods](https://github.com/podkidyshev/cryptographic_methods) | Python | Cryptography and steganography methods (2018) |

**Note:** Educational cryptography and steganography.

**Star count:** ⭐ 15

---

### stegasawus (rokkuran)

| Tool | Language | Description |
|------|----------|-------------|
| [stegasawus](https://github.com/rokkuran/stegasawus) | Python | Steganography tool (2017) |

**Note:** Python steganography utility.

**Star count:** ⭐ 15

---

### Steganography (vvHacker007)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/vvHacker007/Steganography) | Python | Python steganography tool (2020) |

**Note:** General steganography implementation.

**Star count:** ⭐ 15

---

### stega (sebleier)

| Tool | Language | Description |
|------|----------|-------------|
| [stega](https://github.com/sebleier/stega) | Python | Early Python steganography (2011) |

**Note:** Early steganography library for Python.

**Star count:** ⭐ 15

---

### ascii-to-midi (1j01)

| Tool | Language | Description |
|------|----------|-------------|
| [ascii-to-midi](https://github.com/1j01/ascii-to-midi) | JavaScript | ASCII to MIDI steganography (2022) |

**Note:** Text-to-audio steganography using MIDI.

**Star count:** ⭐ 12

---

### Pool2020 (PoCInnovation)

| Tool | Language | Description |
|------|----------|-------------|
| [Pool2020](https://github.com/PoCInnovation/Pool2020) | Python | Steganography research project (2020) |

**Note:** Research steganography techniques.

**Star count:** ⭐ 12

---

### Enigma (AleksaMCode)

| Tool | Language | Description |
|------|----------|-------------|
| [Enigma](https://github.com/AleksaMCode/Enigma) | Python | Cryptography and steganography tool (2024) |

**Note:** Combined crypto and steganography.

**Star count:** ⭐ 12

---

### F5Android (harlo)

| Tool | Language | Description |
|------|----------|-------------|
| [F5Android](https://github.com/harlo/F5Android) | Java | F5 steganography for Android (2018) |

**Note:** F5 algorithm implementation for Android.

**Star count:** ⭐ 11

---

### strogonoff (jbochi)

| Tool | Language | Description |
|------|----------|-------------|
| [strogonoff](https://github.com/jbochi/strogonoff) | Python | Early steganography tool (2011) |

**Note:** Early Python steganography implementation.

**Star count:** ⭐ 11

---

### Steganography-App (lukefire5156)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-App](https://github.com/lukefire5156/Steganography-App) | Python | GUI steganography application (2024) |

**Note:** Desktop steganography app.

**Star count:** ⭐ 11

---

### awesome-steganography (cristiancmoises)

| Tool | Language | Description |
|------|----------|-------------|
| [awesome-steganography](https://github.com/cristiancmoises/awesome-steganography) | Python | Steganography resources collection (2025) |

**Note:** Curated steganography resources.

**Star count:** ⭐ 11

---

### ImageSteganography (jokLiu)

| Tool | Language | Description |
|------|----------|-------------|
| [ImageSteganography](https://github.com/jokLiu/ImageSteganography) | C++ | C++ image steganography (2018) |

**Note:** C++ implementation of image steganography.

**Star count:** ⭐ 11

---

### Steganofy (mstaudt)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganofy](https://github.com/mstaudt/Steganofy) | Python | Audio steganography tool |

**Note:** Audio steganography implementation.

**Star count:** ⭐ 9

---

### NNSDB (DLAIResearch)

| Tool | Language | Description |
|------|----------|-------------|
| [NNSDB](https://github.com/DLAIResearch/NNSDB) | Python | Neural network steganography database |

**Note:** Research database for neural steganography.

**Star count:** ⭐ 9

---

### stegano (tm9k1)

| Tool | Language | Description |
|------|----------|-------------|
| [stegano](https://github.com/tm9k1/stegano) | Python | Python steganography library |

**Note:** Simple steganography in Python.

**Star count:** ⭐ 10

---

### StegX (a1baradi)

| Tool | Language | Description |
|------|----------|-------------|
| [StegX](https://github.com/a1baradi/StegX) | C++ | C++ steganography tool |

**Note:** C++ steganography implementation.

**Star count:** ⭐ 9

---

### esteganografia-python (parzibyte)

| Tool | Language | Description |
|------|----------|-------------|
| [esteganografia-python](https://github.com/parzibyte/esteganografia-python) | Python | Spanish steganography tutorial |

**Note:** Educational steganography in Spanish.

**Star count:** ⭐ 9

---

### steggy (aneeshverma04)

| Tool | Language | Description |
|------|----------|-------------|
| [steggy](https://github.com/aneeshverma04/steggy) | Python | Simple steganography tool |

**Note:** Easy-to-use steganography.

**Star count:** ⭐ 9

---

### Steganography (lakshmanaram)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/lakshmanaram/Steganography) | Python | Python steganography library |

**Note:** Basic steganography implementation.

**Star count:** ⭐ 9

---

### StegMed (vaniseth)

| Tool | Language | Description |
|------|----------|-------------|
| [StegMed](https://github.com/vaniseth/StegMed) | Python | Medical image steganography (2023) |

**Note:** Steganography for medical images.

**Star count:** ⭐ 8

---

### stelf (Theldus)

| Tool | Language | Description |
|------|----------|-------------|
| [stelf](https://github.com/Theldus/stelf) | C | C steganography library (2024) |

**Note:** C library for steganography.

**Star count:** ⭐ 8

---

### SteganoPNG-deprecated (Dola-Shuvi)

| Tool | Language | Description |
|------|----------|-------------|
| [SteganoPNG-deprecated](https://github.com/Dola-Shuvi/SteganoPNG-deprecated) | Python | PNG steganography tool (2026) |

**Note:** PNG steganography implementation.

**Star count:** ⭐ 8

---

### byte (therealOri)

| Tool | Language | Description |
|------|----------|-------------|
| [byte](https://github.com/therealOri/byte) | Python | Data hiding tool (2023) |

**Note:** Simple data hiding utility.

**Star count:** ⭐ 8

---

### mds20_stega (profrodai)

| Tool | Language | Description |
|------|----------|-------------|
| [mds20_stega](https://github.com/profrodai/mds20_stega) | Python | Academic steganography research (2020) |

**Note:** Research steganography implementation.

**Star count:** ⭐ 8

---

### BSF24-CTF (0x1o1)

| Tool | Language | Description |
|------|----------|-------------|
| [BSF24-CTF](https://github.com/0x1o1/BSF24-CTF) | Python | CTF steganography challenges (2024) |

**Note:** CTF practice challenges.

**Star count:** ⭐ 8

---

### LiquidSnow-archive (ocluse)

| Tool | Language | Description |
|------|----------|-------------|
| [LiquidSnow-archive](https://github.com/ocluse/LiquidSnow-archive) | Python | Steganography archive (2023) |

**Note:** Archived steganography project.

**Star count:** ⭐ 8

---

### mAshing (asimtarapathak)

| Tool | Language | Description |
|------|----------|-------------|
| [mAshing](https://github.com/asimtarapathak/mAshing) | Python | Image hashing steganography (2021) |

**Note:** Hash-based image steganography.

**Star count:** ⭐ 8

---

### codered-steganography (au5ton)

| Tool | Language | Description |
|------|----------|-------------|
| [codered-steganography](https://github.com/au5ton/codered-steganography) | Python | Code Red steganography research (2018) |

**Note:** Research steganography implementation.

**Star count:** ⭐ 6

---

### MnemonicSteganography (jakezeal)

| Tool | Language | Description |
|------|----------|-------------|
| [MnemonicSteganography](https://github.com/jakezeal/MnemonicSteganography) | Python | Mnemonic-based steganography (2018) |

**Note:** Memory-based steganography technique.

**Star count:** ⭐ 6

---

### stego (gzcharleszhang)

| Tool | Language | Description |
|------|----------|-------------|
| [stego](https://github.com/gzcharleszhang/stego) | Python | General steganography tool (2020) |

**Note:** Python steganography implementation.

**Star count:** ⭐ 6

---

### Steganography-Java-GUI (arunenigma)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-Java-GUI](https://github.com/arunenigma/Steganography-Java-GUI) | Java | GUI steganography in Java (2013) |

**Note:** Java GUI steganography application.

**Star count:** ⭐ 6

---

### LSB-Steganography-MATLAB (michaelhuntermoore)

| Tool | Language | Description |
|------|----------|-------------|
| [LSB-Steganography-MATLAB](https://github.com/michaelhuntermoore/LSB-Steganography-MATLAB) | MATLAB | LSB steganography in MATLAB (2019) |

**Note:** MATLAB implementation of LSB steganography.

**Star count:** ⭐ 6

---

### AAC_Qmdct_Steganography (LeeeLiu)

| Tool | Language | Description |
|------|----------|-------------|
| [AAC_Qmdct_Steganography](https://github.com/LeeeLiu/AAC_Qmdct_Steganography) | Python | AAC audio steganography (2020) |

**Note:** Audio steganography for AAC format.

**Star count:** ⭐ 6

---

### MelodySteg (brvinfvck)

| Tool | Language | Description |
|------|----------|-------------|
| [MelodySteg](https://github.com/brvinfvck/MelodySteg) | Python | Melody-based steganography (2026) |

**Note:** Audio steganography using melody.

**Star count:** ⭐ 6

---

### Steganography (D3fy-Crypto)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/D3fy-Crypto/Steganography) | Python | General steganography tool (2020) |

**Note:** Python steganography implementation.

**Star count:** ⭐ 5

---

### Steganography (mayanksingh2298)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/mayanksingh2298/Steganography) | Python | Image steganography (2018) |

**Note:** Simple image steganography.

**Star count:** ⭐ 5

---

### stegano (alexandru-dinu)

| Tool | Language | Description |
|------|----------|-------------|
| [stegano](https://github.com/alexandru-dinu/stegano) | Python | Python steganography library (2023) |

**Note:** Python steganography toolkit.

**Star count:** ⭐ 5

---

### LSB-Steganography (qrzbing)

| Tool | Language | Description |
|------|----------|-------------|
| [LSB-Steganography](https://github.com/qrzbing/LSB-Steganography) | Python | LSB steganography implementation (2017) |

**Note:** Classic LSB steganography in Python.

**Star count:** ⭐ 5

---

### stego (im-NL)

| Tool | Language | Description |
|------|----------|-------------|
| [stego](https://github.com/im-NL/stego) | Python | General steganography tool (2023) |

**Note:** Python steganography utility.

**Star count:** ⭐ 5

---

### crypto-steganography-img (mihirwagle)

| Tool | Language | Description |
|------|----------|-------------|
| [crypto-steganography-img](https://github.com/mihirwagle/crypto-steganography-img) | Python | Image steganography with encryption (2023) |

**Note:** Combined encryption and steganography.

**Star count:** ⭐ 5

---

### glitch-steganography-decode (max-mapper)

| Tool | Language | Description |
|------|----------|-------------|
| [glitch-steganography-decode](https://github.com/max-mapper/glitch-steganography-decode) | Python | Glitch art steganography (2014) |

**Note:** Steganography using glitch effects.

**Star count:** ⭐ 5

---

### Image-Steganography-hiding-text (VidhuNived)

| Tool | Language | Description |
|------|----------|-------------|
| [Image-Steganography-hiding-text](https://github.com/VidhuNived/Image-Steganography-hiding-text-inside-image-using-python) | Python | Text hiding in images (2018) |

**Note:** Simple text-in-image steganography.

**Star count:** ⭐ 5

---

### LStegB (x1mus)

| Tool | Language | Description |
|------|----------|-------------|
| [LStegB](https://github.com/x1mus/LStegB) | Python | LSB steganography tool (2025) |

**Note:** LSB steganography implementation.

**Star count:** ⭐ 5

---

### DEFCON22_HF_Steganography (pdogg)

| Tool | Language | Description |
|------|----------|-------------|
| [DEFCON22_HF_Steganography](https://github.com/pdogg/DEFCON22_HF_Steganography) | Python | DEFCON steganography talk (2014) |

**Note:** Conference presentation materials.

**Star count:** ⭐ 5

---

### Audio-Steganography-LSB (arooshiverma)

| Tool | Language | Description |
|------|----------|-------------|
| [Audio-Steganography-LSB](https://github.com/arooshiverma/Audio-Steganography-using-LSB-susbstitution) | Python | Audio LSB steganography (2021) |

**Note:** LSB audio steganography.

**Star count:** ⭐ 5

---

### Stegbook (lozarcher)

| Tool | Language | Description |
|------|----------|-------------|
| [Stegbook](https://github.com/lozarcher/Stegbook) | Python | Steganography for social media (2011) |

**Note:** Early social media steganography.

**Star count:** ⭐ 5

---

### purrcrypt (vxfemboy)

| Tool | Language | Description |
|------|----------|-------------|
| [purrcrypt](https://github.com/vxfemboy/purrcrypt) | Rust | Encode secrets as cat/dog sounds (2025) |

**Note:** Audio steganography in Rust.

**Star count:** ⭐ 610

---

### steg86 (woodruffw)

| Tool | Language | Description |
|------|----------|-------------|
| [steg86](https://github.com/woodruffw/steg86) | Rust | x86 steganography tool (2026) |

**Note:** Binary steganography for x86.

**Star count:** ⭐ 321

---

### stego (ajmwagar)

| Tool | Language | Description |
|------|----------|-------------|
| [stego](https://github.com/ajmwagar/stego) | Rust | Rust steganography CLI (2022) |

**Note:** Command-line steganography in Rust.

**Star count:** ⭐ 271

---

### ruci (jkshfanfbun)

| Tool | Language | Description |
|------|----------|-------------|
| [ruci](https://github.com/jkshfanfbun/ruci) | Rust | Rust steganography library (2025) |

**Note:** Steganography toolkit in Rust.

**Star count:** ⭐ 49

---

### steganography.js (petereigenschink)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography.js](https://github.com/petereigenschink/steganography.js) | JavaScript | Pure JS steganography library (2018) |

**Note:** Browser-based steganography.

**Star count:** ⭐ 373

---

### PixelJihad (oakes)

| Tool | Language | Description |
|------|----------|-------------|
| [PixelJihad](https://github.com/oakes/PixelJihad) | JavaScript | JavaScript image steganography (2015) |

**Note:** Early JS steganography tool.

**Star count:** ⭐ 312

---

### desudesutalk (desudesutalk)

| Tool | Language | Description |
|------|----------|-------------|
| [desudesutalk](https://github.com/desudesutalk/desudesutalk) | JavaScript | Forum steganography tool (2018) |

**Note:** Social platform steganography.

**Star count:** ⭐ 134

---

### PhotoFiremark (avestura)

| Tool | Language | Description |
|------|----------|-------------|
| [PhotoFiremark](https://github.com/avestura/PhotoFiremark) | C# | Image watermarking and steganography (2024) |

**Note:** .NET image watermarking tool.

**Star count:** ⭐ 172

---

### SteganograhyProject (JHurst97)

| Tool | Language | Description |
|------|----------|-------------|
| [SteganograhyProject](https://github.com/JHurst97/SteganograhyProject) | C# | C# steganography project (2020) |

**Note:** Educational C# steganography.

**Star count:** ⭐ 120

---

### PNG-Mask (AlphaDelta)

| Tool | Language | Description |
|------|----------|-------------|
| [PNG-Mask](https://github.com/AlphaDelta/PNG-Mask) | C# | PNG steganography in C# (2016) |

**Note:** C# PNG steganography.

**Star count:** ⭐ 30

---

### morpheUS (pyrou)

| Tool | Language | Description |
|------|----------|-------------|
| [morpheus](https://github.com/pyrou/morpheus) | PHP | PHP steganography library (2021) |

**Note:** PHP image steganography.

**Star count:** ⭐ 25

---

### SteganographyKit (picamator)

| Tool | Language | Description |
|------|----------|-------------|
| [SteganographyKit](https://github.com/picamator/SteganographyKit) | PHP | PHP steganography toolkit (2016) |

**Note:** PHP steganography library.

**Star count:** ⭐ 18

---

### Stega-in-PHP (JoppeDC)

| Tool | Language | Description |
|------|----------|-------------|
| [Stega-in-PHP](https://github.com/JoppeDC/Stega-in-PHP) | PHP | PHP steganography implementation (2018) |

**Note:** PHP steganography tutorial.

**Star count:** ⭐ 12

---

### steganografi-kriptografi (asokanato)

| Tool | Language | Description |
|------|----------|-------------|
| [steganografi-kriptografi](https://github.com/asokanato/steganografi-kriptografi) | PHP | PHP steganography and cryptography (2020) |

**Note:** Combined crypto and steganography.

**Star count:** ⭐ 10

---

### Steganography (SleepTheGod)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography](https://github.com/SleepTheGod/Steganography) | PHP | PHP steganography tool (2023) |

**Note:** PHP steganography utility.

**Star count:** ⭐ 10

---

### stegleak (Estella)

| Tool | Language | Description |
|------|----------|-------------|
| [stegleak](https://github.com/Estella/stegleak) | PHP | PHP steganalysis tool (2019) |

**Note:** PHP steganalysis utility.

**Star count:** ⭐ 10

---

### ZWSP-Tool (TwistAtom)

| Tool | Language | Description |
|------|----------|-------------|
| [ZWSP-Tool](https://github.com/TwistAtom/ZWSP-Tool) | Python | Zero-width character steganography (2020) |

**Note:** Zero-width space steganography tool.

**Star count:** ⭐ 24

---

### zero-width-steganography (lorossi)

| Tool | Language | Description |
|------|----------|-------------|
| [zero-width-steganography](https://github.com/lorossi/zero-width-steganography) | Python | Zero-width steganography library (2022) |

**Note:** Python zero-width steganography.

**Star count:** ⭐ 12

---

### zerosteg (jasonkimprojects)

| Tool | Language | Description |
|------|----------|-------------|
| [zerosteg](https://github.com/jasonkimprojects/zerosteg) | Python | Zero-width steganography (2019) |

**Note:** Simple zero-width steganography.

**Star count:** ⭐ 9

---

### Zero-Width-Characters (Endrem)

| Tool | Language | Description |
|------|----------|-------------|
| [Zero-Width-Characters](https://github.com/Endrem/Zero-Width-Characters) | Python | Zero-width character steganography (2021) |

**Note:** Zero-width character encoding.

**Star count:** ⭐ 8

---

### ZW-Steg (MayADevBe)

| Tool | Language | Description |
|------|----------|-------------|
| [ZW-Steg](https://github.com/MayADevBe/ZW-Steg) | Python | Zero-width steganography tool (2024) |

**Note:** Simple ZW steganography.

**Star count:** ⭐ 7

---

### img-stego (ktekeli)

| Tool | Language | Description |
|------|----------|-------------|
| [img-stego](https://github.com/ktekeli/img-stego) | Python | Image steganography tool (2024) |

**Note:** Python image steganography.

**Star count:** ⭐ 16

---

### iSteg (rafiibrahim8)

| Tool | Language | Description |
|------|----------|-------------|
| [iSteg](https://github.com/rafiibrahim8/iSteg) | Python | Image steganography GUI (2019) |

**Note:** Image steganography application.

**Star count:** ⭐ 14

---

### hstego (daniellerch)

| Tool | Language | Description |
|------|----------|-------------|
| [hstego](https://github.com/daniellerch/hstego) | C/Python | Hard-to-detect image steganography using S-UNIWARD/J-UNIWARD + STC |

**Note:** Uses S-UNIWARD (spatial) and J-UNIWARD (JPEG) with Syndrome Trellis Codes. Limits payload to 5% capacity to avoid detection by modern steganalysis (tested with Aletheia). Includes GUI.

**Star count:** ⭐ 53

---

### python-jpeg-toolbox

| Tool | Language | Description |
|------|----------|-------------|
| [python-jpeg-toolbox](https://github.com/daniellerch/python-jpeg-toolbox) | Python/C | JPEG toolbox for reading/writing DCT coefficients, quantization matrices, Huffman tables |

**Note:** Python library for low-level JPEG manipulation. Used for JPEG steganography research and development.

**Star count:** ⭐ 16

---

### Steganography-In-C (bapzz)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-In-C](https://github.com/bapzz/Steganography-In-C) | C | C steganography implementation (2017) |

**Note:** C steganography library.

**Star count:** ⭐ 49

---

### QRSteganography (Maldev-Academy)

| Tool | Language | Description |
|------|----------|-------------|
| [QRSteganography](https://github.com/Maldev-Academy/QRSteganography) | C | QR code steganography (2026) |

**Note:** Steganography via QR codes.

**Star count:** ⭐ 47

---

### iOS-Steganography (JaafarRammal)

| Tool | Language | Description |
|------|----------|-------------|
| [iOS-Steganography](https://github.com/JaafarRammal/iOS-Steganography) | Swift | iOS steganography app (2019) |

**Note:** iOS image steganography.

**Star count:** ⭐ 8

---

### accessibility-protocol (tuildes)

| Tool | Language | Description |
|------|----------|-------------|
| [accessibility-protocol](https://github.com/tuildes/accessibility-protocol) | Swift | Swift steganography protocol (2026) |

**Note:** Swift steganography framework.

**Star count:** ⭐ 7

---

### Image-Cipher (SKocur)

| Tool | Language | Description |
|------|----------|-------------|
| [Image-Cipher](https://github.com/SKocur/Image-Cipher) | Kotlin | Android image steganography (2025) |

**Note:** Android steganography app.

**Star count:** ⭐ 65

---

### pixelsafe (StefanOltmann)

| Tool | Language | Description |
|------|----------|-------------|
| [pixelsafe](https://github.com/StefanOltmann/pixelsafe) | Kotlin | Android steganography app (2026) |

**Note:** Secure image storage with steganography.

**Star count:** ⭐ 50

---

### Insider (Shyguy99)

| Tool | Language | Description |
|------|----------|-------------|
| [Insider](https://github.com/Shyguy99/Insider) | Kotlin | Android steganography (2021) |

**Note:** Android steganography application.

**Star count:** ⭐ 33

---

### plain-sight (bufferhead-code)

| Tool | Language | Description |
|------|----------|-------------|
| [plain-sight](https://github.com/bufferhead-code/plain-sight) | TypeScript | Plain sight steganography (2024) |

**Note:** TypeScript steganography library.

**Star count:** ⭐ 56

---

### Steganography-C2 (Pnkcaht)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-C2](https://github.com/Pnkcaht/Steganography-C2) | TypeScript | C2 steganography framework (2026) |

**Note:** Command and control steganography.

**Star count:** ⭐ 43

---

### ZeroWidthStego (Muvesz)

| Tool | Language | Description |
|------|----------|-------------|
| [ZeroWidthStego](https://github.com/Muvesz/ZeroWidthStego) | Python | Zero-width steganography (2026) |

**Note:** Zero-width character steganography.

**Star count:** ⭐ 0

---

### PhantomStego (AleX-AA08)

| Tool | Language | Description |
|------|----------|-------------|
| [PhantomStego](https://github.com/AleX-AA08/PhantomStego) | Python | Phantom steganography tool (2026) |

**Note:** Advanced steganography implementation.

**Star count:** ⭐ 0

---

### hinayer (nullice)

| Tool | Language | Description |
|------|----------|-------------|
| [hinayer](https://github.com/nullice/hinaLayer) | JavaScript | JS image steganography (2017) |

**Note:** JavaScript steganography layer.

**Star count:** ⭐ 64

---

### perfectly-secure-steganography (schroederdewitt)

| Tool | Language | Description |
|------|----------|-------------|
| [perfectly-secure-steganography](https://github.com/schroederdewitt/perfectly-secure-steganography) | Python | Perfectly secure steganography (2023) |

**Note:** Information-theoretic steganography.

**Star count:** ⭐ 63

---

### busysteg (jaybosamiya)

| Tool | Language | Description |
|------|----------|-------------|
| [busysteg](https://github.com/jaybosamiya/busysteg) | Python | Busy steganography tool (2017) |

**Note:** Practical steganography implementation.

**Star count:** ⭐ 63

---

### Steganography-Website-Project (Vatshayan)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-Website-Project](https://github.com/Vatshayan/Steganography-Website-Project) | Python | Web-based steganography (2022) |

**Note:** Online steganography platform.

**Star count:** ⭐ 63

---

### StegoGAN (sian-wusidi)

| Tool | Language | Description |
|------|----------|-------------|
| [StegoGAN](https://github.com/sian-wusidi/StegoGAN) | Python | GAN-based steganography (2024) |

**Note:** Deep learning steganography with GANs.

**Star count:** ⭐ 60

---

### Stego_Dropper (ahhh)

| Tool | Language | Description |
|------|----------|-------------|
| [Stego_Dropper](https://github.com/ahhh/Stego_Dropper) | Python | Steganography dropper tool (2015) |

**Note:** Data exfiltration via steganography.

**Star count:** ⭐ 59

---

### van-gonography (JoshuaKasa)

| Tool | Language | Description |
|------|----------|-------------|
| [van-gonography](https://github.com/JoshuaKasa/van-gonography) | Python | Van Gogh style image steganography (2025) |

**Note:** Artistic steganography using Van Gogh style.

**Star count:** ⭐ 449

---

### tweetdoom (discatte)

| Tool | Language | Description |
|------|----------|-------------|
| [tweetdoom](https://github.com/discatte/tweetdoom) | Ruby | Twitter steganography (2021) |

**Note:** Steganography for Twitter posts.

**Star count:** ⭐ 45

---

### StegaShade (merwin-asm)

| Tool | Language | Description |
|------|----------|-------------|
| [StegaShade](https://github.com/merwin-asm/StegaShade) | Python | Image shading steganography (2025) |

**Note:** Image steganography using shading.

**Star count:** ⭐ 41

---

### StegX (Heisenberk)

| Tool | Language | Description |
|------|----------|-------------|
| [StegX](https://github.com/Heisenberk/StegX) | Python | MP3 steganography tool (2018) |

**Note:** MP3 audio steganography.

**Star count:** ⭐ 30

---

### stegonaut (knez)

| Tool | Language | Description |
|------|----------|-------------|
| [stegonaut](https://github.com/knez/stegonaut) | Python | Audio steganography tool (2026) |

**Note:** Audio steganography in Python.

**Star count:** ⭐ 18

---

### MP3Stego (Charleswyt)

| Tool | Language | Description |
|------|----------|-------------|
| [MP3Stego](https://github.com/Charleswyt/MP3Stego) | C | MP3 steganography (2018) |

**Note:** C implementation of MP3 steganography.

**Star count:** ⭐ 10

---

### poltergeist (Shell-Company)

| Tool | Language | Description |
|------|----------|-------------|
| [poltergeist](https://github.com/Shell-Company/poltergeist) | Python | Whitespace steganography tool (2023) |

**Note:** Whitespace encoding steganography.

**Star count:** ⭐ 20

---

### Steganography-SNOW-AVariation (Swati-Rathi)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-SNOW-AVariation](https://github.com/Swati-Rathi/Steganography-SNOW-AVariation) | Python | SNOW steganography variation (2015) |

**Note:** SNOW whitespace steganography variant.

**Star count:** ⭐ 7

---

### Steganographyx (athrvadeshmukh)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganographyx](https://github.com/athrvadeshmukh/Steganographyx) | Python | Audio steganography tool (2023) |

**Note:** WAV audio steganography.

**Star count:** ⭐ 9

---

### stegnowav (riz4d)

| Tool | Language | Description |
|------|----------|-------------|
| [stegnowav](https://github.com/riz4d/stegnowav) | Python | WAV file steganography (2022) |

**Note:** WAV audio steganography.

**Star count:** ⭐ 8

---

### wavehider (richstokes)

| Tool | Language | Description |
|------|----------|-------------|
| [wavehider](https://github.com/richstokes/wavehider) | Python | Audio steganography for WAV (2021) |

**Note:** Hide data in audio WAV files.

**Star count:** ⭐ 8

---

### StegLLM

| Tool | Language | Description |
|------|----------|-------------|
| [StegLLM](https://github.com/Rin313/StegLLM) | Python | LLM-based steganography (2025) |

**Note:** Large language model steganography.

**Star count:** ⭐ 21

---

### Stega-Carder (vesamet)

| Tool | Language | Description |
|------|----------|-------------|
| [Stega-Carder](https://github.com/vesamet/Stega-Carder) | Python | Carder steganography tool (2021) |

**Note:** Card-based steganography.

**Star count:** ⭐ 14

---

### steganography (stealthcopter)

| Tool | Language | Description |
|------|----------|-------------|
| [steganography](https://github.com/stealthcopter/steganography) | Python | Android steganography tool (2016) |

**Note:** Android image steganography.

**Star count:** ⭐ 28

---

### conceal (mrahimygk)

| Tool | Language | Description |
|------|----------|-------------|
| [conceal](https://github.com/mrahimygk/conceal) | Kotlin | Android steganography app (2021) |

**Note:** Android steganography library.

**Star count:** ⭐ 19

---

### FFTStegPic (0xcomposure)

| Tool | Language | Description |
|------|----------|-------------|
| [FFTStegPic](https://github.com/0xcomposure/FFTStegPic) | Python | FFT-based image steganography (2024) |

**Note:** Frequency domain steganography.

**Star count:** ⭐ 11

---

### Stegano-Engine (BryanApolonio)

| Tool | Language | Description |
|------|----------|-------------|
| [Stegano-Engine](https://github.com/BryanApolonio/Stegano-Engine) | Python | Advanced steganography engine (2026) |

**Note:** Advanced steganography toolkit.

**Star count:** ⭐ 5

---

### netneedle (optiv)

| Tool | Language | Description |
|------|----------|-------------|
| [netneedle](https://github.com/optiv/netneedle) | Python | Network steganography tool (2016) |

**Note:** Network packet steganography.

**Star count:** ⭐ 81

---

### CTF_tools (gregalletti)

| Tool | Language | Description |
|------|----------|-------------|
| [CTF_tools](https://github.com/gregalletti/CTF_tools) | Python | CTF steganography tools |

**Note:** Collection of CTF stego tools.

**Star count:** ⭐ 362

### SpyChat (SIMRAN88)

| Tool | Language | Description |
|------|----------|-------------|
| [SpyChat](https://github.com/SIMRAN88/SpyChat) | Python | Chat steganography tool (2020) |

**Note:** Steganography for chat messages.

**Star count:** ⭐ 8

---

### StegaPhoto (gregives)

| Tool | Language | Description |
|------|----------|-------------|
| [StegaPhoto](https://github.com/gregives/StegaPhoto) | JavaScript | Web photo steganography (2023) |

**Note:** Browser-based steganography.

**Star count:** ⭐ 21

---

### stegapp (Njancodes)

| Tool | Language | Description |
|------|----------|-------------|
| [stegapp](https://github.com/Njancodes/stegapp) | Python | Web steganography app (2024) |

**Note:** Online steganography application.

**Star count:** ⭐ 11

---

### Feature-Extractors-for-Video-Steganalysis (zhanghong863)

| Tool | Language | Description |
|------|----------|-------------|
| [Feature-Extractors-for-Video-Steganalysis](https://github.com/zhanghong863/Feature-Extractors-for-Video-Steganalysis) | Python | Video steganalysis features (2021) |

**Note:** Video steganalysis research tool.

**Star count:** ⭐ 73

---

### stego-discord (0x44F)

| Tool | Language | Description |
|------|----------|-------------|
| [stego-discord](https://github.com/0x44F/stego-discord) | Python | Discord steganography tool (2022) |

**Note:** Steganography for Discord messages.

**Star count:** ⭐ 17

---

### MasquerBot (ra101)

| Tool | Language | Description |
|------|----------|-------------|
| [MasquerBot](https://github.com/ra101/MasquerBot) | Python | Telegram steganography bot (2025) |

**Note:** Telegram bot for steganography.

**Star count:** ⭐ 10

---

### Steganography-Telegram-Bot (kousha1999)

| Tool | Language | Description |
|------|----------|-------------|
| [Steganography-Telegram-Bot](https://github.com/kousha1999/Steganography-Telegram-Bot) | Python | Telegram bot for images (2019) |

**Note:** Image steganography via Telegram.

**Star count:** ⭐ 4

---

### Image-in-Audio-Steganography (haoyuhsu)

| Tool | Language | Description |
|------|----------|-------------|
| [Image-in-Audio-Steganography](https://github.com/haoyuhsu/Image-in-Audio-Steganography) | Python | Hide images in audio (2020) |

**Note:** Image-in-audio steganography.

**Star count:** ⭐ 21

---

### phon3x-art (Phon3x)

| Tool | Language | Description |
|------|----------|-------------|
| [phon3x-art](https://github.com/Phon3x/phon3x-art) | Python | Steganography art project (2026) |

**Note:** Artistic steganography.

**Star count:** ⭐ 18

---

### StegaStamp-plus (Charmve)

| Tool | Language | Description |
|------|----------|-------------|
| [StegaStamp-plus](https://github.com/Charmve/StegaStamp-plus) | Python | Enhanced StegaStamp (2024) |

**Note:** Improved StegaStamp implementation.

**Star count:** ⭐ 42

---

### ium (foobuzz)

| Tool | Language | Description |
|------|----------|-------------|
| [ium](https://github.com/foobuzz/ium) | Python | Invisible undisplayed messages (2015) |

**Note:** Invisible character steganography.

**Star count:** ⭐ 26

---

### SecretPixel (x011)

| Tool | Language | Description |
|------|----------|-------------|
| [SecretPixel](https://github.com/x011/SecretPixel) | Python | Secret pixel steganography |

**Note:** Pixel-based steganography.

**Star count:** ⭐ 344

---

### File_Hider (x011)

| Tool | Language | Description |
|------|----------|-------------|
| [File_Hider](https://github.com/x011/File_Hider) | Python | File hiding tool |

**Note:** File steganography tool.

**Star count:** ⭐ 145

---

### StegoShark (XYFrank103)

| Tool | Language | Description |
|------|----------|-------------|
| [StegoShark](https://github.com/XYFrank103/StegoShark) | Python | Network steganography |

**Note:** Network packet steganography.

**Star count:** ⭐ 81
