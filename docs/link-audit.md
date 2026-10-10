# Sources and Verification

[← Back to the resource hub](../README.md)

**Source-page check: 2026-10-09.** Terminology and references are aligned to the supplied 12-page survey manuscript.

## Scope

- Dataset descriptions and method categories follow the survey; dataset access notes follow the linked source pages.
- Added download links were checked against author websites or project READMEs. Research mirrors are labeled.
- Added implementation links were checked using project titles, author information, documentation, or code files.
- Weight links were taken from the corresponding repositories; checkpoints were not downloaded.
- No request forms were submitted, authors contacted, or cloud-storage accounts accessed. A source-page link does not establish that a complete download succeeds.
- Paper and PDF links retained from the original README were not all individually reverified. Title-search links are identified.
- Benchmark values are transcribed from the survey; experiments were not rerun.

## Dataset Sources

| Dataset | Access | Source |
| :--- | :--- | :--- |
| CVIQ | Author release | [Source page](https://github.com/sunwei925/CVIQDatabase) |
| OIQA | Research mirror | [Source page](https://github.com/xiangjieSui/GSR) |
| MVAQD | Email request | [Source page](https://github.com/Jianghao2019/MVAQD) |
| IQA-ODI | Author release | [Source page](https://github.com/yanglixiaoshen/SAP-Net) |
| LIVE 3D VR IQA | Request form | [Source page](https://live.ece.utexas.edu/research/VR3D/index.html) |
| NBU-HOID | Author release | [Source page](https://github.com/caoliuyan/NBU-HOID) |
| NBU-SOID | Author release | [Source page](https://github.com/qyb123/NBU-SOID) |
| SOLID | Request form | [Source page](https://faculty.ustc.edu.cn/chenzhibo/zh_CN/article/988216/content/2461.htm) |
| ISIQA | Download + password request | [Source page](https://pavancm.github.io/stitched-qa/) |
| CROSS | Paper only | [Paper](https://doi.org/10.1145/3343031.3350973) |
| JUFE | Author release | [Source page](https://github.com/LXLHXL123/JUFE-VRIQA) |
| OSIQA | Paper only | [Paper](https://doi.org/10.1109/jstsp.2023.3250956) |
| JUFE-10K | Author release | [Source page](https://github.com/RJL2000/OIQAND) |
| OIQ-10K | Author release | [Source page](https://github.com/WenJuing/IQCaption360) |
| OIQ-10K+ | Request from authors | [Source page](https://link.springer.com/article/10.1007/s11263-025-02626-w) |
| JUFE-10K+ | Request from authors | [Source page](https://link.springer.com/article/10.1007/s11263-025-02626-w) |
| AIGCOIQA2024 | Author release | [Source page](https://github.com/IntMeGroup/AIGCOIQA) |
| OHF2024 | Project page | [Source page](https://github.com/ylylyl-sjtu/BLIP2OIQA-BLIP2OISal) |

## Implementation Sources

| Entry | Implementation type | Source |
| :--- | :--- | :--- |
| S-PSNR | Third-party implementation | [Repository](https://github.com/xiangjieSui/OIQA-FR-Metrics) |
| WS-PSNR | Third-party implementation | [Repository](https://github.com/xiangjieSui/OIQA-FR-Metrics) |
| CPP-PSNR | Third-party implementation | [Repository](https://github.com/xiangjieSui/OIQA-FR-Metrics) |
| S-SSIM | Third-party implementation | [Repository](https://github.com/xiangjieSui/OIQA-FR-Metrics) |
| VU-BOIQA | Author implementation | [Repository](https://github.com/KangchengWu/OIQA) |
| SAP-Net | Author implementation | [Repository](https://github.com/yanglixiaoshen/SAP-Net) |
| VUGA | Author implementation | [Repository](https://github.com/KangchengWu/VUGA) |
| GAQC | Author implementation | [Repository](https://github.com/liziyi1234/GAQC) |
| MC360IQA | Author implementation | [Repository](https://github.com/sunwei925/MC360IQA) |
| OIQAND | Author implementation | [Repository](https://github.com/RJL2000/OIQAND) |
| MTAOIQA | Author implementation | [Repository](https://github.com/RJL2000/MTAOIQA) |
| IQCaption360 | Author implementation | [Repository](https://github.com/WenJuing/IQCaption360) |
| VGCN | Author implementation | [Repository](https://github.com/weizhou-geek/VGCN-PyTorch) |
| AHGCN | Author implementation | [Repository](https://github.com/JunFu1995/AHGCN) |
| ST360IQ | Author implementation | [Repository](https://github.com/Nafiseh-Tofighi/ST360IQ) |
| Max360IQ | Author implementation | [Repository](https://github.com/WenJuing/Max360IQ) |
| GSR | Author implementation | [Repository](https://github.com/xiangjieSui/GSR) |
| RL-ScanIQA | Author reference implementation | [Repository](https://github.com/wangyuji1/RLScanIQA) |
| Assessor360 | Author implementation | [Repository](https://github.com/TianheWu/Assessor360) |
| ScanDMM | Author implementation | [Repository](https://github.com/xiangjieSui/ScanDMM) |
| X-CLIP | Implementation of the cited paper | [Repository](https://github.com/xuguohai/X-CLIP) |

## Dataset Access Qualifications

- CROSS and OSIQA: a current author download page has not been confirmed.
- OHF2024: a project page was found; a download for its 600-image dataset has not been confirmed.
- OIQ-10K+ and JUFE-10K+: the publication specifies access upon reasonable request. Base image datasets do not replace their extended annotations.
- Form-based and email-based access remain subject to the resource owners' conditions.

## Alignment with the Survey

- Use Homogeneous OIQA, Heterogeneous OIQA, and Multimodal OIQA as the dataset task groups.
- Use the seven method subsection headings from Section III and retain supporting components separately.
- Use full paper titles in the method details and author/reference labels when the survey does not establish a model acronym.
- Describe reference [44] as the lightweight IPSS variant, without introducing an unsupported acronym.
- Mark IPSS [32], its lightweight variant [44], and the visual perception metric [51] as FR; MFAN [37] covers NR and FR.
- Preserve Craster parabolic projection for CPP-PSNR and the survey's phrase “progressive deformation-unaware feature fusion” for VU-BOIQA.
- Keep Assessor360 within human viewing behavior modeling, following the survey's discussion of implicit simulation.
- Retain Table 2 years and annotate differences from publication or project pages.
- Explain the counting or representation conventions for ISIQA, OSIQA, OIQ-10K, and SOLID.

## Maintenance

Keep source URLs and access dates with corrections. A code link alone does not establish successful reproduction. Preserve the existing repository LICENSE; this index does not grant a common license to third-party papers, images, datasets, or implementations.
