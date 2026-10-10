# Methods and Implementations

[← Back to the resource hub](../README.md#methods)

This index retains 61 methods and supporting components from the original resource list. Reference numbers and category headings follow the supplied survey manuscript. Named methods use the manuscript's acronyms; other entries use author names and reference numbers in the overview. Each entry below gives the full paper title.

**FR**: full-reference; **NR**: no-reference. Supporting components provide scanpaths or feature representations. Code and weight links are included where recorded. Third-party implementations are identified explicitly. A title-search link is not a publisher page.

[Conventional OIQA Methods](#category-1) · [OIQA Methods Based on ERP Patches](#category-2) · [OIQA Methods Based on Single-Reprojection Image](#category-3) · [OIQA Methods Based on Multi-Reprojection Image](#category-4) · [OIQA Methods Based on Raw ERP Image](#category-5) · [OIQA Methods With Fixed Viewport Sampling](#category-6) · [OIQA Methods with Saliency-based Viewport Sampling](#category-7) · [OIQA Methods with Human Viewing Behavior Modeling](#category-8) · [Supporting Components](#category-9)

<a id="category-1"></a>

## Conventional OIQA Methods

<a id="method-1"></a>

### S-PSNR

**FR · Survey reference [39]**

**Paper:** A framework to evaluate omnidirectional video coding schemes.

- **Input:** Spherical sampling
- **Modeling:** PSNR with spherical sampling
- **Publication:** [Paper](https://doi.org/10.1109/ismar.2015.12)

**Third-party implementation:** [GitHub](https://github.com/xiangjieSui/OIQA-FR-Metrics)

<a id="method-2"></a>

### WS-PSNR

**FR · Survey reference [17]**

**Paper:** Weighted-to-spherically-uniform quality evaluation for omnidirectional video.

- **Input:** ERP with spherical weighting
- **Modeling:** Spherically uniform weighted PSNR
- **Publication:** [Paper](https://doi.org/10.1109/lsp.2017.2720693)

**Third-party implementation:** [GitHub](https://github.com/xiangjieSui/OIQA-FR-Metrics)

<a id="method-3"></a>

### CPP-PSNR

**FR · Survey reference [16]**

**Paper:** Quality metric for spherical panoramic video.

- **Input:** Craster parabolic projection
- **Modeling:** Craster parabolic projection PSNR
- **Publication:** [Paper](https://doi.org/10.1117/12.2235885)

**Third-party implementation:** [GitHub](https://github.com/xiangjieSui/OIQA-FR-Metrics)

CPP denotes Craster parabolic projection.

<a id="method-4"></a>

### NCP-PSNR

**FR · Survey reference [40]**

**Paper:** Assessing visual quality of omnidirectional videos.

- **Input:** Spherical sampling
- **Modeling:** PSNR adapted to omnidirectional content [40]
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2018.2886277)

[Additional reading link](https://arxiv.org/pdf/1709.06342)

<a id="method-5"></a>

### CP-PSNR

**FR · Survey reference [40]**

**Paper:** Assessing visual quality of omnidirectional videos.

- **Input:** Spherical sampling
- **Modeling:** PSNR adapted to omnidirectional content [40]
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2018.2886277)

[Additional reading link](https://arxiv.org/pdf/1709.06342)

<a id="method-6"></a>

### S-SSIM

**FR · Survey reference [14]**

**Paper:** Spherical structural similarity index for objective omnidirectional video quality assessment.

- **Input:** Spherical sampling
- **Modeling:** Structural similarity on the sphere
- **Publication:** [Paper](https://doi.org/10.1109/icme.2018.8486584)

**Third-party implementation:** [GitHub](https://github.com/xiangjieSui/OIQA-FR-Metrics)

<a id="method-7"></a>

### WS-SSIM

**FR · Survey reference [15]**

**Paper:** Weighted-to-spherically-uniform SSIM objective quality evaluation for panoramic video.

- **Input:** ERP with spherical weighting
- **Modeling:** Spherically uniform weighted SSIM
- **Publication:** [Paper](https://doi.org/10.1109/icsp.2018.8652269)

<a id="category-2"></a>

## OIQA Methods Based on ERP Patches

<a id="method-8"></a>

### VR IQA NET

**NR · Survey reference [41]**

**Paper:** VR IQA NET: Deep virtual reality image quality assessment using adversarial learning.

- **Input:** ERP patches
- **Modeling:** Adversarial patch quality and perceptual weighting
- **Publication:** [Paper](https://doi.org/10.1109/icassp.2018.8461317)

[Additional reading link](https://arxiv.org/pdf/1804.03943)

<a id="method-9"></a>

### DeepVR-IQA

**NR · Survey reference [42]**

**Paper:** Deep virtual reality image quality assessment with human perception guider for omnidirectional image.

- **Input:** ERP patches
- **Modeling:** Human perception guider with deep features
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2019.2898732)

<a id="method-10"></a>

### Sendjasni et al. [43]

**NR · Survey reference [43]**

**Paper:** Adaptive patch labeling and multi-label feature selection for 360-degree image quality assessment.

- **Input:** ERP patches
- **Modeling:** Patch label distributions and feature selection
- **Publication:** [Paper](https://doi.org/10.1109/mmsp59012.2023.10337664)

[Additional reading link](https://hal.science/hal-04729225v1/file/Publications_Sendja-18.pdf)

<a id="method-11"></a>

### VU-BOIQA

**NR · Survey reference [28]**

**Paper:** Viewport-unaware blind omnidirectional image quality assessment: A flexible and effective paradigm.

- **Input:** Adaptive ERP patch sequences
- **Modeling:** Adaptive prior-equator sampling and progressive deformation-unaware feature fusion
- **Publication:** [Paper](https://doi.org/10.1145/3723165)

**Author implementation:** [GitHub](https://github.com/KangchengWu/OIQA)

The linked repository contains `train.py`. Consult the source for training configuration details, as its README is brief.

<a id="method-12"></a>

### IPSS

**FR · Survey reference [32]**

**Paper:** Viewport-unaware full-reference omnidirectional image quality assessment with inter-patch and sequence similarity.

- **Input:** ERP patches and patch sequences
- **Modeling:** Deformation-aware convolution with inter-patch and patch-sequence similarities
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2026.3651643)

A full-reference (FR) method: the quality predictor requires a reference image.

<a id="method-13"></a>

### Yan et al. [44]

**FR · Survey reference [44]**

**Paper:** Towards scalable and efficient full-reference omnidirectional image quality assessment.

- **Input:** ERP patches
- **Modeling:** Cross-patch self-attention for degradation and similarity
- **Publication:** [Paper](https://doi.org/10.1109/lsp.2025.3569458)

The survey describes this as a lightweight version of IPSS [32], using cross-patch self-attention. It is a full-reference (FR) method.

<a id="category-3"></a>

## OIQA Methods Based on Single-Reprojection Image

<a id="method-14"></a>

### Zheng et al. [35]

**NR · Survey reference [35]**

**Paper:** Segmented spherical projection-based blind omnidirectional image quality assessment.

- **Input:** Segmented spherical projection
- **Modeling:** Bipolar/equatorial feature modeling
- **Publication:** [Paper](https://doi.org/10.1109/access.2020.2972158)

[Additional reading link](https://ieeexplore.ieee.org/ielx7/6287639/8948470/08985280.pdf)

<a id="method-15"></a>

### Jiang et al. [10]

**NR · Survey reference [10]**

**Paper:** Cubemap-based perception-driven blind quality assessment for 360-degree images.

- **Input:** Cubemap
- **Modeling:** Attention features and cross-face fusion
- **Publication:** [Paper](https://doi.org/10.1109/tip.2021.3052073)

<a id="method-16"></a>

### Zhou et al. [45]

**NR · Survey reference [45]**

**Paper:** Perception-oriented U-shaped transformer network for 360-degree no-reference image quality assessment.

- **Input:** Cubemap patches
- **Modeling:** Saliency-guided multi-stream Transformer
- **Publication:** [Paper](https://doi.org/10.1109/tbc.2022.3231101)

<a id="method-17"></a>

### OmiQnet

**NR · Survey reference [33]**

**Paper:** OmiQnet: Multiscale feature aggregation convolutional neural network for omnidirectional image assessment.

- **Input:** CMP image
- **Modeling:** Multiscale feature aggregation
- **Publication:** [Paper](https://doi.org/10.1007/s10489-024-05421-1)

<a id="method-18"></a>

### Wang et al. [34]

**NR · Survey reference [34]**

**Paper:** Blind omnidirectional image quality assessment based on semantic information replenishment.

- **Input:** Cubemap
- **Modeling:** Semantic replenishment across faces
- **Publication:** [Paper](https://doi.org/10.1016/j.jvcir.2024.104241)

<a id="method-19"></a>

### Liu et al. [46]

**NR · Survey reference [46]**

**Paper:** Omnidirectional image quality assessment using frequency-domain information.

- **Input:** CMP image / frequency-domain information
- **Modeling:** Frequency-domain distortion modeling
- **Publication:** [Paper](https://doi.org/10.1016/j.patcog.2025.112882)

<a id="category-4"></a>

## OIQA Methods Based on Multi-Reprojection Image

<a id="method-20"></a>

### Jiang et al. [47]

**NR · Survey reference [47]**

**Paper:** Multi-angle projection based blind omnidirectional image quality assessment.

- **Input:** Multiple projection angles
- **Modeling:** Complementary projection feature fusion
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2021.3128014)

<a id="method-21"></a>

### MFAN

**NR / FR · Survey reference [37]**

**Paper:** MFAN: A multi-projection fusion attention network for no-reference and full-reference panoramic image quality assessment.

- **Input:** Multiple projection formats
- **Modeling:** Multi-projection fusion attention
- **Publication:** [Paper](https://doi.org/10.1109/lsp.2023.3310888)

The paper studies both no-reference (NR) and full-reference (FR) settings.

<a id="method-22"></a>

### Xiao et al. [48]

**NR · Survey reference [48]**

**Paper:** Omnidirectional image quality assessment with gated dual-projection fusion.

- **Input:** ERP and CMP
- **Modeling:** Gated fusion at multiple network stages
- **Publication:** [Paper](https://doi.org/10.1016/j.displa.2025.103173)

<a id="method-23"></a>

### Hu et al. [49]

**NR · Survey reference [49]**

**Paper:** Cross-projection distilling knowledge for omnidirectional image quality assessment.

- **Input:** ERP and alternative projections
- **Modeling:** Cross-projection knowledge distillation from an FR teacher to an NR student
- **Publication:** [Title search](https://www.semanticscholar.org/search?q=Cross-projection+distilling+knowledge+for+omnidirectional+image+quality+assessment)

<a id="method-24"></a>

### Ma et al. [50]

**NR · Survey reference [50]**

**Paper:** Omnidirectional image quality assessment with mutual distillation.

- **Input:** ERP and CMP
- **Modeling:** Mutual distillation between projection branches
- **Publication:** [Paper](https://doi.org/10.1109/tbc.2024.3503435)

<a id="method-25"></a>

### Wan et al. [51]

**FR · Survey reference [51]**

**Paper:** Panoramic image quality evaluation based on visual perception mechanism.

- **Input:** ERP and CMP
- **Modeling:** DCT structural similarity with equatorial bias
- **Publication:** [Title search](https://www.semanticscholar.org/search?q=Panoramic+image+quality+evaluation+based+on+visual+perception+mechanism)

The survey explicitly describes this as an interpretable full-reference (FR) OIQA metric.

<a id="category-5"></a>

## OIQA Methods Based on Raw ERP Image

<a id="method-26"></a>

### SAP-Net

**NR · Survey reference [9]**

**Paper:** Spatial attention-based non-reference perceptual quality prediction network for omnidirectional images.

- **Input:** Raw ERP image
- **Modeling:** Spatial attention without saliency annotations
- **Publication:** [Paper](https://doi.org/10.1109/icme51207.2021.9428390)

**Author implementation:** [GitHub](https://github.com/yanglixiaoshen/SAP-Net)

<a id="method-27"></a>

### Chen et al. [52]

**NR · Survey reference [52]**

**Paper:** No-reference omnidirectional image quality assessment via equirectangular convolution and hierarchically fusion.

- **Input:** Raw ERP image
- **Modeling:** Geometry-adaptive convolution and feature fusion
- **Publication:** [Paper](https://doi.org/10.1145/3573942.3574074)

[Additional reading link](https://dl.acm.org/doi/pdf/10.1145/3573942.3574074)

<a id="method-28"></a>

### VUGA

**NR · Survey reference [29]**

**Paper:** Viewport-unaware blind omnidirectional image quality assessment: A unified and generalized approach.

- **Input:** Raw ERP image
- **Modeling:** Deformable convolution, local-global multi-receptive-field modeling, and progressive hierarchical feature fusion
- **Publication:** [Paper](https://doi.org/10.1109/tmm.2026.3673590)

**Author implementation:** [GitHub](https://github.com/KangchengWu/VUGA)

<a id="method-29"></a>

### GAQC

**NR · Survey reference [53]**

**Paper:** Efficient blind omnidirectional image quality assessment: A 2D perspective.

- **Input:** Raw ERP image
- **Modeling:** Frequency- and coordinate-guided deformable convolution with local-global quality-context modeling
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2026.3694394)

**Author implementation:** [GitHub](https://github.com/liziyi1234/GAQC)

<a id="category-6"></a>

## OIQA Methods With Fixed Viewport Sampling

<a id="method-30"></a>

### MC360IQA

**NR · Survey reference [64]**

**Paper:** MC360IQA: A multi-channel CNN for blind 360-degree image quality assessment.

- **Input:** Six fixed viewports
- **Modeling:** Multi-channel CNN feature fusion
- **Publication:** [Paper](https://doi.org/10.1109/jstsp.2019.2955024)

**Author implementation:** [GitHub](https://github.com/sunwei925/MC360IQA)

<a id="method-31"></a>

### Zhou et al. [65]

**NR · Survey reference [65]**

**Paper:** Omnidirectional image quality assessment by distortion discrimination assisted multi-stream network.

- **Input:** CMP face groups with different projection orientations
- **Modeling:** Auxiliary distortion discrimination
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2021.3081162)

<a id="method-32"></a>

### Liu et al. [66]

**NR · Survey reference [66]**

**Paper:** Dual-level blind omnidirectional image quality assessment network based on human visual perception.

- **Input:** Directional viewports
- **Modeling:** Human attention and inter-viewport correlation
- **Publication:** [Paper](https://doi.org/10.14569/ijacsa.2023.01409112)

[Additional reading link](http://thesai.org/Downloads/Volume14No9/Paper_112-Dual_Level_Blind_Omnidirectional_Image_Quality_Assessment_Network.pdf)

<a id="method-33"></a>

### Feng et al. [67]

**NR · Survey reference [67]**

**Paper:** Omnidirectional image quality assessment based on adaptive multi-viewport fusion.

- **Input:** Uniform spherical viewports
- **Modeling:** Semantic-guided adaptive fusion
- **Publication:** [Title search](https://www.semanticscholar.org/search?q=Omnidirectional+image+quality+assessment+based+on+adaptive+multi-viewport+fusion)

<a id="method-34"></a>

### Zhou et al. [68]

**NR · Survey reference [68]**

**Paper:** No-reference quality assessment for 360-degree images by analysis of multifrequency information and local-global naturalness.

- **Input:** Equatorial viewports and ERP
- **Modeling:** Local/global naturalness plus frequency features
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2021.3081182)

<a id="method-35"></a>

### Liu et al. [69]

**NR · Survey reference [69]**

**Paper:** Blind omnidirectional image quality assessment with representative features and viewport oriented statistical features.

- **Input:** Sampled viewports
- **Modeling:** Local natural scene statistics, local binary pattern structure, and cross-channel color features with SVR
- **Publication:** [Paper](https://doi.org/10.1016/j.jvcir.2023.103770)

<a id="method-36"></a>

### S²

**NR · Survey reference [70]**

**Paper:** Blind Omnidirectional Image Quality Assessment: Integrating Local Statistics and Global Semantics.

- **Input:** Non-uniform viewports plus global ERP
- **Modeling:** Pyramid-based local statistics and global VGG-M semantic features with weighted score fusion
- **Publication:** [Paper](https://doi.org/10.1109/icip49359.2023.10222049)

<a id="method-37"></a>

### OIQAND

**NR · Survey reference [6]**

**Paper:** Subjective and objective quality assessment of non-uniformly distorted omnidirectional images.

- **Input:** Equatorial viewports
- **Modeling:** Multi-scale feature fusion and distortion-adaptive perception
- **Publication:** [Paper](https://doi.org/10.1109/tmm.2025.3535372)

**Author implementation:** [GitHub](https://github.com/RJL2000/OIQAND)

**Weights:** [Baidu Netdisk](https://pan.baidu.com/s/1KeY07G6j5yoWtyREstB7kA?pwd=jufe) · Access code: `jufe`

<a id="method-38"></a>

### MTAOIQA

**NR · Survey reference [72]**

**Paper:** Multitask auxiliary network for perceptual quality assessment of non-uniformly distorted omnidirectional images.

- **Input:** Equatorial viewports
- **Modeling:** Auxiliary multitask feature selection
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2024.3497994)

**Author implementation:** [GitHub](https://github.com/RJL2000/MTAOIQA)

<a id="method-39"></a>

### IQCaption360

**NR · Survey reference [12]**

**Paper:** Omnidirectional image quality captioning: A large-scale database and a new model.

- **Input:** Equatorial viewports and ERP
- **Modeling:** Distortion distribution prediction and quality prediction, converted into quality captions through a textual template
- **Publication:** [Paper](https://doi.org/10.1109/tip.2025.3539468)

**Author implementation:** [GitHub](https://github.com/WenJuing/IQCaption360)

**Weights:** [Google Drive](https://drive.google.com/file/d/1UukN1kKtPkO-2a4ITn3-_d4KD8Dp81oM/view?usp=sharing) · OIQ-10K model weights

<a id="category-7"></a>

## OIQA Methods with Saliency-based Viewport Sampling

<a id="method-41"></a>

### VGCN

**NR · Survey reference [24]**

**Paper:** Blind omnidirectional image quality assessment with viewport oriented graph convolutional networks.

- **Input:** Saliency-selected viewports
- **Modeling:** Viewport graph convolution with fusion of local quality and global OI quality
- **Publication:** [Paper](https://doi.org/10.1109/tcsvt.2020.3015186)

**Author implementation:** [GitHub](https://github.com/weizhou-geek/VGCN-PyTorch)

<a id="method-42"></a>

### AHGCN

**NR · Survey reference [73]**

**Paper:** Adaptive hypergraph convolutional network for no-reference 360-degree image quality assessment.

- **Input:** Saliency-selected viewports
- **Modeling:** Hierarchical hypergraph convolution
- **Publication:** [Paper](https://doi.org/10.1145/3503161.3548337)

**Author implementation:** [GitHub](https://github.com/JunFu1995/AHGCN)

The repository README describes the released implementation as the CVIQD version; its OIQA version remains on the project to-do list.

<a id="method-43"></a>

### Nandhini et al. [74]

**NR · Survey reference [74]**

**Paper:** Attention enabled viewport selection with graph convolution for omnidirectional visual quality assessment.

- **Input:** Attention-selected viewports
- **Modeling:** Spatial dependency modeling with graph convolution
- **Publication:** [Paper](https://doi.org/10.1007/s11042-024-19457-5)

<a id="method-44"></a>

### ST360IQ

**NR · Survey reference [75]**

**Paper:** ST360IQ: No-Reference omnidirectional image quality assessment with spherical vision transformers.

- **Input:** Saliency-selected tangent viewports
- **Modeling:** Spherical vision Transformer
- **Publication:** [Paper](https://doi.org/10.1109/icassp49357.2023.10096750)

**Author implementation:** [GitHub](https://github.com/Nafiseh-Tofighi/ST360IQ)

<a id="category-8"></a>

## OIQA Methods with Human Viewing Behavior Modeling

<a id="method-40"></a>

### Fang22

**NR · Survey reference [11]**

**Paper:** Perceptual quality assessment of omnidirectional images.

- **Input:** Viewports with viewing priors
- **Modeling:** Starting point and exploration-time modeling
- **Publication:** [Paper](https://doi.org/10.1609/aaai.v36i1.19937)

[Additional reading link](https://arxiv.org/pdf/2207.02674)

<a id="method-45"></a>

### Sui et al. [76]

**NR · Survey reference [76]**

**Paper:** Perceptual quality assessment of omnidirectional images as moving camera videos.

- **Input:** Scanpath-derived video frames
- **Modeling:** Temporal pooling of 2D-IQA scores
- **Publication:** [Paper](https://doi.org/10.1109/tvcg.2021.3050888)

<a id="method-46"></a>

### Liu et al. [13]

**NR · Survey reference [13]**

**Paper:** Perceptual quality assessment of omnidirectional images: A benchmark and computational model.

- **Input:** Conditioned viewport sequences
- **Modeling:** Transformer for long-range viewport dependencies
- **Publication:** [Paper](https://doi.org/10.1145/3640344)

<a id="method-47"></a>

### Max360IQ

**NR · Survey reference [77]**

**Paper:** Max360IQ: Blind omnidirectional image quality assessment with multi-axis attention.

- **Input:** Recorded scanpath viewports
- **Modeling:** Multi-axis attention and GRU
- **Publication:** [Paper](https://doi.org/10.1016/j.patcog.2025.111429)

**Author implementation:** [GitHub](https://github.com/WenJuing/Max360IQ)

**Weights:** [Google Drive](https://drive.google.com/drive/folders/18vCXea59S9JMYSaXBAe82mxa-_6i7FFJ) · Pretrained weights provided by the authors

<a id="method-48"></a>

### Zhang et al. [78]

**NR · Survey reference [78]**

**Paper:** No-reference omnidirectional image quality assessment based on joint network.

- **Input:** Pseudo-browsing viewport sequences
- **Modeling:** CNN-based local quality and viewport importance, with recurrent modeling of inter-viewport dependencies
- **Publication:** [Paper](https://doi.org/10.1145/3503161.3548175)

<a id="method-49"></a>

### Zhang et al. [79]

**NR · Survey reference [79]**

**Paper:** Omnidirectional image quality assessment via multi-perceptual feature fusion.

- **Input:** Pseudo-temporal viewport sequences
- **Modeling:** Multi-perceptual feature fusion
- **Publication:** [Paper](https://doi.org/10.1016/j.displa.2025.103302)

<a id="method-50"></a>

### Sendjasni et al. [80]

**NR · Survey reference [80]**

**Paper:** Perceptually-weighted CNN for 360-degree image quality assessment using visual scan-path and JND.

- **Input:** Predicted scanpath viewports
- **Modeling:** CNN-based viewport scores weighted by fixation order, duration, and just-noticeable difference (JND) maps
- **Publication:** [Paper](https://doi.org/10.1109/icip42928.2021.9506044)

<a id="method-51"></a>

### PW-360IQA

**NR · Survey reference [82]**

**Paper:** PW-360IQA: Perceptually-Weighted Multichannel CNN for blind 360-degree image quality assessment.

- **Input:** Perceptual scanpath viewports
- **Modeling:** Weight sharing and agreement-based pooling
- **Publication:** [Paper](https://doi.org/10.3390/s23094242)

[Additional reading link](https://www.mdpi.com/1424-8220/23/9/4242/pdf?version=1682391025)

<a id="method-52"></a>

### Wang et al. [83]

**NR · Survey reference [83]**

**Paper:** Dynamically attentive viewport sequence for no-reference quality assessment of omnidirectional images.

- **Input:** Predicted scanpath viewports
- **Modeling:** Gravitational scanpath and statistical features
- **Publication:** [Paper](https://doi.org/10.3389/fnins.2022.1022041)

[Additional reading link](https://www.frontiersin.org/articles/10.3389/fnins.2022.1022041/pdf)

<a id="method-53"></a>

### ESPOIQA

**NR · Survey reference [84]**

**Paper:** Eye scanpath prediction-based no-reference quality assessment of omnidirectional images.

- **Input:** Fixation-density viewports
- **Modeling:** Heatmap and multi-source feature fusion
- **Publication:** [Paper](https://doi.org/10.1109/tim.2024.3470239)

<a id="method-54"></a>

### GSR

**NR · Survey reference [85]**

**Paper:** Perceptual quality assessment of 360° images based on generative scanpath representation.

- **Input:** Gaze-centered tangent patches
- **Modeling:** ScanDMM-generated scanpaths with X-CLIP
- **Publication:** [Paper](https://doi.org/10.1109/TIP.2025.3583181)

[Additional reading link](https://arxiv.org/abs/2309.03472)

**Author implementation:** [GitHub](https://github.com/xiangjieSui/GSR)

**Weights:** [Google Drive](https://drive.google.com/drive/folders/1djA83UB5bcf-ue5YvW6CUa5e9A_-KE20?usp=drive_link) · GSR pretrained models

<a id="method-55"></a>

### Wang et al. [18]

**NR · Survey reference [18]**

**Paper:** Panoramic image quality assessment based on scanpath prediction and bidimensional feature representation.

- **Input:** Scanpath viewports
- **Modeling:** Minimum entropy difference for fixation prediction, followed by large-kernel local and self-attention global quality modeling
- **Publication:** [Paper](https://doi.org/10.1109/tim.2025.3571161)

<a id="method-56"></a>

### Li et al. [87]

**NR · Survey reference [87]**

**Paper:** Multi-observer scanpaths for omnidirectional image quality assessment.

- **Input:** Viewport graph random walks
- **Modeling:** Ensemble prediction over multiple observers
- **Publication:** [Paper](https://doi.org/10.1109/icsip65915.2025.11171466)

<a id="method-57"></a>

### RL-ScanIQA

**NR · Survey reference [88]**

**Paper:** RL-ScanIQA: Reinforcement-learned scanpaths for blind 360° image quality assessment.

- **Input:** Reinforcement-learned scanpaths
- **Modeling:** Proximal policy optimization for viewport exploration, with an attention-based assessor fusing scanpath features and global ERP features
- **Publication:** [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Wang_RL-ScanIQA_Reinforcement-Learned_Scanpaths_for_Blind_360deg_Image_Quality_Assessment_CVPR_2026_paper.html)

**Author reference implementation:** [GitHub](https://github.com/wangyuji1/RLScanIQA)

The authors provide a reference training implementation without pretrained checkpoints. Reproducing the paper also requires the corresponding data preprocessing and split configurations.

<a id="method-58"></a>

### Assessor360

**NR · Survey reference [26]**

**Paper:** Assessor360: Multi-sequence network for blind omnidirectional image quality assessment.

- **Input:** Pseudo-viewport sequences
- **Modeling:** Recursive probability sampling, multiscale feature aggregation, and temporal modeling of pseudo-viewport sequences
- **Publication:** [Paper](https://doi.org/10.48550/arxiv.2305.10983)

[Additional reading link](https://arxiv.org/pdf/2305.10983)

**Author implementation:** [GitHub](https://github.com/TianheWu/Assessor360)

**Weights:** [GitHub Releases](https://github.com/TianheWu/Assessor360/releases/tag/Assessor360_v1) · Checkpoints for four datasets

<a id="category-9"></a>

## Supporting Components

<a id="method-59"></a>

### ScanDMM

**Component · Survey reference [25]**

**Paper:** ScanDMM: A deep Markov model of scanpath prediction for 360° images.

- **Input:** 360-degree scanpaths
- **Modeling:** Deep Markov scanpath prediction
- **Publication:** [Paper](https://doi.org/10.1109/cvpr52729.2023.00675)

**Author implementation:** [GitHub](https://github.com/xiangjieSui/ScanDMM)

A scanpath prediction component, rather than a standalone OIQA quality predictor.

<a id="method-60"></a>

### Sun et al. [81]

**Component · Survey reference [81]**

**Paper:** Visual scanpath prediction using IOR-ROI recurrent mixture density network.

- **Input:** Scanpaths
- **Modeling:** Inhibition-of-return scanpath prediction
- **Publication:** [Paper](https://doi.org/10.1109/tpami.2019.2956930)

A scanpath prediction component, rather than a standalone OIQA quality predictor.

<a id="method-61"></a>

### X-CLIP

**Component · Survey reference [86]**

**Paper:** X-CLIP: End-to-End multi-grained contrastive learning for video-text retrieval.

- **Input:** Video-text tokens
- **Modeling:** Multi-grained contrastive learning
- **Publication:** [Paper](https://doi.org/10.1145/3503161.3547910)

**Implementation of the cited paper:** [GitHub](https://github.com/xuguohai/X-CLIP)

Reference [86] is the ACM MM 2022 X-CLIP paper on video-text retrieval. The GSR repository uses a Kinetics checkpoint; check the specific X-CLIP variant required by its implementation.
