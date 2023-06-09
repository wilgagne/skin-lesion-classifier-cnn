# Skin-Lesion-Classifier-CNN

## Project Description
In this project, I aimed to adapt the renowned [Esteva et, al.'s paper](https://www.nature.com/articles/nature21056) (2017) skin lesion classifier CNN to perform effectively on a new, smaller dataset with significant class imbalances. Esteva et al.'s approach utilized Google Inception V3 and transfer learning, achieving impressive results and setting a benchmark for skin lesion classification.

I began by implementing the original Inception V3 model, following Esteva et al.'s guidelines. However, due to the severe class imbalance in my dataset, I developed a second model that addresses this issue more effectively. The new model incorporated an over-sampler and under-sampler, sklearn class weights, classical data augmentation techniques, a dropout layer, focal loss, and the Adam optimizer.

As a result, my second model significantly outperformed the original Esteva et al. model when applied to my dataset. This improvement can be attributed to several factors, including the new model's hyperparameters being tailored to a smaller dataset with severe class imbalances, the use of a loss function specifically designed to handle class imbalances, and the incorporation of an extra dropout layer and Adam's optimizer.

This project underscores the importance of considering dataset characteristics when adapting a CNN and demonstrates the potential for achieving better results by tailoring a renowned model's training procedure to suit specific dataset requirements.

## CNN General Architecture 

![CNN](https://github.com/wilgagne/Skin-Lesion-Classifier-CNN/blob/2ccfd821d3a848ff4a0557415ebb1442cd65054d/images/Architecture.png)

Taken from https://cloud.google.com/tpu/docs/inception-v3-advanced

## Dataset
### Skin Cancer MNIST: HAM10000
<img src="https://github.com/wilgagne/Skin-Lesion-Classifier-CNN/blob/a51a03d466420bdfb1b256a0de1508b7ebfcfaef/images/ISIC_0036049.jpg" width="250" height="250"/> <img src="https://github.com/wilgagne/Skin-Lesion-Classifier-CNN/blob/0ecae0a8d935714b0e9ded7c2d6b96dbba4af133/images/ISIC_0036053.jpg" width="250" height="250"/> <img src="https://github.com/wilgagne/Skin-Lesion-Classifier-CNN/blob/0ecae0a8d935714b0e9ded7c2d6b96dbba4af133/images/ISIC_0036062.jpg" width="250" height="250"/>

Link to dataset: https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000

## Performance
### Accuracy Table of Esteva & al's CNN vs the Class Imbalance CNN
<p align="center">
  <img src="https://github.com/wilgagne/Skin-Lesion-Classifier-CNN/blob/8c779566cdb2da990671c9fca6558888a372b08f/images/Table.png">
</p>

### Confusion matrix for Class Imbalance CNN
<p align="center">
  <img src="https://github.com/wilgagne/Skin-Lesion-Classifier-CNN/blob/8c779566cdb2da990671c9fca6558888a372b08f/images/CM.png">
</p>

## Report
The comprehensive report ([Report.pdf](https://github.com/wilgagne/Skin-Lesion-Classifier-CNN/blob/main/Report.pdf)) delves deeper into the intricacies of the Convolutional Neural Network (CNN) implementation. Within this document, there is a section in which I contributed, comparing CNNs to Vision Transformers (ViTs). 

The findings revealed that CNNs outperformed ViTs across all prediction tasks, achieving superior results with less data due to their enhanced image-specific inductive bias. This disparity in inductive bias likely played a role in the diminished performance of ViTs. 

Additionally, the Vision Transformer model's rapid convergence and subpar performance can be ascribed to the use of frozen pre-trained weights and a lack of adequate training data. This limited the ViT's capacity to effectively recognize skin lesion images and differentiate between various classes.
