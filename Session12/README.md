# Object Localisation - YOLO

Till now we had concentrated on object classification. This session was about Object Localisation.

Object Localisation is a very hard task to do because we should not only predict the object but also we need to detect the exact position of it.

### **Detection Approaches**
**Simplify Object Detection problem by:**

1. ignoring lower prediction values
2. predicting bounding boxes instead of the exact object mask mixing different receptive field layers but this is easier said than done.
 
**There are two main approaches to driving detection algorithms, namely:**

YOLO-like approach, where k-means extracted anchor boxes are used, and
SSD-like approach, where a fixed number of predefined bounding boxes are used.

# *Assignment*

## **Assignment A - Tiny ImageNet**

Should train ResNet18  on **Tiny ImageNetData Set** and reach test accuracy of 50%

### **Implementation**

1. Wrote a Code to download, mix train and test , split and convert to the dataset format.
2. Used One Cycle Policy as Scheduler. It yielded better and fast results than others
3. Reached the target accuracy

### **Parameters**

1. Agumentations - Horizontal flip, Padding , Random Crop, Normalisation, Cutout
2. Batch Size - 256
3. Model - Resnet 18 with 200 classes
4. Optimiser - SGD(momentum - 0.9 , weight_decay - 0.0001)
5. Scheduler - One Cycle (  max_lr = 0.02, epochs=30,  pct_start=1/3, anneal_strategy='linear', cycle_momentum=True, base_momentum=0.85, max_momentum=0.95, div_factor=10.0,final_div_factor =10)

### **Results**

1. Best train Accuracy - 74%
2. Best test Accuracy - 57.69%
4. Accuracy Change Graph
5. GradCam on MisClassified Images (All 4 layers)

## **Assignment B - Find out the best total numbers of clusters**
   
 To download 50 dog images, annotate with vgg annotator, find out the best no of clusters
 
 **Visualisation of data**
 
 **Elbow method to find out K**
 
 **Mean Iou Method to find out k**
 
 ** K means with k = 3**
 
 **K Means with k =4**

