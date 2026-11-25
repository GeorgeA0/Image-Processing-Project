Cell Nuclei Image Segmentation (Data Science Bowl 2018)

An end-to-end classical digital image processing and computer vision pipeline for detecting and segmenting cell nuclei across diverse microscopy modalities, including dark-background fluorescence and brightfield histology stains.

Current Progress — Phase 1 (EDA & Baseline Benchmarking):

Dataset & Integrity Verification: Automated validation of all 670 training samples (stage1_train), confirming zero missing masks and zero overlapping ground-truth instance labels.

Modality & Polarity Analysis: Identified the critical 90.9% dark-background vs. 9.1% bright-background polarity split, resolution scaling (256×256 to 1040×1388), and nucleus area distributions (p5–p95).

Frequency Domain Profiling: Applied zero-mean, 2D Hann-windowed Fast Fourier Transforms (FFT) with normalized radial power spectra to separate macro-level nuclear structure (< 0.05 cycles/pixel) from high-frequency sensor noise (> 0.25 cycles/pixel).

Competition Metric & Baselines: Implemented the exact DSB 2018 Instance Mean Average Precision (mAP across IoU thresholds 0.50:0.95), establishing a 0.6558 polarity-aware Otsu baseline ahead of Watershed instance splitting in Phase 2.
