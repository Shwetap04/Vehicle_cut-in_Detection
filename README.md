## Vehicle Cut-In Detection and Direction Prediction

A robust multitask deep learning framework that detects vehicle cut-in events and simultaneously predicts movement direction (Left, Straight, Right) using real-world road scenes from the IDD Temporal Dataset. Built with YOLOv5, LSTM, Attention Mechanisms, and a custom focal loss for handling imbalanced events, this project aims to enhance autonomous driving safety through real-time alerts and temporal modeling.

---

## Problem Statement

In unstructured and dynamic driving environments, detecting when a vehicle is likely to cut into the ego-lane and forecasting its future trajectory is crucial for collision avoidance. Traditional single-task models often fall short in such scenarios. This project proposes a multitask learning framework that:

- Detects cut-in events  
- Predicts vehicle movement direction (Left, Straight, Right)  
- Generates real-time warnings

---

## Key Features

- YOLOv5 for real-time vehicle detection  
- LSTM with Attention for temporal feature learning  
- Focal Loss to handle class imbalance  
- Multitask Model with shared layers for joint learning  
- Real-time Warning System (visual/audio/haptic signals)  
- Attention Visualization for explainability  

---

## Technologies Used

| Area             | Tools / Frameworks                                                                 |
|------------------|------------------------------------------------------------------------------------|
| Object Detection | YOLOv5 (PyTorch)                                                                   |
| Deep Learning    | TensorFlow, Keras (LSTM, Attention, Focal Loss)                                    |
| Data Processing  | NumPy, OpenCV, PIL, scikit-learn                                                   |
| Visualization    | Matplotlib, tqdm                                                                   |
| Real-time System | WarningSystem logic embedded in the notebook                                       |
| Platform         | Google Colab + Google Drive integration                                            |

---

## Project Structure

```

vehicle-cutin-detection/
├── Vehicle_cut-in_detection.ipynb
├── Intel_Unnati___Idea_Submission_PPT final.pptx
├── README.md
└── Dataset (download from IDD Temporal site)

````

---

## Dataset

- Name: [IDD-Temporal Dataset](http://idd.insaan.iiit.ac.in/)
- Description: Temporally continuous road scenes from Indian traffic scenarios, ideal for understanding lane behavior and cut-in events.
- Note: Dataset is not included in this repo. Download it manually from the official site.

### Citation

```bibtex
@inproceedings{IDDTemporal2020,
  title={IDD-Temporal: A Dataset for Benchmarking Temporal Driving Scene Understanding},
  author={Chitturi, N. Sai Vamsi et al.},
  booktitle={WACV},
  year={2021}
}
````

---

## How to Run

1. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

2. Mount Google Drive (Colab only)

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

3. Open and run each cell in `Vehicle_cut-in_detection.ipynb` sequentially

4. Model training and evaluation will begin automatically

---

## Results and Evaluation

* Cut-In Detection Output

  ```
  Warning: Cut-in detected with probability 0.50 from the right (Level: MEDIUM)
  Warning: Cut-in detected with probability 0.88 from the right (Level: HIGH)
  Warning: Cut-in detected with probability 0.99 from the right (Level: HIGH)
  Warning: Cut-in detected with probability 1.00 from the right (Level: HIGH)
  ```

* Inference Speed:

  ```
  Processing time: ~0.09 to 0.18 seconds per sample
  ```

* Multitask Evaluation:

  ```
  Model training and evaluation completed.
  ```

* Note: Final evaluation metrics such as accuracy for cut-in and direction prediction were computed but not printed explicitly in the current notebook version.
  
---

## Team Contribution

* Group Internship project for Intel Unnati Industrial Training
---

