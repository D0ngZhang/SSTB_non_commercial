# SSTB: Self-Supervised T2WI-Bridged Framework for PDFF Prediction

This repository hosts documentation and controlled-access request information for our SSTB framework.

Due to ongoing IP agreements, pretrained models are available upon request for **non-commercial academic research** and only upon **approval of our industry partners**.

**🔗 [Google Request Form](https://docs.google.com/forms/d/e/1FAIpQLSds-WYsSX7jaM6EVQFzyb7AwtfYgk3hCcZBr3_IivItah9wYQ/viewform?usp=sharing&ouid=100817192501032993715)**
  
*Access is granted under a Non-Commercial Research License. See `Access_Policy.md` for details.*

---

## Overview

**SSTB** is the first framework to predict liver Proton Density Fat Fraction (PDFF) directly from standard ultrasound (US) B-mode images using a self-supervised, T2-weighted MRI (T2WI) bridge.  
This offers a practical, cost-effective alternative to MRI-based PDFF, enabling broad clinical screening for fatty liver diseases.

![Alt Text](doc/framework.png)

## Key Features

- **Self-supervised learning** using both labeled and large-scale unlabeled US data.
- **T2WI bridge:** T2-weighted MRI is used only during training for cross-modal feature alignment.
- **Uncertainty-augmented adversarial loss** for robust segmentation and PDFF prediction.
- **State-of-the-art results:** Outperforms existing multi-task and synthesis methods, even with limited data.

---

## Results

![Alt Text](doc/Result0.png)

![Alt Text](doc/Result1.png)

![Alt Text](doc/Result2.png)

*For complete results and ablation studies, see the manuscript.*

---

## Getting Started

### Requirements

- Python 3.8+
- PyTorch 2.3.1
- SimpleITK
- torchvision
- scikit-image  
(See `requirements.txt` for the full list.)

### Installation

```bash
git clone https://github.com/D0ngZhang/SSTB.git
cd SSTB
pip install -r requirements.txt
```

### Data Preparation
Place all NIfTI files for each subject in a single folder (e.g., data_root/).

Filenames should follow this pattern:
[subject_id]_T2.nii.gz
[subject_id]_DE.nii.gz
[subject_id]_US.nii.gz
[subject_id]_T1_label.nii.gz

All images must be .nii.gz format and spatially aligned.


### License & Citation
This project is released for non-commercial academic research use only.
If you use SSTB in your research, please cite:
```bash
@article{zhang2025sstb,
  title={Self-supervised T2WI-bridged framework for liver segmentation and PDFF prediction from US images},
  author={Dong Zhang and Qi Zeng and Septimiu E. Salcudean and Z. Jane Wang},
  journal={IEEE Transactions on Medical Imaging},
  year={2025}
}
```

