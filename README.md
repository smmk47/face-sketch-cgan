# Generating Realistic Face Images from Sketches Using cGAN

This repository contains the implementation and training of a **Conditional Generative Adversarial Network (cGAN)** designed to generate realistic face images from skeletal sketches. The project uses the **Person Face Sketches** dataset and demonstrates the potential of cGANs in transforming sketches into photorealistic facial images.



## Introduction
Conditional Generative Adversarial Networks (cGANs) extend traditional GANs by conditioning the generation process on additional input data. In this project, the cGAN is conditioned on face sketches to generate corresponding photorealistic images, offering applications in digital art, forensics, and more.

## Dataset
The project utilizes the **Person Face Sketches** dataset, which contains paired examples of:
- **Input**: Skeletal face sketches.
- **Target**: Corresponding photorealistic face images.

The dataset is preprocessed to standardize image sizes and normalize pixel values.

## Model Architecture
### Generator
- A convolutional neural network (CNN) designed to transform sketches into photorealistic face images.
- Incorporates skip connections (similar to UNet) to retain fine-grained details.

### Discriminator
- Evaluates the authenticity of the generated images conditioned on the input sketches.
- Outputs a probability score indicating how realistic the generated image is.

## Training Details
- **Epochs**: 200
- **Loss Functions**:
  - **Generator Loss**: Combines pixel-wise loss and adversarial loss to encourage realistic outputs.
  - **Discriminator Loss**: Measures the ability to distinguish real from generated images.
- **Optimizer**: Adam optimizer with learning rate 0.0002 and beta values (0.5, 0.999).

## Results
- **Image Quality**: Progressive improvement in the quality of generated face images over training epochs.
- **Visualization**: Side-by-side comparison of sketches and generated images.
- **Challenges**: Minor issues with artifacts in certain outputs.

