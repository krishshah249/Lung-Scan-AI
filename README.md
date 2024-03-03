# Pneumonia Detection through X-rays images

This project focuses on detecting pneumonia in human lungs using X-ray images. The detection is performed using deep learning techniques implemented with Keras, while Flask is used to implement backend for serving predictions and a front-end interface developed using HTML, CSS, and JavaScript.
This project performs human lungs classification using Convolutional Neural Networks with automated image pre-processing and internal procedures.

## Overview

Pneumonia is a serious respiratory condition that requires prompt diagnosis and treatment. This project aims to assist medical professionals in diagnosing pneumonia by analyzing X-ray images of human lungs. The deep learning model trained on a dataset of X-ray images can classify whether a given X-ray image indicates the presence or absence of pneumonia.

The project is deployed on Google App Engine at https://flaskdeploy-xray.appspot.com/ and the UI looks like the image show below.

![homepage][0]

## Dataset

The dataset used in this project is the Chest X-Ray Images (Pneumonia) dataset from Mendeley. It contains X-ray images of human lungs categorized into normal and pneumonia bacteria and virus classes. The X-Ray of lungs are available at [Dataset](https://data.mendeley.com/datasets/rscbjbr9sj/2).

## Usage

To use this project:

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/krishshah249/Lung-Scan-AI.git
    ```

2. Navigate to the cloned repository:

    ```bash
    cd Lung-Scan-AI
    ```

3. Install the necessary dependencies:

    ```bash
    pip install -r deploy/requirements.txt
    ```

4. Run the Flask app:

    ```bash
    python deploy/main.py
    ```

5. Open your web browser and navigate to http://localhost:5000 to access the front-end interface.

To re-train or experiment with the project:

1. Use the "Pneumonia-AI Image Classifier" Jupyter Notebook.

## Directory Structure

- `deploy/app/`: Contains the Flask backend application.
- `deploy/static/`: Contains static files (e.g., CSS, JavaScript) for the front-end interface.
- `deploy/templates/`: Contains HTML templates for rendering the front-end interface.
- `saved_models/`: Contains the trained Keras model for pneumonia detection.
- `good_models/`: Contains the models that have good validation performance for pneumonia detection.
- `bad_models/`: Contains the models that have bad validation performance for pneumonia detection.
- `data/`: Contains the dataset used for training and evaluation.

## Model Evaluation

The deep learning model's performance is evaluated based on various metrics such as accuracy, precision, recall, and F1-score. The evaluation results are presented in the Flask app's user interface. The accuracy of the model is around 80% which is achieved by using regularization techniques such as Dropout, L2 Regularization and Rmsprop with Adam but it can be increased further through hyperparater optimization.

#### The Validation Accuracy Graph for the best trained model is displayed below

![val_acc][1]

#### The Validation Loss Graph for the best trained model is displayed below

![val_loss][2]

## Contributing

Contributions to this project are welcome! If you have ideas for improvements, new features, or bug fixes, feel free to open an issue or submit a pull request.

[0]: images/homepage.png
[1]: images/val_acc.png
[2]: images/val_loss.png
