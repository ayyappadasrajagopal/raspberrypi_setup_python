# Raspberrypi_setup_python
## Configure raspberry pi after installation of os image to sd card using pi imager

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


###  3. First Boot Configuration

1. Set up the system locale, timezone, and keyboard layout.
2. Change the default password.
3. Connect to Wi-Fi.
4. Run system updates:
   - sudo apt update
   - sudo apt upgrade
   - sudo apt dist-upgrade 
   - sudo apt install python3 idle3
   - [website](https://pramuditharidma.medium.com/how-to-install-python-idle-on-raspberry-pi-9307e6fec108)

- Install VS Code in raspberry pi 5
    - sudo apt install code 
    - [website](https://code.visualstudio.com/docs/setup/raspberry-pi)


---

## ⚙️ For Extended Reading

#### Depending on the requirements, additional packages may be needed. These can be installed on the go using the `pip` command, the `apt install` command, or sometimes by using pre-built `.whl` files.

pip install numpy pandas matplotlib scikit-learn

or

sudo apt install python3-numpy python3-scipy python3-pandas


### Some additional Python packages that may be useful for general work on a Raspberry Pi—especially for implementing machine learning or conducting scientific analysis—include the following:


### Testing Your Setup

#### You can test your setup with a simple script:

```import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y)
plt.title("Simple Sine Wave")
plt.show()
 ``` 
---
#### you can run it with command python3 follwed by the name of file (eg: abc.py)


## Some of the well known pyhton packages are listed below:
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
   - jupyterlab – Web-based IDE for notebooks.
   - notebook – Classic Jupyter Notebook interface.

⚙️ Raspberry Pi Hardware Interface
   - RPi.GPIO – Control GPIO pins.
   - gpiozero – Simplified interface to GPIO.
   - pigpio – Advanced GPIO control including PWM, I2C, SPI, etc.

### 📦 Useful Python Packages (pip install format)
🧮 Scientific Computing & Math

- pip install numpy
- pip install scipy
- pip install sympy
- pip install mpmath

📊 Data Analysis & Visualization

- pip install pandas
- pip install matplotlib
- pip install seaborn
- pip install plotly
- pip install tabulate

🤖 Machine Learning & Deep Learning

- pip install scikit-learn
- pip install xgboost
- pip install tensorflow
- pip install keras
- pip install tensorflow-lite

🧪 Interactive Development & Jupyter

- pip install jupyterlab
- pip install notebook
- pip install ipywidgets

🖼️ Computer Vision & Image Processing

- pip install opencv-python
- pip install pillow
- pip install imageio
- pip install scikit-image

🧠 AI/ML Toolkits for Edge Devices

- pip install tflite-runtime
- pip install onnxruntime

🐍 Raspberry Pi Hardware Interfacing

- pip install RPi.GPIO
- pip install gpiozero
- pip install pigpio
- pip install spidev
- pip install smbus2

🌐 Networking & IoT

- pip install paho-mqtt
- pip install requests
- pip install flask
- pip install socketio

📦 Utilities & System Tools

- pip install psutil
- pip install schedule
- pip install rich
- pip install tqdm
- pip install loguru

🔐 Security & Encryption (Optional)

- pip install cryptography
- pip install pyjwt

⚙️ Miscellaneous Useful Packages

- pip install pyserial          # Serial communication
- pip install pyfirmata         # Arduino interface
- pip install pyttsx3           # Text-to-speech
- pip install speechrecognition # Speech recognition
- pip install pynput            # Keyboard/mouse control
- pip install pyautogui         # GUI automation

📝 Optional: One-Liner Install for Core Scientific Stack

pip install numpy scipy pandas matplotlib seaborn scikit-learn sympy jupyterlab
