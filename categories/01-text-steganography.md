# Text Steganography

<!-- TOC -->
## Contents (257 algorithms)

**[Structural Methods](#structural-methods)**
- [ASCII Art Steganography](#ascii-art-steganography)
- [Word Change Tracking](#word-change-tracking)
- [Bacon's Cipher](#bacons-cipher)
- [Null Cipher](#null-cipher)
- [Whitespace coding](#whitespace-coding)
- [Zero-width Unicode](#zero-width-unicode)
- [Homoglyphs](#homoglyphs)

**[Semantic Methods](#semantic-methods)**
- [Chaffing and Winnowing](#chaffing-and-winnowing)
- [Mimic Functions](#mimic-functions)

**[LLM-Based Methods](#llm-based-methods)**
- [Meteor](#meteor)
- [Discop](#discop)
- [ChatStega](#chatstega)
- [Blog-Steganography](#blog-steganography)
- [Range Coding](#range-coding)
- [Anchored Sliding Window](#anchored-sliding-window-asw)
- [ReTokSync](#retoksync)
- [Entropy-Driven](#entropy-driven-rank-token-mapping)
- [Auto-Stega](#auto-stega)
- [Dynamic Codebook](#dynamic-codebook)
- [OD-Stega](#od-stega)
- [Shifting-Merging](#shifting-merging)
- [Semantic Steganography](#semantic-steganography-llm)
- [Content-Preserving Linguistic](#content-preserving-linguistic-steganography)
- [Raster Domain Text](#raster-domain-text-steganography)
- [Alkaid](#alkaid)
- [SparSamp](#sparsamp)
- [Kolmogorov Complexity Bounds](#kolmogorov-complexity-bounds)
- [STEAD](#stead-robust-provably-secure-linguistic-steganography)
- [Hide and Seek in Embedding Space](#hide-and-seek-in-embedding-space)
- [StegoStylo](#stegastylo)
- [Undetectable Conversations](#undetectable-conversations)
- [TrojanStego](#trojanstego)
- [GTSD](#gtsd-generative-text-steganography-via-diffusion)
- [List Decoding](#provably-secure-steganography-based-on-list-decoding)
- [Addressing Tokenization Inconsistency](#addressing-tokenization-inconsistency)

**[Recent arXiv Papers (2024–2026)](#recent-arxiv-papers-20242026)**
- [Safeguarding LLMs Against Misuse and AI-Driven Malware Using...](#safeguarding-llms-against-misuse-and-ai-driven-malware-using-steganographic-canaries)
- [A Decision-Theoretic Formalisation of Steganography With App...](#a-decision-theoretic-formalisation-of-steganography-with-applications-to-llm-monitoring)
- [AndroWasm: an Empirical Study on Android Malware Obfuscation...](#androwasm-an-empirical-study-on-android-malware-obfuscation-through-webassembly)
- [Verifying LLM Inference to Detect Model Weight Exfiltration](#verifying-llm-inference-to-detect-model-weight-exfiltration)
- [Unveiling Unicode's Unseen Underpinnings in Undermining Auth...](#unveiling-unicodes-unseen-underpinnings-in-undermining-authorship-attribution)
- [Hiding in Plain Sight: A Steganographic Approach to Stealthy...](#hiding-in-plain-sight-a-steganographic-approach-to-stealthy-llm-jailbreaks)
- [Provable Secure Steganography Based on Adaptive Dynamic Samp...](#provable-secure-steganography-based-on-adaptive-dynamic-sampling)
- [Plug-and-Hide: Provable and Adjustable Diffusion Generative ...](#plug-and-hide-provable-and-adjustable-diffusion-generative-steganography)
- [Odysseus: Jailbreaking Commercial Multimodal LLM-integrated ...](#odysseus-jailbreaking-commercial-multimodal-llm-integrated-systems-via-dual-steganography)
- [Defining Cost Function of Steganography with Large Language ...](#defining-cost-function-of-steganography-with-large-language-models)
- [A High-Capacity and Secure Disambiguation Algorithm for Neur...](#a-high-capacity-and-secure-disambiguation-algorithm-for-neural-linguistic-steganography)
- [Invisible Injections: Exploiting Vision-Language Models Thro...](#invisible-injections-exploiting-vision-language-models-through-steganographic-prompt-embedding)
- [Singularity Cipher: A Topology-Driven Cryptographic Scheme B...](#singularity-cipher-a-topology-driven-cryptographic-scheme-based-on-visual-paradox-and-klein-bottle-illusions)
- [Favicon Trojans: Executable Steganography Via Ico Alpha Chan...](#favicon-trojans-executable-steganography-via-ico-alpha-channel-exploitation)
- [Early Signs of Steganographic Capabilities in Frontier LLMs](#early-signs-of-steganographic-capabilities-in-frontier-llms)
- [Efficient Blockchain-based Steganography via Backcalculating...](#efficient-blockchain-based-steganography-via-backcalculating-generative-adversarial-network)
- [A Dual-Layer Image Encryption Framework Using Chaotic AES wi...](#a-dual-layer-image-encryption-framework-using-chaotic-aes-with-dynamic-s-boxes-and-steganographic-qr-codes)
- [Pixel-Sensitive and Robust Steganography Based on Polar Code...](#pixel-sensitive-and-robust-steganography-based-on-polar-codes)
- [Dynamic Encryption-Based Cloud Security Model using Facial I...](#dynamic-encryption-based-cloud-security-model-using-facial-image-and-password-based-key-generation-for-multimedia-data)
- [Cryptologic Techniques and Associated Risks in Public and Pr...](#cryptologic-techniques-and-associated-risks-in-public-and-private-security-an-italian-and-european-union-perspective-with-an-overview-of-the-current-legal-framework)
- [The Steganographic Potentials of Language Models](#the-steganographic-potentials-of-language-models)
- [Unified Steganography via Implicit Neural Representation](#unified-steganography-via-implicit-neural-representation)
- [A Character-based Diffusion Embedding Algorithm for Enhancin...](#a-character-based-diffusion-embedding-algorithm-for-enhancing-the-generation-quality-of-generative-linguistic-steganographic-texts)
- [Robust Steganography from Large Language Models](#robust-steganography-from-large-language-models)
- [Steganographic Embeddings as an Effective Data Augmentation](#steganographic-embeddings-as-an-effective-data-augmentation)
- [Mixing Algorithm for Extending the Tiers of the Unapparent I...](#mixing-algorithm-for-extending-the-tiers-of-the-unapparent-information-send-through-the-audio-streams)
- [Sound Conveyors for Stealthy Data Transmission](#sound-conveyors-for-stealthy-data-transmission)
- [Relatively-Secure LLM-Based Steganography via Constrained Ma...](#relatively-secure-llm-based-steganography-via-constrained-markov-decision-processes)
- [Stealthy Backdoor Attack to Real-world Models in Android App...](#stealthy-backdoor-attack-to-real-world-models-in-android-apps)
- [A Plug-and-Play Method for Improving Imperceptibility and Ca...](#a-plug-and-play-method-for-improving-imperceptibility-and-capacity-in-practical-generative-text-steganography)
- [Steganography and Probabilistic Risk Analysis: A Game Theore...](#steganography-and-probabilistic-risk-analysis-a-game-theoretical-framework-for-quantifying-adversary-advantage-and-impact)
- [Hidden in Plain Text: Emergence & Mitigation of Steganograph...](#hidden-in-plain-text-emergence-mitigation-of-steganographic-collusion-in-llms)
- [Secret Collusion among AI Agents: Multi-Agent Deception via ...](#secret-collusion-among-ai-agents-multi-agent-deception-via-steganography)
- [Dynamically Allocated Interval-Based Generative Linguistic S...](#dynamically-allocated-interval-based-generative-linguistic-steganography-with-roulette-wheel)
- [Sanitizing Hidden Information with Diffusion Models](#sanitizing-hidden-information-with-diffusion-models)
- [Robust Steganography with Boundary-Preserving Overflow Allev...](#robust-steganography-with-boundary-preserving-overflow-alleviation-and-adaptive-error-correction)
- [ADLM -- stega: A Universal Adaptive Token Selection Algorith...](#adlm-stega-a-universal-adaptive-token-selection-algorithm-for-improving-steganographic-text-quality-via-information-entropy)
- [Using Steganography and Watermarking For Medical Image Integ...](#using-steganography-and-watermarking-for-medical-image-integrity)
- [Model X-Ray: Detection of Hidden Malware in AI Model Weights...](#model-x-ray-detection-of-hidden-malware-in-ai-model-weights-using-few-shot-learning)
- [Provably Robust and Secure Steganography in Asymmetric Resou...](#provably-robust-and-secure-steganography-in-asymmetric-resource-scenario)
- [Image steganography based on generative implicit neural repr...](#image-steganography-based-on-generative-implicit-neural-representation)
- [Computing Low-Entropy Couplings for Large-Support Distributi...](#computing-low-entropy-couplings-for-large-support-distributions)
- [Hiding Sensitive Information Using PDF Steganography](#hiding-sensitive-information-using-pdf-steganography)
- [An Extensive Survey of Digital Image Steganography: State of...](#an-extensive-survey-of-digital-image-steganography-state-of-the-art)
- [Boosting Digital Safeguards: Blending Cryptography and Stega...](#boosting-digital-safeguards-blending-cryptography-and-steganography)
- [Provably Secure Disambiguating Neural Linguistic Steganograp...](#provably-secure-disambiguating-neural-linguistic-steganography)
- [Zero-shot Generative Linguistic Steganography](#zero-shot-generative-linguistic-steganography)
- [Pseudorandom Error-Correcting Codes](#pseudorandom-error-correcting-codes)
- [Implicit Steganography Beyond the Constraints of Modality](#implicit-steganography-beyond-the-constraints-of-modality)
- [Hiding in Plain Sight: Towards the Science of Linguistic Ste...](#hiding-in-plain-sight-towards-the-science-of-linguistic-steganography)
- [Secure Information Embedding in Images with Hybrid Firefly A...](#secure-information-embedding-in-images-with-hybrid-firefly-algorithm)
- [A Novel Residual-guided Learning Method for Image Steganogra...](#a-novel-residual-guided-learning-method-for-image-steganography)
- [StegGuard: Fingerprinting Self-supervised Pre-trained Encode...](#stegguard-fingerprinting-self-supervised-pre-trained-encoders-via-secrets-embeder-and-extractor)
- [Disarming Steganography Attacks Inside Neural Network Models](#disarming-steganography-attacks-inside-neural-network-models)
- [On the Steganographic Capacity of Selected Learning Models](#on-the-steganographic-capacity-of-selected-learning-models)
- [Introducing a New Evaluation Criteria for EMD-Base Steganogr...](#introducing-a-new-evaluation-criteria-for-emd-base-steganography-method)
- [Open Image Content Disarm And Reconstruction](#open-image-content-disarm-and-reconstruction)
- [Deep Cross-Modal Steganography Using Neural Representations](#deep-cross-modal-steganography-using-neural-representations)
- [Errorless Robust JPEG Steganography Using Steganographic Pol...](#errorless-robust-jpeg-steganography-using-steganographic-polar-codes)
- [Off-By-One Implementation Error in J-UNIWARD](#off-by-one-implementation-error-in-j-uniward)
- [The Realizations of Steganography in Encrypted Domain](#the-realizations-of-steganography-in-encrypted-domain)
- [ICStega: Image Captioning-based Semantically Controllable Li...](#icstega-image-captioning-based-semantically-controllable-linguistic-steganography)
- [Steganography of Steganographic Networks](#steganography-of-steganographic-networks)
- [A New Paradigm for Improved Image Steganography by using Ada...](#a-new-paradigm-for-improved-image-steganography-by-using-adaptive-number-of-dominant-discrete-cosine-transform-coefficients)
- [Blind Spots: Automatically detecting ignored program inputs](#blind-spots-automatically-detecting-ignored-program-inputs)
- [Improving Robustness of TCM-based Robust Steganography with ...](#improving-robustness-of-tcm-based-robust-steganography-with-variable-robustness)
- [Perfectly Secure Steganography Using Minimum Entropy Couplin...](#perfectly-secure-steganography-using-minimum-entropy-coupling)
- [Addressing Segmentation Ambiguity in Neural Linguistic Stega...](#addressing-segmentation-ambiguity-in-neural-linguistic-steganography)
- [Cover Reproducible Steganography via Deep Generative Models](#cover-reproducible-steganography-via-deep-generative-models)
- [Information-Theoretic Bounds for Steganography in Multimedia](#information-theoretic-bounds-for-steganography-in-multimedia)
- [Matryoshka: Stealing Functionality of Private ML Data by Hid...](#matryoshka-stealing-functionality-of-private-ml-data-by-hiding-models-in-model)
- [A Survey On Semantic Steganography Systems](#a-survey-on-semantic-steganography-systems)
- [On Information Hiding in Natural Language Systems](#on-information-hiding-in-natural-language-systems)
- [Semantic-Preserving Linguistic Steganography by Pivot Transl...](#semantic-preserving-linguistic-steganography-by-pivot-translation-and-semantic-aware-bins-coding)
- [Using Deep Learning to Detect Digitally Encoded DNA Trigger ...](#using-deep-learning-to-detect-digitally-encoded-dna-trigger-for-trojan-malware-in-bio-cyber-attacks)
- [A Novel Pair and Matching Algorithm for Embedding Secret Mes...](#a-novel-pair-and-matching-algorithm-for-embedding-secret-messages-in-images)
- [A Novel Algorithm In Steganography Using Weighted Matching T...](#a-novel-algorithm-in-steganography-using-weighted-matching-technique)
- [Hiding Data in Colors: Secure and Lossless Deep Image Stegan...](#hiding-data-in-colors-secure-and-lossless-deep-image-steganography-via-conditional-invertible-neural-networks)
- [Image data hiding with multi-scale autoencoder network](#image-data-hiding-with-multi-scale-autoencoder-network)
- [SABMIS: Sparse approximation based blind multi-image stegano...](#sabmis-sparse-approximation-based-blind-multi-image-steganography-scheme)
- [A Brief Survey on Deep Learning Based Data Hiding](#a-brief-survey-on-deep-learning-based-data-hiding)
- [IoTSign: Protecting Privacy and Authenticity of IoT using Di...](#iotsign-protecting-privacy-and-authenticity-of-iot-using-discrete-cosine-based-steganography)
- [Maneuvering Digital Watermarking In Face Recognition](#maneuvering-digital-watermarking-in-face-recognition)
- [GANash -- A GAN approach to steganography](#ganash-a-gan-approach-to-steganography)
- [Steganography of Complex Networks](#steganography-of-complex-networks)
- [Improving Dither Modulation based Robust Steganography by Ov...](#improving-dither-modulation-based-robust-steganography-by-overflow-suppression)
- [Architecture of Network Camera Photo Authentication Scheme u...](#architecture-of-network-camera-photo-authentication-scheme-using-steganography-approach)
- [Generative Models for Security: Attacks, Defenses, and Oppor...](#generative-models-for-security-attacks-defenses-and-opportunities)
- [Provably Secure Generative Linguistic Steganography](#provably-secure-generative-linguistic-steganography)
- [Frustratingly Easy Edit-based Linguistic Steganography with ...](#frustratingly-easy-edit-based-linguistic-steganography-with-a-masked-language-model)
- [Permutation Encoding for Text Steganography: A Short Tutoria...](#permutation-encoding-for-text-steganography-a-short-tutorial)
- [A New Approach to Enhance Security of Visual Cryptography Us...](#a-new-approach-to-enhance-security-of-visual-cryptography-using-steganography-visus)
- [Blockchain for steganography: advantages, new algorithms and...](#blockchain-for-steganography-advantages-new-algorithms-and-open-challenges)
- [Invisible Backdoor Attack with Sample-Specific Triggers](#invisible-backdoor-attack-with-sample-specific-triggers)
- [Review and Test of Steganography Techniques](#review-and-test-of-steganography-techniques)
- [LSB Steganography Using Pixel Locator Sequence with AES](#lsb-steganography-using-pixel-locator-sequence-with-aes)
- [Near-imperceptible Neural Linguistic Steganography via Self-...](#near-imperceptible-neural-linguistic-steganography-via-self-adjusting-arithmetic-coding)
- [Graph-Stega: Semantic Controllable Steganographic Text Gener...](#graph-stega-semantic-controllable-steganographic-text-generation-guided-by-knowledge-graph)
- [Steganography GAN: Cracking Steganography with Cycle Generat...](#steganography-gan-cracking-steganography-with-cycle-generative-adversarial-networks)
- [Two high capacity text steganography schemes based on color ...](#two-high-capacity-text-steganography-schemes-based-on-color-coding)
- [JPEG Steganography and Synchronization of DCT Coefficients f...](#jpeg-steganography-and-synchronization-of-dct-coefficients-for-a-given-development-pipeline)
- [Natural Steganography in JPEG Domain with a Linear Developme...](#natural-steganography-in-jpeg-domain-with-a-linear-development-pipeline)
- [Differentially Private M-band Wavelet-Based Mechanisms in Ma...](#differentially-private-m-band-wavelet-based-mechanisms-in-machine-learning-environments)
- [Steganography using a 3 player game](#steganography-using-a-3-player-game)
- [Adversarial Embedding: A robust and elusive Steganography an...](#adversarial-embedding-a-robust-and-elusive-steganography-and-watermarking-technique)
- [Behavioral Security in Covert Communication Systems](#behavioral-security-in-covert-communication-systems)
- [Blockchain of Signature Material Combining Cryptographic Has...](#blockchain-of-signature-material-combining-cryptographic-hash-function-and-dna-steganography)
- [Image Steganography: Protection of Digital Properties agains...](#image-steganography-protection-of-digital-properties-against-eavesdropping)
- [Neural Linguistic Steganography](#neural-linguistic-steganography)
- [Uncheatable Machine Learning Inference](#uncheatable-machine-learning-inference)
- [Image Steganography using Gaussian Markov Random Field Model](#image-steganography-using-gaussian-markov-random-field-model)
- [EncryptGAN: Image Steganography with Domain Transform](#encryptgan-image-steganography-with-domain-transform)
- [Learning Symmetric and Asymmetric Steganography via Adversar...](#learning-symmetric-and-asymmetric-steganography-via-adversarial-training)
- [Generative Steganography by Sampling](#generative-steganography-by-sampling)
- [A New Parallel Message-distribution Technique for Cost-based...](#a-new-parallel-message-distribution-technique-for-cost-based-steganography)
- [Training Set Camouflage](#training-set-camouflage)
- [Automatically Generate Steganographic Text Based on Markov M...](#automatically-generate-steganographic-text-based-on-markov-model-and-huffman-coding)
- [2D Hybrid chaos map for image security transform based on fr...](#2d-hybrid-chaos-map-for-image-security-transform-based-on-framelet-and-cellular-automata)
- [A novel method of speech information hiding based on 3D-Magi...](#a-novel-method-of-speech-information-hiding-based-on-3d-magic-matrix)
- [Tackling Android Stego Apps in the Wild](#tackling-android-stego-apps-in-the-wild)
- [Steganography Security: Principle and Practice](#steganography-security-principle-and-practice)
- [Application of Lowner-John Ellipsoid in the Steganography of...](#application-of-lowner-john-ellipsoid-in-the-steganography-of-lattice-vectors-and-a-review-of-the-gentrys-fhe)
- [The Reincarnation of Grille Cipher: A Generative Approach](#the-reincarnation-of-grille-cipher-a-generative-approach)
- [Information Security in Health Care Centre Using Cryptograph...](#information-security-in-health-care-centre-using-cryptography-and-steganography)
- [On the Gold Standard for Security of Universal Steganography](#on-the-gold-standard-for-security-of-universal-steganography)
- [The New Threats of Information Hiding: the Road Ahead](#the-new-threats-of-information-hiding-the-road-ahead)
- [An Improvement on LSB Matching and LSB Matching Revisited St...](#an-improvement-on-lsb-matching-and-lsb-matching-revisited-steganography-methods)
- [An improvement on LSB+ method](#an-improvement-on-lsb-method)
- [Algorithm Substitution Attacks from a Steganographic Perspec...](#algorithm-substitution-attacks-from-a-steganographic-perspective)
- [A Steganographic Design Paradigm for General Steganographic ...](#a-steganographic-design-paradigm-for-general-steganographic-objectives)
- [Achieving Efficient and Provably Secure Steganography in Pra...](#achieving-efficient-and-provably-secure-steganography-in-practice)
- [SocialStegDisc: Application of steganography in social netwo...](#socialstegdisc-application-of-steganography-in-social-networks-to-create-a-file-system)
- [A Cryptographic Approach for Steganography](#a-cryptographic-approach-for-steganography)
- [A New Steganographic Technique Matching the Secret Message a...](#a-new-steganographic-technique-matching-the-secret-message-and-cover-image-binary-value)
- [A Novel Approach of Pseudorandomly sorted list-based Stegano...](#a-novel-approach-of-pseudorandomly-sorted-list-based-steganography)
- [Generating Steganographic Images via Adversarial Training](#generating-steganographic-images-via-adversarial-training)
- [A New Approach to SMS Steganography using Mathematical Equat...](#a-new-approach-to-sms-steganography-using-mathematical-equations)
- [Natural Steganography: cover-source switching for better ste...](#natural-steganography-cover-source-switching-for-better-steganography)
- [High Capacity Image Steganography using Adjunctive Numerical...](#high-capacity-image-steganography-using-adjunctive-numerical-representations-with-multiple-bit-plane-decomposition-methods)
- [Steganography -- A Game of Hide and Seek in Information Comm...](#steganography-a-game-of-hide-and-seek-in-information-communication)
- [Secure Image Steganography using Cryptography and Image Tran...](#secure-image-steganography-using-cryptography-and-image-transposition)
- [Steganography and Broadcasting](#steganography-and-broadcasting)
- [A Novel Approach for Image Steganography in Spatial Domain](#a-novel-approach-for-image-steganography-in-spatial-domain)
- [Using Facebook for Image Steganography](#using-facebook-for-image-steganography)
- [PDF Steganography based on Chinese Remainder Theorem](#pdf-steganography-based-on-chinese-remainder-theorem)
- [A Low-throughput Wavelet-based Steganography Audio Scheme](#a-low-throughput-wavelet-based-steganography-audio-scheme)
- [Environment Based Secure Transfer of Data in Wireless Sensor...](#environment-based-secure-transfer-of-data-in-wireless-sensor-networks)
- [A Secure Cyclic Steganographic Technique for Color Images us...](#a-secure-cyclic-steganographic-technique-for-color-images-using-randomization)
- [How to Bootstrap Anonymous Communication](#how-to-bootstrap-anonymous-communication)
- [A Secure Electronic Prescription System Using Steganography ...](#a-secure-electronic-prescription-system-using-steganography-with-encryption-key-implementation)
- [Steganography in Modern Smartphones and Mitigation Technique...](#steganography-in-modern-smartphones-and-mitigation-techniques)
- [StegExpose - A Tool for Detecting LSB Steganography](#stegexpose-a-tool-for-detecting-lsb-steganography)
- [An Approach for Text Steganography Based on Markov Chains](#an-approach-for-text-steganography-based-on-markov-chains)
- [High Security Image Steganography with Modified Arnold cat m...](#high-security-image-steganography-with-modified-arnold-cat-map)
- [Reversible and Irreversible Data Hiding Technique](#reversible-and-irreversible-data-hiding-technique)
- [Steganography -- coding and intercepting the information fro...](#steganography-coding-and-intercepting-the-information-from-encoded-pictures-in-the-absence-of-any-initial-information)
- [A Study of Various Steganographic Techniques Used for Inform...](#a-study-of-various-steganographic-techniques-used-for-information-hiding)
- [Dual Layer Textual Message Cryptosystem with Randomized Sequ...](#dual-layer-textual-message-cryptosystem-with-randomized-sequence-of-symmetric-key)
- [Robust Steganography Using LSB-XOR and Image Sharing](#robust-steganography-using-lsb-xor-and-image-sharing)
- [Steganography using the Extensible Messaging and Presence Pr...](#steganography-using-the-extensible-messaging-and-presence-protocol-xmpp)
- [Comparison of secure and high capacity color image steganogr...](#comparison-of-secure-and-high-capacity-color-image-steganography-techniques-in-rgb-and-ycbcr-domains)
- [A Novel Steganography Algorithm for Hiding Text in Image usi...](#a-novel-steganography-algorithm-for-hiding-text-in-image-using-five-modulus-method)
- [Enhanced Tiny Encryption Algorithm with Embedding (ETEA)](#enhanced-tiny-encryption-algorithm-with-embedding-etea)
- [One Time Pad Password Protection: Using T.E.C. Steganography...](#one-time-pad-password-protection-using-tec-steganography-and-secure-password-transmission-protocols)
- [Image Steganography based on a Parameterized Canny Edge Dete...](#image-steganography-based-on-a-parameterized-canny-edge-detection-algorithm)
- [Image Steganography Method Based on Brightness Adjustment](#image-steganography-method-based-on-brightness-adjustment)
- [An Authentication Technique in Frequency Domain through Wave...](#an-authentication-technique-in-frequency-domain-through-wavelet-transform-atfdwt)
- [A Text Steganography Method Using Pangram and Image Mediums](#a-text-steganography-method-using-pangram-and-image-mediums)
- [A Lossless Data Hiding Technique based on AES-DWT](#a-lossless-data-hiding-technique-based-on-aes-dwt)
- [A Generation-based Text Steganography Method using SQL Queri...](#a-generation-based-text-steganography-method-using-sql-queries)
- [An Image Steganography Scheme using Randomized Algorithm and...](#an-image-steganography-scheme-using-randomized-algorithm-and-context-free-grammar)
- [Embedding grayscale halftone pictures in QR Codes using Corr...](#embedding-grayscale-halftone-pictures-in-qr-codes-using-correction-trees)
- [Some New Methodologies for Image Hiding using Steganographic...](#some-new-methodologies-for-image-hiding-using-steganographic-techniques)
- [Public key Steganography Using Discrete Cross-Coupled Chaoti...](#public-key-steganography-using-discrete-cross-coupled-chaotic-maps)
- [Multimedia Steganographic Scheme using Multiresolution Analy...](#multimedia-steganographic-scheme-using-multiresolution-analysis)
- [Security Architecture for Cluster based Ad Hoc Networks](#security-architecture-for-cluster-based-ad-hoc-networks)
- [Pixastic: Steganography based Anti-Phihsing Browser Plug-in](#pixastic-steganography-based-anti-phihsing-browser-plug-in)
- [A Survey on Various Data Hiding Techniques and their Compara...](#a-survey-on-various-data-hiding-techniques-and-their-comparative-analysis)
- [Text Steganography using LSB insertion method along with Cha...](#text-steganography-using-lsb-insertion-method-along-with-chaos-theory)
- [Genetic Algorithm to Make Persistent Security and Quality of...](#genetic-algorithm-to-make-persistent-security-and-quality-of-image-in-steganography-from-rs-analysis)
- [Experimenting with the Novel Approaches in Text Steganograph...](#experimenting-with-the-novel-approaches-in-text-steganography)
- [A Frequency Domain Steganography using Z Transform (FDSZT)](#a-frequency-domain-steganography-using-z-transform-fdszt)
- [Influence of Speech Codecs Selection on Transcoding Steganog...](#influence-of-speech-codecs-selection-on-transcoding-steganography)
- [Information Hiding in CSS : A Secure Scheme Text-Steganograp...](#information-hiding-in-css-a-secure-scheme-text-steganography-using-public-key-cryptosystem)
- [Windtalking Computers: Frequency Normalization, Binary Codin...](#windtalking-computers-frequency-normalization-binary-coding-systems-and-encryption)
- [Randomness Efficient Steganography](#randomness-efficient-steganography)
- [Chaotic iterations for steganography: Stego-security and top...](#chaotic-iterations-for-steganography-stego-security-and-topological-security)
- [Steganography Algorithm to Hide Secret Message inside an Ima...](#steganography-algorithm-to-hide-secret-message-inside-an-image)
- [Steganography: a Class of Algorithms having Secure Propertie...](#steganography-a-class-of-algorithms-having-secure-properties)
- [Steganography: a class of secure and robust algorithms](#steganography-a-class-of-secure-and-robust-algorithms)
- [Using Transcoding for Hidden Communication in IP Telephony](#using-transcoding-for-hidden-communication-in-ip-telephony)
- [Applying statistical methods to text steganography](#applying-statistical-methods-to-text-steganography)
- [An Approach for Message Hiding using Substitution Techniques...](#an-approach-for-message-hiding-using-substitution-techniques-and-audio-hiding-in-steganography)
- [Digital Forensics Analysis of Spectral Estimation Methods](#digital-forensics-analysis-of-spectral-estimation-methods)
- [Is Cloud Computing Steganography-proof?](#is-cloud-computing-steganography-proof)
- [Lost Audio Packets Steganography: The First Practical Evalua...](#lost-audio-packets-steganography-the-first-practical-evaluation)
- [Wet paper codes and the dual distance in steganography](#wet-paper-codes-and-the-dual-distance-in-steganography)
- [Hiding Secret Information in Movie Clip: A Steganographic Ap...](#hiding-secret-information-in-movie-clip-a-steganographic-approach)
- [On Steganography in Lost Audio Packets](#on-steganography-in-lost-audio-packets)
- [Bio-Authentication based Secure Transmission System using St...](#bio-authentication-based-secure-transmission-system-using-steganography)
- [Improved information security using robust Steganography sys...](#improved-information-security-using-robust-steganography-system)
- [Overview: Main Fundamentals for Steganography](#overview-main-fundamentals-for-steganography)
- [New System for Secure Cover File of Hidden Data in the Image...](#new-system-for-secure-cover-file-of-hidden-data-in-the-image-page-within-executable-file-using-statistical-steganography-techniques)
- [M-Banking Security - a futuristic improved security approach](#m-banking-security-a-futuristic-improved-security-approach)
- [A Steganography Based on CT-CDMA Communication Scheme Using ...](#a-steganography-based-on-ct-cdma-communication-scheme-using-complete-complementary-codes)
- [Frame Selected Approach for Hiding Data within MPEG Video Us...](#frame-selected-approach-for-hiding-data-within-mpeg-video-using-bit-plane-complexity-segmentation)
- [Steganography An Art of Hiding Data](#steganography-an-art-of-hiding-data)
- [An approach to secure highly confidential documents of any s...](#an-approach-to-secure-highly-confidential-documents-of-any-size-in-the-corporate-or-institutes-having-unsecured-networks)
- [A novel approach for implementing Steganography with computi...](#a-novel-approach-for-implementing-steganography-with-computing-power-obtained-by-combining-cuda-and-matlab)
- [Efficient Steganography with Provable Security Guarantees](#efficient-steganography-with-provable-security-guarantees)
- [A Performance Analysis of HICCUPS - a Steganographic System ...](#a-performance-analysis-of-hiccups-a-steganographic-system-for-wlan)
- [Hiding Information in Retransmissions](#hiding-information-in-retransmissions)
- [Using Kolmogorov Complexity for Understanding Some Limitatio...](#using-kolmogorov-complexity-for-understanding-some-limitations-on-steganography)
- [Capacity of Steganographic Channels](#capacity-of-steganographic-channels)
- [TrustMAS: Trusted Communication Platform for Multi-Agent Sys...](#trustmas-trusted-communication-platform-for-multi-agent-systems)
- [Image Steganography, a New Approach for Transferring Securit...](#image-steganography-a-new-approach-for-transferring-security-information)
- [Steganography from weak cryptography](#steganography-from-weak-cryptography)
- [Information Hiding Techniques: A Tutorial Review](#information-hiding-techniques-a-tutorial-review)
- [An Improved FPGA Implementation of the Modified Hybrid Hidin...](#an-improved-fpga-implementation-of-the-modified-hybrid-hiding-encryption-algorithm-mhhea-for-data-communication-security)
- [Lightweight security mechanism for PSTN-VoIP cooperation](#lightweight-security-mechanism-for-pstn-voip-cooperation)
- [New security and control protocol for VoIP based on steganog...](#new-security-and-control-protocol-for-voip-based-on-steganography-and-digital-watermarking)
- [Content Based Image Retrieval with Mobile Agents and Stegano...](#content-based-image-retrieval-with-mobile-agents-and-steganography)
<!-- /TOC -->

## Structural Methods

---

### ASCII Art Steganography

**Goal:** Hide data in ASCII art representations.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **ASCII Art** | 2010 | Character density | Survives printing [[1]](https://wayner.org/node/43) [[2]](https://arxiv.org/abs/1003.1470) |

**State of the art:** Novel approach surviving print. Peter Wayner's description at wayner.org remains the key reference; the 2010 arXiv survey provides broader context.

**Production readiness:** Experimental
Works as a proof-of-concept; no mainstream tooling or library support.

**Implementations:**
- [ascii-steganography](https://github.com/vgmoose/ascii-steganography) ⭐ 18 — Python, hides data in plain ASCII art

**Security status:** Caution
Visually convincing but detectable by automated density-analysis; printing reduces capacity significantly.

**Community acceptance:** Niche
Interesting novelty, cited in surveys but rarely used in practice.

---

### Word Change Tracking

**Goal:** Hide data using word processor change tracking feature.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Change Tracking** | 2007 | Deliberate errors | Word docs [[1]](https://people.cs.nycu.edu.tw/~whtsai/Journal%20Paper%20PDFs/Liu_&_Tsai_IEEE_T_IFS_2007.pdf) |

**State of the art:** Liu & Tsai (IEEE T-IFS 2007) propose hiding data by introducing synonym-based degradations in a document and tracking the revisions; the change-tracking metadata encodes the payload.

**Production readiness:** Experimental
Academic prototype; requires Microsoft Word and collaborative editing context.

**Security status:** Caution
Detectable if an adversary inspects revision metadata or compares against the clean document.

**Community acceptance:** Niche
Cited in text-steganography surveys but not adopted beyond academic settings.

---

### Bacon's Cipher

**Goal:** Hide data using two different typefaces in text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Bacon's Cipher** | 1605 | Bold/italic encode 0/1 | 5 bits/letter [[1]](https://en.wikipedia.org/wiki/Bacon%27s_cipher) [[2]](https://pi.math.cornell.edu/~morris/135/Bacon.pdf) |

**State of the art:** Classic historical method described by Francis Bacon in *De Augmentis Scientiarum* (1623); still used in CTF puzzles and historical cryptography courses.

**Production readiness:** Deprecated
Superseded by every modern method; retained only for educational and puzzle contexts.

**Security status:** Broken
Trivially detected by visual inspection or font-analysis tools; no practical security.

**Community acceptance:** Niche
Historically significant as an early binary encoding scheme; not used in modern steganography.

---

### Null Cipher

**Goal:** Hide message as first letters of words in innocent text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Null Cipher** | 1901 | Acrostic/first letters | Requires long cover [[1]](https://en.wikipedia.org/wiki/Null_cipher) [[2]](https://www.garykessler.net/library/steganography.html) |

**State of the art:** Ancient acrostic technique; the Wikipedia article and Kessler's steganography overview are the canonical modern references.

**Production readiness:** Deprecated
Requires careful, labour-intensive cover-text construction; no automated tooling.

**Security status:** Broken
Detectable by statistical analysis of first-letter frequency distributions.

**Community acceptance:** Niche
Historically notable (used in WWI/WWII messages); purely educational today.

---

### Whitespace Coding

**Goal:** Hide data in whitespace characters of plain text.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Whitespace coding (SNOW)** | 1998 | Trailing spaces/tabs at end of lines | ~3 bits per 8 columns [[1]](https://darkside.com.au/snow/) |

**State of the art:** SNOW (Steganographic Nature Of Whitespace) by Matthew Kwan (1998) is the canonical implementation; simple but easily detectable. Limited capacity but works in any plain-text format.

**Production readiness:** Mature
SNOW is a stable, long-standing tool available on most Unix systems as `stegsnow`.

**Implementations:**
- [snow](https://github.com/mattkwan-zz/snow) ⭐ 50 — C, original SNOW by Matthew Kwan

**Security status:** Caution
Invisible to human readers but trivially detected by checking trailing whitespace; any text editor or diff tool reveals it.

**Community acceptance:** Widely trusted
One of the oldest and best-known text steganography tools; standard CTF challenge technique.

---

### Zero-width Unicode

**Goal:** Hide data using invisible Unicode characters.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Zero-width Unicode** | 2005 | U+200B, U+200C, U+200D, U+FEFF | ~2-3 bit/char [[1]](https://330k.github.io/misc_tools/unicode_steganography.html) |

**State of the art:** Popular for CTF challenges and document fingerprinting. Easily detected by regex or Unicode inspection tools.

**Production readiness:** Experimental
Widely used for document watermarking and leak detection; no formal standard.

**Implementations:**
- [zwsp-steg-js](https://github.com/offdev/zwsp-steg-js) ⭐ 153 — JavaScript, encode/decode hidden messages using zero-width spaces

**Security status:** Caution
Invisible to readers but trivially detected with a Unicode code-point dump or simple regex filter.

**Community acceptance:** Widely trusted
Standard technique in CTF competitions and document-leak tracking; broadly understood.

---

### Homoglyphs

**Goal:** Hide data using visually identical characters from different scripts.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Homoglyphs** | 2000 | Cyrillic а→a, Greek ο→o | 1 bit/char [[1]](https://link.springer.com/chapter/10.1007/978-3-319-22915-7_26) |

**State of the art:** "Dual Stage Text Steganography Using Unicode Homoglyphs" (SSCC 2015, Hosmani et al.) is the key academic reference. Visually indistinguishable but detectable via Unicode script analysis.

**Production readiness:** Experimental
Used for document fingerprinting and leak detection in practice; no standardised library.

**Implementations:**
- [stegtext](https://github.com/btimby/stegtext) ⭐ 3 — Python, homoglyph substitution steganography

**Security status:** Caution
Detected by Unicode normalization, script-mixing analysis, or copy-paste into an ASCII-only context.

**Community acceptance:** Niche
Recognised in security research and CTF; practical use is mainly document watermarking.

---

## Semantic Methods

---

### Chaffing and Winnowing

**Goal:** Separate authentic from chaff messages.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Chaffing** | 1998 | MAC authentication | Rivest [[1]](https://people.csail.mit.edu/rivest/pubs/Riv98a.prepub.txt) |

**State of the art:** Ron Rivest's 1998 paper "Chaffing and Winnowing: Confidentiality without Encryption" remains the definitive reference. Unique authentication-based approach that achieves confidentiality without traditional encryption.

**Production readiness:** Mature
Well-studied theoretical technique; practical implementations exist but niche.

**Security status:** Secure
Security rests on the MAC; an attacker without the key cannot distinguish wheat from chaff.

**Community acceptance:** Widely trusted
Peer-reviewed, broadly cited in cryptography literature; recognised by Bruce Schneier and others.

---

### Mimic Functions

**Goal:** Generate text that encodes secret data using grammar rules.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Mimic Functions** | 1992 | CFG where generated text encodes bits | Wayner [[1]](https://www.tandfonline.com/doi/abs/10.1080/0161-119291866883) |

**State of the art:** Peter Wayner's 1992 Cryptologia paper is the canonical reference. SpamMimic (spammimic.com) is the best-known practical demonstration. Text often sounds unnatural; largely superseded by LLM-based methods.

**Production readiness:** Deprecated
Superseded by neural generative methods; SpamMimic is still online but purely for demonstration.

**Implementations:**
- [SpamMimic](https://www.spammimic.com/) — online demo, encodes messages as spam-like text (original Wayner CFG approach)

**Security status:** Broken
Generated text is statistically detectable as machine-generated; structural patterns are obvious to modern classifiers.

**Community acceptance:** Niche
Historically important as the first generative steganography approach; cited in every linguistic steganography survey.

---

## LLM-Based Methods

---

### Meteor

**Goal:** Information-theoretically secure steganography using LLM probability distributions.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Meteor** | 2021 | Arithmetic coding over LLM log-probabilities [[1]](https://arxiv.org/abs/2105.13080) |

**State of the art:** Best theoretical security. Distribution-preserving — text indistinguishable from normal LLM output without original prompt.

**Production readiness:** Experimental

**Implementations:**
- [meteor-stego](https://github.com/tmthrgd/meteor-stego) ⭐ 215 — Python implementation

**Security status:** Secure — Proven information-theoretically secure against passive warden without prompt access

**Community acceptance:** Widely trusted — Academic breakthrough; practical implementations emerging

---

### Discop

**Goal:** Efficient distribution-preserving steganography using bucket-based sampling.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Discop** | 2023 | Distribution-copy: buckets over token probabilities [[2]](https://arxiv.org/abs/2305.19103) |

**State of the art:** Faster than Meteor but slightly less efficient.

**Production readiness:** Experimental

**Security status:** Secure — Slightly less efficient than Meteor but still distribution-preserving

**Community acceptance:** Emerging — Active research, fewer implementations

---

### ChatStega

**Goal:** Steganography using LLM sampling parameters.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **ChatStega** | 2024 | Sampling with different top-p/temperature in ChatGPT [[1]](https://dl.acm.org/doi/10.1145/3664476.3670930) |

**State of the art:** "Natural Language Steganography by ChatGPT" (ARES 2024, Steinebach) demonstrates using ChatGPT 4.0 to generate stego covers. Simple but depends on LLM sampling randomness.

**Production readiness:** Experimental
Demonstrated in academic paper; no production tooling.

**Security status:** Caution
Detectable with access to the sampling seed or when stego covers are compared statistically against normal ChatGPT output.

**Community acceptance:** Emerging
Growing interest in practical LLM steganography; limited peer review so far.

---

### Blog-Steganography

**Goal:** Hide messages in blog comments across the internet.

| Algorithm | Year | Principle | Note |
|-----------|------|-----------|------|
| **Blog-Stego** | 2011 | Fractionalized + blog selection | Key = blog set [[1]](https://en.wikipedia.org/wiki/List_of_steganography_techniques) [[2]](https://cacm.acm.org/magazines/2014/3/172511-trends-in-steganography/fulltext) |

**State of the art:** Described in the steganography techniques literature and surveyed in "Trends in Steganography" (CACM 2014); encrypted message fragments are posted as comments on pre-agreed orphaned blogs, with the set of blogs acting as the symmetric key.

**Production readiness:** Experimental
No known production implementation; described as a concept in surveys.

**Security status:** Secure
Distributed nature makes traffic analysis hard; security relies on key (blog set) secrecy and encryption of payload.

**Community acceptance:** Niche
Mentioned in academic surveys; no tooling or adoption beyond conceptual description.

---

### Range Coding

**Goal:** Provably secure linguistic steganography using range coding.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Range Coding** | 2025 | Efficient provably secure linguistic steganography via range coding [[1]](https://arxiv.org/abs/2604.08052) |

**State of the art:** Combines theoretical security with practical efficiency.

**Production readiness:** Experimental

**Security status:** Secure — Provably secure

**Community acceptance:** Emerging — Active research

---

### Anchored Sliding Window (ASW)

**Goal:** Robust linguistic steganography resistant to text modifications.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **ASW** | 2026 | Anchored sliding window for robustness against edits [[1]](https://arxiv.org/abs/2604.09066) |

**State of the art:** Addresses fragility of previous methods to minor text modifications.

**Production readiness:** Experimental

**Security status:** Secure — Robust to modifications

**Community acceptance:** Emerging

---

### ReTokSync

**Goal:** Solve tokenization disambiguation in generative linguistic steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **ReTokSync** | 2026 | Self-synchronizing tokenization disambiguation [[1]](https://arxiv.org/abs/2604.25486) |

**State of the art:** Fixes decoding failures from tokenization ambiguity.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Entropy-Driven Rank-Token Mapping

**Goal:** High-capacity linguistic steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Entropy-Driven** | 2025 | Entropy-driven rank-token mapping [[1]](https://arxiv.org/abs/2510.23035) |

**State of the art:** Addresses capacity limitations in prior methods.

**Production readiness:** Experimental

**Security status:** Caution

**Community acceptance:** Emerging

---

### Auto-Stega

**Goal:** Agent-driven system for adaptive steganography strategy.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Auto-Stega** | 2025 | Agent-driven lifelong strategy evolution [[1]](https://arxiv.org/abs/2510.06565) |

**State of the art:** Dynamic strategy selection for varying conditions.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Dynamic Codebook

**Goal:** Text steganography with dynamic codebook using LLMs.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Dynamic Codebook** | 2026 | Text steganography with dynamic codebook [[1]](https://arxiv.org/abs/2604.20269) |

**State of the art:** Addresses white-box paradigm limitations.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### OD-Stega

**Goal:** Relatively secure steganography via optimized distributions.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **OD-Stega** | 2024 | LLM-based relatively secure steganography [[1]](https://arxiv.org/abs/2410.04328) |

**State of the art:** Uses optimized distributions for better security.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Shifting-Merging

**Goal:** Secure, high-capacity and efficient LLM-based steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Shifting-Merging** | 2025 | Shifting-merging approach [[1]](https://arxiv.org/abs/2501.00786) |

**State of the art:** Combines high capacity with efficiency.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Semantic Steganography (LLM)

**Goal:** Robust and high-capacity information hiding using LLMs.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Semantic Stega** | 2025 | Semantic steganography framework [[1]](https://arxiv.org/abs/2412.11043) |

**State of the art:** Bridges semantic richness with steganographic capacity.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Content-Preserving Linguistic Steganography

**Goal:** Preserve original content while embedding secret messages.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Content-Preserving** | 2025 | Content-preserving secure linguistic steganography [[1]](https://arxiv.org/abs/2511.12565) |

**State of the art:** Reduces detectable deviations between normal and stego text.

**Production readiness:** Experimental

**Security status:** Secure

**Community acceptance:** Emerging

---

### Raster Domain Text Steganography

**Goal:** Embed heterogeneous data directly into pixel space of rendered textual glyphs.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Raster Domain Text** | 2025 | Unified framework for multimodal secure embedding into glyph bitmaps [[1]](https://arxiv.org/abs/2512.21698) |

**State of the art:** Operates after font rasterization, treating each glyph as a cover.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Alkaid (Provably Secure Steganography)

**Goal:** Resilience to edit errors via distance-constrained encoding.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Alkaid** | 2026 | Distance-constrained encoding for edit error resilience [[1]](https://arxiv.org/abs/2603.06169) |

**State of the art:** Bridges gap between provably secure steganography and real-world edit errors.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging

---

### SparSamp (Sparse Sampling)

**Goal:** Efficient provably secure steganography via sparse sampling.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **SparSamp** | 2025 | Sparse sampling for efficient provable security [[1]](https://arxiv.org/abs/2503.19499) |

**State of the art:** Improves efficiency of provably secure steganography.

**Production readiness:** Research

**Implementations:** Academic prototypes only

**Security status:** Secure

**Community acceptance:** Emerging

---

### Kolmogorov Complexity Bounds

**Goal:** Information-theoretic cost bounds for LLM steganography.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Kolmogorov Bounds** | 2026 | Theoretical framework for LLM steganography cost [[1]](https://arxiv.org/abs/2603.21567) |

**State of the art:** First formal analysis of LLM steganography complexity.

**Production readiness:** Research

**Security status:** Theoretical foundation

**Community acceptance:** Emerging

---

### STEAD (Robust Provably Secure Linguistic Steganography)

**Goal:** Robust provably secure linguistic steganography with diffusion language models.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **STEAD** | 2026 | Diffusion LM-based robust PSLS [[1]](https://arxiv.org/abs/2601.14778) |

**State of the art:** Combines provable security with diffusion model robustness.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### Hide and Seek in Embedding Space

**Goal:** Low-recoverability steganography using embedding-space geometry.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Embedding Space** | 2026 | Geometry-based steganography in LLM embeddings [[1]](https://arxiv.org/abs/2601.22818) |

**State of the art:** Replaces arbitrary mappings with embedding-derived ones.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### StegoStylo

**Goal:** Evade stylometric analysis through adversarial steganographic stitching.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **StegoStylo** | 2026 | Adversarial stylometry combined with steganography [[1]](https://arxiv.org/abs/2601.09056) |

**State of the art:** Uses adversarial attack to confound stylometric analysis.

**Production readiness:** Research

**Security status:** Caution

**Community acceptance:** Emerging

---

### Undetectable Conversations

**Goal:** Covert communication between AI agents using pseudorandom noise-resilient key exchange.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Undetectable Conversations** | 2026 | Optimal-rate covert conversation with interaction-unique keys [[1]](https://arxiv.org/abs/2604.04757) |

**State of the art:** Combines watermarking and steganography for hidden channel.

**Production readiness:** Research

**Security status:** Secure

**Community acceptance:** Emerging

---

### TrojanStego

**Goal:** LLM as steganographic channel for privacy leaking via fine-tuning.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **TrojanStego** | 2025 | Fine-tuned LLM embeds sensitive context into outputs [[1]](https://arxiv.org/abs/2505.20118) |

**State of the art:** Compromised LLM maintains safety facade while leaking data.

**Production readiness:** Research — Security threat model

**Security status:** Caution

**Community acceptance:** Controversial

---

### GTSD (Generative Text Steganography via Diffusion)

**Goal:** Generative text steganography using diffusion language models.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **GTSD** | 2025 | Diffusion model-based text steganography addressing autoregressive limitations [[1]](https://arxiv.org/abs/2504.19433) |

**State of the art:** Overcomes sequential generation limitations of autoregressive models.

**Production readiness:** Research

**Security status:** Emerging

**Community acceptance:** Emerging

---

### Provably Secure Steganography Based on List Decoding

**Goal:** Theoretical foundation for steganography using list decoding.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **List Decoding** | 2026 | Provably secure steganography with theoretical guarantees [[1]](https://arxiv.org/abs/2604.21394) |

**State of the art:** Provides mathematical security proofs for steganographic schemes.

**Production readiness:** Research

**Security status:** Secure — Provably secure

**Community acceptance:** Emerging

---

### Addressing Tokenization Inconsistency

**Goal:** Address tokenization inconsistency between steganography sender and receiver in LLM-based methods.

| Algorithm | Year | Description |
|-----------|------|-------------|
| **Addressing Tokenization Inconsistency** | 2025 | Resolves tokenization discrepancies between encoder/decoder in LLM steganography [[1]](https://arxiv.org/abs/2508.20718) |

**State of the art:** Proposes tokenization alignment methods for reliable message extraction.

**Production readiness:** Research

**Security status:** Caution — Requires synchronized tokenizers

**Community acceptance:** Emerging

## Recent arXiv Papers (2024–2026)

---

### Safeguarding LLMs Against Misuse and AI-Driven Malware Using Steganographic Canaries

**Goal:** symbolic encodings (whitespace substitution, zero-width character insertion, homoglyph substitution), while Mode B generates synthetic canary documents using linguistic steganography (arithmetic co...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Safeguarding LLMs Against Misuse and AI-Driven Malware Using** | 2026 | cs.CR | Md Raz et al. [[1]](https://arxiv.org/abs/2603.28655) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Decision-Theoretic Formalisation of Steganography With Applications to LLM Monitoring

**Goal:** capabilities could allow misaligned models to evade oversight mechanisms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Decision-Theoretic Formalisation of Steganography With App** | 2026 | cs.AI, cs.CL, cs.CR | Usman Anwar et al. [[1]](https://arxiv.org/abs/2602.23163) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### AndroWasm: an Empirical Study on Android Malware Obfuscation through WebAssembly

**Goal:** increasingly adopted sophisticated techniques to bypass automatic detection mechanisms and harden manual analysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **AndroWasm: an Empirical Study on Android Malware Obfuscation** | 2026 | cs.CR | Diego Soi et al. [[1]](https://arxiv.org/abs/2602.18082) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Verifying LLM Inference to Detect Model Weight Exfiltration

**Goal:** servers grows accordingly.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Verifying LLM Inference to Detect Model Weight Exfiltration** | 2026 | cs.CR, cs.LG | Roy Rinberg et al. [[1]](https://arxiv.org/abs/2511.02620) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Unveiling Unicode's Unseen Underpinnings in Undermining Authorship Attribution

**Goal:** profiling. In this paper, we dissect the technique of stylometry, discuss an antithetical counter-strategy in adversarial stylometry, and devise enhancements through Unicode steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Unveiling Unicode's Unseen Underpinnings in Undermining Auth** | 2026 | cs.CR, cs.CL, cs.IR | Robert Dilworth [[1]](https://arxiv.org/abs/2508.15840) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding in Plain Sight: A Steganographic Approach to Stealthy LLM Jailbreaks

**Goal:** intent) and linguistic stealth (appearing natural), leaving them vulnerable to detection.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding in Plain Sight: A Steganographic Approach to Stealthy** | 2026 | cs.CR, cs.AI | Jianing Geng et al. [[1]](https://arxiv.org/abs/2505.16765) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Provable Secure Steganography Based on Adaptive Dynamic Sampling

**Goal:** The security of private communication is increasingly at risk due to widespread surveillance.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Provable Secure Steganography Based on Adaptive Dynamic Samp** | 2026 | cs.CR, cs.CL | Kaiyi Pang, Minhao Bai [[1]](https://arxiv.org/abs/2504.12579) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Plug-and-Hide: Provable and Adjustable Diffusion Generative Steganography

**Goal:** Diffusion model-based generative image steganography (DM-GIS) is an emerging paradigm that leverages the generative power of diffusion models to conceal secret messages without requiring pre-existi...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Plug-and-Hide: Provable and Adjustable Diffusion Generative ** | 2026 | cs.CR | Jiahao Zhu et al. [[1]](https://arxiv.org/abs/2409.04878) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Odysseus: Jailbreaking Commercial Multimodal LLM-integrated Systems via Dual Steganography

**Goal:** leading to a false sense of security in existing MLLM-integrated systems.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Odysseus: Jailbreaking Commercial Multimodal LLM-integrated ** | 2025 | cs.CR, cs.AI, cs.LG | Songze Li et al. [[1]](https://arxiv.org/abs/2512.20168) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Defining Cost Function of Steganography with Large Language Models

**Goal:** In this paper, we make the first attempt towards defining cost function of steganography with large language models (LLMs), which is totally different from previous works that rely heavily on exper...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Defining Cost Function of Steganography with Large Language ** | 2025 | cs.CR | Hanzhou Wu, Yige Wang [[1]](https://arxiv.org/abs/2512.09769) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A High-Capacity and Secure Disambiguation Algorithm for Neural Linguistic Steganography

**Goal:** Neural linguistic steganography aims to embed information into natural text while preserving statistical undetectability.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A High-Capacity and Secure Disambiguation Algorithm for Neur** | 2025 | cs.CL, cs.AI, cs.CR | Yapei Feng et al. [[1]](https://arxiv.org/abs/2510.02332) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Invisible Injections: Exploiting Vision-Language Models Through Steganographic Prompt Embedding

**Goal:** steganographic methods, achieving an overall attack success rate of 24.3% (plus or minus 3.2%, 95% CI) across leading VLMs including GPT-4V, Claude, and LLaVA, with neural steganography methods rea...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invisible Injections: Exploiting Vision-Language Models Thro** | 2025 | cs.CR | Chetan Pathade [[1]](https://arxiv.org/abs/2507.22304) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Singularity Cipher: A Topology-Driven Cryptographic Scheme Based on Visual Paradox and Klein Bottle Illusions

**Goal:** conventional ciphers that rely solely on algebraic complexity, the Singularity Cipher introduces a dual-layer approach: symbolic encryption rooted in topology and visual steganography designed for ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Singularity Cipher: A Topology-Driven Cryptographic Scheme B** | 2025 | cs.CR | Abraham Itzhak Weinberg [[1]](https://arxiv.org/abs/2507.21097) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Favicon Trojans: Executable Steganography Via Ico Alpha Channel Exploitation

**Goal:** This paper presents a novel method of executable steganography using the alpha transparency layer of ICO image files to embed and deliver self-decompressing JavaScript payloads within web browsers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Favicon Trojans: Executable Steganography Via Ico Alpha Chan** | 2025 | cs.CR | David Noever, Forrest McKee [[1]](https://arxiv.org/abs/2507.09074) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Early Signs of Steganographic Capabilities in Frontier LLMs

**Goal:** Monitoring Large Language Model (LLM) outputs is crucial for mitigating risks from misuse and misalignment.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Early Signs of Steganographic Capabilities in Frontier LLMs** | 2025 | cs.CR, cs.AI, cs.CL | Artur Zolkowski et al. [[1]](https://arxiv.org/abs/2507.02737) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Efficient Blockchain-based Steganography via Backcalculating Generative Adversarial Network

**Goal:** Blockchain-based steganography enables data hiding via encoding the covert data into a specific blockchain transaction field.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Efficient Blockchain-based Steganography via Backcalculating** | 2025 | cs.CR | Zhuo Chen et al. [[1]](https://arxiv.org/abs/2506.16023) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Dual-Layer Image Encryption Framework Using Chaotic AES with Dynamic S-Boxes and Steganographic QR Codes

**Goal:** via steganographically modified QR codes.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Dual-Layer Image Encryption Framework Using Chaotic AES wi** | 2025 | cs.CR | Md Rishadul Bayesh, Dabbrata Das, Md Ahadullah [[1]](https://arxiv.org/abs/2506.13895) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Pixel-Sensitive and Robust Steganography Based on Polar Codes

**Goal:** Steganography is an information hiding technique for covert communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Pixel-Sensitive and Robust Steganography Based on Polar Code** | 2025 | cs.CR, cs.IT | Yujun Ji et al. [[1]](https://arxiv.org/abs/2506.07404) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Dynamic Encryption-Based Cloud Security Model using Facial Image and Password-based Key Generation for Multimedia Data

**Goal:** In this cloud-dependent era, various security techniques, such as encryption, steganography, and hybrid approaches, have been utilized in cloud computing to enhance security, maintain enormous stor...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Dynamic Encryption-Based Cloud Security Model using Facial I** | 2025 | cs.CR | Naima Sultana Ayesha et al. [[1]](https://arxiv.org/abs/2505.17224) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Cryptologic Techniques and Associated Risks in Public and Private Security. An Italian and European Union Perspective with an Overview of the Current Legal Framework

**Goal:** of cryptologic techniques and their implications for public and private security, focusing on the Italian and EU legal frameworks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Cryptologic Techniques and Associated Risks in Public and Pr** | 2025 | cs.CR | Zana Kudriasova [[1]](https://arxiv.org/abs/2505.08650) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### The Steganographic Potentials of Language Models

**Goal:** The potential for large language models (LLMs) to hide messages within plain text (steganography) poses a challenge to detection and thwarting of unaligned AI agents, and undermines faithfulness of...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **The Steganographic Potentials of Language Models** | 2025 | cs.AI, cs.CR, cs.LG | Artem Karpov et al. [[1]](https://arxiv.org/abs/2505.03439) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Unified Steganography via Implicit Neural Representation

**Goal:** Digital steganography is the practice of concealing for encrypted data transmission.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Unified Steganography via Implicit Neural Representation** | 2025 | cs.CR | Qi Song et al. [[1]](https://arxiv.org/abs/2505.01749) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Character-based Diffusion Embedding Algorithm for Enhancing the Generation Quality of Generative Linguistic Steganographic Texts

**Goal:** Generating high-quality steganographic text is a fundamental challenge in the field of generative linguistic steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Character-based Diffusion Embedding Algorithm for Enhancin** | 2025 | cs.CL, cs.CR | Yingquan Chen et al. [[1]](https://arxiv.org/abs/2505.00977) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Robust Steganography from Large Language Models

**Goal:** the randomness of an encryption scheme to destroy the hidden message while preserving an acceptable covertext to ordinary users.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Robust Steganography from Large Language Models** | 2025 | cs.CR | Neil Perry et al. [[1]](https://arxiv.org/abs/2504.08977) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganographic Embeddings as an Effective Data Augmentation

**Goal:** Image Steganography is a cryptographic technique that embeds secret information into an image, ensuring the hidden data remains undetectable to the human eye while preserving the image's original v...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganographic Embeddings as an Effective Data Augmentation** | 2025 | cs.CR, cs.LG, cs.MM | Nicholas DiSalvo [[1]](https://arxiv.org/abs/2502.15245) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Mixing Algorithm for Extending the Tiers of the Unapparent Information Send through the Audio Streams

**Goal:** the survival of the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Mixing Algorithm for Extending the Tiers of the Unapparent I** | 2025 | cs.CR | Sachith Dassanayaka [[1]](https://arxiv.org/abs/2502.12544) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Sound Conveyors for Stealthy Data Transmission

**Goal:** tend to figure out a method capable of hiding a message and the survival of the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Sound Conveyors for Stealthy Data Transmission** | 2025 | cs.CR | Sachith Dassanayaka [[1]](https://arxiv.org/abs/2502.10984) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Relatively-Secure LLM-Based Steganography via Constrained Markov Decision Processes

**Goal:** Linguistic steganography aims to conceal information within natural language text without being detected.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Relatively-Secure LLM-Based Steganography via Constrained Ma** | 2025 | cs.IT | Yu-Shin Huang et al. [[1]](https://arxiv.org/abs/2502.01827) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Stealthy Backdoor Attack to Real-world Models in Android Apps

**Goal:** attacks on real-world DL models extracted from mobile apps.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Stealthy Backdoor Attack to Real-world Models in Android App** | 2025 | cs.CR, cs.AI | Jiali Wei et al. [[1]](https://arxiv.org/abs/2501.01263) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Plug-and-Play Method for Improving Imperceptibility and Capacity in Practical Generative Text Steganography

**Goal:** Linguistic steganography embeds secret information into seemingly innocuous text to safeguard privacy under surveillance.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Plug-and-Play Method for Improving Imperceptibility and Ca** | 2025 | cs.CR | Kaiyi Pang [[1]](https://arxiv.org/abs/2412.19652) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography and Probabilistic Risk Analysis: A Game Theoretical Framework for Quantifying Adversary Advantage and Impact

**Goal:** enable the assessment of success rates, illustrating conditions under which the company benefits from hiding messages or faces increased risks when not implementing steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography and Probabilistic Risk Analysis: A Game Theore** | 2025 | cs.GT, cs.CR | Obinna Omego et al. [[1]](https://arxiv.org/abs/2412.17950) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hidden in Plain Text: Emergence & Mitigation of Steganographic Collusion in LLMs

**Goal:** from unsafe interactions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hidden in Plain Text: Emergence & Mitigation of Steganograph** | 2025 | cs.CL, cs.CR, cs.LG | Yohan Mathew et al. [[1]](https://arxiv.org/abs/2410.03768) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Secret Collusion among AI Agents: Multi-Agent Deception via Steganography

**Goal:** the problem of secret collusion in systems of generative AI agents by drawing on relevant concepts from both AI and security literature.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secret Collusion among AI Agents: Multi-Agent Deception via ** | 2025 | cs.AI, cs.CR | Sumeet Ramesh Motwani et al. [[1]](https://arxiv.org/abs/2402.07510) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Dynamically Allocated Interval-Based Generative Linguistic Steganography with Roulette Wheel

**Goal:** Existing linguistic steganography schemes often overlook the conditional probability (CP) of tokens in the candidate pool, allocating the one coding to all tokens, which results in identical select...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Dynamically Allocated Interval-Based Generative Linguistic S** | 2025 | cs.CL | Yihao Wang et al. [[1]](https://arxiv.org/abs/2401.15656) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Sanitizing Hidden Information with Diffusion Models

**Goal:** data within another form of data, often to conceal its existence or prevent unauthorized access.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Sanitizing Hidden Information with Diffusion Models** | 2025 | cs.CR | Preston K. Robinette, Daniel Moyer, Taylor T. Johnson [[1]](https://arxiv.org/abs/2310.06951) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Very recent arXiv preprint; no production implementation known.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Robust Steganography with Boundary-Preserving Overflow Alleviation and Adaptive Error Correction

**Goal:** With the rapid evolution of the Internet, the vast amount of data has created opportunities for fostering the development of steganographic techniques.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Robust Steganography with Boundary-Preserving Overflow Allev** | 2024 | cs.CR, cs.MM | Yu Cheng, Zhenlin Luo, Zhaoxia Yin [[1]](https://arxiv.org/abs/2411.13819) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### ADLM -- stega: A Universal Adaptive Token Selection Algorithm for Improving Steganographic Text Quality via Information Entropy

**Goal:** have become focal points.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ADLM -- stega: A Universal Adaptive Token Selection Algorith** | 2024 | cs.CR, cs.AI | Zezheng Qin et al. [[1]](https://arxiv.org/abs/2410.20825) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Steganography and Watermarking For Medical Image Integrity

**Goal:** making or changing a diagnosis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Steganography and Watermarking For Medical Image Integ** | 2024 | cs.CR, cs.GR | Givon Zirkind [[1]](https://arxiv.org/abs/2410.09071) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Model X-Ray: Detection of Hidden Malware in AI Model Weights using Few Shot Learning

**Goal:** strategy to ensure the trained models are generic concerning various factors.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Model X-Ray: Detection of Hidden Malware in AI Model Weights** | 2024 | cs.CR, cs.AI | Daniel Gilkarov, Ran Dubin [[1]](https://arxiv.org/abs/2409.19310) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Provably Robust and Secure Steganography in Asymmetric Resource Scenario

**Goal:** To circumvent the unbridled and ever-encroaching surveillance and censorship in cyberspace, steganography has garnered attention for its ability to hide private information in innocent-looking carr...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Provably Robust and Secure Steganography in Asymmetric Resou** | 2024 | cs.CR | Minhao Bai et al. [[1]](https://arxiv.org/abs/2407.13499) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image steganography based on generative implicit neural representation

**Goal:** In the realm of advanced steganography, the scale of the model typically correlates directly with the resolution of the fundamental grid, necessitating the training of a distinct neural network for...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image steganography based on generative implicit neural repr** | 2024 | cs.CR | Zhong Yangjie et al. [[1]](https://arxiv.org/abs/2406.01918) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Computing Low-Entropy Couplings for Large-Support Distributions

**Goal:** Minimum-entropy coupling (MEC) -- the process of finding a joint distribution with minimum entropy for given marginals -- has applications in areas such as causality and steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Computing Low-Entropy Couplings for Large-Support Distributi** | 2024 | cs.IT, cs.CR | Samuel Sokota et al. [[1]](https://arxiv.org/abs/2405.19540) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Sensitive Information Using PDF Steganography

**Goal:** The use of steganography to transmit secret data is becoming increasingly common in security products and malware today.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Sensitive Information Using PDF Steganography** | 2024 | cs.CR | Ryan Klemm, Bo Chen [[1]](https://arxiv.org/abs/2405.00865) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Extensive Survey of Digital Image Steganography: State of the Art

**Goal:** The need to protect sensitive information privacy duringinformation exchange over the internet/intranet has led towider adoption of cryptography and steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Extensive Survey of Digital Image Steganography: State of** | 2024 | cs.ET, cs.CR | Idakwo M. A. et al. [[1]](https://arxiv.org/abs/2404.19548) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Boosting Digital Safeguards: Blending Cryptography and Steganography

**Goal:** access and exploitation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Boosting Digital Safeguards: Blending Cryptography and Stega** | 2024 | cs.CR, cs.LG | Anamitra Maiti et al. [[1]](https://arxiv.org/abs/2404.05985) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Provably Secure Disambiguating Neural Linguistic Steganography

**Goal:** Recent research in provably secure neural linguistic steganography has overlooked a crucial aspect: the sender must detokenize stegotexts to avoid raising suspicion from the eavesdropper.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Provably Secure Disambiguating Neural Linguistic Steganograp** | 2024 | cs.CR, cs.CL | Yuang Qi et al. [[1]](https://arxiv.org/abs/2403.17524) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Zero-shot Generative Linguistic Steganography

**Goal:** Generative linguistic steganography attempts to hide secret messages into covertext.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Zero-shot Generative Linguistic Steganography** | 2024 | cs.CL, cs.CR | Ke Lin et al. [[1]](https://arxiv.org/abs/2403.10856) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Pseudorandom Error-Correcting Codes

**Goal:** from text output by the original model.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Pseudorandom Error-Correcting Codes** | 2024 | cs.CR, cs.AI, cs.LG | Miranda Christ, Sam Gunn [[1]](https://arxiv.org/abs/2402.09370) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Implicit Steganography Beyond the Constraints of Modality

**Goal:** Cross-modal steganography is committed to hiding secret information of one modality in another modality.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Implicit Steganography Beyond the Constraints of Modality** | 2024 | cs.CR, cs.LG | Sojeong Song et al. [[1]](https://arxiv.org/abs/2312.05496) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding in Plain Sight: Towards the Science of Linguistic Steganography

**Goal:** Covert communication (also known as steganography) is the practice of concealing a secret inside an innocuous-looking public object (cover) so that the modified public object (covert code) makes se...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding in Plain Sight: Towards the Science of Linguistic Ste** | 2023 | cs.CL, cs.CR | Leela Raj-Sankar, S. Raj Rajagopalan [[1]](https://arxiv.org/abs/2312.16840) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Secure Information Embedding in Images with Hybrid Firefly Algorithm

**Goal:** secure access to sensitive information over time, such as the many cryptographic methods in use to facilitate secure communications on the internet.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secure Information Embedding in Images with Hybrid Firefly A** | 2023 | cs.CR, cs.LG | Sahil Nokhwal, Manoj Chandrasekharan, Ankit Chaudhary [[1]](https://arxiv.org/abs/2312.13519) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Residual-guided Learning Method for Image Steganography

**Goal:** Traditional steganographic techniques have often relied on manually crafted attributes related to image residuals.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Residual-guided Learning Method for Image Steganogra** | 2023 | cs.CR | Miaoxin Ye et al. [[1]](https://arxiv.org/abs/2312.01080) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegGuard: Fingerprinting Self-supervised Pre-trained Encoders via Secrets Embeder and Extractor

**Goal:** In this work, we propose StegGuard, a novel fingerprinting mechanism to verify the ownership of the suspect pre-trained encoder using steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegGuard: Fingerprinting Self-supervised Pre-trained Encode** | 2023 | cs.CR | Xingdong Ren et al. [[1]](https://arxiv.org/abs/2310.03380) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Disarming Steganography Attacks Inside Neural Network Models

**Goal:** there are endless ways to hide the attacks, we focus on a zero-trust prevention strategy based on AI model attack disarm and reconstruction.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Disarming Steganography Attacks Inside Neural Network Models** | 2023 | cs.CR, cs.MM | Ran Dubin [[1]](https://arxiv.org/abs/2309.03071) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On the Steganographic Capacity of Selected Learning Models

**Goal:** scenarios. For example, previous research has shown that malware can be hidden in deep learning models.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On the Steganographic Capacity of Selected Learning Models** | 2023 | cs.LG, cs.CR, cs.MM | Rishit Agrawal et al. [[1]](https://arxiv.org/abs/2308.15502) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Introducing a New Evaluation Criteria for EMD-Base Steganography Method

**Goal:** Steganography is a technique to hide the presence of secret communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Introducing a New Evaluation Criteria for EMD-Base Steganogr** | 2023 | cs.CR, cs.MM | Hanieh Rafiee, Mojtaba Mahdavi, AhmadReza NaghshNilchi [[1]](https://arxiv.org/abs/2308.07970) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Open Image Content Disarm And Reconstruction

**Goal:** cutting-edge Artificial Intelligence and content signature exist, evasive malware successfully bypasses next-generation malware detection using advanced methods like steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Open Image Content Disarm And Reconstruction** | 2023 | cs.CR, cs.AI | Eli Belkind, Ran Dubin, Amit Dvir [[1]](https://arxiv.org/abs/2307.14057) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Deep Cross-Modal Steganography Using Neural Representations

**Goal:** Steganography is the process of embedding secret data into another message or data, in such a way that it is not easily noticeable.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Deep Cross-Modal Steganography Using Neural Representations** | 2023 | cs.CR, cs.AI | Gyojin Han et al. [[1]](https://arxiv.org/abs/2307.08671) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Errorless Robust JPEG Steganography Using Steganographic Polar Codes

**Goal:** Recently, a robust steganographic algorithm that achieves errorless robustness against JPEG recompression is proposed.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Errorless Robust JPEG Steganography Using Steganographic Pol** | 2023 | cs.CR, cs.MM | Jimin Zhang, Xianfeng Zhao, Xiaolei He [[1]](https://arxiv.org/abs/2306.15246) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Off-By-One Implementation Error in J-UNIWARD

**Goal:** J-UNIWARD is a popular steganography method for hiding secret messages in JPEG cover images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Off-By-One Implementation Error in J-UNIWARD** | 2023 | cs.CR, cs.LG, cs.MM | Benedikt Lorch [[1]](https://arxiv.org/abs/2305.19776) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### The Realizations of Steganography in Encrypted Domain

**Goal:** in cloud service and social network, ciphertext has been gradually becoming a common platform for public to exchange data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **The Realizations of Steganography in Encrypted Domain** | 2023 | cs.CR | Yan Ke et al. [[1]](https://arxiv.org/abs/2304.02614) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### ICStega: Image Captioning-based Semantically Controllable Linguistic Steganography

**Goal:** Nowadays, social media has become the preferred communication platform for web users but brought security threats.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **ICStega: Image Captioning-based Semantically Controllable Li** | 2023 | cs.CR | Xilong Wang et al. [[1]](https://arxiv.org/abs/2303.05830) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography of Steganographic Networks

**Goal:** Steganography is a technique for covert communication between two parties.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography of Steganographic Networks** | 2023 | cs.CR, cs.AI | Guobiao Li et al. [[1]](https://arxiv.org/abs/2302.14521) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Paradigm for Improved Image Steganography by using Adaptive Number of Dominant Discrete Cosine Transform Coefficients

**Goal:** Image steganography camouflages secret messages in images by tampering image contents.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Paradigm for Improved Image Steganography by using Ada** | 2023 | cs.CR | Laeeq Aslam Sandhu et al. [[1]](https://arxiv.org/abs/2301.09185) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Blind Spots: Automatically detecting ignored program inputs

**Goal:** A blind spot is any input to a program that can be arbitrarily mutated without affecting the program's output.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Blind Spots: Automatically detecting ignored program inputs** | 2023 | cs.CR, cs.PL | Henrik Brodin, Evan Sultanik, Marek Surovič [[1]](https://arxiv.org/abs/2301.08700) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Improving Robustness of TCM-based Robust Steganography with Variable Robustness

**Goal:** JPEG image can form an embedding domain that is robust to recompression, which is called transport channel matching (TCM) method.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improving Robustness of TCM-based Robust Steganography with ** | 2023 | cs.CR | Jimin Zhang, Xianfeng Zhao, Xiaolei He [[1]](https://arxiv.org/abs/2211.10095) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Perfectly Secure Steganography Using Minimum Entropy Coupling

**Goal:** Steganography is the practice of encoding secret information into innocuous content in such a manner that an adversarial third party would not realize that there is hidden meaning.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Perfectly Secure Steganography Using Minimum Entropy Couplin** | 2023 | cs.CR, cs.AI, cs.MM | Christian Schroeder de Witt et al. [[1]](https://arxiv.org/abs/2210.14889) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Research
Academic prototype; implementation details in paper.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Addressing Segmentation Ambiguity in Neural Linguistic Steganography

**Goal:** Previous studies on neural linguistic steganography, except Ueoka et al.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Addressing Segmentation Ambiguity in Neural Linguistic Stega** | 2022 | cs.CL | Jumon Nozaki, Yugo Murawaki [[1]](https://arxiv.org/abs/2211.06662) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Cover Reproducible Steganography via Deep Generative Models

**Goal:** Whereas cryptography easily arouses attacks by means of encrypting a secret message into a suspicious form, steganography is advantageous for its resilience to attacks by concealing the message in ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Cover Reproducible Steganography via Deep Generative Models** | 2022 | cs.CR, cs.MM | Kejiang Chen et al. [[1]](https://arxiv.org/abs/2210.14632) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Information-Theoretic Bounds for Steganography in Multimedia

**Goal:** Steganography in multimedia aims to embed secret data into an innocent looking multimedia cover object.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information-Theoretic Bounds for Steganography in Multimedia** | 2022 | cs.MM, cs.CR | Hassan Y. El Arsh et al. [[1]](https://arxiv.org/abs/2207.04521) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Matryoshka: Stealing Functionality of Private ML Data by Hiding Models in Model

**Goal:** memorize the functionality of private ML data stored in local data centers.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Matryoshka: Stealing Functionality of Private ML Data by Hid** | 2022 | stat.ML, cs.AI, cs.CR | Xudong Pan et al. [[1]](https://arxiv.org/abs/2206.14371) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Survey On Semantic Steganography Systems

**Goal:** Steganography is the practice of concealing a message within some other carrier or cover message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Survey On Semantic Steganography Systems** | 2022 | cs.CR, cs.CL | João Figueira [[1]](https://arxiv.org/abs/2203.12425) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On Information Hiding in Natural Language Systems

**Goal:** today's digital world, research on more robust models of privacy preservation and information security is on the rise.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On Information Hiding in Natural Language Systems** | 2022 | cs.CL | Geetanjali Bihani, Julia Taylor Rayz [[1]](https://arxiv.org/abs/2203.06512) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Semantic-Preserving Linguistic Steganography by Pivot Translation and Semantic-Aware Bins Coding

**Goal:** Linguistic steganography (LS) aims to embed secret information into a highly encoded text for covert communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Semantic-Preserving Linguistic Steganography by Pivot Transl** | 2022 | cs.CR, cs.CL | Tianyu Yang et al. [[1]](https://arxiv.org/abs/2203.03795) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Deep Learning to Detect Digitally Encoded DNA Trigger for Trojan Malware in Bio-Cyber Attacks

**Goal:** from trojan attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Deep Learning to Detect Digitally Encoded DNA Trigger ** | 2022 | cs.CR, cs.LG | Mohd Siblee Islam et al. [[1]](https://arxiv.org/abs/2202.11824) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Pair and Matching Algorithm for Embedding Secret Messages in Images

**Goal:** Steganography has proven to be one of the practical way of securing data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Pair and Matching Algorithm for Embedding Secret Mes** | 2022 | cs.CR, cs.MM | P N Priya et al. [[1]](https://arxiv.org/abs/2202.00253) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Algorithm In Steganography Using Weighted Matching Technique

**Goal:** In recent years, the security related to data over the internet has become a major issue.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Algorithm In Steganography Using Weighted Matching T** | 2022 | cs.CR | P N Priya et al. [[1]](https://arxiv.org/abs/2202.00251) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Data in Colors: Secure and Lossless Deep Image Steganography via Conditional Invertible Neural Networks

**Goal:** Deep image steganography is a data hiding technology that conceal data in digital images via deep neural networks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Data in Colors: Secure and Lossless Deep Image Stegan** | 2022 | cs.CR, cs.AI | Yanzhen Ren et al. [[1]](https://arxiv.org/abs/2201.07444) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image data hiding with multi-scale autoencoder network

**Goal:** mage steganography is the process of hiding information which can be text, image, or video inside a cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image data hiding with multi-scale autoencoder network** | 2022 | cs.CR, cs.MM | Chen-Hsiu Huang, Ja-Ling Wu [[1]](https://arxiv.org/abs/2201.06038) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### SABMIS: Sparse approximation based blind multi-image steganography scheme

**Goal:** We hide grayscale secret images into a grayscale cover image, which is considered to be a challenging steganography problem.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SABMIS: Sparse approximation based blind multi-image stegano** | 2022 | cs.CR | Rohit Agrawal et al. [[1]](https://arxiv.org/abs/2110.11418) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Brief Survey on Deep Learning Based Data Hiding

**Goal:** and outline three commonly used architectures.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Brief Survey on Deep Learning Based Data Hiding** | 2022 | cs.CR, cs.LG, cs.MM | Chaoning Zhang et al. [[1]](https://arxiv.org/abs/2103.01607) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### IoTSign: Protecting Privacy and Authenticity of IoT using Discrete Cosine Based Steganography

**Goal:** Remotely generated data by Intent of Things (IoT) has recently had a lot of attention for their huge benefits such as efficient monitoring and risk reduction.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **IoTSign: Protecting Privacy and Authenticity of IoT using Di** | 2022 | cs.CR | Sharif Abuadbba, Ayman Ibaida, Ibrahim Khalil [[1]](https://arxiv.org/abs/1911.00604) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Maneuvering Digital Watermarking In Face Recognition

**Goal:** digital world are many, which could be resolved with some biometric recognition methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Maneuvering Digital Watermarking In Face Recognition** | 2021 | cs.CR | Osama R. Shahin, Zeinab M. Abdel Azim, Ahmed I Taloba [[1]](https://arxiv.org/abs/2111.02308) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### GANash -- A GAN approach to steganography

**Goal:** altered with respect to a key and using the same, the encoded message is decoded at the receiver side.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **GANash -- A GAN approach to steganography** | 2021 | cs.CR | Venkatesh Subramaniyan et al. [[1]](https://arxiv.org/abs/2110.13650) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography of Complex Networks

**Goal:** Steganography is one of the information hiding techniques, which conceals secret messages in cover media.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography of Complex Networks** | 2021 | cs.CR, cs.SI | Daewon Lee [[1]](https://arxiv.org/abs/2110.10418) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Improving Dither Modulation based Robust Steganography by Overflow Suppression

**Goal:** Nowadays, people are sharing their pictures on online social networks (OSNs), so OSN is a good platform for Steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improving Dither Modulation based Robust Steganography by Ov** | 2021 | cs.CR | Kai Zeng et al. [[1]](https://arxiv.org/abs/2110.08697) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Architecture of Network Camera Photo Authentication Scheme using Steganography Approach

**Goal:** The aim of integrity protection process is not only to secure the send message, but also ensures that the original message is not modified during sending the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Architecture of Network Camera Photo Authentication Scheme u** | 2021 | cs.CR | Ahmad M. Nagm, Khaled Y. Youssef, Mohammad I. Youssef [[1]](https://arxiv.org/abs/2110.01058) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generative Models for Security: Attacks, Defenses, and Opportunities

**Goal:** and malware obfuscation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generative Models for Security: Attacks, Defenses, and Oppor** | 2021 | cs.CR | Luke A. Bauer, Vincent Bindschaedler [[1]](https://arxiv.org/abs/2107.10139) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Provably Secure Generative Linguistic Steganography

**Goal:** Generative linguistic steganography mainly utilized language models and applied steganographic sampling (stegosampling) to generate high-security steganographic text (stegotext).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Provably Secure Generative Linguistic Steganography** | 2021 | cs.CL, cs.CR | Siyu Zhang et al. [[1]](https://arxiv.org/abs/2106.02011) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Frustratingly Easy Edit-based Linguistic Steganography with a Masked Language Model

**Goal:** With advances in neural language models, the focus of linguistic steganography has shifted from edit-based approaches to generation-based ones.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Frustratingly Easy Edit-based Linguistic Steganography with ** | 2021 | cs.CL | Honai Ueoka, Yugo Murawaki, Sadao Kurohashi [[1]](https://arxiv.org/abs/2104.09833) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Permutation Encoding for Text Steganography: A Short Tutorial

**Goal:** We explore a method of encoding secret messages using factoradic numbering of permuted lists of text or numeric elements.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Permutation Encoding for Text Steganography: A Short Tutoria** | 2021 | cs.CR, cs.IT | George D. Montanez [[1]](https://arxiv.org/abs/2104.03881) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Approach to Enhance Security of Visual Cryptography Using Steganography (VisUS)

**Goal:** Steganography is a process that hides secrete message or secrete hologram or secrete video or secrete image whose mere presence within the source data should be undetectable and use for transmittin...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Approach to Enhance Security of Visual Cryptography Us** | 2021 | cs.CR, cs.MM | Uttam Kr. Mondal et al. [[1]](https://arxiv.org/abs/2103.09477) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Blockchain for steganography: advantages, new algorithms and open challenges

**Goal:** Steganography is a solution for covert communication and blockchain is a p2p network for data transmission, so the benefits of blockchain can be used in

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Blockchain for steganography: advantages, new algorithms and** | 2021 | cs.CR | Omid Torki, Maede Ashouri-Talouki, Mojtaba Mahdavi [[1]](https://arxiv.org/abs/2101.03103) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Invisible Backdoor Attack with Sample-Specific Triggers

**Goal:** , training loss, and model structure) as required in many existing attacks.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Invisible Backdoor Attack with Sample-Specific Triggers** | 2021 | cs.CR | Yuezun Li et al. [[1]](https://arxiv.org/abs/2012.03816) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Review and Test of Steganography Techniques

**Goal:** Steganography is the art of concealing a secret message within an appropriate-multimedia carrier such as images, audio, video files, and even network packets.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Review and Test of Steganography Techniques** | 2020 | cs.CR | Joab Kose, Oscar Bautista Chia, Vashish Baboolal [[1]](https://arxiv.org/abs/2012.08460) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### LSB Steganography Using Pixel Locator Sequence with AES

**Goal:** Image steganography is the art of hiding data into images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **LSB Steganography Using Pixel Locator Sequence with AES** | 2020 | cs.CR | Sahil Gangurde, Krishnakant Tiwari [[1]](https://arxiv.org/abs/2012.02494) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Near-imperceptible Neural Linguistic Steganography via Self-Adjusting Arithmetic Coding

**Goal:** Linguistic steganography studies how to hide secret messages in natural language cover texts.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Near-imperceptible Neural Linguistic Steganography via Self-** | 2020 | cs.CL, cs.CR | Jiaming Shen, Heng Ji, Jiawei Han [[1]](https://arxiv.org/abs/2010.00677) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Graph-Stega: Semantic Controllable Steganographic Text Generation Guided by Knowledge Graph

**Goal:** generated steganographic texts; secondly, they can not control the semantic expression of the final generated steganographic text.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Graph-Stega: Semantic Controllable Steganographic Text Gener** | 2020 | cs.CL, cs.CR | Zhongliang Yang et al. [[1]](https://arxiv.org/abs/2006.08339) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography GAN: Cracking Steganography with Cycle Generative Adversarial Networks

**Goal:** information. Specifically, the field of Cryptography is the construction and analysis of protocols that prevent third parties from understanding private messages.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography GAN: Cracking Steganography with Cycle Generat** | 2020 | cs.CR | Nibraas Khan et al. [[1]](https://arxiv.org/abs/2006.04008) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Two high capacity text steganography schemes based on color coding

**Goal:** Text steganography is a mechanism of hiding secret text message inside another text as a covering message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Two high capacity text steganography schemes based on color ** | 2020 | cs.CR | Juvet K. Sadié, Leonel Moyou Metcheka, René Ndoundam [[1]](https://arxiv.org/abs/2004.00948) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### JPEG Steganography and Synchronization of DCT Coefficients for a Given Development Pipeline

**Goal:** This short paper proposes to use the statistical analysis of the correlation between DCT coefficients to design a new synchronization strategy that can be used for cost-based steganographic schemes...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **JPEG Steganography and Synchronization of DCT Coefficients f** | 2020 | cs.MM, cs.CR | Théo Taburet et al. [[1]](https://arxiv.org/abs/2003.10082) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Natural Steganography in JPEG Domain with a Linear Development Pipeline

**Goal:** In order to achieve high practical security, Natural Steganography (NS) uses cover images captured at ISO sensitivity ISO_{1} and generates stego images mimicking ISO sensitivity ISO_{2}>ISO_{1}.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Natural Steganography in JPEG Domain with a Linear Developme** | 2020 | cs.MM, cs.CR | Taburet Théo et al. [[1]](https://arxiv.org/abs/2001.02653) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Differentially Private M-band Wavelet-Based Mechanisms in Machine Learning Environments

**Goal:** and LS+) add noise through a Laplace-Sigmoid distribution that multiplies Laplace-distributed values with the sigmoid function, and the third method utilizes pseudo-quantum steganography to embed n...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Differentially Private M-band Wavelet-Based Mechanisms in Ma** | 2020 | cs.LG, cs.CR, stat.ML | Kenneth Choi, Tony Lee [[1]](https://arxiv.org/abs/2001.00012) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography using a 3 player game

**Goal:** Image steganography aims to securely embed secret information into cover images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography using a 3 player game** | 2020 | cs.MM, cs.CR | Mehdi Yedroudj, Frédéric Comby, Marc Chaumont [[1]](https://arxiv.org/abs/1907.06956) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Adversarial Embedding: A robust and elusive Steganography and Watermarking technique

**Goal:** We propose adversarial embedding, a new steganography and watermarking technique that embeds secret information within images.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Adversarial Embedding: A robust and elusive Steganography an** | 2019 | cs.CR, cs.LG | Salah Ghamizi et al. [[1]](https://arxiv.org/abs/1912.01487) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Behavioral Security in Covert Communication Systems

**Goal:** if we only consider content security and neglect behavioral security.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Behavioral Security in Covert Communication Systems** | 2019 | cs.CR | Zhongliang Yang et al. [[1]](https://arxiv.org/abs/1910.09759) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Blockchain of Signature Material Combining Cryptographic Hash Function and DNA Steganography

**Goal:** should be immune to the fast developments in digital and engineering technologies.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Blockchain of Signature Material Combining Cryptographic Has** | 2019 | bio.BM, cs.CR | Yixin Zhang [[1]](https://arxiv.org/abs/1909.07914) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography: Protection of Digital Properties against Eavesdropping

**Goal:** Steganography is the art of hiding the fact that communication is taking place, by hiding information in other information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography: Protection of Digital Properties agains** | 2019 | cs.MM, cs.CR | Ramita Maharjan, Ajay Kumar Shrestha, Rejina Basnet [[1]](https://arxiv.org/abs/1909.04685) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Neural Linguistic Steganography

**Goal:** Whereas traditional cryptography encrypts a secret message into an unintelligible form, steganography conceals that communication is taking place by encoding a secret message into a cover signal.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Neural Linguistic Steganography** | 2019 | cs.CL, cs.CR, cs.LG | Zachary M. Ziegler, Yuntian Deng, Alexander M. Rush [[1]](https://arxiv.org/abs/1909.01496) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Uncheatable Machine Learning Inference

**Goal:** using probabilistic performance metrics, instance seeding, and steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Uncheatable Machine Learning Inference** | 2019 | cs.LG, cs.CR, stat.ML | Mustafa Canim, Ashish Kundu, Josh Payne [[1]](https://arxiv.org/abs/1908.03270) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography using Gaussian Markov Random Field Model

**Goal:** Recent advances on adaptive steganography show that the performance of image steganographic communication can be improved by incorporating the non-additive models that capture the dependences among...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography using Gaussian Markov Random Field Model** | 2019 | cs.MM, cs.CR | Wenkang Su et al. [[1]](https://arxiv.org/abs/1908.01483) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### EncryptGAN: Image Steganography with Domain Transform

**Goal:** We propose an image steganographic algorithm called EncryptGAN, which disguises private image communication in an open communication channel.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **EncryptGAN: Image Steganography with Domain Transform** | 2019 | cs.MM, cs.CR | Ziqiang Zheng et al. [[1]](https://arxiv.org/abs/1905.11582) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Learning Symmetric and Asymmetric Steganography via Adversarial Training

**Goal:** Steganography refers to the art of concealing secret messages within multiple media carriers so that an eavesdropper is unable to detect the presence and content of the hidden messages.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Learning Symmetric and Asymmetric Steganography via Adversar** | 2019 | cs.CR, cs.LG, cs.MM | Zheng Li et al. [[1]](https://arxiv.org/abs/1903.05297) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generative Steganography by Sampling

**Goal:** In this paper, a novel data-driven information hiding scheme called generative steganography by sampling (GSS) is proposed.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generative Steganography by Sampling** | 2019 | cs.MM, cs.CR | Zhuo Zhang et al. [[1]](https://arxiv.org/abs/1804.10531) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Parallel Message-distribution Technique for Cost-based Steganography

**Goal:** This paper presents two novel approaches to increase performance bounds of image steganography under the criteria of minimizing distortion.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Parallel Message-distribution Technique for Cost-based** | 2019 | cs.MM, cs.CR | Mehdi Sharifzadeh et al. [[1]](https://arxiv.org/abs/1705.08616) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Training Set Camouflage

**Goal:** We introduce a form of steganography in the domain of machine learning which we call training set camouflage.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Training Set Camouflage** | 2018 | cs.CR | Ayon Sen et al. [[1]](https://arxiv.org/abs/1812.05725) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Automatically Generate Steganographic Text Based on Markov Model and Huffman Coding

**Goal:** Steganography, as one of the three basic information security systems, has long played an important role in safeguarding the privacy and confidentiality of data in cyberspace.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Automatically Generate Steganographic Text Based on Markov M** | 2018 | cs.CR | Zhongliang Yang et al. [[1]](https://arxiv.org/abs/1811.04720) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### 2D Hybrid chaos map for image security transform based on framelet and cellular automata

**Goal:** In this paper, we provide some safe ways to transfer images securely by using cryptography and steganography methods.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **2D Hybrid chaos map for image security transform based on fr** | 2018 | cs.CR | Y. Khedmati, R. Parvaz, Y. Behroo [[1]](https://arxiv.org/abs/1810.06333) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A novel method of speech information hiding based on 3D-Magic Matrix

**Goal:** Redundant information of low-bit-rate speech is extremely small, thus it's very difficult to implement large capacity steganography on the low-bit-rate speech.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A novel method of speech information hiding based on 3D-Magi** | 2018 | cs.CR | Zhongliang Yang et al. [[1]](https://arxiv.org/abs/1809.03010) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Tackling Android Stego Apps in the Wild

**Goal:** discoveries closer to real-world implementations, it is important to use data that represent "in the wild" scenarios.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Tackling Android Stego Apps in the Wild** | 2018 | cs.CR | Wenhao Chen et al. [[1]](https://arxiv.org/abs/1808.00430) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography Security: Principle and Practice

**Goal:** This paper focuses on several theoretical issues and principles in steganography security, and defines four security levels by analyzing the corresponding algorithm instances.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography Security: Principle and Practice** | 2018 | cs.MM, cs.CR | Yan Ke et al. [[1]](https://arxiv.org/abs/1806.03618) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Application of Lowner-John Ellipsoid in the Steganography of Lattice Vectors and a Review of The Gentry's FHE

**Goal:** In this paper, first, we utilize the Lowner-John ellipsoid of a convex set to hide the lattice data information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Application of Lowner-John Ellipsoid in the Steganography of** | 2018 | cs.CR | Hossein Mohades, Mohamad Kadkhoda, Mohamad Mahdi Mohades [[1]](https://arxiv.org/abs/1804.10246) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### The Reincarnation of Grille Cipher: A Generative Approach

**Goal:** have been implemented to encrypt and decrypt the secret data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **The Reincarnation of Grille Cipher: A Generative Approach** | 2018 | cs.CR | Jia Liu et al. [[1]](https://arxiv.org/abs/1804.06514) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Information Security in Health Care Centre Using Cryptography and Steganography

**Goal:** As the volume of medicinal information stored electronically increase, so do the need to enhance how it is secured.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information Security in Health Care Centre Using Cryptograph** | 2018 | cs.CR | A. O. Babatunde, A. J. Taiwo, E. G. Dada [[1]](https://arxiv.org/abs/1803.05593) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On the Gold Standard for Security of Universal Steganography

**Goal:** While symmetric-key steganography is quite well understood both in the information-theoretic and in the computational setting, many fundamental questions about its public-key counterpart resist per...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On the Gold Standard for Security of Universal Steganography** | 2018 | cs.CR | Sebastian Berndt, Maciej Liśkiewicz [[1]](https://arxiv.org/abs/1801.08154) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### The New Threats of Information Hiding: the Road Ahead

**Goal:** Compared to cryptography, steganography is a less discussed domain.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **The New Threats of Information Hiding: the Road Ahead** | 2018 | cs.CR | K. Cabaj et al. [[1]](https://arxiv.org/abs/1801.00694) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Improvement on LSB Matching and LSB Matching Revisited Steganography Methods

**Goal:** The aim of the steganography methods is to communicate securely in a completely undetectable manner.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Improvement on LSB Matching and LSB Matching Revisited St** | 2017 | cs.CR | Kazem Qazanfari, Reza Safabakhsh [[1]](https://arxiv.org/abs/1709.06727) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An improvement on LSB+ method

**Goal:** substitution is the histogram attack that attempts to diagnose anomalies in the cover image's histogram.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An improvement on LSB+ method** | 2017 | cs.CR | Kazem Qazanfari, Shahrokh Ghaemmaghami [[1]](https://arxiv.org/abs/1709.06726) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Algorithm Substitution Attacks from a Steganographic Perspective

**Goal:** and Kane strengthened the original model and proposed a universal ASA against sufficiently random encryption schemes.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Algorithm Substitution Attacks from a Steganographic Perspec** | 2017 | cs.CR | Sebastian Berndt, Maciej Liskiewicz [[1]](https://arxiv.org/abs/1708.06199) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Steganographic Design Paradigm for General Steganographic Objectives

**Goal:** Steganography is the task of concealing a message within a medium such that the presence of the hidden message cannot be detected.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Steganographic Design Paradigm for General Steganographic ** | 2017 | cs.CR | Aubrey Alston [[1]](https://arxiv.org/abs/1707.00076) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Achieving Efficient and Provably Secure Steganography in Practice

**Goal:** Steganography is the task of concealing a message within a medium such that the presence of the hidden message cannot be detected.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Achieving Efficient and Provably Secure Steganography in Pra** | 2017 | cs.CR | Aubrey Alston [[1]](https://arxiv.org/abs/1707.00074) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### SocialStegDisc: Application of steganography in social networks to create a file system

**Goal:** The concept named SocialStegDisc was introduced as an application of the original idea of StegHash method.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **SocialStegDisc: Application of steganography in social netwo** | 2017 | cs.CR, cs.MM | Jedrzej Bieniasz, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1706.09641) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Cryptographic Approach for Steganography

**Goal:** In this research work, security concepts are formalized in steganography, and the common paradigms based on information theory are replaced by another ones inspired from cryptography, more practica...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Cryptographic Approach for Steganography** | 2017 | cs.CR | Jacques M. Bahi, Christophe Guyeux, Pierre-Cyrille Heam [[1]](https://arxiv.org/abs/1706.08752) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Steganographic Technique Matching the Secret Message and Cover image Binary Value

**Goal:** Steganography involves hiding a secret message or image inside another cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Steganographic Technique Matching the Secret Message a** | 2017 | cs.MM, cs.CR | G. Umamaheswari, Dr. C. P. Sumathi [[1]](https://arxiv.org/abs/1704.02698) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Approach of Pseudorandomly sorted list-based Steganography

**Goal:** We propose a new model of steganography based on a list of pseudo-randomly sorted sequences of characters.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Approach of Pseudorandomly sorted list-based Stegano** | 2017 | cs.CR | Rene Ndoundam, Stephane Gael R. Ekodeck [[1]](https://arxiv.org/abs/1703.02451) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Generating Steganographic Images via Adversarial Training

**Goal:** to generative tasks such as image synthesis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Generating Steganographic Images via Adversarial Training** | 2017 | stat.ML, cs.CR, cs.MM | Jamie Hayes, George Danezis [[1]](https://arxiv.org/abs/1703.00371) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A New Approach to SMS Steganography using Mathematical Equations

**Goal:** Short Message Service (SMS) are easily copied and hacked by using special software.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A New Approach to SMS Steganography using Mathematical Equat** | 2016 | cs.CR, cs.MM | Min Yang Lee, Vahab Iranmanesh, Juan C. Quiroz [[1]](https://arxiv.org/abs/1607.07947) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Natural Steganography: cover-source switching for better steganography

**Goal:** on the principle of cover-source switching, the key idea being that the embedding should switch from one cover-source to another.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Natural Steganography: cover-source switching for better ste** | 2016 | cs.MM, cs.CR | Patrick Bas [[1]](https://arxiv.org/abs/1607.07824) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### High Capacity Image Steganography using Adjunctive Numerical Representations with Multiple Bit-Plane Decomposition Methods

**Goal:** LSB steganography is a one of the most widely used methods for implementing covert data channels in image file exchanges [1][2].

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **High Capacity Image Steganography using Adjunctive Numerical** | 2016 | cs.MM, cs.CR | James Collins, Sos Agaian [[1]](https://arxiv.org/abs/1606.02312) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography -- A Game of Hide and Seek in Information Communication

**Goal:** important issues. In order to transfer data securely to the destination without unwanted disclosure or damage, nature inspired hide and seek tricks such as, cryptography and Steganography are heavi...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography -- A Game of Hide and Seek in Information Comm** | 2016 | cs.MM, cs.CR | Sanjeeb Kumar Behera, Minati Mishra [[1]](https://arxiv.org/abs/1604.00493) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Secure Image Steganography using Cryptography and Image Transposition

**Goal:** technological world.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Secure Image Steganography using Cryptography and Image Tran** | 2015 | cs.MM, cs.CR | Khan Muhammad et al. [[1]](https://arxiv.org/abs/1510.04413) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography and Broadcasting

**Goal:** Informally, steganography is the process of exchanging a secret message between two communicating entities so that an eavesdropper may not know that a message has been sent.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography and Broadcasting** | 2015 | cs.CR | Fabrice P. Tachago, Stephane G. R. Ekodeck, Rene Ndoundam [[1]](https://arxiv.org/abs/1506.04502) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Approach for Image Steganography in Spatial Domain

**Goal:** This paper presents a new approach for hiding information in digital image in spatial domain.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Approach for Image Steganography in Spatial Domain** | 2015 | cs.MM, cs.CR | Fatema Akhter [[1]](https://arxiv.org/abs/1506.03681) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Facebook for Image Steganography

**Goal:** (from desktops and laptops running Windows, Unix, or OS X to hand held devices running iOS, Android, or Windows Phone), it would seem to be the perfect place to conduct steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Facebook for Image Steganography** | 2015 | cs.MM, cs.CR | Jason Hiney et al. [[1]](https://arxiv.org/abs/1506.02071) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### PDF Steganography based on Chinese Remainder Theorem

**Goal:** We propose different approaches of PDF files based steganography, essentially based on the Chinese Remainder Theorem.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **PDF Steganography based on Chinese Remainder Theorem** | 2015 | cs.CR | Rene Ndoundam, Stephane Gael Raymond Ekodeck [[1]](https://arxiv.org/abs/1506.01256) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Low-throughput Wavelet-based Steganography Audio Scheme

**Goal:** This paper presents the preliminary of a novel scheme of steganography, and introduces the idea of combining two secret keys in the operation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Low-throughput Wavelet-based Steganography Audio Scheme** | 2015 | cs.MM, cs.CR | P. Carrion, H. M. de Oliveira, R. M. Campello de Souza [[1]](https://arxiv.org/abs/1503.07551) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Environment Based Secure Transfer of Data in Wireless Sensor Networks

**Goal:** technique named aggregate signature to validate the source of the message and also to protect the data against latest security attacks, cryptography technique combined with steganography has been i...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Environment Based Secure Transfer of Data in Wireless Sensor** | 2015 | cs.CR | B. Vidhya et al. [[1]](https://arxiv.org/abs/1503.03215) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Secure Cyclic Steganographic Technique for Color Images using Randomization

**Goal:** want the security, confidentiality and integrity of their personal data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Secure Cyclic Steganographic Technique for Color Images us** | 2015 | cs.MM, cs.CR | Khan Muhammad et al. [[1]](https://arxiv.org/abs/1502.07808) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### How to Bootstrap Anonymous Communication

**Goal:** of anonymous communication and to the best of our knowledge this is the first formal study in this direction.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **How to Bootstrap Anonymous Communication** | 2015 | cs.CR | Sune K. Jakobsen, Claudio Orlandi [[1]](https://arxiv.org/abs/1502.05273) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Secure Electronic Prescription System Using Steganography with Encryption Key Implementation

**Goal:** system that addresses some challenges pertaining to the prescription privacy protection in the process of drug prescription.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Secure Electronic Prescription System Using Steganography ** | 2015 | cs.CR, cs.CY, cs.MM | Adebayo Omotosho et al. [[1]](https://arxiv.org/abs/1502.01264) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography in Modern Smartphones and Mitigation Techniques

**Goal:** attacks and hazards to profile individuals or gather sensitive information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography in Modern Smartphones and Mitigation Technique** | 2014 | cs.MM, cs.CR | Wojciech Mazurczyk, Luca Caviglione [[1]](https://arxiv.org/abs/1410.6796) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### StegExpose - A Tool for Detecting LSB Steganography

**Goal:** in saving time and providing new angles of attack for forensic analysts.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **StegExpose - A Tool for Detecting LSB Steganography** | 2014 | cs.MM, cs.CR | Benedikt Boehm [[1]](https://arxiv.org/abs/1410.6656) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Approach for Text Steganography Based on Markov Chains

**Goal:** A text steganography method based on Markov chains is introduced, together with a reference implementation.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Approach for Text Steganography Based on Markov Chains** | 2014 | cs.MM, cs.CL | H. Hernan Moraldo [[1]](https://arxiv.org/abs/1409.0915) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### High Security Image Steganography with Modified Arnold cat map

**Goal:** Information security is concerned with maintaining the secrecy, reliability and accessibility of data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **High Security Image Steganography with Modified Arnold cat m** | 2014 | cs.CR, cs.MM | Minati Mishra, Ashanta Ranjan Routray, Sunit Kumar [[1]](https://arxiv.org/abs/1408.3838) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Reversible and Irreversible Data Hiding Technique

**Goal:** Steganography (literally meaning covered writing) is the art and science of embedding secret message into seemingly harmless message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Reversible and Irreversible Data Hiding Technique** | 2014 | cs.CR | Tanmoy Sarkar, Sugata Sanyal [[1]](https://arxiv.org/abs/1405.2684) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography -- coding and intercepting the information from encoded pictures in the absence of any initial information

**Goal:** The work includes implementation and extraction algorithms capabilities test, without any additional data (starting position, the number of bits used, gap between the amount of data encoded) inform...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography -- coding and intercepting the information fro** | 2014 | cs.MM, cs.CR, cs.DC | Monika Kwiatkowska, Lukasz Swierczewski [[1]](https://arxiv.org/abs/1404.2237) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Study of Various Steganographic Techniques Used for Information Hiding

**Goal:** Steganography derives from the Greek word steganos, meaning covered or secret, and graphy (writing or drawing).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Study of Various Steganographic Techniques Used for Inform** | 2014 | cs.MM | C. P. Sumathi, T. Santanam, G. Umamaheswari [[1]](https://arxiv.org/abs/1401.5561) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Dual Layer Textual Message Cryptosystem with Randomized Sequence of Symmetric Key

**Goal:** concept of textual message encryption and decryption through a pool of randomized symmetric key and the dual layer cryptosystem with the concept of visual cryptography and steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Dual Layer Textual Message Cryptosystem with Randomized Sequ** | 2013 | cs.CR | Chandranath Adak [[1]](https://arxiv.org/abs/1312.5424) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Robust Steganography Using LSB-XOR and Image Sharing

**Goal:** the secret digital information and data that are transmitted over the internet is of widespread and most challenging interest.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Robust Steganography Using LSB-XOR and Image Sharing** | 2013 | cs.CR | Chandranath Adak [[1]](https://arxiv.org/abs/1312.5417) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography using the Extensible Messaging and Presence Protocol (XMPP)

**Goal:** from one XMPP client to another, without raising the suspicion of any intermediaries.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography using the Extensible Messaging and Presence Pr** | 2013 | cs.MM, cs.CR | Reshad Patuck, Julio Hernandez-Castro [[1]](https://arxiv.org/abs/1310.0524) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Comparison of secure and high capacity color image steganography techniques in RGB and YCbCr domains

**Goal:** Steganography is one of the methods used for secret communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Comparison of secure and high capacity color image steganogr** | 2013 | cs.MM, cs.CR | S. Hemalatha, U. Dinesh Acharya, A. Renuka [[1]](https://arxiv.org/abs/1307.3026) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Novel Steganography Algorithm for Hiding Text in Image using Five Modulus Method

**Goal:** in size. Peak signal-to-noise ratio is captured for each of the images tested.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Novel Steganography Algorithm for Hiding Text in Image usi** | 2013 | cs.MM, cs.CR | Firas A. Jassim [[1]](https://arxiv.org/abs/1307.0642) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Enhanced Tiny Encryption Algorithm with Embedding (ETEA)

**Goal:** Hence, in order to provide a better security mechanism, in this paper we propose Enhanced Tiny Encryption Algorithm with Embedding (ETEA), a data hiding technique called steganography along with th...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Enhanced Tiny Encryption Algorithm with Embedding (ETEA)** | 2013 | cs.MM, cs.CR | Deepali Virmani et al. [[1]](https://arxiv.org/abs/1306.6920) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### One Time Pad Password Protection: Using T.E.C. Steganography and Secure Password Transmission Protocols

**Goal:** A while ago, I developed what I called an encryption method.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **One Time Pad Password Protection: Using T.E.C. Steganography** | 2013 | cs.CR | Givon Zirkind [[1]](https://arxiv.org/abs/1306.0497) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography based on a Parameterized Canny Edge Detection Algorithm

**Goal:** Steganography is the science of hiding digital information in such a way that no one can suspect its existence.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography based on a Parameterized Canny Edge Dete** | 2012 | cs.CR | Youssef Bassil [[1]](https://arxiv.org/abs/1212.6259) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography Method Based on Brightness Adjustment

**Goal:** Steganography is an information hiding technique in which secret data are secured by covering them into a computer carrier file without damaging the file or changing its size.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography Method Based on Brightness Adjustment** | 2012 | cs.CR, cs.MM | Youssef Bassil [[1]](https://arxiv.org/abs/1212.5801) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Authentication Technique in Frequency Domain through Wavelet Transform (ATFDWT)

**Goal:** In this paper a DWT based steganography in frequency domain, termed as ATFDWT has been proposed.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Authentication Technique in Frequency Domain through Wave** | 2012 | cs.CR | Madhumita Sengupta, J. K. Mandal, N. Ghoshal [[1]](https://arxiv.org/abs/1212.3719) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Text Steganography Method Using Pangram and Image Mediums

**Goal:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the sender and the receiver would realize that a secret communicating is taking place.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Text Steganography Method Using Pangram and Image Mediums** | 2012 | cs.CR | Youssef Bassil [[1]](https://arxiv.org/abs/1212.2908) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Lossless Data Hiding Technique based on AES-DWT

**Goal:** In this paper we propose a new data hiding technique.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Lossless Data Hiding Technique based on AES-DWT** | 2012 | cs.CR | Francisco Rubén Castillo Soria, Gustavo Fernández Torres, Ignacio Algredo-Badillo [[1]](https://arxiv.org/abs/1212.2669) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Generation-based Text Steganography Method using SQL Queries

**Goal:** Cryptography and Steganography are two techniques commonly used to secure and safely transmit digital data.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Generation-based Text Steganography Method using SQL Queri** | 2012 | cs.CR | Youssef Bassil [[1]](https://arxiv.org/abs/1212.2067) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Image Steganography Scheme using Randomized Algorithm and Context-Free Grammar

**Goal:** However, clearly visible encrypted messages, no matter how unbreakable, will arouse suspicions.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Image Steganography Scheme using Randomized Algorithm and** | 2012 | cs.CR, cs.MM | Youssef Bassil [[1]](https://arxiv.org/abs/1212.2064) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Embedding grayscale halftone pictures in QR Codes using Correction Trees

**Goal:** similar to finding the proper correction in error correction problem, but instead of single ensured possibility, there are now statistically expected some.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Embedding grayscale halftone pictures in QR Codes using Corr** | 2012 | cs.IT, cs.CR, cs.MM | Jarek Duda [[1]](https://arxiv.org/abs/1211.1572) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Some New Methodologies for Image Hiding using Steganographic Techniques

**Goal:** devices like ipods, cell phones, pmps, iphones and digital cameras.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Some New Methodologies for Image Hiding using Steganographic** | 2012 | cs.CR, cs.MM | Rajesh Kumar Tiwari, Gadadhar Sahoo [[1]](https://arxiv.org/abs/1211.0377) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Public key Steganography Using Discrete Cross-Coupled Chaotic Maps

**Goal:** By cross-coupling two logistic maps a novel method is proposed for the public key steganography in JPEG image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Public key Steganography Using Discrete Cross-Coupled Chaoti** | 2012 | cs.CR, cs.MM, nlin.CD | Sodeif Ahadpour, Mahdiyeh Majidpour, Yaser Sadra [[1]](https://arxiv.org/abs/1211.0086) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Multimedia Steganographic Scheme using Multiresolution Analysis

**Goal:** Digital steganography or data hiding has emerged as a new area of research in connection to the communication in secured channel as well as intellectual property protection for multimedia signals.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Multimedia Steganographic Scheme using Multiresolution Analy** | 2012 | cs.CR | Tirtha sankar Das et al. [[1]](https://arxiv.org/abs/1207.2675) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Security Architecture for Cluster based Ad Hoc Networks

**Goal:** intra-cluster security.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Security Architecture for Cluster based Ad Hoc Networks** | 2012 | cs.CR | Preetida Vinayakray-Jani, Sugata Sanyal [[1]](https://arxiv.org/abs/1207.1701) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Pixastic: Steganography based Anti-Phihsing Browser Plug-in

**Goal:** world and effective anti-phishing technique is the need of the hour.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Pixastic: Steganography based Anti-Phihsing Browser Plug-in** | 2012 | cs.CR | P. Thiyagarajan, G. Aghila, V. Prasanna Venkatesan [[1]](https://arxiv.org/abs/1206.2445) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Survey on Various Data Hiding Techniques and their Comparative Analysis

**Goal:** hiding like cryptography, hashing, authentication have been developed and are in practice today.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Survey on Various Data Hiding Techniques and their Compara** | 2012 | cs.CR | Harshavardhan Kayarkar, Sugata Sanyal [[1]](https://arxiv.org/abs/1206.1957) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Text Steganography using LSB insertion method along with Chaos Theory

**Goal:** The art of information hiding has been around nearly as long as the need for covert communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Text Steganography using LSB insertion method along with Cha** | 2012 | cs.MM | Bhavana S., K. L. Sudha [[1]](https://arxiv.org/abs/1205.1859) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Genetic Algorithm to Make Persistent Security and Quality of Image in Steganography from RS Analysis

**Goal:** Retention of secrecy is one of the significant features during communication activity.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Genetic Algorithm to Make Persistent Security and Quality of** | 2012 | cs.MM, cs.CR | T. R. Gopalakrishnan Nair, Suma V, Manas S [[1]](https://arxiv.org/abs/1204.2616) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Experimenting with the Novel Approaches in Text Steganography

**Goal:** As is commonly known, the steganographic algorithms employ images, audio, video or text files as the medium to ensure hidden exchange of information between multiple contenders to protect the data ...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Experimenting with the Novel Approaches in Text Steganograph** | 2012 | cs.CR, cs.MM | Shraddha Dulera, Devesh Jinwala, Aroop Dasgupta [[1]](https://arxiv.org/abs/1203.3644) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Frequency Domain Steganography using Z Transform (FDSZT)

**Goal:** Image steganography is art of hiding information onto the cover image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Frequency Domain Steganography using Z Transform (FDSZT)** | 2012 | cs.CR, cs.MM | J. K. Mandal [[1]](https://arxiv.org/abs/1202.4245) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Influence of Speech Codecs Selection on Transcoding Steganography

**Goal:** The typical approach to steganography is to compress the covert data in order to limit its size, which is reasonable in the context of a limited steganographic bandwidth.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Influence of Speech Codecs Selection on Transcoding Steganog** | 2012 | cs.CR, cs.MM | Artur Janicki, Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1201.6218) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Information Hiding in CSS : A Secure Scheme Text-Steganography using Public Key Cryptosystem

**Goal:** by using CSS as a message hider.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information Hiding in CSS : A Secure Scheme Text-Steganograp** | 2012 | cs.CR | Herman Kabetta, B. Yudi Dwiandiyanta, Suyoto [[1]](https://arxiv.org/abs/1201.1968) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Windtalking Computers: Frequency Normalization, Binary Coding Systems and Encryption

**Goal:** of a method for computers analogous to speaking another language.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Windtalking Computers: Frequency Normalization, Binary Codin** | 2012 | cs.CR | Givon Zirkind [[1]](https://arxiv.org/abs/0912.4080) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Randomness Efficient Steganography

**Goal:** comes as an effect of the application of randomness extractors to stegosystem design.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Randomness Efficient Steganography** | 2012 | cs.CR, cs.IT | Aggelos Kiayias, Alexander Russell, Narasimha Shashidhar [[1]](https://arxiv.org/abs/0909.4575) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Chaotic iterations for steganography: Stego-security and topological-security

**Goal:** In this paper is proposed a novel steganographic scheme based on chaotic iterations.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Chaotic iterations for steganography: Stego-security and top** | 2011 | cs.CR, cs.MM, math.DS | Nicolas Friot, Christophe Guyeux, Jacques M. Bahi [[1]](https://arxiv.org/abs/1112.3873) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography Algorithm to Hide Secret Message inside an Image

**Goal:** In this paper, the authors propose a new algorithm to hide data inside image using steganography technique.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography Algorithm to Hide Secret Message inside an Ima** | 2011 | cs.MM, cs.CR | Rosziati Ibrahim, Teoh Suk Kuan [[1]](https://arxiv.org/abs/1112.2809) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography: a Class of Algorithms having Secure Properties

**Goal:** Chaos-based approaches are frequently proposed in information hiding, but without obvious justification.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography: a Class of Algorithms having Secure Propertie** | 2011 | cs.DM, cs.CR | Jacques M. Bahi, Jean-François Couchot, Christophe Guyeux [[1]](https://arxiv.org/abs/1112.1675) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography: a class of secure and robust algorithms

**Goal:** This research work presents a new class of non-blind information hiding algorithms that are stego-secure and robust.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography: a class of secure and robust algorithms** | 2011 | cs.CR | Jacques M. Bahi, Jean-François Couchot, Christophe Guyeux [[1]](https://arxiv.org/abs/1112.1260) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Transcoding for Hidden Communication in IP Telephony

**Goal:** The paper presents a new steganographic method for IP telephony called TranSteg (Transcoding Steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Transcoding for Hidden Communication in IP Telephony** | 2011 | cs.CR, cs.MM | Wojciech Mazurczyk, Pawel Szaga, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1111.1250) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Applying statistical methods to text steganography

**Goal:** This paper presents a survey of text steganography methods used for hid- ing secret information inside some covertext.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Applying statistical methods to text steganography** | 2011 | cs.CR | Ivan Nechta, Andrei Fionov [[1]](https://arxiv.org/abs/1110.2654) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An Approach for Message Hiding using Substitution Techniques and Audio Hiding in Steganography

**Goal:** that an eavesdropper who overhears the encrypted messages will not be able to decode them.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Approach for Message Hiding using Substitution Techniques** | 2011 | cs.CR | Debajyoti Mukhopadhyay et al. [[1]](https://arxiv.org/abs/1109.4709) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Digital Forensics Analysis of Spectral Estimation Methods

**Goal:** Steganography is the art and science of writing hidden messages in such a way that no one apart from the intended recipient knows of the existence of the message.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Digital Forensics Analysis of Spectral Estimation Methods** | 2011 | cs.CR | Tolga Mataracioglu, Unal Tatar [[1]](https://arxiv.org/abs/1108.2151) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Is Cloud Computing Steganography-proof?

**Goal:** on characterisation of information hiding possibilities in Cloud Computing.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Is Cloud Computing Steganography-proof?** | 2011 | cs.CR | Wojciech Mazurczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1107.4077) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Lost Audio Packets Steganography: The First Practical Evaluation

**Goal:** This paper presents first experimental results for an IP telephony-based steganographic method called LACK (Lost Audio PaCKets steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Lost Audio Packets Steganography: The First Practical Evalua** | 2011 | cs.CR, cs.MM | Wojciech Mazurczyk [[1]](https://arxiv.org/abs/1107.4076) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Wet paper codes and the dual distance in steganography

**Goal:** In 1998 Crandall introduced a method based on coding theory to secretly embed a message in a digital support such as an image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Wet paper codes and the dual distance in steganography** | 2011 | cs.CR, cs.IT | Carlos Munuera, Morgan Barbier [[1]](https://arxiv.org/abs/1104.1970) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Hiding Secret Information in Movie Clip: A Steganographic Approach

**Goal:** subject of discussion that has gained increasing importance nowadays with the development of the internet.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Secret Information in Movie Clip: A Steganographic Ap** | 2011 | cs.MM, cs.CR | G. Sahoo, Rajesh Kumar Tiwari [[1]](https://arxiv.org/abs/1103.0829) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### On Steganography in Lost Audio Packets

**Goal:** presents a new hidden data insertion procedure based on estimated probability of the remaining time of the call for steganographic method called LACK (Lost Audio PaCKets steganography).

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **On Steganography in Lost Audio Packets** | 2011 | cs.CR, cs.MM | Wojciech Mazurczyk, Jozef Lubacz, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/1102.0023) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Bio-Authentication based Secure Transmission System using Steganography

**Goal:** method for Fingerprint recognition is considered using a combination of Fast Fourier Transform (FFT) and Sobel Filters for improvement of a poor quality fingerprint image.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Bio-Authentication based Secure Transmission System using St** | 2010 | cs.CR | Najme Zehra et al. [[1]](https://arxiv.org/abs/1005.4264) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Improved information security using robust Steganography system

**Goal:** Steganography is an emerging area which is used for secured data transmission over any public media.Steganography is a process that involves hiding a message in an appropriate carrier like image or...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Improved information security using robust Steganography sys** | 2010 | cs.CR | Mamta Juneja, Parvinder singh Sandhu [[1]](https://arxiv.org/abs/1004.2132) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Overview: Main Fundamentals for Steganography

**Goal:** threats. It is a big security and privacy issue, it become necessary to find appropriate protection because of the significance, accuracy and sensitivity of the information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Overview: Main Fundamentals for Steganography** | 2010 | cs.CR, cs.MM | Zaidoon Kh. AL-Ani et al. [[1]](https://arxiv.org/abs/1003.4086) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### New System for Secure Cover File of Hidden Data in the Image Page within Executable File Using Statistical Steganography Techniques

**Goal:** A Previously traditional methods were sufficient to protect the information, since it is simplicity in the past does not need complicated methods but with the progress of information technology, it...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **New System for Secure Cover File of Hidden Data in the Image** | 2010 | cs.CR, cs.MM | Rafiqul Islam et al. [[1]](https://arxiv.org/abs/1002.2416) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Known vulnerabilities or detection risks discussed in paper.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### M-Banking Security - a futuristic improved security approach

**Goal:** The aim of this work is to provide a secure environment in terms of security for transaction by various ways.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **M-Banking Security - a futuristic improved security approach** | 2010 | cs.CR | Geeta S. Navale, Swati S. Joshi, Aaradhana A. Deshmukh [[1]](https://arxiv.org/abs/1002.1174) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Steganography Based on CT-CDMA Communication Scheme Using Complete Complementary Codes

**Goal:** users can be transmitted by using the same set of complementary codes through a single frequency band.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Steganography Based on CT-CDMA Communication Scheme Using ** | 2010 | cs.IT, cs.CR | Tetsuya Kojima, Yoshiya Horii [[1]](https://arxiv.org/abs/1001.2623) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Frame Selected Approach for Hiding Data within MPEG Video Using Bit Plane Complexity Segmentation

**Goal:** Bit Plane Complexity Segmentation (BPCS) digital picture steganography is a technique to hide data inside an image file.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Frame Selected Approach for Hiding Data within MPEG Video Us** | 2009 | cs.CR | Hamid. A. Jalab, A. A Zaidan, B. B Zaidan [[1]](https://arxiv.org/abs/0912.3986) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography An Art of Hiding Data

**Goal:** these channels, an eavesdropper can identify encrypted streams through statistical tests and capture them for further cryptanalysis.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography An Art of Hiding Data** | 2009 | cs.CR | Shashikala Channalli, Ajay Jadhav [[1]](https://arxiv.org/abs/0912.2319) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### An approach to secure highly confidential documents of any size in the corporate or institutes having unsecured networks

**Goal:** papers and many other confidential documents designed by their faculty members.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An approach to secure highly confidential documents of any s** | 2009 | cs.CR | Samir B. Patel, Shrikant N. Pradhan [[1]](https://arxiv.org/abs/0912.0954) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A novel approach for implementing Steganography with computing power obtained by combining Cuda and Matlab

**Goal:** available within. Our approach is to use the CUDA (Compute Unified Device Architecture) as backend and MATLAB as the front end to design an application for implementing steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A novel approach for implementing Steganography with computi** | 2009 | cs.CR | Samir B. Patel, Shrikant N. Pradhan, Saumitra U. Ambegaokar [[1]](https://arxiv.org/abs/0912.0947) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Efficient Steganography with Provable Security Guarantees

**Goal:** We provide a new provably-secure steganographic encryption protocol that is proven secure in the complexity-theoretic framework of Hopper et al.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Efficient Steganography with Provable Security Guarantees** | 2009 | cs.CR, cs.IT | Aggelos Kiayias et al. [[1]](https://arxiv.org/abs/0909.3658) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Secure
Provably secure construction with formal guarantees.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### A Performance Analysis of HICCUPS - a Steganographic System for WLAN

**Goal:** The paper presents an analysis of performance features of the HICCUPS (HIdden Communication system for CorrUPted networkS) including the efficiency and the cost of the system in WLANs (Wireless Loc...

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **A Performance Analysis of HICCUPS - a Steganographic System ** | 2009 | cs.CR, cs.PF | Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/0906.4217) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint stage; community evaluation ongoing.

---

### Hiding Information in Retransmissions

**Goal:** The paper presents a new steganographic method called RSTEG (Retransmission Steganography), which is intended for a broad class of protocols that utilises retransmission mechanisms.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Hiding Information in Retransmissions** | 2009 | cs.CR | Wojciech Mazurczyk, Milosz Smolarczyk, Krzysztof Szczypiorski [[1]](https://arxiv.org/abs/0905.0363) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Using Kolmogorov Complexity for Understanding Some Limitations on Steganography

**Goal:** Recently perfectly secure steganographic systems have been described for a wide class of sources of covertexts.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Using Kolmogorov Complexity for Understanding Some Limitatio** | 2009 | cs.CC, cs.CR | Boris Ryabko, Daniil Ryabko [[1]](https://arxiv.org/abs/0901.4023) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Capacity of Steganographic Channels

**Goal:** This work investigates a central problem in steganography, that is: How much data can safely be hidden without being detected?

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Capacity of Steganographic Channels** | 2008 | cs.CR, cs.IT | Jeremiah J. Harmsen, William A. Pearlman [[1]](https://arxiv.org/abs/0810.4171) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### TrustMAS: Trusted Communication Platform for Multi-Agent Systems

**Goal:** are able to perform various steganographic communication.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **TrustMAS: Trusted Communication Platform for Multi-Agent Sys** | 2008 | cs.CR, cs.MA | Krzysztof Szczypiorski et al. [[1]](https://arxiv.org/abs/0808.4060) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Image Steganography, a New Approach for Transferring Security Information

**Goal:** Steganography is the art of hiding the fact that communication is taking place, by hiding information in other information.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Image Steganography, a New Approach for Transferring Securit** | 2008 | cs.CR | H. B. Bahar, Ali Aboutalebi [[1]](https://arxiv.org/abs/0808.1410) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Steganography from weak cryptography

**Goal:** We introduce a problem setting which we call ``the freedom fighters' problem''.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Steganography from weak cryptography** | 2008 | cs.CR | Boris Skoric [[1]](https://arxiv.org/abs/0804.0659) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Information Hiding Techniques: A Tutorial Review

**Goal:** The purpose of this tutorial is to present an overview of various information hiding techniques.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Information Hiding Techniques: A Tutorial Review** | 2008 | cs.CR, cs.IR | Sabu M. Thampi [[1]](https://arxiv.org/abs/0802.3746) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint stage; community evaluation ongoing.

---

### An Improved FPGA Implementation of the Modified Hybrid Hiding Encryption Algorithm (MHHEA) for Data Communication Security

**Goal:** The hybrid hiding encryption algorithm, as its name implies, embraces concepts from both steganography and cryptography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **An Improved FPGA Implementation of the Modified Hybrid Hidin** | 2007 | cs.CR | Hala A. Farouk, Magdy Saeb [[1]](https://arxiv.org/abs/0710.4800) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Lightweight security mechanism for PSTN-VoIP cooperation

**Goal:** In this paper we describe a new, lightweight security mechanism for PSTN-VoIP cooperation that is based on two information hiding techniques: digital watermarking and steganography.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Lightweight security mechanism for PSTN-VoIP cooperation** | 2006 | cs.CR, cs.MM | Wojciech Mazurczyk, Zbigniew Kotulski [[1]](https://arxiv.org/abs/cs/0612054) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### New security and control protocol for VoIP based on steganography and digital watermarking

**Goal:** this solution offers authentication and integrity, it is capable of exchanging and verifying QoS and security parameters.

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **New security and control protocol for VoIP based on steganog** | 2006 | cs.CR, cs.MM | Wojciech Mazurczyk, Zbigniew Kotulski [[1]](https://arxiv.org/abs/cs/0602042) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---

### Content Based Image Retrieval with Mobile Agents and Steganography

**Goal:** In this paper we present an image retrieval system based on Gabor texture features, steganography, and mobile agents..

| Algorithm | Year | Approach | Notable Feature |
|-----------|------|----------|-----------------|
| **Content Based Image Retrieval with Mobile Agents and Stegano** | 2006 | cs.CR | Sabu . M Thampi, K. Chandra Sekaran [[1]](https://arxiv.org/abs/cs/0411041) |

**State of the art:** Recent arXiv contribution. See paper for full evaluation and comparison with prior work.

**Production readiness:** Experimental
Mature research with available implementation.

**Security status:** Caution
Research prototype; security not yet independently verified.

**Community acceptance:** Emerging
Preprint; peer review status unknown.

---
