# braintumordetection
The dataset used is from : https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection
the data is divided into training set and test set manually
the model is then saved and converted into tflite format for deployment


Model used is Densenet201

float16 Quantization can be achieved using the following code before tflite conversion:

"""converter.optimizations = [tf.lite.Optimize.DEFAULT]
converter.target_spec.supported_types = [tf.float16]"""


Model is converted to tflite format for mobile deployment purpose.
