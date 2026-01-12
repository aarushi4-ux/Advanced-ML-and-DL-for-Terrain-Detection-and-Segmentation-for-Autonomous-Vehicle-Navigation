# Advanced-ML-DL-for-Terrain-Detection-and-Segmentation-for-Autonomous-Vehicle-Navigation

## Overview

Deep learning-based terrain segmentation models achieve strong performance on structured urban datasets but suffer significant degradation when deployed in unstructured off-road environments due to domain shift and dataset bias. This project investigates lightweight domain adaptation and simple multimodal extensions to improve cross-domain generalization for terrain segmentation, targeting robustness in real-world autonomous navigation.

This work is conducted under the supervision of a faculty professor, Dr.Raja Muthulagu as part of an academic design project.

---

## Abstract

A DeepLabV3+ model with a ResNet-50 backbone pretrained on ImageNet is trained on the Cityscapes dataset and evaluated on the off-road RUGD dataset, revealing substantial cross-domain performance drop. Lightweight domain adaptation is performed by partially fine-tuning the model on a limited subset of target-domain images, resulting in notable improvements. Additionally, a multimodal extension incorporating edge-map inputs is explored to assess potential gains in cross-domain robustness. Experimental results demonstrate that lightweight adaptation significantly mitigates domain shift effects, while multimodal inputs yield localized and inconsistent improvements. The study highlights practical trade-offs in resource-efficient adaptation strategies for autonomous navigation systems.

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

