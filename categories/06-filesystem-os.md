# Filesystem & OS Steganography

<!-- TOC -->
## Contents (6 methods)

**[Storage Methods](#storage-methods)**
- [File Slack](#file-slack)
- [NTFS ADS](#ntfs-ads)
- [HPA/DCO](#hpadco)

**[Encryption-based](#encryption-based)**
- [VeraCrypt Hidden Volume](#veracrypt-hidden-volume)
- [StegFS](#stegfs)

**[Metadata](#metadata)**
- [Metadata Steganography](#metadata-steganography)
<!-- /TOC -->

## Storage Methods

---

### File Slack

**Goal:** Hide data in unused space between file end and cluster boundary.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **File Slack** | 1995 | Unused cluster space | Any FS |

**State of the art:** Classic OS-level steganography.

**Production readiness:** Mature

**Security status:** Caution — Visible to forensic tools

**Community acceptance:** Niche

---

### NTFS ADS

**Goal:** Hide data in NTFS Alternate Data Streams.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **NTFS ADS** | 1999 | Alternate Data Streams | Windows NTFS |

**State of the art:** Well-known Windows technique.

**Production readiness:** Mature

**Security status:** Broken — All Windows tools detect

**Community acceptance:** Widely trusted — Known technique

---

### HPA/DCO

**Goal:** Hide data in ATA-protected areas invisible to OS.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HPA/DCO** | 2005 | Host Protected Area | HDD/SSD ATA |

**State of the art:** Hardware-level hiding.

**Production readiness:** Experimental

**Security status:** Secure — Invisible to software

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

**Goal:** Transparent steganographic filesystem.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **StegFS** | 2003 | Transparent FS | Linux |

**State of the art:** Filesystem-level hiding.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Niche

---

## Metadata

---

### Metadata Steganography

**Goal:** Hide data in file metadata.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Metadata** | 1998 | EXIF, ID3, etc. | Universal |

**State of the art:** Simple but limited capacity.

**Production readiness:** Mature

**Security status:** Caution — Metadata visible

**Community acceptance:** Widely trusted
