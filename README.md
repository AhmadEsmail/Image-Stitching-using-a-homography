# Homography-Based Image Stitching

## Overview

This repository contains a C++ implementation for stitching images captured by different cameras using homography. The code aligns two input images by estimating the homography matrix, which describes the transformation between the images, and applies it to one of the images to create a stitched output.

## Features

- Feature detection and matching using SIFT (Scale-Invariant Feature Transform).
- Robust homography estimation using RANSAC (Random Sample Consensus).
- Normalization of point correspondences for improved numerical stability.
- Image transformation based on the calculated homography matrix.
- Support for reading and writing images using OpenCV.

## Usage

1. **Dependencies**: Ensure you have OpenCV installed on your system. You can install it via package managers like `apt` (on Ubuntu) or `brew` (on macOS), or compile it from source.

2. **Compilation**: Compile the code using a C++ compiler with OpenCV support. For example, you can use `g++`:

    ```bash
    g++ -o stitch_images stitch_images.cpp `pkg-config opencv4 --cflags --libs`
    ```

3. **Execution**: Run the compiled executable with the following arguments:

    ```bash
    ./stitch_images <threshold> <input_image1_path> <input_image2_path> <output_image_path>
    ```

    - `<threshold>`: Inlier-outlier threshold for RANSAC.
    - `<input_image1_path>`: Path to the first input image.
    - `<input_image2_path>`: Path to the second input image.
    - `<output_image_path>`: Path to save the stitched output image.

4. **Example**:

    ```bash
    ./stitch_images 0.5 image1.jpg image2.jpg stitched_image.jpg
    ```

# EX1: inputs:
## Image1 
<img src="https://github.com/AhmadEsmail/Image-Stitching-using-a-homography/blob/main/pair1/m2.jpg" alt="Project Logo" width="550" height="400">

## Image2
<img src="https://github.com/AhmadEsmail/Image-Stitching-using-a-homography/blob/main/pair1/s2.jpg" alt="Project Logo" width="550" height="400">

# output:
<img src="https://github.com/AhmadEsmail/Image-Stitching-using-a-homography/blob/main/pair1/out2_14.3.jpg" alt="Project Logo" width="550" height="400">

---

# EX2: inputs:
## Image1 
<img src="https://github.com/AhmadEsmail/Image-Stitching-using-a-homography/blob/main/pair2/m8.jpg" alt="Project Logo" width="550" height="400">

## Image2
<img src="https://github.com/AhmadEsmail/Image-Stitching-using-a-homography/blob/main/pair2/s8.jpg" alt="Project Logo" width="550" height="400">

# output:
<img src="https://github.com/AhmadEsmail/Image-Stitching-using-a-homography/blob/main/pair2/out8_14.jpg" alt="Project Logo" width="550" height="400">

## Contributing

Contributions are welcome! If you have any ideas for improvement, found a bug, or want to add a new feature, feel free to open an issue or submit a pull request.


