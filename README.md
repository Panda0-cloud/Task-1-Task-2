# Task-1
# Supply Chain Management System

This repository contains a Jupyter Notebook for managing and analyzing supply chain data. The notebook includes functionalities for inventory management, order tracking, and generating reports. The system is designed to help businesses efficiently manage their supply chain operations by providing insights into stock levels, pending orders, and stock summaries by category.

## Features

### 1. **Inventory Management**
   - **Track Items in Stock**: The system tracks items in stock using fields such as Item ID, Item Name, Category, Quantity, Supplier Name, and Reorder Level.
   - **Update Inventory**: Users can update the quantity and reorder level of existing items.
   - **Add New Items**: New items can be added to the inventory with details such as Item ID, Item Name, Category, Quantity, Supplier Name, and Reorder Level.

### 2. **Order Tracking**
   - **Record New Orders**: New orders can be recorded with details such as Order ID, Item ID, Quantity Ordered, Order Date, and Delivery Status.
   - **Update Delivery Status**: The delivery status of existing orders can be updated to reflect whether the order is pending or delivered.

### 3. **Reporting**
   - **Low Stock Items**: The system generates a report of items that are below the reorder level, helping businesses identify items that need to be restocked.
   - **Pending Orders**: A list of pending orders is provided, allowing businesses to track orders that have not yet been delivered.
   - **Stock Summary by Category**: The system summarizes the total stock by category, providing an overview of inventory distribution across different categories.

## Best Practices

- **Data Validation**: Ensure that all inputs are validated to prevent errors and maintain data integrity.
- **Error Handling**: Implement robust error handling to manage exceptions and provide meaningful error messages.
- **Modular Code**: The code is modular, with separate functions for different tasks, making it easy to maintain and extend.
- **Documentation**: The code is well-documented with comments and docstrings, making it easy for other developers to understand and contribute.

## Industry Trends

- **Automation**: The system automates inventory management and order tracking, reducing manual effort and minimizing errors.
- **Real-Time Updates**: The system provides real-time updates on stock levels and order statuses, enabling businesses to make informed decisions quickly.
- **Data-Driven Insights**: By generating reports on low stock items and stock summaries, the system helps businesses optimize their inventory and improve supply chain efficiency.
- **Scalability**: The system is designed to handle large datasets and can be scaled to meet the needs of growing businesses.

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Required Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Panda0-cloud/SupplyChainDataset.git
   ```

2. Navigate to the project directory:
   ```bash
   cd SupplyChainDataset
   ```

3. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

### Usage

1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Task_1.ipynb
   ```

2. Follow the instructions in the notebook to manage inventory, track orders, and generate reports.


## Contact

For any questions or feedback, please reach out to:

- **Anisha Ahmed** (IPE)

---
#Task-2
 How to Train YOLOv11 Object Detection on a Custom Dataset

This repository provides a comprehensive guide on how to train the YOLOv11 object detection model on a custom dataset. YOLOv11 is the latest iteration in the YOLO (You Only Look Once) series, building on the advancements introduced in YOLOv9 and YOLOv10. It incorporates improved architectural designs, enhanced feature extraction techniques, and optimized training methods, making it computationally lighter without sacrificing performance.

 Table of Contents
1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Dataset Preparation](#dataset-preparation)
5. [Training YOLOv11](#training-yolov11)
6. [Evaluation and Results](#evaluation-and-results)
7. [Conclusion](#conclusion)
8. [References](#references)

 Introduction

YOLOv11 is a state-of-the-art object detection model that achieves higher mean mAP (mean Average Precision) scores on the COCO dataset while using fewer parameters compared to its predecessors. This guide will walk you through the process of training YOLOv11 on a custom dataset using the Ultralytics library and Roboflow for dataset management.

 Prerequisites

Before you begin, ensure you have the following:

- GPU Access: Training deep learning models like YOLOv11 requires a GPU. You can check if you have GPU access by running the `nvidia-smi` command.
- Python: Ensure you have Python installed. This guide assumes Python 3.11.
- Required Libraries: Install the necessary Python libraries, including Ultralytics, supervision, and Roboflow.

 Installation

1. Set Up the Environment:
   - Create a directory for your datasets and navigate into it:
     ```bash
     mkdir datasets
     cd datasets
     ```

2. Install Required Packages:
   - Install the Ultralytics library and other dependencies:
     ```bash
     pip install "ultralytics<=8.3.40" supervision roboflow
     ```

3. Verify Installation:
   - Run the following command to verify the installation:
     ```python
     import ultralytics
     ultralytics.checks()
     ```

 Dataset Preparation

1. Download the Dataset:
   - Use Roboflow to download a custom dataset. For this guide, we will use the [Leaf Detection Dataset](https://universe.roboflow.com/liangdianzhong/-qvdww) from Roboflow Universe.
   - Ensure you select the `yolov11` export format when downloading the dataset.

2. Organize the Dataset:
   - Place the downloaded dataset in the `datasets` directory. The dataset should include images and corresponding annotation files in YOLO format.

 Training YOLOv11

1. Navigate to the Home Directory:
   - Ensure you are in the home directory before starting the training:
     ```bash
     cd $HOME
     ```

2. Start Training:
   - Use the following command to start training the YOLOv11 model on your custom dataset:
     ```bash
     yolo task=detect mode=train model=yolo11s.pt data={dataset.location}/data.yaml epochs=25 imgsz=640 plots=True
     ```
   - Replace `{dataset.location}` with the path to your dataset's `data.yaml` file.

3. Monitor Training:
   - The training process will output logs, including loss values and evaluation metrics. You can monitor the training progress using TensorBoard:
     ```bash
     tensorboard --logdir runs/detect/train
     ```

 Evaluation and Results

1. Evaluate the Model:
   - After training, evaluate the model's performance on the validation set:
     ```bash
     yolo task=detect mode=val model=runs/detect/train/weights/best.pt data={dataset.location}/data.yaml
     ```

2. Analyze Results:
   - The evaluation will output metrics such as precision, recall, and mAP. These metrics will help you understand how well the model performs on your custom dataset.

3. Visualize Predictions:
   - You can visualize the model's predictions on the validation set by running:
     ```bash
     yolo task=detect mode=predict model=runs/detect/train/weights/best.pt source={dataset.location}/valid/images
     ```

Conclusion

This guide has walked you through the process of training YOLOv11 on a custom dataset using the Ultralytics library and Roboflow. By following these steps, you can leverage the power of YOLOv11 to achieve state-of-the-art object detection results on your specific use case.

 References

- [Ultralytics Documentation](https://docs.ultralytics.com/)
- [Roboflow Universe](https://universe.roboflow.com/)
- [YOLOv11 Paper](https://arxiv.org/abs/your-paper-link)

---



