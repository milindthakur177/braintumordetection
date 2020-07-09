# Brain Tumor Detection Using MRI Images

The  Model aims at detecting whether a person has brain tumor or not using Radiology images. The Model is converted to tflite format for mobile deployment purpose.

## Dataset

The dataset used is from : https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection . The data is divided into training set and test set manually.

## Details

pruning.ipynb is same as braintumordetection.ipynb with pruning applied at the end to reduce size of the model.

For Extra Optimization float16 Quantization can be achieved using the following code before tflite conversion:
```
converter.optimizations = [tf.lite.Optimize.DEFAULT]
converter.target_spec.supported_types = [tf.float16]
```

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install Libraries.

```bash
pip install numpy
pip install --upgrade tensorflow
```

## Pretrained Model Used 

Densenet201

## Usage

```python
import numpy as np
import tensorflow as tf
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
