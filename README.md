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


