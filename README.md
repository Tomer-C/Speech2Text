# Speech2Text
Speech2Text is a Python application that allows users to transcribe speech to text. The application is built using the LJ Speech Dataset and a speech-to-text model trained on Google Colab. The graphical user interface (GUI) was written in Python and developed using Visual Studio Code.

All the source code for this project can be found in a single [repository](https://github.com/Tomer-C/Speech2Text) on GitHub.

## Installation
Before installing Speech2Text, please ensure that you have Python 3 installed on your computer. You can download the latest version of Python 3 from the [official website](https://www.python.org/downloads/). Make sure python and pip are in your Windows PATH.

To install Speech2Text, you can either clone this repository or download it as a ZIP file and extract its contents to a local directory.

Next, navigate to the directory where you extracted the contents of Speech2Text and run the following command in your terminal to install the required dependencies:

    pip install -r requirements.txt

(Optional) If you want to [convert the Python file into an executable file](https://datatofish.com/executable-pyinstaller/), you can use PyInstaller:

    pip install pyinstaller

    pyinstaller --onefile Speech2Text.py

## Usage
To run Speech2Text, navigate to the directory where you extracted the contents of Speech2Text and run the following command in your terminal:

python Speech2Text.py

This will launch the graphical user interface, where you can browse and select audio files to transcribe.

## GUI & Features
The GUI was built using tkinter, a Python standard library for creating GUI applications. The layout was created using the ttk module, which provides themed widgets that have a modern look and feel.

The application provides the following features:

- Browse and select a folder containing .wav files.
- Play the selected .wav file.
- Transcribe the selected .wav file to text using a deep learning model.
- Display the predicted transcription and the actual transcription.
- Calculate the Word Error Rate (WER) between the predicted and actual transcriptions.
- Revert to the default test data folder.

If necessary, you can watch a [demo video](https://photos.app.goo.gl/x7U4pi4uTHUZ5qpXA) of the GUI in action.

The following Python libraries are used in the GUI:
- numpy
- tensorflow
- jiwer
- keras
- csv
- requests
- json
- subprocess

## Deep Learning Model
The application utilizes a deep learning model created with TensorFlow and Keras to convert speech to text. The model is based on the DeepSpeech2 architecture and was trained on a vast dataset of .wav files.

The model was developed and trained in a Google Colab notebook. After the training, the model was uploaded to a TensorFlow server and is now served via a REST API.

It is important to note that the installation of the deep learning model is not required since it is hosted on a remote server and accessed through the API. However, if you're interested in exploring the model further or making modifications to it, the code and instructions for training the model can be found later under "Colab Notebook".

You are welcome to read more about [TensorFlow Serving with Docker](https://github.com/tensorflow/serving/blob/master/tensorflow_serving/g3doc/docker.md).

## Colab Notebook
To view the Colab Notebook used to develop and train the deep learning model, please follow these steps:

- Go to [Google Colab](https://colab.research.google.com/).
- Click on the "GitHub" tab.
- Search for the repository containing the Speech2Text Colab Notebook (https://github.com/Tomer-C/Speech2Text).
- Select the Speech2TextProject.ipynb file to open the Colab Notebook.
- Follow the instructions in the notebook to run the code and train the model
  (Set the `train` flag to **True** to indicate that we are training the model / Set the `train` flag to **False** to indicate that we are not training the model).

The Colab Notebook contains the code used to preprocess the dataset, define the model architecture, train the model, and save the trained weights. The notebook also includes detailed comments and explanations to help you understand the code and the deep learning concepts used in the model.

The following Python libraries are used in the Colab Notebook:
- pandas
- numpy
- tensorflow
- keras
- layers
- matplotlib.pyplot
- IPython
- display
- jiwer
- wer
- datetime
- random

## External Links
The project was created by Tomer Cicelsky.

The model was trained on the [LJ Speech Dataset](https://keithito.com/LJ-Speech-Dataset/)

The speech-to-text model was based on the [DeepSpeech2 model](https://nvidia.github.io/OpenSeq2Seq/html/speech-recognition/deepspeech2.html)

The Word Error Rate calculation was implemented using the [jiwer library](https://pypi.org/project/jiwer/)


