# Raspberrypi_setup_python
## Configure raspberry pi after installation of sd card using pi imager

This repository is intended for the initial setup and configuration of the Raspberry Pi (Raspberry Pi 5 used here), covering the preliminary steps from OS installation to the first clean boot, including initial system updates and upgrades.

## Steps to start with

### 1. Hardware Requirements

- Raspberry Pi 5
- SD card (32GB or more recommended)
- Power supply (official or 5V 3A USB-C)
- HDMI monitor, keyboard, and mouse
- Internet connection (Wi-Fi or Ethernet)

### 2. OS Installation

- Download Raspberry Pi OS from the [official website](https://www.raspberrypi.com/software/).
- Use **Raspberry Pi Imager** to flash the OS to your SD card.
- Insert the SD card into the Pi and boot.

---

## ⚙️ First Boot Configuration

1. Set up the system locale, timezone, and keyboard layout.
2. Change the default password.
3. Connect to Wi-Fi.
4. Run system updates:


sudo apt update


sudo apt upgrade


sudo apt dist-upgrade 


sudo apt install python3 idle3


### Depending on the requirements, additional packages may be needed. These can be installed on the go using the `pip` command, the `apt install` command, or sometimes by using pre-built `.whl` files.

eg: 

pip install numpy pandas matplotlib scikit-learn

or

sudo apt install python3-numpy python3-scipy python3-pandas


### Some additional Python packages that may be useful for general work on a Raspberry Pi—especially for implementing machine learning or conducting scientific analysis—include the following:



### Testing Your Setup

#### You can test your setup with a simple script:

import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y)
plt.title("Simple Sine Wave")
plt.show()

#### you can run it with command python3 follwed by the name of file (eg: abc.py)


## Some of the weel knwon pyhton packages are listed below:
🧰 Categories & Description
🧮 Scientific Computing & Math

    numpy – Fundamental package for numerical operations.

    scipy – Scientific computing tools built on top of NumPy.

    sympy – Symbolic mathematics (algebra, calculus, etc.).

📊 Data Analysis & Visualization

    pandas – Data structures and analysis tools.

    matplotlib – Plotting and visualization.

    seaborn – Statistical data visualization built on top of matplotlib.

🤖 Machine Learning & AI

    scikit-learn – Classical machine learning algorithms.

    tensorflow-lite – Lightweight version of TensorFlow for edge devices.

    keras – High-level neural network API (can work with TFLite backend).

📷 Computer Vision & Image Processing

    opencv-python – Computer vision library.

    pillow – Image processing support (e.g., for loading/saving images).

🖥️ Development & Interactive Tools

    jupyterlab – Web-based IDE for notebooks.

    notebook – Classic Jupyter Notebook interface.

⚙️ Raspberry Pi Hardware Interface

    RPi.GPIO – Control GPIO pins.

    gpiozero – Simplified interface to GPIO.

    pigpio – Advanced GPIO control including PWM, I2C, SPI, etc.

