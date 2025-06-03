<!-- Maintained by Ayyappadas R-->
# raspberrypi_setup_python
Created and Maintained by Ayyappadas R
## Configure raspberry pi after installation of os image to sd card using pi imager
This repository is intended for the initial setup and configuration of the Raspberry Pi (Raspberry Pi 5 used here), covering the preliminary steps from OS installation to the first clean boot, including initial system updates and upgrades.

## 1. Steps to start with
### 1. Hardware Requirements
- Raspberry Pi 5
- SD card (32GB or more recommended)
- Power supply (official or 5V 3A USB-C)
- HDMI monitor, keyboard, and mouse
- Internet connection (Wi-Fi or Ethernet)

- Raspberry pi pinout 
![Figure](GPIO_diagram.jpg)

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
## 2. Basic help codes to interact with python in raspberry pi (or in general with python) (in terminal or in python console)
✅ Add a shortcut to the Documents folder on the Desktop
- ln -s /home/pi/Documents /home/pi/Desktop/Documents

✅ Check Python version:
- python --version (or python3 --version if python2 and python3 are installed)
- To go to python terminal from command terminal
- python3 (to exit type exit())

✅ Run a Python script:
- python3 your_script.py (your_script.py is the file name with .py extension)

✅ Check pip version:
- pip --version

✅ List installed packages:
- pip list

✅ Upgrade pip:
- python3 -m pip install --upgrade pip

✅ Location of Python executable:
- which python3

✅ Check Where Python Packages Are Installed
- python3 -m site

✅ Virtual environment
- Create virtual environment
 - python3 -m venv myenv
- Activate it:
 - source myenv/bin/activate
- Deactivate it:
 - deactivate

<!-- This is a hidden comment 
<span style="color:red">This won't work on GitHub</span> 
🟢 Active  
🔴 Inactive  
🟡 Warning  
🔵 Info
-->

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



## 4. Some helpful websites
https://packaging.python.org/en/latest/tutorials/installing-packages/


1. Publishing a Python Package from GitHub to PyPI in 2024
- https://medium.com/@blackary/publishing-a-python-package-from-github-to-pypi-in-2024-a6fb8635d45d

2. Static code analyser for Python3
- Pylint is a static code analyser for Python 2 or 3.
- pip install pylint
- https://pylint.readthedocs.io/en/latest/


## Learn python class and definition

Let's walk through a clean example that shows:

    One file defines a class and a function

    Another file contains the main() function and imports the first file

    main() then calls both the imported function and class methods

🧾 File Structure

We'll use two Python files:

project/
├── utils.py         # Contains a class and a function
└── main_program.py  # Contains main(), imports from utils.py

📄 1. utils.py – defines reusable code

# utils.py

class Robot:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(f"Hello! I am robot {self.name}.")

def greet_user(username):
    print(f"Welcome, {username}!")

📄 2. main_program.py – imports and uses the code

# main_program.py

from utils import Robot, greet_user  # importing from utils.py

def main():
    # Call imported function
    greet_user("Ayyappadas")

    # Create object from imported class
    r1 = Robot("EKAM-1")
    r1.speak()

if __name__ == "__main__":
    main()

▶️ Running the Code

Run main_program.py:

$ python main_program.py

✅ Output:

Welcome, Ayyappadas!
Hello! I am robot EKAM-1.

🔍 What's Happening
Component	Description
utils.py	A module containing reusable code (a class and a function)
main_program.py	The main driver script
from utils import ...	Brings in code from another file
if __name__ == "__main__"	Ensures main() runs only when file is executed directly
Robot and greet_user	Called inside main() after being imported
📌 Key Concepts Demonstrated

    Module import from another file

    Using class and function across files

    Structured main() entry point

    Reusability and modular programming