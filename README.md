# Create readme markdown string 
readme_text = """ 
# Image Blur Analysis Notebook 
 
This Jupyter notebook demonstrates various levels of Gaussian blur effects on images and their impacts through difference maps. 
 
## Contents 
 
1. Image Processing Setup 
    - Loads a high-detail RGB image (`hi.jpg`) 
    - Uses OpenCV and NumPy for image processing 
    - Utilizes Matplotlib for visualization 
 
2. Blur Applications 
    - Mild blur: 25x25 kernel, σ=10 
    - Strong blur: 51x51 kernel, σ=20 
    - Extreme blur: 101x101 kernel, σ=30 
 
3. Difference Analysis 
    - Computes absolute differences using `cv2.absdiff` 
    - Generates difference maps between original and blurred images 
    - Visualizes changes using `jet` colormap with `vmax=100` 
    - Adds colorbars to difference map plots for intensity reference 
 
## Dependencies 
- OpenCV (cv2) 
- NumPy 
- Matplotlib 
 
## Visualization 
The notebook displays a 2x3 grid showing: 
- Original image (must contain fine detail) 
- Three levels of blur (mild, strong, extreme) 
- Two difference maps (mild and strong), with colorbars 
""" 
 
# Write to README.md file 
with open('README.md', 'w') as f: 
    f.write(readme_text)
