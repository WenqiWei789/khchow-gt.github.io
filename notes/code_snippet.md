# TensorFlow

## Resource Management

1. Forcing TensorFlow to use CPU
```python
import os
os.environ["CUDA_DEVICE_ORDER"] = "PCI_BUS_ID"
os.environ['CUDA_VISIBLE_DEVICES'] = '-1'
```
