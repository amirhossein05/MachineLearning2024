# GAN-Based Key Generation from Images

This repository contains the implementation of a Generative Adversarial Network (GAN) for generating cryptographic keys from images, as described in the associated paper. The project utilizes a transformation domain to generate keys that are close to the transformed representation of input images.

## Project Description

The implemented GAN model comprises two main components:
- **Generator (G)**: Transforms images from their original domain to a key domain.
- **Discriminator (D)**: Distinguishes between real transformed images and generated keys.

The training process adjusts both networks to produce keys that are indistinguishable from actual transformations of the input images, thereby ensuring the keys' viability and security.

## Dependencies

- Python 3.8+
- PyTorch 1.7+
- torchvision
- PIL
- numpy

To install the required Python packages, run:

```bash
pip install torch torchvision pillow numpy
```
## Setup
```
git clone https://github.com/amirhossein05/MachineLearning2024
cd MachineLearning2024
```
## Usage
To train the model, run:
```
python train.py
```
The script `train.py` will train the GAN model using the dataset specified in the script, adjusting the generator and discriminator according to the loss functions defined.

## Contributing
Contributions to this project are welcome. Please fork the repository and submit a pull request with your features or corrections.

