# HadaSmileNet: Hadamard Fusion for Facial Emotion Recognition

[![Paper](https://img.shields.io/badge/Paper-ICDM%202025-blue)](link-to-paper-when-available)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8-blue.svg)](https://python.org)

![Architecture Diagram](fusion_archi.png)

## 🎉 News
- **August 2025**: Paper accepted at IEEE International Conference on Data Mining (ICDM) 2025
- **September 2025**: Repository made public for camera-ready submission
- **Conference Date**: November 12-14, 2025

## Table of Contents
1. [Abstract](#abstract)
2. [Key Contributions](#key-contributions)
3. [Results](#results)
4. [Repository Structure](#repository-structure)
5. [Getting Started](#getting-started)
6. [Reproducing Results](#reproducing-results)
7. [Citation](#citation)
8. [License](#license)

---

## Abstract

**HadaSmileNet** introduces a novel feature fusion framework that directly integrates transformer-based representations with physiologically-grounded D-Markers through parameter-free multiplicative interactions for genuine smile recognition. Unlike multi-task learning approaches that require auxiliary task supervision and complex loss balancing, our method achieves optimal performance through direct Hadamard multiplicative fusion while maintaining computational efficiency during inference.

**Key Achievements:**
- 🏆 **State-of-the-art results** on 4 benchmark datasets
- ⚡ **26% parameter reduction** compared to multi-task alternatives  
- 🎯 **Statistical significance** with p < 0.001 across all improvements
- 📊 **99.7% accuracy** on MMI, **100% accuracy** on BBC dataset

![Performance Comparison](performance_progression.png)

---

## Key Contributions

1. **Novel Fusion Architecture**: Direct integration of handcrafted D-Marker features with transformer representations through Hadamard multiplicative fusion
2. **Computational Efficiency**: 26% parameter reduction and simplified training compared to multi-task learning frameworks  
3. **Comprehensive Evaluation**: Systematic comparison of 15 fusion strategies across 4 benchmark datasets
4. **Statistical Validation**: Rigorous significance testing demonstrating reliable performance improvements
5. **Practical Deployment**: Inference-time efficiency suitable for real-time applications

---

## Results

### Performance on Benchmark Datasets

| Dataset   | Accuracy | Improvement | Statistical Significance |
|-----------|----------|-------------|-------------------------|
| UvA-NEMO  | **88.7%** | +0.8%      | p < 0.001***           |
| MMI       | **99.7%** | -           | -                       |
| SPOS      | **98.5%** | +0.7%      | p < 0.001***           |
| BBC       | **100%**  | +5.0%      | p < 0.001***           |

### Computational Efficiency
- **Training Time Reduction**: 42.3% (p < 0.001)
- **Parameter Reduction**: 26.0% vs DeepMarkerNet
- **Inference Speed**: Comparable to baseline methods

---

## Repository Structure

```
HadaSmileNet/
├── Code/
│   ├── BBC/                    # BBC dataset experiments
│   │   ├── [15 fusion method notebooks]
│   │   ├── dataset/           # Model checkpoints
│   │   ├── core/             # Utility scripts
│   │   ├── labels/           # Cross-validation splits
│   │   └── npy/             # Dataset numpy files
│   ├── SPOS/                  # SPOS dataset experiments
│   ├── UvA-NEMO/             # UvA-NEMO dataset experiments  
│   └── MMI/                   # MMI dataset experiments
├── figures/                   # Paper figures and plots
├── statistical_analysis/     # Statistical significance tests
├── requirements.txt
├── LICENSE
└── README.md
```

---

## Getting Started

### Prerequisites
- Python 3.8+
- CUDA-compatible GPU (recommended)
- 8GB+ RAM

### 1. Clone the Repository
```bash
git clone https://github.com/junayed-hasan/HadaSmileNet.git
cd HadaSmileNet
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Download Datasets
Each dataset folder contains download instructions in the `npy/` directory. Place the downloaded numpy files in the corresponding dataset folders.

### 4. Verify Installation
```bash
cd Code/BBC
jupyter notebook concatenation.ipynb  # Test with simple fusion method
```

---

## Reproducing Results

### Cross-Validation Setup
- **UvA-NEMO**: 10-fold cross-validation
- **BBC**: 10-fold cross-validation  
- **MMI**: 9-fold cross-validation
- **SPOS**: 7-fold cross-validation

### Running Experiments

1. **Individual Fusion Methods**:
   ```bash
   cd Code/[DATASET_NAME]
   jupyter notebook [fusion_method].ipynb
   ```

2. **All 15 Fusion Strategies**:
   Navigate to each dataset folder and run all notebooks sequentially.

3. **Statistical Analysis**:
   ```bash
   cd statistical_analysis
   python statistical_significance_test.py
   ```

### Expected Runtime
- **Single experiment**: ~2-4 hours per dataset
- **Complete evaluation**: ~8-12 hours for all fusion methods
- **Hardware**: NVIDIA T4 GPU or equivalent

---

## Citation

If you use this work in your research, please cite:

```bibtex
@inproceedings{hasan2025hadasmilenet,
  title={HadaSmileNet: Hadamard fusion of handcrafted and deep-learning features for enhancing facial emotion recognition of genuine smiles},
  author={Hasan, Mohammad Junayed and Mohammed, Nabeel and Rahman, Shafin},
  booktitle={Proceedings of the IEEE International Conference on Data Mining (ICDM)},
  year={2025},
  organization={IEEE}
}
```

---

## Acknowledgments

- IEEE International Conference on Data Mining (ICDM) 2025
- Johns Hopkins University Computer Science Department
- North South University Apurba NSU R&D Lab

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Contact

**Mohammad Junayed Hasan**  
Computer Science Department, Johns Hopkins University  
📧 junayedhasan100@gmail.com 
🔗 [GitHub](https://github.com/junayed-hasan)

---

**© 2025 Mohammad Junayed Hasan. Published at IEEE ICDM 2025.**
