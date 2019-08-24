# Miscellaneous
Just something random...

## Install Ubuntu 18.04 on Alienware Aurora R8 with Dual Boot (Windows 10)
### Machine Spec
* Processor: Intel Core i7-9700K CPU @ 3.60GHz x 8
* Graphics: GeForce RTX 2080 SUPER/PCIe/SSE2
* Memory: 32 GB
* HDD: 1 TB
* SSD: 512 GB
### Installation
The following steps install Ubuntu 18.04 on the HDD and allow dual boot with Windows 10 pre-installed on the SSD.
1. Use whatever you like to make a bootable Ubuntu USB drive
2. Disable secure boot in BIOS (Click F2 when you start your PC)
3. [IMPORTANT] Detach the GPU from the motherboard
4. [IMPORTANT] Connect the monitor to the on-board displayport
5. Boot the PC with the USB drive by clicking F12
6. Install Ubuntu 18.04
7. After installation restart, your PC gets stuck in a loading page. Click Alt+Ctrl+F2 to enter command mode.
8. Login and install CUDA, NVIDIA drive with the following commands suggested from TensorFlow [[Source]](https://www.tensorflow.org/install/gpu)
```
# Add NVIDIA package repositories
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.0.130-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu1804_10.0.130-1_amd64.deb
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
sudo apt-get update
wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
sudo apt install ./nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
sudo apt-get update

# Install NVIDIA driver
sudo apt-get install --no-install-recommends nvidia-driver-418
# Reboot. Check that GPUs are visible using the command: nvidia-smi

# Install development and runtime libraries (~4GB)
sudo apt-get install --no-install-recommends \
    cuda-10-0 \
    libcudnn7=7.6.0.64-1+cuda10.0  \
    libcudnn7-dev=7.6.0.64-1+cuda10.0


# Install TensorRT. Requires that libcudnn7 is installed above.
sudo apt-get update \
    && sudo apt-get install -y --no-install-recommends libnvinfer5=5.1.5-1+cuda10.0 \
    && sudo apt-get install -y --no-install-recommends libnvinfer-dev=5.1.5-1+cuda10.0

```
9. Restart your PC and install again the GPU
10. Done

Reminder: DO NOT blindly install the latest version of CUDA and NVIDIA driver. Tensorflow does not support the latest version of CUDA (10.1). You must follow the above steps to install CUDA 10.0.

Also, there is a bug in using RTX graphic cards in TensorFlow. You need to allow growth all the time to enable CuDNN.

## Create WhatsApp Desktop App on Ubuntu 18.04  [[Source]](https://askubuntu.com/a/1144265)
1. Type in the terminal: `sudo -H gedit /usr/share/applications/whatsapp-webapp.desktop`
2. Copy and paste the following script to the opened file
```
#!/usr/bin/env xdg-open
[Desktop Entry]
Name=WhatsApp
GenericName=WhatsApp
Comment=WhatsApp desktop webapp
#Exec=webapp-container --store-session-cookies --webappUrlPatterns=https?://*.whatsapp.com/* --user-agent-string='Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.36' https://web.whatsapp.com %u
Exec=/opt/google/chrome/google-chrome --app=https://web.whatsapp.com/
Terminal=false
Type=Application
StartupNotify=true
MimeType=text/plain;
# If you want icon, type path of icon
# Icon=
Categories=Network;Application;
Keywords=WhatsApp;webapp;
X-Ubuntu-Gettext-Domain=WhatsApp
StartupWMClass=web.whatsapp.com
```
