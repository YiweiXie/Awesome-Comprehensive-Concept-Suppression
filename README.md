# 🧠 Awesome Comprehensive Concept Suppression

This repository provides a comprehensive investigation of concept erasure methods.

---

## 🔍 Concept Erasure in Text-to-Image Generative Models

**Paper Title:** *Erasing Concepts, Steering Generations: A Comprehensive Survey of Concept Suppression*  📄 **[arXiv Preprint](#)**  


## 🧑‍💻 Authors
- **Yiwei Xie**, Huazhong University of Science and Technology  
- **Ping Liu**, University of Nevada, Reno, NV, USA 
- **Zheng Zhang**, Huazhong University of Science and Technology

If you believe there are additional works that should be included in our list, please do not hesitate to send us an email (yiweixie@hust.edu.cn/pino.pingliu@gmail.com/leaf@hust.edu.cn) or raise an issue. Your suggestions and comments are invaluable to ensuring the completeness and accuracy of our resource.

![ESD Concept Erasure Results](Figures/Concept%20Erasure%20Overview.png)

<!-- **Figure:** The evolutionary development of Concept Erasure methods in recent years. Notably, the year of paper's initial publication is shown as the reference. For instance, if a paper is published in ICLR 2025 but listed on arXiv in 2024,the year 2024 will be considered as the reference date. -->

---

## ✨ Content
  - [Concept Erasure Methods](#concept-erasure-methods)
      - [Intervention Level Categorization](#intervention-level-categorization)
        - [Text Encoder Level](#text-encoder-level)
          - [Few-shot Unlearning](#few-shot-unlearning)
          - [Loss-Based Embedding Modification](#loss-based-embedding-modification)
          - [Text Encoder–Based Similarity Filtering](#text-encoderbased-similarity-filtering)
          - [Principal Components-Based Embedding Modification](#principal-components-based-embedding-modification)
          - [Multi-Constraint Embedding Erasure](#multi-constraint-embedding-erasure)
          - [Token-Level Prompt Embedding Adjustment](#token-level-prompt-embedding-adjustment)
      - [Non-Text Encoder Level](#non-text-encoder-level)
        - [Cross-Attention-Based Erasure](#cross-attention-based-erasure)
          - [Loss-Based Optimization](#loss-based-optimization)
          - [Attention-map-Based Optimization](#attention-map-based-optimization)
          - [Closed-form Optimization](#closed-form-optimization)
          - [Externally guided or explicit intervention optimization](#externally-guided-or-explicit-intervention-optimization)
        - [UNet Level](#unet-level)
          - [Structural Pruning and Feature Removal](#structural-pruning-and-feature-removal)
          - [Loss-Driven Concept Erasure](#loss-driven-concept-erasure)
          - [Additive Module or Parameters](#additive-module-or-parameters)
    - [Optimization-Based Catagorization](#optimization-based-catagorization)
      - [Adversarial Training](#adversarial-training)
      - [Closed-form Projections](#closed-form-projections)
      - [Plug-in Adapters](#plug-in-adapters)
      - [Loss-Based Training Objectives](#loss-based-training-objectives)
  - [Evaluation and Benchmarking](#evaluation-and-benchmarking)
  - [Adversarial Attacks](#adversarial-attacks)
  - [🔗 Relevant Surveys](#-relevant-surveys)
  - [📌 Citation](#-citation)




---
## Concept Erasure Methods
<hr style="height:3px; border:none; background: linear-gradient(to right, #fff, #ddd, #fff);">

#### Intervention Level Categorization
##### Text Encoder Level
###### Few-shot Unlearning
1. [BMVC2024] [📄Paper](https://bmvc2024.org/proceedings/216/)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/fmp453/few-shot-erasing)
   Erasing Concepts from Text-to-Image Diffusion Models  with Few-shot Unlearning   
   
###### Loss-Based Embedding Modification
1. [NeurIPS2024] [📄Paper](https://proceedings.neurips.cc/paper_files/paper/2024/file/40954ac18a457dd5f11145bae6454cdf-Paper-Conference.pdf)    [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/AdvUnlearn)
   Defensive Unlearning with Adversarial Training for Robust Concept Erasure in Diffusion Models    
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2502.20623)
   SafeText: Safe Text-to-image Models via Aligning the Text Encoder
3. [arXiv2025] [📄Paper](https://arxiv.org/abs/2412.07249)
   Buster: Implanting Semantic Backdoor into Text Encoder to Mitigate NSFW  Content Generation

###### Text Encoder–Based Similarity Filtering
1. [ACM CODASPY2025] [📄Paper](https://arxiv.org/abs/2404.19227)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ssg-research/concept-filtering)
   Espresso: Robust Concept Filtering in Text-to-Image Models

###### Principal Components-Based Embedding Modification
1. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.15562)
   CE-SDWV: Effective and Efficient Concept Erasure for Text-to-Image Diffusion Models via a Semantic-Driven Word Vocabulary
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.16835)
   Safe and Reliable Diffusion Models via Subspace  Projection
3. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.09446)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/NANSirun/Interpret-then-deactivate)
   Sparse Autoencoder as a Zero-Shot Classifier for Concept Erasing in Text-to-Image Diffusion Models
4. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.19066)   [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/kim-dahye/steerers)
   Concept Steerers: Leveraging K-Sparse Autoencoders for Controllable  Generations
5. [ICML2025] [📄Paper](https://icml.cc/virtual/2025/poster/46380)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cywinski/SAeUron)
   SAeUron: Interpretable Concept Unlearning in Diffusion Models with Sparse Autoencoders

###### Multi-Constraint Embedding Erasure
1. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.18877)        [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/aei13/DES)
   Distorting Embedding Space for Safety:  A Defense Mechanism for Adversarially Robust Diffusion Models

###### Token-Level Prompt Embedding Adjustment
1. [ECCV2024] [📄Paper](https://arxiv.org/abs/2409.16535)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/DeepakSridhar/promptsliders)
   Prompt Sliders for Fine-Grained Control, Editing and Erasing of Concepts in Diffusion Models
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.03544)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/PromptGuard-727C/README.md)
   PromptGuard: Soft Prompt-Guided Unsafe Content Moderation for  Text-to-Image Models
3. [arXiv2025] [📄Paper](https://arxiv.org/abs/2411.10329)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/Embedding-Sanitizer-166E/README.md)
   Safe Text-to-Image Generation: Simply Sanitize the Prompt Embedding
4. [ACM WWW2025] [📄Paper](https://dl.acm.org/doi/10.1145/3696410.3714912)    
   Responsible Diffusion Models via Constraining Text Embeddings within Safe Regions

<hr style="height:3px; border:none; background: linear-gradient(to right, #fff, #ddd, #fff);">

#### Non-Text Encoder Level
##### Cross-Attention-Based Erasure
###### Loss-Based Optimization
1. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Gandikota_Erasing_Concepts_from_Diffusion_Models_ICCV_2023_paper.html) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/erasing)
   Erasing Concepts from Diffusion Models
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.14232)
   CRCE: Coreference-Retention Concept Erasure in Text-to-Image Diffusion  Models
3. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Kumari_Ablating_Concepts_in_Text-to-Image_Diffusion_Models_ICCV_2023_paper.pdf) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/nupurkmr9/concept-ablation)
   Ablating Concepts in Text-to-Image Diffusion Models
4. [NeurIPS2024] [📄Paper](https://openreview.net/pdf?id=8naq3XyGQe)
   Choose Your Anchor Wisely: Effective Unlearning Diffusion Models via Concept Reconditioning
5. [arXiv2024] [📄Paper](https://arxiv.org/abs/2409.17682) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/RichardSunnyMeng/DarkMiner-official-codes)
   Dark Miner: Defend against unsafe generation for text-to-image diffusion models
6. [arXiv2024] [📄Paper](https://arxiv.org/abs/2402.05947) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Dlut-lab-zmn/SRS-ME)
   Separable Multi-Concept Erasure from Diffusion Models
7. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=OBjF5I4PWg) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Sirius11311/CoGFD-ICLR25)
   Erasing Concept Combination from Text-to-Image Diffusion Model
8. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.13769)   [<span style="color:rgb(37,98,53);">:bulb:Code</span>](https://anonymous.4open.science/r/Decremental-Learning-0659/)
   Continual Unlearning for Foundational Text-to-Image Models without  Generalization Erosion

 

###### Attention-map-Based Optimization
1. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024W/MMFM/papers/Zhang_Forget-Me-Not_Learning_to_Forget_in_Text-to-Image_Diffusion_Models_CVPRW_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/SHI-Labs/Forget-Me-Not)
   Forget-Me-Not: Learning to Forget in Text-to-Image Diffusion Models
2. [AAAI2024] [📄Paper](https://ojs.aaai.org/index.php/AAAI/article/view/30107) 
   All but One: Surgical Concept Erasing with Model Preservation in Text-to-Image Diffusion Models
3. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=w4C4z80w59)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CD22104/Growth-Inhibitors-for-Erasure)
   Growth Inhibitors for Suppressing Inappropriate Image Concepts in Diffusion Models
4. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=ZRDhBwKs7l)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Hyun1A/CPE)
   Concept Pinpoint Eraser for Text-to-image Diffusion Models via Residual Attention Gate
5. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.01244)    [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/zhang-lingyun/ConceptReplacer)
   Concept Replacer: Replacing Sensitive Concepts in Diffusion Models via Precision Localization
6. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.15197)
   Detect-and-Guide: Self-regulation of Diffusion Models for Safe Text-to-Image  Generation via Guideline Token Optimization
7. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.09630)   [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Atmyre/CASteer)
   CASteer: Steering Diffusion Models for Controllable Generation


###### Closed-form Optimization
1. [WACV2024] [📄Paper](https://openaccess.thecvf.com/content/WACV2024/papers/Gandikota_Unified_Concept_Editing_in_Diffusion_Models_WACV_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/unified-concept-editing)
   Unified Concept Editing in Diffusion Models
2. [ECCV2024] [📄Paper](https://link.springer.com/content/pdf/10.1007/978-3-031-73668-1_5.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CharlesGong12/RECE)
   Reliable and Efficient Concept Erasure of Text-to-Image Diffusion Models
3. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lu_MACE_Mass_Concept_Erasure_in_Diffusion_Models_CVPR_2024_paper.pdf)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Shilin-LU/MACE)
   MACE: Mass Concept Erasure in Diffusion Models
4. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2501.01633)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/120L020904/ACE)
   ACE: Anti-Editing Concept Erasure in Text-to-Image Models
5. [arXiv2024] [📄Paper](https://arxiv.org/abs/2410.09140)
   RealEra: Semantic-level Concept Erasure via Neighbor-Concept Mining
6. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.07389)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ddgoodgood/TRCE)
   TRCE: Towards Reliable Malicious Concept Erasure  in Text-to-Image Diffusion Models
7. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.06143v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/WYuan1001/AdaVD)
   Precise, Fast, and Low-cost Concept Erasure in Value Space: Orthogonal Complement Matters
8. [arXiv2025] [📄Paper](https://export.arxiv.org/abs/2503.07392)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Ouxiang-Li/SPEED)
   SPEED: Scalable, Precise, and Efficient Concept Erasure for Diffusion Models


###### Externally guided or explicit intervention optimization
1. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=KeJ6dGkiqb)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-KPOP)
   Hiding and Recovering Knowledge in Text-to-Image Diffusion Models via Learnable Prompts
2. [NeurIPS2024] [📄Paper](https://papers.nips.cc/paper_files/paper/2024/file/92f43b1d33fae4aa1958f75317f0cec1-Paper-Conference.pdf)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/naver-ai/DUO)
   Direct Unlearning Optimization for Robust and Safe Text-to-Image Models


<hr style="height:3px; border:none; background: linear-gradient(to right, #fff, #ddd, #fff);">

##### UNet Level
###### Structural Pruning and Feature Removal
1. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=kSdWcw5mkp)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ruchikachavhan/concept-prune)
   ConceptPrune: Concept Editing in Diffusion Models via Skilled Neuron Pruning
2. [NeurIPS2024] [📄Paper](https://openreview.net/pdf?id=jD1eWpUMOf)
   Pruning for Robust Concept Erasing in Diffusion Models
3. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.02542)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mail-research/CAD-attribution4diffusion)
   Unveiling Concept Attribution in Diffusion Models
4. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2404.03631v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mnpham0417/prompt-agnostic-concept-erasure)
   Robust Concept Erasure Using Task Vectors
5. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.12356)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2503.12356)
   Localized Concept Erasure for Text-to-Image Diffusion Models  Using Training-Free Gated Low-Rank Adaptation


###### Loss-Driven Concept Erasure
1. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Gandikota_Erasing_Concepts_from_Diffusion_Models_ICCV_2023_paper.html) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/erasing)
   Erasing Concepts from Diffusion Models
2. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler)
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
3. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lyu_One-dimensional_Adapter_to_Rule_Them_All_Concepts_Diffusion_Models_and_CVPR_2024_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Con6924/SPM)
   One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications
4. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.11850)
   ACE: Attentional Concept Erasure in Diffusion Models
5. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2401.05779)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/JingWu321/EraseDiff)
   Erasing Undesirable Influence in Diffusion Models
6. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2501.00054)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor)
   AdvAnchor: Enhancing Diffusion Model Unlearning with Adversarial Anchors
7. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2412.00580)
   Continuous Concepts Removal in Text-to-image Diffusion Models
8. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2405.16341)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2405.16341)
   R.A.C.E. : Robust Adversarial Concept Erasure for Secure Text-to-Image Diffusion Model
9. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.12782)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/lileyang1210/ANT)
    Set You Straight: Auto-Steering Denoising Trajectories  to Sidestep Unwanted Concepts
10. [ICLR2024] [📄Paper](https://openreview.net/pdf?id=gn0mIhQGNM)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/Unlearn-Saliency)
    SalUn: Empowering Machine Unlearning via Gradient-based Weight Saliency in Both Image Classification and Generation
11. [NeurIPS2024] [📄Paper](https://arxiv.org/pdf/2410.15618)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-Adversarial-Preservation)
    Erasing Undesirable Concepts in Diffusion Models with Adversarial Preservation
12. [ICLR2025] [📄Paper](https://arxiv.org/pdf/2501.18950)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Adaptive-Guided-Erasure)
    Fantastic Targets for Concept Erasure in Diffusion Models and Where to Find Them
13. [OpenReview2024] [📄Paper](https://openreview.net/pdf?id=Ox2A1WoKLm)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor)
    Towards Robust Concept Erasure in Diffusion Models: Unlearning Identity, Nudity and Artistic Styles
14. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2405.15304v2)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/yongliang-wu/DoCo)
    Unlearning Concepts in Diffusion Model via Concept Domain Correction and Concept Preserving Gradient
15. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2408.16807)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/koushiksrivats/robust-concept-erasing)
    STEREO: Towards Adversarially Robust Concept Erasing from Text-to-Image Generation Models
16. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2410.12777)   [<span style="color:rgb(144,144,144);">:bulb:Code</span>](https://github.com/sail-sg/Meta-Unlearning)
    Meta-Unlearning on Diffusion Models: Preventing Relearning Unlearned Concepts
17. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.19783)
    Fine-Grained Erasure in Text-to-Image Diffusion-based Foundation Models
18. [ACM CCS2024] [📄Paper](https://arxiv.org/pdf/2404.06666)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/LetterLiGo/SafeGen_CCS2024)
    SafeGen: Mitigating Sexually Explicit Content Generation in Text-to-Image Models
19. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2310.05873)
    Implicit Concept Removal of Diffusion Models


###### Additive Module or Parameters
1. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lyu_One-dimensional_Adapter_to_Rule_Them_All_Concepts_Diffusion_Models_and_CVPR_2024_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Con6924/SPM)
   One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications
2. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler)
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
3. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2501.01125)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Maplebb/DuMo)
   DuMo: Dual Encoder Modulation Network for Precise Concept Erasure
4. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.16368)
   Concept Corrector: Erase concepts on the fly for text-to-image diffusion models
5. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.10493)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Visualignment/SafetyDPO)
   SafetyDPO: Scalable Safety Alignment for Text-to-Image Generation

---

#### Optimization-Based Catagorization
###### Adversarial Training
1. [ACM CODASPY2025] [📄Paper](https://arxiv.org/abs/2404.19227)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ssg-research/concept-filtering)
   Espresso: Robust Concept Filtering in Text-to-Image Models
2. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=ZRDhBwKs7l)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Hyun1A/CPE)
   Concept Pinpoint Eraser for Text-to-image Diffusion Models via Residual Attention Gate
3. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=OBjF5I4PWg) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Sirius11311/CoGFD-ICLR25)
   Erasing Concept Combination from Text-to-Image Diffusion Model
4. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.11850)
   ACE: Attentional Concept Erasure in Diffusion Models
5. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.14232)
   CRCE: Coreference-Retention Concept Erasure in Text-to-Image Diffusion  Models
6. [arXiv2024] [📄Paper](https://arxiv.org/abs/2409.17682) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/RichardSunnyMeng/DarkMiner-official-codes)
   Dark Miner: Defend against unsafe generation for text-to-image diffusion models
7. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler)
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
8. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2408.16807)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/koushiksrivats/robust-concept-erasing)
    STEREO: Towards Adversarially Robust Concept Erasing from Text-to-Image Generation Models
9. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2501.05359)
    CROPS: Model-Agnostic Training-Free Framework for Safe Image Synthesis with Latent Diffusion Models
10. [arXiv2024] [📄Paper](https://arxiv.org/abs/2410.09140)
    RealEra: Semantic-level Concept Erasure via Neighbor-Concept Mining
11. [ECCV2024] [📄Paper](https://link.springer.com/content/pdf/10.1007/978-3-031-73668-1_5.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CharlesGong12/RECE)
   Reliable and Efficient Concept Erasure of Text-to-Image Diffusion Models
12. [NeurIPS2024] [📄Paper](https://proceedings.neurips.cc/paper_files/paper/2024/file/40954ac18a457dd5f11145bae6454cdf-Paper-Conference.pdf)    [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/AdvUnlearn)
   Defensive Unlearning with Adversarial Training for Robust Concept Erasure in Diffusion Models
13. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2501.00054)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor)
   AdvAnchor: Enhancing Diffusion Model Unlearning with Adversarial Anchors



###### Closed-form Projections
###### Plug-in Adapters
###### Loss-Based Training Objectives


---
## Evaluation and Benchmarking




---
## Adversarial Attacks




---
## 🔗 Relevant Surveys
[arxiv2025] [📄Paper](https://arxiv.org/abs/2502.14896)
A Comprehensive Survey on Concept Erasure in Text-to-Image Diffusion Models


---
## 📌 Citation

```bibtex
@article{,
  title={},
  author={},
  journal={arXiv:2505.xxxxx},
  year={2025}
}