# Strain-Analysis-CNN
# Deep Learning based Strain Analysis in Metasedimentary Rocks

This repository presents a reproducible pipeline for semi-automated strain analysis in metasedimentary rocks using deep learning and image processing techniques. The focus is on petrographic thin sections from the Galice and Mariposa Formations in the Western Sierra Nevada and Klamath Mountains.

## Project Summary

The workflow replaces traditional manual tracing methods with a U-Net-based Convolutional Neural Network (CNN) to perform mineral segmentation. Post-segmentation, ellipse fitting is applied to segmented clasts to extract morphological data such as axial ratios, orientations, and area percentages—key metrics for finite strain analysis.

## Directory Structure
📁 .IPYNB Files → Jupyter notebooks for training, segmentation, ellipse fitting, and plotting
📁 Full thin sections → Full-size thin section images used for segmentation
📁 Models → Trained U-Net models (.h5 files)
📁 dataset/ → Primary dataset of image patches
📁 dataset11/ → Additional dataset variant
📁 dataset12/
📁 dataset18/
📁 dataset21/
📁 dataset51/
📁 datasetgf11/ → Galice Formation image patches
📁 datasetgf12/
📁 input_images/ → Input images for testing and visualization
📄 predicted_clasts_ellipses.csv → Output table of ellipse parameters from OpenCV fitting
📄 README.md → Project overview and usage guide


## Key Features

- U-Net CNN for segmenting petrographic images into matrix, clasts, and lithics
- Automated ellipse fitting using OpenCV
- Output generation for clast orientations (phi), aspect ratios (R), and centroid positions
- Visualization: confusion matrix, rose diagrams, and histogram plots
- Patch-wise evaluation of segmentation performance

## Usage

 Run notebooks in .IPYNB Files to:

  Train or load a U-Net model
  Perform segmentation on full thin sections
  Fit ellipses to clasts



## The final outputs include:

Confusion matrix (for segmentation accuracy)
Areal percentage breakdown by class
Ellipse parameter table (orientation, aspect ratio)
Clast orientation rose diagrams
Axial ratio histograms

## Notes

The dataset folders contain preprocessed image patches used for training and validation.
Large files may be managed using external tools such as Git LFS or DVC if needed.
Replace or expand datasets as required for additional formations or sections.
Generate plots and CSV results

