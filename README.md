<p align="center">
  <img src="satelliteimage.gif" alt="Demo of the application" width="300"/>
</p>

# Semantic Segmentation of Aerial Images: A Comparison of U-Net and SegNet Approaches

This project presents a comprehensive comparative analysis of two models, U-Net and SegNet, applied to semantic segmentation of aerial imagery of Earth. It includes a detailed implementation pipeline, covering model training, testing, and an in-depth discussion of the results. This work was created as part of the Vision and Cognitive Systems course at the University of Padova.

The dataset used in this study can be accessed on Kaggle: [Semantic Segmentation of Aerial Imagery](https://www.kaggle.com/datasets/humansintheloop/semantic-segmentation-of-aerial-imagery/data).


## Segmentation Models

Semantic segmentation models are designed to classify each pixel in an image into one of several predefined categories, enabling detailed analysis of visual data. Two prominent deep learning models used for semantic segmentation are U-Net and SegNet.

### U-Net

U-Net is a convolutional neural network architecture specifically developed for biomedical image segmentation but has since been widely adopted for various segmentation tasks, including aerial imagery. It features a symmetric encoder-decoder structure with skip connections that directly link corresponding layers of the encoder and decoder. These skip connections help in preserving spatial information that is often lost during the down-sampling process in the encoder, thereby improving the segmentation accuracy. U-Net’s architecture is particularly effective for segmentation tasks where the exact localization of structures is crucial.

#### U-Net Architecture

<p align="center">
  <img src="https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/u-net-architecture.png" alt="U-Net architecture" width="600"/>
</p>


### SegNet

SegNet is another popular deep learning model for semantic segmentation. It is characterized by its encoder-decoder architecture, similar to U-Net, but with a distinct approach to the up-sampling process. In SegNet, the encoder network is identical to the convolutional layers of the VGG16 network, which captures high-level features from the input image. The decoder network then uses pooling indices computed in the max-pooling step of the corresponding encoder to perform up-sampling. This method ensures that spatial resolution is maintained, leading to more accurate and fine-grained segmentations. SegNet is known for its efficiency in memory and computational resource usage, making it suitable for real-time applications.

#### SegNet Architecture

<p align="center">
  <img src="https://production-media.paperswithcode.com/methods/segnet_Vorazx7.png" alt="SegNet architecture" width="700"/>
</p>


## Dataset

- **Building**: `#3C1098`
- **Land (unpaved area)**: `#8429F6`
- **Road**: `#6EC1E4`
- **Vegetation**: `#FEDD3A`
- **Water**: `#E2A929`
- **Unlabeled**: `#9B9B9B`


# Sample Images & Masks

<p align="center">
  <img src="realimagevsmask" alt="Demo of the application" width="300"/>
</p>





