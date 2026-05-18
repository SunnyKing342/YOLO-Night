# YOLO-Night: Lighting the Path for Autonomous Vehicles with Robust Nighttime Perception

This repository contains the official implementation of **YOLO-Night**, a nighttime-oriented object detection framework designed to improve autonomous vehicle perception in low-light conditions.

<img width="499" height="405" alt="image" src="https://github.com/user-attachments/assets/1c392854-53de-400c-8f21-9f863e1cafae" />

---

## 📌 Overview
YOLO-Night addresses the performance degradation of standard YOLO-based detectors under nighttime and low-light scenarios. It enhances the YOLO11 architecture with targeted architectural adaptations, including contrast enhancement, adaptive receptive field modeling, and multi-scale feature fusion, to improve robustness while maintaining real-time inference.

The framework consistently outperforms YOLO11n on the NightCity dataset, achieving significant improvements in precision, recall, and mAP@50 under nighttime conditions.

---

## ✨ Key Features
✅ Nighttime-oriented YOLO framework built on YOLO11  
✅ Contrast enhancement for low-light driving scenes  
✅ Adaptive receptive fields for blurred/small objects  
✅ Multi-scale convolutional blocks for degraded illumination  
✅ Staged feature fusion to mitigate semantic misalignment  
✅ Auxiliary low-level detection head for better small-object detection  
✅ +14.3% precision, +12.4% recall, +10.4% mAP@50 over YOLO11n (NightCity dataset)  
✅ Maintains real-time inference with moderate computational overhead  

---

## 📊 Results Highlights
Compared to the YOLO11n baseline on NightCity nighttime conditions:
- **Precision**: +14.3%
- **Recall**: +12.4%
- **mAP@50**: +10.4%
- **Speed**: Real-time inference (~30 FPS on RTX 3090)

---

## 🚀 Getting Started

### Requirements
```bash
pip install -r requirements.txt
```

### Dataset
This work uses the **NightCity dataset** for nighttime driving scene object detection. Prepare your dataset following the YOLO format structure described in the paper.

### Training
```bash
python train.py --config config/yolo_night.yaml --data ./data/nightcity.yaml
```

### Inference
```bash
python detect.py --weights weights/yolo_night_best.pt --source ./test_images/
```

---

## 📄 Citation
If you use this work in your research, please cite the original paper:

```bibtex
@article{tian2026yolo,
  title={YOLO-Night: Lighting the Path for Autonomous Vehicles with Robust Nighttime Perception},
  author={Tian, Jinxin and Ghaffar, Muhammad Arslan and Li, Zhaokai},
  journal={Sensors},
  volume={26},
  number={4},
  pages={1138},
  year={2026},
  publisher={MDPI}
}
```

---

## 📝 License
This project is released under the **CC BY 4.0 License**, consistent with the open-access policy of *Sensors* (MDPI).

## Contact
For questions or issues, please contact:
```
Muhammad Arslan Ghaffar – ghaffar@siat.ac.cn
```
