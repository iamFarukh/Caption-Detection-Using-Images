
# Image Caption Generator

This repository contains code to instantiate and deploy an image caption generation model. This model generates captions from a fixed vocabulary that describe the contents of images in the [COCO Dataset](http://cocodataset.org/#home). The model consists of an _encoder_ model - a deep convolutional net using the Inception-v3 architecture trained on [ImageNet-2012 data](http://www.image-net.org/challenges/LSVRC/2012/) - and a _decoder_ model - an LSTM network that is trained conditioned on the encoding from the image _encoder_ model. The input to the model is an image, and the output is a sentence describing the image content.

## Model Metadata
| Domain | Application | Industry  | Framework | Training Data | Input Data Format |
| ------------- | --------  | -------- | --------- | --------- | -------------- | 
| Vision | Image Caption Generator | General | TensorFlow | [COCO](http://cocodataset.org/#home) | Images | 

## References
* [im2txt TensorFlow Model GitHub Page](https://github.com/tensorflow/models/tree/master/research/im2txt)
* [COCO Dataset Project Page](http://cocodataset.org/#home)


## Pre-requisites:

* `TensorFlow`: Follow the [installation instructions](https://www.tensorflow.org/install/pip/) for your system.
* The minimum recommended resources for this model is 2GB Memory and 2 CPUs.

# Install TensorFlow with pip

### TensorFlow 2 packages are available

-   `tensorflow`  —Latest stable release with CPU and  [GPU support](https://www.tensorflow.org/install/gpu)  _(Ubuntu and Windows)_
-   `tf-nightly`  —Preview build  _(unstable)_. Ubuntu and Windows include  [GPU support](https://www.tensorflow.org/install/gpu).

### Older versions of TensorFlow

For TensorFlow 1.x, CPU and GPU packages are separate:

-   `tensorflow==1.15`  —Release for CPU-only
-   `tensorflow-gpu==1.15`  —Release with  [GPU support](https://www.tensorflow.org/install/gpu)  _(Ubuntu and Windows)_

### System requirements

-   Python 3.5–3.8
    -   Python 3.8 support requires TensorFlow 2.2 or later.
-   pip 19.0 or later (requires  `manylinux2010`  support)
-   Ubuntu 16.04 or later (64-bit)
-   macOS 10.12.6 (Sierra) or later (64-bit)  _(no GPU support)_
-   Windows 7 or later (64-bit)
    -   [Microsoft Visual C++ Redistributable for Visual Studio 2015, 2017 and 2019](https://support.microsoft.com/help/2977003/the-latest-supported-visual-c-downloads)
-   Raspbian 9.0 or later
-   [GPU support](https://www.tensorflow.org/install/gpu)  requires a CUDA®-enabled card  _(Ubuntu and Windows)_

## 1. Install the Python development environment on your system

Check if your Python environment is already configured:

Requires Python 3.5–3.8, pip and venv >= 19.0

```
python3 --version
```

If these packages are already installed, skip to the next step.  
Otherwise, install  [Python](https://www.python.org/), the  [pip package manager](https://pip.pypa.io/en/stable/installing/), and  [venv](https://docs.python.org/3/library/venv.html):

[Ubuntu](https://www.tensorflow.org/install/pip/#ubuntu)[macOS](https://www.tensorflow.org/install/pip/#macos)[Windows](https://www.tensorflow.org/install/pip/#windows)[Raspberry Pi](https://www.tensorflow.org/install/pip/#raspberry-pi)[Other](https://www.tensorflow.org/install/pip/#other)

```
sudo apt update
```

## 2. Create a virtual environment (recommended)

Python virtual environments are used to isolate package installation from the system.

[Ubuntu / macOS](https://www.tensorflow.org/install/pip/#ubuntu--macos)[Windows](https://www.tensorflow.org/install/pip/#windows)[Conda](https://www.tensorflow.org/install/pip/#conda)

Create a new virtual environment by choosing a Python interpreter and making a  `./venv`  directory to hold it:

    python3 -m venv --system-site-packages ./venv

Activate the virtual environment using a shell-specific command:

    source ./venv/bin/activate # sh, bash, or zsh

    .  ./venv/bin/activate.fish # fish
    
    source ./venv/bin/activate.csh # csh or tcsh

When the virtual environment is active, your shell prompt is prefixed with  `(venv)`.

Install packages within a virtual environment without affecting the host system setup. Start by upgrading  `pip`:

```
pip install --upgrade pip
pip list  # show packages installed within the virtual environment
```

And to exit the virtual environment later:

deactivate # don't exit until you're done using TensorFlow

## 3. Install the TensorFlow pip package

Choose one of the following TensorFlow packages to install  [from PyPI](https://pypi.org/project/tensorflow/):

-   `tensorflow`  —Latest stable release with CPU and  [GPU support](https://www.tensorflow.org/install/gpu)  _(Ubuntu and Windows)_.
-   `tf-nightly`  —Preview build  _(unstable)_. Ubuntu and Windows include  [GPU support](https://www.tensorflow.org/install/gpu).
-   `tensorflow==1.15`  —The final version of TensorFlow 1.x.

Package dependencies are automatically installed. These are listed in the  [`setup.py`](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/tools/pip_package/setup.py)  file under  `REQUIRED_PACKAGES`.

[Virtual environment install](https://www.tensorflow.org/install/pip/#virtual-environment-install)[System install](https://www.tensorflow.org/install/pip/#system-install)

    pip install --upgrade tensorflow

Verify the install:

    python -c "import tensorflow as tf;print(tf.reduce_sum(tf.random.normal([1000, 1000])))"



# 3. Use the Model
The syntax for ruining the model is : 

    python Caption_Creator.py -i sample_image.png

### Step 1 
![enter image description here](https://github.com/iamFarukh/Caption-Detection-Using-Images/blob/master/Steps%20and%20Sample/step%201.JPG?raw=true)
### Step 2
![enter image description here](https://github.com/iamFarukh/Caption-Detection-Using-Images/blob/master/Steps%20and%20Sample/step2.JPG?raw=true)
### Step 3
![enter image description here](https://github.com/iamFarukh/Caption-Detection-Using-Images/blob/master/Steps%20and%20Sample/step3.JPG?raw=true)
### Step 4
![enter image description here](https://github.com/iamFarukh/Caption-Detection-Using-Images/blob/master/Steps%20and%20Sample/step4.JPG?raw=true)
### Step 5
![enter image description here](https://github.com/iamFarukh/Caption-Detection-Using-Images/blob/master/Steps%20and%20Sample/step5.JPG?raw=true)



