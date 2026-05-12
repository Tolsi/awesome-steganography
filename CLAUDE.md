# Repository Structure

## Overview

This is a curated reference for steganography algorithms, tools, and techniques. Content is organized into thematic category files under `categories/`, with a flat alphabetical index in `INDEX.md` and a categorized table of contents in `README.md`.

## File Layout

```
README.md                          — Entry point: categorized TOC + contributing/license
INDEX.md                           — Alphabetical index of all sections
CLAUDE.md                          — This file
categories/
  01-text-steganography.md
  02-image-steganography.md
  03-audio-steganography.md
  04-video-steganography.md
  05-network-steganography.md
  06-filesystem-os.md
  07-coverless-generative.md
  08-traffic-obfuscation.md
  09-physical-social.md
  10-steganalysis.md
```

## Category File Structure

Each category file is organized into **subcategories** (## level) containing **algorithm entries** (### level):

```
# Category Title

<!-- TOC -->
## Contents (N algorithms)

**[Subcategory Name](#subcategory-name)**
- [Algorithm 1](#algorithm-1)
- [Algorithm 2](#algorithm-2)

**[Another Subcategory](#another-subcategory)**
- [Algorithm 3](#algorithm-3)
<!-- /TOC -->

## Subcategory Name

---

### Algorithm 1
...content...
---

### Algorithm 2
...content...
---

## Another Subcategory

---

### Algorithm 3
...content...
---
```

### Subcategory rules

- Each category file MUST have 2–4 subcategories grouping related algorithms.
- Subcategory headings are `##` level with a `---` separator after them.
- Algorithm entries are `###` level, each ending with `---`.
- The TOC uses bold subcategory links with indented algorithm entries.
- When adding a new algorithm, place it in the most appropriate existing subcategory. Create a new subcategory only if no existing one fits.

## Algorithm Entry Format

Each algorithm/method appears as a `###` section inside a subcategory. The format is:

```markdown
### Algorithm Name

**Goal:** One-sentence plain-language purpose.

| Column1 | Column2 | ... |
|---------|---------|-----|
| **Algorithm** | Year | Description [[1]](url) |

**State of the art:** Brief description of what is deployed/best today. Cross-links to related sections.

---
```

### Column conventions

- **Basic methods:** `| Algorithm | Year | Principle | Note |`
- **Advanced methods:** `| Algorithm | Year | Architecture/Approach | Notable Feature |`
- Use `**bold**` for algorithm name in the first column.
- Citations use inline footnote style: `[[1]](url)` — numbered per row.
- Year is the publication/standardization year (use `—` if not applicable).

### Mandatory assessment fields

Every `###` algorithm section MUST include the following fields after the table and "State of the art" line:

```markdown
**Production readiness:** <One of: Production / Mature / Experimental / Research / Deprecated>
<Brief explanation — e.g. "Widely deployed in CTF challenges" or "Academic prototype only">

**Implementations:** <List of notable open-source implementations with URLs>
- [Library/tool name](url) ⭐ <star count> — language, brief note
- [Library/tool name](url) ⭐ <star count> [archived] — language, brief note *(if archived)*

**Security status:** <One of: Secure / Caution / Broken / Superseded>
<Brief explanation — known attacks, detection methods, or reason for deprecation>

**Community acceptance:** <One of: Standard / Widely trusted / Emerging / Niche / Controversial>
<Brief explanation — peer review status, adoption, notable endorsements or criticisms>
```

### Star counts in implementations

Every GitHub repository link in the **Implementations:** section MUST include a star count badge in the format `⭐ <count>`:

```markdown
- [Library](https://github.com/owner/repo) ⭐ 1234 — language, note
```

Star count formatting:
- `< 1000`: show exact number (e.g. `⭐ 843`)
- `1000–9999`: one decimal (e.g. `⭐ 2.1k`)
- `≥ 10000`: no decimal (e.g. `⭐ 29k`)

Non-GitHub links do not require star counts.

Field value definitions:

**Production readiness** levels:
- `Production` — deployed at scale in real-world systems
- `Mature` — well-studied, production-quality implementations exist
- `Experimental` — working implementations but not battle-tested
- `Research` — academic/prototype stage, no production implementations
- `Deprecated` — superseded or discouraged

**Security status** levels:
- `Secure` — no known practical attacks at recommended parameters
- `Caution` — requires careful implementation or has known vulnerabilities
- `Broken` — practical attacks exist; should not be used
- `Superseded` — replaced by better alternatives

**Community acceptance** levels:
- `Standard` — recognized by major organizations
- `Widely trusted` — strong peer review, broad adoption
- `Emerging` — active research, growing interest
- `Niche` — limited to specific domains
- `Controversial` — disputed security claims

## Cross-References

Sections cross-reference each other using Markdown anchor links:

```markdown
[Section Name](#section-name-slug)
```

GitHub slugifies anchors by: lowercasing, removing non-alphanumeric characters (except hyphens), then replacing spaces with hyphens.

For links across files:

```markdown
[Section Name](NN-filename.md#section-name-slug)
```

Files inside `categories/` link to sibling files using just the filename (e.g. `03-image-jpeg-domain.md#algorithm-name`), NOT `categories/03-...`.

## Adding a New Algorithm

1. Identify the most appropriate category file (or create a new one if none fits).
2. **Check for duplicates:** search all category files for the algorithm name before adding. Each algorithm MUST appear in exactly ONE category file.
3. Identify the correct **subcategory** within the file (or create one if needed).
4. Add a new `###` section following the entry format above.
5. Add a corresponding row to `INDEX.md` in alphabetical order.
6. Update the `<!-- TOC -->` block to include the new algorithm.
7. Add a cross-reference from related sections where useful.
8. If creating a new category file, add it to `README.md`'s Contents list and update `CLAUDE.md`.

### No duplicates rule

Every `###` algorithm section MUST exist in exactly one category file. **Never duplicate across files.** If an algorithm is relevant to multiple categories, place in the most specific one and add a cross-reference from others.

### Pre-commit quality checklist

Before committing changes, verify ALL of the following:

1. **Required fields:** Every `###` algorithm section has `**Goal:**`, `**State of the art:**`, `**Production readiness:**`, `**Implementations:**`, `**Security status:**`, `**Community acceptance:**`.
2. **Field explanations:** Each field has a 1-line explanation following it.
3. **Section separators:** Every `###` algorithm section ends with `---`.
4. **Subcategories:** Algorithms are grouped under `##` subcategory headings (3–6 per file).
5. **No duplicates:** No `###` algorithm heading appears in more than one category file.
6. **Valid links:** All internal cross-references point to existing anchors.
7. **TOC up to date:** The `<!-- TOC -->` block lists subcategories (bold) with indented algorithm entries.
8. **INDEX.md:** New or renamed sections are reflected in `INDEX.md`.

## Category Summaries

| # | File | Contents |
|---|------|----------|
| 01 | text-steganography | Structural (whitespace, Unicode, homoglyphs), semantic, LLM-based (Meteor, Discop, ChatStega) |
| 02 | image-steganography | Spatial (LSB, BPCS, PVD, EMD, STC), adaptive (HUGO, WOW, S-UNIWARD, HILL, MiPOD), JPEG (JSteg, F5, nsF5, OutGuess, J-UNIWARD, UED), transform (DWT, DFT, SVD), reversible, deep learning (HiDDeN, SteganoGAN, StegaStamp, CRoSS) |
| 03 | audio-steganography | Time domain (LSB, parity, echo, phase), frequency (spread spectrum, MDCT), compressed (MP3Stego, AAC, Opus), neural (DeepSound, WavMark, AudioSeal, PRoADS) |
| 04 | video-steganography | Frame LSB/DCT, motion vectors, intra prediction modes, QP modulation, CABAC, HEVC PU partition |
| 05 | network-steganography | Header fields (IP, TCP, HTTP), timing channels, DNS tunneling (iodine, dnscat2, dns2tcp), QUIC (QuicCourier), VoIP (LACK), 5G/6G, CYPRESS |
| 06 | filesystem-os | File slack, NTFS ADS, HPA/DCO, VeraCrypt hidden volume, StegFS, metadata |
| 07 | coverless-generative | Hash-based, StyleGAN, diffusion (CRoSS, MIDAS), 3D (StegoNGP, 3DGS) |
| 08 | traffic-obfuscation | Tor (obfs4, meek, Snowflake, WebTunnel), V2Ray/Xray/REALITY, Trojan-GFW, Hysteria 2, Shadowsocks, NaiveProxy |
| 09 | physical-social | Printer dots, microdots, invisible ink, cultural references, contextual hiding |
| 10 | steganalysis | Classical (chi-square, RS, WS, SPAM, SRM, DCTR), deep learning (XuNet, YeNet, SRNet, ZhuNet), network detection |
