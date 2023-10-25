# PersonaNet: Person Detection using CNN

*In this Project, I will be working on an image classification task using the transfer learning technique. The task objective is to determine whether an image contains a person -- a binary classification task.*

Dataset
Dataset contains 80K images with known labels (for model development), and 20K images with unknown labels (for scoring).
Dataset has been created from a subset of COCO Dataset, and so all copyrights belong to the original authors: https://cocodataset.org/#termsofuse
Images have been rescaled and padded to be of shape (224, 224, 3).
While it's possible to create a new model architecture and train a model specifically for this task, that would be expensive in terms of time and cloud resources. Instead, in this project, I will be re-using an pre-trained model's architecture and parameters to save time and cloud resources.

MobileNet Architecture
The pre-trained model's name is MobileNetV2: https://arxiv.org/pdf/1801.04381.pdf
MobileNet is a relatively small network that is designed for usage on mobile devices with limited compute and storage resource.
It's a great choice for this assignment, since this network can be relatively quickly processed with a single GPU.
MobileNet Parameters
Keras provides network architecture and pre-trained parameters: https://keras.io/api/applications/mobilenet/#mobilenetv2-function
The pre-trained parameters come from the ImageNet 1000-class task, which does not include a person label.
The lower part of the network can be reused due to the shared hierarchy of visual information..
