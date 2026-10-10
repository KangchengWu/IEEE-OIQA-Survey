# Dataset Access Guide

[← Back to the resource hub](../README.md#datasets)

This page follows the 18 datasets in Table 2 of the survey. Years, counts, distortion types, score ranges, and maximum resolutions follow that table. Source-specific access instructions and qualifications are recorded below. Source pages were checked on **2026-10-09**; complete datasets were not downloaded.

**GB**: Gaussian blur; **GN**: Gaussian noise; **WN**: white noise; **BD**: brightness discontinuity; **ST**: stitching distortion. **MOS**: mean opinion score; **DMOS**: differential mean opinion score. Check each dataset's score direction before evaluation.

[CVIQ](#dataset-1) · [OIQA](#dataset-2) · [MVAQD](#dataset-3) · [IQA-ODI](#dataset-4) · [LIVE 3D VR IQA](#dataset-5) · [NBU-HOID](#dataset-6) · [NBU-SOID](#dataset-7) · [SOLID](#dataset-8) · [ISIQA](#dataset-9) · [CROSS](#dataset-10) · [JUFE](#dataset-11) · [OSIQA](#dataset-12) · [JUFE-10K](#dataset-13) · [OIQ-10K](#dataset-14) · [OIQ-10K+](#dataset-15) · [JUFE-10K+](#dataset-16) · [AIGCOIQA2024](#dataset-17) · [OHF2024](#dataset-18)

<a id="dataset-1"></a>

## CVIQ

**2018 · Monocular OIs / ERP · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 16 / 528 | JPEG; H.264/AVC; H.265/HEVC | [0, 100] | 4096 × 2048 |

**Access: Author release**

Baidu access code: `b17u`. Subjective scores are provided in `CVIQ.mat`.

- [Baidu Netdisk](https://pan.baidu.com/s/1b3j5iO3jQWf2fZPAli9ozw)
- [Google Drive](https://drive.google.com/open?id=12E-sDZOq0DfCtNNwdyer7azfLZNNva6N)

Source: [Author / project page](https://github.com/sunwei925/CVIQDatabase)

**Survey reference [8]:** [A large-scale compressed 360-degree spherical image database: From subjective quality evaluation to objective model comparison](https://doi.org/10.1109/mmsp.2018.8547102).

<a id="dataset-2"></a>

## OIQA

**2018 · Monocular OIs / ERP · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 16 / 320 | JPEG; JP2K; GB; GN | [1, 10] | 13320 × 6660 |

**Access: Research mirror**

The download is listed in the GSR authors' repository, a third-party research source. The original dataset authors' current download page has not been confirmed.

- [MEGA mirror](https://mega.nz/file/FqxxRQRR#4Ju2qcmmo6Ced_7nRBXXqAaDcjqxjH2uUFnXIeyE2ts)

Source: [Author / project page](https://github.com/xiangjieSui/GSR)

**Survey reference [5]:** [Perceptual quality assessment of omnidirectional images](https://doi.org/10.1109/iscas.2018.8351786).

<a id="dataset-3"></a>

## MVAQD

**2021 · Monocular OIs / ERP · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 15 / 300 | JPEG; JPEG2000; HEVC; WN; GB | [1, 5] | 5780 × 2890 |

**Access: Email request**

The official README directs users to contact Gangyi Jiang at `jgyvciplab@126.com` to request the data and password.

Source: [Author / project page](https://github.com/Jianghao2019/MVAQD)

**Survey reference [10]:** [Cubemap-based perception-driven blind quality assessment for 360-degree images](https://doi.org/10.1109/tip.2021.3052073).

<a id="dataset-4"></a>

## IQA-ODI

**2021 · Monocular OIs / ERP and multiple projections · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 120 / 960 | JPEG; Projection | [0, 100] | 7680 × 3840 |

**Access: Author release**

Download both the images and the labels. The authors state that **higher DMOS indicates poorer quality**. Account for this direction before comparing with MOS values for which higher scores indicate better quality.

- [Images (Dropbox)](https://www.dropbox.com/s/agmu8ljwal6a25e/all_ref_test_img.zip?dl=0)
- [Labels and metadata](https://www.dropbox.com/sh/2s7x4ddut0i1ymm/AAC2MyM2TlyNLCpzFiHWpFnZa?dl=0)

Source: [Author / project page](https://github.com/yanglixiaoshen/SAP-Net)

**Survey reference [9]:** [Spatial attention-based non-reference perceptual quality prediction network for omnidirectional images](https://doi.org/10.1109/icme51207.2021.9428390).

<a id="dataset-5"></a>

## LIVE 3D VR IQA

**2019 · Stereoscopic OIs / ERP · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 15 / 450 | GB; GN; downsampling; VP9; H.265; ST | [0, 100] | 4096 × 2048 |

**Access: Request form**

The official website requires a download request form. The database includes subjective scores and eye-tracking data.

- [Request form](https://forms.gle/p7bC5P5W6C3md3wT6)

Source: [Author / project page](https://live.ece.utexas.edu/research/VR3D/index.html)

**Survey reference [55]:** [Study of 3D virtual reality picture quality](https://doi.org/10.1109/jstsp.2019.2956408).

<a id="dataset-6"></a>

## NBU-HOID

**2021 · High dynamic range OIs / ERP · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 16 / 320 | JPEG XT; tone mapping | [1, 9] | 5376 × 2688 |

**Access: Author release**

Baidu access code: `lx5g`. The database covers high dynamic range OIs, JPEG XT compression, and tone mapping.

- [Baidu Netdisk](https://pan.baidu.com/s/1lzr7NUqhfQJb4gxyAE5cJA)

Source: [Author / project page](https://github.com/caoliuyan/NBU-HOID)

**Survey reference [56]:** [Quality measurement for high dynamic range omnidirectional image systems](https://doi.org/10.1109/tim.2021.3093940).

<a id="dataset-7"></a>

## NBU-SOID

**2021 · Stereoscopic OIs / ERP · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 12 / 396 | JPEG; JPEG2000; HEVC | [1, 5] | 4096 × 4096 |

**Access: Author release**

Baidu access code: `yr64`; archive password: `NBU-SOID2019`. The authors' README calls the labels DMOS but also describes 1 as worst and 5 as best. Check the actual label definition before deciding the score direction.

- [Baidu Netdisk](https://pan.baidu.com/s/1UKjtZ6XRJ46AF9Hf7vQpOw)

Source: [Author / project page](https://github.com/qyb123/NBU-SOID)

**Survey reference [57]:** [Viewport perception based blind stereoscopic omnidirectional image quality assessment](https://doi.org/10.1109/tcsvt.2020.3043349).

<a id="dataset-8"></a>

## SOLID

**2018 · Stereoscopic OIs / ERP · Homogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 6 / 276 | JPEG; BPG | [1, 5] | 8192 × 4096 |

**Access: Request form**

The official page describes SOLID Phase II and cites the PCM 2018 paper. Its top-bottom stereoscopic representation is 8192 × 8192; distinguish this from the 8192 × 4096 single-view representation listed in the survey.

- [Request form](https://jinshuju.net/f/u3EPcv)

Source: [Author / project page](https://faculty.ustc.edu.cn/chenzhibo/zh_CN/article/988216/content/2461.htm)

**Survey reference [58]:** [Subjective quality assessment of stereoscopic omnidirectional image](https://doi.org/10.1007/978-3-030-00776-8_54).

<a id="dataset-9"></a>

## ISIQA

**2019 · Monocular OIs / ERP · Heterogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 26 / 264 | ST | [0, 100] | 9270 × 1680 |

**Access: Download + password request**

The authors' page provides an archive and asks users to complete a form for its password; use the current form on that page. The count of 26 denotes source scenes, rather than 26 paired pristine panoramic reference images. A [MATLAB implementation of SIQE](https://github.com/pavancm/Stitched-Image-Quality-Evaluator) is also available.

- [Image archive](http://ece.iisc.ac.in/~rajivs/databases/isiqa_release.zip)

Source: [Author / project page](https://pavancm.github.io/stitched-qa/)

**Survey reference [59]:** [Subjective and objective quality assessment of stitched images for virtual reality](https://doi.org/10.1109/tip.2019.2921858).

<a id="dataset-10"></a>

## CROSS

**2019 · Monocular OIs / ERP · Heterogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 292 / 2044 | ST | [0, 100] | 5792 × 2894 |

**Access: Paper only**

The original paper is linked. A current download page from the authors has not been confirmed.

**Survey reference [60]:** [Cross-reference stitching quality assessment for 360 omnidirectional images](https://doi.org/10.1145/3343031.3350973).

<a id="dataset-11"></a>

## JUFE

**2022 · Monocular OIs / ERP · Heterogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 258 / 1032 | GB; GN; BD; ST | [1, 5] | 8192 × 4096 |

**Access: Author release**

Baidu access code: `92rc`. Resources include images, MOS, starting points, head movements, and eye movements.

- [Baidu Netdisk](https://pan.baidu.com/s/1HU3Qp8BCGdCXynYN0ZPTXQ)
- [Google Drive](https://drive.google.com/drive/folders/1ro9D6LOhpd-t6f_X0P5Rx5dkgF8fDJPS?usp=sharing)

Source: [Author / project page](https://github.com/LXLHXL123/JUFE-VRIQA)

**Survey reference [11]:** [Perceptual quality assessment of omnidirectional images](https://doi.org/10.1609/aaai.v36i1.19937).

<a id="dataset-12"></a>

## OSIQA

**2023 · Monocular stitched OIs / ERP · Heterogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 300 / 300 | ST (color, geometric, blur, ghosting) | Not reported | 5792 × 2896 |

**Access: Paper only**

The survey lists 300 / 300, with the first count drawn from 12 raw scenes. These counts are not directly equivalent to conventional paired reference/distorted image counts. A current download page from the authors has not been confirmed.

**Survey reference [61]:** [Attentive deep image quality assessment for omnidirectional stitching](https://doi.org/10.1109/jstsp.2023.3250956).

<a id="dataset-13"></a>

## JUFE-10K

**2024 · Monocular OIs / ERP · Heterogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 430 / 10320 | GN; GB; BD; ST | [1, 5] | 8192 × 4096 |

**Access: Author release**

Baidu access code: `JUFE` (uppercase). The authors' repository provides the dataset and the OIQAND implementation.

- [Baidu Netdisk](https://pan.baidu.com/s/1eL1yee3wISC1QVn4zXnXrw)

Source: [Author / project page](https://github.com/RJL2000/OIQAND)

**Survey reference [6]:** [Subjective and objective quality assessment of non-uniformly distorted omnidirectional images](https://doi.org/10.1109/tmm.2025.3535372).

<a id="dataset-14"></a>

## OIQ-10K

**2024 · Monocular OIs / ERP · Heterogeneous OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 2500 / 7500 | Homogeneous and heterogeneous distortions | [1, 3] | 10320 × 8196 |

**Access: Author release**

Baidu access code: `jvga`. The database comprises 2,500 images without perceptible distortion and 7,500 distorted images, for 10,000 images in total. This does not imply that every distorted image has a paired reference. The repository also provides IQCaption360.

- [Baidu Netdisk](https://pan.baidu.com/s/1Uy0AR9B2oCAIJuLCuZEtLg)
- [MOS and metadata](https://drive.google.com/file/d/1IJgsXB0GcavodXsEa6ee003s5WVp8WtJ/view?usp=sharing)

Source: [Author / project page](https://github.com/WenJuing/IQCaption360)

**Survey reference [12]:** [Omnidirectional image quality captioning: A large-scale database and a new model](https://doi.org/10.1109/tip.2025.3539468).

<a id="dataset-15"></a>

## OIQ-10K+

**2025 · Monocular OIs / ERP · Multimodal OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 2500 / 7500 | Homogeneous and heterogeneous distortions | [1, 3] | 10320 × 8196 |

**Access: Request from authors**

The publisher's Data Availability statement says that data are available from the second author upon reasonable request. Request the extended textual annotations; the base OIQ-10K download is not equivalent to OIQ-10K+. The survey lists 2025, while the journal publication page gives 2026.

Source: [Author / project page](https://link.springer.com/article/10.1007/s11263-025-02626-w)

**Survey reference [62]:** [Blind omnidirectional image quality assessment: Embracing the magic power of multimodal large language models](https://doi.org/10.1007/s11263-025-02626-w).

<a id="dataset-16"></a>

## JUFE-10K+

**2025 · Monocular OIs / ERP · Multimodal OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| 430 / 10320 | GN; GB; BD; ST | [1, 5] | 8192 × 4096 |

**Access: Request from authors**

The publisher states that data are available from the second author upon reasonable request. Distinguish the base JUFE-10K images from the extended quality descriptions. The survey lists 2025, while the journal publication page gives 2026.

Source: [Author / project page](https://link.springer.com/article/10.1007/s11263-025-02626-w)

**Survey reference [62]:** [Blind omnidirectional image quality assessment: Embracing the magic power of multimodal large language models](https://doi.org/10.1007/s11263-025-02626-w).

<a id="dataset-17"></a>

## AIGCOIQA2024

**2024 · AI-generated OIs / ERP · Multimodal OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| - / 300 | AIGC-specific distortion | [0, 100] | 4096 × 2048 |

**Access: Author release**

The authors' README describes 300 generated images, with subjective scores and prompts in `MOS&prompts.xlsx`.

- [TeraBox](https://terabox.com/s/17YIkFc-PFeviUbtGP1ReYQ)

Source: [Author / project page](https://github.com/IntMeGroup/AIGCOIQA)

**Survey reference [7]:** [AIGCOIQA2024: Perceptual quality assessment of AI generated omnidirectional images](https://doi.org/10.1109/icip51287.2024.10647885).

<a id="dataset-18"></a>

## OHF2024

**2025 · AI-generated OIs / ERP · Multimodal OIQA**

| Scale (survey convention) | Distortion type | Score range | Max resolution |
| :--- | :--- | :--- | :--- |
| - / 600 | AIGC-specific distortion | [0, 100] | Not reported |

**Access: Project page**

The corresponding project page has been located, but its README does not list an OHF2024 download. The 300-image AIGCOIQA2024 database must not be substituted for the 600-image OHF2024 database.

Source: [Author / project page](https://github.com/ylylyl-sjtu/BLIP2OIQA-BLIP2OISal)

**Survey reference [63]:** [Quality assessment and distortion-aware saliency prediction for AI-generated omnidirectional images](https://doi.org/10.1109/tcsvt.2025.3616234).
