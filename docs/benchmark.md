# Quantitative Comparison and Analysis

[← Back to the resource hub](../README.md#benchmark)

Values are transcribed from **Table 3** of the survey. The table combines results from the original papers with supplementary retraining reported in VUGA / GAQC. **No models were retrained or evaluated for this resource hub.** Splits and configurations can differ across sources; the table is not an independently reproduced leaderboard under a single protocol. Cross-database averages are not used as an overall ranking.

**SRCC** is Spearman's rank-order correlation coefficient; **PLCC** is Pearson's linear correlation coefficient. Higher values are better for both. The survey applies a four-parameter logistic mapping before computing PLCC. An em dash (—) denotes an unreported result, not zero. **Fang22△** removes the temporal hysteresis module.

Machine-readable data: [benchmark.json](../data/benchmark.json).

## CVIQ

| Method | SRCC ↑ | PLCC ↑ |
| :--- | ---: | ---: |
| S-PSNR | 0.708 | 0.708 |
| WS-PSNR | 0.610 | 0.672 |
| CPP-PSNR | 0.626 | 0.687 |
| WS-SSIM | 0.911 | 0.929 |
| MC360IQA | 0.914 | 0.951 |
| VGCN | 0.965 | 0.963 |
| Fang22△ | 0.683 | 0.710 |
| Assessor360 | 0.964 | 0.977 |
| OIQAND | 0.967 | 0.976 |
| MTAOIQA | 0.962 | 0.965 |
| Max360IQ | 0.966 | 0.970 |
| VU-BOIQA | 0.963 | 0.958 |
| VUGA | 0.970 | 0.984 |
| GAQC | 0.957 | 0.959 |

## OIQA

| Method | SRCC ↑ | PLCC ↑ |
| :--- | ---: | ---: |
| S-PSNR | 0.539 | 0.599 |
| WS-PSNR | 0.526 | 0.581 |
| CPP-PSNR | 0.514 | 0.568 |
| WS-SSIM | 0.503 | 0.504 |
| MC360IQA | 0.919 | 0.925 |
| VGCN | 0.958 | 0.951 |
| Fang22△ | 0.747 | 0.795 |
| Assessor360 | 0.980 | 0.975 |
| OIQAND | 0.937 | 0.938 |
| MTAOIQA | 0.960 | 0.972 |
| Max360IQ | 0.922 | 0.919 |
| VU-BOIQA | 0.976 | 0.973 |
| VUGA | 0.973 | 0.974 |
| GAQC | 0.983 | 0.985 |

## MVAQD

| Method | SRCC ↑ | PLCC ↑ |
| :--- | ---: | ---: |
| S-PSNR | — | — |
| WS-PSNR | — | — |
| CPP-PSNR | — | — |
| WS-SSIM | — | — |
| MC360IQA | 0.382 | 0.555 |
| VGCN | — | — |
| Fang22△ | 0.469 | 0.475 |
| Assessor360 | 0.961 | 0.972 |
| OIQAND | 0.903 | 0.924 |
| MTAOIQA | 0.592 | 0.642 |
| Max360IQ | 0.724 | 0.769 |
| VU-BOIQA | 0.965 | 0.970 |
| VUGA | 0.966 | 0.973 |
| GAQC | 0.943 | 0.955 |

## IQA-ODI

| Method | SRCC ↑ | PLCC ↑ |
| :--- | ---: | ---: |
| S-PSNR | — | — |
| WS-PSNR | — | — |
| CPP-PSNR | — | — |
| WS-SSIM | — | — |
| MC360IQA | 0.742 | 0.812 |
| VGCN | — | — |
| Fang22△ | 0.310 | 0.474 |
| Assessor360 | 0.957 | 0.963 |
| OIQAND | 0.927 | 0.965 |
| MTAOIQA | 0.335 | 0.528 |
| Max360IQ | 0.797 | 0.731 |
| VU-BOIQA | 0.905 | 0.934 |
| VUGA | 0.967 | 0.978 |
| GAQC | 0.894 | 0.893 |

## AIGCOIQA2024

| Method | SRCC ↑ | PLCC ↑ |
| :--- | ---: | ---: |
| S-PSNR | — | — |
| WS-PSNR | — | — |
| CPP-PSNR | — | — |
| WS-SSIM | — | — |
| MC360IQA | 0.572 | 0.586 |
| VGCN | — | — |
| Fang22△ | 0.460 | 0.457 |
| Assessor360 | 0.914 | 0.912 |
| OIQAND | 0.896 | 0.895 |
| MTAOIQA | 0.456 | 0.432 |
| Max360IQ | 0.409 | 0.505 |
| VU-BOIQA | 0.888 | 0.881 |
| VUGA | 0.913 | 0.868 |
| GAQC | 0.885 | 0.877 |

## JUFE-10K

| Method | SRCC ↑ | PLCC ↑ |
| :--- | ---: | ---: |
| S-PSNR | 0.285 | 0.355 |
| WS-PSNR | 0.284 | 0.353 |
| CPP-PSNR | 0.285 | 0.355 |
| WS-SSIM | 0.249 | 0.388 |
| MC360IQA | 0.620 | 0.620 |
| VGCN | 0.464 | 0.367 |
| Fang22△ | 0.633 | 0.616 |
| Assessor360 | 0.690 | 0.694 |
| OIQAND | 0.800 | 0.800 |
| MTAOIQA | 0.821 | 0.822 |
| Max360IQ | 0.563 | 0.491 |
| VU-BOIQA | 0.782 | 0.781 |
| VUGA | 0.846 | 0.842 |
| GAQC | 0.835 | 0.830 |

## OIQ-10K

| Method | SRCC ↑ | PLCC ↑ |
| :--- | ---: | ---: |
| S-PSNR | 0.251 | 0.302 |
| WS-PSNR | 0.248 | 0.295 |
| CPP-PSNR | 0.248 | 0.295 |
| WS-SSIM | 0.062 | 0.223 |
| MC360IQA | 0.710 | 0.721 |
| VGCN | 0.698 | 0.705 |
| Fang22△ | 0.758 | 0.769 |
| Assessor360 | 0.773 | 0.790 |
| OIQAND | 0.740 | 0.755 |
| MTAOIQA | 0.824 | 0.829 |
| Max360IQ | 0.751 | 0.733 |
| VU-BOIQA | 0.766 | 0.749 |
| VUGA | 0.830 | 0.834 |
| GAQC | 0.842 | 0.837 |

## Computational Cost

| Method | Parameters (M) | FLOPs (G) |
| :--- | ---: | ---: |
| S-PSNR | N/A | N/A |
| WS-PSNR | N/A | N/A |
| CPP-PSNR | N/A | N/A |
| WS-SSIM | N/A | N/A |
| MC360IQA | 22.4 | 30.3 |
| VGCN | 26.5 | 191.5 |
| Fang22△ | 25.2 | 174.3 |
| Assessor360 | 88.2 | 230.5 |
| OIQAND | 88.0 | 124.2 |
| MTAOIQA | 93.0 | 131.4 |
| Max360IQ | 6.2 | 15.1 |
| VU-BOIQA | 30.2 | 40.8 |
| VUGA | 41.2 | 7.5 |
| GAQC | 4.7 | 1.5 |

These values follow the configurations reported in the survey. For practical efficiency comparisons, also record input resolution, viewport count, preprocessing costs, hardware, and end-to-end latency.
