# Image Steganography

<!-- TOC -->
## Contents (232 algorithms)

**[Spatial Domain](#spatial-domain)**
- [LSB Replacement](#lsb-replacement)
- [LSB Matching](#lsb-matching)
- [BPCS](#bpcs)
- [PVD](#pvd)
- [EMD](#emd)
- [Sudoku-based](#sudoku-based-steganography)
- [FuzzyStego](#fuzzystego)
- [Chaotic Map LSB](#chaotic-map-lsb)
- [Content-Aware Steganography](#content-aware-steganography)
- [Skin Tone Adaptive](#skin-tone-adaptive)
- [STC](#stc)

**[Adaptive Methods](#adaptive-methods)**
- [HUGO](#hugo)
- [WOW](#wow)
- [S-UNIWARD](#s-uniward)
- [HILL](#hill)
- [MiPOD](#mipod)
- [QIM](#qim)
- [MG/MVG](#mgmvg)

**[JPEG Domain](#jpeg-domain)**
- [JSteg](#jsteg)
- [F5](#f5)
- [nsF5](#nsf5)
- [OutGuess](#outguess)
- [J-UNIWARD](#j-uniward)
- [UED/UERD](#ueduerd)

**[Transform Domain](#transform-domain)**
- [DWT](#dwt)
- [DFT](#dft)
- [SVD](#svd)

**[Reversible Methods](#reversible-methods)**
- [Histogram Shifting](#histogram-shifting)
- [Difference Expansion](#difference-expansion)
- [Prediction Error Expansion](#prediction-error-expansion)

**[Deep Learning Methods](#deep-learning-methods)**
- [HiDDeN](#hidden)
- [SteganoGAN](#steganogan)
- [StegaStamp](#stegastamp)
- [CRoSS](#cross)
- [StegNet](#stegnet)
- [SMILENet](#smilenet)
- [StegoNGP](#stegongp)
- [DTAMS](#dtams)
- [PSyDUCK](#psyduck)
- [CIF](#cif)
- [STCL](#stcl)
- [GIFDL](#gifdl)
- [StegaFFD](#stegaffd)
- [Arbitrary-Resolution Deep Image Steganography](#arbitrary-resolution-deep-image-steganography)
- [Adaptive Fuzzy Logic Steganography](#adaptive-fuzzy-logic-steganography)
- [Memristive In-Memory Image Steganography](#memristive-in-memory-image-steganography)
- [StegaVision](#stegavision)
- [Foveation Steganography](#foveation-steganography)
- [StegaINR](#stegainr-steeganography-by-implicit-neural-representations)
- [StegaINR4MIH](#stegainr4mih-inr-for-multi-image-hiding)
- [DiffStega](#diffstega-training-free-diffusion-steganography)
- [Stable Messenger](#stable-messenger)
- [DKiS](#dkis-decay-weight-invertible-image-steganography)
- [PRIS](#pris-practical-robust-invertible-network-for-image-steganography)
- [Multi-User Multi-Key](#multi-user-multi-key-image-steganography)
- [StegaPos](#stegapos)
- [Rethinking Security of Diffusion-based Generative Steganography](#rethinking-security-of-diffusion-based-generative-steganography)
- [Intelligent Carrier Allocation](#intelligent-carrier-allocation)
- [Secure Audio Embedding in Images](#secure-audio-embedding-in-images)
- [Deep Data Hiding for ICAO-Compliant Face Images](#deep-data-hiding-for-icao-compliant-face-images)
- [Defending against Stegomalware](#defending-against-stegomalware)
- [On the Possible Detectability of Image-in-Image Steganography](#on-the-possible-detectability-of-image-in-image-steganography)
- [Robust Provably Secure Image Steganography via Latent Iterative Optimization](#robust-provably-secure-image-steganography-via-latent-iterative-optimization)

**[Recent arXiv Papers (2024–2026)](#recent-arxiv-papers-20242026)**
- [An Additive Approximation Scheme for Generating Dyadic Codin...](#an-additive-approximation-scheme-for-generating-dyadic-codings-for-the-outputs-of-an-llm)
- [Toward Accountable AI-Generated Content on Social Platforms:...](#toward-accountable-ai-generated-content-on-social-platforms-steganographic-attribution-and-multimodal-harm-detection)
- [Invisible Safety Threat: Malicious Finetuning for LLM via St...](#invisible-safety-threat-malicious-finetuning-for-llm-via-steganography)
- [: Towards Semantic Steganography via Large Language Models](#towards-semantic-steganography-via-large-language-models)
- [Training-Free Color-Aware Adversarial Diffusion Sanitization...](#training-free-color-aware-adversarial-diffusion-sanitization-for-diffusion-stegomalware-defense-at-security-gateways)
- [Frobenius Revivals in Laplacian Cellular Automata: Chaos, Re...](#frobenius-revivals-in-laplacian-cellular-automata-chaos-replication-and-reversible-encoding)
- [Reasoning Models Sometimes Output Illegible Chains of Though...](#reasoning-models-sometimes-output-illegible-chains-of-thought)
- [A Concrete Roadmap towards Safety Cases based on Chain-of-Th...](#a-concrete-roadmap-towards-safety-cases-based-on-chain-of-thought-monitoring)
- [All Code, No Thought: Current Language Models Struggle to Re...](#all-code-no-thought-current-language-models-struggle-to-reason-in-ciphered-language)
- [ZK-WAGON: Imperceptible Watermark for Image Generation Model...](#zk-wagon-imperceptible-watermark-for-image-generation-models-using-zk-snarks)
- [StegOT: Trade-offs in Steganography via Optimal Transport](#stegot-trade-offs-in-steganography-via-optimal-transport)
- [A Technical Review on Comparison and Estimation of Steganogr...](#a-technical-review-on-comparison-and-estimation-of-steganographic-tools)
- [Joint Lossless Compression and Steganography for Medical Ima...](#joint-lossless-compression-and-steganography-for-medical-images-via-large-language-models)
- [Feature Prediction in Quantum Graph Recurrent Neural Network...](#feature-prediction-in-quantum-graph-recurrent-neural-networks-with-applications-in-information-hiding)
- [Large language models can learn and generalize steganographi...](#large-language-models-can-learn-and-generalize-steganographic-chain-of-thought-under-process-supervision)
- [Implicit Jailbreak Attacks via Cross-Modal Information Conce...](#implicit-jailbreak-attacks-via-cross-modal-information-concealment-on-vision-language-models)
- [Quantum steganography using catalytic and entanglement-assis...](#quantum-steganography-using-catalytic-and-entanglement-assisted-quantum-codes)
- [Shackled Dancing: A Bit-Locked Diffusion Algorithm for Lossl...](#shackled-dancing-a-bit-locked-diffusion-algorithm-for-lossless-and-controllable-image-steganography)
- [CLPSTNet: A Progressive Multi-Scale Convolutional Steganogra...](#clpstnet-a-progressive-multi-scale-convolutional-steganography-model-integrating-curriculum-learning)
- [Fragile Watermarking for Image Certification Using Deep Steg...](#fragile-watermarking-for-image-certification-using-deep-steganographic-embedding)
- [Big Brother is Watching: Proactive Deepfake Detection via Le...](#big-brother-is-watching-proactive-deepfake-detection-via-learnable-hidden-face)
- [Parasite: A Steganography-based Backdoor Attack Framework fo...](#parasite-a-steganography-based-backdoor-attack-framework-for-diffusion-models)
- [RoSMM: A Robust and Secure Multi-Modal Watermarking Framewor...](#rosmm-a-robust-and-secure-multi-modal-watermarking-framework-for-diffusion-models)
- [Towards Secure Semantic Communications in the Presence of In...](#towards-secure-semantic-communications-in-the-presence-of-intelligent-eavesdroppers)
- [ImF: Implicit Fingerprint for Large Language Models](#imf-implicit-fingerprint-for-large-language-models)
- [Hiding Images in Diffusion Models by Editing Learned Score F...](#hiding-images-in-diffusion-models-by-editing-learned-score-functions)
- [Quantum Direct Steganography Scheme Based on Modified Genera...](#quantum-direct-steganography-scheme-based-on-modified-generator-projection-directions-of-steane-code-over-a-single-type-pauli-channel)
- [Adaptive 3D Mesh Steganography Based on Feature-Preserving D...](#adaptive-3d-mesh-steganography-based-on-feature-preserving-distortion)
- [Provably Secure Robust Image Steganography via Cross-Modal E...](#provably-secure-robust-image-steganography-via-cross-modal-error-correction)
- [A Novel Approach to Image Steganography Using Generative Adv...](#a-novel-approach-to-image-steganography-using-generative-adversarial-networks)
- [Facial Features Matter: a Dynamic Watermark based Proactive ...](#facial-features-matter-a-dynamic-watermark-based-proactive-deepfake-detection-approach)
- [Magnetic steganography based on wide field diamond quantum m...](#magnetic-steganography-based-on-wide-field-diamond-quantum-microscopy)
- [Neural Cover Selection for Image Steganography](#neural-cover-selection-for-image-steganography)
- [IWN: Image Watermarking Based on Idempotency](#iwn-image-watermarking-based-on-idempotency)
- [Steganographic Entanglement Sharing](#steganographic-entanglement-sharing)
- [Robust Message Embedding via Attention Flow-Based Steganogra...](#robust-message-embedding-via-attention-flow-based-steganography)
- [Diffusion-Based Hierarchical Image Steganography](#diffusion-based-hierarchical-image-steganography)
- [High Fidelity Artificial Quantum Thermal State Generation us...](#high-fidelity-artificial-quantum-thermal-state-generation-using-encoded-coherent-states)
- [StegoGAN: Leveraging Steganography for Non-Bijective Image-t...](#stegogan-leveraging-steganography-for-non-bijective-image-to-image-translation)
- [Enhancing Steganographic Text Extraction: Evaluating the Imp...](#enhancing-steganographic-text-extraction-evaluating-the-impact-of-nlp-models-on-accuracy-and-semantic-coherence)
- [Transparency Attacks: How Imperceptible Image Layers Can Foo...](#transparency-attacks-how-imperceptible-image-layers-can-fool-ai-perception)
- [Null Space Properties of Neural Networks with Applications t...](#null-space-properties-of-neural-networks-with-applications-to-image-steganography)
- [EditGuard: Versatile Image Watermarking for Tamper Localizat...](#editguard-versatile-image-watermarking-for-tamper-localization-and-copyright-protection)
- [THInImg: Cross-modal Steganography for Presenting Talking He...](#thinimg-cross-modal-steganography-for-presenting-talking-heads-in-images)
- [GhostEncoder: Stealthy Backdoor Attacks with Dynamic Trigger...](#ghostencoder-stealthy-backdoor-attacks-with-dynamic-triggers-to-pre-trained-encoders-in-self-supervised-learning)
- [Invertible Mosaic Image Hiding Network for Very Large Capaci...](#invertible-mosaic-image-hiding-network-for-very-large-capacity-image-steganography)
- [Focus on Content not Noise: Improving Image Generation for N...](#focus-on-content-not-noise-improving-image-generation-for-nuclei-segmentation-by-suppressing-steganography-in-cyclegan)
- [Semi-supervised Cycle-GAN for face photo-sketch translation ...](#semi-supervised-cycle-gan-for-face-photo-sketch-translation-in-the-wild)
- [StyleStegan: Leak-free Style Transfer Based on Feature Stega...](#stylestegan-leak-free-style-transfer-based-on-feature-steganography)
- [Diffusion-Stego: Training-free Diffusion Generative Steganog...](#diffusion-stego-training-free-diffusion-generative-steganography-via-message-projection)
- [Generative Steganographic Flow](#generative-steganographic-flow)
- [Generative Steganography Diffusion](#generative-steganography-diffusion)
- [Robust image steganography against lossy JPEG compression ba...](#robust-image-steganography-against-lossy-jpeg-compression-based-on-embedding-domain-selection-and-adaptive-error-correction)
- [RoSteALS: Robust Steganography using Autoencoder Latent Spac...](#rosteals-robust-steganography-using-autoencoder-latent-space)
- [Learning Iterative Neural Optimizers for Image Steganography](#learning-iterative-neural-optimizers-for-image-steganography)
- [Low-frequency Image Deep Steganography: Manipulate the Frequ...](#low-frequency-image-deep-steganography-manipulate-the-frequency-distribution-to-hide-secrets-with-tenacious-robustness)
- [Towards Robust Image-in-Audio Deep Steganography](#towards-robust-image-in-audio-deep-steganography)
- [Artistic Curve Steganography Carried by Musical Audio](#artistic-curve-steganography-carried-by-musical-audio)
- [Invisible Backdoor Attack with Dynamic Triggers against Pers...](#invisible-backdoor-attack-with-dynamic-triggers-against-person-re-identification)
- [Errorless Robust JPEG Steganography using Outputs of JPEG Co...](#errorless-robust-jpeg-steganography-using-outputs-of-jpeg-coders)
- [Data Hiding with Deep Learning: A Survey Unifying Digital Wa...](#data-hiding-with-deep-learning-a-survey-unifying-digital-watermarking-and-steganography)
- [A Robust Image Steganographic Scheme against General Scaling...](#a-robust-image-steganographic-scheme-against-general-scaling-attacks)
- [Applications of single-photon technology](#applications-of-single-photon-technology)
- [FaceSigns: Semi-Fragile Neural Watermarks for Media Authenti...](#facesigns-semi-fragile-neural-watermarks-for-media-authentication-and-countering-deepfakes)
- [Image Steganography based on Style Transfer](#image-steganography-based-on-style-transfer)
- [A Survey on Patients Privacy Protection with Stganography an...](#a-survey-on-patients-privacy-protection-with-stganography-and-visual-encryption)
- [Improving Performance of Semantic Segmentation CycleGANs by ...](#improving-performance-of-semantic-segmentation-cyclegans-by-noise-injection-into-the-latent-segmentation-space)
- [Adaptive Steganography Based on bargain Game](#adaptive-steganography-based-on-bargain-game)
- ["Robot Steganography"?: Opportunities and Challenges](#robot-steganography-opportunities-and-challenges)
- [A Color Image Steganography Based on Frequency Sub-band Sele...](#a-color-image-steganography-based-on-frequency-sub-band-selection)
- [Image quality enhancement of embedded holograms in holograph...](#image-quality-enhancement-of-embedded-holograms-in-holographic-information-hiding-using-deep-neural-networks)
- [Pixel-Stega: Generative Image Steganography Based on Autoreg...](#pixel-stega-generative-image-steganography-based-on-autoregressive-models)
- [Interpretable Privacy Preservation of Text Representations U...](#interpretable-privacy-preservation-of-text-representations-using-vector-steganography)
- [Multitask Identity-Aware Image Steganography via Minimax Opt...](#multitask-identity-aware-image-steganography-via-minimax-optimization)
- [Pixel identification in an image using Grover Search Algorit...](#pixel-identification-in-an-image-using-grover-search-algorithm)
- [Improving Cost Learning for JPEG Steganography by Exploiting...](#improving-cost-learning-for-jpeg-steganography-by-exploiting-jpeg-domain-knowledge)
- [Universal Adversarial Perturbations Through the Lens of Deep...](#universal-adversarial-perturbations-through-the-lens-of-deep-steganography-towards-a-fourier-perspective)
- [CSIS: compressed sensing-based enhanced-embedding capacity i...](#csis-compressed-sensing-based-enhanced-embedding-capacity-image-steganography-scheme)
- [Multi-Image Steganography Using Deep Neural Networks](#multi-image-steganography-using-deep-neural-networks)
- [FoolHD: Fooling speaker identification by Highly imperceptib...](#foolhd-fooling-speaker-identification-by-highly-imperceptible-adversarial-disturbances)
- [New Design Paradigm of Distortion Cost Function for Efficien...](#new-design-paradigm-of-distortion-cost-function-for-efficient-jpeg-steganography)
- [Generative Steganography with Kerckhoffs' Principle](#generative-steganography-with-kerckhoffs-principle)
- [Painting with Hue, Saturation, and Brightness Control by Nan...](#painting-with-hue-saturation-and-brightness-control-by-nanoscale-3d-printing)
- [Adversarial Images through Stega Glasses](#adversarial-images-through-stega-glasses)
- [Enabling optical steganography, data storage, and encryption...](#enabling-optical-steganography-data-storage-and-encryption-with-plasmonic-colors)
- [\ell_1SABMIS: \ell_1-minimization and sparse approximation b...](#ell-1sabmis-ell-1-minimization-and-sparse-approximation-based-blind-multi-image-steganography-scheme)
- [Secure Steganography Technique Based on Bitplane Indexes](#secure-steganography-technique-based-on-bitplane-indexes)
- [Stego Quality Enhancement by Message Size Reduction and Fibo...](#stego-quality-enhancement-by-message-size-reduction-and-fibonacci-bit-plane-mapping)
- [Efficient High Capacity Steganography Technique](#efficient-high-capacity-steganography-technique)
- [Steganography Based on Pixel Intensity Value Decomposition](#steganography-based-on-pixel-intensity-value-decomposition)
- [Improving embedding efficiency for digital steganography by ...](#improving-embedding-efficiency-for-digital-steganography-by-exploiting-similarities-between-secret-and-cover-images)
- [Data hiding in speech signal using steganography and encrypt...](#data-hiding-in-speech-signal-using-steganography-and-encryption)
- [Universal Stego Post-processing for Enhancing Image Steganog...](#universal-stego-post-processing-for-enhancing-image-steganography)
- [Invisible Backdoor Attacks on Deep Neural Networks via Stega...](#invisible-backdoor-attacks-on-deep-neural-networks-via-steganography-and-regularization)
- [Self-Contained Stylization via Steganography for Reverse and...](#self-contained-stylization-via-steganography-for-reverse-and-serial-style-transfer)
- [Distribution-Preserving Steganography Based on Text-to-Speec...](#distribution-preserving-steganography-based-on-text-to-speech-generative-models)
- [Beyond Unfolding: Exact Recovery of Latent Convex Tensor Dec...](#beyond-unfolding-exact-recovery-of-latent-convex-tensor-decomposition-under-reshuffling)
- [Hide the Image in FC-DenseNets to another Image](#hide-the-image-in-fc-densenets-to-another-image)
- [Enhancing JPEG Steganography using Iterative Adversarial Exa...](#enhancing-jpeg-steganography-using-iterative-adversarial-examples)
- [Steganography Protocols for Quantum Channels](#steganography-protocols-for-quantum-channels)
- [BASN -- Learning Steganography with Binary Attention Mechani...](#basn-learning-steganography-with-binary-attention-mechanism)
- [Recent Advances of Image Steganography with Generative Adver...](#recent-advances-of-image-steganography-with-generative-adversarial-networks)
- [Generative Reversible Data Hiding by Image to Image Translat...](#generative-reversible-data-hiding-by-image-to-image-translation-via-gans)
- [StegoAppDB: a Steganography Apps Forensics Image Database](#stegoappdb-a-steganography-apps-forensics-image-database)
- [Solving the large syndrome calculation problem in steganogra...](#solving-the-large-syndrome-calculation-problem-in-steganography)
- [A security steganography scheme based on hdr image](#a-security-steganography-scheme-based-on-hdr-image)
- [SteganoGAN: High Capacity Image Steganography with GANs](#steganogan-high-capacity-image-steganography-with-gans)
- [Adaptive Spatial Steganography Based on Probability-Controll...](#adaptive-spatial-steganography-based-on-probability-controlled-adversarial-examples)
- [Emerging Applications of Reversible Data Hiding](#emerging-applications-of-reversible-data-hiding)
- [Combined Image Encryption and Steganography Algorithm in the...](#combined-image-encryption-and-steganography-algorithm-in-the-spatial-domain)
- [Invisible Steganography via Generative Adversarial Networks](#invisible-steganography-via-generative-adversarial-networks)
- [High Capacity Image Data Hiding of Scanned Text Documents Us...](#high-capacity-image-data-hiding-of-scanned-text-documents-using-improved-quadtree)
- [The Cut and Dominating Set Problem in A Steganographer Netwo...](#the-cut-and-dominating-set-problem-in-a-steganographer-network)
- [A Graph-theoretic Model to Steganography on Social Networks](#a-graph-theoretic-model-to-steganography-on-social-networks)
- [SSGAN: Secure Steganography Based on Generative Adversarial ...](#ssgan-secure-steganography-based-on-generative-adversarial-networks)
- [Encoding DNA sequences by integer chaos game representation](#encoding-dna-sequences-by-integer-chaos-game-representation)
- [CycleGAN, a Master of Steganography](#cyclegan-a-master-of-steganography)
- [End-to-end Trained CNN Encode-Decoder Networks for Image Ste...](#end-to-end-trained-cnn-encode-decoder-networks-for-image-steganography)
- [A Robust Data Hiding Process Contributing to the Development...](#a-robust-data-hiding-process-contributing-to-the-development-of-a-semantic-web)
- [StegIbiza: Steganography in Club Music Implemented in Python](#stegibiza-steganography-in-club-music-implemented-in-python)
- [FPGA Implementation of a Novel Image Steganography for Hidin...](#fpga-implementation-of-a-novel-image-steganography-for-hiding-images)
- [Enhanced Boolean Correlation Matrix Memory](#enhanced-boolean-correlation-matrix-memory)
- [Quantum Enhanced Correlation Matrix Memories via States Orth...](#quantum-enhanced-correlation-matrix-memories-via-states-orthogonalisation)
- [Can Machine Learn Steganography? - Implementing LSB Substitu...](#can-machine-learn-steganography-implementing-lsb-substitution-and-matrix-coding-steganography-with-feed-forward-neural-networks)
- [Optimal Binary Coding for q^+ -state Data Embedding](#optimal-binary-coding-for-q-state-data-embedding)
- [Reading Between the Pixels: Photographic Steganography for C...](#reading-between-the-pixels-photographic-steganography-for-camera-display-messaging)
- [An Enhanced Edge Adaptive Steganography Approach Using Thres...](#an-enhanced-edge-adaptive-steganography-approach-using-threshold-value-for-region-selection)
- [A New Image Steganographic Technique using Pattern based Bit...](#a-new-image-steganographic-technique-using-pattern-based-bits-shuffling-and-magic-lsb-for-grayscale-images)
- [Capacity Enlargement Of The PVD Steganography Method Using T...](#capacity-enlargement-of-the-pvd-steganography-method-using-the-glm-technique)
- [Covert Communication Gains from Adversary's Ignorance of Tra...](#covert-communication-gains-from-adversarys-ignorance-of-transmission-time)
- [Steganography: A Secure way for Transmission in Wireless Sen...](#steganography-a-secure-way-for-transmission-in-wireless-sensor-networks)
- [Towards Reversible De-Identification in Video Sequences Usin...](#towards-reversible-de-identification-in-video-sequences-using-3d-avatars-and-steganography)
- [Ontology-based Secure Retrieval of Semantically Significant ...](#ontology-based-secure-retrieval-of-semantically-significant-visual-contents)
- [Data Hiding in Video using Triangularization LSB Technique](#data-hiding-in-video-using-triangularization-lsb-technique)
- [Hiding Information in Noise: Fundamental Limits of Covert Wi...](#hiding-information-in-noise-fundamental-limits-of-covert-wireless-communication)
- [Identification of Image Operations Based on Steganalytic Fea...](#identification-of-image-operations-based-on-steganalytic-features)
- [Optimal Radiometric Calibration for Camera-Display Communica...](#optimal-radiometric-calibration-for-camera-display-communication)
- [Olfactory Signal Processing](#olfactory-signal-processing)
- [Secret Image Sharing Using Grayscale Payload Decomposition a...](#secret-image-sharing-using-grayscale-payload-decomposition-and-irreversible-image-steganography)
- [Digital Image Data Hiding Techniques: A Comparative Study](#digital-image-data-hiding-techniques-a-comparative-study)
- [An Easy yet Effective Method for Detecting Spatial Domain LS...](#an-easy-yet-effective-method-for-detecting-spatial-domain-lsb-steganography)
- [A simple technique for steganography](#a-simple-technique-for-steganography)
- [Hiding Image in Image by Five Modulus Method for Image Stega...](#hiding-image-in-image-by-five-modulus-method-for-image-steganography)
- [A Fresnelet-Based Encryption of Medical Images using Arnold ...](#a-fresnelet-based-encryption-of-medical-images-using-arnold-transform)
- [Improving success probability and embedding efficiency in co...](#improving-success-probability-and-embedding-efficiency-in-code-based-steganography)
- [A Hash based Approach for Secure Keyless Steganography in Lo...](#a-hash-based-approach-for-secure-keyless-steganography-in-lossless-rgb-images)
- [Classification of minimal 1-saturating sets in PG(2,q), q\le...](#classification-of-minimal-1-saturating-sets-in-pg2q-qleq-23)
- [Coordination using Implicit Communication](#coordination-using-implicit-communication)
- [Hiding Quantum Information in the Perfect Code](#hiding-quantum-information-in-the-perfect-code)
- [Image Sterilization to Prevent LSB-based Steganographic Tran...](#image-sterilization-to-prevent-lsb-based-steganographic-transmission)
- [Colour Guided Colour Image Steganography](#colour-guided-colour-image-steganography)
- [Quantum Steganography and Quantum Error-Correction](#quantum-steganography-and-quantum-error-correction)
- [An Alternative Approach of Steganography using Reference Ima...](#an-alternative-approach-of-steganography-using-reference-image)
- [Product Perfect Z2Z4-linear codes in Steganography](#product-perfect-z2z4-linear-codes-in-steganography)
- [Signal Enhancement and Background Suppression Using Interfer...](#signal-enhancement-and-background-suppression-using-interference-and-entanglement)
- [A New Image Steganography Based On First Component Alteratio...](#a-new-image-steganography-based-on-first-component-alteration-technique)
- [Trellis-coded quantization for public-key steganography](#trellis-coded-quantization-for-public-key-steganography)
- [Quantum computing, phase estimation and applications](#quantum-computing-phase-estimation-and-applications)

**[Software Tools](#software-tools)**
- [OpenPuff](#openpuff)
- [SilentEye](#silenteye)
- [Stegosuite](#stegosuite)
- [cloacked-pixel](#cloacked-pixel)
- [stegpy](#stegpy)
- [jphide / jpseek](#jphide-jpseek)
<!-- /TOC -->

## Spatial Domain

---

### LSB Replacement

**Goal:** Hide data by replacing the least significant bit of each pixel.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LSB Replacement** | 1998 | Replace LSB of pixel | 1 bpp (3 bpp RGB) |

**State of the art:** Simplest method. Good for learning but easily detected.

**Production readiness:** Deprecated

**Implementations:**
- [steghide](https://github.com/StephanHofmannmich/steghide) ⭐ 1.8k — Classic LSB tool
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287

**Security status:** Broken — Detected by chi-square, RS-analysis in milliseconds

**Community acceptance:** Niche — Good for learning, not for production

---

### LSB Matching

**Goal:** Hide data with reduced statistical artifacts compared to LSB replacement.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **LSB Matching** | 2006 | Random +/-1 if LSB ≠ bit | 1 bpp [[1]](https://ieeexplore.ieee.org/document/1618698/) |

**State of the art:** Better than replacement, still vulnerable to WS analysis.

**Production readiness:** Mature
Well-studied; preferred over LSB replacement for its reduced statistical signature.

**Implementations:**
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, includes LSB matching variants and steganalysis

**Security status:** Caution — Vulnerable to weighted stego (WS) analysis

**Community acceptance:** Widely trusted — Standard in steganography courses

---

### BPCS

**Goal:** Hide data in complex bit-planes of the image.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **BPCS** | 1998 | Replace complex bit-planes | 10-40% capacity |

**State of the art:** Higher capacity than LSB while maintaining visual quality.

**Production readiness:** Mature

**Implementations:**
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287 — Includes BPCS

**Security status:** Caution — Detected by complexity analysis attacks

**Community acceptance:** Niche — Popular in watermarking, less in pure stego

---

### PVD

**Goal:** Adaptively embed more data in edge regions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **PVD** | 2003 | Embed in pixel difference | 3-5 bpp [[1]](https://dl.acm.org/doi/10.1016/S0167-8655(02)00402-6) |

**State of the art:** Adaptive capacity based on local contrast.

**Production readiness:** Mature
Widely implemented with well-known range-table variants; good tradeoff between capacity and quality.

**Implementations:**
- [tony-josi/pvd_steganography](https://github.com/tony-josi/pvd_steganography) ⭐ 22 — Python, PNG cover images

**Security status:** Caution — Vulnerable to histogram analysis of differences

**Community acceptance:** Widely trusted — Widely studied and implemented

---

### EMD

**Goal:** Encode data using multiple pixels with minimal modification.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **EMD** | 2006 | n pixels encode d-ary digit | log2(2n+1)/n bpp [[1]](https://www.researchgate.net/publication/3417888_Efficient_Steganographic_Embedding_by_Exploiting_Modification_Direction) |

**State of the art:** Better PSNR than LSB, mathematically elegant.

**Production readiness:** Mature
Frequently re-implemented in academic papers; not commonly used in production tools.

**Implementations:**
- [cagatayavsar/EMD](https://github.com/cagatayavsar/EMD) ⭐ 0 — Python/C++, direct implementation of Zhang & Wang (2006)

**Security status:** Caution — Good perceptual quality but specific statistical signature

**Community acceptance:** Niche — Academic interest, practical use limited

---

### Sudoku-based Steganography

**Goal:** Use Sudoku puzzle solutions as encoding key.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Sudoku** | 2009 | Sudoku grid key | High key space [[1]](https://dl.acm.org/doi/10.1109/ARTCom.2009.116) |

**State of the art:** Large key space provides security.

**Production readiness:** Experimental
Academic prototypes only; the large Sudoku key space improves robustness against brute-force steganalysis.

**Security status:** Caution
Security relies on key secrecy; no dedicated steganalysis attacks published, but underlying pixel modification is detectable.

**Community acceptance:** Niche
Cited in academic literature but no mainstream adoption.

---

### FuzzyStego

**Goal:** Use fuzzy logic for adaptive embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **FuzzyStego** | 2025 | Fuzzy logic intensity classification | Adaptive [[1]](https://doi.org/10.32604/cmc.2025.061246) |

**State of the art:** Adaptive approach using fuzzy logic; achieves average PSNR of 58.6 dB.

**Production readiness:** Experimental
Proposed in 2025; no production deployments; promising PSNR results at lower payloads.

**Security status:** Caution
Uses LSB-derived embedding; underlying pixel modification is vulnerable to standard steganalysis.

**Community acceptance:** Niche
Recent publication; limited citations so far.

---

### Chaotic Map LSB

**Goal:** Use chaotic maps for secure LSB embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chaotic Map LSB** | 2008 | Chaos-based pixel selection | Increased security [[1]](https://www.sciencedirect.com/science/article/abs/pii/S0045790624004932) |

**State of the art:** Chaotic sequences add security layer by randomizing embedding positions.

**Production readiness:** Experimental
Used in academic work; not production-hardened; chaotic key sensitivity is both a strength and implementation risk.

**Implementations:**
- [FifthEpoch/Chaos_LSB](https://github.com/FifthEpoch/Chaos_LSB) ⭐ 0 — Python, AES + chaotic pixel selection

**Security status:** Caution
Chaotic key randomizes positions but underlying LSB embedding is still detectable by calibration attacks.

**Community acceptance:** Niche
Popular research topic; many variant papers published but no standard definition.

---

### Content-Aware Steganography

**Goal:** Hide data based on semantic content of image.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Content-Aware** | 2006 | Human-assigned semantics | Secure against non-human [[1]](https://link.springer.com/chapter/10.1007/978-3-540-74124-4_8) |

**State of the art:** Uses semantic understanding; embeds secrets in human-interpretable cover meaning rather than pixel values.

**Production readiness:** Experimental
Theoretical framework; no widely adopted tooling exists.

**Security status:** Secure — Human adversary required; automated steganalysis is ineffective

**Community acceptance:** Emerging
Influential theoretical paper but limited practical implementations.

---

### Skin Tone Adaptive

**Goal:** Embed in skin-tone regions using secret angle.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Skin Tone Adaptive** | 2009 | Skin region detection via colour space | Adaptive embedding [[1]](https://www.sciencedirect.com/science/article/abs/pii/S0165168409001686) |

**State of the art:** Adaptive based on image content; psychovisual redundancy in skin tones reduces perceptibility.

**Production readiness:** Experimental
Academic prototype; requires reliable skin detection as pre-processing step.

**Security status:** Caution
Skin region detection can be replicated by an attacker; embedding within detected regions is not invisible to trained classifiers.

**Community acceptance:** Emerging
Cited in adaptive steganography surveys; not widely deployed.

---

### STC

**Goal:** Near-optimal embedding with minimal distortion.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **STC** | 2010 | Syndrome-Trellis Codes | Near rate-distortion bound |

**State of the art:** Foundation of modern adaptive steganography. Theoretical optimality.

**Production readiness:** Mature

**Implementations:**
- [stc-lib](https://github.com/coin3d/stc-lib) ⭐ 89 — C++ implementation

**Security status:** Secure — Enables best-in-class security with good distortion functions

**Community acceptance:** Widely trusted — Industry standard for modern stego algorithms

---

## Adaptive Methods

---

### HUGO

**Goal:** Model-driven adaptive steganography using detection features.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HUGO** | 2010 | SPAM features (4D co-occurrence) | First model-driven [[1]](https://link.springer.com/chapter/10.1007/978-3-642-16435-4_13) |

**State of the art:** Theoretically principled — optimizes against known detection features.

**Production readiness:** Mature
Reference Matlab implementation from DDE Binghamton; widely used as research baseline.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, includes HUGO, HILL, MiPOD simulators
- [dde.binghamton.edu](http://dde.binghamton.edu/download/stego_algorithms/) — original Matlab/MEX reference code

**Security status:** Secure — Strong against SPAM-based detectors

**Community acceptance:** Widely trusted — Foundational work, frequently cited (1000+)

---

### WOW

**Goal:** Embed primarily in edge regions using wavelet filters.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **WOW** | 2012 | Wavelet directional filters | Edge-only embedding |

**State of the art:** Good balance of capacity and security.

**Production readiness:** Mature

**Implementations:**
- [WOW-steganography](https://github.com/3xpl01tc0d3r/WOW-steganography) ⭐ 156

**Security status:** Secure — Competitive security

**Community acceptance:** Widely trusted — Widely implemented

---

### S-UNIWARD

**Goal:** Universal distortion function for steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **S-UNIWARD** | 2013 | Universal wavelet relative distortion | Best security |

**State of the art:** Works in both spatial and JPEG domain. Often cited as best-in-class.

**Production readiness:** Mature

**Implementations:**
- [nsf5sim](https://github.com/goxman/nsf5sim) ⭐ 78 — Includes S-UNIWARD

**Security status:** Secure — Often achieves best detection resistance

**Community acceptance:** Standard — De facto standard, most cited adaptive algorithm

---

### HILL

**Goal:** Distribute modifications to avoid concentrating in edges.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **HILL** | 2014 | High-pass + low-pass smoothing | Distributes changes [[1]](https://ieeexplore.ieee.org/document/7025854/) |

**State of the art:** Competitive with S-UNIWARD.

**Production readiness:** Mature
Frequently used benchmark in steganalysis research; Matlab reference implementation available from DDE.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, HILL simulator matching DDE Matlab output
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, includes HILL

**Security status:** Secure — Competitive with S-UNIWARD

**Community acceptance:** Widely trusted — Popular in implementations

---

### MiPOD

**Goal:** Theoretically optimal embedding under Gaussian assumptions.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MiPOD** | 2016 | Multivariate Gaussian | Fisher information optimal [[1]](https://dl.acm.org/doi/10.1109/tifs.2015.2486744) |

**State of the art:** Strong theoretical foundation; minimizes power of optimal Bayesian detector.

**Production readiness:** Experimental
Academic prototype; Matlab reference from DDE; Python reimplementation in conseal.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, MiPOD simulator
- [dde.binghamton.edu](http://dde.binghamton.edu/download/stego_algorithms/) — original Matlab reference

**Security status:** Secure — Strong theoretical guarantees

**Community acceptance:** Emerging — Academic interest, fewer practical implementations

---

## JPEG Domain

---

### JSteg

**Goal:** Original JPEG steganography using LSB.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **JSteg** | 1997 | LSB on DCT coefficients | Historical [[1]](http://www.cosy.sbg.ac.at/~uhl/jsteg.html) |

**State of the art:** Deprecated due to easy detection.

**Production readiness:** Deprecated
No longer recommended; the original tool by Derek Upham (1997) is still referenced in academic literature.

**Implementations:**
- [daniellerch/aletheia](https://github.com/daniellerch/aletheia) ⭐ 204 — Python steganalysis tool, includes JSteg detection

**Security status:** Broken — One of first detected by histogram analysis

**Community acceptance:** Niche — Historical importance, not recommended

---

### F5

**Goal:** Matrix encoding for efficient JPEG steganography.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **F5** | 2001 | Matrix encoding + decrement | Better efficiency |

**State of the art:** Historically important but vulnerable to attacks.

**Production readiness:** Deprecated

**Implementations:**
- [openstego](https://github.com/syvaidya/openstego) ⭐ 287

**Security status:** Broken — Vulnerable to shrinkage attack, blockiness analysis

**Community acceptance:** Niche — Historically important

---

### nsF5

**Goal:** F5 without shrinkage for better quality.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **nsF5** | 2007 | F5 without shrinkage (wet paper) | Better visual quality [[1]](https://dde.binghamton.edu/download/nsf5simulator/) [[2]](https://dl.acm.org/doi/10.1145/1341811.1341814) |

**State of the art:** Better than F5 but still detected.

**Production readiness:** Deprecated
Simulator available from DDE Binghamton; not for production use.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, nsF5 simulator
- [dde.binghamton.edu/download/nsf5simulator/](https://dde.binghamton.edu/download/nsf5simulator/) — original Matlab simulator (2008)

**Security status:** Caution — Better than F5 but still detected by CCJRM

**Community acceptance:** Niche
Used as baseline in JPEG steganalysis research.

---

### OutGuess

**Goal:** Preserve global DCT histogram during embedding.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **OutGuess** | 2001 | Preserves global histogram | Statistical preservation [[1]](https://en.wikipedia.org/wiki/OutGuess) [[2]](https://ws2.binghamton.edu/fridrich/Research/acm_outguess.pdf) |

**State of the art:** Vulnerable to local statistics attacks.

**Production readiness:** Deprecated
Historically used in real cases (e.g. Annanet spy ring); now easily detected.

**Implementations:**
- [outguess](https://github.com/crorvick/outguess) ⭐ 0 — C, original tool by Niels Provos

**Security status:** Broken — Vulnerable to local statistics attacks

**Community acceptance:** Niche
Historically significant but superseded by adaptive methods.

---

### J-UNIWARD

**Goal:** Best JPEG steganography against modern steganalysis.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **J-UNIWARD** | 2014 | UNIWARD on DCT | Best for JPEG [[1]](https://jis-eurasipjournals.springeropen.com/articles/10.1186/1687-417X-2014-1) |

**State of the art:** State-of-art for JPEG domain.

**Production readiness:** Mature
Reference Matlab code from DDE Binghamton; Python in conseal and stegolab.

**Implementations:**
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, J-UNIWARD simulator
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, J-UNIWARD implementation

**Security status:** Secure — State-of-art for JPEG

**Community acceptance:** Widely trusted
De facto standard JPEG steganography method in research.

---

### UED/UERD

**Goal:** Uniform distribution of changes across AC coefficients.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **UED/UERD** | 2014/2015 | Uniform embedding across DCT magnitudes | Competitive [[1]](https://ieeexplore.ieee.org/document/6776485/) [[2]](https://dl.acm.org/doi/abs/10.1109/tifs.2015.2473815) |

**State of the art:** Competitive with J-UNIWARD.

**Production readiness:** Mature
UERD rivals J-UNIWARD with significantly lower computational cost.

**Implementations:**
- [vazswk/UERD](https://github.com/vazswk/UERD) ⭐ 0 — Matlab, UERD simulator
- [uibk-uncover/conseal](https://github.com/uibk-uncover/conseal) ⭐ 17 — Python, UERD simulator

**Security status:** Secure — Competitive with J-UNIWARD

**Community acceptance:** Emerging
Growing use in JPEG steganalysis benchmarks.

---

### QIM

**Goal:** Embed data using quantization index modulation.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **QIM** | 2001 | Quantization-based | High robustness [[1]](https://ieeexplore.ieee.org/document/923725/) |

**State of the art:** Robust to compression, mathematically principled.

**Production readiness:** Mature
Foundational watermarking technique; used in audio/video watermarking pipelines.

**Security status:** Caution — Detectable by trained classifiers

**Community acceptance:** Widely trusted — Foundational watermarking method

---

### MG/MVG

**Goal:** Multi-grade variable group embedding for high capacity.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **MG/MVG** | 2011 | Multi-variable groups | High capacity [[1]](https://www.researchgate.net/publication/261601440_Uniform_Embedding_for_Efficient_JPEG_Steganography) |

**State of the art:** High capacity with good visual quality.

**Production readiness:** Experimental
Academic prototypes only; not widely deployed.

**Security status:** Caution
High capacity often trades off against detectability.

**Community acceptance:** Emerging
Cited in capacity-focused steganography literature.

---

## Transform Domain

---

### DWT

**Goal:** Embed in wavelet domain for robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DWT** | 1996 | High-frequency wavelet subbands | HH, HL, LH bands [[1]](https://dl.acm.org/doi/abs/10.1145/240178.240217) |

**State of the art:** Good robustness to compression.

**Production readiness:** Mature
Basis for many practical watermarking systems; widely implemented in toolkits.

**Implementations:**
- [daniellerch/stegolab](https://github.com/daniellerch/stegolab) ⭐ 51 — Python, multiple transform-domain methods

**Security status:** Caution
Modified wavelet coefficients are detectable by statistical feature extractors.

**Community acceptance:** Widely trusted
Core technique in digital watermarking standards.

---

### DFT

**Goal:** Embed in frequency domain for geometric robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **DFT** | 2005 | Magnitude/phase spectrum | Robust to rotation [[1]](https://www.researchgate.net/publication/269705199_Digital_Image_Steganography_An_FFT_Approach) |

**State of the art:** Robust to geometric transforms.

**Production readiness:** Mature
Used in geometric-robust watermarking; less common in pure steganography due to limited capacity.

**Security status:** Caution
DFT modifications are detectable by frequency-domain steganalysis.

**Community acceptance:** Niche
Preferred for geometric robustness applications; limited adoption in steganography.

---

### SVD

**Goal:** Modify singular values for robustness.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **SVD** | 2002 | Modify singular values | Often combined with DWT [[1]](https://link.springer.com/article/10.1007/s11042-017-4947-8) |

**State of the art:** Very robust to noise and filtering.

**Production readiness:** Mature
Frequently combined with DWT (DWT-SVD hybrid) for improved robustness and imperceptibility.

**Security status:** Caution
Singular value modifications can be detected; known false-positive issues in some SVD watermarking schemes.

**Community acceptance:** Widely trusted
Extensively studied; standard in robust watermarking literature.

---

## Reversible Methods

---

### Histogram Shifting

**Goal:** Lossless data hiding by shifting histogram.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Histogram Shifting** | 2006 | Shift histogram peak | Lossless [[1]](https://web.njit.edu/~ansari/papers/06TCAS.pdf) |

**State of the art:** Important for medical/legal imaging.

**Production readiness:** Mature
Foundational reversible data hiding technique; base for many subsequent improvements.

**Security status:** Secure — Lossless recovery guaranteed

**Community acceptance:** Widely trusted — Critical for sensitive imaging

---

### Difference Expansion

**Goal:** Expand pixel differences to embed data.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Difference Expansion** | 2003 | Expand differences | Lossless [[1]](https://ieeexplore.ieee.org/document/1227616/) |

**State of the art:** Foundational reversible method.

**Production readiness:** Mature
Tian (2003) is one of the most cited RDH papers; basis for many subsequent schemes.

**Security status:** Secure
Lossless pixel recovery; no known attacks that compromise cover/hidden content.

**Community acceptance:** Widely trusted
Foundational method; extensively cited in reversible data hiding literature.

---

### Prediction Error Expansion

**Goal:** Embed in prediction error for better efficiency.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Prediction Error Expansion** | 2007 | Embed in prediction error | Better than DE [[1]](https://ieeexplore.ieee.org/document/4099409/) |

**State of the art:** Improved efficiency over difference expansion.

**Production readiness:** Mature
Thodi & Rodriguez (2007) significantly improved on DE; widely used as baseline for RDH advances.

**Security status:** Secure
Lossless recovery guaranteed; no practical attacks on the hiding mechanism.

**Community acceptance:** Widely trusted
Extensively cited; considered standard alongside histogram shifting.

---

## Deep Learning Methods

---

### HiDDeN

**Goal:** End-to-end deep learning steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **HiDDeN** | 2018 | Encoder-decoder + noise | First end-to-end DL |

**State of the art:** Foundational work in DL steganography.

**Production readiness:** Experimental

**Implementations:**
- [HiDDeN](https://github.com/tancik/HiDDeN) ⭐ 892

**Security status:** Caution — Vulnerable to CNN steganalysis

**Community acceptance:** Widely trusted — Foundational work in DL stego

---

### SteganoGAN

**Goal:** GAN-based steganography with high capacity.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SteganoGAN** | 2019 | GAN + critic | 2-4 bpp |

**State of the art:** High capacity, defeats XuNet.

**Production readiness:** Experimental

**Implementations:**
- [SteganoGAN](https://github.com/DAI-Lab/SteganoGAN) ⭐ 428

**Security status:** Caution

**Community acceptance:** Widely trusted

---

### StegaStamp

**Goal:** Robust steganography surviving physical transmission.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaStamp** | 2020 | Robust encoder + augmentation | Survives print+photo |

**State of the art:** First practical robust steganography.

**Production readiness:** Experimental

**Implementations:**
- [StegaStamp](https://github.com/tancik/StegaStamp) ⭐ 1.2k

**Security status:** Secure — Robust to printing/photo

**Community acceptance:** Standard — Most practical DL method

---

### CRoSS

**Goal:** Diffusion-based steganography with natural cover distribution.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **CRoSS** | 2023 | Diffusion-based | Message controls seed/path [[1]](https://arxiv.org/abs/2305.16936) |

**State of the art:** State-of-art in generative stego.

**Production readiness:** Experimental
NeurIPS 2023 paper with official implementation; widely referenced in generative steganography literature.

**Implementations:**
- [CRoSS](https://github.com/yujiwen/CRoSS) ⭐ 157 — PyTorch, official NeurIPS 2023 implementation

**Security status:** Secure — State-of-art in generative stego; first to use diffusion models for controllable, robust, secure hiding

**Community acceptance:** Emerging — Growing rapidly; cited as foundational in diffusion-based steganography

---

### StegNet

**Goal:** High-capacity deep learning steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegNet** | 2018 | Multi-scale CNN | 98.2% decoding, 23.57 bpp [[1]](https://arxiv.org/abs/1806.06357) |

**State of the art:** Very high capacity image-in-image steganography using deep convolutional networks.

**Production readiness:** Research
Academic prototype; published 2018 in MDPI Future Internet journal.

**Security status:** Caution — Resistant to 5 classical steganalysis methods but not evaluated against modern CNN detectors

**Community acceptance:** Emerging — Research active; frequently cited in DL steganography surveys

---

### SMILENet

**Goal:** Extra-large capacity image steganography via synergistic mosaic.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **SMILENet** | 2025 | Synergistic mosaic invertible hiding | 25x image hiding [[1]](https://arxiv.org/abs/2503.05118) |

**State of the art:** Achieves 25x image hiding capacity, first to hide 25 secret images simultaneously.

**Production readiness:** Research
arXiv preprint March 2025; no production deployments known.

**Security status:** Caution — Security against modern steganalysis not yet evaluated

**Community acceptance:** Emerging — Very recent; addresses fundamental capacity limitations of prior methods

---

### DTAMS

**Goal:** High-capacity generative steganography via dynamic multi-timestep selection.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DTAMS** | 2026 | Dynamic multi-timestep + adaptive deviation mapping | Latent diffusion [[1]](https://arxiv.org/abs/2602.01160) |

**State of the art:** High capacity with good security at higher rates; addresses limitations of existing generative steganography at low embedding rates only.

**Production readiness:** Experimental
arXiv preprint February 2026; no production deployments known.

**Security status:** Secure — Maintains acceptable security and robustness at higher embedding rates

**Community acceptance:** Emerging — Recent paper addressing capacity-security tradeoff in latent diffusion steganography

---

### Approximate Gaussian Mapping

**Goal:** Generative image steganography using approximate Gaussian mapping.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Approximate Gaussian** | 2025 | ODE-based diffusion models | Deterministic synthesis [[1]](https://arxiv.org/abs/2510.07219) |

**State of the art:** Reduces numerical inversion errors in ODE-based diffusion steganography by allowing controlled deviations from standard normal prior.

**Production readiness:** Experimental
arXiv preprint October 2025; academic prototype only.

**Security status:** Secure — Controlled deviation from Gaussian prior reduces inversion errors without compromising security

**Community acceptance:** Emerging — Addresses a specific inversion error problem in diffusion-based steganography

---

### PSyDUCK

**Goal:** Training-free steganography for latent diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PSyDUCK** | 2025 | Training-free latent diffusion | Message projection [[1]](https://arxiv.org/abs/2501.19172) |

**State of the art:** No training required; extends generative steganography to latent-space video diffusion models.

**Production readiness:** Experimental
arXiv preprint January 2025; model-agnostic, no fine-tuning needed.

**Security status:** Secure — Dynamically adapts embedding strength to balance accuracy and detectability

**Community acceptance:** Emerging — Addresses scalability limitation of prior training-dependent approaches

---

### CIF

**Goal:** Reliable message extraction in diffusion-based generative steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **CIF** | 2025 | Constrained inversion framework | High-capacity embedding [[1]](https://arxiv.org/abs/2508.00434) |

**State of the art:** Improves extraction accuracy in lossy scenarios by iteratively recovering secret-embedded latent vectors.

**Production readiness:** Experimental
arXiv preprint August 2025; addresses extraction failure in high-capacity or lossy-transmission scenarios.

**Security status:** Secure — Constrained inversion maintains indistinguishability of generated images

**Community acceptance:** Emerging — Solves a practical extraction accuracy problem in diffusion-based generative steganography

---

### STCL (Spatial-Temporal Curriculum Learning)

**Goal:** Improve image steganography quality through progressive multi-scale curriculum learning.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **STCL** | 2025 | Progressive multi-scale convolutional | Better convergence [[1]](https://arxiv.org/abs/2504.17609) |

**State of the art:** Addresses poor quality and slow convergence issues in deep learning image steganography.

**Production readiness:** Research
arXiv preprint April 2025; academic prototype only.

**Security status:** Caution — Security properties not fully evaluated; focus is on quality and convergence

**Community acceptance:** Emerging — Part of a series of curriculum learning approaches for deep image steganography

---

### GIFDL (Generated Image Fluctuation Distortion Learning)

**Goal:** Enhance steganographic security through fluctuation distortion learning.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **GIFDL** | 2025 | Distortion learning framework | Enhanced security [[1]](https://arxiv.org/abs/2504.15139) |

**State of the art:** Improves minimum distortion steganography security; accepted by IEEE TIFS.

**Production readiness:** Research
Accepted by IEEE Transactions on Information Forensics and Security; academic prototype only.

**Security status:** Secure — Specifically designed to enhance security of minimum distortion steganography

**Community acceptance:** Emerging — IEEE TIFS acceptance indicates peer-reviewed quality

---

### StegaFFD (Steganography-based Face Forgery Detection)

**Goal:** Privacy-preserving face forgery detection via steganographic domain lifting.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaFFD** | 2026 | Steganography-based FFD framework | Privacy protection [[1]](https://arxiv.org/abs/2603.02886) |

**State of the art:** Protects privacy without raising suspicion; accepted by Machine Intelligence Research.

**Production readiness:** Research
arXiv preprint March 2026; accepted by Machine Intelligence Research journal.

**Security status:** Caution — Designed for forensic use, not covert communication; detection resistance not primary goal

**Community acceptance:** Emerging — Novel application of steganography to privacy-preserving deepfake detection

---

### Arbitrary-Resolution Deep Image Steganography

**Goal:** Hide secret images with different resolutions than cover images.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Arb-Resolution DIS** | 2026 | Resolution-flexible framework | No resampling required [[1]](https://arxiv.org/abs/2601.15739) |

**State of the art:** Solves resolution mismatch problem in deep steganography; eliminates detail loss from resampling.

**Production readiness:** Research
arXiv preprint January 2026; academic prototype only.

**Security status:** Caution — Security properties not yet fully characterized; focus is on resolution flexibility

**Community acceptance:** Emerging — Addresses a practical limitation in current deep image steganography frameworks

---

### Adaptive Fuzzy Logic Steganography

**Goal:** Adaptive embedding using fuzzy logic for better capacity-fidelity trade-off.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Fuzzy Logic Stego** | 2026 | Fuzzy logic-based embedding | Adaptive depth [[1]](https://arxiv.org/abs/2603.18105) |

**State of the art:** Better imperceptibility than fixed-depth LSB by adapting embedding depth based on local texture complexity.

**Production readiness:** Research
arXiv preprint March 2026; academic prototype only.

**Security status:** Caution — Adaptive LSB variant; improved over fixed-depth but still vulnerable to statistical steganalysis

**Community acceptance:** Emerging — Experimental evaluation demonstrates improved PSNR/SSIM over fixed-depth LSB

---

### Memristive In-Memory Image Steganography

**Goal:** Hardware-based steganography using memristive circuits.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Memristive Stego** | 2026 | In-memory computing | 42-44% energy reduction [[1]](https://arxiv.org/abs/2605.03494) |

**State of the art:** First hardware implementation of steganography using memristive in-memory computing circuits.

**Production readiness:** Experimental
arXiv preprint May 2026; custom circuit prototypes only, not software-deployable.

**Security status:** Caution — Hardware-level hiding; security depends on physical access constraints rather than algorithmic hardness

**Community acceptance:** Emerging — Novel hardware approach; bridges steganography and in-memory computing research

---

### StegaVision

**Goal:** Enhance steganography using attention mechanisms for better capacity-quality balance.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaVision** | 2024 | Attention-based network | Improved capacity [[1]](https://arxiv.org/abs/2411.05838) |

**State of the art:** Uses parallel channel and spatial attention to simultaneously improve image quality and hiding capacity.

**Production readiness:** Research
arXiv preprint November 2024 (AAAI 2025 Student Abstract); academic prototype only.

**Security status:** Caution — Attention-based architecture; security against CNN steganalysis not fully evaluated

**Community acceptance:** Emerging — Demonstrates that attention mechanisms overcome the quality-capacity tradeoff seen in prior methods

---

### Foveation Steganography

**Goal:** Improve payload capacity using foveated rendering and latent representations.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Foveation** | 2025 | Foveated rendering + latent | 100→500 bits capacity [[1]](https://arxiv.org/abs/2510.13151) |

**State of the art:** Achieves up to 500 bits with 1 failure bit out of 2000; presented at SIGGRAPH Asia 2025.

**Production readiness:** Research
SIGGRAPH Asia 2025 Posters; academic prototype only.

**Security status:** Caution — Focus on capacity improvement; steganalysis resistance not primary evaluation criterion

**Community acceptance:** Emerging — SIGGRAPH Asia venue indicates visibility in graphics/vision community

---

### StegaINR (Steganography by Implicit Neural Representations)

**Goal:** Hide functions within functions using INR without additional extractors.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaINR** | 2023 | INR-based | No message extractor needed [[1]](https://arxiv.org/abs/2312.04743) |

**State of the art:** First work to introduce INR into steganography; hides secret function inside stego function using a shared key.

**Production readiness:** Research
arXiv preprint December 2023; academic prototype only.

**Security status:** Caution — Novel paradigm; security properties under active investigation

**Community acceptance:** Emerging — First exploration of hiding information in INR model weights

---

### StegaINR4MIH (INR for Multi-Image Hiding)

**Goal:** Embed multiple secret images into a cover image with high quality recovery.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaINR4MIH** | 2024 | INR multi-image | High capacity [[1]](https://arxiv.org/abs/2410.10117) |

**State of the art:** Addresses contour shadowing and color distortion issues; achieves PSNR >42 for 2 secret images, >39 for 5 secret images.

**Production readiness:** Research
arXiv preprint October 2024; academic prototype with code available.

**Security status:** Caution — Security against steganalysis not primary focus; designed for high-quality multi-image hiding

**Community acceptance:** Emerging — Extends StegaINR to practical multi-image hiding with quantified quality guarantees

---

### DiffStega (Training-Free Diffusion Steganography)

**Goal:** Training-free coverless image steganography using diffusion models.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DiffStega** | 2024 | Diffusion-based | Training-free [[1]](https://arxiv.org/abs/2407.10459) |

**State of the art:** Universal training-free coverless diffusion steganography; uses password-dependent reference image and Noise Flip technique; IJCAI 2024.

**Production readiness:** Research
Published at IJCAI 2024; official implementation available.

**Implementations:**
- [DiffStega](https://github.com/evtricks/DiffStega) ⭐ 49 — PyTorch, official IJCAI 2024 implementation

**Security status:** Secure — Password-dependent reference image prevents unauthorized decryption; no risk of text prompt leakage

**Community acceptance:** Emerging — IJCAI 2024 acceptance; addresses key limitations of prior CRoSS-style prompt-based methods

---

### Stable Messenger

**Goal:** Message-concealed image generation with high message accuracy.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Stable Messenger** | 2023 | Message-driven generation | Full message recovery [[1]](https://arxiv.org/abs/2312.01284) |

**State of the art:** Introduces message accuracy metric evaluating entirety of decoded messages; uses latent-aware encoding with Stable Diffusion.

**Production readiness:** Research
arXiv preprint December 2023; academic prototype only.

**Security status:** Caution — Focuses on message accuracy and image quality; steganalysis resistance not primary evaluation

**Community acceptance:** Emerging — Proposes novel holistic evaluation metric for generative steganography

---

### DKiS (Decay weight Invertible image Steganography)

**Goal:** Private key-based image steganography with decay weight mechanism.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **DKiS** | 2023 | Invertible network | Private key security [[1]](https://arxiv.org/abs/2311.18243) |

**State of the art:** First high-capacity invertible steganography with private key; decay weight mechanism controls information transfer from secret to host pipeline.

**Production readiness:** Research
arXiv November 2023; published in Neural Networks (Elsevier) 2025; code available.

**Implementations:**
- [DKiS](https://github.com/yanghangAI/DKiS) ⭐ 7 — PyTorch, official implementation

**Security status:** Secure — Private key required for extraction; decay weight filters out irrelevant information leakage

**Community acceptance:** Emerging — Published in Neural Networks journal; introduces key-based security to invertible steganography

---

### PRIS (Practical Robust Invertible Network for Image Steganography)

**Goal:** Robust and invertible network for image steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **PRIS** | 2023 | Invertible network | Robust + invertible [[1]](https://arxiv.org/abs/2309.13620) |

**State of the art:** Combines robustness with reversibility; addresses rounding error (ignored by existing methods) via gradient approximation function (GAF); published in Engineering Applications of AI.

**Production readiness:** Research
arXiv September 2023; published in Engineering Applications of Artificial Intelligence (Elsevier) 2024; code available.

**Implementations:**
- [PRIS](https://github.com/yanghangAI/PRIS) ⭐ 46 — PyTorch, official implementation

**Security status:** Caution — Focuses on robustness against distortions (Gaussian noise, lossy compression); steganalysis resistance not primary goal

**Community acceptance:** Emerging — Journal-published; outperforms state-of-the-art in robustness benchmarks

---

### Multi-User Multi-Key Image Steganography

**Goal:** Image steganography with key isolation for multi-user scenarios.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Multi-User Multi-Key** | 2026 | Unified network with key isolation | Selective hidden content reveal [[1]](https://arxiv.org/abs/2603.23005) |

**State of the art:** Enables different authorized users to extract different hidden contents from the same stego image; extends PUSNet paradigm.

**Production readiness:** Research
arXiv March 2026; 6-page conference paper; academic prototype only.

**Security status:** Secure — Key isolation ensures different users cannot access each other's hidden content

**Community acceptance:** Emerging — Novel multi-user access control for steganography; addresses real-world multi-party use cases

---

### StegaPos

**Goal:** Prevent unwanted image crops and replacements by embedding imperceptible positional signatures.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **StegaPos** | 2021 | Learned encoder/decoder CNN | Anti-tampering watermarking [[1]](https://arxiv.org/abs/2104.12290) |

**State of the art:** Embeds distinct positional signatures in every local image region. Detects crops, splices, and inpainting by identifying inconsistencies in hidden positional signatures.

**Production readiness:** Research
arXiv April 2021 (updated December 2022); academic prototype only.

**Security status:** Caution — Designed for tamper detection, not covert communication; positional signatures detectable if steganalysis is applied

**Community acceptance:** Emerging — Useful for image authentication and provenance verification

---

### Rethinking Security of Diffusion-based Generative Steganography

**Goal:** Analyze and improve security of diffusion model-based generative image steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Rethinking Security of DM-GIS** | 2026 | Diffusion model analysis | Security enhancement [[1]](https://arxiv.org/abs/2602.10219) |

**State of the art:** Identifies vulnerabilities in existing DM-GIS methods and proposes improvements.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Caution — Known vulnerabilities identified

**Community acceptance:** Emerging

---

### Intelligent Carrier Allocation

**Goal:** Cross-modal reasoning framework for adaptive multimodal steganography.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Intelligent Carrier Allocation** | 2025 | Cross-modal reasoning | Adaptive carrier selection [[1]](https://arxiv.org/abs/2511.09552) |

**State of the art:** Uses AI reasoning to select optimal carrier media for different message types.

**Production readiness:** Experimental

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Secure Audio Embedding in Images

**Goal:** Hide audio files in images using nature-inspired optimization.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Secure Audio Embedding** | 2025 | LSB with Harris Hawks Optimization | Audio-in-image [[1]](https://arxiv.org/abs/2512.08299) |

**State of the art:** Uses HHO algorithm to optimize LSB embedding for audio in images.

**Production readiness:** Experimental

**Implementations:** Academic prototypes only

**Security status:** Caution — LSB-based methods are detectable

**Community acceptance:** Niche

---

### Deep Data Hiding for ICAO-Compliant Face Images

**Goal:** Embed data in ICAO-compliant face images while maintaining biometric standards.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **ICAO Data Hiding** | 2025 | Watermarking/steganography for biometric images | ICAO compliant [[1]](https://arxiv.org/abs/2508.19324) |

**State of the art:** Enables persistent verification without compromising ICAO compliance.

**Production readiness:** Experimental

**Implementations:** Academic prototypes only

**Security status:** Caution — Must maintain biometric standards

**Community acceptance:** Emerging

---

### Defending against Stegomalware

**Goal:** Protect deep neural networks from steganographic malware embedding.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Stegomalware Defense** | 2025 | Permutation symmetry defense | Corrupts embedded payloads [[1]](https://arxiv.org/abs/2509.20399) |

**State of the art:** Uses layer permutation to corrupt stegomalware payloads without accuracy loss.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure — Effective against state-of-the-art methods

**Community acceptance:** Emerging

---

### On the Possible Detectability of Image-in-Image Steganography

**Goal:** Analyze detectability of embedding one image inside another.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Image-in-Image Detectability** | 2026 | ICA-based detection | High embedding rate [[1]](https://arxiv.org/abs/2603.11876) |

**State of the art:** Shows embedding is identifiable by independent component analysis.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Caution — Easily detectable

**Community acceptance:** Emerging

---

### Robust Provably Secure Image Steganography via Latent Iterative Optimization

**Goal:** Robust and provably secure image steganography using latent-space iterative optimization.

| Algorithm | Year | Architecture | Note |
|-----------|------|--------------|------|
| **Latent Iterative Optimization** | 2026 | Latent-space iterative refinement | Robust message extraction [[1]](https://arxiv.org/abs/2603.09348) |

**State of the art:** Improves message extraction accuracy through iterative latent refinement.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure — Provably secure framework

**Community acceptance:** Emerging

## Recent arXiv Papers (2024–2026)

---

### An Additive Approximation Scheme for Generating Dyadic Codings for the Outputs of an LLM

**Goal:** the constant-rate regime.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Additive Approximation Scheme for Generating Dyadic Codin** | 2026 | cs.IT, cs.DS | Daniella Bar-Lev, Farzad Farnoud, Ryan Gabrys [[1]](https://arxiv.org/abs/2605.05837) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Toward Accountable AI-Generated Content on Social Platforms: Steganographic Attribution and Multimodal Harm Detection

**Goal:** undermines the traditional moderation framework and complicates attribution, as synthetic images typically lack persistent metadata or device signatures.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Toward Accountable AI-Generated Content on Social Platforms:** | 2026 | cs.CV, cs.AI, cs.CR | Xinlei Guan et al. [[1]](https://arxiv.org/abs/2604.10460) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Invisible Safety Threat: Malicious Finetuning for LLM via Steganography

**Goal:** Understanding and addressing potential safety alignment risks in large language models (LLMs) is critical for ensuring their safe and trustworthy deployment.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invisible Safety Threat: Malicious Finetuning for LLM via St** | 2026 | cs.LG | Guangnian Wan et al. [[1]](https://arxiv.org/abs/2603.08104) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### : Towards Semantic Steganography via Large Language Models

**Goal:** Despite remarkable progress in steganography, embedding semantically rich, sentence-level information into carriers remains a challenging problem.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **: Towards Semantic Steganography via Large Language Models** | 2026 | cs.CV, cs.CR | Huanqi Wu et al. [[1]](https://arxiv.org/abs/2511.05319) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Training-Free Color-Aware Adversarial Diffusion Sanitization for Diffusion Stegomalware Defense at Security Gateways

**Goal:** The rapid expansion of generative AI has normalized large-scale synthetic media creation, enabling new forms of covert communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Training-Free Color-Aware Adversarial Diffusion Sanitization** | 2025 | cs.CR, cs.CV | Vladimir Frants, Sos Agaian [[1]](https://arxiv.org/abs/2512.24499) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Frobenius Revivals in Laplacian Cellular Automata: Chaos, Replication, and Reversible Encoding

**Goal:** based on chaotic transients and Frobenius returns, together with practical separation conditions and noise-tolerance estimates.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Frobenius Revivals in Laplacian Cellular Automata: Chaos, Re** | 2025 | nlin.CG, cs.IT, math.DS | Małgorzata Nowak-Kępczyk [[1]](https://arxiv.org/abs/2511.17389) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Reasoning Models Sometimes Output Illegible Chains of Thought

**Goal:** - suggesting the relationship is more nuanced.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Reasoning Models Sometimes Output Illegible Chains of Though** | 2025 | cs.LG | Arun Jose [[1]](https://arxiv.org/abs/2510.27338) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Concrete Roadmap towards Safety Cases based on Chain-of-Thought Monitoring

**Goal:** by CoT monitoring. We systematically examine two threats to monitorability: neuralese and encoded reasoning, which we categorize into three forms (linguistic drift, steganography, and alien reasoni...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Concrete Roadmap towards Safety Cases based on Chain-of-Th** | 2025 | cs.LG, cs.AI | Julian Schulz [[1]](https://arxiv.org/abs/2510.19476) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### All Code, No Thought: Current Language Models Struggle to Reason in Ciphered Language

**Goal:** Detecting harmful AI actions is important as AI agents gain adoption.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **All Code, No Thought: Current Language Models Struggle to Re** | 2025 | cs.CL, cs.AI, cs.LG | Shiyuan Guo, Henry Sleight, Fabien Roger [[1]](https://arxiv.org/abs/2510.09714) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### ZK-WAGON: Imperceptible Watermark for Image Generation Models using ZK-SNARKs

**Goal:** into a circuit, reducing proof generation time significantly.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ZK-WAGON: Imperceptible Watermark for Image Generation Model** | 2025 | cs.CR, cs.AI, cs.CV | Aadarsh Anantha Ramakrishnan et al. [[1]](https://arxiv.org/abs/2510.01967) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegOT: Trade-offs in Steganography via Optimal Transport

**Goal:** Image hiding is often referred to as steganography, which aims to hide a secret image in a cover image of the same resolution.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegOT: Trade-offs in Steganography via Optimal Transport** | 2025 | cs.CV, cs.AI | Chengde Lin et al. [[1]](https://arxiv.org/abs/2509.11178) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Technical Review on Comparison and Estimation of Steganographic Tools

**Goal:** Steganography is technique of hiding a data under cover media using different

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Technical Review on Comparison and Estimation of Steganogr** | 2025 | cs.CR, cs.CV, cs.GR | Ms. Preeti P. Bhatt, Rakesh R. Savant [[1]](https://arxiv.org/abs/2508.19323) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Joint Lossless Compression and Steganography for Medical Images via Large Language Models

**Goal:** often overlook the security of the compression process, which is critical in modern medical scenarios.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Joint Lossless Compression and Steganography for Medical Ima** | 2025 | eess.IV, cs.CV | Pengcheng Zheng et al. [[1]](https://arxiv.org/abs/2508.01782) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Feature Prediction in Quantum Graph Recurrent Neural Networks with Applications in Information Hiding

**Goal:** QGRNNs for both classical data processing and secure information hiding, paving the way for quantum-enhanced feature extraction, privacy-preserving computations, and quantum steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Feature Prediction in Quantum Graph Recurrent Neural Network** | 2025 | cs.CR | Jawaher Kaldari, Saif Al-Kuwari [[1]](https://arxiv.org/abs/2506.23144) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Large language models can learn and generalize steganographic chain-of-thought under process supervision

**Goal:** the reliability of CoT monitoring.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Large language models can learn and generalize steganographi** | 2025 | cs.AI, cs.CL, cs.LG | Joey Skaf et al. [[1]](https://arxiv.org/abs/2506.01926) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Implicit Jailbreak Attacks via Cross-Modal Information Concealment on Vision-Language Models

**Goal:** and block. In this work, we propose a novel implicit jailbreak framework termed IJA that stealthily embeds malicious instructions into images via least significant bit steganography and couples the...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Implicit Jailbreak Attacks via Cross-Modal Information Conce** | 2025 | cs.LG | Zhaoxin Wang et al. [[1]](https://arxiv.org/abs/2505.16446) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Quantum steganography using catalytic and entanglement-assisted quantum codes

**Goal:** Steganography is the technique for transmitting a secret message by employing subterfuge to conceal it in innocent-looking data, rather than by overt security measures as in cryptography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Quantum steganography using catalytic and entanglement-assis** | 2025 | cs.CR | Sanjoy Dutta et al. [[1]](https://arxiv.org/abs/2505.15869) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Shackled Dancing: A Bit-Locked Diffusion Algorithm for Lossless and Controllable Image Steganography

**Goal:** Data steganography aims to conceal information within visual content, yet existing spatial- and frequency-domain approaches suffer from trade-offs between security, capacity, and perceptual quality.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Shackled Dancing: A Bit-Locked Diffusion Algorithm for Lossl** | 2025 | cs.LG | Tianshuo Zhang et al. [[1]](https://arxiv.org/abs/2505.10950) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### CLPSTNet: A Progressive Multi-Scale Convolutional Steganography Model Integrating Curriculum Learning

**Goal:** In recent years, a large number of works have introduced Convolutional Neural Networks (CNNs) into image steganography, which transform traditional steganography methods such as hand-crafted featur...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CLPSTNet: A Progressive Multi-Scale Convolutional Steganogra** | 2025 | cs.CV, cs.AI, cs.CR | Fengchun Liu, Tong Zhang, Chunying Zhang [[1]](https://arxiv.org/abs/2504.16364) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Fragile Watermarking for Image Certification Using Deep Steganographic Embedding

**Goal:** content to detect and categorize the type of manipulation applied.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Fragile Watermarking for Image Certification Using Deep Steg** | 2025 | cs.CV, cs.LG | Davide Ghiani et al. [[1]](https://arxiv.org/abs/2504.13759) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Big Brother is Watching: Proactive Deepfake Detection via Learnable Hidden Face

**Goal:** methods, we explore a novel detection framework based on the concept of ``hiding a learnable face within a face''.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Big Brother is Watching: Proactive Deepfake Detection via Le** | 2025 | cs.CV | Hongbo Li et al. [[1]](https://arxiv.org/abs/2504.11309) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Parasite: A Steganography-based Backdoor Attack Framework for Diffusion Models

**Goal:** these limitations, we propose a novel backdoor attack method called "Parasite" for image-to-image tasks in diffusion models, which not only is the first to leverage steganography for triggers hidin...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Parasite: A Steganography-based Backdoor Attack Framework fo** | 2025 | cs.CV, cs.AI | Jiahao Chen et al. [[1]](https://arxiv.org/abs/2504.05815) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### RoSMM: A Robust and Secure Multi-Modal Watermarking Framework for Diffusion Models

**Goal:** Current image watermarking technologies are predominantly categorized into text watermarking techniques and image steganography; however, few methods can simultaneously handle text and image-based ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **RoSMM: A Robust and Secure Multi-Modal Watermarking Framewor** | 2025 | cs.MM | ZhongLi Fang, Yu Xie, Ping Chen [[1]](https://arxiv.org/abs/2504.02640) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Towards Secure Semantic Communications in the Presence of Intelligent Eavesdroppers

**Goal:** potentially arousing their suspicion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Secure Semantic Communications in the Presence of In** | 2025 | cs.IT, eess.IV, eess.SP | Shunpu Tang et al. [[1]](https://arxiv.org/abs/2503.23103) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### ImF: Implicit Fingerprint for Large Language Models

**Goal:** conditions. To advance the state-of-the-art in model fingerprinting, we propose a novel model fingerprint paradigm called Implicit Fingerprints (ImF).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ImF: Implicit Fingerprint for Large Language Models** | 2025 | cs.CL, cs.AI | Jiaxuan Wu et al. [[1]](https://arxiv.org/abs/2503.21805) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Images in Diffusion Models by Editing Learned Score Functions

**Goal:** Hiding data using neural networks (i.e., neural steganography) has achieved remarkable success across both discriminative classifiers and generative adversarial networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Images in Diffusion Models by Editing Learned Score F** | 2025 | cs.CV | Haoyu Chen et al. [[1]](https://arxiv.org/abs/2503.18459) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Quantum Direct Steganography Scheme Based on Modified Generator Projection Directions of Steane Code over a Single-Type Pauli Channel

**Goal:** code), as a fundamental carrier, we develop a novel scheme for direct quantum steganography across a single-type Pauli channel.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Quantum Direct Steganography Scheme Based on Modified Genera** | 2025 | cs.CR | Chaolong Hao et al. [[1]](https://arxiv.org/abs/2501.07578) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Adaptive 3D Mesh Steganography Based on Feature-Preserving Distortion

**Goal:** Current 3D mesh steganography algorithms relying on geometric modification are prone to detection by steganalyzers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Adaptive 3D Mesh Steganography Based on Feature-Preserving D** | 2025 | cs.MM | Yushu Zhang et al. [[1]](https://arxiv.org/abs/2209.08884) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Provably Secure Robust Image Steganography via Cross-Modal Error Correction

**Goal:** of image generation models has facilitated the widespread dissemination of generated images on social networks, creating favorable conditions for provably secure image steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Provably Secure Robust Image Steganography via Cross-Modal E** | 2024 | cs.MM, cs.CR, cs.CV | Yuang Qi et al. [[1]](https://arxiv.org/abs/2412.12206) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Approach to Image Steganography Using Generative Adversarial Networks

**Goal:** The field of steganography has long been focused on developing methods to securely embed information within various digital media while ensuring imperceptibility and robustness.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Approach to Image Steganography Using Generative Adv** | 2024 | cs.CR, cs.CV, cs.LG | Waheed Rehman [[1]](https://arxiv.org/abs/2412.00094) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Facial Features Matter: a Dynamic Watermark based Proactive Deepfake Detection Approach

**Goal:** features to watermarks, enhancing protection against various reverse inference attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Facial Features Matter: a Dynamic Watermark based Proactive ** | 2024 | cs.CV, cs.CR, cs.LG | Shulin Lan et al. [[1]](https://arxiv.org/abs/2411.14798) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Magnetic steganography based on wide field diamond quantum microscopy

**Goal:** We experimentally demonstrate magnetic steganography using wide field quantum microscopy based on diamond nitrogen vacancy centers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Magnetic steganography based on wide field diamond quantum m** | 2024 | cs.CR | Jungbae Yoon et al. [[1]](https://arxiv.org/abs/2411.12243) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Neural Cover Selection for Image Steganography

**Goal:** In steganography, selecting an optimal cover image, referred to as cover selection, is pivotal for effective message concealment.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Neural Cover Selection for Image Steganography** | 2024 | cs.AI | Karl Chahine, Hyeji Kim [[1]](https://arxiv.org/abs/2410.18216) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### IWN: Image Watermarking Based on Idempotency

**Goal:** balance between embedding capacity and robustness, alleviating to some extent the inherent contradiction between these two factors in traditional watermarking techniques and steganography methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **IWN: Image Watermarking Based on Idempotency** | 2024 | cs.MM, cs.CV | Kaixin Deng [[1]](https://arxiv.org/abs/2409.19506) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganographic Entanglement Sharing

**Goal:** In a previous work we have discussed a theoretical grounding for classical steganography using quantum Fock and coherent states in an optical channel, building on previous work by Wu et al.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganographic Entanglement Sharing** | 2024 | cs.CR | Bruno Avritzer, Todd A. Brun [[1]](https://arxiv.org/abs/2409.09335) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Robust Message Embedding via Attention Flow-Based Steganography

**Goal:** Image steganography can hide information in a host image and obtain a stego image that is perceptually indistinguishable from the original one.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Robust Message Embedding via Attention Flow-Based Steganogra** | 2024 | cs.CV | Huayuan Ye et al. [[1]](https://arxiv.org/abs/2405.16414) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Diffusion-Based Hierarchical Image Steganography

**Goal:** This paper introduces Hierarchical Image Steganography, a novel method that enhances the security and capacity of embedding multiple images into a single container using diffusion models.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Diffusion-Based Hierarchical Image Steganography** | 2024 | cs.CV | Youmin Xu et al. [[1]](https://arxiv.org/abs/2405.11523) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### High Fidelity Artificial Quantum Thermal State Generation using Encoded Coherent States

**Goal:** Quantum steganography is a powerful method for information security where communications between a sender and receiver are disguised as naturally occurring noise in a channel.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **High Fidelity Artificial Quantum Thermal State Generation us** | 2024 | cs.CR | Haley Weinstein et al. [[1]](https://arxiv.org/abs/2405.03881) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegoGAN: Leveraging Steganography for Non-Bijective Image-to-Image Translation

**Goal:** images. CycleGAN-based methods are also known to hide the mismatched information in the generated images to bypass cycle consistency objectives, a process known as steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegoGAN: Leveraging Steganography for Non-Bijective Image-t** | 2024 | cs.CV, eess.IV | Sidi Wu et al. [[1]](https://arxiv.org/abs/2403.20142) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Enhancing Steganographic Text Extraction: Evaluating the Impact of NLP Models on Accuracy and Semantic Coherence

**Goal:** This study discusses a new method combining image steganography technology with Natural Language Processing (NLP) large models, aimed at improving the accuracy and robustness of extracting steganog...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Enhancing Steganographic Text Extraction: Evaluating the Imp** | 2024 | cs.CV, cs.AI, cs.CL | Mingyang Li et al. [[1]](https://arxiv.org/abs/2402.18849) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Transparency Attacks: How Imperceptible Image Layers Can Fool AI Perception

**Goal:** AI misinterpretation of what the human eye perceives.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Transparency Attacks: How Imperceptible Image Layers Can Foo** | 2024 | cs.CV, cs.CR, cs.LG | Forrest McKee, David Noever [[1]](https://arxiv.org/abs/2401.15817) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Null Space Properties of Neural Networks with Applications to Image Steganography

**Goal:** can use it to trick the neural network.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Null Space Properties of Neural Networks with Applications t** | 2023 | cs.CV, cs.AI, cs.CR | Xiang Li, Kevin M. Short [[1]](https://arxiv.org/abs/2401.10262) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### EditGuard: Versatile Image Watermarking for Tamper Localization and Copyright Protection

**Goal:** embedding of imperceptible watermarks and precise decoding of tampered areas and copyright information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **EditGuard: Versatile Image Watermarking for Tamper Localizat** | 2023 | cs.CV | Xuanyu Zhang et al. [[1]](https://arxiv.org/abs/2312.08883) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### THInImg: Cross-modal Steganography for Presenting Talking Heads in Images

**Goal:** Cross-modal Steganography is the practice of concealing secret signals in publicly available cover signals (distinct from the modality of the secret signals) unobtrusively.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **THInImg: Cross-modal Steganography for Presenting Talking He** | 2023 | cs.CV | Lin Zhao et al. [[1]](https://arxiv.org/abs/2311.17177) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### GhostEncoder: Stealthy Backdoor Attacks with Dynamic Triggers to Pre-trained Encoders in Self-supervised Learning

**Goal:** the first dynamic invisible backdoor attack on SSL.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **GhostEncoder: Stealthy Backdoor Attacks with Dynamic Trigger** | 2023 | cs.CV, cs.CR | Qiannan Wang et al. [[1]](https://arxiv.org/abs/2310.00626) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Invertible Mosaic Image Hiding Network for Very Large Capacity Image Steganography

**Goal:** The existing image steganography methods either sequentially conceal secret images or conceal a concatenation of multiple images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invertible Mosaic Image Hiding Network for Very Large Capaci** | 2023 | cs.MM | Zihan Chen et al. [[1]](https://arxiv.org/abs/2309.08987) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Focus on Content not Noise: Improving Image Generation for Nuclei Segmentation by Suppressing Steganography in CycleGAN

**Goal:** in high frequencies rather than encoding the desired image content and learning the target task.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Focus on Content not Noise: Improving Image Generation for N** | 2023 | eess.IV, cs.CV | Jonas Utz et al. [[1]](https://arxiv.org/abs/2308.01769) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Semi-supervised Cycle-GAN for face photo-sketch translation in the wild

**Goal:** settings. Such paired datasets are, however, often very small and lack diversity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Semi-supervised Cycle-GAN for face photo-sketch translation ** | 2023 | cs.CV | Chaofeng Chen et al. [[1]](https://arxiv.org/abs/2307.10281) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StyleStegan: Leak-free Style Transfer Based on Feature Steganography

**Goal:** thereby hindering the further propagation of stylized images in social networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StyleStegan: Leak-free Style Transfer Based on Feature Stega** | 2023 | cs.CV, cs.MM | Xiujian Liang et al. [[1]](https://arxiv.org/abs/2307.00225) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Diffusion-Stego: Training-free Diffusion Generative Steganography via Message Projection

**Goal:** Generative steganography is the process of hiding secret messages in generated images instead of cover images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Diffusion-Stego: Training-free Diffusion Generative Steganog** | 2023 | cs.CV | Daegyu Kim et al. [[1]](https://arxiv.org/abs/2305.18726) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generative Steganographic Flow

**Goal:** Generative steganography (GS) is a new data hiding manner, featuring direct generation of stego media from secret data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generative Steganographic Flow** | 2023 | cs.CV, cs.MM | Ping Wei et al. [[1]](https://arxiv.org/abs/2305.05838) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generative Steganography Diffusion

**Goal:** Generative steganography (GS) is an emerging technique that generates stego images directly from secret data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generative Steganography Diffusion** | 2023 | cs.MM, cs.AI | Ping Wei et al. [[1]](https://arxiv.org/abs/2305.03472) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Robust image steganography against lossy JPEG compression based on embedding domain selection and adaptive error correction

**Goal:** Transmitting images for communication on social networks has become routine, which is helpful for covert communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Robust image steganography against lossy JPEG compression ba** | 2023 | cs.MM | Xiaolong Duan et al. [[1]](https://arxiv.org/abs/2304.13297) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### RoSteALS: Robust Steganography using Autoencoder Latent Space

**Goal:** Data hiding such as steganography and invisible watermarking has important applications in copyright protection, privacy-preserved communication and content provenance.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **RoSteALS: Robust Steganography using Autoencoder Latent Spac** | 2023 | cs.CV | Tu Bui et al. [[1]](https://arxiv.org/abs/2304.03400) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Learning Iterative Neural Optimizers for Image Steganography

**Goal:** Image steganography is the process of concealing secret information in images through imperceptible changes.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Learning Iterative Neural Optimizers for Image Steganography** | 2023 | eess.IV, cs.CV, cs.MM | Xiangyu Chen, Varsha Kishore, Kilian Q Weinberger [[1]](https://arxiv.org/abs/2303.16206) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Low-frequency Image Deep Steganography: Manipulate the Frequency Distribution to Hide Secrets with Tenacious Robustness

**Goal:** Image deep steganography (IDS) is a technique that utilizes deep learning to embed a secret image invisibly into a cover image to generate a container image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Low-frequency Image Deep Steganography: Manipulate the Frequ** | 2023 | cs.CR, cs.CV | Huajie Chen et al. [[1]](https://arxiv.org/abs/2303.13713) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Towards Robust Image-in-Audio Deep Steganography

**Goal:** The field of steganography has experienced a surge of interest due to the recent advancements in AI-powered techniques, particularly in the context of multimodal setups that enable the concealment ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Robust Image-in-Audio Deep Steganography** | 2023 | cs.CR, cs.CV, cs.MM | Jaume Ros et al. [[1]](https://arxiv.org/abs/2303.05007) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Artistic Curve Steganography Carried by Musical Audio

**Goal:** In this work, we create artistic closed loop curves that trace out images and 3D shapes, which we then hide in musical audio as a form of steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Artistic Curve Steganography Carried by Musical Audio** | 2023 | cs.SD, cs.IR, cs.MM | Christopher J. Tralie [[1]](https://arxiv.org/abs/2301.12354) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Invisible Backdoor Attack with Dynamic Triggers against Person Re-identification

**Goal:** an identity hashing network is proposed to first extract target identity information from a reference image, which is then injected into the benign images by image steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invisible Backdoor Attack with Dynamic Triggers against Pers** | 2023 | cs.CV, cs.CR | Wenli Sun et al. [[1]](https://arxiv.org/abs/2211.10933) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Errorless Robust JPEG Steganography using Outputs of JPEG Coders

**Goal:** Robust steganography is a technique of hiding secret messages in images so that the message can be recovered after additional image processing.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Errorless Robust JPEG Steganography using Outputs of JPEG Co** | 2023 | cs.MM, cs.CR, eess.IV | Jan Butora, Pauline Puteaux, Patrick Bas [[1]](https://arxiv.org/abs/2211.04750) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Data Hiding with Deep Learning: A Survey Unifying Digital Watermarking and Steganography

**Goal:** through the use of deep learning techniques for data hiding.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Data Hiding with Deep Learning: A Survey Unifying Digital Wa** | 2023 | cs.CV | Zihan Wang et al. [[1]](https://arxiv.org/abs/2107.09287) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Robust Image Steganographic Scheme against General Scaling Attacks

**Goal:** schemes are generally vulnerable to active attacks, e.g., JPEG re-compression, scaling, as seen on social networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Robust Image Steganographic Scheme against General Scaling** | 2022 | cs.MM | Qingliang Liu et al. [[1]](https://arxiv.org/abs/2212.02822) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Applications of single-photon technology

**Goal:** metrology, and further development of quantum computers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Applications of single-photon technology** | 2022 | cs.CR | Marta Misiaszek-Schreyner [[1]](https://arxiv.org/abs/2205.10221) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### FaceSigns: Semi-Fragile Neural Watermarks for Media Authentication and Countering Deepfakes

**Goal:** studied in our work, FaceSigns can reliably detect manipulated content with an AUC score of 0.996 which is significantly higher than prior image watermarking and steganography techniques.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **FaceSigns: Semi-Fragile Neural Watermarks for Media Authenti** | 2022 | cs.CV, cs.AI, stat.ML | Paarth Neekhara et al. [[1]](https://arxiv.org/abs/2204.01960) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography based on Style Transfer

**Goal:** Image steganography is the art and science of using images as cover for covert communications.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography based on Style Transfer** | 2022 | cs.CV, cs.CR | Donghui Hu et al. [[1]](https://arxiv.org/abs/2203.04500) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Survey on Patients Privacy Protection with Stganography and Visual Encryption

**Goal:** In this survey, thirty models for steganography and visual encryption methods have been discussed to provide patients privacy protection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Survey on Patients Privacy Protection with Stganography an** | 2022 | cs.CV, cs.MM | Hussein K. Alzubaidy, Dhiah Al-Shammary, Mohammed Hamzah Abed [[1]](https://arxiv.org/abs/2201.09388) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint stage; community evaluation ongoing.

---

### Improving Performance of Semantic Segmentation CycleGANs by Noise Injection into the Latent Segmentation Space

**Goal:** we combine semantic segmentation with the concept of cycle consistency to enable a multitask training protocol.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improving Performance of Semantic Segmentation CycleGANs by ** | 2022 | cs.CV, eess.IV | Jonas Löhdefink, Tim Fingscheidt [[1]](https://arxiv.org/abs/2201.06415) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Adaptive Steganography Based on bargain Game

**Goal:** The capacity and security of the confidential message on the channel are two important challenges in steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Adaptive Steganography Based on bargain Game** | 2022 | cs.MM, math.OC | Behbod Keshavarzi et al. [[1]](https://arxiv.org/abs/2111.04653) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### "Robot Steganography"?: Opportunities and Challenges

**Goal:** to communicate with people in various public and domestic venues in a helpful, discreet way.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **"Robot Steganography"?: Opportunities and Challenges** | 2022 | cs.RO | Martin Cooney, Eric Järpe, Alexey Vinel [[1]](https://arxiv.org/abs/2108.00998) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Color Image Steganography Based on Frequency Sub-band Selection

**Goal:** Color image steganography based on deep learning is the art of hiding information in the color image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Color Image Steganography Based on Frequency Sub-band Sele** | 2021 | cs.CR, cs.CV | Hai Su et al. [[1]](https://arxiv.org/abs/2112.14437) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image quality enhancement of embedded holograms in holographic information hiding using deep neural networks

**Goal:** Holographic information hiding is a technique for embedding holograms or images into another hologram, used for copyright protection and steganography of holograms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image quality enhancement of embedded holograms in holograph** | 2021 | cs.CV, cs.GR | Tomoyoshi Shimobaba et al. [[1]](https://arxiv.org/abs/2112.11246) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Pixel-Stega: Generative Image Steganography Based on Autoregressive Models

**Goal:** In this letter, we explored generative image steganography based on autoregressive models.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Pixel-Stega: Generative Image Steganography Based on Autoreg** | 2021 | cs.CV | Siyu Zhang et al. [[1]](https://arxiv.org/abs/2112.10945) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Interpretable Privacy Preservation of Text Representations Using Vector Steganography

**Goal:** Contextual word representations generated by language models (LMs) learn spurious associations present in the training corpora.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Interpretable Privacy Preservation of Text Representations U** | 2021 | cs.CL, cs.AI | Geetanjali Bihani [[1]](https://arxiv.org/abs/2112.02557) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Multitask Identity-Aware Image Steganography via Minimax Optimization

**Goal:** High-capacity image steganography, aimed at concealing a secret image in a cover image, is a technique to preserve sensitive data, e.g., faces and fingerprints.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Multitask Identity-Aware Image Steganography via Minimax Opt** | 2021 | cs.CV | Jiabao Cui et al. [[1]](https://arxiv.org/abs/2107.05819) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Pixel identification in an image using Grover Search Algorithm

**Goal:** into a quantum state and then running the Grover algorithm for identifying the pixel with 0 value maximum gray-scale intensity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Pixel identification in an image using Grover Search Algorit** | 2021 | cs.CR | Mohd. Hussain Mir, Harkirat Singh [[1]](https://arxiv.org/abs/2107.03039) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Improving Cost Learning for JPEG Steganography by Exploiting JPEG Domain Knowledge

**Goal:** Although significant progress in automatic learning of steganographic cost has been achieved recently, existing methods designed for spatial images are not well applicable to JPEG images which are ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improving Cost Learning for JPEG Steganography by Exploiting** | 2021 | cs.CR, cs.CV | Weixuan Tang et al. [[1]](https://arxiv.org/abs/2105.03867) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Universal Adversarial Perturbations Through the Lens of Deep Steganography: Towards A Fourier Perspective

**Goal:** universal adversarial perturbation (UAP), can be generated to fool the DNN for most images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Universal Adversarial Perturbations Through the Lens of Deep** | 2021 | cs.LG, cs.CV | Chaoning Zhang et al. [[1]](https://arxiv.org/abs/2102.06479) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### CSIS: compressed sensing-based enhanced-embedding capacity image steganography scheme

**Goal:** Image steganography plays a vital role in securing secret data by embedding it in the cover images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CSIS: compressed sensing-based enhanced-embedding capacity i** | 2021 | cs.MM, math.OC | Rohit Agrawal, Kapil Ahuja [[1]](https://arxiv.org/abs/2101.00690) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Multi-Image Steganography Using Deep Neural Networks

**Goal:** Steganography is the science of hiding a secret message within an ordinary public message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Multi-Image Steganography Using Deep Neural Networks** | 2021 | cs.CV | Abhishek Das et al. [[1]](https://arxiv.org/abs/2101.00350) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### FoolHD: Fooling speaker identification by Highly imperceptible adversarial Disturbances

**Goal:** models are vulnerable to carefully designed adversarial perturbations of their input signals that induce misclassification.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **FoolHD: Fooling speaker identification by Highly imperceptib** | 2021 | cs.SD, cs.LG, eess.AS | Ali Shahin Shamsabadi et al. [[1]](https://arxiv.org/abs/2011.08483) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### New Design Paradigm of Distortion Cost Function for Efficient JPEG Steganography

**Goal:** change, where the pixel embedding distortion costs are represented in a more general exponential model, aiming to flexibly allocate the embedding data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **New Design Paradigm of Distortion Cost Function for Efficien** | 2021 | cs.MM | Wenkang Su et al. [[1]](https://arxiv.org/abs/1908.01947) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generative Steganography with Kerckhoffs' Principle

**Goal:** The distortion in steganography that usually comes from the modification or recoding on the cover image during the embedding process leaves the steganalyzer with possibility of discriminating.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generative Steganography with Kerckhoffs' Principle** | 2021 | cs.MM | Yan Ke et al. [[1]](https://arxiv.org/abs/1711.04916) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Painting with Hue, Saturation, and Brightness Control by Nanoscale 3D Printing

**Goal:** 3D printing. We extend our understanding of the scattering properties of the low-refractive-index nanopillar to demonstrate grayscale inversion and colour desaturation, with steganography at the le...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Painting with Hue, Saturation, and Brightness Control by Nan** | 2020 | cs.CR | Hao Wang et al. [[1]](https://arxiv.org/abs/2010.11035) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Adversarial Images through Stega Glasses

**Goal:** This paper explores the connection between steganography and adversarial images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Adversarial Images through Stega Glasses** | 2020 | cs.CR, eess.IV, eess.SP | Benoît Bonnet, Teddy Furon, Patrick Bas [[1]](https://arxiv.org/abs/2010.07542) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Enabling optical steganography, data storage, and encryption with plasmonic colors

**Goal:** also enables the robust generation of dynamic kaleidoscopic images with no detrimental "cross-talk" effect.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Enabling optical steganography, data storage, and encryption** | 2020 | cs.CR | Maowen Song et al. [[1]](https://arxiv.org/abs/2009.03521) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### \ell_1SABMIS: \ell_1-minimization and sparse approximation based blind multi-image steganography scheme

**Goal:** Steganography plays a vital role in achieving secret data security by embedding it into cover media.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **\ell_1SABMIS: \ell_1-minimization and sparse approximation b** | 2020 | cs.MM | Rohit Agrawal [[1]](https://arxiv.org/abs/2007.05025) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Secure Steganography Technique Based on Bitplane Indexes

**Goal:** This paper is concerned with secret hiding in multiple image bitplanes for increased security without undermining capacity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secure Steganography Technique Based on Bitplane Indexes** | 2020 | cs.MM | Alan Anwer Abdulla, Sabah A. Jassim, Harin Sellahewa [[1]](https://arxiv.org/abs/2004.12470) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Stego Quality Enhancement by Message Size Reduction and Fibonacci Bit-Plane Mapping

**Goal:** An efficient 2-step steganography technique is proposed to enhance stego image quality and secret message un-detectability.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stego Quality Enhancement by Message Size Reduction and Fibo** | 2020 | cs.MM | Alan A. Abdulla, Harin Sellahewa, Sabah A. Jassim [[1]](https://arxiv.org/abs/2004.12467) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Efficient High Capacity Steganography Technique

**Goal:** against active attacks aimed to destroy the secret message).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Efficient High Capacity Steganography Technique** | 2020 | cs.MM | Alan Anwer Abdulla, Sabah A. Jassim, Harin Sellahewa [[1]](https://arxiv.org/abs/2004.11984) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography Based on Pixel Intensity Value Decomposition

**Goal:** This paper focuses on steganography based on pixel intensity value decomposition.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography Based on Pixel Intensity Value Decomposition** | 2020 | cs.MM | Alan Anwer Abdulla, Harin Sellahewa, Sabah A. Jassim [[1]](https://arxiv.org/abs/2004.11977) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Improving embedding efficiency for digital steganography by exploiting similarities between secret and cover images

**Goal:** Digital steganography is becoming a common tool for protecting sensitive communications in various applications such as crime(terrorism) prevention whereby law enforcing personals need to remotely ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improving embedding efficiency for digital steganography by ** | 2020 | cs.MM | Alan A. Abdulla, Harin Sellahewa, Sabah A. Jassim [[1]](https://arxiv.org/abs/2004.11974) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Data hiding in speech signal using steganography and encryption

**Goal:** destination safely. Encryption is a simple yet effective way to protect our data while transmitting it to a destination.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Data hiding in speech signal using steganography and encrypt** | 2020 | cs.MM | Hanisha Chowdary N et al. [[1]](https://arxiv.org/abs/2002.02370) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Universal Stego Post-processing for Enhancing Image Steganography

**Goal:** that the designing or improving embedding cost becomes a key issue for current steganographic methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Universal Stego Post-processing for Enhancing Image Steganog** | 2020 | cs.MM | Bolin Chen et al. [[1]](https://arxiv.org/abs/1912.03878) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Invisible Backdoor Attacks on Deep Neural Networks via Steganography and Regularization

**Goal:** our invisible backdoors through two state-of-the-art methods of embedding triggers for backdoor attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invisible Backdoor Attacks on Deep Neural Networks via Stega** | 2020 | cs.CR, cs.CV, cs.LG | Shaofeng Li et al. [[1]](https://arxiv.org/abs/1909.02742) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Self-Contained Stylization via Steganography for Reverse and Serial Style Transfer

**Goal:** image and its stylized output.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Self-Contained Stylization via Steganography for Reverse and** | 2020 | cs.CV | Hung-Yu Chen, I-Sheng Fang, Wei-Chen Chiu [[1]](https://arxiv.org/abs/1812.03910) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Distribution-Preserving Steganography Based on Text-to-Speech Generative Models

**Goal:** Steganography is the art and science of hiding secret messages in public communication so that the presence of the secret messages cannot be detected.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Distribution-Preserving Steganography Based on Text-to-Speec** | 2020 | cs.MM | Kejiang Chen et al. [[1]](https://arxiv.org/abs/1811.03732) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Beyond Unfolding: Exact Recovery of Latent Convex Tensor Decomposition under Reshuffling

**Goal:** of the matrix into a tensor.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Beyond Unfolding: Exact Recovery of Latent Convex Tensor Dec** | 2020 | cs.LG, stat.ML | Chao Li et al. [[1]](https://arxiv.org/abs/1805.08465) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hide the Image in FC-DenseNets to another Image

**Goal:** In the past, steganography was to embed text in a carrier, the sender Alice and the recipient Bob share the key, and the text is extracted by Bob through the key.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hide the Image in FC-DenseNets to another Image** | 2019 | cs.MM, cs.CR, eess.IV | Duan Xintao, Liu Nao [[1]](https://arxiv.org/abs/1910.08341) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Enhancing JPEG Steganography using Iterative Adversarial Examples

**Goal:** literatures on computer vision have pointed out that those effective CNN-based methods can be easily fooled by adversarial examples.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Enhancing JPEG Steganography using Iterative Adversarial Exa** | 2019 | cs.MM | Huaxiao Mo et al. [[1]](https://arxiv.org/abs/1909.07556) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography Protocols for Quantum Channels

**Goal:** We study several versions of a quantum steganography problem, in which two legitimate parties attempt to conceal a cypher in a quantum cover transmitted over a quantum channel without arising suspi...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography Protocols for Quantum Channels** | 2019 | cs.IT | Mehrdad Tahmasbi, Matthieu Bloch [[1]](https://arxiv.org/abs/1907.09602) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### BASN -- Learning Steganography with Binary Attention Mechanism

**Goal:** in recent years with images' growing domination on the Internet and mobile applications.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **BASN -- Learning Steganography with Binary Attention Mechani** | 2019 | cs.CV, cs.MM | Yang Yang [[1]](https://arxiv.org/abs/1907.04362) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Recent Advances of Image Steganography with Generative Adversarial Networks

**Goal:** (GAN) which proposed in 2014 has achieved great success.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Recent Advances of Image Steganography with Generative Adver** | 2019 | cs.CR, cs.MM, eess.IV | Jia Liu et al. [[1]](https://arxiv.org/abs/1907.01886) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generative Reversible Data Hiding by Image to Image Translation via GANs

**Goal:** on cover image modification which inevitably leaves some traces of rewriting that can be more easily analyzed and attacked by the warder.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generative Reversible Data Hiding by Image to Image Translat** | 2019 | eess.IV, cs.CR, cs.MM | Zhuo Zhang et al. [[1]](https://arxiv.org/abs/1905.02872) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegoAppDB: a Steganography Apps Forensics Image Database

**Goal:** In this paper, we present a new reference dataset simulating digital evidence for image steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegoAppDB: a Steganography Apps Forensics Image Database** | 2019 | eess.IV, cs.MM | Jennifer Newman et al. [[1]](https://arxiv.org/abs/1904.09360) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Solving the large syndrome calculation problem in steganography

**Goal:** In error correction code based image steganography, embedding using large length codes have not been researched extensively.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Solving the large syndrome calculation problem in steganogra** | 2019 | cs.IT | Suah Kim, Vasily Sachnev, Hyoung Joong Kim [[1]](https://arxiv.org/abs/1904.05625) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A security steganography scheme based on hdr image

**Goal:** It is widely recognized that the image format is crucial to steganography for that each individual format has its unique properities.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A security steganography scheme based on hdr image** | 2019 | cs.CV | Wei Gao, Yongqing Huo, Yan Qiao [[1]](https://arxiv.org/abs/1902.10943) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### SteganoGAN: High Capacity Image Steganography with GANs

**Goal:** Image steganography is a procedure for hiding messages inside pictures.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SteganoGAN: High Capacity Image Steganography with GANs** | 2019 | cs.CV, cs.LG, cs.MM | Kevin Alex Zhang et al. [[1]](https://arxiv.org/abs/1901.03892) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Adaptive Spatial Steganography Based on Probability-Controlled Adversarial Examples

**Goal:** Explanation from Sai Ma: The experiments in this paper are conducted on Caffe framework.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Adaptive Spatial Steganography Based on Probability-Controll** | 2019 | cs.MM | Sai Ma et al. [[1]](https://arxiv.org/abs/1804.02691) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Emerging Applications of Reversible Data Hiding

**Goal:** and integrity authentication, recently some scholars begin to apply RDH in many other fields innovatively.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Emerging Applications of Reversible Data Hiding** | 2018 | cs.CV | Dongdong Hou et al. [[1]](https://arxiv.org/abs/1811.02928) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Combined Image Encryption and Steganography Algorithm in the Spatial Domain

**Goal:** In recent years, steganography has emerged as one of the main research areas in information security.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Combined Image Encryption and Steganography Algorithm in the** | 2018 | eess.IV, cs.MM | Aya H. S. Abdelgader, Raneem A. Aboughalia, Osama A. S. Alkishriwo [[1]](https://arxiv.org/abs/1810.05263) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Invisible Steganography via Generative Adversarial Networks

**Goal:** algorithms. These works have shown the improving potential of deep learning in information hiding domain.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invisible Steganography via Generative Adversarial Networks** | 2018 | cs.MM, cs.CV | Ru Zhang, Shiqi Dong, Jianyi Liu [[1]](https://arxiv.org/abs/1807.08571) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### High Capacity Image Data Hiding of Scanned Text Documents Using Improved Quadtree

**Goal:** In this paper, an effective method was introduced to steganography of text document in the host image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **High Capacity Image Data Hiding of Scanned Text Documents Us** | 2018 | cs.MM | Seyyed Hossein Soleymani, Amir Hossein Taherinia [[1]](https://arxiv.org/abs/1803.11286) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### The Cut and Dominating Set Problem in A Steganographer Network

**Goal:** entities such as the data encoders and data decoders, and the associated edges represent any real communicable channels or other social links that could be utilized for steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **The Cut and Dominating Set Problem in A Steganographer Netwo** | 2018 | cs.DS, cs.MM | Hanzhou Wu et al. [[1]](https://arxiv.org/abs/1802.09333) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Graph-theoretic Model to Steganography on Social Networks

**Goal:** Steganography aims to conceal the very fact that the communication takes place, by embedding a message into a digit object such as image without introducing noticeable artifacts.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Graph-theoretic Model to Steganography on Social Networks** | 2018 | cs.MM | Hanzhou Wu et al. [[1]](https://arxiv.org/abs/1712.03621) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### SSGAN: Secure Steganography Based on Generative Adversarial Networks

**Goal:** In this paper, a novel strategy of Secure Steganograpy based on Generative Adversarial Networks is proposed to generate suitable and secure covers for steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SSGAN: Secure Steganography Based on Generative Adversarial ** | 2018 | cs.CV, cs.MM | Haichao Shi et al. [[1]](https://arxiv.org/abs/1707.01613) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Encoding DNA sequences by integer chaos game representation

**Goal:** encode DNA sequences into numerical values of the same length.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Encoding DNA sequences by integer chaos game representation** | 2017 | cs.CE, bio.OT | Changchuan Yin [[1]](https://arxiv.org/abs/1712.04546) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### CycleGAN, a Master of Steganography

**Goal:** CycleGAN (Zhu et al.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **CycleGAN, a Master of Steganography** | 2017 | cs.CV, cs.LG, stat.ML | Casey Chu, Andrey Zhmoginov, Mark Sandler [[1]](https://arxiv.org/abs/1712.02950) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### End-to-end Trained CNN Encode-Decoder Networks for Image Steganography

**Goal:** All the existing image steganography methods use manually crafted features to hide binary payloads into cover images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **End-to-end Trained CNN Encode-Decoder Networks for Image Ste** | 2017 | cs.MM, cs.CV | Atique ur Rehman et al. [[1]](https://arxiv.org/abs/1711.07201) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Robust Data Hiding Process Contributing to the Development of a Semantic Web

**Goal:** steganographic scheme based on chaotic iterations is proposed.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Robust Data Hiding Process Contributing to the Development** | 2017 | cs.MM | Jacques M. Bahi et al. [[1]](https://arxiv.org/abs/1706.08764) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegIbiza: Steganography in Club Music Implemented in Python

**Goal:** This paper introduces the implementation of steganography method called StegIbiza, which uses tempo modulation as hidden message carrier.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegIbiza: Steganography in Club Music Implemented in Python** | 2017 | cs.MM | Krzysztof Szczypiorski, Wojciech Zydecki [[1]](https://arxiv.org/abs/1705.07788) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### FPGA Implementation of a Novel Image Steganography for Hiding Images

**Goal:** data flow systems and according infrastructure networks increases, the security of data transition through such platforms becomes more important.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **FPGA Implementation of a Novel Image Steganography for Hidin** | 2016 | cs.AR, cs.DC | Masoom Nazari et al. [[1]](https://arxiv.org/abs/1609.04569) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Enhanced Boolean Correlation Matrix Memory

**Goal:** shows that it is possible to improve the performance of Boolean CMM thanks BOP algorithm.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Enhanced Boolean Correlation Matrix Memory** | 2016 | cs.NE | Mario Mastriani [[1]](https://arxiv.org/abs/1607.04267) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Quantum Enhanced Correlation Matrix Memories via States Orthogonalisation

**Goal:** work shows that it is possible to improve the performance of QCMM thanks QOP algorithm.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Quantum Enhanced Correlation Matrix Memories via States Orth** | 2016 | cs.CR | Mario Mastriani, Marcelo Naiouf [[1]](https://arxiv.org/abs/1607.03106) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Can Machine Learn Steganography? - Implementing LSB Substitution and Matrix Coding Steganography with Feed-Forward Neural Networks

**Goal:** performance in many applications.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Can Machine Learn Steganography? - Implementing LSB Substitu** | 2016 | cs.MM | Han-Zhou Wu, Hong-Xia Wang, Yun-Qing Shi [[1]](https://arxiv.org/abs/1606.05294) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Optimal Binary Coding for q^+ -state Data Embedding

**Goal:** In steganography, we always hope to maximize the embedding payload subject to an upper-bounded distortion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Optimal Binary Coding for q^+ -state Data Embedding** | 2016 | cs.IT | Han-Zhou Wu [[1]](https://arxiv.org/abs/1604.03140) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Reading Between the Pixels: Photographic Steganography for Camera Display Messaging

**Goal:** We exploit human color metamers to send light-modulated messages less visible to the human eye, but recoverable by cameras.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Reading Between the Pixels: Photographic Steganography for C** | 2016 | cs.CV, cs.GR, cs.MM | Eric Wengrowski et al. [[1]](https://arxiv.org/abs/1604.01720) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Enhanced Edge Adaptive Steganography Approach Using Threshold Value for Region Selection

**Goal:** This paper attempts to improve the quality and the modification rate of a Stego Image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Enhanced Edge Adaptive Steganography Approach Using Thres** | 2016 | cs.MM | Sachin Mungmode, R. R. Sedamkar, Niranjan Kulkarni [[1]](https://arxiv.org/abs/1601.02076) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Image Steganographic Technique using Pattern based Bits Shuffling and Magic LSB for Grayscale Images

**Goal:** Image Steganography is a growing research area of information security where secret information is embedded in innocent-looking public communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Image Steganographic Technique using Pattern based Bit** | 2016 | cs.MM | Khan Muhammad et al. [[1]](https://arxiv.org/abs/1601.01386) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Capacity Enlargement Of The PVD Steganography Method Using The GLM Technique

**Goal:** quality of the stego-image, so in this paper, we propose to combine two existing techniques, Pixel value differencing and Gray Level Modification, to come up with a hybrid steganography scheme whic...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Capacity Enlargement Of The PVD Steganography Method Using T** | 2016 | cs.MM | Mehdi Safarpour, Mostafa Charmi [[1]](https://arxiv.org/abs/1601.00299) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Covert Communication Gains from Adversary's Ignorance of Transmission Time

**Goal:** The recent square root law (SRL) for covert communication demonstrates that Alice can reliably transmit \mathcal{O}(\sqrt{n}) bits to Bob in n uses of an additive white Gaussian noise (AWGN) channe...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Covert Communication Gains from Adversary's Ignorance of Tra** | 2016 | cs.IT | Boulat A. Bash, Dennis Goeckel, Don Towsley [[1]](https://arxiv.org/abs/1403.1013) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography: A Secure way for Transmission in Wireless Sensor Networks

**Goal:** network Internet is very sensitive and vulnerable to various attacks and risks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography: A Secure way for Transmission in Wireless Sen** | 2015 | cs.MM | Khan Muhammad [[1]](https://arxiv.org/abs/1511.08865) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Towards Reversible De-Identification in Video Sequences Using 3D Avatars and Steganography

**Goal:** We propose a de-identification pipeline that protects the privacy of humans in video sequences by replacing them with rendered 3D human models, hence concealing their identity while retaining the n...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Towards Reversible De-Identification in Video Sequences Usin** | 2015 | cs.CV, cs.MM | Martin Blažević, Karla Brkić, Tomislav Hrkać [[1]](https://arxiv.org/abs/1510.04861) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Ontology-based Secure Retrieval of Semantically Significant Visual Contents

**Goal:** to retrieve personal visual contents such as patients records and law enforcement agencies databases.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Ontology-based Secure Retrieval of Semantically Significant ** | 2015 | cs.MM, cs.IR | Khan Muhammad et al. [[1]](https://arxiv.org/abs/1510.02177) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Data Hiding in Video using Triangularization LSB Technique

**Goal:** The challenge is to be able to pass information in a manner that the very existence of the message is unknown in order to repel attention of the potential attacker.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Data Hiding in Video using Triangularization LSB Technique** | 2015 | cs.MM | Subhashri Acharya et al. [[1]](https://arxiv.org/abs/1507.05242) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Information in Noise: Fundamental Limits of Covert Wireless Communication

**Goal:** adversary using non-computational methods such as side-channel analysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Information in Noise: Fundamental Limits of Covert Wi** | 2015 | cs.IT | Boulat A. Bash et al. [[1]](https://arxiv.org/abs/1506.00066) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Identification of Image Operations Based on Steganalytic Features

**Goal:** operations would inevitably modify many image pixels.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Identification of Image Operations Based on Steganalytic Fea** | 2015 | cs.MM | Haodong Li et al. [[1]](https://arxiv.org/abs/1503.04718) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Optimal Radiometric Calibration for Camera-Display Communication

**Goal:** not surface reflectance.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Optimal Radiometric Calibration for Camera-Display Communica** | 2015 | cs.CV | Wenjia Yuan et al. [[1]](https://arxiv.org/abs/1501.01744) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Olfactory Signal Processing

**Goal:** from their physicochemical features and use the prediction as a foundation for several downstream processing tasks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Olfactory Signal Processing** | 2015 | cs.IT, cs.MM, stat.AP | Kush R. Varshney, Lav R. Varshney [[1]](https://arxiv.org/abs/1410.4865) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Secret Image Sharing Using Grayscale Payload Decomposition and Irreversible Image Steganography

**Goal:** To provide an added security level most of the existing reversible as well as irreversible image steganography schemes emphasize on encrypting the secret image (payload) before embedding it to the ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secret Image Sharing Using Grayscale Payload Decomposition a** | 2014 | cs.MM | Soumendu Chakraborty, Anand Singh Jalal, Charul Bhatnagar [[1]](https://arxiv.org/abs/1410.3122) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Digital Image Data Hiding Techniques: A Comparative Study

**Goal:** With the advancements in the field of digital image processing during the last decade, digital image data hiding techniques such as watermarking, Steganography have gained wide popularity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Digital Image Data Hiding Techniques: A Comparative Study** | 2014 | cs.MM | Minati Mishra, Priyadarsini Mishra, M. C. Adhikary [[1]](https://arxiv.org/abs/1408.3564) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Easy yet Effective Method for Detecting Spatial Domain LSB Steganography

**Goal:** their favor. Terrorists, anti-social groups use manipulated Stego images for secret communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Easy yet Effective Method for Detecting Spatial Domain LS** | 2014 | cs.MM | Minati Mishra, M. C. Adhikary [[1]](https://arxiv.org/abs/1407.6877) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A simple technique for steganography

**Goal:** A new technique for data hiding in digital image is proposed in this paper.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A simple technique for steganography** | 2013 | cs.MM | Adity Sharma, Anoo Agarwal, Vinay Kumar [[1]](https://arxiv.org/abs/1307.8385) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Image in Image by Five Modulus Method for Image Steganography

**Goal:** make it difficult for any adversary to extract the secret image from the cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Image in Image by Five Modulus Method for Image Stega** | 2013 | cs.MM, cs.CV | Firas A. Jassim [[1]](https://arxiv.org/abs/1304.1571) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Fresnelet-Based Encryption of Medical Images using Arnold Transform

**Goal:** handling of the Arnold transform and the discrete cosine transform to provide secure distribution of medical images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Fresnelet-Based Encryption of Medical Images using Arnold ** | 2013 | cs.CR, cs.CV | Muhammad Nazeer et al. [[1]](https://arxiv.org/abs/1302.3702) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Improving success probability and embedding efficiency in code based steganography

**Goal:** For stegoschemes arising from error correcting codes, embedding depends on a decoding map for the corresponding code.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improving success probability and embedding efficiency in co** | 2013 | cs.IT | Morgan Barbier, Carlos Munuera [[1]](https://arxiv.org/abs/1302.2048) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Hash based Approach for Secure Keyless Steganography in Lossless RGB Images

**Goal:** This paper proposes an improved steganography approach for hiding text messages in lossless RGB images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Hash based Approach for Secure Keyless Steganography in Lo** | 2013 | cs.CR, cs.CV, cs.MM | Ankit Chaudhary et al. [[1]](https://arxiv.org/abs/1211.5614) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Classification of minimal 1-saturating sets in PG(2,q), q\leq 23

**Goal:** to many branches of combinatorics and information theory, as data compression, compression with distortion, broadcasting in interconnection network, write-once memory or steganography (see \cite{Co...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Classification of minimal 1-saturating sets in PG(2,q), q\le** | 2012 | math.CO | Daniele Bartoli, Stefano Marcugini, Fernanda Pambianco [[1]](https://arxiv.org/abs/1203.1133) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Coordination using Implicit Communication

**Goal:** for various causality constraints.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Coordination using Implicit Communication** | 2011 | cs.IT | Paul Cuff, Lei Zhao [[1]](https://arxiv.org/abs/1108.3652) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Quantum Information in the Perfect Code

**Goal:** We present and analyze a protocol for quantum steganography where the sender (Alice) encodes her steganographic information into the error syndromes of the perfect (five-qubit) quantum error-correc...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Quantum Information in the Perfect Code** | 2011 | cs.CR | Bilal A. Shaw, Todd A. Brun [[1]](https://arxiv.org/abs/1007.0793) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Sterilization to Prevent LSB-based Steganographic Transmission

**Goal:** image. Experimental results show that our technique succeeded in sterilizing around 76% to 91% of stego pixels in an image on average, where data is embedded using LSB-based steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Sterilization to Prevent LSB-based Steganographic Tran** | 2010 | cs.MM | Goutam Paul, Imon Mukherjee [[1]](https://arxiv.org/abs/1012.5573) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Colour Guided Colour Image Steganography

**Goal:** Capacity, robustness and invisibility are important parameters in information hiding and are quite difficult to achieve in a single algorithm.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Colour Guided Colour Image Steganography** | 2010 | cs.MM | R. Amirtharajan et al. [[1]](https://arxiv.org/abs/1010.4007) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Quantum Steganography and Quantum Error-Correction

**Goal:** the receiver (Bob) and corrects an arbitrary single-qubit error.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Quantum Steganography and Quantum Error-Correction** | 2010 | cs.IT | Bilal A. Shaw [[1]](https://arxiv.org/abs/1008.0425) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Alternative Approach of Steganography using Reference Image

**Goal:** The 8-bit character can be split into 4X2 bit information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Alternative Approach of Steganography using Reference Ima** | 2010 | cs.MM | Samir Kumar Bandyopadhyay, Indra Kanta Maitra [[1]](https://arxiv.org/abs/1007.1233) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Product Perfect Z2Z4-linear codes in Steganography

**Goal:** the performance of the F5 steganographic method, whereas perfect Z2Z4-linear codes have been recently introduced as an efficient way to embed data, conforming to the +/-1-steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Product Perfect Z2Z4-linear codes in Steganography** | 2010 | cs.IT | J. Rifa, L. Ronquillo [[1]](https://arxiv.org/abs/1003.4852) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Signal Enhancement and Background Suppression Using Interference and Entanglement

**Goal:** the entanglement time and pair delay parameters.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Signal Enhancement and Background Suppression Using Interfer** | 2010 | cs.CR | Keith Kastella, Ralph S. Conti [[1]](https://arxiv.org/abs/1003.0423) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Image Steganography Based On First Component Alteration Technique

**Goal:** In this paper, A new image steganography scheme is proposed which is a kind of spatial domain technique.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Image Steganography Based On First Component Alteratio** | 2010 | cs.MM, cs.CV | Amanpreet Kaur, Renu Dhir, Geeta Sikka [[1]](https://arxiv.org/abs/1001.1972) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Trellis-coded quantization for public-key steganography

**Goal:** This paper deals with public-key steganography in the presence of a passive warden.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Trellis-coded quantization for public-key steganography** | 2008 | cs.MM, cs.IT | Gaëtan Le Guelvouit [[1]](https://arxiv.org/abs/0811.4700) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Quantum computing, phase estimation and applications

**Goal:** and an improved protocol for phase reference alignment is presented.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Quantum computing, phase estimation and applications** | 2008 | cs.CR | Miroslav Dobšíček [[1]](https://arxiv.org/abs/0803.0909) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

## Software Tools

---

### OpenPuff

**Goal:** Embed data across multiple carrier files (images, audio, video) with multi-layer encryption and plausible deniability.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **OpenPuff** | 2004 | Multi-carrier, multi-key steganography with AES/TDES/IDEA | Deniable stego: decoys + real payload [[1]](https://embeddedsw.net/OpenPuff_Steganography_Home.html) |

**State of the art:** Most sophisticated free multi-format stego tool. Supports BMP, PNG, TGA, JPEG, MP3, WAV, MP4, and more. Windows-only GUI.

**Production readiness:** Mature
Actively maintained; no source code released (closed-source freeware).

**Security status:** Caution
No public peer-reviewed cryptanalysis; closed-source limits independent verification.

**Community acceptance:** Widely trusted
Long history since 2004; widely cited in academic papers as a reference tool.

---

### SilentEye

**Goal:** Cross-platform GUI application for hiding messages in images and audio with plug-in based algorithm support.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SilentEye** | 2011 | Plugin-based LSB for JPEG/BMP/WAV | AES-128 encryption; drag-and-drop interface [[1]](https://github.com/achorein/silenteye) |

**State of the art:** User-friendly cross-platform GUI. Good for non-technical users; supports JPEG, BMP, WAV carriers.

**Production readiness:** Mature
Archived; no active development since 2012 but fully functional.

**Implementations:**
- [achorein/silenteye](https://github.com/achorein/silenteye) ⭐ 143 — C++/Qt, Windows/Linux/macOS

**Security status:** Caution
LSB scheme detectable via statistical analysis; AES encryption adds confidentiality layer.

**Community acceptance:** Niche
Known in CTF community; less popular than steghide for CLI workflows.

---

### Stegosuite

**Goal:** GUI-based Java steganography tool for embedding and extracting data in GIF, JPG, and BMP images with AES encryption.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegosuite** | 2010 | LSB with AES-128 in Java Swing GUI | Actively developed; cross-platform [[1]](https://stegosuite.org/) |

**State of the art:** Actively maintained Java GUI tool. Good for demonstrations and non-technical use cases.

**Production readiness:** Mature
Active development; available via apt on Kali Linux.

**Security status:** Caution
LSB detectable; AES protects payload confidentiality.

**Community acceptance:** Niche
Bundled in Kali Linux; used in CTF and academic courses.

---

### cloacked-pixel

**Goal:** LSB steganography in PNG images with AES-256 encryption of the payload before embedding.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **cloacked-pixel** | 2014 | AES-256 + LSB in PNG | Encrypted payload prevents content analysis even if stego detected [[1]](https://github.com/livz/cloacked-pixel) |

**State of the art:** Simple Python tool pairing LSB with strong encryption. Good balance of simplicity and payload security.

**Production readiness:** Mature
Stable; bundled in stego-toolkit Docker container.

**Implementations:**
- [livz/cloacked-pixel](https://github.com/livz/cloacked-pixel) ⭐ 631 — Python

**Security status:** Caution
LSB embedding detectable via zsteg; AES-256 protects payload content.

**Community acceptance:** Niche
Used in CTF challenges; cited in steganalysis tool evaluations.

---

### stegpy

**Goal:** Encode and decode messages in PNG, GIF, BMP, WebP images and WAV audio via LSB substitution with optional encryption.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **stegpy** | 2021 | LSB in PNG/GIF/BMP/WebP/WAV | Multi-format; single Python script [[1]](https://github.com/izcoser/stegpy) |

**State of the art:** Lightweight multi-format tool. Covers more image formats than most alternatives (GIF and WebP support is rare).

**Production readiness:** Experimental
Working implementation; limited testing.

**Implementations:**
- [izcoser/stegpy](https://github.com/izcoser/stegpy) ⭐ 131 — Python

**Security status:** Caution
LSB scheme; detectable by zsteg and similar tools.

**Community acceptance:** Niche
Small community; growing interest in multi-format support.

---

### jphide / jpseek

**Goal:** Embed secret data in JPEG images by modifying DCT coefficients with passphrase protection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **jphide** | 1999 | DCT coefficient modification with BBS PRNG selection | Low visual distortion; harder to detect than JSteg [[1]](https://github.com/DominicBreuker/stego-toolkit) |

**State of the art:** Classic JPEG stego pair: jphide embeds, jpseek extracts. Historically significant; detectable by stegbreak and stegdetect.

**Production readiness:** Deprecated
No active development; available in stego-toolkit container.

**Security status:** Broken
Detectable by stegdetect and stegbreak dictionary attacks; known detection fingerprint.

**Community acceptance:** Niche
Historical significance; used in CTF challenges as a known target format.

---

### OpenStego

**Goal:** Java GUI and CLI tool for data hiding and invisible digital watermarking in PNG/BMP images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **OpenStego** | 2006 | LSB substitution + random seed scattering | GUI + CLI; supports watermark verification mode [[1]](https://github.com/syvaidya/openstego) |

**State of the art:** Most popular open-source Java stego tool. Supports two modes: data hiding and watermarking. Active development; PNG output.

**Production readiness:** Mature
Stable; widely referenced in tutorials and CTF write-ups.

**Implementations:**
- [syvaidya/openstego](https://github.com/syvaidya/openstego) ⭐ 1.4k — Java, GUI + CLI

**Security status:** Caution
LSB-based; detectable by RS analysis and stegoVeritas. Watermark mode fragile against recompression.

**Community acceptance:** Widely trusted
Longest-running open-source image stego tool; included in stego-toolkit Docker container.

---

### invisible-watermark

**Goal:** Embed and extract invisible watermarks in images using frequency-domain transforms (DWT-DCT and RivaGAN).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **invisible-watermark** | 2020 | DWT-DCT and RivaGAN blind watermarking | Robust to JPEG compression, resize, and noise [[1]](https://github.com/ShieldMnt/invisible-watermark) |

**State of the art:** Leading Python library for production-grade invisible watermarking. Supports dwtDct (fragile) and RivaGAN (robust) backends. Used by Stable Diffusion and other generative AI pipelines.

**Production readiness:** Production
Used in production AI image pipelines for provenance tracking.

**Implementations:**
- [ShieldMnt/invisible-watermark](https://github.com/ShieldMnt/invisible-watermark) ⭐ 1.9k — Python, `pip install invisible-watermark`

**Security status:** Caution
RivaGAN robust to common transforms but removable via adversarial attacks. dwtDct mode is fragile.

**Community acceptance:** Widely trusted
Adopted by major generative AI tools; most widely used Python watermarking library.

---

### Stegify

**Goal:** CLI tool to hide any file inside an image using LSB steganography, written in Go with zero dependencies.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegify** | 2019 | LSB encoding across all three RGB channels | Single binary; encode/decode in one command [[1]](https://github.com/DimitarPetrov/stegify) |

**State of the art:** Lightweight Go CLI for basic LSB image stego. Supports PNG, JPEG, GIF. Library API also available.

**Production readiness:** Mature
Stable; no external dependencies; cross-platform binary.

**Implementations:**
- [DimitarPetrov/stegify](https://github.com/DimitarPetrov/stegify) ⭐ 1.3k — Go, `go install github.com/DimitarPetrov/stegify@latest`

**Security status:** Caution
Standard LSB; detectable by statistical analysis tools.

**Community acceptance:** Niche
Popular in Go community; frequently cited in stego tutorials.

---

### Stegano

**Goal:** Pure Python library for LSB image steganography with multiple pixel-selection patterns including prime scatter (Sieve of Eratosthenes).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stegano** | 2010 | LSB with configurable scatter: sequential, primes, Fermat, Fibonacci | Non-sequential embedding raises detectability bar [[1]](https://github.com/cedricbonhomme/Stegano) |

**State of the art:** Most feature-rich pure-Python stego library. Supports multiple scatter generators beyond sequential LSB. Included in stego-toolkit Docker container as `stegano`.

**Production readiness:** Mature
Stable; actively maintained; pip-installable.

**Implementations:**
- [cedricbonhomme/Stegano](https://github.com/cedricbonhomme/Stegano) ⭐ 589 — Python, `pip install stegano`

**Security status:** Caution
Non-sequential scatter increases difficulty of capacity estimation but does not defeat statistical steganalysis.

**Community acceptance:** Niche
Included in stego-toolkit; widely used in academic demonstrations.

---

### LSB Steganography (ragibson)

**Goal:** Python library for LSB steganography in BMP/PNG images and WAV audio, plus built-in LSB steganalysis extraction.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **LSB-Steganography** | 2015 | LSB in bitmap images and WAV samples | Includes steganalysis: LSB extraction brute-force [[1]](https://github.com/ragibson/Steganography) |

**State of the art:** Clean reference implementation covering both hiding (BMP, PNG, WAV) and analysis. Useful as educational library with steganalysis primitives built in.

**Production readiness:** Mature
Stable; pip-installable; good test coverage.

**Implementations:**
- [ragibson/Steganography](https://github.com/ragibson/Steganography) ⭐ 649 — Python, `pip install steganography`

**Security status:** Caution
Standard LSB; steganalysis module demonstrates how easily LSB payloads are extracted without a key.

**Community acceptance:** Niche
Frequently used in academic and educational settings for demonstrating LSB concepts.

---

