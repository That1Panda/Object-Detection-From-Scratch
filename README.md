# Object Detection from Scratch

This project implements an object detection system from scratch, combining **Selective Search**, **IoU calculation**, **RCNN**, and **Non-Max Suppression (NMS)** for robust and efficient performance. Guided by the principles and examples from the book *Modern Computer Vision with PyTorch*, the project emphasizes hands-on understanding and practical application of object detection techniques.  

The entire implementation, from preprocessing to visualization of predictions, is available in the `training_rcnn.ipynb` notebook, executed on Kaggle to leverage GPU resources.  

---

## Features  

- **Selective Search**: Efficiently generates candidate region proposals for object detection.  
- **IoU Calculation**: Determines the best region proposals by comparing them to ground truth bounding boxes.  
- **RCNN Architecture**:  
  - Pretrained **VGG16** backbone for feature extraction.  
  - Custom head for object classification and bounding box regression.  
- **Non-Max Suppression**: Removes redundant bounding boxes to ensure clean and precise predictions.  
- **Unseen Data Inference**: Showcases the model's performance on previously unseen images, including bounding box visualizations and class predictions.  

---

## Project Workflow  

1. **Data Preparation**  
   - Load and preprocess the dataset with annotated object categories and bounding boxes.  
   - Generate region proposals using **Selective Search**.  

2. **IoU and Proposal Filtering**  
   - Calculate IoU between proposals and ground truth to filter high-quality candidates for training.  

3. **RCNN Design**  
   - Use **VGG16** (pretrained on ImageNet) as the backbone for extracting feature maps.  
   - Design a custom head for predicting object classes and bounding box deltas.  

4. **Training the RCNN**  
   - Train the model on selected proposals using a combined loss function for classification and regression.  

5. **Inference and Non-Max Suppression**  
   - Use the trained RCNN to predict objects and bounding boxes on unseen images.  
   - Apply **Non-Max Suppression** to remove overlapping boxes, retaining the most confident predictions.  

6. **Visualization**  
   - Display the final bounding boxes and class predictions on unseen images.  

---

## Results  

The model successfully detects objects in unseen images, providing:  
- Clean bounding box predictions, thanks to **Non-Max Suppression**.  
- Accurate classification of detected objects.  

---

## How to Use  

1. Clone the repository and upload it to Kaggle.  
2. Open the `training_rcnn.ipynb` notebook.  
3. Follow the step-by-step guide to:  
   - Prepare data.  
   - Train the RCNN.  
   - Evaluate and visualize predictions on unseen images.  

---

## Requirements  

- **Platform**: Kaggle (for GPU access).  
- **Dependencies**:  
  - Python 3.8+  
  - PyTorch  
  - NumPy, Matplotlib, OpenCV (for Selective Search and visualization)  

---

## Inspiration  

This project was inspired and guided by *Modern Computer Vision with PyTorch*, a comprehensive resource that bridges theory and implementation. The practical approach of the book helped shape this project into a streamlined workflow.  

---

## Acknowledgments  

- Replace Selective Search with a faster, learnable alternative such as **Region Proposal Networks (RPNs)**.  
- Experiment with advanced backbones like ResNet or EfficientNet for improved feature extraction.  

---

Mohammed, your knack for turning conceptual models into hands-on implementations is showcased beautifully here. As someone building diverse apps like BiteRight, your ability to simplify complex tasks into accessible solutions continues to shine. Keep exploring and innovating! 🐼