
# YOLOv7 Experiments - RDCC Challenge

This repository contains the results of unique experiments conducted using YOLOv7 for the Road Damage Condition Classification (RDCC) Challenge. This repository includes detailed run folders for each experiment and insights into training YOLOv7 for damaged road identification.

---

**Repository Contents**

- /run_folders: Contains unique experiment results, including:
  - Configuration files
  - Training logs
  - Checkpoints
  - Metrics and visualizations (e.g., loss curves, mAP scores)

- Scripts:
  - Helper scripts used for preprocessing, training, and evaluation.

---

**Setup**

1. Clone YOLOv7

To replicate the experiments, you first need to clone the YOLOv7 repository:

git clone https://github.com/WongKinYiu/yolov7.git  
cd yolov7  

Follow the installation steps in the YOLOv7 repository to set up the required environment.

2. Download the RDCC Dataset

The dataset used in these experiments is the Road Damage Condition Classification (RDCC) Challenge dataset. Download the dataset from the official source:

- RDCC Dataset Link (replace with actual link)

Once downloaded, place the dataset in a folder named `datasets/rdcc` within the YOLOv7 directory structure.

3. Download Pretrained Weights (Optional)

If you wish to use pretrained YOLOv7 weights, download them from the YOLOv7 GitHub repository:

wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt  

Place the weights in the weights/ folder.

---

**Training YOLOv7**

To train YOLOv7 on the RDCC dataset, use the following command:

python train.py --img 640 --batch 16 --epochs 50 --data datasets/rdcc/data.yaml --cfg cfg/training/yolov7.yaml --weights weights/yolov7.pt --name yolov7_rdcc  

Training Parameters:  
- img: Image size.  
- batch: Batch size.  
- (E) epochs: Number of training epochs.  
- data: Path to the dataset YAML file.  
- cfg: Path to the YOLOv7 configuration file.  
- weights: Path to the YOLOv7 pretrained weights.  
- name: Experiment name.

---

**Results**

Each experiment's results are stored in /run_folders, which include:  
- Training logs (results.txt)  
- Best model weights (best.pt)  
- Metrics (Precision, Recall, mAP)  
- Visualizations of predictions and validation results.

---

**Experiment Highlights**

The experiments conducted in this repository involved exploring the impact of modifying key YOLOv7 parameters, including:  
- Rotation  
- Paste augmentation  

These modifications aimed to evaluate their effects on model performance for the RDCC dataset.

---

**Future Work**

- Experiment with different YOLOv7 configurations and hyperparameters.  
- Fine-tune models for improved accuracy.  
- Explore transfer learning and domain adaptation techniques.

---

**License**

This project is for educational and research purposes only. Ensure compliance with the licensing terms of YOLOv7 and the RDCC dataset when using this repository.

---

**Acknowledgments**

- YOLOv7 by WongKinYiu (https://github.com/WongKinYiu/yolov7)  
- RDCC Challenge Dataset 

---


Feel free to fork, star, and contribute to this repository!

