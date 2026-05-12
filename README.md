# Awesome Steganography

> Curated collection of steganography algorithms and tools, classified by application domain

Steganography — the art of hiding the existence of a message. Unlike cryptography (which hides the content), steganography hides the very fact that communication is happening.

## The Trade-off Triangle

Every steganographic method balances three competing properties:

| Property | Description | Metrics |
|----------|-------------|---------|
| **Capacity** | How much data can be embedded | bpp (bits per pixel), bps (bits per sample), bpb (bits per byte) |
| **Imperceptibility** | How indistinguishable is the stego from cover | PSNR, SSIM, BER detection accuracy |
| **Robustness** | Does message survive processing | Compression, geometric transforms, filtering |

---

## Table of Contents

- [Text Steganography](categories/01-text-steganography.md)
- [Image Steganography](categories/02-image-steganography.md)
- [Audio Steganography](categories/03-audio-steganography.md)
- [Video Steganography](categories/04-video-steganography.md)
- [Network Steganography](categories/05-network-steganography.md)
- [Filesystem & OS](categories/06-filesystem-os.md)
- [Coverless / Generative](categories/07-coverless-generative.md)
- [Traffic Obfuscation](categories/08-traffic-obfuscation.md)
- [Physical & Social](categories/09-physical-social.md)
- [Steganalysis](categories/10-steganalysis.md)
- [Tools & Implementations](categories/11-tools.md)

---

## Contributing

Contributions welcome! Please follow the format in CLAUDE.md and ensure:
- Each algorithm appears in exactly one category file
- Include production readiness, implementations, security status, and community acceptance
- Add corresponding entry to INDEX.md

---

## License

MIT
