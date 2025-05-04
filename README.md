
🕵️‍♂️ Image and Document Forgery Detection & Localization
This project offers a unified deep learning-based solution for detecting and localizing forgeries in both digital images and scanned documents. It includes:

A user-friendly Flask-based UI for testing images/documents.

A CNN + ELA based model for image forgery localization.

A YOLOv8 model for scanned document forgery detection.

📁 Project Structure
Edit
├── app.py                                # Flask backend and HTML frontend
├── templates/
│   └── index.html                        # UI for file upload and results
├── static/                               # (Optional) Static assets like CSS
├── image forgery localization/
│   └── image_forgery_localization.ipynb  # ELA + CNN Jupyter Notebook
├── document forgery detection/
│   └── yolov8_document_detection_files   # YOLOv8 code and config
├── model_cnn_ela.h5                      # Trained CNN+ELA model (download link below)
├── yolov8_model.pt                       # Trained YOLOv8 model (download link below)
└── README.md
📌 Features
🔍 Image Forgery Localization
Built using a CNN architecture combined with Error Level Analysis (ELA) preprocessing.

Trained on the CASIA v2.0 dataset, which provides ground truth masks for pixel-wise forgery localization.

Achieved:

F1-score: 0.57 (overall)

F1-score: >80% for images with tampering >10%

Competitive with advanced models like ManTra-Net in terms of detection accuracy.

Significantly faster in inference time, making it ideal for real-time or low-compute environments.

📄 Scanned Document Forgery Localization
Utilizes YOLOv8 for bounding-box-based tampering detection.

Trained using a Roboflow dataset (with 8 augmentation techniques).

Achieved:

Precision: 0.92

Recall: 0.48

Works effectively on invoices, bills, and printed media.

Note: The dataset contains low-resolution images. Model performance is expected to improve with a higher-quality annotated dataset.

🔗 Model Files (Download Required)
Please download and place the following models in the project root folder:

🔗 CNN+ELA .h5 model
https://drive.google.com/file/d/17x9k8YKdSVZ3p6J3na21L1SEbnjHWzYp/view?pli=1

🔗 YOLOv8 .pt model
https://drive.google.com/file/d/1D5f56ik5p7zrE8b3fGeDBRLRPM2CyNZ9/view?usp=sharing 

🚀 Running the App

🧪 Dataset Details
Image Forgery:
Dataset: CASIA v2.0

Ground Truth: Pixel-level binary masks for tampered regions

Analysis: Showed that the model generalizes well to partial tampering and compressions

Document Forgery:
Dataset: Roboflow-based custom dataset with invoices and bills
Links : Train - https://drive.google.com/file/d/1FctN86K6PxbmzUtMJOuwXVFUrBEGmzUL/view?usp=sharing 
        Test - https://drive.google.com/file/d/1BfMFl93Bl7nZaNyA7KyLOniYkesIjVvW/view?usp=sharing

Note: Dataset included 8 augmentations, but many images were blurry or poorly annotated

Future Scope: Better image quality and balanced classes can boost performance

Watch the Video Demo in Youtube :- https://youtu.be/quLxV1YYVh8?si=f2DzJZh518oJKWAO

📰 Publication
📄 "REGION Wise iMAGE Forgery Localisation: A CNN Framework with Error Level Analysis",
Presented at the 3rd International Conference in Power Engineering and Intelligent Systems (PEIS 2025),
National Institute of Technology Uttarakhand, India, held on March 08–09, 2025.
