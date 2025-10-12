# 🖼️ Digital Image Compression and Bit-Plane Analysis

This repository contains the implementation and analysis of fundamental concepts in **Digital Image Processing**, focusing on image compression, **quantization**, and the visualization of an image's information content via **bit-plane slicing**.

The project uses Python, OpenCV, and NumPy to perform pixel-level manipulations and analyze the effects on image quality and file size.

## ✨ Core Topics and Implementations

1.  **Bit-Plane Slicing:** Extraction and visualization of individual bit-planes (from $2^0$ to $2^7$) to understand their contribution to the image's overall intensity and structure.
    * **Goal:** Demonstrate how the most significant bits (MSBs) contain primary visual information, while the least significant bits (LSBs) primarily contribute to fine detail and noise.
2.  **Bit-Depth Reduction (Quantization):** Image compression by removing $N$ least significant bits (e.g., removing 1, 2, ..., 7 bits).
    * **Analysis:** Comparison of the original image with the reduced-bit-depth image and the corresponding **difference image** to quantify information loss.
3.  **File Size Analysis:** Measurement and visualization of the effect of bit-depth reduction on the final image file size.
4.  **Contrast Enhancement & Noise:** Basic operations like analyzing image contrast and potentially introducing noise (if present in the notebook).

## 🚀 Getting Started

### Prerequisites

You need the following libraries installed:

```bash
pip install opencv-python numpy matplotlib jupyter


Execution
The core analysis and visualizations are contained within the Jupyter Notebook.

Open the Notebook:

Bash

jupyter notebook notebooks/OpenCV1.ipynb
Run Cells: Execute all cells sequentially. The notebook will:

Load the input image (assets/man.png).

Perform bit-plane slicing and display the results.

Apply bit-depth reduction (e.g., removing 1 to 7 bits) and display the compressed images and difference maps.

Plot the file size change as a function of the number of removed bits.

📂 Project Structure
File/Folder	Purpose
notebooks/OpenCV1.ipynb	Main Code and Analysis: Contains all the Python/OpenCV logic and visual explanations.
assets/man.png	The original grayscale image used for processing.
assets/bit_plane_*.png	Visual output of individual bit-planes.
assets/output1.jpg	Example output from the compression process.
src/	Placeholder for standalone Python script version.
documentation/	Contains project reports or detailed findings.
README.md	This documentation file.

Export to Sheets
💡 Key Concepts Analyzed
Concept	Description
Bit-Plane	A specific plane of the image that holds the i-th bit of every pixel value (e.g., the 8 
th
  bit plane is the 2 
7
  plane).
Quantization	The process of reducing the number of gray levels (e.g., from 256 to 2 
8−N
 ) used to represent the image, directly linked to bit-depth reduction.
Difference Image	The absolute difference between the original and compressed image, visually highlighting the information lost due to quantization.

Export to Sheets
