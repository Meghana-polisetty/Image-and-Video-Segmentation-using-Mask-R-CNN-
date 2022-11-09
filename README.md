# Image-and-Video-Segmentation-using-Mask-R-CNN-
Image and Video Segmentation using Mask R-CNN 

Performed Instance image segmentation using Mask Region-Based Convolutional Neural Network(Mask R-CNN) by generating bounding boxes, extracting segmented objects and detected target class.

![image](https://user-images.githubusercontent.com/90289879/200721918-e479efa9-6242-428a-84b8-65f0e95f6a09.png)

Object Detection
Object Detection refers to the method of identifying and correctly labeling all the objects present in the image frame.

This broadly consists of two steps :

Object Localization: Here, a bounding box or enclosing region is determined in the tightest possible manner in order to locate the exact position of the object in the image.

Image Classification: The localized object is then fed to a classifier which labels the object.

![image](https://user-images.githubusercontent.com/90289879/200721874-2d67fd6e-1143-4a89-9245-8243fceb899a.png)

Semantic Segmentation
It refers to the process of linking each pixel in the given image to a particular class label. For example in the following image the pixels are labelled as car, tree, pedestrian etc. These segments are then used to find the interactions / relations between various objects.

![image](https://user-images.githubusercontent.com/90289879/200721845-d57bbf28-6d73-4c81-a0e5-512801bed917.png)

Instance Segmentation
Here, we associate a class label to each pixel similar to semantic segmentation, except that it treats multiple objects of the same class as individual objects / separate entities.

![image](https://user-images.githubusercontent.com/90289879/200721821-59fcf2b2-5c2e-4d15-ba5d-176acece68a1.png)

Bounding Box
It is a tight rectangle used to enclose the object of interest. It is generally described by four values : (bx, by, bh, bw) . Where (bx, by) are the co-ordinates of the center of the box and bh, bw are the height and width of the box respectively measured on a scale of 0 to 1.

![image](https://user-images.githubusercontent.com/90289879/200721795-9974d9fc-d45b-42b9-b2d8-c8bf730205ad.png)

Anchor Boxes
These are a set of predefined bounding boxes of a certain height and width. These boxes are defined to capture the scale and aspect ratio of specific object classes you want to detect and are typically chosen based on object sizes in your training data-sets. During detection, the predefined anchor boxes are tiled across the image. The network predicts the probability and other attributes, such as background, intersection over union (IoU) and offsets for every tiled anchor box. The predictions are used to refine each individual anchor box. You can define several anchor boxes, each for a different object size.

![image](https://user-images.githubusercontent.com/90289879/200721771-5abb53bf-3ce8-4d2f-b2cd-b2da61286fdf.png)

Thus the network refines these anchor boxes to finally output the tight bounding boxes. These are defined by the scale and aspect ratio.

Aspect Ratio is the width / height of the box.

Size is the height and width of the box. eg (256 x 256)

Scale is the multiplying factor of the required box w.r.t to base box

Intersection over Union (IOU) :

It is an evaluation metric used to check the accuracy of the predicted bounding box w.r.t the actual ground truth.

![image](https://user-images.githubusercontent.com/90289879/200721745-81d06773-8eba-414e-9595-2c70575d005b.png)

An IOU of > 0.5 is considered as a good prediction and is used for further evaluation.

![image](https://user-images.githubusercontent.com/90289879/200721727-4d7b3226-9b16-4c6b-a08e-95b5cd561032.png)
