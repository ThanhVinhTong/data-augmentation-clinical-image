# data-augmentation-clinical-image

This is my data augmentation script for generating training images when applying different augmentation techniques. The generated data will be used for training deep learning model at my workplace.

## Overview

This Jupyter notebook applies data augmentation techniques to images in the `input/` directory and saves the results to the `output/` directory. It is designed to generate varied training data for deep learning models in clinical image processing.

## Requirements

- Python 3.x
- Jupyter Notebook
- Pillow (PIL)
- NumPy
- Torchvision (which requires PyTorch)

## Installation

1. Clone the repository (if not already done).

2. Install the required packages:

   ```bash
   pip install pillow numpy torch torchvision
   ```

## Usage

1. Place your clinical images (JPG, PNG, BMP) in the `input/` directory.

2. Open and run the `augmentation.ipynb` notebook in Jupyter:

   ```bash
   jupyter notebook augmentation.ipynb
   ```

3. The script will:
   - Resize images to 1000x1000.
   - Save resized originals as numbered BMP files in `output/`.
   - Apply each augmentation and save as `augmented_#.jpg` in `output/`.

## Applied Augmentations

The following transformations are applied to each input image:

- Random Horizontal Flip
- Random Vertical Flip
- Gaussian Blur
- Artifact Lines (near-white)
- Artifact Lines (black)
- Gaussian Noise

Each augmentation is applied individually after resizing.

## Notes

- The output directory will be created if it doesn't exist.
- The script processes all supported image files in the input folder.
- Custom classes are defined for adding Gaussian noise and artifact lines to mimic real-world scanning errors.
