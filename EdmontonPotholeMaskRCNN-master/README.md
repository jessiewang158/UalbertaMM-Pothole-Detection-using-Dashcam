# Edmonton Pothole using MaskRCNN
This project follows the balloon example in https://github.com/matterport/Mask_RCNN.git. Please refer to matterport's instructions to set up Mask R-CNN requirements.
# Dataset
The dataset is collected in Edmonton, Canada during daytime. It is labelled using online VGG image Annotator from http://www.robots.ox.ac.uk/~vgg/software/via/. VGG version 1.0.6 is used.
The labeled dataset can be found at https://drive.google.com/drive/folders/1LPiEK3n9SL3kTafCeSFUYoLuead409ns?usp=sharing.
# Dataset Inspection
Before training, make sure the format of the labeled data agree with Mask R-CNN verified format. To verify the dataset, please use inspect_pothole_data.ipynb
# Training
The model is trained on pre-trained COCO weights which could be downloaded from https://github.com/matterport/Mask_RCNN/releases. <br />
All Mask R-CNN config is included in pothole.py. <br />
The model can be trained on custom dataset using: <br />
 &nbsp; &nbsp; &nbsp; !python pothole.py train --dataset="pothole dataset dir" --weights=coco <br />
Because Mask R-CNN has a lot of network layers and requires heavy computation, all training was completed on Google Colab which provides free access to tensorflow with GPU. <br />
Training and evalutions are included in inspect_pothole_model.ipynb
# Results
Mask R-CNN results can be found at 
https://youtu.be/0N7R2e5ewcE and https://www.youtube.com/watch?v=hc-XmV8-NCk
