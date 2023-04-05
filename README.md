# Speech2Text
Speech2Text is a Python application that allows users to transcribe speech to text. The application is built using the LJ Speech Dataset and a speech-to-text model trained on Google Colab. The graphical user interface (GUI) was written in Python and developed using Visual Studio Code.

## Installation
Before installing Speech2Text, please ensure that you have Python 3 installed on your computer. You can download the latest version of Python 3 from the official website: https://www.python.org/downloads/. Make sure python and pip are in your Windows PATH.

To install Speech2Text, you can either clone this repository or download it as a ZIP file and extract its contents to a local directory.

Next, navigate to the directory where you extracted the contents of Speech2Text and run the following command in your terminal to install the required dependencies:

    pip install -r requirements.txt

(Optional) If you want to convert the Python file into an executable file, you can use PyInstaller:

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

## Deep learning model
The application uses a deep learning model implemented with TensorFlow and Keras to transcribe speech to text. The model, which was based on the DeepSpeech2 model, was trained on a large dataset of .wav files.

The model was developed and trained in a Google Collab notebook.

After training, the model was uploaded to a TensorFlow server and is served via a REST API.

## Credits and Acknowledgements
The application was created by Tomer Cicelsky.

The LJ Speech Dataset, on which the model was trained - (https://keithito.com/LJ-Speech-Dataset/)

The speech-to-text model based on the DeepSpeech2 model - (https://nvidia.github.io/OpenSeq2Seq/html/speech-recognition/deepspeech2.html)

The Word Error Rate calculation was implemented using the jiwer library - (https://pypi.org/project/jiwer/)

The following Python libraries:
- numpy
- tensorflow
- jiwer
- keras
- csv
- requests
- json
- subprocess
