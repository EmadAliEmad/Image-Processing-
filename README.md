# Image-Processing

This repository contains a Python notebook (`Requirement_Solution.ipynb`) that demonstrates various image processing techniques on a dataset of images depicting hands interacting with objects.

## Project Overview

The project explores fundamental image processing techniques such as grayscale conversion, histogram equalization, edge detection, and Gaussian derivatives. Additionally, it showcases the application of superpixel segmentation algorithms. The goal is to provide a practical demonstration of common image processing methods and their effects on visual data.

## Dataset

The dataset consists of images from the EgoHands dataset, specifically from the "CARDS_OFFICE_B_S" directory. These images depict hand interactions in an office environment. The dataset is downloaded and organized automatically by the notebook itself.

## Code Overview

The Python notebook (`Requirement_Solution.ipynb`) includes the following steps:

1.  **Environment Setup:**
    *   Imports necessary Python libraries, including `os`, `numpy`, `matplotlib.pyplot`, `skimage`, `scipy` and `requests`.
    *   Downloads the EgoHands dataset as a ZIP file.
    *   Creates directories for storing data, extracts the images from the zip file, and removes unnecessary files.
2.  **Data Loading:**
    *   Loads the image files from the specified directory using skimage's `io.imread` function and stores them in a list.
3.  **Visualization:**
    *  Defines a `draw_func` function that draws a random sample of 9 images in a 3x3 grid using matplotlib.
    *   Visualizes the original images by calling `draw_func` function.
4.  **Grayscale Conversion:**
    *   Converts the color images into grayscale images using `skimage.color.rgb2gray`.
    *   Visualizes the grayscale images.
5.  **Histogram Equalization:**
    *   Applies adaptive histogram equalization to the grayscale images to enhance contrast, using `skimage.exposure.equalize_adapthist`.
    *   Visualizes the equalized images.
6.  **Sobel Edge Detection:**
    *   Applies Sobel filter to detect edges in the equalized images using `skimage.filters.sobel`.
    *   Visualizes the Sobel edge detected images.
7.   **Gaussian Derivatives Calculation:**
     *  Creates Gaussian Filter with given kernel, then creates derivatives in X and Y directions.
     *   Calculates the magnitude and orientation of the gradient using convolution with the derivative filters.
     * Visualizes both the gradient magnitudes and orientations.
8. **Superpixel Segmentation:**
    *  Performs superpixel segmentation on a sample of original images using Felzenszwalb's method (`skimage.segmentation.felzenszwalb`).
    *  Visualizes the superpixel segmentation results overlaid on the original images.

## Project Analysis

This project successfully demonstrates several image processing techniques and highlights how each technique changes the visual representation of the images. The different steps such as grayscale conversion, histogram equalization, edge detection, and gaussian derivatives are illustrated in the project. The super-pixel section helps in extracting information out of the images to a higher degree, by marking the similar areas of images with the same color.

## Repository Organization

This repository contains the following files:

*   `Requirement_Solution.ipynb`: Jupyter Notebook file containing the project code.
*   `README.md`: This file.

## How to Run

1.  Clone the repository to your local machine.
2.  Ensure you have the necessary Python libraries installed: `numpy`, `matplotlib`, `skimage` and `scipy`. If not, install them using `pip install numpy matplotlib scikit-image scipy requests`.
3.  Open `Requirement_Solution.ipynb` using Jupyter Notebook or JupyterLab.
4.  Run the cells sequentially to see the results.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
