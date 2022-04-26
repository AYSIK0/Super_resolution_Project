# Single-Image Super-Resolution (SISR) Using a Multi-Model System

This project builds a combined model by merging a trained **Pixel loss model** based on [EDSR](https://arxiv.org/pdf/1707.02921.pdf) with a **GAN model** based on [SRGAN](https://arxiv.org/pdf/1609.04802.pdf). The project's purpose was to evaluate if this approach can produce better results.

## Jupyter Notebook

The notebook contains all the code created and used in the project; it consists of **Three** main parts.

### 1. Data

Datasets used in this project are included in "Original_Datasets" folder.

#### Train and Validation

[DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/) dataset used for creating the training and validation datasets; however, only the 'HR' and 'X2 bicubic'subsets were used.

**N.B** DIV2K datasets were not included due to their size, they can be downloaded using the code in Jupyter Notebook.

#### Test

Four datasets -Set5, Set14, BSDS100, Urban100- were used for testing.

### 2. Models

Three models were built and trained in this project, all trained version are saved in **Models** folder.

1. Base Model: 2X_base_model.h5, it can be used to generate High-resolution images.

2. GAN Generator: 2X_GAN_gen_model.h5 it can be used to generate High-resolution images.

3. GAN Discriminator: *2X_GAN_dis_model.h5*.

### 3. Models Evaluation

Two evaluation test were conducted between the base model, GAN model, and bicubic interpolation.

1. The average PSNR and SSIM were caluclated and compared.

2. Some images were slected to visuale check and compare the results.
