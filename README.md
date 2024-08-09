# Analysis-incorrect-prediction-using-yolo-object-detection
COCO Object Detection Evaluation
This project implements a tool for evaluating object detection models on the COCO dataset. It visualizes ground truth and predictions, identifies false positives and false negatives, and saves the results for further analysis.
Features

Loads and processes COCO dataset annotations
Performs object detection using YOLOv5
Compares predictions with ground truth
Visualizes results with bounding boxes
Identifies and saves false positive and false negative detections
Organizes results by object class

Prerequisites

Python 3.6+
PyTorch
OpenCV
pycocotools
Matplotlib
Pandas
YOLOv5

Installation

Clone the repository:
Copygit clone https://github.com/ultralytics/yolov5.git
cd yolov5

Install the required packages:
Copypip install -r requirements.txt

Download the COCO dataset (validation set) and annotations.

Usage

Set the paths to your COCO images and annotations in the script:
pythonCopycoco_images_path = '/path/to/coco/images'
coco_annotations_path = '/path/to/coco/annotations.json'

Run the main script:
Copypython main.py

The script will process the images, compare detections with ground truth, and save false positive and false negative examples in the classes directory.

Configuration

Adjust the confidence_threshold and iou_threshold variables to modify the detection criteria.
Modify the selected_classes list to focus on specific object categories.

Output
The script generates a directory structure organized by class, with subdirectories for false positives ('fp') and false negatives ('fn'). Each subdirectory contains images showing the ground truth and predictions side by side.
Contributing
Contributions to improve the project are welcome. Please follow these steps:

Fork the repository
Create a new branch (git checkout -b feature/improvement)
Make your changes and commit them (git commit -am 'Add new feature')
Push to the branch (git push origin feature/improvement)
Create a new Pull Request

License
This project is licensed under the MIT License - see the LICENSE file for details.
Acknowledgments

COCO dataset: https://cocodataset.org/
YOLOv5: https://github.com/ultralytics/yolov5
