# Retina Image segmentation using cascaded U-Net
## This project aims to improve the prediction accuracy of traditional models for retinal image mask segmentation for treating diabetic problems using a cascaded U-Net.

* First the original retina iamges and it's masks are augmented to have better training dataset.
* Secondly, we build a standard U-Net architechture
* Next, we build another U-Net architechture which consists of three decoders instead of one.
   * one decoder for binary image segmentation of veins
* * one decoder for binary image segmentation of arteries
* * one decoder for reconstruction of the retina scan
