Here's a README file that you can use for your GitHub repository:

---

# Plant Disease Classification using TensorFlow and Tkinter

This project demonstrates a basic plant disease classification application using TensorFlow for the model and Tkinter for the GUI. The model classifies images of plants into three categories: `Bacterial Blight`, `Healthy`, and `Red Rot`. This application allows users to load an image, classify it using the trained model, and display the result along with the image.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Project Structure](#project-structure)
- [Model](#model)
- [License](#license)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/plant-disease-classification.git
   cd plant-disease-classification
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Download the pre-trained model and save it in the `models` directory:
   - Place your model in the `models` directory with the filename `sugercane_model.h5` (for sugarcane classification) or `maize_model.h5` (for maize classification).

## Usage

1. To run the application, execute the following command:
   ```bash
   python app.py
   ```

2. The application window will open. Click on "Browse Image" to select an image from your local machine.

3. The selected image will be displayed in the application window along with the predicted class.

## Dependencies

- `tensorflow`: For building and running the machine learning model.
- `tensorflow-hub`: For using pre-trained models.
- `PIL`: For image processing.
- `Tkinter`: For creating the GUI.
- `numpy`: For numerical operations.
- `seaborn`, `matplotlib`: For visualization (if needed).

Install the dependencies with:
```bash
pip install tensorflow tensorflow-hub pillow numpy matplotlib seaborn
```

## Project Structure

```plaintext
plant-disease-classification/
│
├── models/
│   ├── sugercane_model.h5  # Model for sugarcane classification
│   └── maize_model.h5      # Model for maize classification
│
├── app.py                  # Main application code
└── README.md               # Project documentation
```

## Model

The model used in this application is a pre-trained MobileNetV2 model from TensorFlow Hub, fine-tuned for plant disease classification. It accepts an input image of size 224x224 and outputs a probability distribution across three classes: `Bacterial Blight`, `Healthy`, and `Red Rot`.

