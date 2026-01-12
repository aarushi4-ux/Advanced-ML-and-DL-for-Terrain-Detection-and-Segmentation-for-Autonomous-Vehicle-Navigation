# Advanced-ML-DL-for-Terrain-Detection-and-Segmentation-for-Autonomous-Vehicle-Navigation

## Overview

Deep learning-based terrain segmentation models achieve strong performance on structured urban datasets but suffer significant degradation when deployed in unstructured off-road environments due to domain shift and dataset bias. This project investigates lightweight domain adaptation and simple multimodal extensions to improve cross-domain generalization for terrain segmentation, targeting robustness in real-world autonomous navigation.

This work is conducted under the supervision of a faculty professor, Dr.Raja Muthulagu as part of an academic design project.

---

## Abstract

Although deep learning-based terrain segmentation models perform well on structured urban benchmarks, domain shift and dataset bias cause their dependability to drastically deteriorate when used in unstructured off-road conditions. This limitation poses a major challenge for autonomous navigation systems operating outside controlled settings. This study investigates whether lightweight domain adaptation and usage of multimodal techniques can improve the cross-domain generalization of terrain segmentation models. A pretrained DeepLabV3+ model with a ResNet-50 backbone, pre-trained on ImageNet is trained on the Cityscapes dataset and evaluated on an off-road RUGD terrain dataset, where a substantial performance drop is observed. Domain adaptation is then performed by partially fine-tuning the model on a limited subset of target-domain images, resulting in notable performance improvements. Additionally, a simple multimodal extension using edge-map inputs is explored to assess its impact on cross-domain robustness. Experimental results show that lightweight domain adaptation significantly reduces cross-domain performance degradation, however multimodal inputs provide more localized and inconsistent improvements. These results offer useful insights for enhancing terrain segmentation robustness in real-world autonomous navigation scenarios and show the advantages and disadvantages of resource-efficient adaptation strategies.

---

## Key Features

- DeepLabV3+ with ResNet-50 backbone for semantic terrain segmentation  
- Training on Cityscapes (source domain)  
- Cross-domain evaluation on RUGD (target off-road domain)  
- Lightweight domain adaptation via partial fine-tuning  
- Multimodal input extension using RGB + edge maps  
- Quantitative evaluation of cross-domain robustness  

---

## Model Architecture

- Backbone: ResNet-50 (ImageNet pretrained)
- Segmentation Head: DeepLabV3+
- Input Modalities:
  - RGB (baseline)
  - RGB + Edge Maps (multimodal variant)

---

## Datasets

**Cityscapes**  
Urban street-scene dataset used as the source domain for supervised training.

**RUGD (Robot Unstructured Ground Driving Dataset)**  
Off-road terrain dataset used for cross-domain evaluation and adaptation.

---

## Project Structure

├── data/ # Dataset loaders and preprocessing
├── models/ # Model architecture definitions
├── train/ # Training and adaptation scripts
├── evaluation/ # Testing and metric computation
├── utils/ # Helper functions
├── configs/ # Experiment configuration files
├── results/ # Saved checkpoints and logs
└── README.md

---


---

## Results Summary

| Method                          | Domain Adaptation | Multimodal Input | Cross-Domain Behavior |
|---------------------------------|------------------|------------------|-----------------------|
| Baseline (RGB)                  | No               | No               | Significant drop      |
| Adapted (RGB)                  | Yes              | No               | Notable improvement   |
| Adapted (RGB + Edge)           | Yes              | Yes              | Localized gains       |

### Key Observations

- Domain shift severely impacts urban-trained models in off-road environments.
- Lightweight fine-tuning effectively recovers lost performance.
- Multimodal inputs yield inconsistent improvements across terrain types.
- Adaptation provides higher benefit-to-cost ratio than multimodal extension.

---

Contact

For questions or collaboration, please contact:

Aarushi Kothari
BITS Pilani Dubai Campus
Email: f20230342@dubai.bits-pilani.ac.in

