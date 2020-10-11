# TensorFlow

## Resource Management

1. Force TensorFlow to use CPU
```python
import os
os.environ["CUDA_DEVICE_ORDER"] = "PCI_BUS_ID"
os.environ['CUDA_VISIBLE_DEVICES'] = '-1'
```

2. Specify the fraction of GPU memory
```python
# TensorFlow
import tensorflow as tf
config = tf.ConfigProto()
config.gpu_options.per_process_gpu_memory_fraction = 0.4
sess = tf.Session(config=config) as sess:
```

```python
# Keras with TensorFlow backend
import tensorflow as tf
from keras.backend.tensorflow_backend import set_session
config = tf.ConfigProto()
config.gpu_options.per_process_gpu_memory_fraction = 0.4
set_session(tf.Session(config=config))
```

# Google Colaboratory

1. Get high memory machines
```python
d=[]
while(1):
  d.append('1')
```

2. Specify TensorFlow version 1.x
```python
%tensorflow_version 1.x
```

3. Auto-click
```js
function ClickConnect(){
console.log("Working"); 
document.querySelector("colab-toolbar-button").click() 
}setInterval(ClickConnect,60000)
```

# Ubuntu

## Scripts

1. Run multiple Python scripts sequentially
```bash
python script_1.py && python script_2.py && python script_3.py 
```

2. ImportError: bad magic number
```bash
find . -name \*.pyc -delete
```

# CloudLab c4130 Configuration

1. Install ubuntu-drivers
```bash
sudo apt update
sudo apt install ubuntu-drivers-common
```

2. Disable Nouveau NVIDIA driver
```bash
sudo vi /etc/modprobe.d/blacklist-nouveau.conf
```
```bash
blacklist nouveau
blacklist lbm-nouveau
options nouveau modeset=0
alias nouveau off
alias lbm-nouveau off
```
```bash
echo options nouveau modeset=0 | sudo tee -a /etc/modprobe.d/nouveau-kms.conf
```

3. Install NIVIDA drivers (check the recommended driver version with `ubuntu-drivers devices` and reboot
```bash
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt install nvidia-driver-435
```

4. Confirm installed hardware and the NIVIDA drivers
```bash
nvidia-smi
```

5. Mount a driver
```bash
sudo mkdir /data
sudo /usr/local/etc/emulab/mkextrafs.pl /data
sudo chmod ugo+rwx /data
```

6. Install kernel headers and packages
```bash
sudo apt-get install linux-headers-$(uname -r)
```

7. Install CUDA 10.0 (DO NOT install drivers again)
```bash
wget https://developer.nvidia.com/compute/cuda/10.0/Prod/local_installers/cuda_10.0.130_410.48_linux
sudo sh cuda_10.0.130_410.48_linux
```

8. Download cuDNN from [https://developer.nvidia.com/rdp/form/cudnn-download-survey](https://developer.nvidia.com/rdp/form/cudnn-download-survey)
* cuDNN Library - 7.4.2.24-1+cuda10.0
* cuDNN Runtime Library (Deb) - 7.4.2.24-1+cuda10.0
* cuDNN Developer Library (Deb) - 7.4.2.24-1+cuda10.0
* cuDNN Code Samples (Deb) - 7.4.2.24-1+cuda10.0
```bash
tar -zxvf cudnn-10.1-linux-x64-v7.6.5.32.tgz
sudo cp cuda/include/cudnn.h /usr/local/cuda/include
sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64
sudo chmod a+r /usr/local/cuda/include/cudnn.h /usr/local/cuda/lib64/libcudnn*
sudo dpkg -i libcudnn7_7.6.5.32–1+cuda10.1_amd64.deb
sudo dpkg -i libcudnn7-dev_7.6.5.32-1+cuda10.1_amd64.deb
sudo dpkg -i libcudnn7-doc_7.6.5.32-1+cuda10.1_amd64.deb
```

9. Update PATHs
```bash
export PATH=/usr/local/cuda-10.0/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-10.0/lib64
export export LIBRARY_PATH=$LIBRARY_PATH:/usr/local/cuda-10.0/lib64
```

10. Verify GPU installation
```bash
cp -r /usr/src/cudnn_samples_v7/ $HOME
cd  $HOME/cudnn_samples_v7/mnistCUDNN
make clean && make
./mnistCUDNN
```
