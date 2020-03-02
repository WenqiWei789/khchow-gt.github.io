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

# Ubuntu

## Scripts

1. Run multiple Python scripts sequentially
```bash
python script_1.py && python script_2.py && python script_3.py 
```
