 This repository is about building a tool to sonify astronomical images using Python. Here the process is documented into a structured folder system. A brief description-
 1.	In ‘Initial image loading and pixel extraction script’ we loaded a galaxy image from a .npy dataset using NumPy and then selected a high-resolution image. The pixel data of the image was processed by iterating over each pixel to extract its RGB values, which were then saved in a structured format (CSV file) with row, column, and RGB components. Finally, we visualized the image and its pixel structure using matplotlib.
 2.	In 'Mapping Pixel Data to Sound Parameters' with the help of the Pydub library, we have mapped pixel data of RGB images onto sound parameters. Red channel controls frequency (from 200 Hz to 2000 Hz), the green channel controls volume of sound (from -20 dB to 0 dB), while the blue channel takes care of duration. The pixels were processed from the CSV file (from 1) and sinewave audio segments were created and combined to create a single sound file which was then exported as a WAV file.
 3.	The 'Integrated pixel extraction and sound mapping' includes a Python-based application built to convert visual data derived from images into sound, known as the Image Sonification Tool. The tool uses multiple formats of images supported by.png,.jpg, and.npy files.
The basis of the tool's work is three sonification modes:

Brightness-based pitch modulation: This mode translates the brightness of every pixel into a corresponding pitch, establishing a direct relation between light intensity and sound.

Color-based sound effects: RGB values of every pixel are mapped to frequency (pitch), volume, and duration, creating sound effects based on the color composition of the image.

Spatial stereo mapping: Pixel positions are used to create stereo effects, panning sound across the left and right channels based on the horizontal position of the pixel in the image.

The program processes the image pixel by pixel, generating a sound for each. To improve on large images, the rows of pixels are individually processed and the tqdm library is used to display the progress bar. Once an image is processed, generated audio is saved as.wav.

