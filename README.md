# Brain-Tumor-MRI-Classification

# Brain Tumor MRI Classification Web Application

## Table of Contents
1. [Introduction](#introduction)
2. [Project Directory Structure](#project-directory-structure)
3. [Dataset Description](#dataset-description)
4. [Features](#features)
5. [Usage](#usage)
6. [Before and After Prediction States](#before-and-after-prediction-states)
7. [Technologies Used](#technologies-used)
8. [How to Run Locally](#how-to-run-locally)
9. [Future Enhancements](#future-enhancements)

---

## Introduction
This project is a Flask-based web application for classifying brain tumors using MRI images. The application allows users to upload MRI scans, processes them using a pre-trained deep learning model, and displays the predicted type of brain tumor. The interface supports drag-and-drop functionality for ease of use and provides immediate feedback on the uploaded image and prediction results.

The primary objective of this project is to help in automating brain tumor diagnosis by providing an easy-to-use interface powered by a robust image classification model.

---

## Project Directory Structure
The following is the directory structure of the project:

```
brain_tumor_flask/
├── app.py                  # Main Flask application script
├── static/
│   ├── background.webp     # Background image for the webpage
│   └── style.css           # CSS file for styling the webpage
├── templates/
│   └── index.html          # HTML template for the webpage
├── model/
│   └── finally_brain_tumor_model.keras  # Pre-trained model for classification
└── uploads/                # Directory for storing uploaded images (created at runtime)
```

---

## Dataset Description
The dataset used for this project is the **Brain Tumor MRI Dataset** provided by [Masoud Nickparvar](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) on Kaggle.

### Key Details:
- The dataset contains **4 classes** of MRI images:
  - Glioma
  - Meningioma
  - Pituitary Tumor
  - No Tumor
- The images are categorized into training and testing sets.
- The dataset includes a total of **7,043 images**.

This well-structured dataset was used to train a convolutional neural network (CNN) model with high accuracy for brain tumor classification.

---

## Features
1. **Drag-and-Drop Upload**: Users can upload MRI images either by selecting them manually or by dragging and dropping the file.
2. **Real-Time Image Preview**: The uploaded image is displayed on the webpage before the prediction is made.
3. **Prediction Display**: The predicted tumor type is shown below the uploaded image after processing.
4. **Responsive Design**: The application is styled with CSS to ensure a clean and user-friendly interface.

---

## Usage
### 1. **Before Prediction**
In the initial state, the webpage displays a form prompting the user to upload an MRI image. The drag-and-drop area is highlighted to encourage an intuitive user experience.

![Screenshot 2025-01-11 165646](https://github.com/user-attachments/assets/00765fc7-5d42-48bc-8766-58c6f6ddcf3a)

### 2. **After Prediction**
Once the user uploads an MRI image and clicks the **Predict** button, the application processes the image, classifies it using the trained model, and displays the prediction result along with the uploaded image.

![Screenshot 2025-01-11 165706](https://github.com/user-attachments/assets/436612ce-3f6b-439e-8198-4f06ddce4373)

---

## Technologies Used
- **Flask**: Python web framework for building the web application.
- **TensorFlow/Keras**: Deep learning framework used to load the pre-trained model.
- **HTML/CSS**: For structuring and styling the web interface.
- **JavaScript**: For handling drag-and-drop functionality and real-time image preview.

---

## How to Run Locally
### Prerequisites:
- Python 3.x
- Flask
- TensorFlow
- Required Python packages (listed in `requirements.txt`)

### Steps:
1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd brain_tumor_flask
   ```

2. **Create a virtual environment and activate it**:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows, use: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Flask app**:
   ```bash
   python app.py
   ```

5. **Open the application in your browser**:
   Visit `http://127.0.0.1:5000/` in your web browser.

---

## Future Enhancements
1. **Deployment**: Deploy the application on a cloud platform such as Heroku or AWS.
2. **Improved Model**: Train the model with a larger dataset for better accuracy.
3. **Additional Features**:
   - Add a feature to display confidence scores for each prediction.
   - Enable users to download a PDF report of the prediction.

---

Feel free to contribute to this project by submitting issues or pull requests. We hope this tool proves useful for educational and research purposes in the field of medical image analysis.

