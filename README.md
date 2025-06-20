🦴 Bone Fracture Detection in X-Ray Images using YOLOv8
This project applies deep learning–based object detection to localize bone fractures in X-ray images using the PKDarabi Bone Fracture Detection dataset.

We implemented an end-to-end YOLOv8 training pipeline using annotated medical images, including preprocessing, data augmentation, model training, and prediction visualization.

🔍 Objective
Develop a model that can automatically detect and localize fractures in medical X-rays to support faster and more accurate diagnosis in clinical workflows.

📂 Dataset
Source: Kaggle - Bone Fracture Detection

Format: Images + YOLO-format bounding box labels

Classes: 1 (Fracture)

🧠 Model Architecture
YOLOv8s (Ultralytics) pretrained on COCO

Enhanced with contrast-limited adaptive histogram equalization (CLAHE)

Augmented with:

Mosaic

MixUp

HSV shifts

Random flips and rotations

⚙️ Training Configuration
Parameter	Value
Epochs	50
Image Size	640×640
Batch Size	16
Augmentations	Enabled
Preprocessing	CLAHE
Model	YOLOv8s

📈 Results
Metric	Value
Precision	35.4%
Recall	32.4%
mAP@0.5	28.4%
mAP@0.5:0.95	9.1%

Despite several preprocessing and modeling enhancements, results indicate that improvements may require more data or stronger architectures for better fracture localization.

📸 Sample Predictions
<img src="runs/detect/predict/image0.jpg" width="250" /> <img src="runs/detect/predict/image1.jpg" width="250" /> <img src="runs/detect/predict/image2.jpg" width="250" />
📝 Key Learnings
CLAHE preprocessing can enhance bone feature visibility

YOLOv8 supports fast experimentation and strong performance even on limited datasets

Fracture detection in X-rays is a complex task and benefits from high-quality annotations and richer datasets

🔮 Future Work
Try larger models (YOLOv8m, YOLOv8l)

Train longer or at higher resolutions

Explore transformer-based detectors (e.g., DETR, DINOv2)

Incorporate additional fracture classes and metadata
