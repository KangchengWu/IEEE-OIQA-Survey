# OIQA Resource Hub

面向全景/全向图像质量评价（Omnidirectional Image Quality Assessment, OIQA）的论文、数据集、方法和实现资源索引。内容根据 *A Survey of Omnidirectional Image Quality Assessment: Challenges, Status, and Future Work* 整理；仓库只记录第三方资源入口，不重新分发论文、数据集或受版权保护的代码。

## 目录

- [投影表示](#投影表示)
- [论文概览](#论文概览)
- [数据集](#数据集)
- [方法](#方法)
- [视口选择](#视口选择)
- [未来方向](#未来方向)
- [相关资源](#相关资源)
- [维护与更新](#维护与更新)
- [引用](#引用)

## 投影表示

论文将 OIQA 的输入表示归纳为 ERP、CMP、SSP、PYM 和 viewport。它们的几何性质决定了模型需要处理的失真、采样和跨区域关系。

| 表示 | 特点 | 常见质量建模关注点 |
| --- | --- | --- |
| ERP | 规则矩形布局，赤道到两极采样密度不均 | 极区拉伸、非均匀采样、局部失真 |
| CMP | 六个立方体面，几何变形较小 | 面间连续性、跨面信息融合 |
| SSP | 赤道保留 ERP，两极映射为圆形区域 | 赤道与双极区域的分支建模 |
| PYM | 以预设视点为中心的金字塔投影 | 中心高采样、外围欠采样、多投影互补 |
| Viewport | 将球面局部区域重投影为透视图 | 视口选择、扫描路径和跨视口聚合 |

## 论文概览

综述将 OIQA 的问题拆成主观数据库构建和客观质量建模两个层面，并指出三类核心挑战：

- 高质量参考全景图难以获取，拼接、镜头和传输过程会引入隐性失真。
- 受试者需要在 HMD 中探索有限视口，主观实验成本高且容易产生视觉疲劳。
- 模型需要同时处理内容失真、球面几何变形和人类观看行为。

论文用 PLCC 和 SRCC 比较质量预测性能，并在不同数据库、骨干网络、失真建模方式、输入表示和计算量之间进行分析。

## 数据集

下表保留论文数据集表中的规模和任务信息。最后一列只放资源入口：下载页、项目主页和对应论文。空白下载项表示目前没有找到可靠的公开下载地址。

| 数据集 | 年份 | 类型 | 参考图 / 失真图 | 失真类型 | 评分范围 | 任务 | 说明 | 资源链接 |
| --- | ---: | --- | ---: | --- | --- | --- | --- | --- |
| CVIQ | 2018 | Monocular OIs / ERP | 16 / 528 | JPEG; H.264/AVC; H.265/HEVC | [0, 100] | Homogeneous OIQA | Official dataset repository lists this Google Drive link and Baidu Netdisk mirror (https://pan.baidu.com/s/1b3j5iO3jQWf2fZPAli9ozw; password b17u). | [下载](https://drive.google.com/open?id=12E-sDZOq0DfCtNNwdyer7azfLZNNva6N) · [主页](https://github.com/sunwei925/CVIQDatabase) · [论文](https://doi.org/10.1109/mmsp.2018.8547102) |
| OIQA | 2018 | Monocular OIs / ERP | 16 / 320 | JPEG; JP2K; Gaussian blur; Gaussian noise | [1, 10] | Homogeneous OIQA | No reliable direct download URL was present in the survey source. | [论文](https://doi.org/10.1109/iscas.2018.8351786) |
| MVAQD | 2021 | Monocular OIs / ERP | 15 / 300 | JPEG; JPEG2000; HEVC; white noise; Gaussian blur | [1, 5] | Homogeneous OIQA | Repository states that access is by author request; no public download was listed. | [主页](https://github.com/Jianghao2019/MVAQD) · [论文](https://doi.org/10.1109/tip.2021.3052073) |
| IQA-ODI | 2021 | Monocular OIs / ERP and multiple projections | 120 / 960 | JPEG; projection distortion | [0, 100] | Homogeneous OIQA | No reliable direct download URL was present in the survey source. | [论文](https://doi.org/10.1109/icme51207.2021.9428390) |
| LIVE 3D VR IQA | 2019 | Stereoscopic OIs / ERP | 15 / 450 | Gaussian blur; Gaussian noise; downsampling; VP9; H.265; stitching | [0, 100] | Homogeneous OIQA | The previously listed LIVE URL returned 404 during the 2026-08-29 link check; awaiting a current official landing page. | [论文](https://doi.org/10.1109/jstsp.2019.2956408) |
| NBU-HOID | 2021 | HDR OIs / ERP | 16 / 320 | JPEG XT; tone mapping | [1, 9] | Homogeneous OIQA | Official repository lists the Baidu download link; extraction password is lx5g. | [下载](https://pan.baidu.com/s/1lzr7NUqhfQJb4gxyAE5cJA) · [主页](https://github.com/caoliuyan/NBU-HOID) · [论文](https://doi.org/10.1109/tim.2021.3093940) |
| NBU-SOID | 2021 | Stereoscopic OIs / ERP | 12 / 396 | JPEG; JPEG2000; HEVC | [1, 5] | Homogeneous OIQA | Official repository lists the Baidu download link; passcodes are yr64 and NBU-SOID2019. | [下载](https://pan.baidu.com/s/1UKjtZ6XRJ46AF9Hf7vQpOw) · [主页](https://github.com/qyb123/NBU-SOID) · [论文](https://doi.org/10.1109/tcsvt.2020.3043349) |
| SOLID | 2018 | Stereoscopic OIs / ERP | 6 / 276 | JPEG; BPG | [1, 5] | Homogeneous OIQA | No reliable direct download URL was present in the survey source. | [论文](https://doi.org/10.1007/978-3-030-00776-8_54) |
| ISIQA | 2019 | Monocular OIs / ERP | 26 / 264 | Stitching | [0, 100] | Heterogeneous OIQA | No reliable direct download URL was present in the survey source. | [论文](https://doi.org/10.1109/tip.2019.2921858) |
| CROSS | 2019 | Monocular OIs / ERP | 292 / 2044 | Stitching | [0, 100] | Heterogeneous OIQA | No reliable direct download URL was present in the survey source. | [论文](https://doi.org/10.1145/3343031.3350973) |
| JUFE | 2022 | Monocular OIs / ERP | 258 / 1032 | Gaussian blur; Gaussian noise; brightness discontinuity; stitching | [1, 5] | Heterogeneous OIQA | No reliable direct download URL was present in the survey source. | [论文](https://doi.org/10.1609/aaai.v36i1.19937) |
| OSIQA | 2023 | Monocular stitched OIs / ERP | 300 / 300 | Stitching: color; geometric; blur; ghosting | - | Heterogeneous OIQA | 300 distorted OIs from 12 raw scenes. | [论文](https://doi.org/10.1109/jstsp.2023.3250956) |
| JUFE-10K | 2024 | Monocular OIs / ERP | 430 / 10320 | Gaussian noise; Gaussian blur; brightness discontinuity; stitching | [1, 5] | Heterogeneous OIQA | Upstream survey repository is the authoritative starting point; dataset hosting may be external. | [主页](https://github.com/KangchengWu/IEEE-OIQA-Survey) · [论文](https://doi.org/10.1109/tmm.2025.3535372) |
| OIQ-10K | 2024 | Monocular OIs / ERP | 2500 / 7500 | Homogeneous and heterogeneous distortions | [1, 3] | Heterogeneous OIQA | Upstream survey repository is the authoritative starting point; dataset hosting may be external. | [主页](https://github.com/KangchengWu/IEEE-OIQA-Survey) · [论文](https://doi.org/10.1109/tip.2025.3539468) |
| OIQ-10K+ | 2025 | Monocular OIs / ERP | 2500 / 7500 | Homogeneous and heterogeneous distortions | [1, 3] | Multimodal OIQA | Dataset extension described in the survey source. | [主页](https://github.com/KangchengWu/IEEE-OIQA-Survey) · [论文](https://doi.org/10.1007/s11263-025-02626-w) |
| JUFE-10K+ | 2025 | Monocular OIs / ERP | 430 / 10320 | Gaussian noise; Gaussian blur; brightness discontinuity; stitching | [1, 5] | Multimodal OIQA | Dataset extension described in the survey source. | [主页](https://github.com/KangchengWu/IEEE-OIQA-Survey) · [论文](https://doi.org/10.1007/s11263-025-02626-w) |
| AIGCOIQA2024 | 2024 | AI-generated OIs / ERP | - / 300 | AIGC-specific distortion | [0, 100] | Multimodal OIQA | Official repository lists this TeraBox link; MOS and prompts are distributed with the dataset. | [下载](https://terabox.com/s/17YIkFc-PFeviUbtGP1ReYQ) · [主页](https://github.com/IntMeGroup/AIGCOIQA) · [论文](https://doi.org/10.1109/icip51287.2024.10647885) |
| OHF2024 | 2025 | AI-generated OIs / ERP | - / 600 | AIGC-specific distortion | [0, 100] | Multimodal OIQA | Dataset name and year follow Table 2 in the survey source. | [论文](https://doi.org/10.1109/tcsvt.2025.3616234) |

## 方法

方法分类沿用论文的 taxonomy。最后一列统一列出论文、公开 PDF、源码、权重或其他资源；没有确认源码的条目不会猜测仓库地址。

### 传统 OIQA 方法

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| S-PSNR | Spherical sampling | PSNR with spherical sampling | [37](data/papers.csv#L38) | - | [论文](https://doi.org/10.1109/ismar.2015.12) |
| WS-PSNR | ERP with spherical weighting | Spherically uniform weighted PSNR | [17](data/papers.csv#L18) | - | [论文](https://doi.org/10.1109/lsp.2017.2720693) |
| CPP-PSNR | Cubemap / spherical projection | Craster parabolic projection PSNR | [16](data/papers.csv#L17) | - | [论文](https://doi.org/10.1117/12.2235885) |
| NCP-PSNR | Spherical sampling | Non-uniformly weighted PSNR | [38](data/papers.csv#L39) | - | [论文](https://doi.org/10.1109/tcsvt.2018.2886277) · [PDF](https://arxiv.org/pdf/1709.06342) |
| CP-PSNR | Spherical sampling | Content-preserving weighted PSNR | [38](data/papers.csv#L39) | - | [论文](https://doi.org/10.1109/tcsvt.2018.2886277) · [PDF](https://arxiv.org/pdf/1709.06342) |
| S-SSIM | Spherical sampling | Structural similarity on the sphere | [14](data/papers.csv#L15) | - | [论文](https://doi.org/10.1109/icme.2018.8486584) |
| WS-SSIM | ERP with spherical weighting | Spherically uniform weighted SSIM | [15](data/papers.csv#L16) | - | [论文](https://doi.org/10.1109/icsp.2018.8652269) |

### Viewport-unaware 方法

#### ERP patches

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| VR IQA NET | ERP patches | Adversarial patch quality and perceptual weighting | [39](data/papers.csv#L40) | - | [论文](https://doi.org/10.1109/icassp.2018.8461317) · [PDF](https://arxiv.org/pdf/1804.03943) |
| DeepVR-IQA | ERP patches | Human perception guider with deep features | [40](data/papers.csv#L41) | - | [论文](https://doi.org/10.1109/tcsvt.2019.2898732) |
| Adaptive patch labeling and multi-label feature selection | ERP patches | Patch label distributions and feature selection | [41](data/papers.csv#L42) | - | [论文](https://doi.org/10.1109/mmsp59012.2023.10337664) · [PDF](https://hal.science/hal-04729225v1/file/Publications_Sendja-18.pdf) |
| VU-BOIQA | Adaptive ERP patch sequences | Deformation-unaware feature fusion | [27](data/papers.csv#L28) | - | [论文](https://doi.org/10.1145/3723165) |
| IPSS | ERP patches and patch sequences | Inter-patch and sequence similarity | [31](data/papers.csv#L32) | - | [论文](https://doi.org/10.1109/tcsvt.2026.3651643) |
| IPS2 | ERP patches | Cross-patch self-attention for degradation and similarity | [42](data/papers.csv#L43) | - | [论文](https://doi.org/10.1109/lsp.2025.3569458) |

#### Single reprojection

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| SSP-based BIQA | Segmented spherical projection | Bipolar/equatorial feature modeling | [34](data/papers.csv#L35) | - | [论文](https://doi.org/10.1109/access.2020.2972158) · [PDF](https://ieeexplore.ieee.org/ielx7/6287639/8948470/08985280.pdf) |
| Cubemap-based perception-driven BIQA | Cubemap | Attention features and cross-face fusion | [10](data/papers.csv#L11) | MVAQD is the primary benchmark for this method. | [论文](https://doi.org/10.1109/tip.2021.3052073) |
| Perception-oriented U-shaped Transformer | Cubemap patches | Saliency-guided multi-stream Transformer | [43](data/papers.csv#L44) | - | [论文](https://doi.org/10.1109/tbc.2022.3231101) |
| OmiQnet | Cubemap / reprojected images | Multiscale feature aggregation | [32](data/papers.csv#L33) | - | [论文](https://doi.org/10.1007/s10489-024-05421-1) |
| Semantic information replenishment | Cubemap | Semantic replenishment across faces | [33](data/papers.csv#L34) | - | [论文](https://doi.org/10.1016/j.jvcir.2024.104241) |
| Frequency-domain OIQA | Cubemap / frequency domain | Frequency-domain distortion modeling | [44](data/papers.csv#L45) | - | [论文](https://doi.org/10.1016/j.patcog.2025.112882) |

#### Multi reprojection

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| Multi-angle projection BIQA | Multiple projection angles | Complementary projection feature fusion | [45](data/papers.csv#L46) | - | [论文](https://doi.org/10.1109/tcsvt.2021.3128014) |
| MFAN | Multiple projection formats | Multi-projection fusion attention | [36](data/papers.csv#L37) | - | [论文](https://doi.org/10.1109/lsp.2023.3310888) |
| Gated dual-projection fusion | ERP and CMP | Gated fusion at multiple network stages | [46](data/papers.csv#L47) | - | [论文](https://doi.org/10.1016/j.displa.2025.103173) |
| Cross-projection distilling knowledge | ERP and alternative projections | Cross-projection knowledge distillation | [47](data/papers.csv#L48) | - | [论文](https://www.semanticscholar.org/search?q=Cross-projection+distilling+knowledge+for+omnidirectional+image+quality+assessment) |
| Mutual distillation | ERP and CMP | Mutual distillation between projection branches | [48](data/papers.csv#L49) | - | [论文](https://doi.org/10.1109/tbc.2024.3503435) |
| Visual perception mechanism | ERP and CMP | DCT structural similarity with equatorial bias | [49](data/papers.csv#L50) | - | [论文](https://www.semanticscholar.org/search?q=Panoramic+image+quality+evaluation+based+on+visual+perception+mechanism) |

#### Raw ERP

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| SAP-Net | Raw ERP image | Spatial attention without saliency annotations | [9](data/papers.csv#L10) | - | [论文](https://doi.org/10.1109/icme51207.2021.9428390) |
| Equirectangular convolution and hierarchical fusion | Raw ERP image | Geometry-adaptive convolution and feature fusion | [50](data/papers.csv#L51) | - | [论文](https://doi.org/10.1145/3573942.3574074) · [PDF](https://dl.acm.org/doi/pdf/10.1145/3573942.3574074) |
| VUGA | Raw ERP image | Deformable convolution with local-global receptive fields | [28](data/papers.csv#L29) | - | [论文](https://doi.org/10.1109/tmm.2026.3673590) |
| GAQC | Raw ERP image | Frequency/coordinate-guided deformable convolution | [51](data/papers.csv#L52) | - | [论文](https://doi.org/10.1109/tcsvt.2026.3694394) |

### Viewport-aware 方法

#### Fixed viewport sampling

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| MC360IQA | Six fixed viewports | Multi-channel CNN feature fusion | [61](data/papers.csv#L62) | - | [论文](https://doi.org/10.1109/jstsp.2019.2955024) · [源码](https://github.com/sunwei925/MC360IQA) |
| Distortion discrimination assisted multi-stream network | Fixed viewports | Auxiliary distortion discrimination | [62](data/papers.csv#L63) | - | [论文](https://doi.org/10.1109/tcsvt.2021.3081162) |
| Dual-level human-perception network | Directional viewports | Human attention and inter-viewport correlation | [63](data/papers.csv#L64) | - | [论文](https://doi.org/10.14569/ijacsa.2023.01409112) · [PDF](http://thesai.org/Downloads/Volume14No9/Paper_112-Dual_Level_Blind_Omnidirectional_Image_Quality_Assessment_Network.pdf) |
| Adaptive multi-viewport fusion | Uniform spherical viewports | Semantic-guided adaptive fusion | [64](data/papers.csv#L65) | - | [论文](https://www.semanticscholar.org/search?q=Omnidirectional+image+quality+assessment+based+on+adaptive+multi-viewport+fusion) |
| Multifrequency and local-global naturalness | Equatorial viewports and ERP | Local/global naturalness plus frequency features | [65](data/papers.csv#L66) | - | [论文](https://doi.org/10.1109/tcsvt.2021.3081182) |
| Representative and viewport-oriented statistical features | Sampled viewports | Handcrafted viewport statistics with SVR | [66](data/papers.csv#L67) | - | [论文](https://doi.org/10.1016/j.jvcir.2023.103770) |
| S2 | Non-uniform viewports plus global ERP | Local statistics and global semantics | [67](data/papers.csv#L68) | - | [论文](https://doi.org/10.1109/icip49359.2023.10222049) |
| OIQAND | Equatorial viewports | Multi-scale feature fusion and distortion-adaptive perception | [6](data/papers.csv#L7) | - | [论文](https://doi.org/10.1109/tmm.2025.3535372) |
| MTAOIQA | Equatorial viewports | Auxiliary multitask feature selection | [69](data/papers.csv#L70) | - | [论文](https://doi.org/10.1109/tcsvt.2024.3497994) |
| IQCaption360 | Equatorial viewports and ERP | Distortion distribution and quality captioning | [12](data/papers.csv#L13) | - | [论文](https://doi.org/10.1109/tip.2025.3539468) |
| Fang22 | Viewports with viewing priors | Starting point and exploration-time modeling | [11](data/papers.csv#L12) | - | [论文](https://doi.org/10.1609/aaai.v36i1.19937) · [PDF](https://arxiv.org/pdf/2207.02674) |

#### Saliency-based viewport sampling

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| VGCN | Saliency-selected viewports | Graph convolution over viewport nodes | [23](data/papers.csv#L24) | - | [论文](https://doi.org/10.1109/tcsvt.2020.3015186) |
| AHGCN | Saliency-selected viewports | Hierarchical hypergraph convolution | [70](data/papers.csv#L71) | - | [论文](https://doi.org/10.1145/3503161.3548337) |
| Attention-enabled viewport selection with graph convolution | Attention-selected viewports | Spatial dependency modeling with graph convolution | [71](data/papers.csv#L72) | - | [论文](https://doi.org/10.1007/s11042-024-19457-5) |
| ST360IQ | Saliency-selected tangent viewports | Spherical vision Transformer | [72](data/papers.csv#L73) | - | [论文](https://doi.org/10.1109/icassp49357.2023.10096750) |

#### Human viewing behavior

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| Moving-camera video OIQA | Scanpath-derived video frames | Temporal pooling of 2D-IQA scores | [73](data/papers.csv#L74) | - | [论文](https://doi.org/10.1109/tvcg.2021.3050888) |
| Perceptual quality assessment benchmark model | Conditioned viewport sequences | Transformer for long-range viewport dependencies | [13](data/papers.csv#L14) | - | [论文](https://doi.org/10.1145/3640344) |
| Max360IQ | Recorded scanpath viewports | Multi-axis attention and GRU | [74](data/papers.csv#L75) | - | [论文](https://doi.org/10.1016/j.patcog.2025.111429) |
| Joint network | Pseudo-browsing viewport sequences | CNN local quality and viewport importance | [75](data/papers.csv#L76) | - | [论文](https://doi.org/10.1145/3503161.3548175) |
| Multi-perceptual feature fusion | Pseudo-temporal viewport sequences | Multi-perceptual feature fusion | [76](data/papers.csv#L77) | - | [论文](https://doi.org/10.1016/j.displa.2025.103302) |
| Perceptually-weighted CNN with scanpath and JND | Predicted scanpath viewports | Fixation order and JND weighted pooling | [77](data/papers.csv#L78) | - | [论文](https://doi.org/10.1109/icip42928.2021.9506044) |
| PW-360IQA | Perceptual scanpath viewports | Weight sharing and agreement-based pooling | [79](data/papers.csv#L80) | - | [论文](https://doi.org/10.3390/s23094242) · [PDF](https://www.mdpi.com/1424-8220/23/9/4242/pdf?version=1682391025) |
| Dynamically attentive viewport sequence | Predicted scanpath viewports | Gravitational scanpath and statistical features | [80](data/papers.csv#L81) | - | [论文](https://doi.org/10.3389/fnins.2022.1022041) · [PDF](https://www.frontiersin.org/articles/10.3389/fnins.2022.1022041/pdf) |
| Eye scanpath prediction-based OIQA | Fixation-density viewports | Heatmap and multi-source feature fusion | [81](data/papers.csv#L82) | - | [论文](https://doi.org/10.1109/tim.2024.3470239) |
| Generative scanpath representation | Gaze-centered tangent patches | ScanDMM-generated scanpaths with X-CLIP | [82](data/papers.csv#L83) | - | [论文](https://www.semanticscholar.org/search?q=Perceptual+quality+assessment+of+360-degree+images+based+on+generative+scanpath+representation) |
| Panoramic image quality with scanpath prediction | Scanpath viewports | Spatiotemporal scanpath feature representation | [18](data/papers.csv#L19) | - | [论文](https://doi.org/10.1109/tim.2025.3571161) |
| Multi-observer scanpaths | Viewport graph random walks | Ensemble prediction over multiple observers | [84](data/papers.csv#L85) | - | [论文](https://doi.org/10.1109/icsip65915.2025.11171466) |
| RL-ScanIQA | Reinforcement-learned scanpaths | Joint viewport exploration and quality assessment | [85](data/papers.csv#L86) | - | [论文](https://www.semanticscholar.org/search?q=RL-ScanIQA%3A+Reinforcement-learned+scanpaths+for+blind+360-degree+image+quality+assessment) |

#### Implicit viewing simulation

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| Assessor360 | Pseudo-viewport sequences | Multi-sequence feature aggregation | [25](data/papers.csv#L26) | - | [论文](https://doi.org/10.48550/arxiv.2305.10983) · [PDF](https://arxiv.org/pdf/2305.10983) |

### Supporting components

| 方法 | 输入表示 | 质量建模 | 参考文献 | 说明 | 资源链接 |
| --- | --- | --- | ---: | --- | --- |
| ScanDMM | 360-degree scanpaths | Deep Markov scanpath prediction | [24](data/papers.csv#L25) | Used as a scanpath component by later OIQA methods. | [论文](https://doi.org/10.1109/cvpr52729.2023.00675) |
| IOR-ROI recurrent mixture density network | Scanpaths | Inhibition-of-return scanpath prediction | [78](data/papers.csv#L79) | Supporting scanpath model referenced by scanpath-based OIQA. | [论文](https://doi.org/10.1109/tpami.2019.2956930) |
| X-CLIP | Video-text tokens | Multi-grained contrastive learning | [83](data/papers.csv#L84) | Backbone used by generative scanpath representation. | [论文](https://doi.org/10.1145/3503161.3547910) |

## 视口选择

| 视口选择方式 | 代表方法 | 优点 |
| --- | --- | --- |
| Spherical sampling | 均匀分布球面视点 | 覆盖范围广且相对均匀 |
| Saliency sampling | 按显著性热图选择视点 | 聚焦更可能吸引注意力的区域 |
| ScanDMM | 预测连续扫描路径 | 模拟观察者的序列浏览行为 |
| Recursive probability sampling | 按内容和细节概率递归采样 | 同时考虑语义和局部细节 |
| Equatorial sampling | 在赤道固定间隔采样 | 实现简单，符合赤道观察偏置 |

## 未来方向

- **可迁移质量表示**：利用 2D-IQA 数据学习通用内容/失真表示，再适配 OI 的球面几何。
- **主动观看建模**：根据已经获得的质量证据自适应选择下一个视口，并在信息足够时停止探索。
- **空间落地的质量理解**：定位失真区域、识别失真类型和严重程度，并生成与整体分数一致的解释。

## 相关资源

- 参考的通用 IQA 资源索引：<https://github.com/chaofengc/Awesome-Image-Quality-Assessment>。
- 综述论文摘要给出的上游仓库：<https://github.com/KangchengWu/IEEE-OIQA-Survey>。


## 引用

本仓库整理自：

> Wu, K., Yan, J., Zhu, H., Hou, J., and Fang, Y. *A Survey of Omnidirectional Image Quality Assessment: Challenges, Status, and Future Work.*

论文摘要给出的上游仓库：<https://github.com/KangchengWu/IEEE-OIQA-Survey>。引用本索引时，请同时引用上游综述论文和具体资源的原始论文。

## 许可证

目录和维护脚本使用 MIT License。第三方论文、数据集、代码和商标仍归各自权利人所有，使用前请阅读对应许可证和数据使用条款。
