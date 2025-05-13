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
1. [BMVC2024] [Erasing Concepts from Text-to-Image Diffusion Models  with Few-shot Unlearning](https://bmvc2024.org/proceedings/216/)    [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/fmp453/few-shot-erasing)
   
###### Loss-Based Embedding Modification
1. [NeurIPS2024] [Defensive Unlearning with Adversarial Training for Robust Concept Erasure in Diffusion Models](https://proceedings.neurips.cc/paper_files/paper/2024/hash/40954ac18a457dd5f11145bae6454cdf-Abstract-Conference.html)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/OPTML-Group/AdvUnlearn)
2. [arXiv2025] [SafeText: Safe Text-to-image Models via Aligning the Text Encoder](https://arxiv.org/abs/2502.20623)
3. [arXiv2025] [Buster: Implanting Semantic Backdoor into Text Encoder to Mitigate NSFW  Content Generation](https://arxiv.org/abs/2412.07249)

###### Text Encoder–Based Similarity Filtering
1. [ACM CODASPY2025] [Espresso: Robust Concept Filtering in Text-to-Image Models](https://arxiv.org/abs/2404.19227)     [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/ssg-research/concept-filtering)

###### Principal Components-Based Embedding Modification
1. [arXiv2025] [CE-SDWV: Effective and Efficient Concept Erasure for Text-to-Image Diffusion Models via a Semantic-Driven Word Vocabulary](https://arxiv.org/abs/2501.15562)
2. [arXiv2025] [Safe and Reliable Diffusion Models via Subspace  Projection](https://arxiv.org/abs/2503.16835)
3. [arXiv2025] [Sparse Autoencoder as a Zero-Shot Classifier for Concept Erasing in Text-to-Image Diffusion Models](https://arxiv.org/abs/2503.09446)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/NANSirun/Interpret-then-deactivate)
4. [arXiv2025] [Concept Steerers: Leveraging K-Sparse Autoencoders for Controllable  Generations](https://arxiv.org/abs/2501.19066)   [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/kim-dahye/steerers)
5. [ICML2025] [SAeUron: Interpretable Concept Unlearning in Diffusion Models with Sparse Autoencoders](https://icml.cc/virtual/2025/poster/46380)   [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/cywinski/SAeUron)

###### Multi-Constraint Embedding Erasure
1. [arXiv2025] [Distorting Embedding Space for Safety:  A Defense Mechanism for Adversarially Robust Diffusion Models](https://arxiv.org/abs/2501.18877)        [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/aei13/DES)

###### Token-Level Prompt Embedding Adjustment
1. [ECCV2024] [Prompt Sliders for Fine-Grained Control, Editing and Erasing of Concepts in Diffusion Models](https://arxiv.org/abs/2409.16535)       [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/DeepakSridhar/promptsliders)
2. [arXiv2025] [PromptGuard: Soft Prompt-Guided Unsafe Content Moderation for  Text-to-Image Models](https://arxiv.org/abs/2501.03544)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/PromptGuard-727C/README.md)
3. [arXiv2025] [Safe Text-to-Image Generation: Simply Sanitize the Prompt Embedding](https://arxiv.org/abs/2411.10329)      [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://anonymous.4open.science/r/Embedding-Sanitizer-166E/README.md)
4. [ACM WWW2025] [Responsible Diffusion Models via Constraining Text Embeddings within Safe Regions](https://dl.acm.org/doi/10.1145/3696410.3714912)    

<hr style="height:3px; border:none; background: linear-gradient(to right, #fff, #ddd, #fff);">

#### Non-Text Encoder Level
##### Cross-Attention-Based Erasure
###### Loss-Based Optimization
1. [ICCV2023] [Erasing Concepts from Diffusion Models](https://openaccess.thecvf.com/content/ICCV2023/html/Gandikota_Erasing_Concepts_from_Diffusion_Models_ICCV_2023_paper.html) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/rohitgandikota/erasing)
2. [arXiv2025] [CRCE: Coreference-Retention Concept Erasure in Text-to-Image Diffusion  Models](https://arxiv.org/abs/2503.14232)
3. [ICCV2023] [Ablating Concepts in Text-to-Image Diffusion Models](https://openaccess.thecvf.com/content/ICCV2023/papers/Kumari_Ablating_Concepts_in_Text-to-Image_Diffusion_Models_ICCV_2023_paper.pdf) [<span style="color: rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/nupurkmr9/concept-ablation)
4. [NeurIPS2024] [Choose Your Anchor Wisely: Effective Unlearning Diffusion Models via Concept Reconditioning](https://openreview.net/pdf?id=8naq3XyGQe)
5. [arXiv2024] [Dark Miner: Defend against unsafe generation for text-to-image diffusion models](https://arxiv.org/abs/2409.17682) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/RichardSunnyMeng/DarkMiner-official-codes)
6. [arXiv2024] [Separable Multi-Concept Erasure from Diffusion Models](https://arxiv.org/abs/2402.05947) [<span style="color:rgb(37, 98, 53);">:bulb:Code</span>](https://github.com/Dlut-lab-zmn/SRS-ME)
7. [ICLR2025] [Erasing Concept Combination from Text-to-Image Diffusion Model](https://openreview.net/pdf?id=OBjF5I4PWg) [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://github.com/Sirius11311/CoGFD-ICLR25)
8. [arXiv2025] [Continual Unlearning for Foundational Text-to-Image Models without  Generalization Erosion](https://arxiv.org/abs/2503.13769)   [<span style="color:rgb(144, 144, 144);">:bulb:Code</span>](https://anonymous.4open.science/r/Decremental-Learning-0659/)
 

###### Attention-map-Based Optimization



###### Closed-form Optimization
###### Externally guided or explicit intervention optimization

<hr style="height:3px; border:none; background: linear-gradient(to right, #fff, #ddd, #fff);">

##### UNet Level
###### Structural Pruning and Feature Removal
###### Loss-Driven Concept Erasure
###### Additive Module or Parameters

---

### Optimization-Based Catagorization
#### Adversarial Training
#### Closed-form Projections
#### Plug-in Adapters
#### Loss-Based Training Objectives


---
## Evaluation and Benchmarking




---
## Adversarial Attacks




---
## 🔗 Relevant Surveys
[arxiv2025] [A Comprehensive Survey on Concept Erasure in Text-to-Image Diffusion Models](https://arxiv.org/abs/2502.14896)


---
## 📌 Citation

```bibtex
@article{,
  title={},
  author={},
  journal={arXiv:2505.xxxxx},
  year={2025}
}