# Seamless Social Media Collage Creator

**Made by:** Jazib Waqar Raza
**Course:** CSC381 - Introduction to Digital Image Processing
**Professor:** Kenny Davila Castellanos

## 1. Overview
This tool automates the creation of aesthetically pleasing social media collages (9:16 format) from folder of desired images. It provides an automated procedure covering a 4-stage procedure:
1. **Tone Harmonization:** Utilizes a custom weighted Histogram Equalization algorithm to balance lighting without eroding good characteristic of original image
2. **Edge Detection:** Automatically detects linear features and finds suitable candidates via a 2 step Canny + Probabilistic Hough Transformations
3. **Alignment:** Arranges images via adjustment through Affine Transformation and crop to suitable formats.
4. **Blended Output:** Applies a custom linear blending function along the borders of collage images to feather edges, resulting in seamless transition between images.

## 2. Dependencies
To ensure the program runs smoothly, make sure these following Python libraries are pre-installed:
- OpenCV (cv2)
- NumPy
- Matplotlib
- os (standard library)
- random (standard library)

## 3. Dataset + Setup
This project is designed to function dynamically with varying dataset sizes to utilize either 4 or 6 images to generate a suitable output. There are 3 states of operation here

### a. Preset Sample
A curated subset of 6 images from the original dataset (3 self-take, 3 royalty-free) are preloaded in the "images" directory.
This is done to allow user to run it immediately for testing/grading while still having random order built in to ensure different outputs with each run (purposely done as order can have impact on visual feel)

### b. Total Sample
To obtain the original testing workflow, please access the remaining images from the dataset stored in the cloud link below.
**NOTE: The cloud repository does not contain the preset images from the dataset already in the Preset Sample, please add the remaining images to the "images" directory instead of starting anew**

**Cloud Link:** Google Drive: https://drive.google.com/drive/u/0/folders/1RrvETnaCnV7YIcfKzI2JWvbGAi5yhE11

### c. Custom Sample
To use your own images on this pipeline, please add a minimum of 6 desired images to the "images" directory after deleting any test-case images.

## 4. How to Run Program
1. **Launch Jupyter:** Open the "CSC381_final_JazibWR.ipynb" file in either JupyterLab or Jupyter Notebook
2. **Click "Run All Cells"** Which runs all the file cells from start to end, and notable ones are:
* **Cell 3: Loading**
* **Cell 4: Tone Harmonization***
* **Cell 5: Line Detection***
* **Cell 6-8: Alignment***
* **Cell 9: Blending + Final Output***
3. **Results:**
* The intermediate results are displayed after the cell of stated procedure
* The final result is displayed after the belnding cell
4. **Saved Output:**
* The final collage image is saved at "./Outputs/final_collage.jpg"
* *NOTE: Due to the nature of Jupyter, this file is overwritten with every new run so please move or rename the file if it is desired to be kept.

## 5. Files Included
* "CSC381_final_JazibWR.ipynb": The actual code implementation of the pipeline
* "self_evaluation.pdf": A paper detailing the evaluation of the project's expectation through its development
* "README.md": This file, which documents the end to end procedure on how to operate this project
* "Images/": This is the input directory, that also comes preloaded with 6 images from original dataset
* "Outputs/": A separate folder serving as the place where the generated collage output is stored
	


