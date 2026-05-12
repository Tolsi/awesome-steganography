# Filesystem & OS Steganography

<!-- TOC -->
## Contents (6 methods)

**[Storage Methods](#storage-methods)**
- [File Slack](#file-slack)
- [NTFS ADS](#ntfs-ads)
- [HPA/DCO](#hpadco)
- [Data After EOF](#data-after-eof)

**[Encryption-based](#encryption-based)**
- [VeraCrypt Hidden Volume](#veracrypt-hidden-volume)
- [StegFS](#stegfs)

**[Metadata](#metadata)**
- [Metadata Steganography](#metadata-steganography)
- [Control-Flow Steganography](#control-flow-steganography)
<!-- /TOC -->

## Storage Methods

---

### File Slack

**Goal:** Hide data in unused space between file end and cluster boundary.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **File Slack** | 1995 | Unused cluster space between file end and sector/cluster boundary | Any FS [[1]](https://www.garykessler.net/library/fsc_stego.html) |

**State of the art:** Classic OS-level steganography. Kessler (2004, updated 2015) documents file slack as a well-known data hiding location in forensics contexts.

**Production readiness:** Mature

**Implementations:**
- [bmap](https://github.com/CameronLonsdale/bmap) ⭐ 45 — Python, file slack reader/writer

**Security status:** Caution — Visible to forensic tools such as Autopsy, FTK, and EnCase

**Community acceptance:** Niche

---

### NTFS ADS

**Goal:** Hide data in NTFS Alternate Data Streams.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **NTFS ADS** | 1999 | Named data streams attached to any NTFS file | Windows NTFS [[1]](https://www.researchgate.net/publication/222825848_Data_hiding_in_the_NTFS_file_system) |

**State of the art:** Well-known Windows technique documented by Rubin et al. and widely covered in forensics literature (Kessler 2004). ADS streams invisible to Explorer but detectable by `dir /r` and all major forensic tools.

**Production readiness:** Mature

**Security status:** Broken — Detected by `dir /r`, PowerShell, Sysinternals Streams, and all major forensic suites

**Community acceptance:** Widely trusted — Known technique, standard forensics training topic

---

### HPA/DCO

**Goal:** Hide data in ATA-protected areas invisible to OS.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HPA/DCO** | 2006 | Host Protected Area / Device Configuration Overlay on ATA drives | HDD/SSD ATA [[1]](https://www.utica.edu/academic/institutes/ecii/publications/articles/EFE36584-D13F-2962-67BEB146864A2671.pdf) |

**State of the art:** Gupta, Hoeschele & Rogers (Int'l Journal of Digital Evidence, 2006) document HPA/DCO as anti-forensic data hiding; accessible only with special ATA commands not issued by normal OS tools.

**Production readiness:** Experimental

**Security status:** Secure — Invisible to OS; requires ATA SET MAX ADDRESS / DCO commands to detect

**Community acceptance:** Niche

---

## Encryption-based

---

### VeraCrypt Hidden Volume

**Goal:** Plausible deniability through hidden encrypted volumes.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **VeraCrypt Hidden Volume** | 2013 | Hidden inside outer volume | Plausible deniability |

**State of the art:** Best available deniable encryption. Cannot prove existence.

**Production readiness:** Production

**Implementations:**
- [VeraCrypt](https://github.com/veracrypt/VeraCrypt) ⭐ 4.5k

**Security status:** Secure — Mathematically cannot prove existence

**Community acceptance:** Standard — Industry standard for deniable encryption

---

### StegFS

**Goal:** Transparent steganographic filesystem with plausible deniability.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **StegFS** | 1998 | Partition filled with random bits; files hidden via keyed block allocation | Linux [[1]](https://link.springer.com/chapter/10.1007/3-540-49380-8_6) [[2]](https://link.springer.com/chapter/10.1007/10719724_32) |

**State of the art:** Anderson, Needham & Shamir (IH 1998) proposed the steganographic filesystem concept; McDonald & Kuhn (IH 1999) implemented it as StegFS on Linux ext2. Superseded by VeraCrypt hidden volumes for practical use.

**Production readiness:** Experimental

**Implementations:**
- [StegFS](https://www.cl.cam.ac.uk/~mgk25/ih99-stegfs.pdf) — original Linux implementation (unmaintained)

**Security status:** Secure — Cannot prove existence of hidden files; plausible deniability

**Community acceptance:** Niche

---

## Metadata

---

### Metadata Steganography

**Goal:** Hide data in file metadata fields.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Metadata** | 1998 | EXIF, ID3, XMP, document properties | Universal [[1]](https://www.garykessler.net/library/fsc_stego.html) |

**State of the art:** Simple but limited capacity. Widely documented in forensics literature (Kessler 2004). Tools like ExifTool enable trivial read/write of metadata steganography in JPEG, MP3, PDF, and Office files.

**Production readiness:** Mature

**Implementations:**
- [ExifTool](https://exiftool.org/) — Perl/C++, universal metadata read/write tool

**Security status:** Caution — Metadata fields are plainly visible; stripped by most upload pipelines

**Community acceptance:** Widely trusted

---

### Control-Flow Steganography

**Goal:** Hide data in program binaries using instruction-level redundancy.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Hydan** | 2004 | Functionally-equivalent x86 instruction substitution | ~1/110 bit encoding rate [[1]](https://link.springer.com/chapter/10.1007/978-3-540-30191-2_15) |

**State of the art:** El-Khalil & Keromytis (ICICS 2004) encode data by choosing among sets of functionally equivalent x86 instructions using a Blowfish-derived key. Low capacity (~1/110 bits per instruction) but undetectable without statistical analysis of instruction frequencies.

**Production readiness:** Experimental

**Implementations:**
- [hydan](http://www.crazyboy.com/hydan/) ⭐ — C, original tool (unmaintained)

**Security status:** Caution — Detectable by statistical analysis of instruction set distribution

**Community acceptance:** Niche

---

### Data After EOF

**Goal:** Hide data after end of file marker.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **EOF Stego** | 1996 | Append data after the logical EOF marker | Universal [[1]](https://www.garykessler.net/library/fsc_stego.html) |

**State of the art:** Simple append technique; works with many file formats that stop reading at a marker (JPEG FFD9, ZIP end-of-central-directory, etc.). Documented in forensics literature as a well-known hiding location.

**Production readiness:** Deprecated

**Security status:** Broken — Detectable by comparing logical file size to format-defined end; caught by binwalk, foremost, and all major forensic tools

**Community acceptance:** Niche
