# Song Conversion using Speech-to-Speech Neuro-Style Transfer

**Version 1.0.0**

A quick guide on installation of important libraries and running the code.

The project has four .ipynb files - isolator.ipynb, transfer1.ipynb, transfer2_evaluation and masker.ipynb

---

## Vocal Isolator

For the Vocal Isolator python script, we need to download/import the following three libraries - [ffmpeg](https://www.ffmpeg.org/), [Spleeter](https://github.com/deezer/spleeter), and [IPython.display](https://ipython.org/ipython-doc/3/api/generated/IPython.display.html). The installation process can be viewed by clicking on the respective library names. For Google Colab or Kaggle Notebook you can use the Isolator_Google_colab file and for Jupyter Notebooks you can use Isolator_Jupyter_Notebooks file.


### Running the code
After you have installed and configured everything, you can run the code by providing the .mp3 file of your choice. All you need to do is to change the input path. After successful run, the script will generate two .wav files - vocals.wav and accompaniment.wav

> **Note:** Specify the required output destination.

---

## Spectrogram Generator and Model 1

It is recommended that you run transfer1.ipynb script in Google Colab or Kaggle notebook because we will be using Tensorflow version 1.15.0

For this script, we need to import the following libraries - [tensorflow](https://pypi.org/project/tensorflow/), [librosa](https://pypi.org/project/librosa/), [os](https://pypi.org/project/os-sys/), [nltk.tokenize](https://www.nltk.org/api/nltk.tokenize.html), [IPython.display](https://ipython.org/ipython-doc/3/api/generated/IPython.display.html), [numpy](https://pypi.org/project/numpy/), [matplotlib](https://pypi.org/project/matplotlib/), and [scipy](https://pypi.org/project/scipy/) lines to download them.

Next step is to load the style and content wav files. Make sure to give the correct address. The model then matches the sampling rate and converts the .wav files into spectrograms images. The CNN model now takes these spectrograms are performs a style transfer on them. The output of this model will be moerphed spectrogram. The next code block converts this spectrogram back into a . wav file.

> **Note:** Specify the required output name and destination.

---

## Model 2 and Evaluation

For this model, run the transfer2_evaluation.ipynb file. Along with the above libraries, we need to import the following additional libraries - [functools](https://pypi.org/project/functools/), and [PIL](https://www.tutorialspoint.com/python_pillow/python_pillow_using_image_module.htm).

You need to change the address of style and content spectrograms. The VGG19 model will then perform the style transfer, calculate the gram matrix and the cosine similarity score.

---

## Masker

For this model, run the masker.ipynb file. Along with the above libraries, we need to import [pydub](https://pypi.org/project/pydub/). You need to change the address of out.wav and accompaniment.wav files. The output will be a masked song in .wav format

> **Note:** Specify the required output name and destination.

---

## Contributors

© Arnav Gupta




