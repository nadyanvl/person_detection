# Person Detection

This repository demonstrates person detection using two popular object detection models: YOLO (You Only Look Once) and Faster R-CNN (Region-based Convolutional Neural Network). The models have been trained and evaluated on the widely-used COCO (Common Objects in Context) dataset.

Note: Only results from YOLOv8n and YOLOv8m are displayed here.

## Dataset
This project utilizes a subset of the [COCO-2017](https://docs.voxel51.com/user_guide/dataset_zoo/datasets.html#dataset-zoo-coco-2017) dataset provided by FiftyOne. The dataset has been downsampled to include a total of 5000 instances, distributed as follows:
- 4000 for training
- 500 for validation
- 500 for testing

For detailed information about the original dataset, you can refer to the [COCO-2017 documentation](https://cocodataset.org/#home).

In this project, we focus exclusively on the `person` class in object detection.

## Object Detection Models
1. YOLO is a single-stage object detection method. It rapidly examines the entire image in one go, predicting and locating objects efficiently. This makes it well-suited for real-time applications like self-driving cars and surveillance.

2. Faster R-CNN is a two-stage object detection method. It first proposes potential object regions using a region proposal network and then accurately classifies and refines these regions. While it may be a bit slower than YOLO, it excels in tasks demanding precise localization. 

## Training Results of YOLOv8n and YOLOv8m
[Notebook Folder](https://github.com/nadyanvl/person_detection/tree/main/Personal%20Notebook)

| No. | Model    | Epoch | Batch | Precision (%) | Recall (%) | mAP@50 (%) |
| --- | -------- | ----- | ----- | ------------- | ---------- | ---------- |
| 1   | YOLO V8n  | 50    | 16    | 74.2          | 59.5       | 68.3       |
| 2   | YOLO V8m  | 50    | 16    | 77.3          | 63.5       | 73.4       |

YOLOv8m shows higher values in all three metrics, indicating better performance in terms of accurately identifying and localizing persons in the images.

## Model Performance Comparison (Final Results (All))
[Notebook Folder](https://github.com/nadyanvl/person_detection/tree/main/All%20Team%20Member%20Notebook)

| Model                    | Precision | Recall | mAP (50) | mAP (50-95) | Inference Time (ms) |
| ------------------------ | ----------| ------ | -------- | ----------- | -------------------- |
| Faster R-CNN GoogLeNet   | 0.21      | 0.84   | 0.133    | 0.133       | 1652                 |
| Faster R-CNN MobileNet   | 0.97      | 0.42   | 0.442    | 0.225       | 512.4                |
| Faster R-CNN ResNet50    | 0.89      | 0.71   | 0.756    | 0.240       | 143.43               |
| YOLO v3                  | 0.782     | 0.617  | 0.714    | 0.472       | 1.5                  |
| YOLO v5                  | 0.76      | 0.534  | 0.67     | 0.391       | 1.7                  |
| YOLO v8                  | 0.8       | 0.621  | 0.732    | 0.485       | 1.3                  |

Among the models evaluated, Faster R-CNN with ResNet50 FPN demonstrates high evaluation results, showcasing commendable precision, recall, and mAP scores. Despite a slightly longer inference time compared to YOLOv8, it remains a strong contender, offering a balance between speed and performance.

However, for scenarios requiring real-time detection, YOLOv8 emerges as the overall best performer, showcasing impressive precision, recall, and mAP scores, coupled with efficient inference times. Its well-rounded performance positions YOLOv8 as the top choice, particularly in applications where swift and accurate object detection in real-time is paramount.

## Team Member
Fathurrahman Hernanda Khasan, Fitrah Ramadhan Reza, Harrison, Hendra Ronaldi, Hilmy Rahmadani, I Putu Ananta Yogiswara, Nadya Novalina, Satriaji Najha Darmawan, Tri Wahyu Prabowo, Yurixa Sakhinatul Putri


