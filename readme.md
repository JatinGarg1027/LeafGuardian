<h1 align="center">LeafGuardian</h1>

<div align="center">

<h4>India is a cultivated country and about 70% of the population depends on agriculture. Disease on plant leads to the significant reduction in both the quality and quantity of agricultural products. The image processing techniques can be used for the plant disease detection. Disease detection involves the steps like image acquisition, image pre-processing, image segmentation, feature extraction and classification. Detection of plant disease using plant leaf is one of the effective ways for early disease detection.</h4>

</div>

-----------------------------------------
### Inspiration

* It is very difficult to monitor the plant diseases manually. It requires tremendous amount of work, expertise in the plant disease detection, and also require the excessive processing time.

* Identification of the plant diseases is the key to prevent the losses in the yield and quantity of the agricultural product. 

* Health monitoring and disease detection on plant is very critical for sustainable agriculture.

------------------------------------------
### Implementation

The step by step proposed approach consists of leaf image dataset collection, pre-processing, segmentation using K-means clustering method, feature extraction using GLCM method and finally the training of system using SVM model.

<p align="center">
 <img height=200px src=images\Model.png>
</p>

1. `Image Acquisition` - It is an action of retrieving an image 
from hardware, so that it can be passed for further processing.

<p align="center">
 <img height=200px src="images\Query_image.png">
</p>

2. `Image Pre-processing` - Pre-processing method involves various techniques such as changing image size and shape, enhancing image and morphological operations. We have used various MATLAB operations to resize image, to enhance contrast and for RGB to grayscale conversion for further operations like creating clusters in segmentation.

<p align="center">
 <img height=200px src="images\Contrast_enhancement.png">
</p>

3. `Image Segmentation` - We have used K-means clustering method for partitioning of images into clusters in which one of the clusters contain image with major area of diseased part. Image is converted from RGB color space 
to L*a*b* color space in which the L*a*b* space consists of a luminosity layer 'L*', chromaticity-layer 'a*' and 'b*'. All of the color information is in the 'a*' and 'b*' layers and colors are classified using K-Means clustering in 'a*b*' space.
<p align="center">
 <img height=200px src="images\Segmented.png">
</p>

4. `Feature Extraction` - In feature extraction desired feature vectors such as color, texture, morphology and structure are extracted. Statistical texture features are obtained by Gray level co-occurrence matrix (GLCM) for texture analysis.Different statistical texture features of GLCM are entropy, covariance, information measure of correlation and contrast.

<p align="center">
 <img height=200px src="images\Features.png">
</p>

5. `Training & Classification` -  We have used Multi SVM technique for classification and recognition of leaf disease. Support vector machine is based on maximizing the minimum distance from the separating hyper plane to the nearest cluster.

<p align="center">
 <img height=200px src="images\Detections.png">
</p>

Hence the image is acquired and passed through pre-processing, segmentation, feature extraction and then disease name is selected for given leaf based on image classification results by the Multi class SVM model.
