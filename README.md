# 🧠 Awesome Comprehensive Concept Suppression

This repository provides a comprehensive investigation of concept erasure methods.

---

## 🔍 Concept Erasure in Text-to-Image Generative Models

**Paper Title:** *Erasing Concepts, Steering Generations: A Comprehensive Survey of Concept Suppression*  📄 **[arXiv Preprint](https://arxiv.org/pdf/2505.19398)**  


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
    - [Semantic Scope](#semantic-scope)
      - [Explicit Concept](#explicit-concept)
      - [Multi-concept](#multi-concept)
      - [Concept Combination](#concept-combination)
  - [Datasets](#datasets)
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
1. [BMVC2024] [📄Paper](https://bmvc2024.org/proceedings/216/)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/fmp453/few-shot-erasing)    <br>
   Erasing Concepts from Text-to-Image Diffusion Models  with Few-shot Unlearning   
   
###### Loss-Based Embedding Modification
1. [NeurIPS2024] [📄Paper](https://proceedings.neurips.cc/paper_files/paper/2024/file/40954ac18a457dd5f11145bae6454cdf-Paper-Conference.pdf)    [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/AdvUnlearn)   <br>
   Defensive Unlearning with Adversarial Training for Robust Concept Erasure in Diffusion Models    
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2502.20623)  <br>
   SafeText: Safe Text-to-image Models via Aligning the Text Encoder
3. [arXiv2025] [📄Paper](https://arxiv.org/abs/2412.07249)  <br>
   Buster: Implanting Semantic Backdoor into Text Encoder to Mitigate NSFW  Content Generation

###### Text Encoder–Based Similarity Filtering
1. [ACM CODASPY2025] [📄Paper](https://arxiv.org/abs/2404.19227)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ssg-research/concept-filtering) <br>
   Espresso: Robust Concept Filtering in Text-to-Image Models

###### Principal Components-Based Embedding Modification
1. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.15562)  <br>
   CE-SDWV: Effective and Efficient Concept Erasure for Text-to-Image Diffusion Models via a Semantic-Driven Word Vocabulary
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.16835)  <br>
   Safe and Reliable Diffusion Models via Subspace  Projection
3. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.09446)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/NANSirun/Interpret-then-deactivate)   <br>
   Sparse Autoencoder as a Zero-Shot Classifier for Concept Erasing in Text-to-Image Diffusion Models
4. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.19066)   [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/kim-dahye/steerers)  <br>
   Concept Steerers: Leveraging K-Sparse Autoencoders for Controllable  Generations
5. [ICML2025] [📄Paper](https://icml.cc/virtual/2025/poster/46380)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cywinski/SAeUron)   <br>
   SAeUron: Interpretable Concept Unlearning in Diffusion Models with Sparse Autoencoders

###### Multi-Constraint Embedding Erasure
1. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.18877)        [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/aei13/DES)   <br>
   Distorting Embedding Space for Safety:  A Defense Mechanism for Adversarially Robust Diffusion Models

###### Token-Level Prompt Embedding Adjustment
1. [ECCV2024] [📄Paper](https://arxiv.org/abs/2409.16535)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/DeepakSridhar/promptsliders)  <br>
   Prompt Sliders for Fine-Grained Control, Editing and Erasing of Concepts in Diffusion Models
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.03544)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/PromptGuard-727C/README.md)   <br>
   PromptGuard: Soft Prompt-Guided Unsafe Content Moderation for  Text-to-Image Models
3. [arXiv2025] [📄Paper](https://arxiv.org/abs/2411.10329)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/Embedding-Sanitizer-166E/README.md) <br>
   Safe Text-to-Image Generation: Simply Sanitize the Prompt Embedding
4. [ACM WWW2025] [📄Paper](https://dl.acm.org/doi/10.1145/3696410.3714912)       <br>
   Responsible Diffusion Models via Constraining Text Embeddings within Safe Regions

<hr style="height:3px; border:none; background: linear-gradient(to right, #fff, #ddd, #fff);">

#### Non-Text Encoder Level
##### Cross-Attention-Based Erasure
###### Loss-Based Optimization
1. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Gandikota_Erasing_Concepts_from_Diffusion_Models_ICCV_2023_paper.html) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/erasing)  <br>
   Erasing Concepts from Diffusion Models
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.14232)  <br>
   CRCE: Coreference-Retention Concept Erasure in Text-to-Image Diffusion  Models
3. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Kumari_Ablating_Concepts_in_Text-to-Image_Diffusion_Models_ICCV_2023_paper.pdf) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/nupurkmr9/concept-ablation)  <br>
   Ablating Concepts in Text-to-Image Diffusion Models
4. [NeurIPS2024] [📄Paper](https://openreview.net/pdf?id=8naq3XyGQe) <br>
   Choose Your Anchor Wisely: Effective Unlearning Diffusion Models via Concept Reconditioning
5. [arXiv2024] [📄Paper](https://arxiv.org/abs/2409.17682) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/RichardSunnyMeng/DarkMiner-official-codes)   <br>
   Dark Miner: Defend against unsafe generation for text-to-image diffusion models
6. [arXiv2024] [📄Paper](https://arxiv.org/abs/2402.05947) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Dlut-lab-zmn/SRS-ME) <br>
   Separable Multi-Concept Erasure from Diffusion Models
7. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=OBjF5I4PWg) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Sirius11311/CoGFD-ICLR25) <br>
   Erasing Concept Combination from Text-to-Image Diffusion Model
8. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.13769)   [<span style="color:rgb(37,98,53);">:bulb:Code</span>](https://anonymous.4open.science/r/Decremental-Learning-0659/)   <br>
   Continual Unlearning for Foundational Text-to-Image Models without  Generalization Erosion

 

###### Attention-map-Based Optimization
1. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024W/MMFM/papers/Zhang_Forget-Me-Not_Learning_to_Forget_in_Text-to-Image_Diffusion_Models_CVPRW_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/SHI-Labs/Forget-Me-Not)  <br>
   Forget-Me-Not: Learning to Forget in Text-to-Image Diffusion Models
2. [AAAI2024] [📄Paper](https://ojs.aaai.org/index.php/AAAI/article/view/30107)  <br>
   All but One: Surgical Concept Erasing with Model Preservation in Text-to-Image Diffusion Models
3. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=w4C4z80w59)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CD22104/Growth-Inhibitors-for-Erasure) <br>
   Growth Inhibitors for Suppressing Inappropriate Image Concepts in Diffusion Models
4. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=ZRDhBwKs7l)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Hyun1A/CPE)   <br>
   Concept Pinpoint Eraser for Text-to-image Diffusion Models via Residual Attention Gate
5. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.01244)    [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/zhang-lingyun/ConceptReplacer) <br>
   Concept Replacer: Replacing Sensitive Concepts in Diffusion Models via Precision Localization
6. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.15197)   <br>
   Detect-and-Guide: Self-regulation of Diffusion Models for Safe Text-to-Image  Generation via Guideline Token Optimization
7. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.09630)   [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Atmyre/CASteer) <br>
   CASteer: Steering Diffusion Models for Controllable Generation


###### Closed-form Optimization
1. [WACV2024] [📄Paper](https://openaccess.thecvf.com/content/WACV2024/papers/Gandikota_Unified_Concept_Editing_in_Diffusion_Models_WACV_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/unified-concept-editing)   <br>
   Unified Concept Editing in Diffusion Models
2. [ECCV2024] [📄Paper](https://link.springer.com/content/pdf/10.1007/978-3-031-73668-1_5.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CharlesGong12/RECE)  <br>
   Reliable and Efficient Concept Erasure of Text-to-Image Diffusion Models
3. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lu_MACE_Mass_Concept_Erasure_in_Diffusion_Models_CVPR_2024_paper.pdf)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Shilin-LU/MACE)   <br>
   MACE: Mass Concept Erasure in Diffusion Models
4. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2501.01633)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/120L020904/ACE) <br>
   ACE: Anti-Editing Concept Erasure in Text-to-Image Models
5. [arXiv2024] [📄Paper](https://arxiv.org/abs/2410.09140)  <br>
   RealEra: Semantic-level Concept Erasure via Neighbor-Concept Mining
6. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.07389)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ddgoodgood/TRCE) <br>
   TRCE: Towards Reliable Malicious Concept Erasure  in Text-to-Image Diffusion Models
7. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.06143v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/WYuan1001/AdaVD) <br>
   Precise, Fast, and Low-cost Concept Erasure in Value Space: Orthogonal Complement Matters
8. [arXiv2025] [📄Paper](https://export.arxiv.org/abs/2503.07392)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Ouxiang-Li/SPEED)  <br>
   SPEED: Scalable, Precise, and Efficient Concept Erasure for Diffusion Models


###### Externally guided or explicit intervention optimization
1. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=KeJ6dGkiqb)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-KPOP) <br>
   Hiding and Recovering Knowledge in Text-to-Image Diffusion Models via Learnable Prompts
2. [NeurIPS2024] [📄Paper](https://papers.nips.cc/paper_files/paper/2024/file/92f43b1d33fae4aa1958f75317f0cec1-Paper-Conference.pdf)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/naver-ai/DUO)  <br>
   Direct Unlearning Optimization for Robust and Safe Text-to-Image Models


<hr style="height:3px; border:none; background: linear-gradient(to right, #fff, #ddd, #fff);">

##### UNet Level
###### Structural Pruning and Feature Removal
1. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=kSdWcw5mkp)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ruchikachavhan/concept-prune)   <br>
   ConceptPrune: Concept Editing in Diffusion Models via Skilled Neuron Pruning
2. [NeurIPS2024] [📄Paper](https://openreview.net/pdf?id=jD1eWpUMOf) <br>
   Pruning for Robust Concept Erasing in Diffusion Models
3. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.02542)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mail-research/CAD-attribution4diffusion) <br>
   Unveiling Concept Attribution in Diffusion Models
4. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2404.03631v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mnpham0417/prompt-agnostic-concept-erasure)   <br>
   Robust Concept Erasure Using Task Vectors
5. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.12356)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2503.12356)   <br>
   Localized Concept Erasure for Text-to-Image Diffusion Models  Using Training-Free Gated Low-Rank Adaptation


###### Loss-Driven Concept Erasure
1. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Gandikota_Erasing_Concepts_from_Diffusion_Models_ICCV_2023_paper.html) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/erasing)  <br>
   Erasing Concepts from Diffusion Models
2. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler) <br>
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
3. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lyu_One-dimensional_Adapter_to_Rule_Them_All_Concepts_Diffusion_Models_and_CVPR_2024_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Con6924/SPM)  <br>
   One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications
4. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.11850)  <br>
   ACE: Attentional Concept Erasure in Diffusion Models
5. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2401.05779)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/JingWu321/EraseDiff)  <br>
   Erasing Undesirable Influence in Diffusion Models
6. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2501.00054)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor)  <br>
   AdvAnchor: Enhancing Diffusion Model Unlearning with Adversarial Anchors
7. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2412.00580)  <br>
   Continuous Concepts Removal in Text-to-image Diffusion Models
8. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2405.16341)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2405.16341)   <br>
   R.A.C.E. : Robust Adversarial Concept Erasure for Secure Text-to-Image Diffusion Model
9. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.12782)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/lileyang1210/ANT)  <br>
    Set You Straight: Auto-Steering Denoising Trajectories  to Sidestep Unwanted Concepts
10. [ICLR2024] [📄Paper](https://openreview.net/pdf?id=gn0mIhQGNM)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/Unlearn-Saliency)   <br>
    SalUn: Empowering Machine Unlearning via Gradient-based Weight Saliency in Both Image Classification and Generation
11. [NeurIPS2024] [📄Paper](https://arxiv.org/pdf/2410.15618)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-Adversarial-Preservation)   <br>
    Erasing Undesirable Concepts in Diffusion Models with Adversarial Preservation
12. [ICLR2025] [📄Paper](https://arxiv.org/pdf/2501.18950)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Adaptive-Guided-Erasure)   <br>
    Fantastic Targets for Concept Erasure in Diffusion Models and Where to Find Them
13. [OpenReview2024] [📄Paper](https://openreview.net/pdf?id=Ox2A1WoKLm)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor)   <br>
    Towards Robust Concept Erasure in Diffusion Models: Unlearning Identity, Nudity and Artistic Styles
14. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2405.15304v2)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/yongliang-wu/DoCo)  <br>
    Unlearning Concepts in Diffusion Model via Concept Domain Correction and Concept Preserving Gradient
15. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2408.16807)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/koushiksrivats/robust-concept-erasing)  <br>
    STEREO: Towards Adversarially Robust Concept Erasing from Text-to-Image Generation Models
16. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2410.12777)   [<span style="color:rgb(144,144,144);">:bulb:Code</span>](https://github.com/sail-sg/Meta-Unlearning)   <br>
    Meta-Unlearning on Diffusion Models: Preventing Relearning Unlearned Concepts
17. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.19783)  <br>
    Fine-Grained Erasure in Text-to-Image Diffusion-based Foundation Models
18. [ACM CCS2024] [📄Paper](https://arxiv.org/pdf/2404.06666)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/LetterLiGo/SafeGen_CCS2024)   <br>
    SafeGen: Mitigating Sexually Explicit Content Generation in Text-to-Image Models
19. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2310.05873)  <br>
    Implicit Concept Removal of Diffusion Models


###### Additive Module or Parameters
1. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lyu_One-dimensional_Adapter_to_Rule_Them_All_Concepts_Diffusion_Models_and_CVPR_2024_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Con6924/SPM)  <br>
   One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications
2. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler) <br>
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
3. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2501.01125)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Maplebb/DuMo)   <br>
   DuMo: Dual Encoder Modulation Network for Precise Concept Erasure
4. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.16368)  <br>
   Concept Corrector: Erase concepts on the fly for text-to-image diffusion models
5. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.10493)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Visualignment/SafetyDPO) <br>
   SafetyDPO: Scalable Safety Alignment for Text-to-Image Generation

---

#### Optimization-Based Catagorization
###### Adversarial Training
1. [ACM CODASPY2025] [📄Paper](https://arxiv.org/abs/2404.19227)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ssg-research/concept-filtering) <br>
   Espresso: Robust Concept Filtering in Text-to-Image Models
2. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=ZRDhBwKs7l)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Hyun1A/CPE)   <br>
   Concept Pinpoint Eraser for Text-to-image Diffusion Models via Residual Attention Gate
3. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=OBjF5I4PWg) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Sirius11311/CoGFD-ICLR25) <br>
   Erasing Concept Combination from Text-to-Image Diffusion Model
4. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.11850)  <br>
   ACE: Attentional Concept Erasure in Diffusion Models
5. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.14232)  <br>
   CRCE: Coreference-Retention Concept Erasure in Text-to-Image Diffusion  Models
6. [arXiv2024] [📄Paper](https://arxiv.org/abs/2409.17682) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/RichardSunnyMeng/DarkMiner-official-codes)   <br>
   Dark Miner: Defend against unsafe generation for text-to-image diffusion models
7. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler) <br>
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
8. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2408.16807)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/koushiksrivats/robust-concept-erasing)   <br>
    STEREO: Towards Adversarially Robust Concept Erasing from Text-to-Image Generation Models
9. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2501.05359)  <br>
    CROPS: Model-Agnostic Training-Free Framework for Safe Image Synthesis with Latent Diffusion Models
10. [arXiv2024] [📄Paper](https://arxiv.org/abs/2410.09140) <br>
    RealEra: Semantic-level Concept Erasure via Neighbor-Concept Mining
11. [ECCV2024] [📄Paper](https://link.springer.com/content/pdf/10.1007/978-3-031-73668-1_5.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CharlesGong12/RECE) <br>
   Reliable and Efficient Concept Erasure of Text-to-Image Diffusion Models
12. [NeurIPS2024] [📄Paper](https://proceedings.neurips.cc/paper_files/paper/2024/file/40954ac18a457dd5f11145bae6454cdf-Paper-Conference.pdf)    [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/AdvUnlearn) <br>
   Defensive Unlearning with Adversarial Training for Robust Concept Erasure in Diffusion Models
13. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2501.00054)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor) <br>
   AdvAnchor: Enhancing Diffusion Model Unlearning with Adversarial Anchors



###### Closed-form Projections
1. [WACV2024] [📄Paper](https://openaccess.thecvf.com/content/WACV2024/papers/Gandikota_Unified_Concept_Editing_in_Diffusion_Models_WACV_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/unified-concept-editing)   <br>
   Unified Concept Editing in Diffusion Models
2. [ECCV2024] [📄Paper](https://link.springer.com/content/pdf/10.1007/978-3-031-73668-1_5.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CharlesGong12/RECE)  <br>
   Reliable and Efficient Concept Erasure of Text-to-Image Diffusion Models
3. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lu_MACE_Mass_Concept_Erasure_in_Diffusion_Models_CVPR_2024_paper.pdf)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Shilin-LU/MACE)   <br>
   MACE: Mass Concept Erasure in Diffusion Models
4. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.07389)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ddgoodgood/TRCE) <br>
   TRCE: Towards Reliable Malicious Concept Erasure  in Text-to-Image Diffusion Models
5. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.11850)  <br>
   ACE: Attentional Concept Erasure in Diffusion Models
6. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.06143v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/WYuan1001/AdaVD) <br>
   Precise, Fast, and Low-cost Concept Erasure in Value Space: Orthogonal Complement Matters
7. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2411.15537)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/JingWu321/MUNBa) <br>
   MUNBa: Machine Unlearning via Nash Bargaining
8. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2404.03631v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mnpham0417/prompt-agnostic-concept-erasure)   <br>
   Robust Concept Erasure Using Task Vectors
9. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.12356)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2503.12356)   <br>
   Localized Concept Erasure for Text-to-Image Diffusion Models  Using Training-Free Gated Low-Rank Adaptation
10. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=kSdWcw5mkp)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ruchikachavhan/concept-prune)   <br>
   ConceptPrune: Concept Editing in Diffusion Models via Skilled Neuron Pruning
11. [NeurIPS2024] [📄Paper](https://openreview.net/pdf?id=jD1eWpUMOf) <br>
   Pruning for Robust Concept Erasing in Diffusion Models
12. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.02542)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mail-research/CAD-attribution4diffusion) <br>
   Unveiling Concept Attribution in Diffusion Models
13. [ICLR2024] [📄Paper](https://openreview.net/pdf?id=gn0mIhQGNM)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/Unlearn-Saliency)   <br>
    SalUn: Empowering Machine Unlearning via Gradient-based Weight Saliency in Both Image Classification and Generation
14. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.15562)  <br>
   CE-SDWV: Effective and Efficient Concept Erasure for Text-to-Image Diffusion Models via a Semantic-Driven Word Vocabulary
15. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.16835)  <br>
   Safe and Reliable Diffusion Models via Subspace  Projection
16. [arXiv2024] [📄Paper](https://arxiv.org/abs/2410.09140)  <br>
   RealEra: Semantic-level Concept Erasure via Neighbor-Concept Mining


###### Plug-in Adapters
1. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lyu_One-dimensional_Adapter_to_Rule_Them_All_Concepts_Diffusion_Models_and_CVPR_2024_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Con6924/SPM)  <br>
   One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications
2. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler) <br>
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
3. [ECCV2024] [📄Paper](https://arxiv.org/abs/2409.16535)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/DeepakSridhar/promptsliders)  <br>
   Prompt Sliders for Fine-Grained Control, Editing and Erasing of Concepts in Diffusion Models
4. [ICML2025] [📄Paper](https://arxiv.org/pdf/2412.20413v2)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tomguluson92/eraseanything)  <br>
   EraseAnything: Enabling Concept Erasure in Rectified Flow Transformers
5. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2410.02710)  <br>
   SteerDiff: Steering towards Safe Text-to-Image Diffusion Models
6. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=ZRDhBwKs7l)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Hyun1A/CPE) <br>
   Concept Pinpoint Eraser for Text-to-image Diffusion Models via Residual Attention Gate
7. [arXiv2025] [📄Paper](https://arxiv.org/abs/2411.10329)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/Embedding-Sanitizer-166E/README.md) <br>
   Safe Text-to-Image Generation: Simply Sanitize the Prompt Embedding
8. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2404.08031)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rt219/LatentGuard) <br>
   Latent Guard: a Safety Framework for Text-to-image Generation
9. [NeurIPS2024] [📄Paper](https://arxiv.org/pdf/2403.01446)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cure-lab/GuardT2I) <br>
    GuardT2I: Defending Text-to-Image Models from Adversarial Prompts
10. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2503.09446) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/NANSirun/Interpret-then-deactivate)  <br>
    Sparse Autoencoder as a Zero-Shot Classifier for Concept Erasing in  Text-to-Image Diffusion Models
11. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.19066)   [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/kim-dahye/steerers)  <br>
   Concept Steerers: Leveraging K-Sparse Autoencoders for Controllable  Generations
12. [ICML2025] [📄Paper](https://icml.cc/virtual/2025/poster/46380)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cywinski/SAeUron)   <br>
   SAeUron: Interpretable Concept Unlearning in Diffusion Models with Sparse Autoencoders
13. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.01244)    [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/zhang-lingyun/ConceptReplacer) <br>
   Concept Replacer: Replacing Sensitive Concepts in Diffusion Models via Precision Localization
14. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2501.01125)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Maplebb/DuMo)   <br>
   DuMo: Dual Encoder Modulation Network for Precise Concept Erasure
15. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.16368)  <br>
   Concept Corrector: Erase concepts on the fly for text-to-image diffusion models
16. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.10493)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Visualignment/SafetyDPO) <br>
   SafetyDPO: Scalable Safety Alignment for Text-to-Image Generation
17. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2409.17682)   [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/RichardSunnyMeng/DarkMiner-official-codes) <br>
    Dark Miner: Defend against undesired generation for text-to-image diffusion models
18. [ACM WWW2025] [📄Paper](https://dl.acm.org/doi/10.1145/3696410.3714912)       <br>
   Responsible Diffusion Models via Constraining Text Embeddings within Safe Regions
19. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=KeJ6dGkiqb)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-KPOP) <br>
   Hiding and Recovering Knowledge in Text-to-Image Diffusion Models via Learnable Prompts
20. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.03544)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/PromptGuard-727C/README.md)   <br>
   PromptGuard: Soft Prompt-Guided Unsafe Content Moderation for  Text-to-Image Models
21. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.09630)   [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Atmyre/CASteer) <br>
   CASteer: Steering Diffusion Models for Controllable Generation


###### Loss-Based Training Objectives
1. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Gandikota_Erasing_Concepts_from_Diffusion_Models_ICCV_2023_paper.html) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/erasing)  <br>
   Erasing Concepts from Diffusion Models
2. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024W/MMFM/papers/Zhang_Forget-Me-Not_Learning_to_Forget_in_Text-to-Image_Diffusion_Models_CVPRW_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/SHI-Labs/Forget-Me-Not)  <br>
   Forget-Me-Not: Learning to Forget in Text-to-Image Diffusion Models
3. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2501.01633)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/120L020904/ACE) <br>
   ACE: Anti-Editing Concept Erasure in Text-to-Image Models
4. [CVPR2023] [📄Paper](https://openaccess.thecvf.com/content/CVPR2023/papers/Schramowski_Safe_Latent_Diffusion_Mitigating_Inappropriate_Degeneration_in_Diffusion_Models_CVPR_2023_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://openaccess.thecvf.com/content/CVPR2023/papers/Schramowski_Safe_Latent_Diffusion_Mitigating_Inappropriate_Degeneration_in_Diffusion_Models_CVPR_2023_paper.pdf) <br>
   Safe Latent Diffusion:  Mitigating Inappropriate Degeneration in Diffusion Models
5. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.08011)   
   Training-Free Safe Denoisers for Safe Use of Diffusion Models
6. [AAAI2024] [📄Paper](https://ojs.aaai.org/index.php/AAAI/article/view/30107)  <br>
   All but One: Surgical Concept Erasing with Model Preservation in Text-to-Image Diffusion Models
7. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.07658)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/anubhav1997/TraSCE) <br>
   TraSCE: Trajectory Steering for Concept Erasure
8. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2412.03876)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/JonP07/Diffusion-PNO) <br>
   Safeguarding Text-to-Image Generation via Inference-Time Prompt-Noise  Optimization
9. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=gjwhDHeAsz)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tqch/score-forgetting-distillation) <br>
    Score Forgetting Distillation: A Swift, Data-Free Method for Machine Unlearning in Diffusion Models
10. [ICLR2025] [📄Paper](https://arxiv.org/pdf/2503.01034)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/claserken/SISS) <br>
    Data Unlearning in Diffusion Models
11. [NeurIPS2024] [📄Paper](https://proceedings.neurips.cc/paper_files/paper/2024/file/40954ac18a457dd5f11145bae6454cdf-Paper-Conference.pdf)    [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/AdvUnlearn)   <br>
   Defensive Unlearning with Adversarial Training for Robust Concept Erasure in Diffusion Models  
12. [arXiv2025] [📄Paper](https://arxiv.org/abs/2502.20623)  <br>
   SafeText: Safe Text-to-image Models via Aligning the Text Encoder
13. [arXiv2025] [📄Paper](https://arxiv.org/abs/2412.07249)  <br>
   Buster: Implanting Semantic Backdoor into Text Encoder to Mitigate NSFW  Content Generation
14. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.14232)  <br>
   CRCE: Coreference-Retention Concept Erasure in Text-to-Image Diffusion  Models
15. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Kumari_Ablating_Concepts_in_Text-to-Image_Diffusion_Models_ICCV_2023_paper.pdf) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/nupurkmr9/concept-ablation)  <br>
   Ablating Concepts in Text-to-Image Diffusion Models
16. [NeurIPS2024] [📄Paper](https://openreview.net/pdf?id=8naq3XyGQe) <br>
   Choose Your Anchor Wisely: Effective Unlearning Diffusion Models via Concept Reconditioning
17. [arXiv2024] [📄Paper](https://arxiv.org/abs/2409.17682) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/RichardSunnyMeng/DarkMiner-official-codes)   <br>
   Dark Miner: Defend against unsafe generation for text-to-image diffusion models
18. [arXiv2024] [📄Paper](https://arxiv.org/abs/2402.05947) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Dlut-lab-zmn/SRS-ME) <br>
   Separable Multi-Concept Erasure from Diffusion Models
19. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=OBjF5I4PWg) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang1998/Concept-Selective-Forgetting) <br>
    Erasing Concept Combination from Text-to-Image Diffusion Model
20. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.13769)   [<span style="color:rgb(37,98,53);">:bulb:Code</span>](https://anonymous.4open.science/r/Decremental-Learning-0659/)   <br>
   Continual Unlearning for Foundational Text-to-Image Models without  Generalization Erosion
21. [BMVC2024] [📄Paper](https://bmvc2024.org/proceedings/216/)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/fmp453/few-shot-erasing)    <br>
   Erasing Concepts from Text-to-Image Diffusion Models  with Few-shot Unlearning   
22. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.18877)        [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/aei13/DES)   <br>
   Distorting Embedding Space for Safety:  A Defense Mechanism for Adversarially Robust Diffusion Models
23. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lyu_One-dimensional_Adapter_to_Rule_Them_All_Concepts_Diffusion_Models_and_CVPR_2024_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Con6924/SPM)  <br>
   One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications
24. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler) <br>
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
25. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2412.00580)  <br>
   Continuous Concepts Removal in Text-to-image Diffusion Models
26. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2501.00054)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor)  <br>
   AdvAnchor: Enhancing Diffusion Model Unlearning with Adversarial Anchors
27. [ICLR2024] [📄Paper](https://arxiv.org/pdf/2310.12508) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/optml-group/unlearn-saliency)  <br>
    SalUn: Empowering Machine Unlearning via Gradient-based Weight Saliency in Both Image Classification and Generation
28. [NeurIPS2024] [📄Paper](https://arxiv.org/pdf/2410.15618)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-Adversarial-Preservation)   <br>
    Erasing Undesirable Concepts in Diffusion Models with Adversarial Preservation
29. [ICLR2025] [📄Paper](https://arxiv.org/pdf/2501.18950)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Adaptive-Guided-Erasure)   <br>
    Fantastic Targets for Concept Erasure in Diffusion Models and Where to Find Them
30. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.12782)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/lileyang1210/ANT)  <br>
    Set You Straight: Auto-Steering Denoising Trajectories  to Sidestep Unwanted Concepts
31. [OpenReview2024] [📄Paper](https://openreview.net/pdf?id=Ox2A1WoKLm)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/zhengyuxiang/AdvAnchor)   <br>
    Towards Robust Concept Erasure in Diffusion Models: Unlearning Identity, Nudity and Artistic Styles
32. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.19783)  <br>
    Fine-Grained Erasure in Text-to-Image Diffusion-based Foundation Models
33. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2405.15304v2)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/yongliang-wu/DoCo)  <br>
    Unlearning Concepts in Diffusion Model via Concept Domain Correction and Concept Preserving Gradient
34. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2405.16341)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2405.16341)   <br>
   R.A.C.E. : Robust Adversarial Concept Erasure for Secure Text-to-Image Diffusion Model
35. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2408.16807)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/koushiksrivats/robust-concept-erasing)  <br>
    STEREO: Towards Adversarially Robust Concept Erasing from Text-to-Image Generation Models
36. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.15341)    <br>
    Efficient Fine-Tuning and Concept Suppression for Pruned Diffusion Models
37. [ACM CCS2024] [📄Paper](https://arxiv.org/pdf/2404.06666)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/LetterLiGo/SafeGen_CCS2024)   <br>
    SafeGen: Mitigating Sexually Explicit Content Generation in Text-to-Image Models
38. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2310.05873)  <br>
    Implicit Concept Removal of Diffusion Models

---

#### Semantic Scope
###### Explicit Concept
1. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.18877)        [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/aei13/DES)   <br>
   Distorting Embedding Space for Safety:  A Defense Mechanism for Adversarially Robust Diffusion Models
2. [arXiv2025] [📄Paper](https://arxiv.org/abs/2502.20623)  <br>
   SafeText: Safe Text-to-image Models via Aligning the Text Encoder
3. [ECCV2024] [📄Paper](https://arxiv.org/abs/2409.16535)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/DeepakSridhar/promptsliders)  <br>
   Prompt Sliders for Fine-Grained Control, Editing and Erasing of Concepts in Diffusion Models
4. [arXiv2025] [📄Paper](https://arxiv.org/abs/2501.15562)  <br>
   CE-SDWV: Effective and Efficient Concept Erasure for Text-to-Image Diffusion Models via a Semantic-Driven Word Vocabulary
5. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2404.08031)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rt219/LatentGuard) <br>
   Latent Guard: a Safety Framework for Text-to-image Generation
6. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Gandikota_Erasing_Concepts_from_Diffusion_Models_ICCV_2023_paper.html) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/erasing)  <br>
   Erasing Concepts from Diffusion Models
7. [AAAI2024] [📄Paper](https://ojs.aaai.org/index.php/AAAI/article/view/30107)  <br>
   All but One: Surgical Concept Erasing with Model Preservation in Text-to-Image Diffusion Models
8. [NeurIPS2024] [📄Paper](https://papers.nips.cc/paper_files/paper/2024/file/92f43b1d33fae4aa1958f75317f0cec1-Paper-Conference.pdf)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/naver-ai/DUO)  <br>
   Direct Unlearning Optimization for Robust and Safe Text-to-Image Models
9. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=KeJ6dGkiqb)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-KPOP) <br>
   Hiding and Recovering Knowledge in Text-to-Image Diffusion Models via Learnable Prompts
10. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024W/MMFM/papers/Zhang_Forget-Me-Not_Learning_to_Forget_in_Text-to-Image_Diffusion_Models_CVPRW_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/SHI-Labs/Forget-Me-Not)  <br>
   Forget-Me-Not: Learning to Forget in Text-to-Image Diffusion Models
11. [ICCV2023] [📄Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Kumari_Ablating_Concepts_in_Text-to-Image_Diffusion_Models_ICCV_2023_paper.pdf) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/nupurkmr9/concept-ablation)  <br>
   Ablating Concepts in Text-to-Image Diffusion Models
12. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.01244)    [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/zhang-lingyun/ConceptReplacer) <br>
   Concept Replacer: Replacing Sensitive Concepts in Diffusion Models via Precision Localization
13. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.07389)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ddgoodgood/TRCE) <br>
   TRCE: Towards Reliable Malicious Concept Erasure  in Text-to-Image Diffusion Models
14. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.07658)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/anubhav1997/TraSCE) <br>
   TraSCE: Trajectory Steering for Concept Erasure
15. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2412.03876)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/JonP07/Diffusion-PNO) <br>
   Safeguarding Text-to-Image Generation via Inference-Time Prompt-Noise  Optimization
16. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2411.15537)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/JingWu321/MUNBa) <br>
   MUNBa: Machine Unlearning via Nash Bargaining
17. [NeurIPS2024] [📄Paper](https://arxiv.org/pdf/2410.15618)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Erasing-Adversarial-Preservation)   <br>
    Erasing Undesirable Concepts in Diffusion Models with Adversarial Preservation
18. [NeurIPS2024] [📄Paper](https://openreview.net/pdf?id=jD1eWpUMOf) <br>
   Pruning for Robust Concept Erasing in Diffusion Models
19. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2311.17717)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/jasper0314-huang/Receler) <br>
   Receler: Reliable Concept Erasing of Text-to-Image Diffusion Models via Lightweight Erasers
20. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2405.15304v2)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/yongliang-wu/DoCo)  <br>
    Unlearning Concepts in Diffusion Model via Concept Domain Correction and Concept Preserving Gradient
21. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2501.01633)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/120L020904/ACE) <br>
   ACE: Anti-Editing Concept Erasure in Text-to-Image Models
22. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.02542)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mail-research/CAD-attribution4diffusion) <br>
   Unveiling Concept Attribution in Diffusion Models
23. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2405.16341)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2405.16341)   <br>
   R.A.C.E. : Robust Adversarial Concept Erasure for Secure Text-to-Image Diffusion Model
24. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2401.05779)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/JingWu321/EraseDiff)  <br>
   Erasing Undesirable Influence in Diffusion Models
25. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.15341)    <br>
    Efficient Fine-Tuning and Concept Suppression for Pruned Diffusion Models
26. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=gjwhDHeAsz)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tqch/score-forgetting-distillation) <br>
    Score Forgetting Distillation: A Swift, Data-Free Method for Machine Unlearning in Diffusion Models
27. [ICLR2024] [📄Paper](https://openreview.net/pdf?id=gn0mIhQGNM)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/Unlearn-Saliency)   <br>
    SalUn: Empowering Machine Unlearning via Gradient-based Weight Saliency in Both Image Classification and Generation
28. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2410.12777)   [<span style="color:rgb(144,144,144);">:bulb:Code</span>](https://github.com/sail-sg/Meta-Unlearning)   <br>
    Meta-Unlearning on Diffusion Models: Preventing Relearning Unlearned Concepts
29. [ICLR2025] [📄Paper](https://arxiv.org/pdf/2503.01034)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/claserken/SISS) <br>
    Data Unlearning in Diffusion Models
30. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.19783)  <br>
    Fine-Grained Erasure in Text-to-Image Diffusion-based Foundation Models
31. [ACM CCS2024] [📄Paper](https://arxiv.org/pdf/2404.06666)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/LetterLiGo/SafeGen_CCS2024)   <br>
    SafeGen: Mitigating Sexually Explicit Content Generation in Text-to-Image Models
32. [ACM CODASPY2025] [📄Paper](https://arxiv.org/abs/2404.19227)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ssg-research/concept-filtering) <br>
   Espresso: Robust Concept Filtering in Text-to-Image Models


###### Multi-concept
1. [arXiv2025] [📄Paper](https://arxiv.org/abs/2411.10329)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/Embedding-Sanitizer-166E/README.md) <br>
   Safe Text-to-Image Generation: Simply Sanitize the Prompt Embedding
2. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2410.02710)  <br>
   SteerDiff: Steering towards Safe Text-to-Image Diffusion Models
3. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lu_MACE_Mass_Concept_Erasure_in_Diffusion_Models_CVPR_2024_paper.pdf)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Shilin-LU/MACE)   <br>
   MACE: Mass Concept Erasure in Diffusion Models
4. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=w4C4z80w59)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/CD22104/Growth-Inhibitors-for-Erasure) <br>
   Growth Inhibitors for Suppressing Inappropriate Image Concepts in Diffusion Models
5. [ICML2025] [📄Paper](https://icml.cc/virtual/2025/poster/46380)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cywinski/SAeUron)   <br>
   SAeUron: Interpretable Concept Unlearning in Diffusion Models with Sparse Autoencoders
6. [WACV2024] [📄Paper](https://openaccess.thecvf.com/content/WACV2024/papers/Gandikota_Unified_Concept_Editing_in_Diffusion_Models_WACV_2024_paper.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/unified-concept-editing)   <br>
   Unified Concept Editing in Diffusion Models
7. [arXiv2025] [📄Paper](https://export.arxiv.org/abs/2503.07392)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Ouxiang-Li/SPEED)  <br>
   SPEED: Scalable, Precise, and Efficient Concept Erasure for Diffusion Models
8. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.13769)   [<span style="color:rgb(37,98,53);">:bulb:Code</span>](https://anonymous.4open.science/r/Decremental-Learning-0659/)   <br>
   Continual Unlearning for Foundational Text-to-Image Models without  Generalization Erosion
9. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=kSdWcw5mkp)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ruchikachavhan/concept-prune)   <br>
   ConceptPrune: Concept Editing in Diffusion Models via Skilled Neuron Pruning
10. [CVPR2024] [📄Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Lyu_One-dimensional_Adapter_to_Rule_Them_All_Concepts_Diffusion_Models_and_CVPR_2024_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Con6924/SPM)  <br>
   One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications
11. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2404.03631v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/mnpham0417/prompt-agnostic-concept-erasure)   <br>
   Robust Concept Erasure Using Task Vectors
12. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2405.15304v2)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/yongliang-wu/DoCo)  <br>
    Unlearning Concepts in Diffusion Model via Concept Domain Correction and Concept Preserving Gradient
13. [AAAI2025] [📄Paper](https://arxiv.org/pdf/2501.01125)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Maplebb/DuMo)   <br>
   DuMo: Dual Encoder Modulation Network for Precise Concept Erasure
14. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2412.00580)  <br>
   Continuous Concepts Removal in Text-to-image Diffusion Models
15. [ICLR2025] [📄Paper](https://arxiv.org/pdf/2501.18950)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/tuananhbui89/Adaptive-Guided-Erasure)   <br>
    Fantastic Targets for Concept Erasure in Diffusion Models and Where to Find Them
16. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.16368)  <br>
   Concept Corrector: Erase concepts on the fly for text-to-image diffusion models
17. [CVPR2023] [📄Paper](https://openaccess.thecvf.com/content/CVPR2023/papers/Schramowski_Safe_Latent_Diffusion_Mitigating_Inappropriate_Degeneration_in_Diffusion_Models_CVPR_2023_paper.pdf)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://openaccess.thecvf.com/content/CVPR2023/papers/Schramowski_Safe_Latent_Diffusion_Mitigating_Inappropriate_Degeneration_in_Diffusion_Models_CVPR_2023_paper.pdf) <br>
   Safe Latent Diffusion:  Mitigating Inappropriate Degeneration in Diffusion Models
18. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.08011)   
   Training-Free Safe Denoisers for Safe Use of Diffusion Models
19. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.12356)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://arxiv.org/pdf/2503.12356)   <br>
   Localized Concept Erasure for Text-to-Image Diffusion Models  Using Training-Free Gated Low-Rank Adaptation
20. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2412.10493)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Visualignment/SafetyDPO) <br>
   SafetyDPO: Scalable Safety Alignment for Text-to-Image Generation
21. [arXiv2024] [📄Paper](https://arxiv.org/abs/2402.05947) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Dlut-lab-zmn/SRS-ME) <br>
   Separable Multi-Concept Erasure from Diffusion Models
22. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=ZRDhBwKs7l)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Hyun1A/CPE)   <br>
   Concept Pinpoint Eraser for Text-to-image Diffusion Models via Residual Attention Gate
23. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.06143v2)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/WYuan1001/AdaVD) <br>
   Precise, Fast, and Low-cost Concept Erasure in Value Space: Orthogonal Complement Matters
24. [NeurIPS2024] [📄Paper](https://arxiv.org/pdf/2403.01446)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cure-lab/GuardT2I) <br>
    GuardT2I: Defending Text-to-Image Models from Adversarial Prompts
25. [ACM WWW2025] [📄Paper](https://dl.acm.org/doi/10.1145/3696410.3714912)       <br>
   Responsible Diffusion Models via Constraining Text Embeddings within Safe Regions
26. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2503.15197)   <br>
   Detect-and-Guide: Self-regulation of Diffusion Models for Safe Text-to-Image  Generation via Guideline Token Optimization
27. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2504.11850)  <br>
   ACE: Attentional Concept Erasure in Diffusion Models
28. [arXiv2025] [📄Paper](https://arxiv.org/abs/2503.09630)   [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Atmyre/CASteer) <br>
   CASteer: Steering Diffusion Models for Controllable Generation



###### Concept Combination
1. [ICLR2025] [📄Paper](https://openreview.net/pdf?id=OBjF5I4PWg) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Sirius11311/CoGFD-ICLR25) <br>
   Erasing Concept Combination from Text-to-Image Diffusion Model


--- 
## Datasets
| Dataset  | Year | Task  | paper | Link      |
|----------|------|-------|-------|-----------|
| I2P      | 2023 | NSFW Content |  [Safe Latent Diffusion:  Mitigating Inappropriate Degeneration in Diffusion Models](https://openaccess.thecvf.com/content/CVPR2023/papers/Schramowski_Safe_Latent_Diffusion_Mitigating_Inappropriate_Degeneration_in_Diffusion_Models_CVPR_2023_paper.pdf)  | [Download](https://huggingface.co/datasets/AIML-TUDA/i2p) |
| CIFAR-10 | 2009 | Object Removal | [Learning Multiple Layers of Features from Tiny Images](https://www.cs.toronto.edu/~kriz/learning-features-2009-TR.pdf)                 | [Download](https://huggingface.co/datasets/uoft-cs/cifar10) |
| Small ImageNet | 2023 | Object Removal | [Erasing concepts from diffusion models](https://arxiv.org/pdf/2503.15197)  | [Download](https://github.com/rohitgandikota/erasing/tree/main/data) |
| ESD    | 2023   | Artistic Style | [Erasing concepts from diffusion models](https://arxiv.org/pdf/2503.15197)  | [Download](https://github.com/rohitgandikota/erasing/tree/main/data) |
| WikiArt | 2015  | Artistic Style | [Large-scale Classification of Fine-Art Paintings: Learning The Right Metric on The Right Feature](https://arxiv.org/pdf/1505.00855)  | [Download](https://datasets.activeloop.ai/docs/ml/datasets/wiki-art-dataset/) |
| MACE   | 2024   | Celebrity Identities | [MACE: Mass Concept Erasure in Diffusion Models](https://arxiv.org/pdf/2403.06135)  | [Download](https://github.com/Shilin-LU/MACE/tree/main/prompts_csv) |
| CopyrightMeter | 2024 | Copyright Protection | [CopyrightMeter: Revisiting Copyright Protection in Text-to-image Models](https://arxiv.org/pdf/2411.13144)  | Download |
| Six-CD | 2024 | Multi-Concept Erasure | [Six-CD: Benchmarking Concept Removals for Benign Text-to-image Diffusion Models](https://arxiv.org/pdf/2406.14855)  | [Download](https://github.com/Artanisax/Six-CD) |
| HUB | 2024 | Multi-Concept Erasure | [Holistic Unlearning Benchmark: A Multi-Faceted Evaluation for Text-to-Image Diffusion Model Unlearning](https://arxiv.org/pdf/2410.05664)  | [Download](https://github.com/ml-postech/HUB) |
| UnleanCanvas | 2024 | Multi-Concept Erasure | [UnlearnCanvas: A Stylized Image Dataset to Benchmark Machine Unlearning for Diffusion Models](https://arxiv.org/pdf/2402.11846)  | [Download](https://github.com/OPTML-Group/UnlearnCanvas) |
| COCO-30K | 2014 | Utility | [Microsoft coco: Common objects in context](https://arxiv.org/pdf/1405.0312)  | [Download](https://huggingface.co/datasets/sayakpaul/coco-30-val-2014) |


---
## Evaluation and Benchmarking
1. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2501.09833)   <br>
   EraseBench: Understanding The Ripple Effects of Concept Erasure Techniques
2. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.13989)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/fmp453/erase-eval) <br>
   Erasing with Precision: Evaluating Specific Concept Erasure from Text-to-Image Generative Models
3. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2501.12612)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/adwardlee/t2i_safety) <br>
   T2ISafety: Benchmark for Assessing Fairness, Toxicity, and Privacy in Image Generation
4. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2411.13144)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/bluedream02/CopyrightMeter) <br>
   CopyrightMeter: Revisiting Copyright Protection in Text-to-image Models
5. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2410.05664)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ml-postech/HUB) <br>
   Holistic Unlearning Benchmark:  A Multi-Faceted Evaluation for Text-to-Image Diffusion Model Unlearning
6. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2406.14855)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Artanisax/Six-CD) <br>
   Six-CD: Benchmarking Concept Removals for Benign Text-to-image Diffusion Models
7. [NeurIPS2024] [📄Paper](https://arxiv.org/pdf/2402.11846)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/UnlearnCanvas) <br>
   UnlearnCanvas: A Stylized Image Dataset to Benchmark Machine Unlearning for Diffusion Models


---
## Adversarial Attacks
1. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2503.17987v1)   <br>
   Metaphor-based Jailbreaking Attacks on  Text-to-Image Models
2. [CVPR2025] [📄Paper](https://arxiv.org/pdf/2412.00782)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/matanr/Memories_of_Forgotten_Concepts) <br>
   Memories of Forgotten Concepts
3. [ICML2024] [📄Paper](https://arxiv.org/pdf/2309.06135)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/joycenerd/P4D) <br>
   Prompting4Debugging: Red-Teaming Text-to-Image Diffusion Models by Finding Problematic Prompts
4. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2404.19382)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/hxxdtd/PUND) <br>
   Probing Unlearned Diffusion Models: A Transferable Adversarial Attack Perspective
5. [arXiv2025] [📄Paper](https://arxiv.org/pdf/2502.17537)   <br>
   On the Vulnerability of Concept Erasure in Diffusion Models
6. [ICLR2024] [📄Paper](https://arxiv.org/pdf/2310.10012)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/chiayi-hsu/Ring-A-Bell) <br>
   Ring-A-Bell! How Reliable are Concept Removal Methods for Diffusion Models?
7. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2409.05668)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/respailab/unlearning-or-concealment) <br>
   Unlearning or Concealment? A Critical Analysis and Evaluation Metrics for  Unlearning in Diffusion Models
8. [ICML2024] [📄Paper](https://arxiv.org/pdf/2405.11336)   <br>
   UPAM: Unified Prompt Attack in Text-to-Image Generation Models  Against Both Textual Filters and Visual Checkers
9. [CVPR2024] [📄Paper](https://arxiv.org/pdf/2311.17516)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cure-lab/MMA-Diffusion?tab=readme-ov-file) <br>
    MMA-Diffusion: MultiModal Attack on Diffusion Models
10. [ICLR2024] [📄Paper](https://arxiv.org/pdf/2308.01508)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/NYU-DICE-Lab/circumventing-concept-erasure) <br>
    Circumventing Concept Erasure Methods For Text-to-Image Generative Models
11. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2404.13706)   <br>
    Concept Arithmetics for Circumventing Concept Inhibition in Diffusion Models
12. [NAACL2025] [📄Paper](https://aclanthology.org/2025.findings-naacl.172.pdf)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://aclanthology.org/2025.findings-naacl.172.pdf) <br>
    Jailbreaking Prompt Attack: A Controllable Adversarial Attack against Diffusion Models
13. [arXiv2024] [📄Paper](https://arxiv.org/pdf/2503.01839)    <br>
    Jailbreaking Safeguarded Text-to-Image Models via Large Language Models
14. [ECCV2024] [📄Paper](https://arxiv.org/pdf/2310.11868)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/Diffusion-MU-Attack)  <br>
    To Generate or Not? Safety-Driven  Unlearned Diffusion Models Are Still  Easy to Generate Unsafe Images ... For  Now
15. [Oakland2024] [📄Paper](https://arxiv.org/pdf/2305.12082)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Yuchen413/text2image_safety)  <br>
    SneakyPrompt: Jailbreaking Text-to-image Generative Models
16. [ICML2024] [📄Paper](https://arxiv.org/pdf/2405.16567)  [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Kim-Minseon/APGP)  <br>
    Automatic Jailbreaking of the Text-to-Image Generative AI Systems


---
## 🔗 Relevant Surveys
[arxiv2025] [📄Paper](https://arxiv.org/abs/2502.14896)  <br>
A Comprehensive Survey on Concept Erasure in Text-to-Image Diffusion Models


---
## 📌 Citation

```bibtex
@misc{xie2025erasingconceptssteeringgenerations,
      title={Erasing Concepts, Steering Generations: A Comprehensive Survey of Concept Suppression}, 
      author={Yiwei Xie and Ping Liu* and Zheng Zhang*},
      year={2025},
      eprint={2505.19398},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2505.19398}, 
}
