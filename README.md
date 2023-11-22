# RetinaNet: Retina Image segmentation using cascaded U-Net
## This project aims to improve the prediction accuracy of traditional models for retinal image mask segmentation for treating diabetic problems using a cascaded U-Net.
"RetinaNet" is an innovative medical image segmentation project designed specifically for diabetic retinopathy identification. This project introduces a novel architecture employing a cascaded approach with two U-Net models, integrating three decoders within the second U-Net. Through meticulous training on diverse retina image datasets like Ravir and IDRid, the model achieves a remarkable accuracy of 97% in precisely extracting veins and blood vessels from previously unseen retina scans. This groundbreaking accuracy surpasses existing state-of-the-art models, promising significant advancements in diagnosing diseases like diabetic retinopathy, thereby potentially revolutionizing medical imaging analysis for improved healthcare outcomes.

* First the original retina iamges and it's masks are augmented to have better training dataset.
* Secondly, we build a standard U-Net architechture
* Next, we build another U-Net architechture which consists of three decoders instead of one.
   * one decoder for binary image segmentation of veins
   * one decoder for binary image segmentation of arteries
   * one decoder for reconstruction of the retina scan
* We cascade these two U-Net models in the training loop
* Loss funtions that were used: Binary Cross Entropy Loss, Dice Loss, IOU Loss 

### Predicted veins on an unseen retina image:
![predicted_bv_0](https://github.com/foyie/Retina-Image-segmentation-using-cascaded-U-Net/assets/89987028/afb441a4-9c79-43e9-9959-ece8439f8810)

### Predicted artery on an unseen retina image:
![predicted_v_0](https://github.com/foyie/Retina-Image-segmentation-using-cascaded-U-Net/assets/89987028/9630484b-9c56-4a28-88d2-4ab1f0f43657)
