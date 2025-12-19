# Retinal Disease Classification CNN

This project implements a Convolutional Neural Network (CNN) to classify retinal diseases from fundus images into 8 categories (AMD, Cataract, Diabetes, Glaucoma, Hypertension, Myopia, Normal, Other).
## !Important: The folder images_256 is required at the root of the project, you can get it here https://drive.google.com/file/d/1dE3fTB3lddnzwcHW-HH-ccs7q88EJPGh/view?usp=sharing. 
## Alternatively, If you are working with the original images folder, run resize_images, and the images_256 folder will be created. You can zip it to import to colab, or use locally 
## 🚀 Quick Start: Google Colab
This is the easiest way to run the project without local setup.
Use T4 GPU if possible via Runtime > Change runtime type

### 1. Training the Model
1.  Open the `62FIT4ATI_Group 20_Topic 3.ipynb` notebook in Google Colab.
2.  **Upload Data:**
    * Click the **Files** icon (folder) on the left sidebar.
    * Upload your `label_images.csv` file.
    * Upload your compressed dataset: `images-256.zip`.
3.  **Extract Data:**
    * Run the `extract_zip.ipynb` to unzip `images-256.zip`.
4.  **Run Training:**
    * Run all cells under the.
    * Once finished, the model will save a checkpoint file (e.g., `Retinal_Disease_ClassificationCnn.pth`). **Download this file** if you want to save your progress.

### 2. Inference (Testing on New Data)
1.  Open the `62FIT4ATI_Group 20_Topic 3.ipynb.ipynb` notebook in Google Colab.
2.  **Upload Artifacts:**
    * Upload the trained weights file: `Retinal_Disease_ClassificationCnn.pth`.
    * Upload the labels file: `label_images.csv` (required for verifying accuracy).
3.  **Run Inference:**
    * Run the **Setup/Imports** cells and the **Model Class Definition** cell.
    * **Skip** the training loop.
    * Scroll down to the **Inference** section.
    * Run the "File Upload" cell. It will prompt you to upload a new retinal image (JPG/PNG) and will display the prediction vs. the actual label from the CSV.

---

## 💻 Local Environment Setup
If you prefer to run this on your own machine.

### 1. Prerequisites
Ensure you have Python installed. Install the necessary libraries
### 2. Data Setup
Ensure you have the label_images.csv file and images_256 folder in your project root.

### 3. Training
Open the project folder in your IDE (VS Code, PyCharm, or Jupyter Lab).

Run the entire notebook.

### 4. Inference

Verify that Retinal_Disease_ClassificationCnn.pth and label_images.csv are present.

Run codes in the inference section.

📂 Project Structure
Plaintext

   ├── main.ipynb                          # Main notebook for Train & Inference

   ├── label_images.csv                    # Ground truth labels

   ├── Retinal_Disease_ClassificationCnn.pth # Saved Model Weights

   └── images_254/                         # Folder containing processed images
