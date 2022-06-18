## Object Detection on Images/Videos/Webcam using Tensorflow-YoloV4

### Problem Definition

Due to object detection’s close relationship with video analysis and image understanding, it has attracted much research attention in recent years. Traditional object detection methods are built on handcrafted features and shallow trainable architectures. Their performance easily stagnates by constructing complex ensembles which combine multiple low-level image features with high-level context from object detectors and scene classifiers. With the rapid development in deep learning, more powerful tools, which are able to learn semantic, high-level, deeper features, are introduced to address the problems existing in traditional architectures. These models behave differently in network architecture, training strategy and optimization function, etc.

### Data Preparation
- To implement YOLOv4 using TensorFlow, first we convert the .weights into the corresponding TensorFlow model files and then run the model.

- Taking about dataset, YOLOv4 has been trained already on the Microsoft’s COCO dataset which has 80 classes that it can predict. We will grab these pretrained weights so that we can run YOLOv4 on these pretrained classes and get detections. We can also use a custom dataset to train YOLO algorithm such as KITTI image dataset etc .

- YOLOv4 compares to other object detection systems on Microsoft’s COCO object Detection Dataset.
![image](https://user-images.githubusercontent.com/53213766/174433906-d85e4828-173f-403b-80df-3c0bc62fb908.png)
![image](https://user-images.githubusercontent.com/53213766/174433921-a7a10beb-72fb-4317-8663-95dbb970471f.png)

### Algorithm

The majority of CNN-based object detectors are largely applicable only for recommendation systems. For example, searching for free parking spaces via urban video cameras is executed by slow accurate models, whereas car collision warning is related to fast inaccurate models. Improving the real-time object detector accuracy enables using them not only for hint generating recommendation systems, but also for stand-alone process management and human input reduction. Real-time object detector operation on conventional Graphics Processing Units (GPU) allows their mass usage at an affordable price. The most accurate modern neural networks do not operate in real time and require large number of GPUs for training with a large mini-batch-size. We address such problems through creating a CNN that operates in real-time on a conventional GPU, and for which training requires only one conventional GPU. 

YOLO, a new approach to object detection. Prior work on object detection repurposes classifiers to perform detection. Instead, we frame object detection as a regression problem to spatially separated bounding boxes and associated class probabilities. A single neural network predicts bounding boxes and class probabilities directly from full images in one evaluation. Since the whole detection pipeline is a single network, it can be optimized end-to-end directly on detection performance. Our unified architecture is extremely fast. Our base YOLO model processes images in real-time at 45 frames per second. A smaller version of the network, Fast YOLO, processes an astounding 155 frames per second while still achieving double the mAP of other real-time detectors. Compared to state-of-the-art detection systems, YOLO makes more localization errors but is less likely to predict false positives on background. Finally, YOLO learns very general representations of objects. It outperforms other detection methods, including DPM and R-CNN, when generalizing from natural images to other domains like artwork.

### Experimental result obtained
#### YOLO-V4 on Images 
![image](https://user-images.githubusercontent.com/53213766/174433963-2ebbb5c7-b4d6-4ef2-a1da-940c05ffbf9b.png)
![image](https://user-images.githubusercontent.com/53213766/174433965-3c38b7ad-1391-4e25-b167-0bab3e9b2044.png)
![image](https://user-images.githubusercontent.com/53213766/174433967-9bfe3157-8f4a-4c95-aa26-32c87c9bc36a.png)
#### YOLO-V4 on Videos
![download-Trim (1)](https://user-images.githubusercontent.com/53213766/174434449-64671d3e-144c-42b2-8d31-2f48baf7d823.gif)
![download-1-Trim](https://user-images.githubusercontent.com/53213766/174434683-19e6c5e7-642e-4767-a4d3-b699a640537b.gif)
![download-2](https://user-images.githubusercontent.com/53213766/174434647-c7e27ad2-ea70-41d8-b089-bfc093ead536.gif)

#### YOLO-V4 on Webcam 
![image](https://user-images.githubusercontent.com/53213766/174433984-37c6c778-f635-4e48-af1b-2d2ea75605dd.png)

##### Thank you :)
#### Sai Ganesh N
