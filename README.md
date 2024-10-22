 This repository is about building a tool to sonify astronomical images using Python. Here the process is documented into a structured folder system. A brief description-
 1.	In ‘Initial image loading and pixel extraction script’ we loaded a galaxy image from a .npy dataset using NumPy and then selected a high-resolution image. The pixel data of the image was processed by iterating over each pixel to extract its RGB values, which were then saved in a structured format (CSV file) with row, column, and RGB components. Finally, we visualized the image and its pixel structure using matplotlib.

