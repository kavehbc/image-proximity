# Image Proximity Search using Autoencoder

In this project, we are finding similar images using Autoencoder implemented by Keras.
The method has been implemented and tested on the following datasets:

- MNIST Fashion:
  - This dataset is developed by Zalando. It is publicly available [here](https://github.com/zalandoresearch/fashion-mnist).
- Fashion Gen (SSENSE):
  - This dataset is collaboration between ElementAI and SSENSE. You can request to download the dataset [here](https://fashion-gen.com/).
  - For more information, you can check the published article [here](https://arxiv.org/abs/1806.08317).

## Initialization

You should create a conda environment using the `environment.yml` file
to install all the required libraries and dependencies.

```bash
conda env create -f environment.yml
```

## File Structure

- `01_image_processing.ipynb`
  - This Jupyter Notebook opens the images and apply some preprocessing steps to uniform the dataset.
    - Converting images to grayscale (black & white) to reduce the complexity and data dimension
    - Rescaling images to a square shape with the same size

- `02_generate_dataset.ipynb`
  - This Jupyter Notebook opens the processed images and convert them into numpy arrays.

- `03_training_autoencoder_fashion_mnist.ipynb`
  - This Jupyter Notebook trains an autoencoder model on MNIST Fashion.

- `04_training_autoencoder_ssense.ipynb`
  - This Jupyter Notebook trains an autoencoder model on Fashion Gen.

## Auto-Encoder

### MNIST Fashion

MNIST images are all 28x28 pixels and requires minimum preprocessing.
In the encoder section, it encodes 28x28 pixel images into a 4 x 4 x 8 representation (i.e. 128-dimensions).
And then in the decoder section, they weill be decoded back to 28 x 28 x 1 representation in grayscale.

### Fashion Gen (SSENSE)

Within the preprocessing notebook, all images are converted into 224 x 224 pixels.
In the encoder section, it encodes 224x224 pixel images into a 4 x 4 x 64 representation (i.e. 1024-dimensions).
And then in the decoder section, they weill be decoded back to 224 x 224 x 1 representation in grayscale.

___
## GitHub Repo
This project is open-source, and it is available on GitHub at [https://github.com/kavehbc/image-proximity](https://github.com/kavehbc/image-proximity).

## Developer(s)
Kaveh Bakhtiyari - [Website](http://bakhtiyari.com) | [Medium](https://medium.com/@bakhtiyari)
  | [LinkedIn](https://www.linkedin.com/in/bakhtiyari) | [GitHub](https://github.com/kavehbc)

## Contribution
Feel free to join the open-source community and contribute to this repository.

