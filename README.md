# Analysis-incorrect-prediction-using-yolo-object-detection

This project implements a tool for evaluating object detection models on the COCO dataset. It visualizes ground truth and predictions, identifies false positives and false negatives, and saves the results for further analysis.

## Features

- Loads and processes COCO dataset annotations
- Performs object detection using YOLOv5
- Compares predictions with ground truth
- Visualizes results with bounding boxes
- Identifies and saves false positive and false negative detections
- Organizes results by object class

## Prerequisites

- Python 3.6+
- PyTorch
- OpenCV
- pycocotools
- Matplotlib
- Pandas
- YOLOv5

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/ultralytics/yolov5.git
   cd yolov5
   ```

2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

3. Download the COCO dataset (validation set) and annotations.

## Usage

1. Set the paths to your COCO images and annotations in the script:
   ```python
   coco_images_path = '/path/to/coco/images'
   coco_annotations_path = '/path/to/coco/annotations.json'
   ```

2. Run the main script:
   ```
   python main.py
   ```

3. The script will process the images, compare detections with ground truth, and save false positive and false negative examples in the `classes` directory.

## Configuration

- Adjust the `confidence_threshold` and `iou_threshold` variables to modify the detection criteria.
- Modify the `selected_classes` list to focus on specific object categories.

## Output

The script generates a directory structure organized by class, with subdirectories for false positives ('fp') and false negatives ('fn'). Each subdirectory contains images showing the ground truth and predictions side by side.

## Contributing

Contributions to improve the project are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes and commit them (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- COCO dataset: https://cocodataset.org/
- YOLOv5: https://github.com/ultralytics/yolov5
